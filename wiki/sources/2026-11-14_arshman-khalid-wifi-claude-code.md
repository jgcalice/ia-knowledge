---
title: "Claude Code para dobrar a velocidade do Wi-Fi"
type: source
source_file: "2026-11-14_arshman_khalid_Dftm7llOQ7T.md"
author: "@Arshman Khalid"
date: 2026-11-14
format: reel
tags: [claude, claude-code, automação, ferramentas-ia]
source_url: "https://www.instagram.com/reel/Dftm7llOQ7T/"
source_count: 1
---

# Claude Code para dobrar a velocidade do Wi-Fi

> **Fonte:** [[2026-11-14_arshman_khalid_Dftm7llOQ7T]] | **Autor:** @Arshman Khalid | **Data:** 2026-11-14 | **Formato:** reel (54s) | **[↗ Ver post](https://www.instagram.com/reel/Dftm7llOQ7T/)**

## TL;DR
Depois de reiniciar o roteador, trocar o cabo e falar com a operadora sem resultado, o autor diz que colou um prompt no Claude Code (dentro do Claude Desktop) e dobrou a velocidade do Wi-Fi, com o Claude pedindo aprovação antes de aplicar as correções.

## Contexto
Reel de @Arshman Khalid (ver [[arshman-khalid]]), que antes apresentou o CareerOps. CTA: comentar "WIFI" para receber o prompt. O prompt não aparece na fonte. Na transcrição, "Cloud" é erro de transcrição para "Claude".

## O que foi ensinado
- Abrir o Claude Desktop, selecionar a aba Claude Code e colar o prompt.
- O Claude roda um speed test e compara com a velocidade contratada.
- Se estiver abaixo, investiga configurações do computador e programas que consomem banda em segundo plano.
- Analisa o sinal e lista os dispositivos conectados, para identificar desconhecidos; o usuário aprova ou rejeita cada um.
- Verifica redes vizinhas para detectar conflito de canal com o roteador.
- Pede permissão antes de aplicar as correções. No teste do autor foram recomendadas 23 mudanças. Após a aprovação, aplica e refaz o speed test.

## Insights para o wiki
- Segunda fonte sobre Wi-Fi com Claude, junto com [[2026-11-09_harish-bhatt-7-prompts-wifi-claude]]. O fluxo é o mesmo (speed test, banda, dispositivos, canal, configurações), mas aqui vem num único prompt, e lá em sete.
- Reforça o human-in-the-loop: diagnóstico livre, mudanças só com aprovação.
- Diferença: o autor usa o Claude Code no Claude Desktop, e não o computer use.
- "Dobrou a velocidade" e "23 mudanças" são relatos de um único teste, sem números antes e depois e sem o prompt. Não verificado.

## Entidades relacionadas
- [[arshman-khalid]] — autor
- [[claude-code]] — executa o diagnóstico e as correções

## Conceitos relacionados
- [[agentes-ia]] — agente que diagnostica, propõe e aplica mudanças com aprovação
- [[prompt-engineering]] — prompt único com fluxo diagnóstico → aprovação → correção → reteste
