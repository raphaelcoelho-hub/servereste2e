# Relatório de Bugs e Anomalias - ServeRest

Este documento apresenta o modelo oficial e exemplos práticos de relatórios de defeitos (Bugs) documentados durante os testes exploratórios e funcionais da aplicação ServeRest, seguindo os padrões da indústria de garantia de qualidade.

---

## Template Padrão de Relatório de Defeito
Para cada bug encontrado, a seguinte estrutura deve ser rigorosamente seguida:

* **ID do Bug:** BUG-00X
* **Título:** [Módulo] Descrição curta e objetiva do problema
* **Severidade:** (Crítica / Alta / Média / Baixa)
* **Prioridade:** (Alta / Média / Baixa)
* **Ambiente:** (Frontend Web / API - Localhost)
* **Pré-condições:** O que precisa ter sido feito antes para testar.
* **Passo a Passo (Steps to Reproduce):**
  1. Acessar a tela X...
  2. Clicar no botão Y...
  3. Inserir o dado Z...
* **Resultado Obtido:** O que o sistema fez de errado.
* **Resultado Esperado:** O que o sistema deveria ter feito segundo a regra de negócio.
* **Evidências:** Prints de tela, logs ou requisições Postman.

---

##  Exemplo Prático Registrado no Projeto

### BUG-001: Botão de finalizar compra permanece habilitado com carrinho vazio
* **Severidade:** Média
* **Prioridade:** Média
* **Ambiente:** ServeRest Frontend (Localhost)
* **Pré-condições:** 
  - Usuário logado no sistema.
  - Carrinho de compras atualmente vazio (0 itens).

**Passo a Passo:**
1. Realizar o login com um usuário válido.
2. Navegar até a página do carrinho de compras.
3. Observar o estado do botão "Finalizar Compra" ou "Concluir Pedido".

* **Resultado Obtido:** O botão de finalizar compra permanece ativo/clicável mesmo sem nenhum produto adicionado no carrinho, permitindo avançar para uma tela de sucesso vazia.
* **Resultado Esperado:** O botão de finalizar compra deveria estar desabilitado (disabled) ou oculto quando o carrinho contiver 0 itens.
* **Evidências:** `[Inserir aqui print da tela do carrinho vazio com o botão aceso]`
