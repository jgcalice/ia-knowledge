---
title: "find-skills: Como Descobrir a Skill Certa no Claude Code"
type: source
source_file: "2026-04-22_pabloinpublic_DXcWjL0jLsd.md"
author: "@PabloInPublic"
date: 2026-04-22
format: reel
tags: [claude-code, skills, ferramentas-ia, automação, vercel]
source_url: "https://www.instagram.com/reel/DXcWjL0jLsd/"
source_count: 1
---

# find-skills: Como Descobrir a Skill Certa no Claude Code

> **Fonte:** [[2026-04-22_pabloinpublic_DXcWjL0jLsd]] | **Autor:** @PabloInPublic | **Data:** 2026-04-22 | **Formato:** Reel (33s) | **[↗ Ver post](https://www.instagram.com/reel/DXcWjL0jLsd/)**

## TL;DR

A `find-skills` (Vercel Labs) é uma meta-skill para o Claude Code que busca entre milhares de skills publicadas no GitHub usando linguagem natural — resolve o problema de descoberta num ecossistema que cresceu demais para navegar manualmente.

## Contexto

Com o ecossistema de [[claude-skills]] em expansão acelerada (128k+ skills catalogadas no [[smithery]]), o verdadeiro gargalo deixou de ser "não existir skills" e passou a ser "não saber qual instalar". Um desenvolvedor japonês identificou esse problema e encontrou a solução: uma meta-skill criada pelo Vercel Labs que age como mecanismo de busca semântica para o próprio ecossistema de skills.

## O que foi ensinado

- **O problema**: Há milhares de skills publicadas no GitHub; procurar manualmente ou ler README de cada uma é ineficiente
- **A solução**: `find-skills` — skill do Vercel Labs que busca entre todas as outras por você
- **Instalação** (único comando):
  ```
  npx skills add https://github.com/vercel-labs/skills --skill find-skills
  ```
- **Uso dentro do Claude Code**: perguntar em linguagem natural, ex.:
  > "há alguma skill boa para [objetivo]?"
- **O que resolve**: elimina busca cega, economiza até 30 min lendo documentações
- A skill retorna a **coincidência mais relevante** para a intenção descrita

## Insights para o wiki

- Confirma que o ecossistema de skills atingiu escala suficiente para precisar de **tooling de descoberta** — metadado de maturidade do ecossistema
- Cria uma nova camada no uso do Claude Code: primeiro descobrir a skill certa, depois instalá-la
- Padrão "meta-skill" (skill que ajuda a usar outras skills) é novo no wiki — extensão natural da arquitetura de skills
- Complementa a lista documentada por [[aashish-pahwa]] e o catálogo do [[smithery]]

## Entidades relacionadas

- [[claude-skills]] — o ecossistema que esta skill navega
- [[pablo-in-public]] — criador do conteúdo
- [[claude-code]] — ambiente onde find-skills roda

## Conceitos relacionados

- [[agentes-ia]] — skills como micro-agentes; meta-skill como orquestrador de descoberta
- [[prompt-engineering]] — busca por linguagem natural como forma de acesso a comportamentos
