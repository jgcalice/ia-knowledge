---
title: "LinkedIn"
type: entity
category: platform
tags: [linkedin, carreira, recrutamento, perfil, otimização, ats, currículo]
source_count: 8
last_updated: 2026-06-20
---

# LinkedIn

> **Categoria:** Plataforma de carreira e networking profissional | **Aparece em:** 4 fontes

## Papel no wiki

LinkedIn aparece como alvo de otimização com IA. Dois criadores documentaram sistemas completos de reescrita de perfil com Claude, cada um com ângulo diferente.

## Abordagem 1: "cole o perfil do LinkedIn" (Bruno Souza)

Exportar os dados do LinkedIn e colá-los diretamente no prompt. O LLM analisa e reescreve seções específicas com constraints de caracteres.

### Seções otimizáveis com IA (per [[2026-04-11_transformacao-linkedin-ia]])

1. Headline (até 120 caracteres)
2. About / Sobre (até 2000 caracteres)
3. Mensagens de referência (cold outreach)
4. Skills e Keywords (otimizado para SEO de recrutadores)
5. Seção de experiência (formato: Fiz X, usando Y, resultou em Z)

## Abordagem 2: "perspectiva do recrutador primeiro" (Sanskaar Singh)

Diagnóstico antes de qualquer reescrita: pedir ao Claude para simular o julgamento de um recrutador senior. Sequência:

1. **First Impression Test** — Claude como recrutador avalia o perfil honestamente
2. **Headline Rewrite** — 5 versões em espectro de ousadia (conservador → bold)
3. **About Section** — gancho + o que faz + quem ajuda + resultados + CTA
4. **Keywords & Search** — comparar JDs com o perfil para identificar lacunas de SEO
5. **Experience Polish** — ação + resultado mensurável; Claude faz perguntas para ajudar a encontrar métricas

→ [[2026-04-16_sanskaar-singh-linkedin-prompts]] | [[sanskaar-singh]]

## Abordagem 3: "pipeline completo de reconstrução de candidatura" (Your AI Compass)

4 prompts sequenciais usando ROLEs de recrutadores de elite:

1. **6-Second Resume Rewriter** — ROLE: senior Google recruiter; fórmula XYZ, métricas obrigatórias, 1 página
2. **ATS Optimization** — ROLE: especialista em Workday/Greenhouse/Lever; integração de keywords sem soar artificial
3. **McKinsey Achievement Quantifier** — ROLE implícito McKinsey; fórmula "Conseguiu X → Resultado Y → Por fazer Z"
4. **High-Conversion Cover Letter** — ROLE: recruitment director at Robert Half; 250–300 palavras, demonstração de pesquisa, fit cultural

→ [[2026-04-28_your-ai-compass-perfil-profissional]] | [[your-ai-compass]]

## Abordagem 4: "cold outreach direto para o hiring manager" (Hollyfield lA)

Além do perfil otimizado, o LinkedIn é canal de abordagem direta. Mensagem estruturada com 3 elementos:
1. Início específico sobre a empresa (não genérico)
2. Conexão de valor pessoal
3. Pedido de baixa fricção

Limite: <75 palavras. Destinatário: responsável pela contratação, não o RH.

→ [[2026-06-15_hollyfield-la-7-prompts-emprego]] | [[hollyfield-la]]

## Abordagem 5: "scraping de vagas via modo agente do ChatGPT" (Rafa Grandi)

ChatGPT em modo agente navega no LinkedIn (e no Lensa) para encontrar vagas dos últimos 7 dias compatíveis com os cargos mapeados no Prompt 1, gerando planilha com link, pontuação de compatibilidade e versão de currículo personalizada por vaga. Após a planilha, o agente se candidata nas 500 vagas de maior compatibilidade de forma autônoma.

**Distinção das abordagens anteriores:**
- vs. [[arshman-khalid]]: também faz scraping do LinkedIn, mas usa Apify Actor + Career Ops (plugin Claude); esta abordagem usa diretamente o modo agente do ChatGPT, sem tools externas
- vs. [[hollyfield-la]]: cold outreach manual de <75 palavras; esta abordagem é totalmente automática (agente aplica sem o usuário interagir)

→ [[2026-06-18_rafa-grandi-candidaturas-emprego-ia]] | [[rafa-grandi]]

## Fontes

- [[2026-04-11_transformacao-linkedin-ia]]
- [[2026-04-16_sanskaar-singh-linkedin-prompts]]
- [[2026-04-07_career-ops-busca-emprego-ia]] — LinkedIn como canal de vagas integrado ao sistema Career Ops
- [[2026-04-15_leads-qualificados-claudecode]] — LinkedIn como dado de enriquecimento de lead (perfil do prospect)
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]] — LinkedIn Jobs scraped via Apify Actor para alimentar pipeline de candidatura automatizada
- [[2026-04-28_your-ai-compass-perfil-profissional]] — 4 prompts com ROLEs de recrutadores de elite para reconstrução completa de candidatura
- [[2026-06-15_hollyfield-la-7-prompts-emprego]] — cold outreach <75 palavras para hiring manager + otimização de perfil para 3 audiências simultâneas
- [[2026-06-18_rafa-grandi-candidaturas-emprego-ia]] — scraping de vagas via modo agente do ChatGPT + auto-candidatura em 500 vagas com currículo personalizado por JD
