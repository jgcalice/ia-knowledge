---
title: "10 Repos GitHub que Parecem Ilegais de Usar"
type: source
source_file: "2026-05-21_harish_bhatt_DYmxVBNkjLg.md"
author: "@Harish bhatt (@codingknowledge)"
date: 2026-05-21
format: carousel
tags: [open-source, github, ferramentas-ia, automação, ollama, whisper, n8n, custo-zero]
source_url: "https://www.instagram.com/p/DYmxVBNkjLg/?img_index=10"
source_count: 1
---

# 10 Repos GitHub que Parecem Ilegais de Usar

> **Fonte:** [[2026-05-21_harish_bhatt_DYmxVBNkjLg]] | **Autor:** @Harish bhatt (@codingknowledge) | **Data:** 2026-05-21 | **Formato:** carousel (10/11 slides) | **[↗ Ver post](https://www.instagram.com/p/DYmxVBNkjLg/?img_index=10)**

## TL;DR

9 repositórios GitHub open-source que eliminam custos recorrentes com serviços SaaS populares — de vídeo e IA até design e automação — enquanto oferecem funcionalidades equivalentes ou superiores.

## Contexto

[[harish-bhatt]] (@codingknowledge) publica sua segunda coleção de repos GitHub no mesmo período. O ângulo editorial é distinto da [primeira fonte](2026-05-16_harish-bhatt-repos-renda-passiva): enquanto o post de 16/05 propõe "fork → white-label → tornar-se o provedor de SaaS", este propõe **"pare de pagar o SaaS proprietário, use o equivalente gratuito"**. O framing de "parecem ilegais de usar" alude à desproporcionalidade entre o custo zero e o valor entregue — a afirmação é que esses repos estão "destruindo $50 bilhões em receita corporativa".

## O que foi ensinado

| # | Repo | Substitui | Custo evitado | Equivalente gratuito |
|---|------|-----------|---------------|---------------------|
| 1 | **yt-dlp** | YouTube Premium | $14/mês | Download de vídeo de qualquer plataforma (YouTube, TikTok, Instagram, X) via linha de comando |
| 2 | **[[ollama]]** | OpenAI API | ~$500/mês (devs) | Modelos GPT-4 class rodando offline, sem custo de API |
| 3 | **Foooocus** | Midjourney | $30/mês | Geração de imagens com qualidade Midjourney no próprio GPU, ilimitada |
| 4 | **[[whisper]]** | Otter.ai | $20/mês | Transcrição de áudio em 99 idiomas — modelo da OpenAI, open-source |
| 5 | **Plausible Analytics** | Google Analytics 360 | $150K/ano (enterprise) | Analytics privacidade-first, GDPR/CCPA/PECR, script leve, UE |
| 6 | **AppFlowy** | Notion | $20/usuário/mês | Workspace AI self-hosted com usuários ilimitados e privacidade de dados |
| 7 | **Penpot** | Figma | $45/editor/mês | Design e prototipagem open-source, self-hosted, licença aberta |
| 8 | **[[n8n]]** | Zapier Pro | $600/mês | Automações ilimitadas com 400+ integrações e IA nativa |
| 9 | **Cal.com** | Calendly Teams | $16/usuário/mês | Agendamento open-source; Cal.diy = fork 100% MIT sem código Enterprise |

**Ponto central do [[ollama]]**: desenvolvedores que usam a OpenAI API gastam ~$500/mês; o Ollama roda os mesmos modelos offline por $0. "Start building with open models" — o benefício é financeiro, de privacidade (dados nunca saem da máquina) e de latência.

**Ponto central do [[whisper]]**: modelo de reconhecimento de fala da OpenAI treinado em 680K horas de dados multitarefa — transcrição em inglês, tradução de fala de qualquer idioma para inglês, transcrição multilíngue e identificação de idioma. O Otter.ai cobra $20/mês pelo que o Whisper entrega gratuitamente com a mesma tecnologia subjacente.

**[[n8n]] como ponto de convergência**: segunda aparição desta ferramenta no wiki. Aqui o custo evitado é o Zapier Pro ($600/mês) para o usuário-operador — ângulo de economia pessoal e indie, distinto do modelo de agência de automação documentado no post anterior de [[harish-bhatt]].

## Insights para o wiki

- **5ª perspectiva sobre repos open-source**: este post complementa os quatro anteriores com enquadramento centrado no **custo pessoal e de desenvolvedor** — não em operação de canais ([[paras-madan]]), não em B2B enterprise ([[bestapps-ai]]), não em $10K/mês ([[growai]]), não em white-label SaaS ([[2026-05-16_harish-bhatt-repos-renda-passiva]]). O beneficiário direto é o desenvolvedor ou usuário indie que elimina assinaturas.
- **Ollama como entrada do tema "IA local" no wiki**: primeira documentação de execução de modelos LLM **offline** — custo zero de API, privacidade por design, sem dependência de conectividade. Relevante para qualquer arquétipo de negócio do wiki que hoje incorre em custo de OpenAI API.
- **Whisper fecha o ciclo de ferramentas de transcrição**: o wiki documenta pipelines onde transcrição seria valiosa (análise de chamadas de vendas em [[jordan-lee]], sessões longas em [[nate-herk]]); Whisper é a alternativa gratuita ao Otter.ai/Rev para integrar transcrição local sem custo por minuto.
- **Sobreposição com post anterior confirma robustez dos repos**: Cal.com, Plausible, AppFlowy e [[n8n]] aparecem em ambos os posts de [[harish-bhatt]]. O mesmo autor, dois frameworks distintos (tornar-se o provedor vs. usar gratuitamente), mesmos repos — valida a versatilidade desses projetos como fundação para múltiplos modelos de uso.

## Entidades relacionadas

- [[harish-bhatt]] — segunda contribuição; ângulo editorial complementar ao post de 2026-05-16
- [[ollama]] — plataforma de LLM local; nova entidade no wiki
- [[whisper]] — modelo de transcrição open-source da OpenAI; nova entidade no wiki
- [[n8n]] — automação de workflows; segunda aparição (ângulo custo pessoal vs. modelo de agência)
- [[bestapps-ai]] — ângulo anterior de substituição de softwares B2B caros
- [[paras-madan]] — ângulo anterior de operação de canais com repos

## Conceitos relacionados

- [[estratégia-de-negócios-com-ia]] — 5ª perspectiva sobre repos open-source: custo zero pessoal/dev como valor primário
- [[agentes-ia]] — Ollama como alternativa de custo zero para construir pipelines de agentes locais
