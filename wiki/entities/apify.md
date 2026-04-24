---
title: "Apify"
type: entity
category: tool
tags: [scraping, automação, leads, google-maps, conector]
source_count: 2
last_updated: 2026-04-24
---

# Apify

> **Categoria:** Plataforma de scraping | **Aparece em:** 1 fonte

## O que é

Apify é uma plataforma de web scraping e automação com marketplace de "Actors" (scrapers pré-construídos). Tem conector nativo no Claude, instalável diretamente pelo painel de conectores.

## Configuração com Claude

1. Criar conta em apify.com
2. Settings → API e Integrations → copiar token
3. No Claude: Personalizar → Conectores → buscar "Apify" → Instalar → colar token

## Capacidade documentada

### Google Maps Scraper (leads B2B)
- Scraping do Google Maps filtrado por nicho, cidade e quantidade
- Retorna: telefone, endereço, site, redes sociais, avaliação Google, categoria
- **Limitação**: e-mail raramente disponível (depende de dados públicos no Maps)

### LinkedIn Jobs Scraper Actor (busca de emprego)
- Scraping de vagas no LinkedIn integrado ao plugin CareerOps
- Alimenta pipeline automatizado de candidatura (scoring, currículo ATS, outreach)
- Configuração: ativar o Actor na conta Apify → copiar API token → instalar conector Apify no Claude

## Comparação com API File

| | Apify | API File |
|--|-------|----------|
| Instalação | Conector nativo no Claude | Via chave de API no Claude Code |
| Fontes de dados | Google Maps, LinkedIn Jobs (e outros) | Google Maps (entre outros) |
| Enriquecimento | Não mencionado | Busca adicional na internet |
| Popularidade no wiki | 2 fontes | 1 fonte |

## Fontes

- [[2026-03-28_prospecção-leads-claude-apify]]
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]]
