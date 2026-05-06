---
title: "Claude Skills"
type: entity
category: tool
tags: [claude, anthropic, skills, agentes-ia, prompt-engineering, marketplace]
source_count: 4
last_updated: 2026-05-06
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

## Skills para Fundadores (baseadas em [[paras-madan]])

5 skills de fonte aberta distribuídas via `varnam.tech/opendirectory`, focadas em canais de crescimento para founders:

| Skill | Canal | Destaque |
|-------|-------|---------|
| Meta Ads | Paid Ads | Agent como media buyer — CPA, audiências, relatórios da Meta API |
| Position Me | Conversão | Crawl + LIFT model + reescrita PAS + GEO checks |
| LinkedIn Post Generator | Social | Input livre → hook + arco narrativo + post publicável |
| Reddit ICP Monitor | Community | Score 1-5 por post; ≥4 dispara resposta útil sem autopromoção |
| Google Trends SEO | SEO | Breakout keywords antes do pico + outline SEO-otimizado |

→ [[2026-04-18_paras-madan-top5-skills-founders]]

## Stack oficial de automação (baseada em [[nate-herk]])

6 plugins/skills que [[nate-herk]] identifica como os que empresas reais pagam, após 400h de prática:

| # | Nome | Instalação | O que faz |
|---|------|-----------|-----------|
| 1 | **Skill Creator** | `/plugin install skill-creator@claude-plugins-official` | Fábrica de skills: descreve em linguagem natural → Claude rascunha, testa, empacota |
| 2 | **Superpowers** | `/plugin install superpowers@claude-plugins-official` | Fluxo sênior: planejar → ambiente isolado → testes → brainstorm → revisão dupla |
| 3 | **GSD** | `npx get-shit-done-cc --claude --global` | Context engineering: sub-agentes frescos por tarefa + quality gates automáticos |
| 4 | **/review & /ultra review** | Built-in (Claude Code 2.1.86+) | Revisão local rápida e revisão multi-agente em cloud com reprodução verificada |
| 5 | **Context Mode** | `/plugin marketplace add mksglu/context-mode` | Sandbox por tool call: 315 KB → 5 KB por sessão; SQLite para continuidade |
| 6 | **Claude Mem** | `/plugin marketplace add thedotmack/claude-mem` | Memória cross-session automática via SQLite + busca vetorial; 10x menos tokens |
| B | **Frontend Design** | `/plugin install frontend-design@claude-plugins-official` | UI com menos cara de IA; bônus — nativo no Claude Design (Anthropic Labs) |

→ [[2026-05-03_nate-herk-6-habilidades-claude-code]]

## Fontes

- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-22_pabloinpublic-find-skills]]
- [[2026-04-18_paras-madan-top5-skills-founders]]
- [[2026-05-03_nate-herk-6-habilidades-claude-code]]
