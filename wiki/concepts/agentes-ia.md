---
title: "Agentes de IA"
type: concept
tags: [agentes-ia, claude-code, automação, multi-agent, subagentes]
source_count: 4
last_updated: 2026-04-21
---

# Agentes de IA

> **Fontes:** 4 | **Domínio:** Arquitetura de sistemas de IA

## Definição

Sistemas baseados em LLMs que executam tarefas de forma autônoma, podendo integrar ferramentas externas, chamar outros agentes e tomar decisões sequenciais sem intervenção humana constante.

## O que foi documentado

### Claude como agente executor (não apenas chat)
[[ross-fledderjohn]] documenta mudança fundamental: Claude está migrando de ferramenta de conversa para ferramenta de delegação de trabalho:
- Antes: "converse com Claude"
- Agora: "atribua trabalho ao Claude"
→ [[2026-04-17_claude-update-task-assignment]]

### Arquitetura multi-agent para branding
[[rafael-brandao]] usa 120+ agentes especializados em pipeline para criar marca completa em 2h:
- Time de Brand → essência da marca
- Time de Copy → textos
- Time de Design → brandbook
→ [[2026-04-14_marca-cloudcode-2horas]]

### Agentes para busca de emprego
[[career-ops]] usa Claude Code para orquestrar pipeline de job search: escaneamento, avaliação, customização de currículo, rastreamento
→ [[2026-04-07_career-ops-busca-emprego-ia]]

### Cursos para aprender a construir agentes
- Nick Saarev: subagentes, agent teams, MCP (4h, YouTube)
- Greg Isenberg: "Building AI Agents that actually work"
- KJ Rainey: "Claude Cowork: Zero to Working AI Employee"
→ [[2026-04-05_5-videos-especialista-claude]]

## Fontes

- [[2026-04-17_claude-update-task-assignment]]
- [[2026-04-14_marca-cloudcode-2horas]]
- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-05_5-videos-especialista-claude]]
