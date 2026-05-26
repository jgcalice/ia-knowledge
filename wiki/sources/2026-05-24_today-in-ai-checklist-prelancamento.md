---
title: "Checklist Pré-Lançamento Essencial para Apps de IA"
type: source
source_file: "2026-05-24_today_in_ai_DYvSElpEpui.md"
author: "@TODAY IN AI"
date: 2026-05-24
format: carousel
tags: [segurança, vibecoding, supabase, rls, gdpr, ccpa, owasp, validação, pré-lançamento, desenvolvimento, jurídico]
source_url: "https://www.instagram.com/p/DYvSElpEpui/?img_index=9"
source_count: 1
---

# Checklist Pré-Lançamento Essencial para Apps de IA

> **Fonte:** [[2026-05-24_today_in_ai_DYvSElpEpui]] | **Autor:** @TODAY IN AI (curadoria de @PrajwalTomar_ / X) | **Data:** 2026-05-24 | **Formato:** carousel (10 slides) | **[↗ Ver post](https://www.instagram.com/p/DYvSElpEpui/?img_index=9)**

## TL;DR

"Vibe coders are getting sued" — um dev com 20+ anos documenta a checklist que todo builder de app com IA deve executar *antes* de lançar para usuários reais: privacidade legal (GDPR/CCPA), Row Level Security no Supabase, testes em caminhos de falha, headers de segurança, revisão OWASP e validação no servidor além do Zod no cliente.

## Contexto

@TODAY IN AI (editorial aitickerdaily/curatedai.net) republica uma thread de segurança do X de @PrajwalTomar_ — desenvolvedor com 20+ anos e 60+ MVPs em contexto de agência. O conteúdo surge num momento em que "vibe coders" (devs que usam LLMs para construir apps rapidamente sem revisão de segurança) estão enfrentando processos judiciais por negligência no pré-lançamento. A thread original é de 25 de maio de 2026.

## O que foi ensinado

**Por que vibe coders estão sendo processados**
- Equipes otimizam para o *dia de demo*, não para o dia do breach
- Processos judiciais e vazamentos de dados atingem quem ignora a checklist pré-lançamento
- "Do not skip this before the next deploy with real user data" — regra número 1

**1. Conformidade legal (GDPR / CCPA)**
- O instante em que o app coleta dado do usuário, entra em território legal
- Mínimo obrigatório: publicar política de privacidade + saber exatamente onde o dado vive + não fazer nada duvidoso com as informações do usuário
- "Legal exposure scales with user count. Fix privacy before marketing scales traffic."

**2. Row Level Security (RLS) — #1 miss mais crítico**
- Sem RLS, qualquer pessoa pode abrir o DevTools e ler o banco inteiro — "not a hack. Not an exploit. Just open the browser console and query it"
- Caminho no Supabase: Authentication → Policies; se há zero policies, o banco está aberto
- Toda tabela com dado de usuário precisa de policies que restringem linhas ao proprietário autenticado
- "Ship RLS before inviting beta users"

**3. Testar além do happy path**
- A maioria dos devs só testa o fluxo ideal — falhas ocorrem quando algo dá errado
- O que testar: login com senha errada, reset de senha para e-mail inexistente
- Rate limiting, bloqueios e mensagens de erro **não devem revelar a existência de contas**
- "Demos on the happy path don't survive real users or attackers"

**4-5. Security Headers + OWASP**
- Revisar o app como especialista em segurança, garantindo headers de segurança fortes
- Headers sozinhos não são suficientes: OWASP ajuda a identificar SQL injection, XSS e controle de acesso quebrado
- Sequência: headers primeiro, OWASP segundo — antes de considerar o MVP pronto para produção

**6. Validação no servidor — Zod no cliente é UX, não segurança**
- "Attackers disable JavaScript, open Postman, and send whatever they want straight to the API"
- Se um form escreve no banco de dados, valide de novo no servidor — cliente não é fronteira de segurança
- Padrão: schemas duplicados — cliente para feedback instantâneo, servidor para enforcement
- "One unvalidated API route bypasses every form validator in the frontend"

**Lente de agência (60+ MVPs — @PrajwalTomar_)**
- Erros recorrentes em lançamentos de clientes: sem RLS no Supabase, sem política de privacidade até ser solicitado, QA só no happy path, rotas API confiando na validação do cliente
- "Builds that win demos, skipped checklists win incidents"
- Tratar segurança pré-lançamento como portão de liberação, não como tópico pós-morte

**Ordem de lançamento (pré-launch ship order)**

| Passo | Ação |
|-------|------|
| 1 | Política de privacidade + mapa de dados |
| 2 | Supabase RLS em cada tabela de usuários |
| 3 | Testes de auth em caminhos de falha |
| 4 | Security headers aprovados |
| 5 | Revisão OWASP |
| 6 | Validação server-side em cada rota de escrita |
| ✓ | Somente então: escalar marketing ou cobrar usuários |

"Each layer takes minutes to hours, not weeks."

## Insights para o wiki

**Novo ângulo — consequência jurídica do vibecoding**: as dimensões 1 e 4 de [[segurança-com-ia]] abordam como *construir com segurança* e como *auditar antes de fazer deploy*. Este post acrescenta uma 6ª dimensão: o que verificar na ordem certa *antes de lançar para usuários reais*, com foco explícito em conformidade legal (GDPR/CCPA) como portão obrigatório. A expressão "getting sued" é o primeiro registro do wiki de **consequência jurídica concreta** decorrente de segurança neglicenciada no vibecoding.

**Confirmações e extensões de material existente**:
- Confirma o ponto #02 de [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] (RLS no Supabase), mas com perspectiva de consequência: "who can open DevTools and read your database in 2 minutes"
- Estende o ponto #03 do mesmo post (lógica sensível no servidor) com o caso específico do Zod no cliente — a distinção UX vs. segurança não estava documentada antes
- Adiciona testing de failure paths como novo requisito pré-lançamento (não coberto em nenhuma dimensão anterior)
- Adiciona security headers + OWASP como etapa pré-MVP (novo item operacional)

**Contribuição de @PrajwalTomar_**: a lente de 60+ MVPs é valiosa porque confirma que esses erros são *sistemáticos*, não acidentais — padrão de agência, não caso isolado.

## Entidades relacionadas

- [[today-in-ai]] — canal agregador que republica o conteúdo de aitickerdaily/curatedai.net

## Conceitos relacionados

- [[segurança-com-ia]] — este post adiciona Dimensão 6 (pré-lançamento jurídico-técnico) e confirma pontos das Dimensões 1 e 4
- [[vibecoding]] — o causal link "vibecoding → processo jurídico" é formalizado aqui pela primeira vez no wiki
