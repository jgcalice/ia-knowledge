---
title: "11 Prompts para Aumentar a Produtividade em Engenharia de Software com Claude"
type: source
source_file: "2026-05-25_harish_bhatt_DYwv5Adkuc5.md"
author: "@Harish Bhatt (@codingknowledge)"
date: 2026-05-25
format: carousel
tags: [prompt-engineering, engenharia-de-software, claude, produtividade, arquitetura, debugging, performance]
source_url: "https://www.instagram.com/p/DYwv5Adkuc5/?img_index=12"
source_count: 1
---

# 11 Prompts para Aumentar a Produtividade em Engenharia de Software com Claude

> **Fonte:** [[2026-05-25_harish_bhatt_DYwv5Adkuc5]] | **Autor:** @Harish Bhatt (@codingknowledge) | **Data:** 2026-05-25 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DYwv5Adkuc5/?img_index=12)**

## TL;DR

Pare de pedir ao Claude para "escrever o código" — trate-o como um engenheiro sênior de $1B e use prompts estruturados que convocam arquitetura, debugging, otimização e liderança técnica de nível profissional.

## Contexto

@Harish Bhatt (@codingknowledge) — já documentado no wiki com posts sobre repos open-source — publica aqui um ângulo completamente diferente: **Claude como parceiro de engenharia sênior**. O gancho do post é direto: "Stop telling Claude 'write the code, find the bug, make this work' — you're treating a billion-dollar AI engineer like a confused junior intern." O foco é em prompts que convocam papéis completos de engenharia, não comandos pontuais.

## O que foi ensinado

Os 11 prompts (10 documentados nos slides processados) são organizados por papel convocado:

| # | Papel | Entregável principal |
|---|-------|----------------------|
| 1 | Full startup engineering team | System architecture + file structure + DB schema + API endpoints + UI + production-ready code |
| 2 | Senior engineer auditando codebase desconhecido | Reverse-engineered architecture + lista de problemas + refactoring strategies + código melhorado |
| 3 | Production-level debugging monster | Root cause analysis + failure explanation + edge case analysis + código corrigido |
| 4 | Performance optimization engineer | Bottlenecks + lógica ineficiente + renderização + memory leaks + código otimizado |
| 5 | Architect reconstruindo código legado | Nova folder structure + clean architecture breakdown + código refatorado + explicação das melhorias |
| 6 | Senior systems architect (startup backend) | System architecture + API design + DB schema + caching strategy + implementação mínima escalável |
| 7 | 4-agent AI engineering team | Architect (design) → Engineer (build) → Reviewer (senior review) → Optimizer (production finish) |
| 8 | Senior frontend engineer | Reusable UI components + accessible interfaces + loading/empty/edge states + usage examples |
| 9 | AI Technical Lead | Clarifying questions + challenge bad decisions + scalability risks + 5-year maintainability thinking |

**Padrão recorrente em todos os prompts:**
- Abertura: `"Act like a senior [papel específico]"` — convoca o perfil completo sem descrever cada comportamento
- Missão: instrução explícita do problema ou codebase a tratar
- Constraint invariável: `"Do not change functionality. Only upgrade [qualidade/arquitetura/performance]."`
- Entregável estruturado: lista de bullet points com o que deve ser fornecido
- Fecho: `"Build it like it's going into a real production app used by millions."` / `"Think deeply before making changes."`

**Prompt 7 — 4-agent team** é o mais sofisticado: instrui o Claude a simular quatro papéis em sequência dentro de um único prompt, cada um criticando e melhorando o output do anterior — Architect → Engineer → Reviewer → Optimizer. Equivalente a fazer code review multi-perspectiva em uma única chamada.

**Prompt 9 — AI Technical Lead Mode** é o mais operacional: antes de escrever código, o Claude deve fazer perguntas clarificadoras, desafiar decisões ruins, identificar riscos de escalabilidade e sugerir abordagens melhores — pensando como se fosse manter o produto por 5 anos.

## Insights para o wiki

- **3ª contribuição de [[harish-bhatt]]**: ângulo completamente diferente das duas anteriores (repos open-source). Aqui o foco é Claude como ferramenta de engenharia, não como base para produto SaaS.
- **Extensão do padrão "Act like a senior X"**: confirma e expande o padrão [[Persona Mode e Output Constraints]] documentado em [[2026-04-16_yik-chan-100-recursos-ocultos-claude]]. Aqui o padrão é aplicado exaustivamente a engenharia de software, com deliverables estruturados em cada variante.
- **Simulação de equipe de engenharia em um único prompt (Prompt 7)**: o 4-agent team (Architect → Engineer → Reviewer → Optimizer) é uma técnica de auto-revisão multi-perspectiva — o Claude passa pelas 4 lentes sem precisar de orquestração externa. Conecta-se ao conceito de [[agentes-ia]], mas implementado via instrução de papel, não via sub-agentes reais.
- **AI Technical Lead Mode (Prompt 9)**: instrui o Claude a ser *pro-active* antes de executar — perguntas clarificadoras + challenge de decisões + pensamento de 5 anos. É uma aplicação prática do princípio de [[boris-cherny]] ("entrar em plan mode antes de qualquer tarefa não trivial").

## Entidades relacionadas

- [[harish-bhatt]] — 3ª contribuição, novo ângulo: Claude para engenharia de software
- [[claude-code]] — ferramenta central convocada pelos prompts

## Conceitos relacionados

- [[prompt-engineering]] — extensão do padrão "Act like a senior X", simulação de equipe de engenharia
- [[agentes-ia]] — Prompt 7 simula 4 papéis em cadeia dentro de um único prompt
