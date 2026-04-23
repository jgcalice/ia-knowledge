---
title: "Otimização de Tokens no Claude"
type: concept
tags: [tokens, otimização, claude, pdf, markdown, contexto, modelo]
source_count: 3
last_updated: 2026-04-21
---

# Otimização de Tokens no Claude

> **Fontes:** 3 | **Domínio:** Eficiência no uso de LLMs

## Por que importa

O número de tokens consumidos por sessão determina quanto você consegue fazer antes de atingir os limites do Claude. É uma das principais dores dos power users — e o tema mais recorrente no wiki até agora (3 fontes independentes).

## Técnicas documentadas

### 1. Pré-processamento de documentos
**Problema:** PDFs enviados diretamente ao Claude fazem o modelo ler o arquivo completo → alto consumo de tokens.

**Soluções:**
- **[[markitdown]]** (Microsoft) — converte PDF, Word, Excel, PPT, áudio, vídeo para Markdown limpo antes de enviar ao Claude ([[rafael-brandao]])
- **Modelo intermediário barato** — processar com Haiku/GPT-4o mini usando prompt de compressão ([[evolving-ai]], Hack #4)

### 2. Prompts concisos (Método "Caveman")
Usar um prompt de sistema que proíbe linguagem de preenchimento: sem "I'd be happy to", sem recapitulações, sem artigos desnecessários.
→ Redução de 30-50% nos tokens de output ([[evolving-ai]], Hack #1)

### 3. Escolha inteligente de modelo
| Modelo | Custo relativo | Melhor para |
|--------|---------------|-------------|
| Haiku | Baixo | Tarefas simples, alto volume |
| Sonnet | Médio | Código, análise, Q&A geral |
| Opus | ~5x Sonnet | Arquitetura complexa, debugging profundo |

([[evolving-ai]], Hack #3)

### 4. Code Review Graph
Para projetos de código: tool que usa Tree-sitter para mapear a estrutura e fazer o Claude ler apenas arquivos afetados pela mudança.
→ 8x menos tokens em revisões, até 49x em monorepos ([[evolving-ai]], Hack #2)

### 5. Compactação de contexto ("Compact Skill")
Para sessões longas: usar prompt de compressão para criar resumo de continuação entre sessões.
```
Summarize our entire conversation so I can paste it into a new chat and continue without losing context...
```
([[evolving-ai]], Hack #6)

### 6. Timing da sessão
- Abrir a janela de uso apenas quando pronto para trabalhar
- Concentrar trabalho pesado na primeira metade da janela
- Evitar horários de pico (dias úteis no horário comercial)

([[evolving-ai]], Hacks #5 e #7)

## Princípio unificador

> "The clearer and tighter your input, the less work Claude has to do, and the longer your session lasts before you hit a wall." — @Evolving AI

## Fontes

- [[2026-04-11_tokens-markdown]]
- [[2026-04-18_7-hacks-tokens-claude]]
- [[2026-04-11_transformacao-linkedin-ia]] (indiretamente — prompts concisos)
