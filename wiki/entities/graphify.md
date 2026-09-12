---
title: "Graphify"
type: entity
category: tool
tags: [claude-code, tokens, knowledge-graph, skill, otimização, obsidian, y-combinator]
source_count: 2
last_updated: 2026-08-26
---

# Graphify

> **Categoria:** Ferramenta — Skill para Claude Code | **Repositório:** `/github.com/safishamsi/graphify`

## O que é

Graphify é uma skill open-source para [[claude-code]] que escaneia o workspace do usuário e constrói um **grafo de conhecimento estruturado**. Em vez de o Claude ler arquivos inteiros a cada sessão, ele consulta o grafo primeiro — reduzindo o consumo de tokens de ~20.000 para ~280 por sessão (**71,5x menos**).

Inspirado no sistema de [[andrej-karpathy]] (ex-OpenAI/Tesla). Pode ser visualizado em [[obsidian]] via "graph view".

## Confirmação e novos números (via [[neeraj-chemburkar]])

- **110.416 estrelas**
- **Apoiado pelo Y Combinator** — primeiro dado de apoio institucional documentado para esta ferramenta, não presente na fonte original
- **37 idiomas** analisados localmente
- Custo de **$0** para construir o grafo
- "10x de memorização" (métrica do próprio projeto, distinta da redução de 71,5x em tokens documentada anteriormente)

## Como funciona

```
/graphify ~/.claude
→ escaneia todos os arquivos
→ constrói o grafo de conhecimento
✔ Claude consulta o mapa, não os arquivos brutos
```

## Integração com CLAUDE.md

Padrão recomendado para instruir o Claude a usar o grafo:
```markdown
## Context Navigation
1. ALWAYS query the knowledge graph first
2. Only read raw files if I explicitly say so
```

## Impacto na otimização de tokens

| Métrica | Sem Graphify | Com Graphify |
|---------|-------------|-------------|
| Tokens/sessão | ~20.000 | ~280 |
| Redução | — | 71,5x |

## Fontes

- [[2026-04-12_graphify-memoria-infinita-claude]]
- [[2026-08-26_neeraj-chemburkar-10-skills-claude]]
