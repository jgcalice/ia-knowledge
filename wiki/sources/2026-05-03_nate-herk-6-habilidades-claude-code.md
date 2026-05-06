---
title: "Seis Habilidades Fundamentais em Claude Code para Automação de IA"
type: source
source_file: "2026-05-03_nate_herk_ai_automation_eRS3CmvrOvA.md"
author: "@Nate Herk | AI Automation"
date: 2026-05-03
format: video
tags: [claude-code, automação, ferramentas-ia, skills, tokens, negócios, context-mode, claude-mem, superpowers, gsd]
source_url: "https://youtu.be/eRS3CmvrOvA"
source_count: 1
---

# Seis Habilidades Fundamentais em Claude Code para Automação de IA

> **Fonte:** [[2026-05-03_nate_herk_ai_automation_eRS3CmvrOvA]] | **Autor:** @Nate Herk | AI Automation | **Data:** 2026-05-03 | **Formato:** Vídeo YouTube (819s) | **[↗ Ver vídeo](https://youtu.be/eRS3CmvrOvA)**

## TL;DR

Após 400 horas no Claude Code, Nate Herk identifica as 6 habilidades que empresas reais pagam — simples, "chatas", mas altamente eficazes em economizar tempo, cortar custo e eliminar erros.

## Contexto

[[nate-herk]] tem trabalhado com agências de real estate, empresas de HVAC, coaches e agências de marketing. Percebeu os mesmos padrões se repetindo: clientes de indústrias diferentes enfrentam os mesmos problemas, e as mesmas seis habilidades aparecem repetidamente. O conteúdo é voltado para quem quer **monetizar automações com IA** em 2026.

## O que foi ensinado

### Habilidade 1 — Skill Creator
- Skill oficial da Anthropic: você descreve o que quer em linguagem natural, o Claude rascunha, testa, itera e empacota a skill
- Resolve o problema de quem tenta escrever `skill.md` manualmente e trava no formato e na estrutura
- **Não é a habilidade que o cliente paga** — é a "fábrica" que produz todas as outras
- Instalação: `/plugin install skill-creator@claude-plugins-official` (com escopo global recomendado)

### Habilidade 2 — Superpowers
- Força o Claude a trabalhar como um desenvolvedor sênior: planeja antes de codar, trabalha em ambiente isolado, escreve testes antes do código, brainstorma e revisa em dois estágios (spec vs. qualidade)
- Resolve o principal modo de falha do Claude Code: código apressado que parece OK na superfície mas quebra quando o cliente usa
- Resultado: subir de 60% para 80% de acerto na primeira passagem → menos ciclos de debugging → menor custo de tokens
- Mais de 150.000 stars no GitHub
- Instalação: `/plugin install superpowers@claude-plugins-official`

### Habilidade 3 — GSD (Get Shit Done)
- Endereça o *environment* em que o Claude escreve, não o processo — complementa o Superpowers
- Resolve o **context rot**: ao redor de 50% da janela de contexto, o código piora, o Claude esquece requisitos, pula etapas e corta atalhos
- Mecanismo: spawna sub-agentes frescos para cada tarefa, cada um com janela de contexto limpa
- Inclui quality gates automáticos: *Scope protection* (detecta quando o planejador dropa um requisito silenciosamente) e *Security enforcement*
- Tem modo autônomo: entrega uma spec e o agente planeja, executa, commita e avança sem babysitting
- **Não é um plugin de economia de tokens** — os sub-agentes custam tokens, mas economizam as horas de retrabalho por esquecimento
- Instalação: `npx get-shit-done-cc --claude --global`; comando `/gsd-help` para ver opções

### Habilidade 4 — /review e /ultra review
- `/review`: auditoria estruturada do código escrito — bugs, edge cases, problemas de design; roda localmente, rápido, custo apenas de tokens normais
- `/ultra review` (lançado com Opus 4.7): sobe o branch para um sandbox na nuvem, spawna uma frota de agentes revisores em paralelo (lógica, segurança, performance, edge cases); um bug só entra na lista se for reproduzido e verificado independentemente — sem falsos positivos ou nitpicks de estilo
- Fluxo recomendado: planejar com Superpowers → executar com contexto limpo via GSD → antes de qualquer merge importante, rodar /ultra review
- Requisitos: Claude Code 2.1.86+; login com conta Claude (não funciona só com API key)
- Custo: 3 runs grátis em planos Pro/Max; depois $5–$20 por run conforme tamanho; tempo de 10–20 min (roda em background)
- Não precisa instalar — já vem embutido na versão 2.1.86+

### Habilidade 5 — Context Mode
- Problema: cada tool call despeja dados brutos no contexto — snapshot do Playwright (56 KB), 20 issues do GitHub (59 KB); em 30 min de trabalho, 40% da janela é lixo
- Solução dupla: (1) roteia chamadas por sandbox — só o fragmento relevante volta ao contexto; (2) rastreia cada evento da sessão (edições, tarefas, decisões, erros) em banco SQLite local
- Benchmarks publicados pelo projeto: 56 KB → 299 bytes; 46 KB → 155 bytes; 315 KB totais → 5 KB por sessão completa
- Ao compactar, o Context Mode injeta um snapshot da sessão de volta — o modelo retoma exatamente onde parou
- Sessões de 30 min passam a durar 3 horas
- Instalação: dois comandos — `/plugin marketplace add mksglu/context-mode` e `/plugin install context-mode@context-mode` — depois reiniciar o Claude Code

### Habilidade 6 — Claude Mem
- Problema: Claude Code começa cada sessão do zero; você re-explica o projeto pela quinta vez no mês — ~10 min e milhares de tokens por sessão
- Distingue-se do `CLAUDE.md` e arquivos de memória manuais: esses funcionam, mas precisam de manutenção manual e se tornam desatualizados
- Claude Mem hookaça no ciclo de vida da sessão: captura automaticamente edições de arquivos, decisões, bug fixes, comandos → comprime em resumos semânticos → armazena em SQLite local com busca vetorial
- Auto-gera arquivos `CLAUDE.md` por pasta e os atualiza enquanto você codifica — documentação que se escreve sozinha
- Recuperação em 3 camadas: índice compacto → timeline das observações relevantes → detalhes completos do handoff necessário
- 10x economia de tokens na recuperação vs. dump total no início da sessão (dado do repo)
- Web viewer local: você vê o que Claude "lembra" do seu projeto
- Instalação: `/plugin marketplace add thedotmack/claude-mem` + `/plugin install claude-mem` (NÃO rodar `npm install` — os hooks não registram)

### Bônus — Frontend Design
- Skill oficial da Anthropic para design de UI
- Torna outputs de design menos "com cara de IA"
- Instalação global recomendada: `/plugin install frontend-design@claude-plugins-official`
- Nativo no produto Claude Design (Anthropic Labs) — mas ao trazer o projeto de volta para o Claude Code, é necessária a skill

### Como vender essas habilidades
- **Erro comum**: tentar vender o workflow
- **Certo**: vender o **outcome** — "10 horas economizadas por semana", "erros humanos cortados", "mais leads mais rápido"
- O cliente não se importa com quantas linhas de código foram escritas — quer que o sistema funcione quando o negócio depende dele
- Para iniciantes: escolher **uma** skill, aprender, construir 2–3 workflows e mostrar um demo

## Insights para o wiki

- **Distinção técnica documentada pela primeira vez**: **skills** (um arquivo `.md`) vs **plugins** (pacote maior com múltiplas skills + hooks + MCPs); na prática do vídeo o termo é intercambiável mas a distinção é operacional
- **GSD como arquitetura de context engineering**: o conceito de "sub-agentes frescos para cada tarefa" é apresentado não como economia de tokens mas como *garantia de qualidade* — os tokens são um custo aceito para eliminar o retrabalho por context rot
- **Ultra review** é o primeiro produto de revisão multi-agente verificado descrito em detalhe no wiki (reprodução independente antes de reportar)
- **Claude Mem** é a primeira solução de memória cross-session totalmente automatizada documentada — diferente de [[graphify]] (grafo de workspace) e dos arquivos `CLAUDE.md` manuais

## Entidades relacionadas

- [[nate-herk]] — autor, 400h de experiência prática, padrões extraídos de clientes reais
- [[claude-code]] — ambiente em que todas as habilidades operam
- [[claude-skills]] — ecossistema de skills e plugins mencionados

## Conceitos relacionados

- [[otimização-de-tokens]] — Context Mode (Técnica #17) e Claude Mem são soluções de nível infraestrutura para context rot
- [[agentes-ia]] — GSD usa sub-agentes frescos como estratégia de context engineering
- [[estratégia-de-negócios-com-ia]] — framework "vender outcomes, não workflows"
