---
title: "As 5 Camadas do Desenvolvimento de Agentes com Claude"
type: source
source_file: "2026-04-30_manthan_patel_lead_gen_man_DXxAsiXDQ9L.md"
author: "@Manthan Patel | Lead Gen Man"
date: 2026-04-30
format: carousel
tags: [claude-code, agentes-ia, claude-md, skills, hooks, subagentes, plugins, prompt-engineering]
source_url: "https://www.instagram.com/p/DXxAsiXDQ9L/?img_index=6&igsh=czJ4amd6OTM5eDRs"
source_count: 1
---

# As 5 Camadas do Desenvolvimento de Agentes com Claude

> **Fonte:** [[2026-04-30_manthan_patel_lead_gen_man_DXxAsiXDQ9L]] | **Autor:** @Manthan Patel | Lead Gen Man | **Data:** 2026-04-30 | **Formato:** carousel (7 slides) | **[↗ Ver post](https://www.instagram.com/p/DXxAsiXDQ9L/?img_index=6&igsh=czJ4amd6OTM5eDRs)**

## TL;DR

O "Agent Development Kit" organiza o Claude Code em 5 camadas hierárquicas — CLAUDE.md, Skills, Hooks, Subagents e Plugins — cada uma com localização, função e artefatos próprios, formando uma arquitetura completa de agente autônomo e distribuível.

## Contexto

Segunda contribuição de [[manthan-patel]] ao wiki (a primeira foi sobre os princípios do CLAUDE.md de Boris Cherny). Aqui ele sistematiza a visão mais completa de infraestrutura de agentes documentada até hoje — abrangendo desde a "constituição" (CLAUDE.md) até a distribuição em equipe (Plugins).

## O que foi ensinado

### Camada 1 — CLAUDE.md (Memória / Constituição)
- **O que é**: arquivo sempre carregado, sempre ativo. É a "constituição do agente".
- **Onde vive** (dois escopos):
  - **Global** (`~/.claude/CLAUDE.md`): carregado em todos os projetos — voz/estilo padrão, ferramentas pessoais, preferências
  - **Project** (`.claude/CLAUDE.md`): carregado só neste repo — regras de arquitetura, convenções de naming, o que o agente esqueceria sem isso
- **O que colocar**: `architecture.rules`, `naming.conventions`, `test.expectations`, `repo.map`
- **Princípio**: escrever uma vez = economizar 100 prompts futuros

### Camada 2 — Skills (Conhecimento Sob Demanda)
- **O que é**: contexto modular, ativado por descrição (description-matched), carregado apenas quando necessário
- **Onde vive**: `~/.claude/skills/` — reutilizável entre projetos; inclui scripts, templates, assets (PDF, vídeo, Excalidraw)
- **Mecanismo**: `"convert this PDF"` → Claude seleciona skill `pdf-skill` que descreve "Read and convert PDF files"
- **Princípio**: uma skill conectada → qualquer sessão futura já sabe executar aquela tarefa

### Camada 3 — Hooks (Controle Determinístico)
- **O que é**: shell scripts que disparam em eventos de agente — **não é IA**, é execução determinística
- **Como dispara**: matcher define padrão da chamada de ferramenta (wildcards, regex, exato); command executa o script
- **Tipos de hooks disponíveis**:
  - `PreToolUse.sh` — antes de qualquer chamada de ferramenta
  - `PostToolUse.sh` — após execução de ferramenta
  - `SessionStart.sh` — ao iniciar sessão
  - `Stop.sh` — ao parar agente
  - `SubagentStop.sh` — ao parar sub-agente
- **Princípio**: hooks transformam intenções vagas em regras rígidas — a diferença entre um agente que sugere e um que obedece

### Camada 4 — Subagents (Delegação)
- **O que é**: instâncias do Claude com janela de contexto própria — o agente principal delega sem poluir sua sessão
- **Modelo pai/filho**:
  - **Pai** (sessão principal): planeja, chama sub-agentes como ferramentas, permanece limpo — só vê resultados
  - **Filho** (subagent run): system prompt próprio + ferramentas + contexto fresh; executa e retorna **uma mensagem**
- **Exemplos de sub-agentes especializados**:
  - `code-reviewer.md` — revisa diffs contra convenções do repo
  - `test-runner.md` — executa suite e relata falhas
  - `explorer.md` — mapeia codebase e retorna achados
  - `feature-dev.md` — projeta e implementa de ponta a ponta
- **Princípio**: "Delegue o ruído. Mantenha o fio principal limpo."

### Camada 5 — Plugins (Distribuição)
- **O que é**: pacotes npm que empacotam capacidades de agente para distribuição em equipe
- **Estrutura**: `plugin.json` (manifest) declara nome, versão e lista de skills; pode conter skills, agents, hooks e commands
- **Princípio**: "Build it once. Install it everywhere. The team levels up together."

## Insights para o wiki

- **Primeira taxonomia completa de infraestrutura de agente** no wiki — cobre desde memória persistente (CLAUDE.md) até distribuição (Plugins), passando por controle determinístico (Hooks)
- **Hooks como camada nova**: nenhuma fonte anterior documentou hooks com esta profundidade — cinco tipos de evento com matcher pattern + command. É o elo que faltava entre "o agente sabe o que fazer" (CLAUDE.md/Skills) e "o agente é forçado a seguir regras" (Hooks)
- **Plugins como npm**: a analogia com ecossistema npm é significativa — skills e agentes viram pacotes versionados e assinados, instaláveis em qualquer máquina da equipe
- **Complementa e sistematiza** [[2026-04-17_manthan-patel-claudemd-boris-cherny]] (que focava só no CLAUDE.md de [[boris-cherny]]) — agora temos o quadro completo de 5 camadas

## Entidades relacionadas

- [[manthan-patel]] — autor, segunda contribuição
- [[boris-cherny]] — contexto: CLAUDE.md de referência (Anthropic)
- [[claude-code]] — plataforma central de todas as camadas

## Conceitos relacionados

- [[agentes-ia]] — arquitetura completa de agente com 5 camadas
- [[prompt-engineering]] — Skills como contexto modular ativado por descrição
