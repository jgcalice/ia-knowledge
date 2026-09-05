---
title: "20 Códigos Secretos para Melhorar Respostas de IA"
type: source
source_file: "2026-08-21_eduardo_cavalcanti_DcTsJ4VxJwi.md"
author: "@Eduardo Cavalcanti"
date: 2026-08-21
format: reel
tags: [prompt-engineering, claude, chatgpt, gemini, ativadores-semanticos, comandos, produtividade]
source_url: "https://www.instagram.com/reel/DcTsJ4VxJwi/?stkn=MXhnNm1ucmwxcjc5MQ=="
source_count: 1
---

# 20 Códigos Secretos para Melhorar Respostas de IA

> **Fonte:** [[2026-08-21_eduardo_cavalcanti_DcTsJ4VxJwi]] | **Autor:** @Eduardo Cavalcanti | **Data:** 2026-08-21 | **Formato:** reel (34s) | **[↗ Ver post](https://www.instagram.com/reel/DcTsJ4VxJwi/?stkn=MXhnNm1ucmwxcjc5MQ==)**

## TL;DR

20 pseudo-comandos com prefixo `/` (de uma lista de 50) que funcionam como convenção pessoal instalável em ChatGPT, Claude e Gemini — cobrindo análise crítica, tomada de decisão, ensino, verificação de fontes e formato de entrega.

## Contexto

Reel de @Eduardo Cavalcanti com gancho de captura de lead: mostra 20 dos 50 códigos que o autor usa, e oferece a lista completa (as outras 30, voltadas a operação de negócio — `/PREMORTEM`, `/TRADEOFF`, `/BLINDSPOT`, `/UNKNOWN`, `/NUMEROS`, `/ROI`, `/ESCALA`, `/CRISE`) em troca de um comentário ("RS3"). O post é explícito sobre a natureza do mecanismo: **não são comandos escondidos de nenhum modelo** — é uma convenção que o próprio usuário instala uma vez (via bloco colado no início da conversa) e pode alterar livremente.

## O que foi ensinado

Os 20 códigos, agrupados por função:

**Rigor analítico**
| Código | Efeito |
|--------|--------|
| `/EXPERT` | Responde como especialista sênior, sem simplificar |
| `/CRITIC` | Critica sem amenizar, aponta o que quebra primeiro |
| `/DEEP` | Vai três camadas abaixo da resposta óbvia |
| `/RISK` | Lista riscos por probabilidade e impacto |
| `/CHANCE` | Dá a chance em % com o raciocínio aberto |
| `/DEVIL` | Assume que o usuário está errado e argumenta contra |

**Tomada de decisão**
| Código | Efeito |
|--------|--------|
| `/DECISION` | Vira decisão: opções, critérios e uma recomendação |
| `/COMPARE` | Tabela com critérios declarados e veredito |
| `/ALT3` | Três caminhos genuinamente diferentes, não variações |
| `/PLAN` | Etapas com dono, prazo e critério de pronto |
| `/REVIEW` | Revisa com nota de 0 a 10 e devolve corrigido |
| `/ASK3` | Faz 3 perguntas antes de responder, e espera |

**Ensino e verificação**
| Código | Efeito |
|--------|--------|
| `/TEACHER` | Ensina do zero com analogia, exemplo e teste |
| `/SOURCE` | Só afirma o que tem fonte com link e data |
| `/RESEARCH` | Cruza 5 fontes e mostra onde elas divergem |
| `/CHECKLIST` | Vira checklist com item verificável |

**Formato de entrega**
| Código | Efeito |
|--------|--------|
| `/CANVAS` | Entrega em documento editável, não no chat |
| `/VISUAL` | Entrega diagrama ou fluxo com legenda |
| `/HANDOFF` | Empacota a conversa para colar em outro modelo |
| `/NATURAL` | Reescreve sem cara de texto de IA |

## Insights para o wiki

- **Quarta confirmação independente** do padrão "slash-command style activators" já documentado em [[2026-04-22_ai-developer-claude-secret-codes]] (13 comandos) e adjacente às palavras-gatilho sem prefixo de [[2026-04-08_gatilhos-cognitivos-claude]] e [[2026-04-22_castilho-6-palavras-claude]]. Esta é a lista mais extensa (20 de 50) e a mais explícita sobre o mecanismo: o autor afirma diretamente que os códigos **não são comandos nativos** de nenhuma IA — são convenção instalada pelo usuário via bloco de texto colado, e funcionam de forma agnóstica de plataforma (ChatGPT, Claude, Gemini).
- **Cobertura temática mais ampla e mais séria** que a lista de [[ai-developer-js]] (que tinha `/godmode`, `/ghost`, `/pitch` — tom mais "vibe"/casual). Aqui os 20 códigos organizam-se em quatro funções nítidas: rigor analítico, decisão, ensino/verificação e formato de entrega — sobreposição parcial com ativadores já documentados (`/DEVIL` ≈ Devil's Advocate de [[castilho]]; `/CRITIC`/`/REVIEW` ≈ padrão "Rasga isso" de [[nate-herk]]).
- **`/ASK3` formaliza como código o princípio de "perguntar antes de responder"** já visto de forma verbal em [[2026-04-27_nate-herk-32-hacks-claude-code]] (95% de confiança) — aqui virou um único código de 5 caracteres em vez de uma instrução de uma frase.
- **`/HANDOFF` é um padrão novo no wiki**: portabilidade de contexto *entre modelos diferentes* (Claude → ChatGPT → Gemini), distinto do "session handoff" de [[nate-herk]] ([[otimização-de-tokens]]), que resume contexto *dentro da mesma sessão/modelo* para liberar janela de tokens. Aqui o objetivo não é economizar tokens, é preservar continuidade ao trocar de fornecedor de LLM.
- **`/SOURCE` e `/RESEARCH` são a primeira formalização explícita de anti-alucinação como código** — "só afirma o que tem fonte com link e data" e "cruza 5 fontes e mostra onde divergem" endereçam diretamente o problema de invenção de fatos, algo que os pseudo-comandos anteriores (mais focados em tom e formato) não cobriam.

## Entidades relacionadas

- [[eduardo-cavalcanti]] — autor do conteúdo
- [[claude-code]] — uma das três plataformas onde os códigos funcionam (junto de ChatGPT e Gemini)

## Conceitos relacionados

- [[prompt-engineering]] — nova iteração da subcategoria "slash-command style activators", com foco em rigor analítico e anti-alucinação
