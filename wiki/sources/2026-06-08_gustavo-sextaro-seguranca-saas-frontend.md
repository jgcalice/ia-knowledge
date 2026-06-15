---
title: "Segurança no Front-End do SaaS: Proteja Seus Dados e Requisições"
type: source
source_file: "2026-06-08_gustavo_sextaro_DZU-RaVRCrt.md"
author: "@Gustavo Sextaro"
date: 2026-06-08
format: reel
tags: [segurança, saas, front-end, javascript, next-js, env-vars, local-storage, cookies, cors, csp, desenvolvimento-web]
source_url: "https://www.instagram.com/reel/DZU-RaVRCrt/"
source_count: 1
---

# Segurança no Front-End do SaaS: Proteja Seus Dados e Requisições

> **Fonte:** [[2026-06-08_gustavo_sextaro_DZU-RaVRCrt]] | **Autor:** @Gustavo Sextaro | **Data:** 2026-06-08 | **Formato:** reel (121s) | **[↗ Ver post](https://www.instagram.com/reel/DZU-RaVRCrt/)**

## TL;DR

Cinco práticas de segurança do lado do cliente que impedem vazamentos de dados e acesso não autorizado ao seu SaaS, complementando os fundamentos de back-end.

## Contexto

Gustavo Sextaro é criador BR associado ao curso "MVP Ao SaaS". O reel aborda a "ponta do iceberg" de segurança para SaaS — especificamente o que pode ser visto, capturado ou abusado diretamente do front-end. O contexto pressuposto é desenvolvimento acelerado (vibecoding), onde front-end e back-end são construídos rapidamente com LLMs, deixando vulnerabilidades do lado cliente.

## O que foi ensinado

**1. Variáveis de ambiente — nunca com prefixo público**
- `NEXT_PUBLIC_` expõe a variável ao bundle client-side — qualquer pessoa no DevTools a vê
- Mesmo no Vite: sem o prefixo `VITE_`, a variável não vai ao cliente
- **Regra**: nenhuma chave de acesso (API key, segredo) tem prefixo público. Zero.

**2. Proteger Source Maps**
- Source maps no DevTools expõem o código TSX original — um atacante vê a estrutura exata do app
- Configurar Webpack/Vite para não gerar source maps em produção ou restringir acesso

**3. LocalStorage — não para tokens nem PII**
- LocalStorage é acessível por qualquer JavaScript na página (vulnerável a XSS)
- **Proibido guardar**: token de autenticação, e-mail, CPF, telefone, dados pessoais
- Tokens devem ir em cookies HTTP-only + Secure (inacessíveis ao JavaScript)

**4. Session Storage — limpeza automática**
- Session Storage persiste enquanto a aba está aberta — se não limpar, dados críticos ficam na memória
- Deve ser configurado para limpar automaticamente ao fechar a aba
- Não armazenar dados críticos nem tokens aqui

**5. CORS e CSP — configuração obrigatória (ponto mais avançado)**
- **CORS**: define quais origens externas podem fazer requisições à sua API — sem configuração correta, qualquer site pode chamar seus endpoints
- **CSP (Content Security Policy)**: define de onde scripts podem ser carregados — previne injeção de código externo malicioso
- O autor indica este como "mais confuso" e remete ao material do MVP Ao SaaS para detalhamento

## Insights para o wiki

1. **Complemento direto da Dimensão 1** de [[segurança-com-ia]]: Lucas Garcia Pit cobriu o lado back-end (API keys server-side, RLS, lógica server-side, rate limiting, webhooks). Gustavo Sextaro cobre o lado client-side (env vars, LocalStorage, Session Storage, cookies, CORS/CSP). Os dois formam o par completo de segurança para um SaaS construído com LLMs.

2. **Princípio unificador equivalente**: ambas as fontes seguem o mesmo princípio — "nunca confiar no cliente". Lucas Pit: lógica sensível só no servidor. Sextaro: tokens e chaves nunca no client-side storage.

3. **Regra do `NEXT_PUBLIC_`** é o anti-padrão mais comum em apps Next.js vibecoded: o desenvolvedor expõe a API key do Stripe, OpenAI ou Supabase no bundle client porque é mais fácil do que passar pelo servidor.

4. **Cookies HTTP-only como padrão de auth**: este é o padrão correto que o wiki ainda não tinha documentado explicitamente — tokens de autenticação devem ser gerenciados via cookies com flags HTTP-only + Secure, invisíveis ao JavaScript, em vez de LocalStorage.

## Entidades relacionadas

- [[gustavo-sextaro]] — criador BR, fundador do "MVP Ao SaaS"; foco em segurança e desenvolvimento de produto

## Conceitos relacionados

- [[segurança-com-ia]] — Dimensão 7: segurança no front-end do SaaS (complementa as 6 dimensões existentes)
- [[vibecoding]] — contexto que gera as vulnerabilidades front-end descritas aqui
