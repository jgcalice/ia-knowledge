---
title: "Vibecoding"
type: concept
tags: [vibecoding, desenvolvimento, llm, segurança, produtividade, claude-code, jurídico, gdpr, pré-lançamento, front-end, local-storage, cookies, ios, ferramentas, stack, ui, animação, svg, mcp, claude-skills, design]
source_count: 6
last_updated: 2026-08-19
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

Três abordagens documentadas no wiki para mitigar riscos de vibecoding:

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

### Abordagem jurídico-técnica (pré-lançamento)
[[2026-05-24_today-in-ai-checklist-prelancamento]] — Checklist ordenada de 6 itens obrigatórios antes de abrir para usuários reais, curada de 60+ MVPs em contexto de agência (@PrajwalTomar_):
1. Política de privacidade + mapa de dados (GDPR/CCPA desde o 1º dado coletado)
2. RLS em cada tabela de usuário no Supabase
3. Testes em caminhos de falha (login errado, reset para e-mail inexistente)
4. Security headers aprovados
5. Revisão OWASP
6. Validação server-side em cada rota de escrita (Zod no cliente é UX, não segurança)

A distinção desta abordagem: foco em **conformidade legal** e **consequência jurídica** — "vibe coders are getting sued". A sequência importa: escalar marketing antes de completar todos os 6 passos amplifica o risco.

### Abordagem front-end específica (client-side)
[[2026-06-08_gustavo-sextaro-seguranca-saas-frontend]] — 5 práticas de segurança especificamente para o lado cliente do SaaS, que vibecoding frequentemente ignora:
1. Nenhuma chave de acesso com prefixo `NEXT_PUBLIC_` ou `VITE_` (expõe no bundle JS)
2. Source maps desativados ou restritos em produção
3. LocalStorage proibido para tokens e PII (e-mail, CPF, telefone)
4. Cookies de auth com flags HTTP-only + Secure (invisíveis ao JavaScript)
5. Session Storage com limpeza automática ao fechar aba; CORS e CSP configurados

**As quatro abordagens são complementares**: preventiva (back-end) e front-end evitam os erros mais comuns no design; detective pega o que passou antes do deploy; jurídico-técnica garante conformidade legal e sequência correta antes do lançamento para usuários reais.

## Stack de ferramentas para vibe coders iOS

[[2026-06-28_joaquin-fernandez-ferramentas-vibecoding-ios]] (@Joaquin Fernandez) documenta cinco ferramentas que formam a toolchain de referência para quem vibecoda em iOS:

| Ferramenta | Papel | Novidade no wiki |
|-----------|-------|-----------------|
| [[shadcn-ui]] | Base layer de componentes (código no projeto, editável pelo LLM) | Primeira menção — padrão de facto do ecossistema |
| [[10x-app-builder]] | Descrição → app iOS nativo SwiftUI, App Store ready | Primeiro builder iOS nativo por descrição do wiki |
| [[21st-dev]] | Marketplace de componentes + geração por IA sob demanda | Padrão "marketplace + IA generativa" (ver também [[smithery]]) |
| Animista | Criação visual de CSS animations | Ferramenta puramente visual, sem camada de IA |
| Phosphor Icons | Set de ícones em 6 pesos visuais | Design token; cobre todos os estilos de um app |

**Distinção relevante**: [[10x-app-builder]] expande o paradigma vibecoding além do web — pela primeira vez no wiki, "descreve e aparece" chega ao iOS nativo (SwiftUI), sem Xcode. O stack web análogo seria [[claude-code]] + [[lovable]], mas a stack iOS tem um único ponto de entrada: o 10X.

**Padrão emergente**: [[shadcn-ui]] ter o código no projeto (não em node_modules) é o que o torna ideal para vibecoding — o LLM consegue ler, modificar e estender qualquer componente como arquivo normal.

## Stack de ferramentas visuais para vibe coders web

[[2026-08-05_aleeshh-ferramentas-vibecore]] (@aleeshh) documenta quatro ferramentas que resolvem o gargalo estético do "site vibecoded que parece amador":

| Ferramenta | Papel | Novidade no wiki |
|-----------|-------|-----------------|
| [[watermelon-ui]] | Biblioteca open source de componentes para landing pages | Especializada em landing pages, vs. [[shadcn-ui]] (generalista) |
| [[motion-primitives]] | Código de animação copy-paste | Primeira ferramenta do wiki dedicada especificamente a animação |
| [[menace]] | App builder sem código — gera back-end e front-end por descrição | Terceira ferramenta "descreva e apareça" full-stack, após [[10x-app-builder]] (iOS) e [[lovable]] (web) |
| [[hyke]] | Gerador gratuito de backgrounds SVG (blobs, gradientes, waves) | Primeira ferramenta do wiki para geração de assets visuais vetoriais |

**Mesmo gênero editorial do stack iOS**: @aleeshh replica o formato "X ferramentas que todo vibe coder deveria conhecer" já documentado por [[joaquin-fernandez]], mas com foco em front-end web em vez de iOS nativo — inclusive usando "VibeCore" como variação de vocabulário para o mesmo conceito de "vibe coder".

**Lacuna preenchida**: até esta fonte, o wiki cobria componentes ([[shadcn-ui]]) e app builders ([[10x-app-builder]], [[21st-dev]]), mas não animação nem geração de arte de fundo — [[motion-primitives]] e [[hyke]] fecham essas duas categorias.

## Stack nativo do Claude para sites profissionais (Skills + MCP)

[[2026-08-19_vinicius-delmonego-sites-claude]] (@Vinícius Delmônego) documenta uma quarta variação de stack de vibecoding — diferente das anteriores (iOS: [[joaquin-fernandez]]; web visual: [[aleeshh]]), esta é composta 100% por recursos nativos do ecossistema Claude, sem ferramentas de terceiros:

| Componente | Tipo | Papel |
|-----------|------|-------|
| Milkovalski Design | [[claude-skills]] | Layout moderno |
| Impeccable Design | [[claude-skills]] | Tipografia e espaçamento |
| Taste Skill | [[claude-skills]] | Busca inspiração em sites reais em vez de gerar do zero |
| [[figma]] | MCP | Monta o site diretamente na ferramenta de design |
| [[playwright]] | MCP | Testa o site automaticamente antes da entrega |

**Distinção relevante**: as três stacks de vibecoding do wiki agora cobrem ângulos diferentes do mesmo problema (site/app com "cara de IA"): iOS usa builders e bibliotecas de componentes de terceiros; web visual usa bibliotecas de UI e animação; esta usa apenas Skills + MCP nativos do Claude — o "gosto visual" e o "teste" viram configuração do próprio agente, não ferramenta externa. Primeira aparição de MCPs de design ([[figma]]) e QA ([[playwright]]) no wiki.

## Relação com produtividade

Vibecoding é a face prática de usar LLMs para desenvolvimento — a mesma velocidade que [[claude-code]] proporciona para gerar leads, criar marcas, construir web apps, escrever código e automatizar processos. Os clusters de produtividade do wiki (leads, negócios, carreira) são todos habilitados indiretamente por vibecoding.

## Fontes

- [[2026-04-25_vibecoding-seguranca-auditoria-ia]] — auditoria red team para apps vibecoded (via @thewizeai)
- [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 fundamentos de segurança preventivos back-end
- [[2026-05-24_today-in-ai-checklist-prelancamento]] — checklist jurídico-técnica pré-lançamento; consequência jurídica como motivador explícito do vibecoding responsável
- [[2026-06-08_gustavo-sextaro-seguranca-saas-frontend]] — 5 práticas client-side de segurança front-end: env vars, LocalStorage, cookies HTTP-only, Session Storage, CORS/CSP
- [[2026-06-28_joaquin-fernandez-ferramentas-vibecoding-ios]] — stack de 5 ferramentas para vibe coders iOS: ShadCN + 10X + 21st Dev + Animista + Phosphor Icons
- [[2026-08-05_aleeshh-ferramentas-vibecore]] — stack de 4 ferramentas visuais para vibe coders web: Watermelon UI + Motion Primitives + Menace + Hyke
- [[2026-08-19_vinicius-delmonego-sites-claude]] — stack nativo Claude para sites profissionais: 3 Skills (Milkovalski Design, Impeccable Design, Taste Skill) + 2 MCPs (Figma, Playwright)
