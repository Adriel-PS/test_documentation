# Documentação de Testes (Test Documentation)

Este repositório reúne padrões e templates padronizados para documentação de testes de software, servindo como guia de boas práticas para garantir qualidade, rastreabilidade e clareza na comunicação entre equipes de QA, Desenvolvimento e Produto.

---

##  Modelos Disponíveis

| Documento | Tipo de Teste | Finalidade Principal |
| :--- | :--- | :--- |
| [Teste_De_API.md](./Teste_De_API.md) | **Testes de API / Integração** | Documentar requisições (cURL), parâmetros, status codes de sucesso e erros mapeados. |
| [Teste_de_Nova_funcionalidade.md](./Teste_de_Nova_funcionalidade.md) | **Nova Funcionalidade / História** | Validar critérios de aceite, cenários de negócio, fluxo principal e impacto de regressão. |
| [Teste_Exploratorio.md](./Teste_Exploratorio.md) | **Teste Exploratório (SBTM)** | Guiar sessões de teste com missão definida (Charter), heurísticas, timebox e achados. |
| [Teste_de_correção.md](./Teste_de_correção.md) | **Correção de Bug (Reteste)** | Validar a resolução de defeitos, contrastando comportamento anterior vs. atual e efeitos colaterais. |

---

## Detalhamento dos Modelos

### 1. [Teste de API](./Teste_De_API.md)
Voltado para testes de endpoints HTTP e contratos de serviço.
- **Destaques:**
  - Comando `cURL` pronto para execução e reprodução direta em ferramentas como Postman, Insomnia ou terminal.
  - Mapeamento claro de payloads de requisição e respostas esperadas (tanto para casos de sucesso quanto para erros mapeados).
  - Contexto de autenticação, headers e base URL.

### 2. [Teste de Nova Funcionalidade](./Teste_de_Nova_funcionalidade.md)
Voltado para entregas de User Stories e novas features de produto.
- **Destaques:**
  - Rastreabilidade completa com links de tickets (Jira, Azure DevOps), protótipos (Figma) e feature flags.
  - Separação em cenários: caminho feliz, regras de validação/limites e fluxos de exceção.
  - Checklist dedicado para **testes de regressão** em módulos adjacentes.

### 3. [Teste Exploratório](./Teste_Exploratorio.md)
Baseado na metodologia *Session-Based Test Management* (SBTM).
- **Destaques:**
  - Definição de **Missão (Charter)**, escopo e tempo limite (**Timebox**).
  - Checklist de heurísticas de teste (limites, interrupções, permissões e exceções).
  - Separação entre defeitos encontrados e oportunidades de melhoria de UX/Regra de negócio.

### 4. [Teste de Correção (Bug Fix)](./Teste_de_correção.md)
Voltado para homologação e reteste de defeitos corrigidos.
- **Destaques:**
  - Vínculo direto com o ticket do bug e Pull Request / Build da correção.
  - Comparativo explícito entre o **comportamento anterior (bug)** e o **comportamento esperado (corrigido)**.
  - Verificação de impactos e regressão em áreas que compartilham o mesmo código alterado.
  - Conclusão clara: Homologado vs. Reaberto.

---

## Princípios Adotados

- **Objetividade:** Estruturas enxutas em Markdown, sem burocracia desnecessária.
- **Rastreabilidade:** Vínculo claro entre requisitos, código, testes e evidências.
- **Mentalidade de Regressão:** Preocupação constante em garantir que novas entregas ou correções não afetem funcionalidades existentes.
- **Reprodutibilidade:** Facilidade para qualquer membro do time reproduzir os cenários descritos.
