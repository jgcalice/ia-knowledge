---
title: "Overview — IA Knowledge Base"
type: overview
last_updated: 2026-05-01
source_count: 60

---

# Overview — IA Knowledge Base

> Wiki iniciado em 2026-04-21 | 60 fontes ingeridas | Domínio: IA Aplicada a Negócios, Carreira, Gestão, Produto, **Adoção Empresarial**, **Finanças** e **Bem-estar**

## Tese atual

O conteúdo de IA consumido até agora orbita em torno de **cinco domínios práticos**:

1. **Como gerar mais leads com menos esforço** — usando LLMs + scraping de Google Maps e APIs
2. **Como usar Claude de forma mais eficiente** — reduzindo consumo de tokens e escolhendo ferramentas certas
3. **Como acelerar carreira e aumentar renda** — LinkedIn, busca de emprego automatizada, certificações, redesenho estratégico
4. **Como construir negócios com IA** — estratégia de mercado, branding, SEO e automação de processos
5. **Como organizações adotam IA em escala** — playbook empresarial, mudança organizacional, escolha de modelo, dado como moat (NOVO via [[stanford-digital-economy-lab]])

---

## Clusters de conhecimento

### Cluster 1: Geração de Leads com IA
**Conceito central:** [[geração-de-leads-com-ia]]

Três métodos documentados, padrão similar, ferramentas diferentes:
- **Método 1**: [[claude-code]] + [[api-file]] → [[google-maps]] → leads enriquecidos ([[lucas-garcia-pit]])
- **Método 2**: [[claude-code]] + [[apify]] → [[google-maps]] → leads organizados ([[hudson-brendon]])
- **Método 3**: Skill "lista de alto valor" + API → leads com dados completos incluindo LinkedIn ([[flavio-rafael]])
- **Método 4**: [[vibe-prospecting]] (Conector Claude.ai web) + prompt → leads por nicho/cargo/cidade, gratuito e sem CLI ([[eduardo-santos]])

- **Método 5**: Prompts + ChatGPT/Claude → identificar negócios #6–20 no Maps → prospecção + entrega de serviço GMB ($500–$1K/mês retainer) ([[derek-gray]])

**Síntese**: [[comparação-métodos-leads]]

---

### Cluster 2: Otimização de Tokens
**Conceito central:** [[otimização-de-tokens]]

Três fontes convergem no mesmo problema:
- **Documentos**: usar [[markitdown]] ou modelo intermediário antes de enviar PDFs ([[rafael-brandao]], [[evolving-ai]])
- **Prompts**: ser conciso, proibir linguagem de preenchimento ([[evolving-ai]])
- **Modelo**: escolher Haiku/Sonnet/Opus conforme a tarefa ([[evolving-ai]])
- **Contexto**: compactar sessões longas com Compact Skill ([[evolving-ai]])
- **Grafo de conhecimento**: [[graphify]] mapeia o workspace e reduz tokens em 71,5x → 20.000 → 280/sessão ([[marc-cleroux]])
- **Session handoff**: custo é exponencial (98,5% dos tokens = rereading); context rot degrada acurácia de 92%→78%; sessões devem ser reiniciadas a ~12% via handoff estruturado ([[nate-herk]])

---

### Cluster 3: Carreira e LinkedIn com IA
**Conceito central:** [[carreira-com-ia]]

Sistema completo documentado — da visibilidade à estratégia de longo prazo:

| Camada | O que faz | Fonte |
|--------|-----------|-------|
| Visibilidade (LinkedIn) — Abordagem 1 | 5 prompts por formato/constraint para reescrever headline, about, skills, experiência | [[bruno-souza]] |
| Visibilidade (LinkedIn) — Abordagem 2 | Diagnóstico recruiter-first + 5 versões em espectro + keywords por JD | [[sanskaar-singh]] |
| Busca automatizada v1 | Career Ops terminal: 700+ vagas avaliadas, currículo ATS por vaga | [[career-ops]] |
| Busca automatizada v2 | Career Ops plugin: LinkedIn scraping → scoring → ATS → STAR → outreach → negociação | [[arshman-khalid]] |
| Candidaturas personalizadas (sem código) | JD → Claude extrai skills → reescreve currículo → cover letter; caso: 6 entrevistas/7 dias | [[coding-ai-fullstack]] |
| Redesenho estratégico | 4 prompts Tim Ferriss: vantagem injusta, DEAL, freedom ratio, 10 anos | [[god-of-prompt]] |
| Monetização imediata | 4 prompts para ganhar $1k em 30 dias com skills existentes | [[sabrina-ramonov]] |
| Monetização com templates | 5 prompts-template `[insert X]`: freelance do cargo atual, plano 30 dias $10K, desafio 7 dias, day rate $1K/dia, serviço $10K/mês | [[laura-anderson]] |
| Certificação formal | Claude Certified Architect (grátis, proctored, valorizado pela Deloitte) | [[bashiri]] |
| Filosofia de riqueza | 6 prompts Naval Ravikant — texto completo de 5 prompts nomeados (Excavator, Auditor, Brand Architect, Productize, Judgment); 3ª variação confirmando o framework | [[god-of-prompt]] · [[simplifying-ai]] · [[ai-fied]] |

---

### Cluster 7: Segurança Digital com IA
**Conceito central:** [[segurança-com-ia]]

- **Dimensão 1 — Desenvolvimento preventivo**: 5 fundamentos design-time para apps com Claude Code: API keys no servidor, RLS no Supabase, lógica sensível no back-end, rate limiting e webhooks assinados ([[lucas-garcia-pit]])
- **Dimensão 2 — Privacidade/OSINT**: 14 ferramentas documentadas em 3 fontes BR: ZoomEye, HIBP, Namecheck, Pic2Map, EPA, Exploding Database ([[gustavo-melo]] post 1) + Sherlock, Maltego, SpiderFoot, Shodan, Google Dorking ([[sidney-rodrigo]]) + Webmail e My7 — investigação de pessoa física ([[gustavo-melo]] post 2)
- **Dimensão 3 — Empresarial**: Shadow AI (70-80% usam ferramentas não aprovadas), segurança como enabler front-loaded, pipeline PII scrubbing como moat ([[stanford-digital-economy-lab]])
- **Dimensão 4 — Vibecoding pré-deploy**: prompt de 6 blocos que instrui o agente a auditar o codebase como engenheiro sênior de segurança ($15k em valor); conceito de **attack chains** (3 vulns "low" = 1 "critical") ([[artificial-intelligence-business]] / @thewizeai) — NOVO
- **Tese unificada**: aceleração (LLMs no dev, internet nos dados, mandato corporativo) cria exposições invisíveis que exigem intenção ativa para serem corrigidas — em 4 escalas diferentes

---

### Cluster 4: Negócios e Estratégia com IA
**Conceito central:** [[estratégia-de-negócios-com-ia]]

- 5 prompts para validar idea de startup com framework Paul Graham: pressure test → problema real → concorrentes → primeiros 10 clientes → MVP em 2 semanas ([[harry]])
- 7 prompts para análise de mercado, oferta e escalonamento ([[evolving-ai]], [[business-bulls]])
- Playbook "low-hanging fruit": Reddit hand-to-hand combat (primeiros 100 clientes) → Programmatic SEO ($3M+ ARR, 150K+ usuários, $250K/mês) — ([[starter-story]], case Joseph)
- Branding completo em 2h com 120+ agentes ([[rafael-brandao]])
- SEO na primeira página do Google com 3 arquivos de texto ([[brycen-wood]])
- 5 modelos nativos de IA (eBook, YouTube narrado, newsletter, curso online, agente WhatsApp como AIaaS) ([[bruno-wambier]])
- Mini web app focado + Instagram como canal único ([[luna-vega]])
- AI Agency (Dan Martell, Liam Ottley) — agência automatiza outras empresas ([[paul-hilse]])
- Stack de 5 skills open-source para founder solo: Meta Ads + Position Me + LinkedIn Post Generator + Reddit ICP Monitor + Google Trends SEO ([[paras-madan]])
- GMB Optimization Agency: 8 prompts para prospectar negócios #6–20 no Maps e entregar SEO local como serviço — retainers $500–$1K/mês ([[derek-gray]])
- AI Sales Agency: 3 agentes (AI SDR + Sales Call Analyzer + AI Consultant) cobrem todo o funil — do outreach ao contrato fechado — sem código. $3K/cliente vs $30–50K economizados/ano ([[jordan-lee]])
- One-Person Business (Dan Koe model): 5 prompts — ideia → oferta-transformação → sistema de conteúdo → vendas autônomas → escalar sem contratar. Case: $6M, 0 funcionários, 4h/dia ([[ai-fied]] via [[dan-koe]])

---

### Cluster 5: Aprendizado e Recursos sobre IA
**Conceito central:** [[aprendizado-com-ia]]

- 6 prompts para Claude funcionar como tutor pessoal ([[evolving-ai]])
- 5 cursos gratuitos no YouTube para dominar Claude Code ([[usama-akram]])
- 7 YouTubers com ângulos distintos (business, no-code, estratégia, ferramentas, escala, economia, AI agency) ([[paul-hilse]])

---

### Cluster 6: Produto com IA (emergente)
**Conceito central:** [[claude-skills]]

- 6 Claude Skills para Product Managers: Feature Forge, Spec Miner, The Fool, Architecture Designer, API Designer, Microservice Architect ([[aashish-pahwa]])
- Marketplace [[smithery]] com 128k+ skills — ecossistema já em escala
- Skills formalizam o padrão de "palavra-gatilho" iniciado por [[adriano-couto]]

---

### Cluster 8: Adoção Empresarial de IA (NOVO via Stanford)
**Conceito central:** [[adoção-empresarial-de-ia]]

Primeira fonte empírica em larga escala no wiki: [[stanford-digital-economy-lab]] estudou 51 implementações bem-sucedidas em 41 organizações, 7 países, 5 regiões ([[2026-04-01_enterprise-ai-playbook-stanford]]).

| Achado | Dado |
|---|---|
| Custos invisíveis | **77%** dos desafios são change management, dado, processo (não tecnologia) |
| Falha como pré-requisito | **61%** dos sucessos tiveram falha anterior; 100% dos sponsors continuaram através da falha |
| Sponsorship | Active Steering em **58%**, Strategic Integration (OKR + bônus) em **29%** — único caminho para transformação organization-wide |
| Resistência | Staff functions (Legal/HR/Risk/Compliance) em **35%** > end-users **23%** |
| Headcount | **45%** reduzem; 55% redeployment, hiring avoided ou sem mudança |
| Agentic | **20%** dos casos; **71%** ganho mediano vs 40% high-automation |
| Dado | **47%** explicitamente descrevem dado proprietário como moat |
| Modelo | **42%** commodity (rotineiras 71% commodity; advanced 18%) |
| Segurança | Em todos os 12 casos analisados: bloqueia inicialmente, **habilita depois** |

Sub-conceitos derivados:
- [[mudança-organizacional-com-ia]] — change management como 35% da resistência
- [[dados-como-moat]] — 47% citam dado proprietário; "save everything"
- [[escolha-de-modelo-fundacional]] — 42% commodity; multi-model + abstraction layer
- [[produtividade-e-emprego-com-ia]] — 45% reduzem; canários: workers 22-25 expostos -16%

Síntese: [[instagram-vs-pesquisa-empirica-ia]] — comparação dos dois ângulos do wiki

---

### Cluster 9: Finanças e Investimentos com IA (NOVO)
**Conceito central:** [[finanças-com-ia]]

Primeiro domínio de finanças no wiki — técnica de usar instituições financeiras de elite como ROLE em prompts de análise:

| # | ROLE | Análise |
|---|---|---|
| 1 | Goldman Sachs | Stock Screener multi-critério (P/L, crescimento, bull/bear, nota de risco) |
| 2 | Morgan Stanley | DCF completo com WACC, valor terminal e tabela de sensibilidade |
| 3 | Bridgewater | Risk report com stress test, tail risk e hedges recomendados |
| 4 | JPMorgan | Pre-earnings brief com histórico beat/miss e movimento de opções |
| 5 | BlackRock | Portfólio multi-asset com policy statement e regras de rebalanceamento |
| 6 | Citadel | Análise técnica quantitativa (MMAs, RSI, MACD, Fibonacci, plano de trade) |
| 7 | Harvard Endowment | Carteira de dividendos com simulação DRIP 10 anos |
| 8 | Bain | Análise competitiva setorial com SWOT das 2 líderes e catalisadores 12 meses |

Fonte: ([[faria-lima-elevator]])

---

## Mapa de entidades

**Ferramentas e plataformas**: [[claude-code]] · [[claude-skills]] · [[smithery]] · [[apify]] · [[api-file]] · [[markitdown]] · [[linkedin]] · [[google-maps]] · [[career-ops]] · [[graphify]] · [[obsidian]] · [[vibe-prospecting]] · [[simplifying-ai]] · [[context7]] · [[tradingagents]]

**Instituições acadêmicas**: [[stanford-digital-economy-lab]]

**Referências externas**: [[paul-graham]] · [[naval-ravikant]] · [[dan-koe]] · [[erik-brynjolfsson]] · [[alvin-wang-graylin]] · [[elisa-pereira]]

**Conceitos de segurança**: [[segurança-com-ia]]

**Pessoas (BR)**: [[lucas-garcia-pit]] · [[hudson-brendon]] · [[bruno-souza]] · [[rafael-brandao]] · [[flavio-rafael]] · [[rony-meisler]] · [[bruno-wambier]] · [[adriano-couto]] · [[eduardo-santos]] · [[castilho]] · [[gustavo-melo]] · [[sidney-rodrigo]] · [[faria-lima-elevator]]

**Pessoas (Internacional)**: [[evolving-ai]] · [[god-of-prompt]] · [[bashiri]] · [[sabrina-ramonov]] · [[ross-fledderjohn]] · [[michael-kocher]] · [[brandon-lew]] · [[usama-akram]] · [[brycen-wood]] · [[business-bulls]] · [[aashish-pahwa]] · [[luna-vega]] · [[paul-hilse]] · [[marc-cleroux]] · [[andrej-karpathy]] · [[alex-finn]] · [[nate-herk]] · [[pablo-in-public]] · [[sanskaar-singh]] · [[arshman-khalid]] · [[paras-madan]] · [[harry]] · [[yik-chan]] · [[ai-fied]] · [[ai-updater]] · [[manthan-patel]] · [[arising-ai]] · [[starter-story]] · [[coding-ai-fullstack]] · [[derek-gray]] · [[jordan-lee]]

**Referências de produto Anthropic**: [[boris-cherny]]

---

## Padrões emergentes

- **Claude como orquestrador**: em todas as fontes, Claude/Claude Code é o centro — não apenas chatbot, mas agente que integra ferramentas externas
- **Carreira com IA é tema central**: 7 das 21 fontes abordam diretamente carreira, LinkedIn ou renda — é o segundo maior cluster
- **Combinação de skills > skill isolada**: padrão recorrente em múltiplas fontes independentes
- **Ação antes de planejamento**: "stop planning, start selling" / "just go build it" — mensagem anti-procrastinação dominante
- **Tokens como recurso escasso**: quatro fontes abordam → preocupação consolidada; [[nate-herk]] documenta que custo é exponencial e que o 1M token window convida desperdício
- **Context rot como risco subestimado**: além de custo, longas sessões degradam *qualidade* — acurácia de recuperação cai 14pp de 256k→1M tokens ([[nate-herk]])
- **Conteúdo duplicado confirmado**: prompts de estratégia de negócios aparecem idênticos em [[evolving-ai]] e [[business-bulls]] — sinal de que são referência consolidada
- **Palavras-gatilho como novo padrão**: [[adriano-couto]] introduz MECE/5 Whys/Invert/ELI5/Artefato como ativadores semânticos — uma palavra muda o pipeline de resposta do Claude, sem precisar explicar o framework
- **Skills formalizam os gatilhos**: [[aashish-pahwa]] + [[smithery]] mostram ecossistema de ~128k Claude Skills — a palavra-gatilho artesanal virou pacote distribuível
- **Ecossistema de skills exige tooling próprio**: `find-skills` (Vercel Labs) é uma meta-skill que busca entre todas as outras por linguagem natural — sinal de que o ecossistema atingiu escala de descoberta ([[pablo-in-public]])
- **Mental Models como ativadores semânticos**: Steelman, Rubber Duck, SCAMPER, Force Multiplier, Red Team e Devil's Advocate funcionam como palavras-gatilho de segunda geração — nomes de frameworks de raciocínio que o modelo já conhece e executa com uma palavra ([[castilho]])
- **Arquétipos de negócio se multiplicando**: já mapeamos 7 — consultoria estratégica, infoprodutos nativos, mini web app + Instagram, AI Agency, stack de skills para founder solo, bootstrap SaaS + distribuição sequencial e GMB Optimization Agency ([[paras-madan]], [[derek-gray]]). Nenhum é "IA só como ferramenta" — todos são **produtos/serviços nascidos da IA**
- **Google Maps como mercado duplo**: [[derek-gray]] documenta o segundo papel do Maps no wiki — além de fonte de leads para prospecção B2B (métodos 1–4), o Maps é o *canal de entrega e prospecção simultânea* para agências de SEO local. Negócios rankeados #6–20 são o mercado-alvo; 8 prompts cobrem todo o ciclo operacional
- **Skills como equipe virtual distribuível**: [[paras-madan]] expande o padrão de [[aashish-pahwa]] (skills para PMs) para canais de crescimento — o founder substitui media buyer, CRO consultant, copywriter, community manager e SEO analyst com 5 skills open-source
- **Claude Code como agente autônomo**: Auto Mode + Frontload + Notificações mudam o paradigma de "babysitting" (aprovação constante) para "delegação real" — o agente trabalha horas sem supervisão ([[alex-finn]])
- **Segurança como ponto cego do desenvolvimento com IA**: Claude Code acelera tanto o desenvolvimento que devs pulam fundamentos clássicos de back-end (RLS, rate limit, server-side secrets) — [[lucas-garcia-pit]] documenta os 5 mais críticos
- **OSINT como alfabetização digital**: a internet expõe muito mais dados pessoais do que as pessoas percebem — duas fontes BR independentes documentam 12 ferramentas para auditar exposição: [[gustavo-melo]] (7 ferramentas para uso pessoal defensivo) e [[sidney-rodrigo]] (5 ferramentas do arsenal de analistas profissionais — Sherlock, Maltego, SpiderFoot, Shodan, Google Dorking). Convergência em duas categorias: scanners de dispositivos (ZoomEye ≈ Shodan) e Google Dorks (Exploding Database ≈ Google Dorking)
- **Validação como etapa anterior à estratégia**: o framework [[paul-graham]] (via [[harry]]) documenta a camada pré-estratégia — testar ideia antes de qualquer planejamento de mercado; complementa os 7 prompts de [[evolving-ai]] / [[business-bulls]] que começam depois que o produto existe
- **Claude tem dois modos de usuário documentados**: "usuário conversacional" (Daily Efficiency sem CLI, sem API — emails, PDFs, tone) e "usuário técnico" (Claude Code com CLAUDE.md, sub-agentes, slash commands); [[yik-chan]] é a primeira fonte a catalogar os 25 usos de nível básico de forma sistemática
- **Brand Voice Document em Projects como padrão de persistência de estilo**: salvar tom/palavras proibidas/regras de escrita no Projects elimina repetição de briefing — evolução da lógica do CLAUDE.md para contextos de conteúdo (não só código)
- **Wealth Protocol como template viral**: dois criadores distintos ([[god-of-prompt]] e [[simplifying-ai]]) publicam o mesmo "Wealth Protocol" baseado em [[naval-ravikant]] — sinal de que é um framework circulando como template na comunidade, não conteúdo original; a segunda fonte ([[2026-04-18_simplifying-ai-wealth-protocol-naval]]) revelou o texto completo dos 5 prompts nomeados
- **Tecnologia não é o gargalo (dado empírico)**: 51 cases empresariais bem-sucedidos confirmam que **77% dos desafios são não-técnicos** — change management, dado, processo. Para **42% dos casos o modelo é commodity**. A vantagem competitiva durável está na **camada de orquestração + dado proprietário**, não na escolha do LLM ([[stanford-digital-economy-lab]])
- **Custo invisível como ponto cego do Instagram**: nenhuma fonte de criadores enxerga que 80% do trabalho de IA empresarial é não-técnico (Legal, HR, Risk, Compliance, redesenho de processos). [[stanford-digital-economy-lab]] preenche essa lacuna com 51 cases — comparação completa em [[instagram-vs-pesquisa-empirica-ia]]
- **Claude Managed Agents como plataforma de infraestrutura**: a Anthropic lançou runtime hospedado para agentes com estado (Agent + Environment + Session + Events) — elimina setup manual de orquestração e oferece observabilidade nativa via Console; o caso de uso demonstrado (CSV → relatório HTML interativo) é o template canônico de agente de análise de dados ([[ai-updater]])
- **Shadow AI em escala industrial**: fabricante de semiconductors com 1.500-1.600 ferramentas IA não-aprovadas em uso simultâneo antes de plataforma oficial — primeira evidência empírica no wiki da magnitude do uso "informal" de IA dentro de empresas
- **Canários no mercado de trabalho**: workers 22-25 em ocupações expostas a IA já têm queda relativa de 16% em emprego (devs jovens: -20%) — caveat crítico ao otimismo dos criadores de Instagram sobre redeployment automático
- **Modelos chineses open-source dominando o stack agêntico**: Qwen, Kimi, Minimax, GLM = 4 dos top-5 no OpenRouter por volume de tokens em fev/2026, puxados por agentic workloads — invisível na conversa anglófona até agora
- **CLAUDE.md como sistema de autonomia, não só de configuração**: [[boris-cherny]] (Anthropic) documenta que o CLAUDE.md pode codificar meta-comportamentos de agente — plan mode obrigatório, sub-agentes para contexto limpo, ciclo de autoaperfeiçoamento, bug fixing autônomo e princípios Simplicity/No Laziness/Minimal Impact; complementa e fundamenta os hacks táticos de [[sal-shirgaleev]], [[alex-finn]] e [[nate-herk]]
- **Finanças como novo domínio do wiki**: [[faria-lima-elevator]] documenta o primeiro conteúdo de investimentos — técnica de usar nomes de instituições financeiras de elite (Goldman Sachs, Bridgewater, BlackRock) como ROLE em prompts. Estende o padrão ROLE/TASK/STEPS/RULES/OUTPUT de *pessoas* para *firmas*: o modelo carrega as metodologias publicadas por essas casas como conhecimento semântico, e nomeá-las é suficiente para convocar o framework completo sem descrever o método
- **Bem-estar como novo domínio do wiki**: [[arising-ai]] documenta o primeiro conteúdo de fitness — 7 prompts parametrizados substituem um personal trainer de $200/sessão. O padrão central é "inputs de anamnese → outputs de protocolo profissional": o LLM já internalizou décadas de literatura de fitness, e campos `[age]`, `[goal]`, `[equipment]` são suficientes para convocar um programa de nível profissional. A lógica escala para nutrição, planejamento financeiro pessoal e outros domínios de alto custo ([[bem-estar-com-ia]])
- **Reddit + Programmatic SEO como playbook replicável de distribuição**: [[starter-story]] confirma (case Joseph, $3M+ ARR) que a sequência "hand-to-hand combat no Reddit → programmatic SEO" é um caminho bootstrap provado. Complementa os dados do wiki sobre [[brycen-wood]] (SEO técnico) e [[paras-madan]] (Reddit ICP Monitor Skill): as três fontes convergem em Reddit e SEO programático como canais de menor resistência para SaaS
- **Busca de emprego com IA tem três níveis documentados**: (1) nível de entrada — Claude.ai direto, sem setup, currículo por vaga em minutos ([[coding-ai-fullstack]]); (2) nível intermediário — Career Ops terminal, 700+ vagas avaliadas em script ([[career-ops]]); (3) nível avançado — plugin + Apify LinkedIn, pipeline end-to-end até negociação salarial ([[arshman-khalid]]). O mesmo objetivo, três profundidades técnicas diferentes — o nível de entrada já entrega resultado concreto
- **Agent teams vs sub-agentes — distinção formalizada**: sub-agentes rodam em paralelo mas não se comunicam; agent teams compartilham task list, comunicam entre si e podem atribuir trabalho uns aos outros. Git worktrees complementam: isolam por branch (filesystem), enquanto sub-agentes isolam por contexto (tokens). [[nate-herk]] é o primeiro criador do wiki a documentar essa taxonomia completa
- **Ultra think como budget máximo de raciocínio**: digitar `ultra think` no prompt aloca ~32.000 tokens de thinking antes de qualquer resposta — modo reservado para decisões de arquitetura, debugging profundo e refatorações sistêmicas. Complementa o Adaptive Thinking ([[alex-finn]]) e o `/effort` ([[boris-cherny]]): são três eixos de controle de profundidade independentes
- **Permissões explícitas como alternativa responsável ao modo perigoso**: configurar allow list + deny list (deny tem prioridade) produz a mesma velocidade do `--dangerously-skip-permissions` sem o risco. [[nate-herk]] documenta que a maioria dos criadores (inclusive ele) promoveu o modo perigoso sem apresentar essa alternativa
- **Pipeline agêntico de vendas como novo arquétipo**: [[jordan-lee]] documenta o primeiro sistema do wiki onde a IA cobre tanto a aquisição (AI SDR → qualificação → chamada agendada) quanto a entrega (Sales Call Analyzer → proposta). Arquétipos anteriores separavam essas funções — aqui o funil comercial inteiro é agêntico, operado sem código por quem "foca em relacionamentos"
- **Repositórios open-source como modelo de monetização direta**: [[paras-madan]] apresenta 6 repos onde o retorno é direto — cortar budget de anúncios, automatizar trading e extrair dados de sites protegidos. [[tradingagents]] (55.700 stars) introduz o padrão "debate entre agentes" como mecanismo de decisão: fundamentos + sentimento + técnica + risco discutem antes de agir. HKUDS/AI-Trader introduz `SKILL.md` como protocolo de integração de agentes em sistemas financeiros — ecos do CLAUDE.md de [[boris-cherny]] aplicados ao domínio de finanças
- **Templates com placeholders como padrão de democratização de prompts**: [[laura-anderson]] documenta o padrão mais explícito até aqui — todos os 5 prompts usam `[insert job title]`, `[list skills]`, `[insert background]` como portas de entrada. O usuário não precisa aprender prompt engineering; preenche campos e executa. O LLM faz 70–90% do trabalho operacional. Convergência com [[sabrina-ramonov]] (mesma intenção, formatos diferentes): ambas posicionam IA como parceiro de execução, não de planejamento.
- **"One-Person Business" como arquétipo mais restritivo do wiki**: [[dan-koe]] (via [[ai-fied]]) documenta negócio de $6M com zero funcionários e 4h/dia — a restrição de equipe é princípio de design, não limitação. O arquétipo é complementar aos demais: usa os mesmos LLMs, mas o objetivo explícito é "runs without you" — sistemas que operam sem presença ativa do criador. Convergência com [[naval-ravikant]] (produtize yourself) e [[tim-ferriss]] (Muse Business), agora com case empírico documentado e 5 prompts acionáveis

---

## Status do wiki

| Tipo | Quantidade |
|------|-----------|
| Fontes ingeridas | 60 |
| Páginas de fontes | 60 |
| Páginas de conceitos | 18 |
| Páginas de entidades | 72 |
| Páginas de síntese | 2 |
| **Total de páginas** | **152** |
