---
title: "Prompt Engineering"
type: concept
tags: [prompt-engineering, prompts, llm, claude, técnicas]
source_count: 19
last_updated: 2026-04-24
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

### Prompts de execução de modelo de negócio
Cada prompt orquestra um pipeline completo (conteúdo → distribuição → automação → monetização) em uma única chamada: ideia → título → estrutura → estratégia de venda → integrações.
→ [[2026-04-07_5-negocios-automatizados-ia]]

### Palavras-gatilho (ativadores semânticos)
Uma única palavra anexada ao prompt ativa um framework que o modelo já conhece, mudando o pipeline de resposta antes da geração. Exemplos documentados: **MECE**, **Confidence Level**, **5 Whys**, **Invert**, **ELI5**, **Artefato**. Distinto dos prompts estruturados — aqui o poder está em uma palavra reconhecível que carrega toda a semântica do framework.
→ [[2026-04-08_gatilhos-cognitivos-claude]]

### Skills como palavras-gatilho formalizadas
[[claude-skills]] são a evolução industrial da palavra-gatilho: cada skill tem nome, frases de ativação e `Search Tag`, distribuídas em marketplaces como [[smithery]] (128k+ skills). Feature Forge, Spec Miner, The Fool, Architecture Designer, API Designer e Microservice Architect são exemplos catalogados.
→ [[2026-04-07_claude-skills-product-managers]]

### Prompts parametrizados encadeados para pipeline produto-marketing
7 prompts em sequência onde cada um alimenta o seguinte: ideia → build → bio → carrossel → caption → reel → DM. Parâmetros padronizados (`[target audience]`, `[niche]`, `[product name]`, `[transformation]`) garantem reuso entre projetos.
→ [[2026-04-17_mini-web-app-claude]]

### Comandos como interface de instrução estruturada
Comandos built-in do Claude Code funcionam como prompts de sistema permanentes ou contextuais:
- `/plan` — força mapeamento completo (etapas, arquivos, decisões) antes de qualquer código → elimina retrabalho por desalinhamento
- `#` — adiciona regra permanente ao rulebook em 3 segundos, sem editar CLAUDE.md manualmente
- `/review` — prompt de QA profundo embutido: audita todo o codebase, não só o arquivo aberto
→ [[2026-04-22_sal-shirgaleev-5-comandos-claude]]

### Adaptive Thinking via Prompts
Com Opus 4.7, o extended thinking não tem mais toggle de UI — é controlado exclusivamente por linguagem natural no prompt:
- Tarefa complexa / desafiadora: `"think carefully step by step"`
- Tarefa simples / trivial: `"prioritize responding quickly rather than thinking deeply"`

Combinado com `/effort`, o usuário controla dois eixos independentes:
- **Esforço total na tarefa** → `/effort` (low → max)
- **Profundidade de raciocínio por microtarefa** → instrução de thinking no prompt

→ [[2026-04-18_alex-finn-dicas-claude-code]]

### Frontload Information
Opus 4.7 é superior na capacidade de seguir instruções longas e complexas fornecidas de uma vez só. Melhor prática: enviar todas as especificações, restrições e requisitos em um único prompt inicial em vez de incrementalmente. Em Auto Mode, o modelo executa o plano completo sem interrupções.
→ [[2026-04-18_alex-finn-dicas-claude-code]]

### Diagnóstico pelo ângulo do usuário-alvo (Recruiter Perspective)
Em vez de pedir ao LLM para "melhorar" um texto, solicitar que ele simule o julgamento de quem vai ler o texto (e.g., recrutador, cliente, investidor) antes de qualquer reescrita. Sequência: diagnóstico honesto → reescrita. Evita otimizar na direção errada.
→ [[2026-04-16_sanskaar-singh-linkedin-prompts]] | [[sanskaar-singh]]

### Entrega em espectro de versões
Para decisões com componente criativo (headline, copy, pitch), pedir N versões ao longo de um espectro explícito (e.g., "de conservador a ousado"). Devolve a decisão criativa final ao usuário, que escolhe o ponto do espectro que prefere.
→ [[2026-04-16_sanskaar-singh-linkedin-prompts]]

### Frameworks de raciocínio como ativadores semânticos (Mental Models)
Nomes de frameworks de raciocínio já conhecidos pelo modelo funcionam como ativadores de modo — uma palavra muda o pipeline de resposta sem precisar explicar o método. Seis documentados:

| Palavra | Efeito | Quando usar |
|---------|--------|-------------|
| **Steelman** | Constrói o argumento mais sólido possível em favor da ideia | Testar decisão antes de executar |
| **Rubber Duck** | Faz perguntas para o usuário descobrir a resposta sozinho | Pensar em voz alta, não receber solução pronta |
| **SCAMPER** | Gera variações sistemáticas (Substitute, Combine, Adapt, Modify, Put to other uses, Eliminate, Reverse) | Travado, precisa de ângulos novos |
| **Force Multiplier** | Identifica a alavanca de maior impacto entre todas as iniciativas | Muitas frentes abertas, pouco foco |
| **Red Team** | Ataca a ideia buscando todas as vulnerabilidades, sem filtro | Apresentar plano para quem vai tentar destruí-lo |
| **Devil's Advocate** | Assume posição contrária à premissa definida com argumentos reais | Testar crença específica (cirúrgico, vs. Red Team que é total) |

Steelman e Red Team são opostos complementares: usados em sequência cobrem todo o espectro de revisão crítica.
→ [[2026-04-22_castilho-6-palavras-claude]] | [[castilho]]

### Skills como pipeline de conteúdo parametrizado (Founder's stack)
[[paras-madan]] documenta 3 skills que codificam pipelines completos de produção de conteúdo e análise:
- **LinkedIn Post Generator:** qualquer input (blog, PR, frase) → detecção automática de hook + arco narrativo + formato (Founder/Ship, Insight, Product Launch) → post publicável
- **Reddit ICP Monitor:** prompt permanente de escuta → score 1-5 por post → resposta útil (score ≥ 4) sem autopromoção
- **Google Trends SEO:** query de tendência → breakout keyword → outline SEO completo

Diferencial vs. prompts únicos: são skills instaláveis, não prompts que o usuário mantém — o pipeline fica encapsulado na skill.
→ [[2026-04-18_paras-madan-top5-skills-founders]]

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
- [[2026-04-07_5-negocios-automatizados-ia]]
- [[2026-04-08_gatilhos-cognitivos-claude]]
- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-17_mini-web-app-claude]]
- [[2026-04-22_sal-shirgaleev-5-comandos-claude]]
- [[2026-04-18_alex-finn-dicas-claude-code]]
- [[2026-04-16_sanskaar-singh-linkedin-prompts]]
- [[2026-04-22_castilho-6-palavras-claude]]
