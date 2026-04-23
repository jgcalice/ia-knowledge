---
title: "7 Hacks para Reduzir o Uso de Tokens do Claude em 80%"
type: source
source_file: "2026-04-18_evolving_ai_DXRkZseDSg1.md"
author: "@Evolving AI"
date: 2026-04-18
format: carousel
tags: [tokens, otimização, claude, prompt-engineering, haiku, sonnet, opus, pdf]
source_url: "https://www.instagram.com/p/DXRkZseDSg1/?igsh=MWVoeWdobXdpMmcxdg=="
source_count: 1
---

# 7 Hacks para Reduzir o Uso de Tokens do Claude em 80%

> **Fonte:** [[2026-04-18_evolving_ai_DXRkZseDSg1]] | **Autor:** @Evolving AI | **Data:** 2026-04-18 | **Formato:** Carousel (9 slides) | **[↗ Ver post](https://www.instagram.com/p/DXRkZseDSg1/?igsh=MWVoeWdobXdpMmcxdg==)**

## TL;DR

7 técnicas concretas para reduzir em até 80% o uso de tokens no Claude: prompts concisos, revisão de código com grafo, escolha inteligente de modelo, pré-processamento de PDFs, timing de sessão, compactação de contexto e horários de menor pico.

## Contexto

Newsletter de IA com +100k assinantes compartilha um carousel técnico com hacks acionáveis para otimizar o uso de tokens no Claude. Conteúdo em inglês voltado para power users.

## O que foi ensinado

### Hack 1 — Método "Caveman"
Prompt de sistema que proíbe o Claude de usar linguagem de preenchimento:
```
Reply in the most concise form possible. Skip pleasantries, preambles, and recaps of my question. No phrases like 'I'd be happy to', 'Great question', or 'Let me explain'. Drop articles and filler words wherever the meaning stays clear...
```
→ Reduz 30-50% dos tokens de output em respostas conversacionais

### Hack 2 — Code Review Graph
- Ferramenta: `github.com/tirth8205/code-review-graph`
- Usa Tree-sitter para mapear a estrutura do código
- Claude lê apenas arquivos afetados pela mudança, não o repositório inteiro
- Benchmarks: 8x menos tokens em revisões, até 49x em monorepos

### Hack 3 — Escolha de Modelo
| Modelo | Uso recomendado |
|--------|-----------------|
| Haiku | Lookups rápidos, classificação, formatação, tarefas simples em volume |
| Sonnet | Código, análise de dados, Q&A geral, sumarização |
| Opus | Trade-offs de arquitetura, debugging multi-arquivo, escrita longa e nuançada |

> Opus custa ~5x mais por token que Sonnet. Usar Sonnet para tarefas básicas é um dos maiores ganhos de eficiência.

### Hack 4 — Não fazer upload direto de PDFs
- PDFs consomem muito contexto (especialmente os com imagens ou scaneados)
- Solução: processar com modelo mais barato primeiro (Haiku, GPT-4o mini, ou ferramenta local)
- Prompt de compressão:
```
Read this document end to end. Output a condensed plain-text version that preserves: (1) all factual claims, numbers, dates, and names; (2) every actionable instruction or recommendation; (3) the document's structure as short headings. Drop filler phrases, repeated context, marketing language, formatting artifacts, and page headers/footers. Target 20 to 30 percent of the original length.
```
→ Alinhado com a recomendação do [[markitdown]] de [[rafael-brandao]]

### Hack 5 — Timing de Sessão
- A janela de uso do Claude.ai começa no primeiro token enviado
- Abrir a sessão apenas quando estiver pronto para trabalhar
- Concentrar o trabalho mais pesado na primeira metade da janela

### Hack 6 — Compact Skill (Compressão de Contexto)
Prompt para criar um resumo de continuação entre sessões:
```
Summarize our entire conversation so I can paste it into a new chat and continue without losing context. Include: (1) the original goal or problem, (2) key decisions made and why, (3) any code, config, or data we settled on verbatim in code blocks, (4) open questions and next steps.
```
→ Mantém continuidade sem carregar histórico longo

### Hack 7 — Evitar Horários de Pico
- Pior horário: dias úteis no horário comercial da sua região
- Melhor horário: fins de semana, noites, manhãs cedo
- Não muda o custo em tokens, mas reduz chance de rate limiting mid-task

## Insights para o wiki

- Hack 4 (PDFs) + recomendação do [[rafael-brandao]] = convergência de duas fontes independentes sobre o mesmo problema
- O Hack 1 (Caveman) é uma técnica de prompt de sistema reutilizável — pode ser salvo como snippet permanente
- A tabela Haiku/Sonnet/Opus é a referência de escolha de modelo mais clara encontrada até agora no wiki
- Hack 6 (Compact Skill) é especialmente relevante para este próprio workflow de wiki — sessões longas de ingestão se beneficiam disso

## Entidades relacionadas

- [[evolving-ai]] — autor do conteúdo
- [[claude-code]] — LLM sobre o qual os hacks se aplicam

## Conceitos relacionados

- [[otimização-de-tokens]] — tema central: 6 dos 7 hacks são sobre isso diretamente
- [[prompt-engineering]] — Hacks 1, 4 e 6 são essencialmente técnicas de prompt
