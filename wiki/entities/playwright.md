---
title: "Playwright (MCP)"
type: entity
category: tool
tags: [playwright, mcp, testes, qa, claude-code, vibecoding]
source_count: 1
last_updated: 2026-08-19
---

# Playwright (MCP)

> **Categoria:** Framework de automação de testes (Microsoft) · **Papel no wiki:** MCP que permite ao Claude testar sites automaticamente antes da entrega

## O que é

Playwright é um framework open-source de automação de navegador usado tradicionalmente para testes end-to-end de aplicações web. Via MCP, o Claude consegue abrir e navegar o site que acabou de gerar para verificar se ele funciona antes de entregá-lo ao usuário.

## Papel no stack documentado

Componente de **QA automatizado** no setup de [[vinicius-delmonego]] para sites profissionais com Claude: depois que o MCP [[figma]] monta o site, o Playwright testa automaticamente o resultado. Paralelo conceitual ao quality gate do GSD ([[nate-herk]]) — mas aplicado a verificação visual/funcional de um site em vez de código de backend.

## Conexões no wiki

- [[claude-code]] — ambiente que consome o MCP
- [[figma]] — MCP anterior no pipeline (montagem → teste)
- [[vibecoding]] — QA automatizado como nova peça do stack de vibe coding

## Fontes

- [[2026-08-19_vinicius-delmonego-sites-claude]]
