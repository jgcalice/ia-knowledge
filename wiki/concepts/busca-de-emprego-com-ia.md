---
title: "Busca de Emprego com IA"
type: concept
tags: [carreira, busca-de-emprego, automação, ats, currículo, claude-code, apify, linkedin, negociação, cover-letter, quantificação, entrevista, star-method]
source_count: 7
last_updated: 2026-05-30
---

# Busca de Emprego com IA

> **Fontes:** 2 | **Domínio:** Automação de carreira / Job search pipeline

## Definição

Uso de LLMs e automação para transformar a busca de emprego de processo manual e baseado em esforço para pipeline estruturado baseado em dados e fit real.

## O que foi documentado

### Career Ops — Sistema completo de job search
Projeto open-source (MIT) construído com Claude Code por desenvolvedor individual:

**Pipeline do sistema:**
```
Escanear páginas de carreira de empresas
    ↓
Avaliar vagas em 10 dimensões de fit
    ↓
Filtrar vagas com match real (não aplicar em massa)
    ↓
Reescrever currículo otimizado para ATS por vaga
    ↓
Preparar conteúdo de entrevista
    ↓
Dashboard de rastreamento de candidaturas
```

**Resultado documentado:** 700+ vagas avaliadas → oferta de emprego real.

## Por que ATS importa

ATS (Applicant Tracking System) é o software que empresas usam para filtrar currículos antes de um humano ver. Currículo genérico é reprovado pelo ATS antes de chegar ao recrutador. Otimização por vaga específica aumenta drasticamente a taxa de passagem.

## Integração com LinkedIn

A busca de emprego com IA complementa a otimização de LinkedIn:
1. **LinkedIn otimizado** ([[2026-04-11_transformacao-linkedin-ia]]) → te acha por busca de recrutadores
2. **Career Ops** → você acha as vagas certas e aplica com currículo customizado

## CareerOps como plugin Claude (Arshman Khalid)

Segunda documentação do Career Ops — desta vez como **plugin instalável via zip** no Claude, integrado ao **Apify LinkedIn Jobs Scraper**. Pipeline expandido em relação à versão anterior:

```
Scraping de vagas LinkedIn (via Apify)
    ↓
Scoring A-F contra experiência do candidato
    ↓
Currículo ATS + carta de apresentação para vagas A-tier
    ↓
Identificação de gaps de skills + como corrigir
    ↓
Histórias STAR mapeadas para a vaga
    ↓
Outreach para o hiring manager
    ↓
Scripts de negociação salarial (após oferta)
```

**Nova dimensão documentada:** o pipeline vai além da candidatura — acompanha até a negociação salarial, o que não estava documentado na fonte anterior.

**Argumento central do autor:** "Empresas usam IA para rejeitar seu currículo em 6 segundos. Use IA para rejeitar a vaga delas em 3 segundos."

→ [[2026-04-22_arshman-khalid-automacao-busca-emprego]] | Autor: [[arshman-khalid]]

## Candidaturas personalizadas sem automação (Coding AI FullStack 300K)

Nível de entrada documentado — uso direto do Claude.ai, sem CLI, sem plugins:

**Fluxo documentado:**
```
Colar job description no Claude
    ↓
Claude extrai skills e palavras-chave prioritárias do anúncio
    ↓
Claude reescreve o currículo com foco naquelas skills
    ↓
Claude gera carta de apresentação alinhada à vaga
```

**Resultado do caso**: 6 entrevistas em 7 dias (anedota narrativa, não verificável).

**Diferença chave em relação ao Career Ops**: não há automação ou scraping — o fluxo é manual por vaga, mas muito mais rápido que reescrita sem IA. Acessível para qualquer pessoa sem conhecimento técnico.

→ [[2026-04-26_coding-ai-fullstack-entrevistas-claude]] | Autor: [[coding-ai-fullstack]]

## Toolkit de reconstrução de candidatura (Your AI Compass)

4 prompts sequenciais com personas de recrutadores de elite — pipline de reconstrução completa do perfil:

| # | Prompt | ROLE | Foco |
|---|--------|------|------|
| 1 | 6-Second Resume Rewriter | Senior Google recruiter | Fórmula XYZ + métricas + 1 página |
| 2 | ATS Optimization | Especialista Workday/Greenhouse/Lever | Keywords integradas + estrutura limpa |
| 3 | McKinsey Achievement Quantifier | McKinsey (implícito) | "Conseguiu X → Resultado Y → Por fazer Z" |
| 4 | High-Conversion Cover Letter | Recruitment director Robert Half | 250–300 palavras, fit cultural, próximo passo |

**Nível de acesso:** Claude.ai direto, sem CLI. Pipeline executável por qualquer candidato.

**Diferencial vs. abordagens anteriores:** enquanto [[coding-ai-fullstack]] usa Claude como revisor genérico e [[career-ops]] automatiza o scraping, este toolkit foca na *qualidade da candidatura em si* — especialmente a otimização ATS (Prompt 2) e a quantificação de conquistas (Prompt 3), que as outras abordagens documentam superficialmente.

→ [[2026-04-28_your-ai-compass-perfil-profissional]] | [[your-ai-compass]]

## Preparação para entrevistas de emprego (Roshan Krishna)

Enquanto as abordagens anteriores cobrem **antes** da entrevista (perfil, currículo, candidaturas), este pipeline cobre o **desempenho durante a entrevista** — uma fase até então não documentada no wiki.

5 prompts encadeados, cada um usando o output do anterior como input:

| # | Prompt | Output |
|---|--------|--------|
| 1 | Prever as perguntas exatas (colar JD) | 15 perguntas em 3 categorias (Técnicas, Comportamentais STAR, Curva) + nota do que cada uma testa |
| 2 | Construir respostas impactantes | Resposta forte por pergunta via STAR; <90s oral; `[INSERT YOUR STORY]` como placeholder |
| 3 | Encontrar pontos fracos | 3 respostas mais fracas + gaps + follow-ups difíceis + como tratar cada um |
| 4 | Mock Interview Brutal Mode | Entrevista ao vivo pergunta a pergunta: score 0-10 + feedback + versão reescrita que pontuaria 9+ |
| 5 | Cheatsheet de 60 segundos | 3 pontos fortes, 2 histórias essenciais, 1 pergunta-fumble + como salvar, abertura confiante para "Tell me about yourself" |

**Instrução editorial do Prompt 4**: "Don't go easy on me" — combate explicitamente o viés de complacência do modelo.

**Resultado documentado**: o irmão do autor recebeu oferta de emprego; prompts "previram quase todas as perguntas da entrevista".

→ [[2026-05-18_roshan-krishna-5-prompts-entrevista]] | Autor: [[roshan-krishna]]

## Perguntas estratégicas para o final da entrevista (@Mike)

Enquanto [[roshan-krishna]] prepara o candidato para *responder* as perguntas do entrevistador, @Mike documenta as perguntas que o *candidato* deve fazer ao entrevistador no final.

**Premissa**: "No questions" sinaliza desinteresse ou passividade — revela o candidato antes que qualquer pergunta seja feita.

10 das 11 perguntas capturadas:

| # | Pergunta | Sinal que envia |
|---|----------|----------------|
| 1 | "How will you know after 3 months that I'm doing well?" | Foco em resultados |
| 2 | "What usually breaks new people here?" | Pronto para a realidade |
| 3 | "Who would I work with most often?" | Consciência do ambiente humano |
| 4 | "How do you give feedback here?" | Revela cultura real |
| 5 | "Who grows fastest in this company?" | Expõe valores reais |
| 6 | "What mistakes are serious here?" | Maturidade |
| 7 | "What matters most here: speed, quality, or independence?" | Prioridade real |
| 8 | "Is there room to grow for people who deliver results?" | Esforço tem retorno? |
| 9 | "What do you personally like about working here?" | Reação do entrevistador conta quase tudo |
| 10 | "Do you have any doubts about me that I can clear up right now?" | Move final poderoso — quase ninguém usa |

> ⚠️ **Nota**: conteúdo não usa IA diretamente. Pode ser usado com Claude para gerar variações das perguntas adaptadas à JD e ao setor.

→ [[2026-05-17_mike-perguntas-entrevista]] | Autor: [[mike]]

## A Regra dos 75% e Claude como Scoring Engine (@thinkentrepreneurs)

Ângulo distinto de todas as abordagens anteriores: Claude não é usado para *preparar* a candidatura, mas para *decidir se vale a pena aplicar*.

**Premissa**: a maioria dos candidatos aplica sem filtro — 27 candidaturas para 1 entrevista, na média. O problema não é o mercado, é o targeting.

**Fluxo documentado:**
```
Ativar "Web search" no Claude.ai
    ↓
Carregar currículo em PDF
    ↓
Usar prompt de recrutador de IA (busca vagas reais + scores cada uma)
    ↓
Score ≥ 75 → aplicar
Score < 75 → pular (ATS vai eliminar antes de humano ver)
```

**Prompt template:**
```
Act as an AI recruiter. Analyse my resume. Find real companies currently hiring 
for senior roles in [your field] in [your country]. Categorise by high, medium, 
and stretch probability. Score each role out of 100 based on my resume match. 
Include verified application links posted within the last 30 days.
```

**Por que 75% é o threshold:**
ATS (Workday, Greenhouse, Lever) escaneia currículos em busca de keywords da JD antes de qualquer humano ver. Score baixo = keywords não alinhadas = eliminação automática. Claude identifica esse gap antecipadamente, antes de desperdiçar uma candidatura.

**Posição na cadeia de job search:**
- Este conteúdo cobre a **triagem de vagas** (fase 0) — anterior ao Career Ops e ao toolkit de [[your-ai-compass]], que cobrem a preparação da candidatura após a seleção

→ [[2026-05-29_claude-ia-busca-emprego-score]] | Autor: [[think-entrepreneurs]]

## Fontes

- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]]
- [[2026-04-26_coding-ai-fullstack-entrevistas-claude]]
- [[2026-04-28_your-ai-compass-perfil-profissional]]
- [[2026-05-18_roshan-krishna-5-prompts-entrevista]]
- [[2026-05-17_mike-perguntas-entrevista]]
- [[2026-05-29_claude-ia-busca-emprego-score]]
