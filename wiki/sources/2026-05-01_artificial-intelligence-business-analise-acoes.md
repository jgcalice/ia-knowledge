---
title: "10 Prompts para Analisar Ações como Analistas de Wall Street com Claude"
type: source
source_file: "2026-05-01_artificial_intelligence_l_business_DXzzxyCDk-9.md"
author: "@Artificial Intelligence l Business"
date: 2026-05-01
format: carousel
tags: [finanças-com-ia, investimentos, análise-financeira, prompt-engineering, claude, bloomberg, wall-street]
source_url: "https://www.instagram.com/p/DXzzxyCDk-9/?img_index=1&igsh=NDBrOXBoY21qcGM2"
source_count: 1
---

# 10 Prompts para Analisar Ações como Analistas de Wall Street com Claude

> **Fonte:** [[2026-05-01_artificial_intelligence_l_business_DXzzxyCDk-9]] | **Autor:** @Artificial Intelligence l Business (@thewizeai) | **Data:** 2026-05-01 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXzzxyCDk-9/?img_index=1&igsh=NDBrOXBoY21qcGM2)**

## TL;DR

10 prompts sequenciais que replicam o raciocínio completo de analistas institucionais de Wall Street com Claude, tornando gratuito o que um Bloomberg Terminal cobra $24.000/ano para fornecer.

## Contexto

O Bloomberg Terminal é o padrão ouro de análise de ações em Wall Street — custa $24.000/ano ($2.000/mês). @thewizeai (repostado pela conta @Artificial Intelligence l Business) propõe que Claude já consegue executar a maior parte do que investidores individuais usam o terminal para fazer, de graça, via 10 prompts estruturados que devem ser usados *em sequência*, não isoladamente.

O diferencial da abordagem: os prompts replicam a *metodologia de raciocínio* de analistas institucionais — não olham para uma métrica isolada, mas percorrem um ciclo completo (entender o negócio → stress test da tese → verificar contabilidade → comparar alternativas → dimensionar risco pessoal).

## O que foi ensinado

Os 10 prompts documentados (9 dos 10 slides capturados):

| # | Prompt | O que faz |
|---|--------|-----------|
| 1 | **Institutional Kickoff Report** | Atua como analista sênior: modelo de negócio, motores de receita, estrutura de custos, vantagens competitivas, riscos, qualidade da gestão, posição setorial, perspectivas; entrega 3 bulls + 3 bears + conclusão equilibrada |
| 2 | **Quarterly Results Analysis** | Lê relatório/transcript de resultados e decompõe: o que melhorou, o que piorou, o que a gestão enfatiza, o que evita, red flags ocultos, números-chave para o próximo trimestre |
| 3 | **Bull vs Bear Debate** | Constrói o caso otimista (crescimento de receita, expansão de margem, catalisadores) vs. pessimista (desaceleração, riscos de margem, ameaças competitivas, exposição macro, preocupações de valuation); conclui qual lado tem argumento mais forte agora |
| 4 | **Forensic Accounting Analysis** | Analisa como contador forense: qualidade das receitas, solidez do fluxo de caixa, riscos de dívida e diluição, stock-based compensation, ajustes únicos, sinais de contabilidade agressiva, discrepâncias entre números reportados e reais; gera seção "Red flags I would investigate before buying" |
| 5 | **Honest Valuation Framework** | Cria framework de valuation sem fingir precisão: P/E, EV/EBITDA, Price/Sales, FCF yield e DCF simplificado; para cada método explica quando é mais útil, o que diz sobre a ação agora, e se o preço está barato/justo/caro |
| 6 | **Company Comparison** | Compara duas empresas head-to-head via tabela: modelo de negócio, taxa de crescimento, margens, fluxo de caixa, balanço, valuation, moat, qualidade da gestão, riscos-chave, vencedor em cada categoria; finaliza com qual segurar por 5 anos e por quê |
| 7 | **Investor Summary Sheet** | Converte arquivo de empresa ou transcript de resultados em resumo de 1 página: o que faz, como gera receita, principais motores de crescimento, riscos, figuras-chave, segmentos de receita, tom da gestão, citações relevantes, o que observar no próximo relatório |
| 8 | **Stress Test of Investment Thesis** | Teste de estresse da tese: 3 cenários (bullish/base/bearish); para cada um estima direção de crescimento da receita, direção das margens, sentimento de mercado, variação possível do preço da ação e probabilidade atribuída a cada cenário |
| 9 | **Big Business vs Big Stock** | Distingue grande negócio de grande ação: qualidade do negócio, qualidade da gestão, força financeira, valuation, expectativas de mercado, probabilidade de alta vs. baixa; classifica em: grande negócio a ótimo preço / grande negócio a preço ruim / negócio ruim a ótimo preço / evitar |

**Instrução-chave:** usar os prompts *em ordem*, começando pelo Kickoff Report para construir a base, depois empilhando earnings, valuation e risk assessment — não em isolamento.

## Insights para o wiki

- **5º ângulo de finanças com IA documentado no wiki**: a abordagem é radicalmente diferente das anteriores — não usa uma única instituição como ROLE, não faz triagem em funil, não aplica template genérico de analista. É um *pipeline sequencial completo* que cobre o ciclo inteiro de análise institucional
- **"Sequência como metodologia"**: o insight mais valioso é que a ordem dos prompts importa — replicar o *processo* de raciocínio institucional, não apenas extrair métricas
- **Forensic Accounting como ângulo inédito no wiki**: nenhuma fonte anterior abordou análise de qualidade contábil (aggressive accounting signals, stock-based comp, discrepâncias reportado vs. real)
- **Bull vs Bear Debate como artefato deliberado**: o prompt 3 não pede análise neutra — pede explicitamente qual lado tem argumento mais forte *agora*, forçando o modelo a tomar posição
- **Stress test com probabilidades**: o Prompt 8 exige atribuição de probabilidades aos três cenários, não apenas descrição — introduz raciocínio quantitativo explícito ao framework

## Entidades relacionadas

- [[artificial-intelligence-business]] — canal que publicou o post (repost de @thewizeai)

## Conceitos relacionados

- [[finanças-com-ia]] — 5º ângulo documentado: pipeline sequencial de análise institucional completa
- [[prompt-engineering]] — sequência como padrão: prompts em ordem > prompts isolados
