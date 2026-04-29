---
title: "Geração de Leads com IA"
type: concept
tags: [leads, prospecção, automação, google-maps, ia, b2b, conectores, vibe-prospecting, seo-local]
source_count: 5
last_updated: 2026-04-29
---

# Geração de Leads com IA

> **Fontes:** 5 | **Domínio:** Automação de negócios / Prospecção B2B

## Definição

Uso de LLMs (principalmente [[claude-code]]) integrados a ferramentas de scraping para coletar, enriquecer e organizar listas de leads de forma automatizada, sem planilhas manuais.

## Padrão dominante documentado

```
Claude Code / Claude
    ↓ integra com
Ferramenta de scraping (Apify / API File)
    ↓ coleta de
Google Maps (por nicho + cidade + quantidade)
    ↓ gera
Tabela de leads (telefone, endereço, site, redes, avaliação)
    ↓ opcional: enriquecimento por busca na internet
    ↓ opcional: links de WhatsApp pré-gerados
```

## Ferramentas documentadas

| Ferramenta | Fonte | Observações |
|------------|-------|-------------|
| [[apify]] | [[hudson-brendon]] | Conector nativo no Claude, instalação fácil |
| [[api-file]] | [[lucas-garcia-pit]] | Marketplace de APIs, enriquecimento adicional |
| [[vibe-prospecting]] | [[eduardo-santos]] | Conector do Claude.ai (web), gratuito, sem Claude Code |
| Prompts + ChatGPT/Claude | [[derek-gray]] | Prospecção via ranking Maps (#6–20), sem scraping automatizado |

## Método 5: Prospecção por posição no Google Maps (GMB)

[[derek-gray]] apresenta um ângulo distinto dos métodos anteriores: em vez de *extrair* dados do Maps via scraping, usa prompts para **identificar e abordar negócios mal rankeados**. A lógica:

- Negócios rankeados #6–20 são "invisíveis" para ~70% dos clientes (não aparecem na primeira tela)
- Prompt de prospecção gera lista de 50+ empresas nessa faixa, com nome, contato, posição e dor específica
- O lead é abordado com proposta de subir para o top 3 via otimização de GBP

Diferença chave: aqui o objetivo não é *usar* o lead como cliente direto do seu produto — é *ajudar o negócio local a melhorar seu próprio rankeamento* como serviço recorrente.
→ [[2026-04-05_derek-gray-renda-recorrente-google-maps]]

## Boas práticas identificadas

1. **Contextualizar o ICP** antes de iniciar o scraping — quanto mais contexto sobre o lead ideal, mais qualificados os resultados (Lucas Garcia Pit)
2. **Usar o mesmo chat** para evitar repetição de leads já capturados (Lucas Garcia Pit)
3. **Pedir links de WhatsApp** na tabela de saída para reduzir fricção no contato
4. **Especificar parâmetros** no prompt: nicho, cidade, quantidade (Hudson Brendon)

## Limitações conhecidas

- E-mail raramente disponível via Google Maps (mencionado por Hudson Brendon)
- Qualidade dos dados depende do que está público no Maps

## Sínteses relacionadas

- [[comparação-métodos-leads]] — comparação direta dos dois métodos

## Fontes

- [[2026-03-19_leads-infinitos-cloudcode]]
- [[2026-03-28_prospecção-leads-claude-apify]]
- [[2026-04-15_leads-qualificados-claudecode]]
- [[2026-04-14_eduardo-santos-vibe-prospecting]]
- [[2026-04-05_derek-gray-renda-recorrente-google-maps]]
