---
title: "5 Prompts Claude para Entrevistas de Emprego"
type: source
source_file: "2026-05-18_roshan_krishna_DYeuUzkk5IW.md"
author: "@Roshan Krishna"
date: 2026-05-18
format: carousel
tags: [carreira, entrevista, busca-de-emprego, prompt-engineering, star-method, claude, preparação]
source_url: "https://www.instagram.com/p/DYeuUzkk5IW/?img_index=6"
source_count: 1
---

# 5 Prompts Claude para Entrevistas de Emprego

> **Fonte:** [[2026-05-18_roshan_krishna_DYeuUzkk5IW]] | **Autor:** @Roshan Krishna | **Data:** 2026-05-18 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DYeuUzkk5IW/?img_index=6)**

## TL;DR

5 prompts Claude encadeados que preparam o candidato para uma entrevista do zero — prevendo as perguntas, construindo respostas, identificando fraquezas, simulando a entrevista e gerando um cheatsheet de 60 segundos para revisar antes de entrar na sala.

## Contexto

O autor conta que seu irmão tinha uma entrevista marcada para o dia seguinte e zero preparação. Ele enviou 5 prompts do Claude. O irmão afirma que eles previram quase todas as perguntas feitas na entrevista — e ele conseguiu a oferta. O carousel é uma versão viralizável do tweet que documentou os prompts.

## O que foi ensinado

**Prompt 1 — Prever as perguntas exatas:**
- Colar a JD completa e pedir as 15 perguntas mais prováveis
- Divididas em 3 categorias: Técnicas (5), Comportamentais STAR (5), Curva/Situacionais (5)
- Para cada pergunta: nota de uma linha sobre o que o entrevistador está realmente testando

**Prompt 2 — Construir respostas impactantes:**
- Para cada pergunta gerada no Prompt 1, criar uma resposta forte
- STAR para comportamentais; <90 segundos quando ditas em voz alta
- Usar `[INSERT YOUR STORY]` como placeholder onde uma história pessoal é necessária
- Instrução explícita: "Don't sound rehearsed. Sound confident but natural."

**Prompt 3 — Encontrar pontos fracos:**
- Analisar todas as respostas e identificar as 3 mais fracas
- Para cada fraqueza: o que está faltando + onde um entrevistador difícil faria follow-up
- Gerar as perguntas de follow-up e como tratá-las

**Prompt 4 — Simulação de entrevista (Brutal Mode):**
- Claude atua como entrevistador senior da vaga específica
- Uma pergunta por vez, aguarda resposta, depois pontua de 0 a 10
- Feedback: o que acertou + o que foi fraco + versão reescrita que pontuaria 9+
- "Don't go easy on me. Start when ready."

**Prompt 5 — Cheatsheet de 60 segundos:**
- Com base em tudo (JD + perguntas + respostas), gerar cheatsheet para revisar 10 minutos antes
- Contém: 3 pontos mais fortes, 2 histórias essenciais, a pergunta que o candidato mais pode travar + como salvar, linha de abertura confiante para "Tell me about yourself"

## Insights para o wiki

- **Pipeline de 5 prompts encadeados** — cada prompt usa o output do anterior como input. É a mesma estrutura sequencial já documentada em leads ([[derek-gray]]), produtos ([[luna-vega]]) e finanças ([[faria-lima-elevator]]), agora aplicada a entrevistas.
- **STAR como framework explícito**: primeiro uso do wiki onde STAR é invocado como instrução direta ao modelo (não apenas mencionado). O Prompt 2 instrui o LLM a usar STAR para perguntas comportamentais e a marcar com placeholder onde o candidato deve inserir história pessoal — design de delegação parcial.
- **"Brutal Mode" como padrão de feedback honesto**: o Prompt 4 instrui explicitamente "Don't go easy on me" — antítese do viés de complacência documentado em outros contextos ([[harish-bhatt]], feedback engineering). O score 0-10 + versão 9+ torna o gap acionável imediatamente.
- **Cheatsheet como artefato terminal**: o Prompt 5 sintetiza todo o pipeline anterior em um entregável para uso imediato — padrão de "síntese final acionável" também presente no plano diário de [[laura-anderson]] e no handoff de sessão de [[nate-herk]].
- Diferença em relação a [[your-ai-compass]] (reconstrução de candidatura): aquele foca no *perfil e currículo* antes da entrevista; este foca no *desempenho durante a entrevista* — são fases complementares da mesma jornada de emprego.

## Entidades relacionadas

- [[roshan-krishna]] — autor e originador dos prompts

## Conceitos relacionados

- [[busca-de-emprego-com-ia]] — 5ª fonte, foco em preparação para entrevista (fase pós-candidatura)
- [[carreira-com-ia]] — acrescenta a dimensão de performance em entrevistas ao cluster de carreira
- [[prompt-engineering]] — pipeline sequencial + STAR como instrução explícita + "Brutal Mode" como padrão de feedback
