---
title: "Agentes de IA"
type: concept
tags: [agentes-ia, claude-code, automação, multi-agent, subagentes, tokens]
source_count: 7
last_updated: 2026-04-23
---

# Agentes de IA

> **Fontes:** 6 | **Domínio:** Arquitetura de sistemas de IA

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

### Agentes como serviço B2B (AIaaS)
[[bruno-wambier]] formaliza o modelo **Agente-as-a-Service**: IA configurada para atender empresas no WhatsApp — responde clientes, agenda, gera leads, vende — cobrada como assinatura mensal (~R$297/mês/cliente). Primeira menção no wiki a agente IA como **produto comercial empacotado**, não como ferramenta interna.
→ [[2026-04-07_5-negocios-automatizados-ia]]

### Claude Skills como micro-agentes distribuíveis
[[aashish-pahwa]] cataloga 6 skills (Feature Forge, Spec Miner, The Fool, Architecture Designer, API Designer, Microservice Architect) — cada uma opera como micro-agente especializado ativado por frase-gatilho. Marketplaces como [[smithery]] têm 128k+ skills — evidência de ecossistema maduro de agentes compartilháveis.
→ [[2026-04-07_claude-skills-product-managers]]

### Sub-agentes como estratégia de token management
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

Além de paralelizar trabalho, sub-agentes são uma estratégia primária para economizar tokens:
- Cada sub-agente tem **janela de contexto própria e fresca** — o agente principal não acumula o trabalho interno
- Podem usar modelos mais baratos: *"spin up a sub agent to summarize this using Haiku"*
- Analogia: pesquisador interno — o chefe só recebe o resumo, não lê os 50 artigos junto

Prompt simples de delegação: `"Spin up a sub agent to [tarefa] and make sure that sub agent is using Haiku"`

## Fontes

- [[2026-04-17_claude-update-task-assignment]]
- [[2026-04-14_marca-cloudcode-2horas]]
- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-05_5-videos-especialista-claude]]
- [[2026-04-07_5-negocios-automatizados-ia]]
- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-20_nate-herk-gerenciar-limites-sessao]]
