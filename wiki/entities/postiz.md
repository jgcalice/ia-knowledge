---
title: "Postiz"
type: entity
category: tool
tags: [open-source, automação, mídias-sociais, self-hosted, agentes-ia, n8n, criação-de-conteúdo, scheduling]
source_count: 1
last_updated: 2026-05-28
---

# Postiz

> **Categoria:** Ferramenta | **Tipo:** Plataforma open-source de gestão e automação de mídias sociais

## O que é

Postiz é uma plataforma open-source e self-hostada para gestão completa de redes sociais. Posicionada como alternativa gratuita a Buffer, Hootsuite e Sprout Social — com suporte nativo a automação por agentes de IA.

**Funcionalidades principais:**
- Agendamento de posts em 30+ plataformas
- Geração de legendas por IA
- Analytics de desempenho
- Colaboração de equipe
- Publicação cross-platform
- Workflows automatizados

**Plataformas suportadas:** X, LinkedIn, Instagram, TikTok, Threads, Reddit, YouTube, Discord, Bluesky e 20+ outras

## Stack de automação

| Recurso | Descrição |
|---------|-----------|
| Agent CLI | Suporte a linha de comando para integração com agentes |
| Public API | API aberta para integração com qualquer sistema |
| [[n8n]] | Integração nativa com fluxos de automação |
| Make.com | Suporte à plataforma de automação visual |
| Claude / AI agents | Compatível com Claude e agentes de IA customizados |

## Por que é relevante para o wiki

1. **Camada de distribuição para pipelines de conteúdo**: com suporte a Agent CLI e Public API, o Postiz pode ser o endpoint de distribuição em pipelines onde Claude escreve e o Postiz agenda/publica
2. **Confirmação do padrão open-source**: terceira grande categoria de SaaS substituída por solução self-hosted — após [[n8n]] (automação de workflows) e [[ollama]] (LLMs)
3. **Pipeline multi-agente de conteúdo**: a fonte documenta o modelo futuro: agente escreve → agente agenda → agente analisa → agente otimiza — tudo sem intervenção humana

## Modelo de uso documentado

O post de [[ask-gpts]] enquadra o Postiz como infraestrutura para "AI-managed content systems": diferente de "agendar um post", o objetivo é um sistema autônomo de criação e distribuição de conteúdo.

## Fontes

- [[2026-05-28_ask-gpts-postiz-social-media]] — introdução da ferramenta: 30+ plataformas, stack de automação, modelo futuro multi-agente, self-hosted sem taxas mensais
