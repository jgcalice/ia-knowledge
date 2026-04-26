---
title: "Vibecoding"
type: concept
tags: [vibecoding, desenvolvimento, llm, segurança, produtividade, claude-code]
source_count: 1
last_updated: 2026-04-26
---

# Vibecoding

> Desenvolvimento acelerado de software guiado por LLMs, onde o programador descreve a intenção ("vibe") e o modelo gera o código. Alta velocidade de entrega, mas com risco proporcional de acumular débito de segurança invisível.

## Definição

Vibecoding é a prática de construir apps com LLMs de forma iterativa e rápida, onde:
- O desenvolvedor descreve o que quer em linguagem natural
- O LLM (ex: Claude Code) gera, itera e corrige o código
- O ciclo feedback-geração é muito mais rápido do que o desenvolvimento tradicional

O termo carrega uma tensão embutida: a "vibe" de produtividade contrasta com o rigor que segurança exige.

## O problema central

> "The dirty secret of vibecoding is that speed and security are inversely correlated. The faster you ship, the more assumptions you skip. And every skipped assumption is an attack surface."
> — @thewizeai via [[artificial-intelligence-business]]

### Por que vibecoding cria vulnerabilidades

| Dinâmica | Consequência de segurança |
|---|---|
| Código gerado sem revisão crítica | LLMs geram código funcional, não necessariamente seguro |
| Sem auth checks | Endpoints expostos sem autenticação |
| Sem validação de entrada | XSS, SQL injection, CSRF |
| Sem ideia do que está exposto | Dados sensíveis em localStorage, logs, APIs abertas |
| Velocidade > revisão | Assumptions puladas = attack surface acumulada |

## Relação com segurança

Duas abordagens documentadas no wiki para mitigar riscos de vibecoding:

### Abordagem preventiva (design-time)
[[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 fundamentos que devem ser configurados **antes** de vibercodar:
1. API keys no servidor, nunca no front-end
2. RLS ativo no Supabase
3. Lógica sensível apenas no servidor
4. Rate limiting nas APIs
5. Webhooks com assinatura verificada

### Abordagem detective (pré-deploy)
[[2026-04-25_vibecoding-seguranca-auditoria-ia]] — Prompt red team que instrui o agente a auditar o codebase inteiro como um engenheiro de segurança sênior, cobrindo:
- Auth/Input Handling, Data Security, API Logic
- Infrastructure & Supply Chain
- Ameaças avançadas: exploit chains, timing attacks, cache poisoning

**As duas abordagens são complementares**: preventiva evita os erros mais comuns; detective pega o que passou.

## Relação com produtividade

Vibecoding é a face prática de usar LLMs para desenvolvimento — a mesma velocidade que [[claude-code]] proporciona para gerar leads, criar marcas, construir web apps, escrever código e automatizar processos. Os clusters de produtividade do wiki (leads, negócios, carreira) são todos habilitados indiretamente por vibecoding.

## Fontes

- [[2026-04-25_vibecoding-seguranca-auditoria-ia]] — auditoria red team para apps vibecoded (via @thewizeai)
- [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 fundamentos de segurança preventivos
