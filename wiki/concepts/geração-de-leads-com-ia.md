---
title: "Geração de Leads com IA"
type: concept
tags: [leads, prospecção, automação, google-maps, ia, b2b, conectores, vibe-prospecting, seo-local]
source_count: 7
last_updated: 2026-05-12
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

### Variante #7–25: faixa expandida de qualificação

([[derek-gray]], [[2026-05-11_derek-gray-setores-tier-agentes-ia]]) — 4ª fonte Derek Gray

Esta fonte documenta a faixa **#7–25** (vs. #6–20 das fontes anteriores) com critério adicional: **4–5 estrelas** de avaliação. O objetivo muda ligeiramente: criar lista de 15–20 leads antes do primeiro outreach. Mesma lógica, janela de prospecção ligeiramente mais ampla.

### Sweet spot pattern (critérios objetivos de qualificação de lead)

Segunda fonte de [[derek-gray]] (2026-05-09) documenta critérios de filtragem antes de qualquer outreach — o "padrão de mina de ouro":

| Critério | Valor-alvo |
|----------|-----------|
| Tempo de operação | Mais de 5 anos (negócio estabelecido) |
| Número de avaliações | Menos de 80 (baixa visibilidade online) |
| Presença na web | Sem website ou website desatualizado |
| Qualidade das avaliações | 3,9 estrelas ou mais (boa reputação) |

**Meta**: 25–30 leads de **um único nicho em uma cidade**. A combinação (negócio maduro + presença digital fraca + boa reputação) indica receita existente perdendo clientes por ausência online.

**Pipeline completo com o sweet spot**:

```
Maps (sweet spot filter) → Claude (diagnóstico + brief + mensagem <70 palavras)
→ Lovable (landing page mockup em 5 min) → Outreach (link do mockup, nunca mencionar IA)
→ GBP Management recorrente ($500–800/mês via Quepo)
```

→ [[2026-05-09_derek-gray-google-maps-claude-monetizacao]]

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
- [[2026-05-09_derek-gray-google-maps-claude-monetizacao]]
- [[2026-05-11_derek-gray-setores-tier-agentes-ia]]
