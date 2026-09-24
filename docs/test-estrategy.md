#  Plano de Testes e Estratégia - Case ServeRest

Este documento descreve a estratégia de qualidade, o escopo e o planejamento de testes para o projeto prático de QA utilizando a aplicação **ServeRest**.

##  1. Objetivo do Projeto
Demonstrar competências técnicas de um **Analista de QA Pleno**, cobrindo o ciclo de qualidade de ponta a ponta: desde o mapeamento de cenários e testes manuais até testes de API, validação de banco de dados e automação E2E com Cypress integrada com CI/CD.

##  2. Módulos e Escopo de Testes
O sistema será testado com foco nas seguintes entidades principais:
1. **Usuários:** Cadastro, edição, listagem e remoção de usuários comuns e administradores.
2. **Produtos:** Gestão de catálogo de produtos (criação, edição, exclusão e controle de estoque).
3. **Carrinhos:** Simulação de adição de produtos ao carrinho e fechamento de compra.
4. **Login:** Autenticação via credenciais e validação de geração de token JWT de acesso.

##  3. Tipos de Testes Aplicados
* **Testes Manuais Exploratórios:** Mapeamento de regras de negócio e busca por comportamentos inesperados.
* **Testes de API (Postman):** Validação de rotas, contratos, *Status Codes* e cenários negativos.
* **Validação de Dados (SQL / Persistência):** Auditoria da gravação correta dos dados na camada de armazenamento local.
* **Testes Automatizados E2E (Cypress):** Automação dos fluxos críticos de interface com suporte de Inteligência Artificial.
* **Pipeline de CI/CD (GitHub Actions):** Execução automatizada dos testes de regressão na nuvem.
