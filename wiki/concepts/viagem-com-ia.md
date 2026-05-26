---
title: "Viagem com IA"
type: concept
tags: [viagem, voos, otimização, prompt-engineering, custos, geo-pricing, consumidor]
source_count: 1
last_updated: 2026-05-26
---

# Viagem com IA

> **Fontes:** 1 | **Domínio:** Aplicações pessoais de IA — viagem e otimização de custos de transporte

## Definição

Uso de LLMs para replicar o know-how de analistas profissionais de preços de voos — democratizando técnicas de otimização (skiplagging, geo-pricing, fare rules, timing) que antes exigiam agentes de viagem especializados, ferramentas pagas ou anos de experiência acumulada.

## Tese central

O knowledge de pricing de voos (revenue management, fare buckets, window de compra, POS diferenciado por país, fare classes) está codificado no treinamento dos LLMs a partir de documentação de companhias aéreas, relatórios regulatórios e pesquisas acadêmicas. Nomear o ROLE `analista profissional de preços de voos` e fornecer parâmetros estruturados é suficiente para convocar esse corpus — eliminando a necessidade de agente ou ferramenta paga.

## Padrão documentado

### Template base

```
Atue como analista profissional de preços de voos.

ROTA: [Origem] → [Destino]
DATAS: [Data de ida] / [Data de volta]
PASSAGEIROS: [Número, classe da cabina]
FLEXIBILIDADE: [± dias, bagagem de mão apenas?]
```

O template é parametrizado — os campos entre `[ ]` são os únicos inputs variáveis. O modelo convoca o framework de análise a partir do ROLE; o usuário apenas preenche o contexto específico.

### Os 7 domínios cobertos

| Domínio | Nome do Prompt | Diferencial |
|---------|----------------|-------------|
| Rotas alternativas | Hidden Route Scanner | Classifica por custo estimado + risco (baixo/médio/alto) |
| Reality check de pricing | Price-Behavior Reality Check | 3 buckets: confirmado, plausível, mito — combate viés de confirmação |
| Diferencial de POS | Geo-Pricing Bypass | Compara POS do país da companhia, de origem e de destino |
| Janela de compra | Timing Sweet-Spot Finder | Distingue doméstico/regional/longo curso + "fare reset" patterns |
| Decodificação de tarifas | Fare Rules Exploiter | Classifica estratégias em 3 tiers éticos (ver abaixo) |
| Canal de compra | Airline vs OTA | Gera "regra de decisão" específica para a rota |
| Monitoramento de preços | Price-Drop Tracker | Estratégia com ferramentas, cadência e regras de decisão |

### Classificação ética de tier (Prompt 5)

O Fare Rules Exploiter é o primeiro exemplo no wiki de um prompt que categoriza explicitamente o risco legal/ético de cada estratégia:

- **Legitimate optimization** — sempre seguro usar
- **Against airline T&Cs but not illegal** (ex: hidden-city/skiplagging) — explica o risco
- **Off-limits** (fraude, representação de identidade errônea) — claramente marcado

Essa estrutura de 3 tiers é reutilizável em qualquer domínio onde "otimização" pode cruzar limites regulatórios (fiscal, creditício, jurídico).

## Comparação com domínios análogos

| Conceito | Serviço substituído | Custo típico | Padrão de prompt |
|----------|---------------------|--------------|-----------------|
| [[viagem-com-ia]] | Agente de viagem especializado | $50–$200/consulta | ROLE "analista profissional de preços de voos" |
| [[bem-estar-com-ia]] | Personal trainer | $200/sessão | ROLE implícito + anamnese de 6 variáveis |
| [[finanças-com-ia]] | Analista financeiro / Bloomberg ($24K/ano) | $5K–$30K/ano | ROLE "Goldman Sachs / Bridgewater / etc." |

**Padrão comum**: o serviço caro existe porque o profissional coleta inputs estruturados e aplica knowledge já documentado. O LLM elimina o intermediário ao internalizar o mesmo conhecimento e ao receber os inputs via prompt parametrizado.

## Limitações documentadas

- **Sem acesso a dados ao vivo**: todos os prompts operam sobre padrões históricos e conhecimento de treinamento — não fazem scraping em tempo real de preços. Para busca de tarifas ao vivo, ferramentas como Google Flights, Hopper e Kayak ainda são necessárias.
- **Honestidade forçada necessária**: o Prompt 2 (Reality Check) inclui instrução explícita para separar mecanismos confirmados de mitos (ex: cookies elevando preços) — sem essa instrução, o modelo pode reproduzir crenças populares não verificadas.

## Fontes

- [[2026-05-25_bestapps-7-prompts-voos]] — 7 prompts para análise profissional de preços de voos; lançamento do conceito no wiki
