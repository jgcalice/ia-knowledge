---
title: "5 Configurações para Sites Profissionais com Claude"
type: source
source_file: "2026-08-19_vinicius_delmonego_estrategista_de_infoprodutos_ia_DcJUB_yipdH.md"
author: "@Vinícius Delmônego | Estrategista de Infoprodutos + IA"
date: 2026-08-19
format: reel
tags: [claude, claude-code, claude-skills, mcp, figma, playwright, vibecoding, design, ferramentas-ia]
source_url: "https://www.instagram.com/reel/DcJUB_yipdH/?stkn=MTdrMGltazVqa3ljcQ=="
source_count: 1
---

# 5 Configurações para Sites Profissionais com Claude

> **Fonte:** [[2026-08-19_vinicius_delmonego_estrategista_de_infoprodutos_ia_DcJUB_yipdH.md]] | **Autor:** @Vinícius Delmônego | Estrategista de Infoprodutos + IA | **Data:** 2026-08-19 | **Formato:** reel | **[↗ Ver post](https://www.instagram.com/reel/DcJUB_yipdH/?stkn=MTdrMGltazVqa3ljcQ==)**

## TL;DR

Três Claude Skills (Milkovalski Design, Impeccable Design, Taste Skill) + dois MCPs (Figma, Playwright) transformam o Claude de gerador de sites genéricos em uma ferramenta capaz de entregar layouts modernos, inspirados em referências reais e já testados automaticamente.

## Contexto

Post curto (66s) de um estrategista de infoprodutos que resolve um problema recorrente e implícito em quase todo o cluster de vibecoding do wiki: sites gerados por Claude/Claude Code sem configuração adicional tendem a ter "aquela cara de site feito por IA" — layout genérico, sem inspiração real. O autor propõe um setup mínimo de 5 peças (3 skills + 2 MCPs) como solução.

## O que foi ensinado

- **Milkovalski Design** (skill) e **Impeccable Design** (skill): ensinam ao Claude layout moderno, tipografia e espaçamento — o "gosto visual" que falta por padrão
- **Taste Skill**: em vez de o Claude gerar o design do zero, a skill busca inspiração em sites reais antes de montar o layout — mecanismo explícito contra o "começar do zero e ficar ruim"
- **MCP Figma**: conecta o Claude ao Figma para montar o site diretamente na ferramenta de design
- **MCP Playwright**: permite que o Claude teste o site automaticamente (navegação, renderização) antes de entregar o resultado ao usuário
- Aplicações sugeridas: landing page de infoproduto, portfólio de agência, página de venda de serviços

## Insights para o wiki

- **Confirma e refina o padrão de "stack de ferramentas para vibe coders"** já documentado para iOS ([[joaquin-fernandez]]) e web visual ([[aleeshh]]) — mas aqui a composição é 100% nativa do ecossistema Claude (Skills + MCP), sem ferramentas de terceiros como ShadCN ou Watermelon UI
- **Primeira menção no wiki de "buscar inspiração em sites reais" como mecanismo de skill** (Taste Skill) — distinto de bibliotecas de componentes (ShadCN, Watermelon UI) ou geradores de assets (Hyke): aqui a skill resolve o problema de referência visual, não de código
- **Primeira aparição do MCP Figma e do MCP Playwright no wiki** — Playwright introduz um padrão novo: teste automatizado do output *antes* da entrega, um paralelo ao "quality gate" documentado em GSD ([[nate-herk]]), mas aplicado a QA visual/funcional de sites em vez de código de backend
- Reforça a tese consolidada de "combinação de skills > skill isolada" (ver [[claude-skills]]) — aqui a combinação é aplicada especificamente ao domínio de design de sites

## Entidades relacionadas

- [[vinicius-delmonego]] — autor, estrategista de infoprodutos com foco em configuração do Claude para design
- [[claude-code]] — ambiente onde as skills e MCPs operam
- [[claude-skills]] — feature que abriga Milkovalski Design, Impeccable Design e Taste Skill
- [[figma]] — MCP para montagem direta do site
- [[playwright]] — MCP para teste automatizado do site

## Conceitos relacionados

- [[vibecoding]] — nova composição de stack (skills + MCP nativos) para elevar a qualidade visual de sites vibecoded
- [[estratégia-de-negócios-com-ia]] — aplicações práticas citadas (landing page de infoproduto, portfólio, página de serviços)
