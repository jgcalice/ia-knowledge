---
title: "Plugin de Forrest Chang corrige os 3 problemas do Claude Code"
type: source
source_file: "2026-04-15_max_kelley_DXKu9xViZsM.md"
author: "@Max Kelley"
date: 2026-04-15
format: reel
tags: [claude-code, plugins, vibe-coding, github, agentes-ia]
source_url: "https://www.instagram.com/reel/DXKu9xViZsM/?igsh=ZDZ6bnB0ZDltNjI3"
source_count: 1
---

# Plugin de Forrest Chang corrige os 3 problemas do Claude Code

> **Fonte:** [[2026-04-15_max_kelley_DXKu9xViZsM]] | **Autor:** @Max Kelley | **Data:** 2026-04-15 | **Formato:** reel (64s) | **[↗ Ver post](https://www.instagram.com/reel/DXKu9xViZsM/?igsh=ZDZ6bnB0ZDltNjI3)**

## TL;DR

O "godfather of Vibe coding" apontou 3 problemas crônicos do Claude Code (suposições silenciosas, complexidade excessiva, regressões); o dev Forrest Chang empacotou as soluções em um repositório (~42k stars no GitHub) instalável como plugin do Claude Code via comando único no terminal.

## Contexto

Max Kelley faz o típico reel de divulgação "comment AI" (lead magnet por DM) — o repo e o install command não são revelados publicamente no vídeo. Mesmo assim, o conteúdo identifica três falhas reais e amplamente reclamadas do Claude Code e aponta para uma resposta da comunidade que virou tração (42,3k stars em poucas semanas).

## O que foi ensinado

Os 3 problemas do Claude Code, segundo o "padrinho do Vibe coding":

1. **Suposições silenciosas** — o modelo escolhe sozinho o que você "deve ter querido dizer" e segue em frente sem perguntar
2. **Sobre-engenharia** — você pede uma mudança pequena e ele escreve mil linhas
3. **Regressões em cascata** — corrigir uma coisa quebra três outras

O developer **Forrest Chang** publicou no GitHub um repositório que endereça os três pontos como **Claude Code plugin** — instalável com uma linha no terminal. Tem ~42,3k stars (39k no momento do vídeo).

## Insights para o wiki

- **3 problemas operacionais documentados pela primeira vez no wiki**: até aqui as fontes destacavam *o que Claude Code faz* (skills, hooks, sub-agentes); esta é a primeira a nomear *o que Claude Code falha em fazer por padrão* — assunção silenciosa, hipertrofia de código, regressão.
- **Plugin como remédio comportamental, não como feature**: os 5 níveis do Agent Development Kit ([[2026-04-30_manthan-patel-agent-development-kit]]) já incluíam *Plugins (pacotes npm)* como camada de distribuição; aqui o plugin é usado para *corrigir comportamento default* — não para adicionar capacidade nova. Padrão novo.
- **Reels com "comment X for the link" são um gargalo do wiki**: dois links críticos (nome do repo e install command) ficaram fora do conteúdo. Limita o aprofundamento — mas o sinal de tração (42k stars em ~semanas) é informação acionável: vale auditar o ecossistema de plugins do Claude Code para identificar o repositório citado.
- **Convergência com princípios do CLAUDE.md de [[boris-cherny]]**: os 3 problemas listados são exatamente o que os princípios *Simplicity*, *No Laziness* e *Minimal Impact* do CLAUDE.md de referência tentam mitigar. O plugin de Forrest Chang parece ser a versão *embarcada* desses princípios — em vez de depender do dev escrever CLAUDE.md, vem pré-configurado via npm.
- **"Godfather of Vibe coding"**: epíteto não atribuído explicitamente, mas no contexto do wiki o termo se aplica historicamente a [[andrej-karpathy]] (popularizou o "vibe coding" como prática) — provável autor da crítica original.

## Entidades relacionadas

- [[max-kelley]] — criador da fonte (divulgação)
- [[forrest-chang]] — autor do plugin (primeira aparição no wiki)
- [[claude-code]] — alvo do plugin
- [[andrej-karpathy]] — provável "padrinho do Vibe coding" referenciado

## Conceitos relacionados

- [[agentes-ia]] — plugins como camada de comportamento default
- [[prompt-engineering]] — três falhas que o engineering precisa contornar manualmente sem o plugin
