---
title: "7 Subagentes Paralelos para Limpar Código Gerado por IA"
type: source
source_file: "2026-04-16_artificial_intelligence_l_business_DXMre9XFNCh.md"
author: "@Artificial Intelligence l Business"
date: 2026-04-16
format: carousel
tags: [claude-code, agentes-ia, desenvolvimento-software, qualidade-de-codigo, subagentes]
source_url: "https://www.instagram.com/p/DXMre9XFNCh/?img_index=10&igsh=MzRnbXpzbjlpNmI1"
source_count: 1
---

# 7 Subagentes Paralelos para Limpar Código Gerado por IA

> **Fonte:** [[2026-04-16_artificial_intelligence_l_business_DXMre9XFNCh]] | **Autor:** @Artificial Intelligence l Business | **Data:** 2026-04-16 | **Formato:** Carousel (10/11 slides processados) | **[↗ Ver post](https://www.instagram.com/p/DXMre9XFNCh/?img_index=10&igsh=MzRnbXpzbjlpNmI1)**

## TL;DR

Um único prompt lança 7 subagentes paralelos no Claude/Codex para auditar e limpar código gerado por IA ("vibe-coded slop") — cada subagente é especialista em uma dimensão da qualidade: deduplicação, tipos, código morto, dependências circulares, type strengthening, error handling e remoção de artefatos de IA.

## Contexto

Conta @Artificial Intelligence l Business (repost de @thewizeai) apresenta o problema de código gerado em "one-shot" por IA: dependências circulares, tipos fracos (`any`, `unknown`), dead code e lógica falha. A solução é orquestração multi-agent com o loop: Research → Critical Assessment → Implementation.

## O que foi ensinado

### O Prompt Master (cola no Claude ou Codex)
> "I want to clean up my codebase and improve code quality through a careful, low-risk cleanup pass. Work in 7 focused tracks. For each track: inspect the code, write a critical assessment, rank changes by confidence, implement ONLY high-confidence low-risk fixes, then run all checks after."

### Os 7 Subagentes

**Subagente 1 — Deduplicação**
- Varrer o codebase por lógica repetida, funções copiadas e abstrações redundantes
- Consolidar onde reduz complexidade sem obscurecer intenção
- Aplicar DRY apenas onde genuinamente simplifica

**Subagente 2 — Consolidação de Tipos**
- Encontrar definições de tipos espalhadas entre arquivos
- Consolidar as que devem ser compartilhadas
- Merge em single source of truth

**Subagente 3 — Remoção de Código Morto**
- Usar knip para encontrar exportações não usadas, funções não referenciadas, arquivos órfãos
- Verificar manualmente antes de remover (imports dinâmicos, convenções de framework)
- Remover APENAS o que for código morto confirmado

**Subagente 4 — Dependências Circulares**
- Usar madge para mapear o grafo de dependências
- Identificar importações circulares que impactam manutenibilidade ou testabilidade
- Desatar extraindo lógica compartilhada em módulos neutros

**Subagente 5 — Type Strengthening**
- Encontrar todo `any`, `unknown` e tipos fracos deixados pela IA
- Pesquisar os tipos reais no codebase, packages relacionados e uso em runtime
- Substituir por tipos fortes, executar type checks após cada batch

**Subagente 6 — Error Handling Cleanup**
- Encontrar todos os try/catch e padrões defensivos
- Remover os que engolem erros silenciosamente ou mascaram falhas com defaults
- Manter apenas error handling que serve boundary real: recovery, logging, cleanup

**Subagente 7 — Código Deprecated e AI Slop**
- Identificar e remover código legado desnecessário
- Encontrar artefatos de IA: stubs, comentários sem intenção clara
- Reescrever comentários importantes para que novos engenheiros entendam o propósito

### Resultado documentado
- Antes: code score 23% (dead code, weak types)
- Depois: code score 96% (otimizado, limpo, eficiente)

## Insights para o wiki

- "Orquestração agentiva" está emergindo como categoria própria — não é só usar Claude, é distribuir o trabalho em especialistas
- O loop Research → Critical Assessment → Implementation é aplicável a qualquer tarefa de auditoria
- Diretamente relevante para o projeto Escala AI do usuário — pode usar esse prompt para auditar o codebase atual

## Entidades relacionadas

- [[artificial-intelligence-business]] — novo autor (repost de @thewizeai)
- [[claude-code]] — ferramenta principal (Claude e Codex mencionados)

## Conceitos relacionados

- [[agentes-ia]] — arquitetura de 7 subagentes paralelos para uma tarefa
- [[desenvolvimento-de-software]] — qualidade de código gerado por IA
