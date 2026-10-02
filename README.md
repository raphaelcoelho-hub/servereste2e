# servereste2e

# Case ServeRest - Automação e Qualidade de Software (QA Portfolio)

> **Projeto em andamento / em construção**
>
> Este repositório está sendo construído ativamente como parte de um portfólio prático de QA. Novas funcionalidades, cenários de teste e códigos de automação são adicionados regularmente.

## Sobre o Projeto

Repositório dedicado à demonstração de competências em **Quality Assurance (QA)**, abrangendo:

* Testes manuais exploratórios
* Planejamento de cenários de teste
* Automação de testes E2E com Cypress
* Testes de API
* Validações de banco de dados
* Documentação técnica
* Estratégia de testes

O projeto tem como alvo a aplicação **ServeRest**, uma API e interface de e-commerce voltada para testes de software.

O objetivo é aplicar uma estratégia de **Quality Assurance de ponta a ponta**, cobrindo diferentes etapas do ciclo de vida da qualidade e da documentação técnica.

---

## Escopo e Limitações do Projeto

### Módulos Validados (In-Scope)

| Módulo               | Descrição                                          |
| -------------------- | -------------------------------------------------- |
| Autenticação (Login) | Geração de token JWT e validação de credenciais    |
| Cadastro de Usuários | Regras de negócio, unicidade de e-mail e perfis    |
| Produtos             | Gestão completa do catálogo de itens               |
| Carrinho de Compras  | Adição de produtos e validação de itens vinculados |

### Limitações Conhecidas (Out of Scope)

#### Checkout / Pagamento

A funcionalidade de finalização de compra e fechamento de pedido encontra-se atualmente em construção no ambiente simulado do ServeRest.

Por esse motivo, os testes de ponta a ponta (E2E) focados estritamente na transação final de pagamento estão explicitamente excluídos deste escopo e são tratados como uma **limitação conhecida da aplicação simulada**.

---

## Tecnologias e Ferramentas Utilizadas

| Tecnologia/Ferramenta | Utilização                               |
| --------------------- | ---------------------------------------- |
| JavaScript            | Linguagem utilizada no projeto           |
| Node.js               | Ambiente de execução                     |
| Cypress               | Automação de testes E2E e API            |
| Postman               | Testes de API manuais                    |
| SQL                   | Consultas e validações de banco de dados |
| Git                   | Controle de versão                       |
| GitHub                | Hospedagem do repositório                |
| VS Code               | Ambiente de desenvolvimento              |

---

## Pré-requisitos e Instalação

Para executar este projeto e a aplicação alvo (ServeRest) localmente, é necessário ter instalado:

* [Node.js](https://nodejs.org/) — versão LTS recomendada
* [Git](https://git-scm.com/)

---

## Clonando o Repositório

Clone este repositório utilizando:

```bash
git clone https://github.com/raphaelcoelho-hub/qa-portfolio-serverest.git
```

Em seguida, acesse a pasta do projeto:

```bash
cd qa-portfolio-serverest
```

---

## Configuração e Execução

### Instalação das Dependências

Instale as dependências do projeto:

```bash
npm install
```

### Execução da Aplicação ServeRest

Execute a aplicação ServeRest localmente utilizando:

```bash
npx serverest
```

O servidor será iniciado em:

http://localhost:3000

---

## Estrutura do Repositório

```text
qa-portfolio-serverest/
├── case-serverest-qa/
│   ├── docs/
│   │   ├── bug-reports.md
│   │   ├── test-estrategy.md
│   │   └── test-scenarios.md
│   └── feature/
├── cypress/
│   ├── e2e/
│   ├── fixtures/
│   │   └── example.json
│   └── support/
│       ├── commands.js
│       └── e2e.js
├── node_modules/
├── cypress.config.js
├── package-lock.json
├── package.json
└── README.md
```

---

## Backlog e Planejamento de Execução

O projeto é gerenciado com base nas seguintes entregas (User Stories) e marcos de qualidade:

| ID    | Épico / Módulo              | Tarefa / User Story (US)                                       | Status    |
| ----- | --------------------------- | -------------------------------------------------------------- | --------- |
| US-01 | Configuração e Planejamento | Setup do Ambiente Local ServeRest                              | Concluído |
| US-02 | Configuração e Planejamento | Documento de Estratégia, Requisitos e Mapeamento de Cenários   | Concluído |
| US-03 | Qualidade Manual e Defeitos | Execução de Testes Manuais (Exploratórios) e Relatório de Bugs | A Fazer   |
| US-04 | Testes de API e Dados       | Criação de Validações de API e Contrato no Postman             | A Fazer   |
| US-05 | Testes de API e Dados       | Validação e Investigação de Persistência via SQL               | A Fazer   |
| US-06 | Automação e CI/CD           | Automação de Fluxos Críticos com Cypress (UI + API)            | A Fazer   |
| US-07 | Automação e CI/CD           | Configuração de Pipeline de CI/CD (GitHub Actions)             | A Fazer   |

---

## Autor

Desenvolvido por **Raphael D' Assunção Coelho** como parte do portfólio de evolução profissional em QA.

Case prático de QA cobrindo:

* Testes manuais
* Estratégia de testes
* Testes de API
* SQL
* Automação com Cypress
* ServeRest
* Documentação técnica
* Práticas de qualidade de software
