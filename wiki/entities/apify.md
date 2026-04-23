---
title: "Apify"
type: entity
category: tool
tags: [scraping, automação, leads, google-maps, conector]
source_count: 1
last_updated: 2026-04-21
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

- Scraping do Google Maps filtrado por nicho, cidade e quantidade
- Retorna: telefone, endereço, site, redes sociais, avaliação Google, categoria
- **Limitação**: e-mail raramente disponível (depende de dados públicos no Maps)

## Comparação com API File

| | Apify | API File |
|--|-------|----------|
| Instalação | Conector nativo no Claude | Via chave de API no Claude Code |
| Fonte de leads | Google Maps (entre outros) | Google Maps (entre outros) |
| Enriquecimento | Não mencionado | Busca adicional na internet |
| Popularidade no wiki | 1 fonte | 1 fonte |

## Fontes

- [[2026-03-28_prospecção-leads-claude-apify]]
