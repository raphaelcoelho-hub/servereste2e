# Plano de Testes e Estratégia - Case ServeRest

Este documento descreve a estratégia de qualidade, o escopo e o planejamento de testes para o projeto prático de QA utilizando a aplicação **ServeRest**.

## 1. Objetivo do Projeto
Demonstrar competências técnicas de um **Analista de QA**, cobrindo o ciclo de qualidade: desde o mapeamento de cenários e testes manuais até testes de API, validação de persistência e simulação de automação E2E.

## 2. Módulos e Escopo de Testes

### 🟢 Módulos Incluídos (In-Scope)
O sistema será testado com foco nas seguintes entidades principais:
1. **Usuários:** Cadastro, edição, listagem e remoção de usuários comuns e administradores.
2. **Produtos:** Gestão de catálogo de produtos (criação, edição, exclusão e controle de estoque).
3. **Carrinhos:** Simulação de adição de produtos ao carrinho.
4. **Login:** Autenticação via credenciais e validação de geração de token JWT de acesso.

### 🔴 Fora do Escopo / Limitações Conhecidas (Out of Scope)
* **Fluxo de Checkout / Pagamento:** A funcionalidade de finalização de compra e fechamento de pedido encontra-se atualmente em construção no ambiente simulado do ServeRest. Portanto, os testes E2E focados estritamente na transação final de pagamento estão excluídos deste escopo.

## 3. Tipos de Testes Aplicados
- **Testes Manuais Exploratórios:** Mapeamento de regras de negócio e busca por comportamentos inesperados.
- **Testes de API:** Validação de rotas, contratos, *Status Codes* e cenários negativos.
- **Validação de Dados (Persistência):** Auditoria da gravação correta dos dados na camada de armazenamento.
- **Testes Automatizados (E2E / Camada de Interface):** Abordagem voltada à validação dos fluxos críticos de tela.
- **Estruturação de CI/CD (GitHub Actions):** Configuração conceitual/prática voltada para portfólio, demonstrando o entendimento de integração contínua e execução automatizada de regressão na nuvem.