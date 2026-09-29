# Matriz de Cenários de Testes - ServeRest

Este documento detalha os cenários de testes planejados (Manuais e Automatizados) para a aplicação ServeRest, cobrindo os fluxos críticos de negócio, validações de interface, regras de API e comportamentos de borda.

##  Legenda de Tipos
* **POS:** Positivo (Caminho feliz)
* **NEG:** Negativo (Validação de erros e bloqueios)
* **BOR:** Borda (Limites de caracteres, valores zerados ou extremos)

---

## 1. Módulo: Autenticação (Login)
| ID | Cenário | Tipo | Resultado Esperado |
| :--- | :--- | :---: | :--- |
| CT-LOG-01 | Realizar login com e-mail e senha válidos | POS | Acesso permitido, redirecionamento para o painel e token JWT gerado. |
| CT-LOG-02 | Tentar login com e-mail não cadastrado | NEG | Mensagem de erro informando que e-mail/senha são inválidos. |
| CT-LOG-03 | Tentar login com senha incorreta para e-mail válido | NEG | Mensagem de erro informando credenciais inválidas. |
| CT-LOG-04 | Tentar login com campos de e-mail e senha vazios | NEG | Validação de campos obrigatórios impedindo o envio. |

---

## 2. Módulo: Cadastro de Usuários
| ID | Cenário | Tipo | Resultado Esperado |
| :--- | :--- | :---: | :--- |
| CT-USR-01 | Cadastrar novo usuário com dados válidos | POS | Usuário cadastrado com sucesso e mensagem de confirmação exibida. |
| CT-USR-02 | Tentar cadastrar usuário com e-mail já existente | NEG | Sistema bloqueia o cadastro e retorna mensagem de e-mail já em uso. |
| CT-USR-03 | Cadastrar usuário marcando o perfil de administrador | POS | Usuário criado com permissões administrativas ativas. |
| CT-USR-04 | Enviar formulário de cadastro com formato de e-mail inválido | NEG | Validação de formato de e-mail impede o cadastro. |

---

## 3. Módulo: Gestão de Produtos (Admin)
| ID | Cenário | Tipo | Resultado Esperado |
| :--- | :--- | :---: | :--- |
| CT-PRD-01 | Cadastrar produto com todos os campos válidos | POS | Produto cadastrado e listado corretamente no catálogo. |
| CT-PRD-02 | Tentar cadastrar produto com preço zerado ou negativo | BOR | Sistema deve impedir o cadastro ou validar valor mínimo. |
| CT-PRD-03 | Tentar cadastrar produto com estoque negativo | BOR | Validação de campo impede números negativos no estoque. |
| CT-PRD-04 | Cadastrar produto com nome duplicado | NEG | Mensagem de alerta informando que já existe produto com esse nome. |

---

## 4. Módulo: Carrinho e Compra (Checkout)
| ID | Cenário | Tipo | Resultado Esperado |
| :--- | :--- | :---: | :--- |
| CT-CAR-01 | Adicionar produto disponível ao carrinho | POS | Produto adicionado, quantidade incrementada e valor atualizado. |
| CT-CAR-02 | Tentar comprar quantidade superior ao estoque disponível | NEG | Sistema barra a operação informando insuficiência de estoque. |
| CT-CAR-03 | Esvaziar o carrinho de compras | POS | Carrinho fica limpo e botões de checkout são desabilitados. |
| CT-CAR-04 | Concluir a compra (Concluir pedido) com sucesso | POS | Pedido registrado no sistema, baixa automática no estoque correspondente. |
