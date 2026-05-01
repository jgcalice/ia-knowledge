---
title: "Como Encontrar Ações em 5 Minutos Usando IA — Scanner de 3 Prompts"
type: source
source_file: "2026-04-30_bert_no_chase_swing_trading_for_9_5s_DXwl6eFla3k.md"
author: "@Bert | No-Chase Swing Trading for 9-5s"
date: 2026-04-30
format: reel
tags: [finanças-com-ia, trading, swing-trading, prompt-engineering, investimentos, llm]
source_url: "https://www.instagram.com/reel/DXwl6eFla3k/?igsh=NWNpZGQ5bTdieWJ4"
source_count: 1
---

# Como Encontrar Ações em 5 Minutos Usando IA — Scanner de 3 Prompts

> **Fonte:** [[2026-04-30_bert_no_chase_swing_trading_for_9_5s_DXwl6eFla3k]] | **Autor:** @Bert | No-Chase Swing Trading for 9-5s | **Data:** 2026-04-30 | **Formato:** reel (58s) | **[↗ Ver post](https://www.instagram.com/reel/DXwl6eFla3k/?igsh=NWNpZGQ5bTdieWJ4)**

## TL;DR

Um pipeline de 3 prompts sequenciais (tema → lista de 25 ações → ranking por qualidade + desconto → deep dive no top 3) para identificar candidatos a swing trade em menos de 5 minutos — com reconhecimento explícito de que IA não substitui análise técnica no timing de entrada.

## Contexto

Bert ensina swing trading para pessoas com emprego em tempo integral ("No-Chase" = sem perseguir ações em movimento). O post é resposta direta a perguntas da audiência sobre como *encontrar* ações — etapa anterior ao framework de 5 prompts que ele publicou antes. O caso pessoal citado: $129.000 em swing trading no último ano com emprego full-time; AMD e Palantir como exemplos de acertos antes de corridas de "centenas de porcento".

## O que foi ensinado

**Prompt 1 — Construtor de universo**
- Defina um tema de mercado que está observando (ex: semicondutores, energia, IA)
- Claude gera uma lista de 25 ações relacionadas ao tema
- Saída: universo temático com 25 candidatos

**Prompt 2 — Ranqueador por qualidade + desconto**
- Aplica dois filtros em paralelo para cada ação:
  1. A empresa é financeiramente saudável? (qualidade do negócio)
  2. A ação está com desconto real? (avaliação de preço)
- Saída: lista ranqueada combinando solidez + barganha

**Prompt 3 — Deep dive no top 3**
- Para cada uma das 3 melhores, Claude produz análise completa:
  - Por que o negócio é forte
  - Por que a ação está barata agora
  - O que pode fazer a ação subir (catalisador)
  - O que pode dar errado (risco)

**Limitação reconhecida explicitamente**
- IA *não é boa* em decidir o *timing* de entrada ("when to get in")
- Essa etapa requer leitura de gráfico + análise técnica humana
- A combinação IA (screening/fundamental) + chart reading (timing) é o diferencial

**Compatível com múltiplos LLMs:** Claude, ChatGPT ou Gemini

## Insights para o wiki

- **Terceiro ângulo de finanças com IA**: complementa [[2026-04-26_faria-lima-elevator-ia-investimentos]] (análise institucional via ROLE) e [[2026-04-28_derek-gray-chatgpt-wealth]] (riqueza pessoal). Aqui o foco é *seleção de ativos* — triagem eficiente antes da análise aprofundada
- **Pipeline sequencial como metodologia de screening**: três prompts encadeados cobrem funil completo (amplo → filtrado → profundo) — padrão análogo ao funil de leads documentado em [[geração-de-leads-com-ia]]
- **Honestidade editorial sobre limitações da IA**: criador explicita que IA falha no timing — raro no nicho de conteúdo "IA faz tudo". Reforça o dado empírico de [[stanford-digital-economy-lab]] de que IA aumenta produtividade em tarefas específicas, não substitui julgamento humano em decisões de alta incerteza
- **Case com dados concretos**: $129K em 1 ano com emprego full-time + AMD/Palantir como exemplos verificáveis — aumenta credibilidade vs. afirmações sem comprovação do nicho

## Entidades relacionadas

- [[bert-no-chase]] — autor; trader e educador de swing trading para trabalhadores CLT

## Conceitos relacionados

- [[finanças-com-ia]] — terceira abordagem documentada: pipeline de screening com LLM para seleção de ações
- [[prompt-engineering]] — padrão de multi-prompt sequencial para funil de triagem em domínio especializado
