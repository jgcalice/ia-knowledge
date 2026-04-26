---
title: "Cookbook para Agente de Análise de Dados com Claude"
type: source
source_file: "2026-04-21_artificial_intelligence_ai_updater_DXZWWAjkmy9.md"
author: "@Artificial Intelligence (AI) Updater"
date: 2026-04-21
format: carousel
tags: [claude, agentes-ia, análise-de-dados, python, claude-managed-agents, ferramentas-ia]
source_url: "https://www.instagram.com/p/DXZWWAjkmy9/?img_index=11&igsh=MXZnemRjb3lid2tpMw=="
source_count: 1
---

# Cookbook para Agente de Análise de Dados com Claude

> **Fonte:** [[2026-04-21_artificial_intelligence_ai_updater_DXZWWAjkmy9]] | **Autor:** @Artificial Intelligence (AI) Updater | **Data:** 2026-04-21 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXZWWAjkmy9/?img_index=11&igsh=MXZnemRjb3lid2tpMw==)**

## TL;DR

A Anthropic lançou um cookbook mostrando como construir um agente de análise de dados com Claude Managed Agents: o usuário sobe um CSV e o agente devolve um relatório HTML interativo.

## Contexto

Post do canal @Artificial Intelligence (AI) Updater divulgando o lançamento de um cookbook oficial da Anthropic. O tutorial demonstra o uso de **Claude Managed Agents** — runtime hospedado para agentes com estado e uso de ferramentas — para automatizar análise de dados em CSV e geração de relatórios.

## O que foi ensinado

### Arquitetura dos Claude Managed Agents

Quatro conceitos centrais da plataforma:

| Conceito | O que é |
|----------|---------|
| **Agent** | Modelo + system prompt + ferramentas + MCP servers + skills |
| **Environment** | Container reutilizável com pacotes pré-instalados (ex: pandas, plotly) e configurações de rede |
| **Session** | Instância do agente em execução dentro de um environment |
| **Events** | Mensagens trocadas entre aplicação e agente (`user.message`, `agent.message`, tool calls) |

### Ferramentas disponíveis (`agent_toolset_20260401`)

8 ferramentas nativas: `bash`, `read`, `write`, `edit`, `glob`, `grep`, `web_fetch`, `web_search`  
*(no cookbook, as duas web ficam desativadas — análise offline)*

### Fluxo completo (5 passos)

1. **Criar Environment** — container reutilizável com pandas e plotly pré-instalados; rede irrestrita para CDN do plotly (usar allowlist em produção)
2. **Criar Agent** — combina modelo (`claude-sonnet-4-6`), system prompt de "analista sênior" e toolset com web desativado
3. **Upload do dataset** — CSV enviado via `client.beta.files.upload()`; retorna `file_id`
4. **Criar Session + enviar tarefa** — session conecta agent + environment + arquivo montado; análise inicia com `client.beta.sessions.events.send()`
5. **Stream da execução** — acompanhar eventos em tempo real via `client.beta.sessions.events.stream(session_id)`

### System prompt para analista de dados

```
You are a senior data analyst producing a publication-quality report.
Style: Professional, precise, curto parágrafo entre charts.
Execution: scripts .py rodados com python3; sample grandes tabelas; sempre set marker_color e template='simple_white'.
```

### Pré-requisitos

- Python 3.11+ e `anthropic>=0.91.0`
- ANTHROPIC_API_KEY configurada

## Insights para o wiki

- **Primeira fonte documentando Claude Managed Agents** — runtime hospedado oficial da Anthropic para agentes com estado; muda o paradigma de "montar stack próprio" para "usar plataforma gerenciada"
- **Environment como abstração de infraestrutura**: elimina setup de dependências por sessão — pacotes já instalados no container
- **Agente de dados como caso de uso canônico**: confirma o padrão "upload → agente autônomo → relatório" como template reutilizável
- **Streaming como observabilidade nativa**: `sessions.events.stream()` permite acompanhar tool calls e tokens ao vivo na Console — menos caixa-preta

## Entidades relacionadas

- [[claude-code]] — modelo usado (claude-sonnet-4-6) e plataforma central
- [[ai-updater]] — canal criador do conteúdo

## Conceitos relacionados

- [[agentes-ia]] — Claude Managed Agents como nova camada de runtime hospedado
