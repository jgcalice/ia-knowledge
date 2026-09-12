---
title: "Claude Skills"
type: entity
category: tool
tags: [claude, anthropic, skills, agentes-ia, prompt-engineering, marketplace, design, vibecoding]
source_count: 7
last_updated: 2026-08-26
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

## Skills de design de sites (baseadas em [[vinicius-delmonego]])

3 skills que resolvem o problema de sites gerados pelo Claude com "cara de site feito por IA":

| Skill | Papel | Destaque |
|-------|-------|---------|
| Milkovalski Design | Layout | Ensina layout moderno ao Claude |
| Impeccable Design | Estilo | Tipografia e espaçamento ideais |
| Taste Skill | Inspiração | Busca referências em sites reais em vez de começar do zero |

Combinadas com os MCPs [[figma]] (montagem) e [[playwright]] (teste automatizado antes da entrega). Primeira aparição de MCPs de design/QA no wiki associados a Claude Skills.

→ [[2026-08-19_vinicius-delmonego-sites-claude]]

## Conflito de atenção entre skills concorrentes (baseada em [[fabiano-carvalho]])

Primeiro relato no wiki do **modo de falha** da composição de skills. Skill não é plugin nem modelo — é arquivo de instrução que entra no contexto quando a tarefa combina com sua descrição. Consequência: quando duas ou mais skills atacam o mesmo ponto de decisão (ex: três skills de estética visual ligadas ao mesmo tempo), elas competem pelo mesmo espaço de atenção do modelo, e qual delas "vence" muda de sessão para sessão — o resultado deixa de ser reprodutível, que é a única coisa que importa numa skill de gosto/estética.

**Catálogo verificado (10 skills, links abertos manualmente um a um; 1 fora do ar)**:

| Skill | Autor | Foco |
|-------|-------|------|
| UI/UX Pro Max | nextlevelbuilder | Layouts, tipografia, interfaces |
| Impeccable | pbakaus | Corrige interfaces "com cara de IA" feias |
| Taste Skill | Leonxlnx | Senso de design, saída menos genérica |
| Humanizer | blader | Escrita menos "cara de IA" |
| Understand Anything | Egonex-AI | Simplifica documentos/pesquisa/conceitos |
| Frontend Slides | zarazhangrui | Apresentações interativas com código |
| Diagram Design | cathrynlavery | Diagramas de fluxos/sistemas/processos |
| Stop Slop | hardikpandya | Menos enrolação, raciocínio e execução melhores |
| Awesome Design MD | VoltAgent | — |
| Design.md | google-labs-code | — |

**Protocolo de instalação incremental recomendado**: instalar uma skill → rodar uma tarefa já conhecida → comparar a saída nova com a antiga lado a lado → anotar a diferença → só então instalar a próxima. Sem essa comparação, o usuário "acha" que melhorou, mas não tem como saber.

**Ponto de partida se for instalar só uma**: quem faz interface começa por **Impeccable** ou **Taste Skill** (nunca as duas juntas); quem escreve texto começa por **Stop Slop**. Confirma, com fonte independente, os mesmos links de Impeccable e Taste Skill já citados via [[vinicius-delmonego]].

→ [[2026-09-07_skills-design-conflito-atencao]]

## Confirmação cruzada de tração via curadoria de "top repos GitHub" (baseada em [[neeraj-chemburkar]])

Fonte independente que cataloga skills como "repositórios GitHub de alta tração" (não como skills de design) confirma dois repos já catalogados acima, agora com métricas de estrelas:

| Skill | Já catalogada em | Nova confirmação |
|-------|-------------------|-------------------|
| Diagram Design (cathrynlavery) | via [[fabiano-carvalho]] | 26.758 estrelas em 4 meses — lê o site, escreve o guia de estilo, gera 39 tipos de diagrama × 3 variantes, HTML/SVG sem compilação |
| Impeccable (pbakaus) | via [[fabiano-carvalho]] e [[vinicius-delmonego]] | 62.534 estrelas — 23 comandos, 59 regras determinísticas contra "tells" de IA |

Também documenta o **[[gsd]]** (5 fases com comandos dedicados, 64.642 estrelas) — item já citado por [[nate-herk]] mas agora com a mecânica interna detalhada — e três skills/repos novos no wiki: **[[scroll-world]]** (landing page 3D, 8.581 estrelas), **[[cap]]** (Loom open-source, 21.228 estrelas) e **[[moneyprinterturbo]]** (vídeo vertical automático, 116.387 estrelas). Também cataloga **[[codex-plugin-cc]]**, plugin oficial da OpenAI que roda o Codex dentro do Claude Code — primeiro caso de integração oficial de uma lab concorrente dentro do produto da Anthropic.

→ [[2026-08-26_neeraj-chemburkar-10-skills-claude]]

## Fontes

- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-22_pabloinpublic-find-skills]]
- [[2026-04-18_paras-madan-top5-skills-founders]]
- [[2026-05-03_nate-herk-6-habilidades-claude-code]]
- [[2026-08-19_vinicius-delmonego-sites-claude]]
- [[2026-09-07_skills-design-conflito-atencao]]
- [[2026-08-26_neeraj-chemburkar-10-skills-claude]]
