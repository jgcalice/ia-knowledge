---
title: "Ruflo"
type: entity
category: tool
tags: [claude-code, agentes-ia, orquestração, open-source, roteamento, tokens]
source_count: 1
last_updated: 2026-05-07
---

# Ruflo

> **Repositório:** `ruvnet/ruflo` | **Licença:** MIT | **Stars (2026-05-03):** 38.2K | **Aparece em:** 1 fonte

## O que é

Camada de orquestração open-source que se instala sobre o [[claude-code]] via um único comando `init`. Fornece um "sistema nervoso" de mais de 100 agentes auto-organizáveis que coordenam pesquisa, codificação, testes e revisão, compartilhando memória e melhorando a cada execução.

## Funcionalidades principais

| Funcionalidade | Descrição |
|---------------|-----------|
| Roteamento automático de modelo | Lê complexidade do task → envia para modelo barato (simples) ou poderoso (complexo) |
| 100+ agentes coordenados | Auto-organização: pesquisa, código, testes, revisão em paralelo |
| Memória compartilhada | Agentes compartilham contexto; cada run torna o sistema mais inteligente |
| Instalação `init` | Um único comando configura tudo; o desenvolvedor continua usando o Claude Code normalmente |

## Resultados declarados

- Redução de até **50% nos custos de tokens**
- Extensão de até **250% no uso do Claude Code**
- Licença MIT — gratuito e open-source

## Relação com outras ferramentas

- **vs. sub-agentes nativos do Claude**: Ruflo é infraestrutura externa instalada no projeto; sub-agentes são chamados internamente pelo Claude durante a sessão (ver [[agentes-ia]])
- **vs. GSD**: ambos usam sub-agentes e memory management, mas Ruflo adiciona roteamento dinâmico por complexidade automatizado
- **vs. [[graphify]]**: Graphify foca em memória cross-session via grafo; Ruflo foca em orquestração multi-agent e roteamento de modelo

## Fontes

- [[2026-05-03_duncan-rogoff-ruflo-claude-code]]
