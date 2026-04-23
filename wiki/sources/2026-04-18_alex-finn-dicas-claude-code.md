---
title: "7 Dicas para Dominar o Claude Code — Alex Finn"
type: source
source_file: "2026-04-18_alex_finn_8YhYtIF9PYI.md"
author: "@Alex Finn"
date: 2026-04-18
format: video
tags: [claude-code, claude, opus, auto-mode, prompt-engineering, adaptive-thinking, notificações, ferramentas-ia]
source_url: "https://youtu.be/8YhYtIF9PYI?si=IP5OqhegoH1noWax"
source_count: 1
---

# 7 Dicas para Dominar o Claude Code — Alex Finn

> **Fonte:** [[2026-04-18_alex_finn_8YhYtIF9PYI]] | **Autor:** @Alex Finn | **Data:** 2026-04-18 | **Formato:** Vídeo (YouTube, 13min) | **[↗ Ver vídeo](https://youtu.be/8YhYtIF9PYI?si=IP5OqhegoH1noWax)**

## TL;DR

Boris Cherny (criador do Claude Code) revelou 7 segredos para extrair o máximo do Claude Code e Opus 4.7 — Alex Finn os demonstra ao vivo construindo um clone do Linear em Next.js.

## Contexto

Boris Cherny (`@bcherny` no X) publicou um thread e um blog post com as melhores práticas para Opus 4.7 com Claude Code. Alex Finn traduz esses insights em demonstração prática, construindo um app completo do zero no CLI do Claude Code.

## O que foi ensinado

### Dica 1 — Auto Mode
- Ativar: `Shift+Tab` → `Shift+Tab` → `Shift+Tab` no CLI (terceiro estado)
- Claude Code passa a decidir permissões autonomamente, sem pedir aprovação a cada passo
- Permite sessões contínuas de horas sem interrupção
- Recomendado como **modo padrão** para usuários frequentes

### Dica 2 — Frontload Information
- Opus 4.7 é muito melhor em seguir instruções complexas de uma vez só
- Em vez de enviar instruções incrementais ("passo 1, passo 2..."), enviar tudo em um único prompt detalhado
- Combinado com Auto Mode, o modelo executa todo o plano sem pedir confirmação

### Dica 3 — /recap
- Comando `/recap` gera um resumo de uma linha de tudo que o agente fez na sessão
- Útil após sessões longas, ou quando o Claude rodou durante a noite
- Permite retomar o contexto rapidamente sem reler o histórico completo

### Dica 4 — /effort
- Comando `/effort` configura o nível de esforço por tarefa
- Níveis disponíveis: low / medium / high / **extra high** / **max**
- Recomendação de Alex Finn:
  - **Max**: para o prompt inicial que lança o app (frontload completo)
  - **Extra High**: para a maioria das tarefas durante o desenvolvimento
  - **High/Medium/Low**: apenas para planos mais baratos ou tarefas triviais (ex: mudar cor de botão)

### Dica 5 — Notificações
- Pedir ao Claude para configurar notificações: `"after every piece of work you do, please send me a notification"`
- O Claude configura automaticamente um hook que envia ping ao finalizar tarefas longas
- Permite trabalhar em paralelo (ex: chattar com Opus no desktop) e retornar ao foco quando o trabalho está pronto

### Dica 6 — Adaptive Thinking via Prompts
- Opus 4.7 removeu o toggle de "extended thinking" presente no Opus 4.6
- Agora o nível de reflexão é controlado por prompts:
  - Tarefa complexa: `"think carefully step by step"`
  - Tarefa simples: `"prioritize responding quickly rather than thinking deeply"`
- A combinação `/effort` + instrução de thinking cobre dois eixos:
  - **Esforço total** (quanto tempo na tarefa completa) → `/effort`
  - **Profundidade de raciocínio por microtarefa** → instrução no prompt

### Dica 7 — Vibe Coding com Opus no Chat
- Enquanto Claude Code roda tarefas longas, usar o modo chat do Claude Desktop com Opus 4.7
- Opus 4.7 considerado pelo autor como superior ao ChatGPT para brainstorming de negócios
- Workflow: task longa no CLI → aguardar notificação → chat estratégico no Desktop em paralelo

## Insights para o wiki

- **Novo modelo mental**: Claude Code em Auto Mode funciona como um empregado confiável que pode trabalhar horas sem supervisão — muda fundamentalmente o workflow de "babysitting" para "delegação real"
- **Adaptive Thinking confirma tendência**: controle via linguagem natural (prompts) ao invés de toggles de UI → alinha com o princípio de [[prompt-engineering]] como interface principal
- **Opus 4.7** marca uma ruptura com versões anteriores: sem extended thinking explícito, com Auto Mode nativo e granularidade de esforço configurável
- **/recap** e **/effort** são comandos built-in ainda pouco documentados no wiki, complementando o catálogo de [[sal-shirgaleev]]

## Entidades relacionadas

- [[claude-code]] — ferramenta central demonstrada em todos os 7 tips
- [[alex-finn]] — autor do vídeo, criador de conteúdo sobre Claude Code

## Conceitos relacionados

- [[prompt-engineering]] — adaptive thinking via prompts, frontload information
- [[agentes-ia]] — auto mode como habilitador de sessões autônomas prolongadas
- [[otimização-de-tokens]] — /effort como controle granular de custo computacional
