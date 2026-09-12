---
title: "10 Habilidades Incríveis para Usar com Claude"
type: source
source_file: "2026-08-26_neeraj_chemburkar_DcgjbHxkVFh.md"
author: "@Neeraj Chemburkar"
date: 2026-08-26
format: carousel
tags: [claude, claude-code, ferramentas-ia, open-source, agentes-ia, prompt-engineering, design, vídeo]
source_url: "https://www.instagram.com/p/DcgjbHxkVFh/?img_index=12&stkn=Zml6cTRmcXY4aWU3"
source_count: 1
---

# 10 Habilidades Incríveis para Usar com Claude

> **Fonte:** [[2026-08-26_neeraj_chemburkar_DcgjbHxkVFh]] | **Autor:** @Neeraj Chemburkar | **Data:** 2026-08-26 | **Formato:** Carousel | **[↗ Ver post](https://www.instagram.com/p/DcgjbHxkVFh/?img_index=12&stkn=Zml6cTRmcXY4aWU3)**

> ⚠️ Ingestão parcial: apenas 10 de 14 slides processados (`MAX_SLIDES_TO_PROCESS` no `.env` do capturador). Os slides ausentes provavelmente cobrem os 3 repositórios restantes citados na caption (xAI For You ranking, buzz do Block) — não documentados aqui.

## TL;DR

Curadoria de repositórios GitHub (chamados de "Claude skill folders") que somam mais de 500.000 estrelas, cobrindo design de landing page 3D, context engineering, memória via knowledge graph, integração cruzada Claude↔Codex, correção de "cara de site feito por IA", gravação de tela open-source e geração automática de vídeo vertical.

## Contexto

Post no formato "lista numerada com prova social" (stars do GitHub como métrica de credibilidade), mesmo template narrativo já visto em [[cooper-simson]], [[growai]], [[bestapps-ai]] e [[paras-madan]]. Diferencial aqui: enquadra os repositórios como **"Claude skill folders"** — uma pasta de instruções que o Claude lê antes de trabalhar e que "acompanha todas as sessões subsequentes" — aproximando o conceito de instalação de repo do conceito formal de [[claude-skills]].

## O que foi ensinado

- **Definição de skill (slide 2)**: "uma pasta de instruções que o Claude lê antes de trabalhar" — instalação única, ganho em toda sessão seguinte ("One install upgrades every session after it").
- **Skill 1 — [[scroll-world]]**: gera landing page 3D com câmera em voo contínuo entre cenas ao rolar a página; 100% gerado por IA, zero stock footage; ~$27 em créditos de vídeo por página de 6 cenas; 8.581 estrelas em 7 semanas.
- **Skill 2 — [[gsd]]**: workflow de 5 fases com comandos dedicados (`/gsd-discuss-phase`, `/gsd-plan-phase`, `/gsd-execute-phase`, `/gsd-verify-work`, `/gsd-ship`); 64.642 estrelas.
- **Skill 3 — [[graphify]]**: confirma dados já documentados via [[marc-cleroux]], com números novos — 110.416 estrelas, **apoiado pelo Y Combinator**, 37 idiomas analisados localmente, custo $0 para construir o grafo, "10x de memorização".
- **Skill 4 — [[codex-plugin-cc]]**: plugin oficial da OpenAI que roda o Codex dentro do Claude Code — `/codex:review` (segunda opinião), `/codex:adversarial-review` (ataca suposições), `/codex:rescue` (resgata sessão travada); 32.354 estrelas; funciona na camada gratuita do ChatGPT.
- **Skill 5 — diagram-design** (cathrynlavery): lê um site, escreve o guia de estilo e gera 39 tipos de diagrama editorial × 3 variantes, em HTML/SVG sem etapa de compilação; 26.758 estrelas em 4 meses. Mesmo autor e repositório já catalogados em [[claude-skills]] via [[fabiano-carvalho]] — **confirmação cruzada** de um repo citado antes como skill de design, agora com métrica de tração.
- **Skill 6 — impeccable** (Paul Bakhaus, criador do jQuery UI): 23 comandos (polish, audit, critique, animate), 59 regras determinísticas que detectam "tells" de IA (fonte Inter, gradientes roxos, cards aninhados); 62.534 estrelas. Mesmo repo já catalogado em [[claude-skills]] via [[fabiano-carvalho]] e [[vinicius-delmonego]] — **3ª confirmação independente** deste repositório específico.
- **Skill 7 — [[cap]]**: alternativa open-source ao Loom — grava, edita e compartilha vídeos de tela; auto-hospedagem via `docker compose up -d`; Instant Mode (link imediato) e Studio Mode (edição, legendas, exportação 4K); 21.228 estrelas.
- **Skill 8 (slide 10) — [[moneyprinterturbo]]**: gera vídeo vertical completo a partir de um tópico — roteiro via 15+ LLMs, imagens gratuitas, voz, legendas, publicação em TikTok/YouTube; 116.387 estrelas, 10.647 na última semana.

## Insights para o wiki

- **Graphify ganha dado novo e relevante**: apoio do **Y Combinator** não estava documentado na fonte original ([[2026-04-12_graphify-memoria-infinita-claude]]) — atualiza [[graphify]] e reforça [[dados-como-moat]]/[[otimização-de-tokens]] como área com investimento institucional, não só hobby open-source.
- **GSD ganha estrutura formal**: até agora só era citado por [[nate-herk]] como item de uma stack de 6; esta fonte detalha o workflow interno de 5 fases com comandos exatos — primeira vez que o wiki documenta a mecânica completa do GSD, não só sua existência.
- **Confirmação cruzada rara**: dois repositórios (diagram-design e impeccable) aparecem *pela terceira e segunda vez respectivamente* no wiki, vindos de fontes completamente diferentes (curadoria de design vs. curadoria de "top repos do GitHub") — evidência de que certas skills atingiram massa crítica de reconhecimento no nicho, independente do ângulo de curadoria.
- **Interoperabilidade entre labs rivais**: `codex-plugin-cc` é o primeiro caso documentado no wiki de uma lab (OpenAI) construindo integração oficial *dentro* do produto de uma concorrente (Anthropic/Claude Code) — sinal de que "terminal como plataforma neutra" está se tornando um padrão de mercado, não um hack de usuário.
- **Vídeo automatizado ganha 2º ponto de dados**: [[moneyprinterturbo]] confirma o padrão já visto com Hyperframes ([[growai]], [[cooper-simson]]) de pipeline completo de vídeo vertical monetizável a partir de texto.

## Entidades relacionadas

- [[neeraj-chemburkar]] — autor do conteúdo
- [[scroll-world]] — landing page 3D gerada por IA
- [[gsd]] — workflow de 5 fases para "spec-driven development"
- [[graphify]] — atualizado com apoio YC e novos números
- [[codex-plugin-cc]] — plugin oficial OpenAI dentro do Claude Code
- [[cap]] — alternativa open-source ao Loom
- [[moneyprinterturbo]] — geração automática de vídeo vertical
- [[claude-skills]] — confirmação cruzada de diagram-design e impeccable

## Conceitos relacionados

- [[agentes-ia]] — GSD como orquestração de sub-agentes em paralelo; codex-plugin-cc como agente de segunda opinião
- [[otimização-de-tokens]] — graphify como solução de memória/context engineering, agora com apoio institucional
- [[estratégia-de-negócios-com-ia]] — vídeo automatizado (MoneyPrinterTurbo) e landing pages 3D (scroll-world) como novos arquétipos de produto monetizável
- [[vibecoding]] — impeccable e diagram-design como correção de "cara de site feito por IA"
