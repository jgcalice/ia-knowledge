---
title: "6 Claude Skills que Substituem um Time de Produto Inteiro"
type: source
source_file: "2026-04-07_aashish_pahwa_DW0siNeD0ao.md"
author: "@Aashish Pahwa"
date: 2026-04-07
format: carousel
tags: [claude-skills, product-management, prompt-engineering, agentes-ia, arquitetura]
source_url: "https://www.instagram.com/p/DW0siNeD0ao/"
source_count: 1
---

# 6 Claude Skills que Substituem um Time de Produto Inteiro

> **Fonte:** [[2026-04-07_aashish_pahwa_DW0siNeD0ao]] | **Autor:** @Aashish Pahwa | **Data:** 2026-04-07 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DW0siNeD0ao/)**

## TL;DR

Seis [[claude-skills]] especializadas para Product Managers — cobrem descoberta, spec, stress test de decisões e arquitetura — ativadas por frases-gatilho específicas e disponíveis em marketplaces públicos como [[smithery]].

## Contexto

[[aashish-pahwa]] é consultor de IA e fundador do feedough.com. Aponta que o trabalho tradicional do PM (alternar entre ferramentas, escrever docs manualmente, depender de múltiplos times para clareza) está migrando para Claude Skills — **não substituindo PMs, mas mudando como trabalham**. O material também aponta 3 marketplaces para baixar skills prontas.

## O que foi ensinado

### As 6 Claude Skills para PMs

| # | Skill | Quando usar | Frases-gatilho | Search Tag |
|---|-------|-------------|----------------|------------|
| 1 | **Feature Forge** | Antes de qualquer linha de código — entrevista como PM e dev, gera spec completa com requisitos + critérios de aceitação + checklist | "define this feature", "write a spec for...", "requirements" | `planning` |
| 2 | **Spec Miner** | Engenharia reversa de produto/feature existente — identifica requisitos reais, lacunas, edge cases | "reverse engineer this", "document this codebase", "understand existing system" | `discovery` |
| 3 | **The Fool** | Stress test de decisões grandes — desafia de 5 ângulos: advogado do diabo, red team, pre-mortem | "challenge this", "poke holes in my plan", "stress test" | `critical thinking` |
| 4 | **Architecture Designer** | Design de sistema novo ou escolha entre abordagens — trade-offs + decisões + diagramas | "design this system", "architecture", "help me choose between..." | `system design` |
| 5 | **API Designer** | Criar APIs limpas — endpoints, modelos de dados, documentação estruturada | "design this API", "REST API", "OpenAPI spec" | `APIs` |
| 6 | **Microservice Architect** | Quebrar sistema complexo em serviços independentes escaláveis | "microservices", "service boundaries", "distributed systems" | `distributed systems` |

### Marketplaces de Claude Skills recomendados

- `jeffallan.github.io/claude-skills/skills-guide/`
- `BehiSecc/awesome-clause-skills/`
- **[[smithery]]** — 128.624 skills catalogadas (referência de escala)

## Insights para o wiki

- **Primeira entrada detalhada sobre [[claude-skills]]** como arquétipo. Até agora o wiki tinha menções soltas — aqui temos mapa concreto: skill = pacote nomeado com frases-gatilho + search tag + caso de uso
- **Conexão com [[adriano-couto]]** (palavras-gatilho): Claude Skills são a formalização industrial da ideia de "palavra-gatilho ativa comportamento". Gatilhos livres viram skills nomeadas e distribuíveis
- **"The Fool" é um meta-skill de decisão**: red team + advogado do diabo + pre-mortem consolidados — poderia virar conceito próprio no wiki se aparecerem mais fontes
- **Product Management com IA como novo cluster**: primeira fonte focada em PM. Diferente de "estratégia de negócios" (mercado/oferta) ou "gestão com IA" (time/problemas) — aqui é **ciclo de vida de produto** (descoberta → spec → arquitetura → deploy)
- **Escala do ecossistema Smithery** (128k+ skills): evidência de que a economia de skills compartilháveis já existe e está grande

## Entidades relacionadas

- [[aashish-pahwa]] — autor, consultor de IA, fundador do feedough.com
- [[claude-skills]] — feature nativa da Anthropic, pacotes de comportamento ativáveis por trigger
- [[smithery]] — marketplace com 128k+ skills
- [[claude-code]] — ambiente onde as skills operam

## Conceitos relacionados

- [[agentes-ia]] — cada skill é um micro-agente especializado
- [[prompt-engineering]] — skills formalizam o padrão de "palavra-gatilho" em pacotes distribuíveis
- [[estratégia-de-negócios-com-ia]] — skills de Architecture Designer e API Designer cruzam com planejamento de produto
