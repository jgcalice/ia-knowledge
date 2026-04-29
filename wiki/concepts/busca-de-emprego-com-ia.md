---
title: "Busca de Emprego com IA"
type: concept
tags: [carreira, busca-de-emprego, automação, ats, currículo, claude-code, apify, linkedin, negociação]
source_count: 3
last_updated: 2026-04-29
---

# Busca de Emprego com IA

> **Fontes:** 2 | **Domínio:** Automação de carreira / Job search pipeline

## Definição

Uso de LLMs e automação para transformar a busca de emprego de processo manual e baseado em esforço para pipeline estruturado baseado em dados e fit real.

## O que foi documentado

### Career Ops — Sistema completo de job search
Projeto open-source (MIT) construído com Claude Code por desenvolvedor individual:

**Pipeline do sistema:**
```
Escanear páginas de carreira de empresas
    ↓
Avaliar vagas em 10 dimensões de fit
    ↓
Filtrar vagas com match real (não aplicar em massa)
    ↓
Reescrever currículo otimizado para ATS por vaga
    ↓
Preparar conteúdo de entrevista
    ↓
Dashboard de rastreamento de candidaturas
```

**Resultado documentado:** 700+ vagas avaliadas → oferta de emprego real.

## Por que ATS importa

ATS (Applicant Tracking System) é o software que empresas usam para filtrar currículos antes de um humano ver. Currículo genérico é reprovado pelo ATS antes de chegar ao recrutador. Otimização por vaga específica aumenta drasticamente a taxa de passagem.

## Integração com LinkedIn

A busca de emprego com IA complementa a otimização de LinkedIn:
1. **LinkedIn otimizado** ([[2026-04-11_transformacao-linkedin-ia]]) → te acha por busca de recrutadores
2. **Career Ops** → você acha as vagas certas e aplica com currículo customizado

## CareerOps como plugin Claude (Arshman Khalid)

Segunda documentação do Career Ops — desta vez como **plugin instalável via zip** no Claude, integrado ao **Apify LinkedIn Jobs Scraper**. Pipeline expandido em relação à versão anterior:

```
Scraping de vagas LinkedIn (via Apify)
    ↓
Scoring A-F contra experiência do candidato
    ↓
Currículo ATS + carta de apresentação para vagas A-tier
    ↓
Identificação de gaps de skills + como corrigir
    ↓
Histórias STAR mapeadas para a vaga
    ↓
Outreach para o hiring manager
    ↓
Scripts de negociação salarial (após oferta)
```

**Nova dimensão documentada:** o pipeline vai além da candidatura — acompanha até a negociação salarial, o que não estava documentado na fonte anterior.

**Argumento central do autor:** "Empresas usam IA para rejeitar seu currículo em 6 segundos. Use IA para rejeitar a vaga delas em 3 segundos."

→ [[2026-04-22_arshman-khalid-automacao-busca-emprego]] | Autor: [[arshman-khalid]]

## Candidaturas personalizadas sem automação (Coding AI FullStack 300K)

Nível de entrada documentado — uso direto do Claude.ai, sem CLI, sem plugins:

**Fluxo documentado:**
```
Colar job description no Claude
    ↓
Claude extrai skills e palavras-chave prioritárias do anúncio
    ↓
Claude reescreve o currículo com foco naquelas skills
    ↓
Claude gera carta de apresentação alinhada à vaga
```

**Resultado do caso**: 6 entrevistas em 7 dias (anedota narrativa, não verificável).

**Diferença chave em relação ao Career Ops**: não há automação ou scraping — o fluxo é manual por vaga, mas muito mais rápido que reescrita sem IA. Acessível para qualquer pessoa sem conhecimento técnico.

→ [[2026-04-26_coding-ai-fullstack-entrevistas-claude]] | Autor: [[coding-ai-fullstack]]

## Fontes

- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]]
- [[2026-04-26_coding-ai-fullstack-entrevistas-claude]]
