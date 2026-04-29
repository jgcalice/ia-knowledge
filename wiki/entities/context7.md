---
title: "Context7 MCP"
type: entity
category: tool
tags: [mcp, documentação, claude-code, context-window, libraries]
source_count: 1
last_updated: 2026-04-29
---

# Context7 MCP

> **Categoria:** Ferramenta — Servidor MCP | **Tipo:** Servidor MCP de documentação | **Aparece em:** 1 fonte

## O que é

Servidor MCP que injeta documentação técnica atualizada e version-specific de milhares de bibliotecas populares diretamente no contexto do Claude antes de qualquer geração de código.

## Problema que resolve

O Claude tem um training cutoff — às vezes sugere funções, APIs ou flags que foram renomeadas, deprecadas ou não existem mais. O Context7 endereça isso fornecendo documentação live e version-specific.

## Como funciona

1. Instalar o servidor Context7 MCP (um comando)
2. Quando precisar de documentação de uma biblioteca, prompar o Claude para usar o servidor Context7
3. O servidor busca a documentação mais atualizada da lib solicitada e a injeta no contexto
4. Claude gera código baseado em documentação atual, não em dados de treinamento potencialmente desatualizados

## Bibliotecas cobertas

Documentação de até 8 versões por biblioteca de milhares de libs populares, incluindo:
- Next.js, React, MongoDB e outras populares no desenvolvimento web
- Qualquer lib que um assistente de código usaria frequentemente

## Fontes no wiki

- [[2026-04-27_nate-herk-32-hacks-claude-code]] — hack #32
