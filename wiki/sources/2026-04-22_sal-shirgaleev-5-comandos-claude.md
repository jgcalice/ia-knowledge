---
title: "5 Comandos do Claude Code Pouco Utilizados"
type: source
source_file: "2026-04-22_sal_shirgaleev_DXa1Hf7ldZZ.md"
author: "@Sal Shirgaleev"
date: 2026-04-22
format: carousel
tags: [claude-code, prompt-engineering, comandos, otimização, contexto]
source_url: "https://www.instagram.com/p/DXa1Hf7ldZZ/?igsh=MWJuYjV6OHZoMGI0cg=="
source_count: 1
---

# 5 Comandos do Claude Code Pouco Utilizados

> **Fonte:** [[2026-04-22_sal_shirgaleev_DXa1Hf7ldZZ]] | **Autor:** @Sal Shirgaleev (@sshirg) | **Data:** 2026-04-22 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXa1Hf7ldZZ/?igsh=MWJuYjV6OHZoMGI0cg==)**

## TL;DR

Cinco comandos nativos do Claude Code que a maioria ignora: `/init`, `#`, `/review`, `/plan` e `/compact` — cada um endereça um ponto de atrito recorrente no uso diário.

## Contexto

@Sal Shirgaleev (handle @sshirg) publica dicas práticas de produtividade com IA. Neste carousel de 7 slides, ele apresenta comandos built-in do Claude Code que existem há algum tempo mas são pouco conhecidos entre usuários intermediários.

## O que foi ensinado

- **`/init`** — Escaneia o codebase inteiro e gera automaticamente um `CLAUDE.md` com contexto, convenções e estrutura do projeto. O arquivo é carregado em toda sessão: Claude sempre parte com consciência total do projeto, sem precisar de README colado no prompt.

- **`#` (hashtag inline)** — Adiciona uma regra permanente em 3 segundos. Exemplo: `Always use TypeScript. # Never use var.` A regra é salva no "rulebook" pessoal do Claude e persiste entre sessões. Constrói preferências incrementalmente sem editar CLAUDE.md manualmente.

- **`/review`** — Revisão de código como "engenheiro sênior gratuito": audita o codebase inteiro (não só o arquivo aberto), detecta edge cases, race conditions, falhas silenciosas, code smell, chaves expostas e padrões ruins — com explicação, não só flag.

- **`/plan`** — Força um mapa de execução antes de qualquer linha de código: lista cada etapa, arquivo e decisão. Permite corrigir desalinhamento antes que Claude siga pelo caminho errado. O plano vira a especificação; aprovar e deixar executar.

- **`/compact`** — Quando a janela de contexto enche, comprime o histórico da sessão sem perder a intenção original. Evita que Claude "esqueça" o início do trabalho. Deve ser usado proativamente, não apenas quando o contexto estourar.

## Insights para o wiki

- Confirma e expande o uso do **Compact Skill** mencionado em [[2026-04-18_7-hacks-tokens-claude]] — aqui chamado de `/compact`, é um comando built-in, não uma skill externa.
- O comando `#` para regras permanentes é uma alternativa mais rápida a editar o CLAUDE.md manualmente (tema central de [[2026-04-22_sal_shirgaleev_DXa1Hf7ldZZ]]).
- O `/plan` mapeia bem ao conceito de arquitetura antes de codificação — reforça o padrão de [[agentes-ia]] onde delegação eficaz exige especificação prévia.
- O `/review` posiciona Claude como par de revisão de código (QA integrado), não só assistente de escrita.

## Entidades relacionadas

- [[claude-code]] — ferramenta central cujos comandos são ensinados
- [[sal-shirgaleev]] — autor do conteúdo

## Conceitos relacionados

- [[prompt-engineering]] — comandos como interface estruturada de instrução ao LLM
- [[otimização-de-tokens]] — `/compact` endereça diretamente o problema de contexto longo
