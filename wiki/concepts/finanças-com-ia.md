---
title: "Finanças com IA"
type: concept
tags: [finanças-com-ia, investimentos, análise-financeira, prompt-engineering, llm]
source_count: 1
last_updated: 2026-04-26
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

## Estado atual do wiki

Domínio com apenas 1 fonte (2026-04-26). Conceito-semente — aguarda expansão com mais fontes sobre finanças com IA.

## Fontes

- [[2026-04-26_faria-lima-elevator-ia-investimentos]] — 8 prompts com 8 instituições distintas, cobrindo o ciclo completo de análise financeira
