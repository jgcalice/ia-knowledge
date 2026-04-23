---
title: "Comparação: Métodos de Geração de Leads via Google Maps com IA"
type: synthesis
tags: [leads, prospecção, apify, api-file, comparação, google-maps]
sources: [2026-03-19_leads-infinitos-cloudcode.md, 2026-03-28_prospecção-leads-claude-apify.md]
created: 2026-04-21
last_updated: 2026-04-21
---

# Comparação: Métodos de Geração de Leads via Google Maps com IA

> Análise cruzada de [[2026-03-19_leads-infinitos-cloudcode]] e [[2026-03-28_prospecção-leads-claude-apify]]

## Contexto

Dois criadores brasileiros ensinam, com 9 dias de diferença, métodos muito parecidos de geração de leads usando Claude + scraping do Google Maps. Isso não é coincidência — é sinal de que o padrão está se consolidando como prática recomendada no nicho de automação de negócios.

## Comparação direta

| Dimensão | Lucas Garcia Pit | Hudson Brendon |
|----------|-----------------|----------------|
| **Ferramenta** | [[api-file]] | [[apify]] |
| **Integração** | Chave de API no Claude Code | Conector nativo no Claude |
| **Facilidade de setup** | Intermediária | Fácil (conector oficial) |
| **Enriquecimento** | Sim (busca adicional na internet) | Não mencionado |
| **Links de WhatsApp** | Sim (solicitado explicitamente) | Não mencionado |
| **Filtros de busca** | Nicho + ICP detalhado | Nicho + cidade + quantidade |
| **Contextualização** | Forte ênfase em ICP | Prompt simples com parâmetros |
| **Data do conteúdo** | 2026-03-19 | 2026-03-28 |

## Convergências

1. Ambos usam [[google-maps]] como fonte de dados
2. Ambos usam [[claude-code]] como orquestrador
3. Ambos prometem "leads infinitos" sem esforço manual
4. A limitação de e-mail é real nos dois casos (Hudson menciona explicitamente)

## Divergências principais

- **Enriquecimento**: Lucas enfatiza enriquecer dados com busca na internet — Hudson não menciona isso. Pode ser uma vantagem real do método de Lucas.
- **Contextualização do ICP**: Lucas dá muito mais ênfase à qualidade do briefing antes do scraping. Hudson foca mais na facilidade de instalação e execução.
- **Ferramenta**: A Apify tem conector nativo no Claude (menor fricção de setup); a API File requer configuração manual de chave.

## Recomendação

Para quem está começando: **Apify** pela facilidade do conector nativo.
Para quem quer leads mais qualificados: **API File** + enriquecimento via busca na internet, com briefing detalhado do ICP.

## Lacuna identificada

Nenhum dos dois cria faz teste comparativo head-to-head das ferramentas. Dados reais de conversão de leads gerados por esses métodos não estão disponíveis no wiki.
