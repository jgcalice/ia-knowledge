---
title: "Otimização de Tokens no Claude"
type: concept
tags: [tokens, otimização, claude, pdf, markdown, contexto, modelo, sessão, context-rot]
source_count: 6
last_updated: 2026-04-23
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

### 5. Compactação de contexto (`/compact`)
Para sessões longas: o comando built-in `/compact` comprime o histórico da sessão sem perder a intenção original, permitindo continuar no mesmo chat. Deve ser usado **proativamente**, não apenas quando o contexto estourar.
([[sal-shirgaleev]], [[2026-04-22_sal-shirgaleev-5-comandos-claude]])

> Anteriormente documentado como "Compact Skill" em [[evolving-ai]] (Hack #6 de [[2026-04-18_7-hacks-tokens-claude]]): variante manual via prompt de resumo. O comando `/compact` é a versão built-in equivalente.

### 6. Timing da sessão
- Abrir a janela de uso apenas quando pronto para trabalhar
- Concentrar trabalho pesado na primeira metade da janela
- Evitar horários de pico (dias úteis no horário comercial)

([[evolving-ai]], Hacks #5 e #7)

### 7. Grafo de conhecimento (Graphify)
Instalar [[graphify]] no workspace do Claude Code: a ferramenta escaneia todos os arquivos e constrói um grafo estruturado. Adicionar ao CLAUDE.md a instrução de consultar o grafo antes de ler arquivos brutos.
→ Redução de 20.000 → 280 tokens/sessão (**71,5x menos**) ([[marc-cleroux]])

Técnica baseada no sistema de [[andrej-karpathy]] (ex-OpenAI/Tesla). Visualização possível via [[obsidian]] graph view.

### 8. Mecânica real dos tokens — custo exponencial
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

- Cada mensagem faz o Claude **reler toda a conversa** desde o início — custo compõe, não soma
- Mensagem 1 = ~500 tokens; Mensagem 30 = ~15.500 tokens (31x mais)
- Análise de 100+ msgs por um desenvolvedor: **98,5% dos tokens foram gastos relendo histórico**
- Sessões frescas já consomem overhead: [[claude-code]] pode partir de 62.000 tokens antes do primeiro prompt (CLAUDE.md + MCPs + skills)

### 9. Context rot — degradação progressiva de qualidade
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

- À medida que a sessão cresce, a atenção do modelo se dispersa e a qualidade degrada
- **Dados**: acurácia de recuperação cai de 92% (256k tokens) → 78% (1M tokens)
- Sintomas: edição de arquivos sem leitura, contradições, respostas vagas
- Implicação: sessões longas custam mais E produzem pior output — o problema é duplo
- Análise de 18.000 thinking blocks / 7.000 sessões: profundidade de thinking caiu 67% com sessões mais longas; "edit without reading" foi de 6% → 34%

### 10. Compactação manual vs. automática
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

> ⚠️ Complementa (e amplia) a Técnica #5 (compactação com `/compact`)

| Tipo | Quando dispara | Resultado |
|------|---------------|-----------|
| Auto compaction | 95% da janela | Retém 20-30% dos detalhes; dispara no pico do context rot |
| `/compact` | Manual | Resume o histórico, melhor que auto mas ainda perde contexto |
| Session handoff (Nate) | ~12% da janela (120k/1M) | Resumo controlado + `/clear` + nova sessão com handoff = melhor qualidade |

**Método session handoff:**
1. Pedir ao Claude: *"Give me a full summary of everything we've done and current status"*
2. Copiar o resumo
3. `/clear` — janela completamente fresca
4. Colar o resumo e continuar

[[nate-herk]] construiu uma skill `/session handoff` que automatiza esse processo e gera um output estruturado com: decisões bloqueadas, arquivos-chave, estado atual e perguntas abertas.

> Divergência registrada: [[sal-shirgaleev]] recomenda `/compact` como boa prática; [[nate-herk]] diz que abandonou `/compact` em favor do session handoff manual. Ambas são válidas — a diferença é o nível de controle sobre o que é preservado.

### 11. /rewind — voltar no tempo e limpar contexto
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

- `/re` (double ESC ou comando): pula para qualquer mensagem anterior e descarta tudo depois
- Inclui opção "summarize from here" para criar handoff note a partir daquele ponto
- Prática recomendada pela Anthropic: usar após tentativas falhas em vez de deixar código errado no contexto

### 12. /btw — perguntas laterais sem poluir o contexto
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

- `/btw` abre overlay para perguntas rápidas que **não entram no histórico da sessão**
- Mantém o contexto principal limpo enquanto resolve dúvidas pontuais

### 13. Regra dos 0-20% (Prime Time)
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

- Os primeiros 20% da sessão têm melhor performance: CLAUDE.md fresco, sem context rot
- [[nate-herk]] usa 120k tokens como limite pessoal no Opus (1M ctx) e reinicia via session handoff
- Um usuário foi de $345/mês → $42.000/mês apenas por maus hábitos de contexto (sem aumento de output quality)

## Princípio unificador

> "The clearer and tighter your input, the less work Claude has to do, and the longer your session lasts before you hit a wall." — @Evolving AI

> "The 1 million token window is insurance, not a goal to fill." — @Nate Herk

## Fontes

- [[2026-04-11_tokens-markdown]]
- [[2026-04-18_7-hacks-tokens-claude]]
- [[2026-04-11_transformacao-linkedin-ia]] (indiretamente — prompts concisos)
- [[2026-04-12_graphify-memoria-infinita-claude]]
- [[2026-04-22_sal-shirgaleev-5-comandos-claude]]
- [[2026-04-20_nate-herk-gerenciar-limites-sessao]]
