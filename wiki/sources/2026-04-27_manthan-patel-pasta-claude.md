---
title: "Estrutura da Pasta .claude: O Sistema de Infraestrutura do Claude Code"
type: source
source_file: "2026-04-27_manthan_patel_lead_gen_man_DXpO61yDZ1m.md"
author: "@Manthan Patel | Lead Gen Man"
date: 2026-04-27
format: single_image
tags: [claude-code, claude-md, hooks, skills, agentes-ia, plugins, infraestrutura]
source_url: "https://www.instagram.com/p/DXpO61yDZ1m/?igsh=YW5jc3Vxdmt4YXFj"
source_count: 1
---

# Estrutura da Pasta .claude: O Sistema de Infraestrutura do Claude Code

> **Fonte:** [[2026-04-27_manthan_patel_lead_gen_man_DXpO61yDZ1m]] | **Autor:** @Manthan Patel | Lead Gen Man | **Data:** 2026-04-27 | **Formato:** imagem única | **[↗ Ver post](https://www.instagram.com/p/DXpO61yDZ1m/?igsh=YW5jc3Vxdmt4YXFj)**

## TL;DR

A pasta `.claude/` deixou de ser uma caixa preta e se tornou o núcleo do setup — cada subdiretório tem um papel distinto e bem definido no sistema de infraestrutura do Claude Code.

## Contexto

Terceiro post de [[manthan-patel]] no wiki. Enquanto o primeiro abordou os princípios do CLAUDE.md de [[boris-cherny]] e o segundo sistematizou o "Agent Development Kit" em 5 camadas, este foca na **anatomia física da pasta `.claude/`**: o que vai onde e por quê. A distinção central é operacional — CLAUDE.md é consultivo, hooks são obrigatórios.

## O que foi ensinado

- **`.claude/CLAUDE.md`** — regras advisory: o modelo lê e *pode* seguir; define comportamentos esperados, convenções e contexto do projeto
- **`.claude/hooks/`** — scripts determinísticos: sempre executam, independentemente do modelo; o sistema força, a IA não escolhe
- **`.claude/commands/`** — atalhos de barra: comandos `/` que disparam workflows predefinidos dentro da sessão
- **`.claude/skills/`** — workflows reutilizáveis: carregados sob demanda por description-matching, injetam contexto especializado na sessão principal
- **`.claude/agents/`** — tarefas isoladas: agentes com contexto próprio, o agente principal só recebe o resultado final
- **`.claude/plugins/`** — empacotamento: agrupa tudo (skills + agents + hooks + commands) em artefato distribuível
- **Princípio central**: *"The folder structure IS the system"* — a organização física dos arquivos é a arquitetura de comportamento do agente

## Insights para o wiki

**Clarificação crítica sobre CLAUDE.md vs. hooks**: o wiki já documentava a distinção técnica via [[2026-04-30_manthan-patel-agent-development-kit]], mas este post a torna explícita de forma editorial — "CLAUDE.md is advisory. hooks are deterministic." Isso resolve uma ambiguidade frequente: desenvolvedores tendem a tratar o CLAUDE.md como regras obrigatórias, quando na verdade são recomendações que o modelo pode ignorar em contextos extremos. Apenas hooks garantem execução.

**Primeiro infográfico do wiki com o layout físico completo da pasta `.claude/`**: os posts anteriores listavam os componentes como camadas abstratas; este mostra a estrutura de diretórios concreta — informação acionável para quem está montando seu setup.

**Confirmação e extensão do Agent Development Kit**: o post de 2026-04-30 descrevia as 5 camadas como conceito; este as ancora em localização física (`hooks/`, `commands/`, `skills/`, `agents/`, `plugins/`), tornando a taxonomia implementável sem ambiguidade.

## Entidades relacionadas

- [[manthan-patel]] — autor; terceira contribuição ao wiki
- [[claude-code]] — ferramenta central documentada
- [[boris-cherny]] — criador do CLAUDE.md de referência mencionado indiretamente

## Conceitos relacionados

- [[agentes-ia]] — infraestrutura física da pasta `.claude/` como sistema de agentes
- [[prompt-engineering]] — distinção advisory (CLAUDE.md) vs. determinístico (hooks)
