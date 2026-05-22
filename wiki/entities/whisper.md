---
title: "Whisper"
type: entity
category: tool
tags: [llm, transcrição, speech-to-text, open-source, openai, ferramentas-ia]
source_count: 1
last_updated: 2026-05-22
---

# Whisper

> **Categoria:** Ferramenta | **Tipo:** Modelo de reconhecimento de fala open-source (OpenAI)

## O que é

Whisper é o modelo de reconhecimento de fala de propósito geral da OpenAI, publicado como open-source. Treinado em 680K horas de dados de áudio diversificado, opera como modelo multitarefa:

- **Transcrição em inglês**
- **Tradução de fala de qualquer idioma para inglês**
- **Transcrição multilíngue** (99 idiomas)
- **Identificação de idioma**

## Posição no ecossistema

Ferramentas comerciais como Otter.ai ($20/mês) e Rev funcionam como wrappers em torno de capacidades similares às do Whisper. Usar o modelo diretamente — via Python, CLI ou integração no pipeline — reduz o custo a zero além do hardware.

## Relevância no wiki

O wiki documenta pipelines onde transcrição de áudio seria valiosa:
- [[jordan-lee]] (Sales Call Analyzer — análise de gravações de chamadas de vendas)
- [[nate-herk]] (compressão de sessões longas com contexto falado)

O Whisper oferece essa capacidade sem custo por minuto e sem dependência de serviço externo — complemento natural de [[ollama]] para pipelines de IA totalmente locais.

## Fontes

- [[2026-05-21_harish-bhatt-repos-ilegais]] — mencionado como alternativa gratuita ao Otter.ai ($20/mês), com suporte a 99 idiomas e tradução de fala
