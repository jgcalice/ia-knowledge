---
title: "Prompt Engineering"
type: concept
tags: [prompt-engineering, prompts, llm, claude, técnicas]
source_count: 10
last_updated: 2026-04-21
---

# Prompt Engineering

> **Fontes:** 3 | **Domínio:** Técnicas de uso de LLMs

## Definição

Conjunto de técnicas para estruturar instruções enviadas a LLMs de forma a obter resultados mais úteis, precisos e eficientes.

## Padrões documentados no wiki

### Prompts parametrizados
Prompts com campos obrigatórios a preencher. Reduzem ambiguidade e permitem reutilização:
- `[perfil LinkedIn]`, `[currículo]`, `[cargo-alvo]` — [[bruno-souza]]
- `[nicho]`, `[cidade]`, `[quantidade]` — [[hudson-brendon]]

### Prompts com constraints explícitas
Definir limites específicos melhora a saída:
- "até 120 caracteres" (headline LinkedIn)
- "menos de 2000 caracteres" (About LinkedIn)
- "3 versões com menos de 300 caracteres cada" (mensagens de referência)
→ [[2026-04-11_transformacao-linkedin-ia]]

### Prompts de sistema de comportamento
Instruções permanentes que mudam como o modelo responde:
- Método "Caveman": proíbe linguagem de preenchimento → reduz 30-50% dos tokens de output
- "Compact Skill": comprime histórico de conversa para continuidade entre sessões
→ [[2026-04-18_7-hacks-tokens-claude]]

### Prompts de compressão de documentos
Template para resumir documentos antes de enviar ao LLM principal:
```
Read this document end to end. Output a condensed plain-text version that preserves: 
(1) all factual claims, numbers, dates, and names; 
(2) every actionable instruction or recommendation; 
(3) the document's structure as short headings. 
Target 20 to 30 percent of the original length.
```
→ [[2026-04-18_7-hacks-tokens-claude]]

### Contextualização de ICP
Antes de scraping de leads: fornecer ao LLM contexto completo sobre o projeto, o ICP e o lead ideal. A qualidade do briefing determina a qualidade dos leads.
→ [[2026-03-19_leads-infinitos-cloudcode]]

## Princípio central

Prompts mais específicos e restritivos geralmente produzem resultados mais úteis e consomem menos tokens. A imprecisão no input gera imprecisão e verbosidade no output.

### Prompts com estrutura ROLE/TASK/STEPS/RULES/OUTPUT
Formato ultra-estruturado adotado pelo [[god-of-prompt]]:
- ROLE: define persona/especialidade do modelo
- TASK: objetivo claro em uma frase
- STEPS: sequência numerada de ações
- RULES: constraints explícitas (o que proibir)
- OUTPUT: formato exato esperado
→ [[2026-03-22_redesenho-carreira-tim-ferriss]], [[2026-04-16_wealth-protocol-naval]]

### Prompts sequenciais encadeados
4 prompts em sequência no mesmo chat, cada um dependendo do anterior:
- Prompt 1 identifica o que vender → Prompt 2 encontra mentor → Prompt 3 cria plano → Bônus corta o plano
→ [[2026-04-17_prompts-renda-rapida]]

### Prompts de análise estratégica de negócios
7 prompts com saída ultra-estruturada (tabelas, seções nomeadas, limite de palavras) para análise de mercado, priorização de problemas e escalonamento:
→ [[2026-04-01_claude-fundador-startup-7-prompts]], [[2026-04-20_claude-ceo-7-prompts]]

## Fontes

- [[2026-03-19_leads-infinitos-cloudcode]]
- [[2026-04-11_transformacao-linkedin-ia]]
- [[2026-04-18_7-hacks-tokens-claude]]
- [[2026-03-22_redesenho-carreira-tim-ferriss]]
- [[2026-04-16_wealth-protocol-naval]]
- [[2026-04-17_prompts-renda-rapida]]
- [[2026-04-01_claude-fundador-startup-7-prompts]]
- [[2026-04-20_claude-ceo-7-prompts]]
- [[2026-03-24_aprender-com-claude-6-prompts]]
- [[2026-03-13_estrutura-de-prompt-6-partes]]
