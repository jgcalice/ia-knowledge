---
title: "Automatizando Prospecção de Leads com Claude e Apify"
type: source
source_file: "2026-03-28_hudson_brendon_automacao_com_ia_para_negocios_DWcVBIYiWJF.md"
author: "@Hudson Brendon | Automação com IA para Negócios"
date: 2026-03-28
format: reel
duration_seconds: 114
tags: [claude, apify, leads, prospecção, google-maps, automação, b2b]
source_url: "https://www.instagram.com/reel/DWcVBIYiWJF/?igsh=eDE0YWM0cXI3dmVp"
source_count: 1
---

# Automatizando Prospecção de Leads com Claude e Apify

> **Fonte:** [[2026-03-28_hudson_brendon_automacao_com_ia_para_negocios_DWcVBIYiWJF]] | **Autor:** @Hudson Brendon | **Data:** 2026-03-28 | **Formato:** Reel (114s) | **[↗ Ver post](https://www.instagram.com/reel/DWcVBIYiWJF/?igsh=eDE0YWM0cXI3dmVp)**

## TL;DR

Conecte o Claude ao [[apify]] via conector nativo para extrair leads filtrados do Google Maps por nicho, cidade e quantidade — sem planilha manual, com telefone, endereço, site, redes sociais e avaliação Google.

## Contexto

Hudson Brendon mostra um método de prospecção B2B automatizada usando o Claude com o conector Apify. Diferente do método de [[lucas-garcia-pit]] (que usa [[api-file]]), Hudson usa o marketplace de scrapers da Apify integrado diretamente via painel do Claude.

## O que foi ensinado

- **Configuração**: Criar conta Apify → copiar token de API → no Claude: Personalizar → Conectores → buscar "Apify" → instalar → colar token
- **Prompt estruturado**: Especificar nicho, cidade e quantidade desejada (ex: "dentistas em São Paulo, 10 resultados")
- **Dados extraídos**: Telefone, endereço, cidade, site, redes sociais, avaliação no Google, categoria
- **Limitação observada**: E-mail nem sempre disponível (depende do que está público no Google Maps)
- **Resultado**: Planilha limpa e organizada, pronta para prospecção B2B

## Insights para o wiki

- Método muito parecido com o de [[lucas-garcia-pit]], mas com ferramenta diferente ([[apify]] vs [[api-file]]). Ambos usam Google Maps como fonte.
- A Apify tem conector nativo no Claude, o que facilita a instalação em relação ao método via API File
- E-mail raramente disponível — ponto de fricção em ambos os métodos de leads via Google Maps
- Hudson não menciona enriquecimento adicional (busca na internet), ao contrário de Lucas

## Entidades relacionadas

- [[hudson-brendon]] — autor do conteúdo
- [[claude-code]] — ferramenta principal (chamado de "Cloud" no vídeo)
- [[apify]] — plataforma de scraping integrada ao Claude
- [[google-maps]] — fonte dos dados de leads

## Conceitos relacionados

- [[geração-de-leads-com-ia]] — método central
- [[prompt-engineering]] — uso de prompt estruturado com parâmetros (nicho, cidade, quantidade)
