---
title: "Segurança com IA"
type: concept
tags: [segurança, claude-code, desenvolvimento, api, backend, supabase]
source_count: 1
last_updated: 2026-04-23
---

# Segurança com IA

> Práticas de segurança para apps construídos com LLMs, especialmente Claude Code.

## Tese

Ferramentas de IA como Claude Code não são inerentemente inseguras — o risco está no desenvolvedor que, acelerado pela IA, pula fundamentos clássicos de segurança back-end. A velocidade de geração de código com LLMs amplia o gap entre "funciona" e "é seguro".

## Os 5 fundamentos (via @Lucas Garcia Pit)

Documentados em [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]]:

| Ponto | Prática | Por quê |
|-------|---------|---------|
| 01 | API keys no servidor, nunca no front-end | Expor no front-end = qualquer um usa sua chave |
| 02 | RLS ativo no Supabase | Sem Row Level Security, usuário A acessa dados de B |
| 03 | Lógica sensível apenas no servidor | Preço, pagamento e regras de negócio não podem vir do cliente |
| 04 | Rate limiting nas APIs | Previne abuso e ataques de negação de serviço |
| 05 | Webhooks com assinatura verificada | Valida que a requisição veio de quem diz que veio |

## Padrão subjacente

Todos os 5 pontos seguem o mesmo princípio: **nunca confiar no cliente**. É o princípio clássico de "zero trust" aplicado a apps construídos com LLMs.

## Relação com desenvolvimento acelerado por IA

Claude Code gera código funcional em minutos — mas velocidade sem segurança cria vulnerabilidades invisíveis. O anti-padrão mais comum: dev usa Claude Code para tudo (incluindo front-end) e expõe API keys no bundle JS sem perceber.

## Fontes

- [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 pontos de segurança para apps com Claude Code
