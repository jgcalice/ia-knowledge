---
title: "LinkedIn"
type: entity
category: platform
tags: [linkedin, carreira, recrutamento, perfil, otimização]
source_count: 5
last_updated: 2026-04-24
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

## Fontes

- [[2026-04-11_transformacao-linkedin-ia]]
- [[2026-04-16_sanskaar-singh-linkedin-prompts]]
- [[2026-04-07_career-ops-busca-emprego-ia]] — LinkedIn como canal de vagas integrado ao sistema Career Ops
- [[2026-04-15_leads-qualificados-claudecode]] — LinkedIn como dado de enriquecimento de lead (perfil do prospect)
- [[2026-04-22_arshman-khalid-automacao-busca-emprego]] — LinkedIn Jobs scraped via Apify Actor para alimentar pipeline de candidatura automatizada
