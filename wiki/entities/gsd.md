---
title: "GSD (Get Shit Done)"
type: entity
category: tool
tags: [claude-code, agentes-ia, automação, context-engineering, open-source]
source_count: 2
last_updated: 2026-08-26
---

# GSD (Get Shit Done)

> **Categoria:** Skill/framework open-source de "spec-driven development" · **Repositório:** `github.com/open-gsd/gsd-core` · **Instalação:** `npx get-shit-done-cc --claude --global`

## O que é

Framework que estrutura a construção de software com Claude Code como um loop de 5 fases, cada uma com comando dedicado, desenhado para sobreviver a sessões longas sem perder contexto ("the loop does the remembering"):

| Fase | Comando | O que faz |
|------|---------|-----------|
| 1. Discuss | `/gsd-discuss-phase` | Captura decisões primeiro |
| 2. Plan | `/gsd-plan-phase` | Gera arquivos de tarefa atômicos e verificados |
| 3. Execute | `/gsd-execute-phase` | Sub-agentes frescos em paralelo executam as tarefas |
| 4. Verify | `/gsd-verify-work` | Revisa o que foi construído |
| 5. Ship | `/gsd-ship` | Abre PR automaticamente |

## Números

- **64.642 estrelas**

## Histórico no wiki

Primeira aparição via [[nate-herk]], como item 3 de uma stack de 6 skills (citado apenas como "context engineering: sub-agentes frescos por tarefa + quality gates automáticos"). Esta fonte é a primeira a detalhar a mecânica interna completa (as 5 fases e seus comandos exatos).

## Conexões no wiki

- [[claude-code]] — ambiente de execução
- [[agentes-ia]] — sub-agentes frescos por tarefa como padrão de context engineering
- [[otimização-de-tokens]] — custo em tokens aceito para eliminar retrabalho por context rot
- [[nate-herk]] — primeira menção no wiki

## Fontes

- [[2026-05-03_nate-herk-6-habilidades-claude-code]]
- [[2026-08-26_neeraj-chemburkar-10-skills-claude]]
