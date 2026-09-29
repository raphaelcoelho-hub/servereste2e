
> ⚠️ **Projeto em Andamento / Em Construção** ⚠️
> Este repositório está sendo construído ativamente como parte de um portfólio prático de QA. Novas funcionalidades, cenários de teste e códigos de automação são adicionados regularmente.

# 🧪 Case ServeRest - Automação e Qualidade de Software (QA Portfolio)

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge\&logo=javascript\&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge\&logo=node.js\&logoColor=white)](https://nodejs.org/)
[![Cypress](https://img.shields.io/badge/Cypress-17202C?style=for-the-badge\&logo=cypress\&logoColor=white)](https://www.cypress.io/)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge\&logo=postman\&logoColor=white)](https://www.postman.com/)
[![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge\&logo=mysql\&logoColor=white)](https://www.w3schools.com/sql/)
[![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge\&logo=git\&logoColor=white)](https://git-scm.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/)
[![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge\&logo=visual-studio-code\&logoColor=white)](https://code.visualstudio.com/)

Repositório dedicado à demonstração de competências em **Garantia da Qualidade (QA)**, abrangendo testes manuais exploratórios, planejamento de cenários, automação de testes E2E com Cypress, testes de API e validações de banco de dados.

---

##  Sobre o Projeto

O projeto tem como alvo a aplicação **ServeRest**, uma API e interface de e-commerce voltada para testes de software.

O objetivo é aplicar uma estratégia de **Quality Assurance de ponta a ponta**, cobrindo o ciclo de vida da qualidade e a documentação técnica.

---

##  Tecnologias e Ferramentas Utilizadas

| Tecnologia/Ferramenta | Utilização                               |
| --------------------- | ---------------------------------------- |
| **JavaScript**        | Linguagem utilizada no projeto           |
| **Node.js**           | Ambiente de execução                     |
| **Cypress**           | Automação de testes E2E e API            |
| **Postman**           | Testes de API manuais                    |
| **SQL**               | Consultas e validações de banco de dados |
| **Git**               | Controle de versão                       |
| **GitHub**            | Hospedagem do repositório                |
| **VS Code**           | Ambiente de desenvolvimento              |

---

## ⚙️ Pré-requisitos e Instalação

Para rodar este projeto e a aplicação alvo (**ServeRest**) localmente, você precisará ter instalado:

* [Node.js](https://nodejs.org/) — versão LTS recomendada
* [Git](https://git-scm.com/)

### 📥 Clonando o Repositório

Clone este repositório utilizando:

```bash
git clone https://github.com/raphaelcoelho-hub/qa-portfolio-serverest.git
```

Em seguida, acesse a pasta do projeto:

```bash
cd qa-portfolio-serverest
```

## ⚙️ Configuração e Execução

### 📦 Instalação das Dependências

Instale as dependências do projeto:

```bash
npm install
```

### 🚀 Execução da Aplicação ServeRest

Execute a aplicação ServeRest localmente utilizando:

```bash
npx serverest
```

O servidor será iniciado em:

```text
http://localhost:3000
```

---

## 📂 Estrutura do Repositório

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

O projeto é gerenciado com base nas seguintes entregas (**User Stories**) e marcos de qualidade:

| ID        | Épico / Módulo              | Tarefa / User Story (US)                                       | Status          |
| --------- | --------------------------- | -------------------------------------------------------------- | --------------- |
| **US-01** | Configuração e Planejamento | Setup do Ambiente Local ServeRest                              | ✅ Concluído     |
| **US-02** | Configuração e Planejamento | Documento de Estratégia, Requisitos e Mapeamento de Cenários   | 🔄 Em Andamento |
| **US-03** | Qualidade Manual e Defeitos | Execução de Testes Manuais (Exploratórios) e Relatório de Bugs | ⏳ A Fazer       |
| **US-04** | Testes de API e Dados       | Criação de Validações de API e Contrato no Postman             | ⏳ A Fazer       |
| **US-05** | Testes de API e Dados       | Validação e Investigação de Persistência via SQL               | ⏳ A Fazer       |
| **US-06** | Automação e CI/CD           | Automação de Fluxos Críticos com Cypress (UI + API)            | ⏳ A Fazer       |
| **US-07** | Automação e CI/CD           | Configuração de Pipeline de CI/CD (GitHub Actions)             | ⏳ A Fazer       |

---

## Autor

Desenvolvido por **Raphael D' Assunção Coelho** como parte do portfólio de evolução profissional em QA.

=======
# case-serverest-qa
Case prático de QA cobrindo testes manuais, estratégia, API, SQL e automação com Cypress na ServeRest

