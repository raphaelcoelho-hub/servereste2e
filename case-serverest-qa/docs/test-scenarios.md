# Matriz de Cenários de Testes - ServeRest

Este documento detalha os cenários de testes planejados (Manuais e Automatizados) para a aplicação ServeRest, cobrindo os fluxos críticos de negócio, validações de interface, regras de API e comportamentos de borda.

##  Legenda de Tipos
* **POS:** Positivo (Caminho feliz)
* **NEG:** Negativo (Validação de erros e bloqueios)
* **BOR:** Borda (Limites de caracteres, valores zerados ou extremos)

---

### 1. Módulo: Cadastro de Usuários

| ID | Cenário | Tipo | Camada | Resultado Esperado | Resultado obtido |
| :--- | :--- | :---: | :---: | :--- |
| CT-USR-01 | Realizar cadastro de um novo usuário com dados válidos | POS | **API / BD** | Status 201, mensagem "Cadastro realizado com sucesso", retorno do `_id` e registro persistido no banco. |
| CT-USR-02 | Tentar cadastrar usuário utilizando e-mail já existente | NEG | **API / BD** | Status 400, mensagem informando que o e-mail já está em uso e garantia de que não houve duplicação no banco. |
| CT-USR-03 | Tentar cadastrar usuário omitindo campo obrigatório (ex: senha) | NEG | **API** | Status 400 e mensagem da API indicando a obrigatoriedade do campo ausente. |
| CT-USR-04 | Tentar cadastrar usuário com formato de e-mail inválido | NEG | **API** | Status 400 e mensagem de validação de formato de e-mail retornada pelo servidor. |
| CT-USR-05 | Preencher formulário de cadastro com dados válidos e submeter | POS | **Interface** | Exibição de mensagem visual de sucesso na tela e redirecionamento para a tela de login. |
| CT-USR-06 | Tentar submeter o formulário de cadastro com campos em branco | NEG | **Interface** | Validação visual na tela ou mensagens de erro bloqueando o envio do formulário. |
| CT-USR-07 | Interagir com a opção de perfil de administrador na tela | POS | **Interface** | Alternância correta do estado da seleção garantindo o envio do parâmetro correspondente. |

## 2. Módulo: Autenticação (Login)
| ID | Cenário | Tipo | Resultado Esperado | Resultado obtido |
| :--- | :--- | :---: | :--- |
| CT-LOG-01 | Realizar login com e-mail e senha válidos | POS | Acesso permitido, redirecionamento para o painel e token JWT gerado. |
| CT-LOG-02 | Tentar login com e-mail não cadastrado | NEG | Mensagem de erro informando que e-mail/senha são inválidos. |
| CT-LOG-03 | Tentar login com senha incorreta para e-mail válido | NEG | Mensagem de erro informando credenciais inválidas. |
| CT-LOG-04 | Tentar login com campos de e-mail e senha vazios | NEG | Validação de campos obrigatórios impedindo o envio. |

---

## 3. Módulo: Gestão de Produtos (Admin)
| ID | Cenário | Tipo | Resultado Esperado | Resultado obtido |
| :--- | :--- | :---: | :--- |
| CT-PRD-01 | Cadastrar produto com todos os campos válidos | POS | Produto cadastrado e listado corretamente no catálogo. |
| CT-PRD-02 | Tentar cadastrar produto com preço zerado ou negativo | BOR | Sistema deve impedir o cadastro ou validar valor mínimo. |
| CT-PRD-03 | Tentar cadastrar produto com estoque negativo | BOR | Validação de campo impede números negativos no estoque. |
| CT-PRD-04 | Cadastrar produto com nome duplicado | NEG | Mensagem de alerta informando que já existe produto com esse nome. |

---

## 4. Módulo: Carrinho e Compra (Checkout)
| ID | Cenário | Tipo | Resultado Esperado | Resultado obtido |
| :--- | :--- | :---: | :--- |
| CT-CAR-01 | Adicionar produto disponível ao carrinho | POS | Produto adicionado, quantidade incrementada e valor atualizado. |
| CT-CAR-02 | Tentar comprar quantidade superior ao estoque disponível | NEG | Sistema barra a operação informando insuficiência de estoque. |
| CT-CAR-03 | Esvaziar o carrinho de compras | POS | Carrinho fica limpo e botões de checkout são desabilitados. |
| CT-CAR-04 | Concluir a compra (Concluir pedido) com sucesso | POS | Pedido registrado no sistema, baixa automática no estoque correspondente. |
