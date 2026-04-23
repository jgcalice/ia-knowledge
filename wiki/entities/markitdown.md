---
title: "MarkItDown (Microsoft)"
type: entity
category: tool
tags: [markdown, conversão, documentos, tokens, pdf, otimização, microsoft]
source_count: 2
last_updated: 2026-04-21
---

# MarkItDown (Microsoft)

> **Categoria:** Ferramenta de conversão de documentos | **Fabricante:** Microsoft | **Aparece em:** 2 fontes

## O que é

MarkItDown é uma ferramenta open-source da Microsoft que converte qualquer tipo de arquivo em Markdown limpo e otimizado para consumo por LLMs. Tem mais de 100k stars no GitHub.

## Formatos suportados

PDF, Word (.docx), Excel (.xlsx), PowerPoint (.pptx), vídeos do YouTube (transcrição), áudio, imagens

## Por que usar com Claude

1. PDFs enviados diretamente ao Claude consomem tokens excessivos (o modelo lê o arquivo completo)
2. MarkItDown pré-processa o arquivo → gera Markdown limpo → Claude processa menos tokens
3. Resultado: redução de tokens + respostas mais precisas (texto limpo é mais fácil de interpretar)

## Relação com outras fontes

- [[rafael-brandao]] recomenda diretamente ([[2026-04-11_tokens-markdown]])
- [[evolving-ai]] recomenda abordagem similar no Hack #4 (usar modelo mais barato como intermediário) — MarkItDown é solução mais direta para o mesmo problema ([[2026-04-18_7-hacks-tokens-claude]])

## Fontes

- [[2026-04-11_tokens-markdown]]
- [[2026-04-18_7-hacks-tokens-claude]] (indireto — Hack #4)
