---
title: "Segurança no Uso do Claude Code"
type: source
source_file: "2026-04-15_lucas_garcia_pit_pit_ia_negocios_DXJw3MkkScn.md"
author: "@Lucas Garcia Pit | IA & Negócios"
date: 2026-04-15
format: carousel
tags: [claude-code, segurança, desenvolvimento, api, supabase, backend]
source_url: "https://www.instagram.com/p/DXJw3MkkScn/"
source_count: 1
---

# Segurança no Uso do Claude Code

> **Fonte:** [[2026-04-15_lucas_garcia_pit_pit_ia_negocios_DXJw3MkkScn]] | **Autor:** @Lucas Garcia Pit | **Data:** 2026-04-15 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXJw3MkkScn/)**

## TL;DR

O problema de segurança em apps com Claude Code não é a ferramenta — é o desenvolvedor que ignora os fundamentos: 5 práticas eliminam 99% das vulnerabilidades.

## Contexto

O carousel combate a narrativa de que "Claude Code gera código vulnerável por padrão". Lucas Pit argumenta que a fragilidade é comportamental, não da ferramenta. O post é direcionado a devs/empreendedores que usam Claude Code para construir apps e podem criar brechas por desconhecimento de boas práticas de back-end.

## O que foi ensinado

**5 pontos de segurança fundamentais:**

- **Ponto 01 — API keys nunca no front-end**: Chaves de API pertencem ao servidor. Ninguém do lado externo precisa de acesso.
- **Ponto 02 — RLS ativo no Supabase**: Row Level Security garante que cada usuário enxergue apenas seus próprios dados. Sem RLS, qualquer usuário acessa tudo.
- **Ponto 03 — Lógica sensível só no servidor**: Preço nunca vem do cliente; pagamento processa no servidor; regras de negócio ficam protegidas.
- **Ponto 04 — Rate limit nas APIs**: Limitar requisições por usuário por minuto previne abuso e ataques de negação de serviço.
- **Ponto 05 — Webhooks com assinatura verificada**: Validar a assinatura da requisição garante autenticidade; qualquer um pode chamar seu endpoint se você não verificar.

## Insights para o wiki

- Primeira fonte que aborda **segurança no desenvolvimento com IA** — abre um novo cluster temático.
- Reforça a narrativa anti-FUD: Claude Code não é inerentemente inseguro; o risco está no uso negligente.
- Os 5 pontos são práticas de back-end clássicas (não específicas de IA), mas a mensagem implícita é que **LLMs aceleram tanto o desenvolvimento que novatos pulam fundamentos de segurança**.
- Complementa [[claude-code]] ao adicionar a dimensão de "o que proteger quando Claude Code escreve seu código".

## Entidades relacionadas

- [[lucas-garcia-pit]] — autor do conteúdo
- [[claude-code]] — ferramenta central mencionada no título e contexto

## Conceitos relacionados

- [[segurança-com-ia]] — práticas de segurança ao construir apps com IA
- [[estratégia-de-negócios-com-ia]] — contexto de quem usa Claude Code para construir produtos
