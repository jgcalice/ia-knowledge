---
title: "Ative o Founder Thinking Mode no Claude"
type: source
source_file: "2026-05-29_prakash_kumar_DY7bJr5DJfR.md"
author: "@Prakash Kumar"
date: 2026-05-29
format: carousel
tags: [prompt-engineering, founders, claude, estratégia, negócios, modos-claude, custom-instructions]
source_url: "https://www.instagram.com/p/DY7bJr5DJfR/?img_index=7"
source_count: 1
---

# Ative o Founder Thinking Mode no Claude

> **Fonte:** [[2026-05-29_prakash_kumar_DY7bJr5DJfR]] | **Autor:** @Prakash Kumar | **Data:** 2026-05-29 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DY7bJr5DJfR/?img_index=7)**

## TL;DR
Um único prompt instalado nas Custom Instructions do Claude transforma todas as conversas de negócios em aconselhamento direto de operador experiente — sem evasões, sem frameworks genéricos, sem "depende".

## Contexto
@Prakash Kumar (canal @startup.snack) documenta o "Founder Thinking Mode" como um modo do Claude que a maioria dos fundadores desconhece. O conteúdo apresenta o prompt de ativação e 6 casos de uso práticos para os principais pontos de decisão de um early-stage founder.

## O que foi ensinado

### Prompt de ativação (Custom Instructions)
Colar antes de cada conversa de negócios **ou** salvar permanentemente nas Custom Instructions:

```
You are now in Founder Thinking Mode. Think like a first-principles operator 
who has built and exited companies. When I give you a problem — don't give 
generic advice. Give me the exact decision a seasoned founder would make. 
Include trade-offs, risks, and what most people miss. Start every response 
with: 'Here's what I'd actually do.'
```

**Dica de instalação**: Settings → Custom Instructions → "Every session starts sharp"

### 6 casos de uso documentados

| # | Caso | Prompt central |
|---|------|---------------|
| 1 | **Stress Test Your Business** | Descreva em 2 frases → stress test como Series A investor (500 pitches) → o que quebra primeiro, o que você não vê, o que o top 3% faz diferente. "Be blunt. Don't protect my feelings." |
| 2 | **Find The Gap They Can't Fill** | Nomeie o concorrente → 3 movimentos que o tornam irrelevante ao cliente-alvo em 12 meses, ranqueados por velocidade de execução |
| 3 | **Kill The Spiral In 10 Minutes** | Decisão paralisada → run-through: o que quebra se errar, o que você otimiza vs. deveria otimizar, o que um founder que já errou aqui diria |
| 4 | **Hidden Revenue** | Oferta atual → 3 ângulos de monetização não tentados, ranqueados por effort-to-return ratio, como testar cada um em 2 semanas sem reconstruir nada |
| 5 | **Hire Slow (30 min)** | Cargo da 1ª contratação → 5 perguntas que separam A-players de quem apenas sabe entrevistar + 1 red flag invisível no mês 3 detectável em 30 minutos |

### Tese central (Slide 8)
"O sucesso de founders não vem de ser mais inteligentes, mas de ter melhor pensamento mais rápido. Claude nunca dorme, não tem dias ruins e leu tudo sobre como construir empresas — trate-o como co-fundador."

## Insights para o wiki

- **Custom Instructions como modo persistente**: diferente dos prompts de sessão única documentados até aqui, o Founder Thinking Mode é instalado uma vez e herdado por todas as conversas subsequentes — uma evolução do padrão ROLE de [[prompt-engineering]]
- **"Here's what I'd actually do."** como constraint de comprometimento: a abertura obrigatória força o modelo a dar uma recomendação específica, eliminando hedging e frameworks genéricos — reforça o padrão de "Output Constraints" de [[yik-chan]]
- **Cobertura dos 5 pontos críticos de decisão do early-stage**: modelo de negócio (stress test), mercado (gap competitivo), executivo (kill the spiral), receita (hidden revenue) e time (hiring) — 5 dos 7 prompts de [[evolving-ai]] cobrem território diferente (análise de mercado, distribuição, escalonamento); as duas fontes são complementares
- **Contradição implícita com abordagem ROLE/TASK/STEPS**: [[evolving-ai]] e [[business-bulls]] estruturam cada prompt com seções nomeadas; aqui o poder está na instrução de modo permanente — o usuário simplesmente descreve o problema, e o contexto de "seasoned founder" está sempre ativo

## Entidades relacionadas
- [[prakash-kumar]] — autor do conteúdo (@startup.snack)
- [[claude-code]] — plataforma onde o modo é configurado

## Conceitos relacionados
- [[prompt-engineering]] — padrão de Custom Instructions como modo persistente de persona
- [[estratégia-de-negócios-com-ia]] — 6 casos de uso para tomada de decisão de founder
