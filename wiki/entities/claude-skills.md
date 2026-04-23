---
title: "Claude Skills"
type: entity
category: tool
tags: [claude, anthropic, skills, agentes-ia, prompt-engineering, marketplace]
source_count: 2
last_updated: 2026-04-23
---

# Claude Skills

> **Categoria:** Feature nativa da Anthropic · **Propósito:** Pacotes nomeados de comportamento ativáveis por frase-gatilho ou tag

## O que é

**Claude Skills** são pacotes de comportamento distribuíveis que alteram a forma como o modelo responde a partir de uma frase-gatilho ou `Search Tag` reconhecida. Funcionam como uma evolução industrial da ideia de "palavra-gatilho" documentada por [[adriano-couto]]: aqui cada skill tem nome, escopo, frases de ativação formais e pode ser compartilhada publicamente.

## Estrutura canônica (baseada em [[aashish-pahwa]])

- **Nome da skill** — identificação única (ex: `Feature Forge`)
- **Quando usar** — contexto de ativação
- **Frases-gatilho** — ex: "define this feature", "write a spec for..."
- **Search Tag** — categoria para descoberta (`planning`, `discovery`, `APIs`, etc.)
- **Output esperado** — formato estruturado (spec, diagrama, lista)

## Skills documentadas no wiki

Catalogadas via [[2026-04-07_claude-skills-product-managers]]:

| Skill | Tag | Caso de uso |
|-------|-----|-------------|
| Feature Forge | `planning` | Spec completa antes de codar |
| Spec Miner | `discovery` | Engenharia reversa de produto existente |
| The Fool | `critical thinking` | Stress test de decisão (red team, pre-mortem) |
| Architecture Designer | `system design` | Design de sistemas com trade-offs e diagramas |
| API Designer | `APIs` | Endpoints, modelos de dados, OpenAPI |
| Microservice Architect | `distributed systems` | Decomposição em serviços independentes |

## Meta-skill de descoberta: find-skills

Com o ecossistema em escala de centenas de milhares de skills, o problema virou **descoberta**. [[pablo-in-public]] documenta a solução: `find-skills` (Vercel Labs) — uma skill que busca entre todas as outras usando linguagem natural dentro do Claude Code.

**Instalação:**
```
npx skills add https://github.com/vercel-labs/skills --skill find-skills
```
**Uso:** dentro do Claude Code, perguntar: "há alguma skill boa para [objetivo]?" → recebe a coincidência mais relevante.

→ [[2026-04-22_pabloinpublic-find-skills]]

## Marketplaces

- **[[smithery]]** — 128.624 skills catalogadas (escala de referência)
- `jeffallan.github.io/claude-skills/skills-guide/`
- `BehiSecc/awesome-clause-skills/`

## Conexões no wiki

- [[claude-code]] — ambiente em que as skills rodam
- [[agentes-ia]] — cada skill é um micro-agente especializado
- [[prompt-engineering]] — formalização do padrão "palavra-gatilho"
- [[adriano-couto]] — precursor artesanal (MECE, 5 Whys como gatilhos antes de virarem skills)

## Fontes

- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-22_pabloinpublic-find-skills]]
