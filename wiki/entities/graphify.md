---
title: "Graphify"
type: entity
category: tool
tags: [claude-code, tokens, knowledge-graph, skill, otimização, obsidian]
source_count: 1
last_updated: 2026-04-23
---

# Graphify

> **Categoria:** Ferramenta — Skill para Claude Code | **Repositório:** `/github.com/safishamsi/graphify`

## O que é

Graphify é uma skill open-source para [[claude-code]] que escaneia o workspace do usuário e constrói um **grafo de conhecimento estruturado**. Em vez de o Claude ler arquivos inteiros a cada sessão, ele consulta o grafo primeiro — reduzindo o consumo de tokens de ~20.000 para ~280 por sessão (**71,5x menos**).

Inspirado no sistema de [[andrej-karpathy]] (ex-OpenAI/Tesla). Pode ser visualizado em [[obsidian]] via "graph view".

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
