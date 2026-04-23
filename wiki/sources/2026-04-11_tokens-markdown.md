---
title: "Melhore o uso de tokens no Claude com Markdown"
type: source
source_file: "2026-04-11_rafael_brandao_DXAFtxUk2dl.md"
author: "@Rafael Brandão"
date: 2026-04-11
format: reel
duration_seconds: 59
tags: [tokens, markdown, otimização, claude, documentos, markitdown]
source_url: "https://www.instagram.com/reel/DXAFtxUk2dl/?igsh=MXZwem81MnV0bHJqdQ=="
source_count: 1
---

# Melhore o uso de tokens no Claude com Markdown

> **Fonte:** [[2026-04-11_rafael_brandao_DXAFtxUk2dl]] | **Autor:** @Rafael Brandão | **Data:** 2026-04-11 | **Formato:** Reel (59s) | **[↗ Ver post](https://www.instagram.com/reel/DXAFtxUk2dl/?igsh=MXZwem81MnV0bHJqdQ==)**

## TL;DR

Usar a ferramenta MarkItDown da Microsoft para converter PDFs, Word, Excel, PowerPoint, áudios e vídeos em Markdown limpo antes de enviar ao Claude reduz drasticamente o consumo de tokens e melhora a qualidade das respostas.

## Contexto

Rafael Brandão alerta que enviar PDFs diretamente ao Claude consome muito mais tokens do que o necessário, pois o modelo precisa processar o documento inteiro. A solução apresentada é o MarkItDown, ferramenta open-source da Microsoft com mais de 100k stars no GitHub.

## O que foi ensinado

- **Problema**: PDFs enviados diretamente ao Claude fazem o modelo ler o documento completo → consome muitos tokens → sessão acaba rápido
- **Solução**: [[markitdown]] — converte qualquer arquivo (PDF, Word, Excel, PowerPoint, vídeo YouTube, áudio, imagem) para Markdown limpo e otimizado
- **Benefício duplo**: 
  1. Reduz consumo de tokens
  2. Melhora qualidade das respostas (Claude interpreta texto limpo melhor que PDFs brutos)
- **Disponibilidade**: Gratuita, open-source, >100k stars no GitHub

> ⚠️ **Nota de precisão**: Rafael atribui o MarkItDown à "Microsoft", o que é correto (é um projeto Microsoft open-source), mas enquadra como solução para o Claude especificamente. Na prática, funciona com qualquer LLM.

## Insights para o wiki

- Confirma e complementa o Hack #4 de [[evolving-ai]] ("Don't Upload PDFs Directly To Claude") — ambos recomendam pré-processar documentos antes de enviar ao LLM
- O MarkItDown vai além do hack do Evolving AI (que usa outro LLM como intermediário): converte diretamente para Markdown sem precisar de outro modelo
- Tema de otimização de tokens aparece em **3 fontes diferentes** — sinal de que é uma dor real e frequente dos usuários de Claude

## Entidades relacionadas

- [[rafael-brandao]] — autor do conteúdo
- [[markitdown]] — ferramenta central recomendada
- [[claude-code]] — LLM cujo consumo de tokens é otimizado

## Conceitos relacionados

- [[otimização-de-tokens]] — tema principal do conteúdo
