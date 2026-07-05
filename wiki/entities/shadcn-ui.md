---
title: "ShadCN UI"
type: entity
category: tool
tags: [vibecoding, componentes, ui, react, desenvolvimento, frontend]
source_count: 1
last_updated: 2026-06-28
---

# ShadCN UI — Biblioteca de Componentes Base para Vibe Coders

> Biblioteca de componentes de UI para React/Next.js descrita como "a base layer que quase todo vibe coder usa" — componentes bonitos e prontos que ficam no código do projeto (não como pacote externo).

## O que é

ShadCN UI é uma coleção de componentes reutilizáveis construídos sobre Radix UI e Tailwind CSS. Diferente de bibliotecas tradicionais (Material UI, Chakra), o ShadCN:

- **Não é instalado como dependência**: os componentes são copiados para o projeto, ficando no código do usuário
- **Customizável por design**: o código está no projeto, então pode ser modificado diretamente pelo LLM
- **Compatível com Claude Code**: o LLM consegue ler e modificar os componentes como qualquer outro arquivo

## Por que é a "base layer" do vibecoding

A característica de "código no projeto" (não em node_modules) é especialmente valiosa para vibecoding: o Claude Code pode ver, ler, adaptar e estender qualquer componente. Bibliotecas trancadas em pacotes são caixas pretas para o LLM; ShadCN não é.

## Fontes

- [[2026-06-28_joaquin-fernandez-ferramentas-vibecoding-ios]] — descrito como "base layer almost every vibe coder is building on right now" (via @Joaquin Fernandez)
