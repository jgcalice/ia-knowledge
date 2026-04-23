---
title: "Gerencie Limites de Sessão em Claude Code"
type: source
source_file: "2026-04-20_nate_herk_ai_automation__qZvORxGqI0.md"
author: "@Nate Herk | AI Automation"
date: 2026-04-20
format: video
tags: [tokens, claude-code, otimização, sessão, contexto, sub-agentes, compactação]
source_url: "https://www.youtube.com/watch?v=_qZvORxGqI0"
source_count: 1
---

# Gerencie Limites de Sessão em Claude Code

> **Fonte:** [[2026-04-20_nate_herk_ai_automation__qZvORxGqI0]] | **Autor:** @Nate Herk | AI Automation | **Data:** 2026-04-20 | **Formato:** Vídeo YouTube (24min) | **[↗ Ver vídeo](https://www.youtube.com/watch?v=_qZvORxGqI0)**

## TL;DR

O janela de 1 milhão de tokens é um seguro, não uma meta — e boa gestão de sessão começa antes dos 20% do uso, com hábitos de compactação manual, sub-agentes e session handoff.

## Contexto

[[nate-herk]] é criador de conteúdo focado em AI Automation, com comunidade no Skool e cursos pagos. O vídeo responde à reclamação crescente da comunidade sobre hitting session limits no [[claude-code]], e apresenta o dashboard de tokens customizado que ele mesmo construiu e disponibilizou gratuitamente.

## O que foi ensinado

### Como tokens funcionam (mecânica real)
- **Cada mensagem** faz o Claude reler toda a conversa anterior — o custo é **exponencial, não aditivo**
- Exemplo: mensagem 1 = 500 tokens; mensagem 30 = 15.500 tokens (31x mais)
- Um desenvolvedor rastreou 100+ mensagens e descobriu que **98,5% dos tokens foram gastos relendo o histórico**
- Antes de digitar qualquer coisa, já há overhead: `/context` numa sessão fresca de Nate mostrou 62.000 tokens de startup (CLAUDE.md + MCPs + skills)

### Context rot — AI Dementia
- À medida que a sessão cresce, a acurácia de recuperação do modelo **cai de 92% (256k tokens) para 78% (1M tokens)**
- Sintomas: modelo edita arquivos sem ler, contradiz a si mesmo, fica vago e repetitivo
- Implicação: sessões longas são mais caras E produzem pior qualidade simultaneamente

### Auto compaction vs. Manual compaction
| Tipo | Quando dispara | Qualidade |
|------|---------------|-----------|
| Auto | 95% da janela | Retém só 20-30% dos detalhes; dispara no pico do context rot |
| Manual | ~60% da janela | Preserva mais contexto, modelo ainda está "inteligente" |

### Método de session handoff de Nate (substitui /compact)
1. Quando chega a ~120k tokens (12% da janela de 1M no Opus), Nate pede: *"Give me a full summary of everything we've done and current status"*
2. Copia o resumo
3. Faz `/clear`
4. Cola o resumo na nova sessão e continua

Ele construiu uma **skill `/session handoff`** que automatiza esse processo: lê tudo, extrai decisões bloqueadas, arquivos-chave, estado atual, perguntas abertas e gera o "pickup message" estruturado.

### Opções após cada resposta do Claude
1. **Continue** — responde e segue (mais fácil, mas compõe tokens)
2. **`/re` (Rewind)** — volta a qualquer mensagem anterior e descarta tudo depois; inclui opção "summarize from here" para criar handoff note
3. **`/clear`** — reinicia completamente
4. **`/compact`** — resume a sessão e substitui histórico pelo resumo
5. **Sub agent** — delega para janela de contexto nova e recebe apenas o resultado

### /btw — side questions que não entram no histórico
- `/btw` abre overlay para perguntas rápidas sem poluir o contexto da sessão principal
- Útil quando se está fundo em um projeto e precisa esclarecer algo pontual

### Sub-agentes para eficiência de tokens
- Cada sub-agente tem **janela de contexto fresca**
- Podem usar modelos mais baratos: *"spin up a sub agent to summarize this and make sure that sub agent is using Haiku"*
- Analogia: pesquisador interno — você não lê os 50 artigos junto com ele, só recebe o resumo

### Conversão para Markdown
| Formato | Redução de tokens |
|---------|------------------|
| HTML → Markdown | ~90% |
| PDF → Markdown | 65-70% |
| DOCX → Markdown | ~33% |

Um PDF de 40 páginas ocupa o mesmo espaço que um arquivo Markdown de 130 páginas.

### Plan Mode (Boris Cherny)
- O criador do Claude Code começa **toda sessão em plan mode**
- Investir tokens no plano upfront evita correções caras depois
- Nate usa Ultra Plan / Superpowers antes de construir

### CLAUDE.md discipline
- Manter **sob 200 linhas / ~2.000 tokens** — carrega a cada sessão
- Mover instruções especializadas para skills ou context files carregados on-demand
- Usar `.claudeignore` para excluir pastas/arquivos irrelevantes do repo

### Token dashboard customizado
- Nate construiu e disponibilizou repo público com dashboard de monitoramento
- Mostra: sessões, turns, input/output tokens, cache read/create, por projeto, por modelo, por skill invocada
- Permite identificar sessões caras e quais prompts consumiram mais tokens

### Frameworks externos para redução de tokens (10 repos)
- Rust Token Killer, Context Mode (SQL-lite ao invés de dump no contexto), Code Review Graph, Token Savior, Caveman Plugin, Claude Token Efficient, Token Optimizer MCP, Claude Context, entre outros
- Recomendação: escolher 2-3 específicos ao workflow do projeto, não usar todos ao mesmo tempo

### Regra dos 0-20% (Prime Time)
- Os primeiros 20% da sessão são o período de melhor performance
- CLAUDE.md está fresco, modelo ainda não sofre de context rot
- Nate usa 120k como limite pessoal no Opus (1M context) e reinicia via handoff

## Insights para o wiki

- **Confirma e aprofunda** o conceito de [[otimização-de-tokens]] com dados concretos: 98,5% de tokens gastos em rereading, queda de 14pp na acurácia de recuperação de 256k→1M
- **Novo conceito documentado**: "context rot" como degradação progressiva da qualidade — mais preciso do que apenas "sessão longa"
- **Expande** o conceito de sub-agentes: além de paralelizar, são uma estratégia primária de token management (modelo barato + contexto limpo)
- **Contradição parcial com /compact**: Sal Shirgaleev recomendou /compact como boa prática; Nate diz que não usa mais e prefere session handoff manual. Ambas as abordagens têm méritos — o ponto de divergência é o nível de controle desejado sobre o que é preservado

## Entidades relacionadas

- [[nate-herk]] — autor e criador do conteúdo
- [[claude-code]] — ferramenta central; comandos /re, /clear, /compact, /btw, /context discutidos
- [[markitdown]] — mencionado indiretamente (conversão para Markdown)

## Conceitos relacionados

- [[otimização-de-tokens]] — tema central do vídeo
- [[agentes-ia]] — sub-agentes como estratégia de token management
- [[prompt-engineering]] — plan mode, session handoff, CLAUDE.md discipline
