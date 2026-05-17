---
title: "Finanças com IA"
type: concept
tags: [finanças-com-ia, investimentos, análise-financeira, prompt-engineering, llm, trading]
source_count: 6
last_updated: 2026-05-17
---

# Finanças com IA

> **Fontes:** 1 | **Domínio:** Aplicação de LLMs em análise financeira e de investimentos

## Definição

Uso de LLMs — via técnicas de prompt engineering — para executar análises financeiras de nível institucional, substituindo ou complementando dicas de gurus e relatórios de casas de investimento tradicionais.

## Abordagem documentada: Instituição como ROLE

A técnica central é usar o nome de uma instituição financeira de elite como ROLE no prompt. O modelo já carrega as metodologias publicadas por essas casas (relatórios, whitepapers, livros, entrevistas) como conhecimento semântico — nomear a instituição convoca o framework correspondente sem precisar descrevê-lo.

| Instituição (ROLE) | Análise ativada | Artefato de saída |
|---|---|---|
| Goldman Sachs | Stock Screener multi-critério | Relatório profissional de stock picking |
| Morgan Stanley | Valuation por DCF (M&A style) | Valuation memo com tabelas |
| Bridgewater | Risk management e stress test | Risk management report com heat map |
| JPMorgan | Pre-earnings brief (equity research) | Pre-earnings brief com resumo executivo |
| BlackRock | Portfólio multi-asset com policy statement | Documento de política de investimento |
| Citadel | Análise técnica quantitativa | Technical analysis report card |
| Harvard Endowment | Carteira de dividendos com DRIP | Dividend portfolio blueprint |
| Bain | Análise competitiva setorial | Bain-style strategy deck summary |

## Princípio subjacente

O modelo tem memória semântica das metodologias publicadas por essas instituições. Usar o nome como ROLE é uma forma compacta de convocar esse conhecimento acumulado sem precisar descrever o método — o mesmo mecanismo que faz "MECE" ou "Steelman" funcionarem como ativadores semânticos em [[prompt-engineering]].

## Conexão com padrões gerais de prompt engineering

Confirma e estende o padrão ROLE/TASK/STEPS/RULES/OUTPUT documentado em [[prompt-engineering]]: em finanças, a escolha do ROLE (instituição ou gestor) é especialmente poderosa porque as metodologias de análise financeira são bem codificadas e amplamente documentadas publicamente. Difere do padrão de *pessoas* (Paul Graham, Tim Ferriss, Naval Ravikant) — aqui a autoridade é a firma, não o indivíduo.

## Segundo ângulo documentado: ChatGPT para construção de riqueza individual

@Derek Gray publica carousel sobre uso de ChatGPT para construção de riqueza pessoal ("Are you using ChatGPT to build wealth?"). Contraste com a abordagem da Faria Lima Elevator:

| Dimensão | Faria Lima Elevator | Derek Gray |
|----------|--------------------|-----------:|
| Foco | Análise institucional (portfólio, valuation, risk) | Construção de riqueza pessoal |
| Ferramenta | ChatGPT / Claude (qualquer LLM) | ChatGPT |
| Público-alvo | Investidor sofisticado | Público geral |
| Conteúdo no wiki | Completo (8 prompts detalhados) | Parcial (apenas título) |

> **Nota:** O caption menciona "ChatGPT 5.5" — modelo inexistente até 2026-04-28. Possível clickbait ou erro do criador.

## Terceira abordagem: Pipeline de screening sequencial para seleção de ações

@Bert (No-Chase Swing Trading for 9-5s) documenta um pipeline de 3 prompts para encontrar e selecionar ações em menos de 5 minutos — diferente das abordagens anteriores por focar em *seleção eficiente de candidatos* antes de qualquer análise aprofundada.

| Prompt | Entrada | Saída |
|--------|---------|-------|
| #1 — Construtor de universo | Tema de mercado (ex: IA, energia, semis) | Lista de 25 ações relacionadas ao tema |
| #2 — Ranqueador | Lista de 25 ações | Ranking por qualidade do negócio + desconto de preço |
| #3 — Deep dive | Top 3 ranqueados | Análise completa: pontos fortes, por que está barata, catalisador, riscos |

**Limitação explicitamente reconhecida:** IA não é eficaz no *timing* de entrada — essa etapa exige leitura de gráfico + análise técnica humana. A combinação IA (triagem fundamentalista) + chart reading (timing) é o diferencial do método.

**Compatível com Claude, ChatGPT ou Gemini.**

Fonte: [[2026-04-30_bert-swing-trading-ia]] | [[bert-no-chase]]

## Padrão estrutural comparativo entre as três abordagens

| Abordagem | Técnica central | Público | Limitações reconhecidas |
|-----------|-----------------|---------|------------------------|
| Institucional (ROLE) | Nomear instituição → convoca metodologia publicada | Investidor sofisticado | Nenhuma mencionada |
| Riqueza individual | ChatGPT para construção de patrimônio | Público geral | Parcial (conteúdo incompleto) |
| Screening sequencial | Pipeline funil (tema → 25 → top 3 + deep dive) | Trabalhador CLT / swing trader | Timing de entrada permanece humano |

## Quarto ângulo documentado: Análise DIY de ações com template estruturado

[[ai-fied]] publica o "Analyze Any Stock" — prompt de analista financeiro genérico (não uma instituição específica) com estrutura ROLE/TASK/STEPS/RULES/OUTPUT completa:

| Seção | Conteúdo |
|-------|---------|
| ROLE | Analista financeiro para análise completa: fundamentos, valuation, entrada e saída |
| TASK | Analisar ação-alvo com recomendação compra/hold/venda e metas de preço |
| OUTPUT | Modelo de negócios → Saúde financeira → Moat → Valuation → Bear case → Bull case → Recomendação |

**Distinção vs. abordagens anteriores:**
- Vs. [[faria-lima-elevator]]: lá o ROLE é uma *instituição* (Goldman Sachs, BlackRock) — convoca metodologia publicada específica. Aqui é um "analista financeiro" genérico com template explícito
- Vs. [[bert-no-chase]]: lá o foco é *triagem eficiente* (tema → 25 candidatos → top 3). Aqui é análise completa de uma ação já selecionada
- Vs. [[derek-gray]]: lá o foco é *construção de riqueza pessoal*. Aqui é análise técnica de ação específica

**Primeira menção de planejamento fiscal no wiki**: o Prompt 5 do mesmo carousel documenta um "Tax Strategist" — checklist de deduções + documentos + erros comuns + cenários fiscais + comparação CPA vs. software. Abre espaço para expansão do domínio "finanças pessoais" além de análise de investimentos.

Fonte: [[2026-05-08_ai-fied-munger-5-prompts]] | [[ai-fied]]

## Padrão estrutural comparativo entre as quatro abordagens

| Abordagem | Técnica central | Público | Limitações reconhecidas |
|-----------|-----------------|---------|------------------------|
| Institucional (ROLE) | Nomear instituição → convoca metodologia publicada | Investidor sofisticado | Nenhuma mencionada |
| Riqueza individual | ChatGPT para construção de patrimônio | Público geral | Parcial (conteúdo incompleto) |
| Screening sequencial | Pipeline funil (tema → 25 → top 3 + deep dive) | Trabalhador CLT / swing trader | Timing de entrada permanece humano |
| DIY estruturado | Template explícito com analista genérico | Qualquer usuário | Finaliza com disclaimer "não é recomendação financeira" |

## Quinto ângulo documentado: Pipeline sequencial completo de análise institucional

@Artificial Intelligence l Business (@thewizeai) publica 10 prompts para replicar o raciocínio de analistas de Wall Street com Claude — alternativa gratuita ao Bloomberg Terminal ($24.000/ano).

**Diferença fundamental em relação às abordagens anteriores:** não é um único prompt com ROLE institucional (vs. [[faria-lima-elevator]]), nem triagem em funil (vs. [[bert-no-chase]]), nem template genérico de analista (vs. [[ai-fied]]). É um *pipeline sequencial completo* onde a ordem dos prompts é parte da metodologia.

| # | Prompt | Função no pipeline |
|---|--------|--------------------|
| 1 | Institutional Kickoff Report | Base: modelo de negócio, motores de receita, moat, riscos, gestão, 3 bulls + 3 bears |
| 2 | Quarterly Results Analysis | Camada: earnings breakdown — melhorou/piorou/gestão enfatiza/evita/red flags/KPIs próximo tri |
| 3 | Bull vs Bear Debate | Posição: caso otimista vs. pessimista; qual lado vence *agora* |
| 4 | Forensic Accounting Analysis | Auditoria: qualidade de receitas, cash flow, diluição, stock-based comp, contabilidade agressiva, red flags antes de comprar |
| 5 | Honest Valuation Framework | Preço: P/E, EV/EBITDA, Price/Sales, FCF yield, DCF — barato/justo/caro sem fingir precisão |
| 6 | Company Comparison | Alternativa: head-to-head A vs. B em 10 critérios; qual segurar 5 anos |
| 7 | Investor Summary Sheet | Síntese: 1 página a partir de filings/transcript — o que observar no próximo relatório |
| 8 | Stress Test of Investment Thesis | Risco: 3 cenários (bull/base/bear) com estimativas de receita, margem, sentimento, variação de preço e *probabilidade* |
| 9 | Big Business vs Big Stock | Qualidade: o negócio é grande? A ação também? — classificação em 4 quadrantes |

**Princípio-chave:** os prompts devem ser usados *em sequência*, não em isolamento. "Start with the Kickoff Report to build your foundation, then layer on the earnings analysis, valuation, and risk assessment."

**Novidades em relação ao domínio até então documentado:**
- **Forensic Accounting** como camada de análise — qualidade contábil, stock-based compensation, discrepâncias reportado vs. real. Inédito no wiki de finanças
- **Bull vs Bear Debate como artefato forçado** — não análise neutra, mas posição explícita sobre qual tese vence agora
- **Stress test com probabilidades** — os três cenários exigem atribuição numérica de probabilidade, não apenas descrição qualitativa
- **Sequência como metodologia** — insight estrutural: a ordem dos prompts replica o *processo* de raciocínio institucional

Fonte: [[2026-05-01_artificial-intelligence-business-analise-acoes]] | [[artificial-intelligence-business]]

## Padrão estrutural comparativo entre as cinco abordagens

| Abordagem | Técnica central | Público | Limitações reconhecidas |
|-----------|-----------------|---------|------------------------|
| Institucional (ROLE) | Nomear instituição → convoca metodologia publicada | Investidor sofisticado | Nenhuma mencionada |
| Riqueza individual | ChatGPT para construção de patrimônio | Público geral | Parcial (conteúdo incompleto) |
| Screening sequencial | Pipeline funil (tema → 25 → top 3 + deep dive) | Trabalhador CLT / swing trader | Timing de entrada permanece humano |
| DIY estruturado | Template explícito com analista genérico | Qualquer usuário | Finaliza com disclaimer "não é recomendação financeira" |
| Pipeline completo sequencial | 10 prompts em sequência replicando workflow institucional | Investidor individual ambicioso | Não substitui dado proprietário (Bloomberg) |

## Sexto ângulo documentado: Claude como gestor de portfólio autônomo com dinheiro real

[[roman-khaneichuk]] apresenta o primeiro caso no wiki onde Claude *executa trades* com capital real ($50.000) sem supervisão humana — cruzamento sem precedente entre análise financeira agêntica e execução efetiva.

**O pipeline de 5 etapas:**

| Etapa | O que acontece | Output |
|-------|---------------|--------|
| 1 — Triagem | Filtra 1.000 ações para candidatas válidas | Lista filtrada |
| 2 — Debate | 30 agentes IA em paralelo: 15 bulls vs 15 bears por ativo | Debate estruturado |
| 3 — Price targets | Price targets com peso de probabilidade por cenário | Alvo ponderado (bull/base/bear) |
| 4 — Portfólio | Constrói carteira de 15 ações com alocação por posição | Pesos definidos |
| 5 — Rebalanceamento | Rebalanceia automaticamente na corretora do usuário | Trades executados |

**[[autopilot]] como camada de distribuição**: qualquer usuário pode espelhar automaticamente os trades do Claude em sua própria conta de corretora — democratizando acesso a gestão agêntica sem necessidade de código ou análise própria.

**Distinção em relação às abordagens anteriores:**
- Vs. [[faria-lima-elevator]]: lá, o usuário faz a análise com prompts; aqui, o Claude *decide e executa* autonomamente
- Vs. [[bert-no-chase]]: lá, a IA faz triagem e o humano decide quando entrar; aqui, não há decisão humana no loop
- Vs. [[artificial-intelligence-business]]: lá, o pipeline gera análise para o usuário agir; aqui, o Claude age diretamente
- **Novidade estrutural**: primeiro registro do wiki de um **agente de IA com skin in the game real** — dinheiro real, execução real, sem humano no loop

**Confirmação do padrão "debate como mecanismo de decisão"**: o debate bull vs bear com 30 agentes é a mesma lógica do [[tradingagents]] (55.700 stars, open-source) e do Prompt 3 de [[artificial-intelligence-business]] ("Bull vs Bear Debate"). Três fontes independentes convergem no mesmo padrão de decisão — debate estruturado entre perspectivas opostas produz decisões mais robustas que um único agente.

> **Caveat editorial**: o conteúdo é uma parceria paga com @autopilot. Os resultados passados não garantem resultados futuros. Investimentos carregam risco de perda de principal.

Fonte: [[2026-04-14_roman-khaneichuk-claude-portfolio]] | [[roman-khaneichuk]]

## Padrão estrutural comparativo entre as seis abordagens

| Abordagem | Técnica central | Público | Autonomia da IA |
|-----------|-----------------|---------|----------------|
| Institucional (ROLE) | Nomear instituição → convoca metodologia publicada | Investidor sofisticado | Nenhuma — IA analisa, humano decide |
| Riqueza individual | ChatGPT para construção de patrimônio | Público geral | Nenhuma — parcial (conteúdo incompleto) |
| Screening sequencial | Pipeline funil (tema → 25 → top 3 + deep dive) | Trabalhador CLT / swing trader | Parcial — IA triagem, humano timing |
| DIY estruturado | Template explícito com analista genérico | Qualquer usuário | Nenhuma — análise, humano decide |
| Pipeline completo sequencial | 10 prompts em sequência replicando workflow institucional | Investidor individual ambicioso | Nenhuma — análise, humano decide |
| **Gestor autônomo (dinheiro real)** | **30 agentes debate → portfólio → execução automática** | **Qualquer usuário via Autopilot** | **Total — Claude decide e executa** |

## Estado atual do wiki

Domínio com 6 fontes. Seis ângulos distintos: análise financeira institucional via ROLE (Faria Lima Elevator), construção de riqueza individual via ChatGPT (Derek Gray — parcial), pipeline de screening para seleção de ações (Bert), análise DIY com template estruturado (AI-Fied), pipeline sequencial completo de análise institucional (Artificial Intelligence l Business / @thewizeai) e **gestor de portfólio autônomo com dinheiro real e multi-agent debate** (Roman Khaneichuk via Autopilot).

## Fontes

- [[2026-04-26_faria-lima-elevator-ia-investimentos]] — 8 prompts com 8 instituições distintas, cobrindo o ciclo completo de análise financeira
- [[2026-04-28_derek-gray-chatgpt-wealth]] — carousel sobre ChatGPT para construção de riqueza (ingestão parcial)
- [[2026-04-30_bert-swing-trading-ia]] — pipeline de 3 prompts para screening e seleção de ações em 5 minutos
- [[2026-05-08_ai-fied-munger-5-prompts]] — prompt DIY de análise de ações com template ROLE/TASK/STEPS/RULES/OUTPUT + primeiro prompt de planejamento fiscal do wiki
- [[2026-05-01_artificial-intelligence-business-analise-acoes]] — 10 prompts sequenciais para análise institucional completa: Kickoff → Earnings → Bull/Bear → Forensic → Valuation → Comparison → Summary → Stress Test → Quality
- [[2026-04-14_roman-khaneichuk-claude-portfolio]] — Claude como gestor autônomo: $50K, 30 agentes bull/bear, portfólio de 15 ações, execução automática via Autopilot (sem supervisão humana)
