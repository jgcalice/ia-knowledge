---
title: "OpenWA"
type: entity
category: tool
tags: [whatsapp, open-source, self-hosted, api, webhooks, docker, automação]
source_count: 1
last_updated: 2026-06-28
---

# OpenWA

> **Repositório:** `github.com/rmyndharis/OpenWA` | **Licença:** MIT | **Tipo:** Ferramenta open-source de comunicação

## O que é

API de WhatsApp 100% open-source e auto-hospedada. Permite enviar e receber mensagens WhatsApp via REST API sem pagar por mensagem — ao contrário da API oficial do WhatsApp Business.

## Funcionalidades principais

| Recurso | Descrição |
|---------|-----------|
| Contas ilimitadas | Múltiplas contas WhatsApp em uma única instância |
| REST API | Endpoint HTTP para envio de mensagens, mídias e reações |
| Webhooks | Receber eventos de mensagens em tempo real |
| Painel React | Dashboard web com audit logs |
| Backend plugável | Arquitetura extensível para integrações customizadas |
| Deploy via Docker | Um único `docker run` para subir toda a stack |

## Modelo de custo

- **Custo de mensagem:** $0 (vs. cobrança por mensagem da API oficial)
- **Infraestrutura:** custo do servidor próprio (VPS, Cloud Run, etc.)
- **Licença:** MIT — sem restrições comerciais

## Relevância para o wiki

O OpenWA é o primeiro representante no wiki de automação de WhatsApp. Combinado com agentes Claude via REST API + Webhooks, habilita pipelines como:
- Outreach de leads por WhatsApp (extensão dos Métodos do [[geração-de-leads-com-ia]])
- Onboarding automatizado de clientes
- Notificações e alertas de agentes (follow-ups, alertas de portfólio via [[finanças-com-ia]])

## Fontes no wiki

- [[2026-06-14_marc-kaz-openwa-api-whatsapp]] — apresentação inicial por [[marc-kaz]]
