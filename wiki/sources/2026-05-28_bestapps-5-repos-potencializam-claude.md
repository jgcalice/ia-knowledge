---
title: "5 Repos GitHub que Potencializam o Claude para Criação de Conteúdo"
type: source
source_file: "2026-05-28_bestapps_artificial_intelligence_ai_agents_DY4X7EyjLXK.md"
author: "@Bestapps | Artificial Intelligence | AI Agents"
date: 2026-05-28
format: carousel
tags: [claude, claude-code, open-source, github, conteúdo, scraping, automação, vídeo, criação-de-conteúdo, agent-browser, firecrawl]
source_url: "https://www.instagram.com/p/DY4X7EyjLXK/?img_index=3&igsh=MWxlYmp0aWNoc3h0aA=="
source_count: 1
---

# 5 Repos GitHub que Potencializam o Claude para Criação de Conteúdo

> **Fonte:** [[2026-05-28_bestapps_artificial_intelligence_ai_agents_DY4X7EyjLXK]] | **Autor:** @Bestapps \| Artificial Intelligence \| AI Agents | **Data:** 2026-05-28 | **Formato:** carousel (8 slides) | **[↗ Ver post](https://www.instagram.com/p/DY4X7EyjLXK/?img_index=3&igsh=MWxlYmp0aWNoc3h0aA==)**

## TL;DR

5 repos open-source do GitHub — menos conhecidos, todos gratuitos — que expandem o Claude para criação de conteúdo: scraping (Firecrawl), encadeamento de tarefas (Superpowers), geração de vídeo (Remotion), automação de browser (Agent Browser) e escrita long-form com rubric (Claude Blog).

## Contexto

Bestapps.ai (@bestapps.ai, 170K seguidores, 600+ posts) posiciona o post como curadoria de repos que "os pros realmente usam" — em contraste com as 3 skills oficiais que aparecem em todas as listas. O enquadramento: "você está 6 meses adiantado" — 4 dos 5 repos têm menos de 50k estrelas porque são recentes.

## O que foi ensinado

### 1. Firecrawl
- API open-source para scraping em escala: pesquisar, extrair e interagir com a web
- Alimenta agentes IA com dados limpos: páginas de concorrentes, artigos, lançamentos de produtos
- Claude analisa os dados coletados diretamente
- Caso de uso: monitoramento competitivo automatizado

### 2. Superpowers (`obra/superpowers`)
- Terminal "supercharged" — extensível, rápido
- Permite encadear múltiplas tarefas em sequência sem perder o contexto
- Exemplo de prompt único: "pesquise este tópico, escreva 3 variações de hook, escolha a melhor, redija o carrossel"
- Resolve o problema crônico de Claude "esquecer" tarefas anteriores em sessões longas

### 3. Remotion (`remotion-dev/skills`) — 3.3k ⭐
- Gera vídeos verticais reais a partir de um prompt de texto
- Pipeline: escreve o código → renderiza o vídeo → entrega um MP4 pronto
- Elimina CapCut, After Effects e outros softwares de edição para conteúdo simples
- Caso de uso: reels e shorts gerados automaticamente pelo Claude

### 4. Agent Browser (`vercel-labs/agent-browser`) — 34k ⭐
- CLI de automação de browser para agentes de IA (Vercel Labs)
- Abre e opera uma janela real do Chrome como um humano
- Executa tarefas web complexas de forma autônoma — funciona em background
- 114 colaboradores, 2k forks

### 5. Claude Blog — 859 ⭐
- "Content Operating System" para posts long-form
- Recebe: voz do autor + audiência + tópico
- Processo: escreve o post + aplica rubric de 100 pontos antes de mostrar
- Resultado: escrita que não soa como IA — o rubric funciona como filtro de qualidade automático

## Insights para o wiki

- **Rubric como controle de qualidade autônomo**: Claude Blog introduz o padrão de "escrever + avaliar antes de mostrar" — primeira documentação no wiki de um agente que executa um ciclo de auto-avaliação baseado em critério explícito antes de entregar output.
- **Agent Browser como par do Vercel Labs**: complementa o find-skills [[pabloinpublic]] que já documentou o `vercel-labs/find-skills` — Vercel Labs aparece como produtor ativo de tools para o ecossistema Claude.
- **Superpowers resolve context rot para criadores**: o caso de uso descrito é análogo ao que [[nate-herk]] documenta como "session handoff" — mas resolvido via terminal em vez de estratégia de prompt.
- **Ângulo distinto do bestapps anterior**: o post de maio/2026 focava em substituir softwares de cinco dígitos (Bloomberg, HeyGen); este foca em potencializar Claude especificamente para **criadores de conteúdo de mídias sociais** — público diferente, problema diferente.

## Entidades relacionadas

- [[bestapps-ai]] — canal curador, 3ª contribuição ao wiki
- [[claude-code]] — plataforma central de todos os repos

## Conceitos relacionados

- [[agentes-ia]] — Agent Browser como agente de automação de browser
- [[estratégia-de-negócios-com-ia]] — repos como infraestrutura para criadores de conteúdo
- [[otimização-de-tokens]] — Superpowers resolve context rot via terminal
- [[prompt-engineering]] — Claude Blog rubric de 100 pontos como auto-avaliação
