---
title: "Finanças com IA"
type: concept
tags: [finanças-com-ia, investimentos, análise-financeira, prompt-engineering, llm, trading]
source_count: 3
last_updated: 2026-04-30
---

# Finanças com IA

> **Fontes:** 1 | **Domínio:** Aplicação de LLMs em análise financeira e de investimentos

## Definição

Uso de LLMs — via técnicas de prompt engineering — para executar análises financeiras de nível institucional, substituindo ou complementando dicas de gurus e relatórios de casas de investimento tradicionais.

## Abordagem documentada: Instituição como ROLE

A técnica central é usar o nome de uma instituição financeira de elite como ROLE no prompt. O modelo já carrega as metodologias publicadas por essas casas (relatórios, whitepapers, livros, entrevistas) como conhecimento semântico — nomear a instituição convoca o framework correspondente sem precisar descrevê-lo.

| Instituição (ROLE) | Análise ativada | Artefato de saída |
|---|---|---|
| Goldman Sachs | Stock Screener multi-critério | Relatório profissional de stock picking |
| Morgan Stanley | Valuation por DCF (M&A style) | Valuation memo com tabelas |
| Bridgewater | Risk management e stress test | Risk management report com heat map |
| JPMorgan | Pre-earnings brief (equity research) | Pre-earnings brief com resumo executivo |
| BlackRock | Portfólio multi-asset com policy statement | Documento de política de investimento |
| Citadel | Análise técnica quantitativa | Technical analysis report card |
| Harvard Endowment | Carteira de dividendos com DRIP | Dividend portfolio blueprint |
| Bain | Análise competitiva setorial | Bain-style strategy deck summary |

## Princípio subjacente

O modelo tem memória semântica das metodologias publicadas por essas instituições. Usar o nome como ROLE é uma forma compacta de convocar esse conhecimento acumulado sem precisar descrever o método — o mesmo mecanismo que faz "MECE" ou "Steelman" funcionarem como ativadores semânticos em [[prompt-engineering]].

## Conexão com padrões gerais de prompt engineering

Confirma e estende o padrão ROLE/TASK/STEPS/RULES/OUTPUT documentado em [[prompt-engineering]]: em finanças, a escolha do ROLE (instituição ou gestor) é especialmente poderosa porque as metodologias de análise financeira são bem codificadas e amplamente documentadas publicamente. Difere do padrão de *pessoas* (Paul Graham, Tim Ferriss, Naval Ravikant) — aqui a autoridade é a firma, não o indivíduo.

## Segundo ângulo documentado: ChatGPT para construção de riqueza individual

@Derek Gray publica carousel sobre uso de ChatGPT para construção de riqueza pessoal ("Are you using ChatGPT to build wealth?"). Contraste com a abordagem da Faria Lima Elevator:

| Dimensão | Faria Lima Elevator | Derek Gray |
|----------|--------------------|-----------:|
| Foco | Análise institucional (portfólio, valuation, risk) | Construção de riqueza pessoal |
| Ferramenta | ChatGPT / Claude (qualquer LLM) | ChatGPT |
| Público-alvo | Investidor sofisticado | Público geral |
| Conteúdo no wiki | Completo (8 prompts detalhados) | Parcial (apenas título) |

> **Nota:** O caption menciona "ChatGPT 5.5" — modelo inexistente até 2026-04-28. Possível clickbait ou erro do criador.

## Terceira abordagem: Pipeline de screening sequencial para seleção de ações

@Bert (No-Chase Swing Trading for 9-5s) documenta um pipeline de 3 prompts para encontrar e selecionar ações em menos de 5 minutos — diferente das abordagens anteriores por focar em *seleção eficiente de candidatos* antes de qualquer análise aprofundada.

| Prompt | Entrada | Saída |
|--------|---------|-------|
| #1 — Construtor de universo | Tema de mercado (ex: IA, energia, semis) | Lista de 25 ações relacionadas ao tema |
| #2 — Ranqueador | Lista de 25 ações | Ranking por qualidade do negócio + desconto de preço |
| #3 — Deep dive | Top 3 ranqueados | Análise completa: pontos fortes, por que está barata, catalisador, riscos |

**Limitação explicitamente reconhecida:** IA não é eficaz no *timing* de entrada — essa etapa exige leitura de gráfico + análise técnica humana. A combinação IA (triagem fundamentalista) + chart reading (timing) é o diferencial do método.

**Compatível com Claude, ChatGPT ou Gemini.**

Fonte: [[2026-04-30_bert-swing-trading-ia]] | [[bert-no-chase]]

## Padrão estrutural comparativo entre as três abordagens

| Abordagem | Técnica central | Público | Limitações reconhecidas |
|-----------|-----------------|---------|------------------------|
| Institucional (ROLE) | Nomear instituição → convoca metodologia publicada | Investidor sofisticado | Nenhuma mencionada |
| Riqueza individual | ChatGPT para construção de patrimônio | Público geral | Parcial (conteúdo incompleto) |
| Screening sequencial | Pipeline funil (tema → 25 → top 3 + deep dive) | Trabalhador CLT / swing trader | Timing de entrada permanece humano |

## Estado atual do wiki

Domínio com 3 fontes. Três ângulos distintos: análise financeira institucional via ROLE (Faria Lima Elevator), construção de riqueza individual via ChatGPT (Derek Gray — parcial), e pipeline de screening para seleção de ações (Bert).

## Fontes

- [[2026-04-26_faria-lima-elevator-ia-investimentos]] — 8 prompts com 8 instituições distintas, cobrindo o ciclo completo de análise financeira
- [[2026-04-28_derek-gray-chatgpt-wealth]] — carousel sobre ChatGPT para construção de riqueza (ingestão parcial)
- [[2026-04-30_bert-swing-trading-ia]] — pipeline de 3 prompts para screening e seleção de ações em 5 minutos
