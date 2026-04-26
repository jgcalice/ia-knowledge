---
title: "Princípios Fundamentais do CLAUDE.md de Boris Cherny"
type: source
source_file: "2026-04-17_manthan_patel_lead_gen_man_DXPlgNwDZgz.md"
author: "@Manthan Patel | Lead Gen Man"
date: 2026-04-17
format: carousel
tags: [claude-code, prompt-engineering, agentes-ia, claude, workflow, plan-mode, subagentes]
source_url: "https://www.instagram.com/p/DXPlgNwDZgz/?img_index=2&igsh=MW81dWVxb2hjZ3VyMg=="
source_count: 1
---

# Princípios Fundamentais do CLAUDE.md de Boris Cherny

> **Fonte:** [[2026-04-17_manthan_patel_lead_gen_man_DXPlgNwDZgz]] | **Autor:** @Manthan Patel | Lead Gen Man | **Data:** 2026-04-17 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXPlgNwDZgz/?img_index=2&igsh=MW81dWVxb2hjZ3VyMg==)**

## TL;DR

O arquivo CLAUDE.md de [[boris-cherny]] codifica um sistema de orquestração de workflow para o Claude Code em três pilares: Workflow Orchestration, Task Management e Core Principles — fazendo o agente trabalhar de forma autônoma, estruturada e com impacto mínimo.

## Contexto

[[manthan-patel]] apresenta o CLAUDE.md de Boris Cherny (engenheiro da Anthropic) como "cheat code" para maximizar o desempenho do [[claude-code]]. O conteúdo é um carousel de 5 slides documentando as seções do arquivo e os princípios por trás de cada diretiva.

## O que foi ensinado

### Workflow Orchestration

- **Modo de Planejamento Padrão**: entrar em plan mode para tarefas não triviais; parar e replanejar se algo der errado
- **Estratégia de Sub-agentes**: usar sub-agentes para manter o contexto limpo e realizar análises em paralelo
- **Ciclo de Autoaperfeiçoamento**: atualizar lições conforme necessário e revisar frequentemente
- **Correção Autônoma de Bugs**: corrigir erros sem pedir ajuda e resolver testes com falhas de forma independente

### Task Management

1. **Planejar Primeiro** — antes de qualquer código ou ação
2. **Verificar o Plano** — checar o plano antes de executar
3. **Rastrear Progresso** — acompanhar o estado durante a execução
4. **Explicar Mudanças** — documentar o que foi alterado e por quê
5. **Documentar Resultados** — registrar o que foi entregue
6. **Capturar Lições** — armazenar aprendizados para reutilizar

### Core Principles

| Princípio | Descrição |
|-----------|-----------|
| **Simplicity First** | Manter mudanças simples; o menor change que funciona |
| **No Laziness** | Identificar causas raízes, não criar patches |
| **Minimal Impact** | Tocar apenas o que a tarefa exige — zero side effects |

## Insights para o wiki

- **CLAUDE.md como instrumento de orquestração**: Boris Cherny documenta que o CLAUDE.md não é só um arquivo de configuração — é um sistema completo de diretrizes de autonomia. Complementa e fundamenta as boas práticas documentadas em [[sal-shirgaleev]] e [[alex-finn]].
- **Plan Mode reforçado como padrão**: segunda fonte confirmando plan mode explícito para tarefas não triviais — a primeira foi [[2026-04-22_sal-shirgaleev-5-comandos-claude]] (comando `/plan`).
- **Sub-agentes como estratégia de contexto limpo**: a motivação explicitada aqui é diferente da de [[nate-herk]] (tokens) — aqui é qualidade de contexto e paralelismo. São complementares.
- **Minimal Impact como princípio de design**: primeiro registro explícito de um princípio de impacto mínimo no wiki — relevante para qualquer agente autônomo que modifica arquivos ou estados externos.

## Entidades relacionadas

- [[manthan-patel]] — autor do post
- [[boris-cherny]] — criador do CLAUDE.md referenciado
- [[claude-code]] — ferramenta central do conteúdo

## Conceitos relacionados

- [[prompt-engineering]] — CLAUDE.md como sistema de instruções permanentes; Plan Mode; princípios Core
- [[agentes-ia]] — sub-agentes para contexto limpo e paralelismo; ciclo de autoaperfeiçoamento
