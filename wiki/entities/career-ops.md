---
title: "Career Ops"
type: entity
category: tool
tags: [busca-de-emprego, claude-code, automação, currículo, ats, open-source, linkedin, apify, negociação]
source_count: 2
last_updated: 2026-04-24
---

# Career Ops

> **Categoria:** Ferramenta open-source | **Licença:** MIT | **Aparece em:** 2 fontes

## O que é

Sistema de busca de emprego automatizado disponível como **plugin para Claude** (zip instalável) e como projeto open-source no GitHub. Integra com o conector Apify do Claude para scraping de vagas no LinkedIn.

## Funcionalidades

### Versão documentada em [[2026-04-07_career-ops-busca-emprego-ia]] (script/terminal)
- Escaneia páginas de carreira de empresas automaticamente
- Avalia vagas em **10 dimensões** de compatibilidade
- Reescreve currículo otimizado para **ATS** por vaga específica
- Dashboard terminal para rastreamento de candidaturas
- Mantém camada de decisão humana ("aplica só onde há match real")
- Gera PDFs otimizados

### Versão documentada em [[2026-04-22_arshman-khalid-automacao-busca-emprego]] (plugin Claude)
- Scraping automático de vagas no **LinkedIn** via Apify (LinkedIn Jobs Scraper Actor)
- Scoring **A a F** de cada vaga contra a experiência real do candidato
- Gera currículo ATS-friendly + carta de apresentação para cada vaga **A-tier**
- Identifica lacunas de skills e instrui correções antes da entrevista
- Constrói histórias **STAR** mapeadas para a vaga específica
- Redige mensagem de outreach para o **hiring manager**
- Entrega **scripts de negociação salarial** com framework após receber oferta

## Instalação (versão plugin)

1. Baixar zip do GitHub (link nos comentários do post original)
2. Claude → Novo plugin → Upload do zip
3. Criar conta Apify → ativar LinkedIn Jobs Scraper Actor → copiar API token
4. Claude → Conectores → instalar Apify → colar token

## Resultados documentados

- [[2026-04-07_career-ops-busca-emprego-ia]]: 700+ vagas avaliadas → oferta de emprego real
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]]: autor (@Arshman Khalid) afirma 518 candidaturas → 28 entrevistas (incluindo Google)

## Fontes

- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]]
