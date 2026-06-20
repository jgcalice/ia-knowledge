---
title: "Automatizando Candidaturas de Emprego com IA"
type: source
source_file: "2026-06-18_rafa_grandi_DZvmQsnTu3I.md"
author: "@Rafa Grandi"
date: 2026-06-18
format: reel
tags: [chatgpt, busca-de-emprego, candidaturas, ats, carreira, automação, linkedin, currículo, agente-ia]
source_url: "https://www.instagram.com/reel/DZvmQsnTu3I/"
source_count: 1
---

# Automatizando Candidaturas de Emprego com IA

> **Fonte:** [[2026-06-18_rafa_grandi_DZvmQsnTu3I]] | **Autor:** @Rafa Grandi | **Data:** 2026-06-18 | **Formato:** Reel (63s) | **[↗ Ver post](https://www.instagram.com/reel/DZvmQsnTu3I/)**

## TL;DR

Usar o modo agente do ChatGPT para se candidatar automaticamente a 500 vagas de emprego em 24 horas, com currículo personalizado por vaga e pontuação de compatibilidade automática.

## Contexto

Criador BR mostra experimento de "candidatura em massa com IA" — o oposto do processo tradicional (uma candidatura de cada vez). A proposta central: delegar toda a fase de triagem de vagas e submissão de candidaturas ao ChatGPT em modo agente, liberando o candidato para focar em relacionamentos.

## O que foi ensinado

O processo acontece em 4 prompts sequenciais:

**Prompt 1 — Mapeamento de vagas-alvo com palavras-chave ATS**
```
Atue como recrutador sênior, com base no meu currículo, liste os 20 cargos 
para os quais eu mais me qualifico com as palavras-chave exatas que o sistema 
ATS procura.
```
*Input necessário:* PDF do currículo carregado no chat.

**Prompt 2 — Reescrita do currículo em modelo-mestre**
```
Reescreve meu currículo em um modelo mestre que eu possa adaptar 
instantaneamente. Use a fórmula X, Y, Z do Google e remova todos os sinais 
de alerta que um gerente de contratação detectaria em menos de 10 segundos.
```
*Nota:* A **fórmula X, Y, Z do Google** é: "Você alcançou [X] medido por [Y] fazendo [Z]" — estrutura de bullets orientada a resultados quantificados.

**Prompt 3 — Scraping de vagas com planilha de pontuação** *(com modo agente ativado)*
```
Vai no LinkedIn e no [Lensa] e encontre todos os empregos correspondentes 
a esses cargos postados nos últimos sete dias. Crie uma planilha com link, 
pontuação de compatibilidade e versão de currículo personalizada pra cada 
um deles.
```
*Ação necessária:* clicar no botão "+" e ativar o **modo agente** antes deste prompt.

**Prompt 4 — Auto-candidatura nas 500 vagas de maior compatibilidade**
```
Se candidate nas 500 vagas com maior compatibilidade, personalize cada 
candidatura com base na descrição de cada uma das vagas.
```

**Resultado reportado:** ChatGPT se candidata de forma autônoma enquanto o usuário dorme.

## Insights para o wiki

- **Primeiro caso documentado de auto-candidatura em massa via agente de IA** — 500 candidaturas automatizadas com personalização por JD. Abordagem oposta ao "só aplicar se score ≥ 75%" de [[think-entrepreneurs]]; aqui o critério é "top 500" e a personalização é delegada ao agente.
- **ChatGPT (não Claude) como executor principal** — este é um dos raros casos no wiki onde a ferramenta central é o ChatGPT, em especial o **modo agente** que permite navegar em sites e executar ações. Contrasta com a maioria das fontes que usam Claude/Claude Code.
- **Planilha de pontuação de compatibilidade como pré-filtro** — análogo à Regra dos 75% de [[think-entrepreneurs]], mas aqui a pontuação é gerada para todas as vagas e usada para rankear (não filtrar).
- **Fórmula XYZ do Google** — estrutura de bullet de currículo ("você alcançou [X] medido por [Y] fazendo [Z]") é mencionada por nome. Complementa a "fórmula de conquistas McKinsey" já documentada em [[your-ai-compass]].
- **"Sinais de alerta em 10 segundos"** — instrução que força o modelo a simular o julgamento rápido do hiring manager, análogo ao "6-Second Resume Rewriter" de [[your-ai-compass]].

## Entidades relacionadas

- [[rafa-grandi]] — criador do conteúdo; criador BR
- [[linkedin]] — plataforma de vagas scrapeada pelo agente no Prompt 3

## Conceitos relacionados

- [[busca-de-emprego-com-ia]] — abordagem de auto-candidatura em massa (novo ângulo)
- [[carreira-com-ia]] — extensão do pipeline de candidatura
- [[prompt-engineering]] — fórmula XYZ, modo agente, persona de recrutador sênior
- [[agentes-ia]] — modo agente do ChatGPT executando ações autônomas (navegar, candidatar)
