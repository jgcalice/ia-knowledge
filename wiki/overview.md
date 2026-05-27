---
title: "Overview — IA Knowledge Base"
type: overview
last_updated: 2026-05-27
source_count: 98

---

# Overview — IA Knowledge Base

> Wiki iniciado em 2026-04-21 | 98 fontes ingeridas | Domínio: IA Aplicada a Negócios, Carreira, Gestão, Produto, **Adoção Empresarial**, **Finanças**, **Bem-estar**, **SEO + Conteúdo**, **IA Local**, **Viagem** e **Segurança/Compliance**

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

- **Método 5**: Prompts + ChatGPT/Claude → identificar negócios #6–20 no Maps → prospecção + entrega de serviço GMB ($500–$1K/mês retainer) ([[derek-gray]]); **sweet spot pattern** documentado na 3ª fonte: 5+ anos, <80 reviews, sem site, 3.9+ ⭐ → 25–30 leads de um nicho/cidade

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
- **Claude Mem**: primeira solução de memória cross-session totalmente automática — SQLite + busca vetorial, 10x menos tokens de startup; auto-gera CLAUDE.md por pasta ([[nate-herk]])
- **GSD como context engineering**: sub-agentes frescos por tarefa + quality gates automáticos (scope protection + security enforcement) — custo em tokens aceito para eliminar retrabalho por context rot ([[nate-herk]])
- **Ruflo (roteamento automático)**: camada de orquestração externa `ruvnet/ruflo` roteia tasks automaticamente para o modelo mais barato compatível com a complexidade → -50% tokens, +250% uso por sessão ([[duncan-rogoff]])

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
| Reconstrução completa de candidatura | 4 prompts com ROLEs de recrutadores elite: resume XYZ + ATS optimization + McKinsey quantifier + cover letter Robert Half | [[your-ai-compass]] |
| Preparação para entrevista | 5 prompts encadeados: prever perguntas → respostas STAR → pontos fracos → mock brutal (score 0-10) → cheatsheet 60s | [[roshan-krishna]] |
| Redesenho estratégico | 4 prompts Tim Ferriss: vantagem injusta, DEAL, freedom ratio, 10 anos | [[god-of-prompt]] |
| Monetização imediata | 4 prompts para ganhar $1k em 30 dias com skills existentes | [[sabrina-ramonov]] · confirmado por [[allessandra-sinisgalli]] |
| Monetização com templates | 5 prompts-template `[insert X]`: freelance do cargo atual, plano 30 dias $10K, desafio 7 dias, day rate $1K/dia, serviço $10K/mês | [[laura-anderson]] |
| Certificação formal | Claude Certified Architect (grátis, proctored, valorizado pela Deloitte) | [[bashiri]] |
| Filosofia de riqueza | 6 prompts Naval Ravikant — texto completo de 5 prompts nomeados (Excavator, Auditor, Brand Architect, Productize, Judgment); 3ª variação confirmando o framework | [[god-of-prompt]] · [[simplifying-ai]] · [[ai-fied]] |

---

### Cluster 7: Segurança Digital com IA
**Conceito central:** [[segurança-com-ia]]

- **Dimensão 1 — Desenvolvimento preventivo**: 5 fundamentos design-time para apps com Claude Code: API keys no servidor, RLS no Supabase, lógica sensível no back-end, rate limiting e webhooks assinados ([[lucas-garcia-pit]])
- **Dimensão 2 — Privacidade/OSINT**: 14 ferramentas documentadas em 3 fontes BR: ZoomEye, HIBP, Namecheck, Pic2Map, EPA, Exploding Database ([[gustavo-melo]] post 1) + Sherlock, Maltego, SpiderFoot, Shodan, Google Dorking ([[sidney-rodrigo]]) + Webmail e My7 — investigação de pessoa física ([[gustavo-melo]] post 2)
- **Dimensão 3 — Empresarial**: Shadow AI (70-80% usam ferramentas não aprovadas), segurança como enabler front-loaded, pipeline PII scrubbing como moat ([[stanford-digital-economy-lab]])
- **Dimensão 4 — Vibecoding pré-deploy**: prompt de 6 blocos que instrui o agente a auditar o codebase como engenheiro sênior de segurança ($15k em valor); conceito de **attack chains** (3 vulns "low" = 1 "critical") ([[artificial-intelligence-business]] / @thewizeai)
- **Dimensão 5 — Remoção ativa de pegada digital**: guia de 7 passos para apagar 99,8% da exposição online — data brokers (Spokeo, Whitepages, BeenVerified), Google removal request, contas esquecidas via Gmail, HaveIBeenPwned, desativar rastreamento Google, posts antigos (TweetDelete/Redact) e prevenção futura com SimpleLogin e Brave/Firefox ([[ai-technology]])
- **Dimensão 6 — Checklist jurídico-técnica pré-lançamento** (NOVO): "vibe coders are getting sued" — checklist ordenada de 6 itens obrigatórios antes de abrir para usuários reais, curada de 60+ MVPs de agência. GDPR/CCPA desde o 1º dado coletado; RLS (#1 miss — qualquer um abre o DevTools e lê o banco); failure-path testing; security headers + OWASP; server-side validation ("Zod on client is UX, not security"). A **sequência importa**: escalar marketing antes de completar a checklist amplifica o risco e o passivo jurídico ([[today-in-ai]] / @PrajwalTomar_)
- **Tese unificada**: aceleração (LLMs no dev, internet nos dados, mandato corporativo) cria exposições invisíveis que exigem intenção ativa para serem corrigidas — em 6 escalas diferentes

---

### Cluster 4: Negócios e Estratégia com IA
**Conceito central:** [[estratégia-de-negócios-com-ia]]

- 5 prompts para validar idea de startup com framework Paul Graham: pressure test → problema real → concorrentes → primeiros 10 clientes → MVP em 2 semanas ([[harry]])
- 7 prompts para análise de mercado, oferta e escalonamento ([[evolving-ai]], [[business-bulls]])
- Playbook "low-hanging fruit": Reddit hand-to-hand combat (primeiros 100 clientes) → Programmatic SEO ($3M+ ARR, 150K+ usuários, $250K/mês) — ([[starter-story]], case Joseph)
- Branding completo em 2h com 120+ agentes ([[rafael-brandao]])
- SEO na primeira página do Google com 3 arquivos de texto ([[brycen-wood]])
- SEO data-driven: Google Search Console + Claude para priorizar palavras-chave "quase ranqueando" e otimizar conteúdo existente sem criar nova página — workflow que agências cobram R$5K, feito em minutos ([[daniel-socrates]])
- **Guia oficial Google (NOVO)**: AI Overviews e AI Mode usam RAG + query fan-out sobre o mesmo ranking tradicional — não existe algoritmo separado de IA. Mythbusting oficial: `llms.txt`, fragmentação de conteúdo e reescrita para IA **não são necessários**. ⚠️ Contradição com [[brycen-wood]] que recomenda `llms.txt` como chave para SEO na era IA ([[ai-researches-ai]])
- 5 modelos nativos de IA (eBook, YouTube narrado, newsletter, curso online, agente WhatsApp como AIaaS) ([[bruno-wambier]])
- Mini web app focado + Instagram como canal único ([[luna-vega]])
- AI Agency (Dan Martell, Liam Ottley) — agência automatiza outras empresas ([[paul-hilse]])
- Stack de 5 skills open-source para founder solo: Meta Ads + Position Me + LinkedIn Post Generator + Reddit ICP Monitor + Google Trends SEO ([[paras-madan]])
- GMB Optimization Agency: stack completo Google Maps → Claude → [[lovable]] → Outreach → [[quepo]] (95% automatizado) — $12K/mês em 6 meses. Sweet spot: 5+ anos, <80 reviews, sem site, 3.9+ ⭐. Argumento de ROI: top 5 captura 60% dos cliques = $4–6K em PPC → proposta a $500/mês ([[derek-gray]])
- AI Sales Agency: 3 agentes (AI SDR + Sales Call Analyzer + AI Consultant) cobrem todo o funil — do outreach ao contrato fechado — sem código. $3K/cliente vs $30–50K economizados/ano ([[jordan-lee]])
- Playbook operacional completo de AI Agency: 7 prompts de [[jordan-lee]] (via [[your-ai-compass]]) — Niche Domination → Offer Builder ($2K/$5K/$10K) → Cold Email Machine → Objection Destroyer → Onboarding Playbook → Upsell Identifier → CEO Weekly Report
- One-Person Business (Dan Koe model): 5 prompts — ideia → oferta-transformação → sistema de conteúdo → vendas autônomas → escalar sem contratar. Case: $6M, 0 funcionários, 4h/dia ([[ai-fied]] via [[dan-koe]])
- Repos open-source como substitutos de softwares de cinco dígitos: FinceptTerminal ($24K/ano → grátis), Open-Gen-AI ($100+/mês → grátis), Claude Ads ($2K/cliente → $1,5K de receita via revenda). O ângulo não é "ferramenta para operar negócio", mas "substituir a linha de despesa e embolsar a diferença" ([[bestapps-ai]])
- **Amazon FBA com IA**: 5 prompts para lançar produto físico na Amazon — único arquétipo de e-commerce físico do wiki. Produto → fabricante → marca → listing SEO → plano de lançamento. Amazon FBA cuida de toda a logística. Exemplo documentado: Cleaning Gel Tablets, marca Dissolv, margem 28%, $10K/mês em 7–9 meses ([[shimin-mohammadi]])
- **3ª confirmação — repos como modelo de monetização**: [[growai]] confirma o ecossistema de repos open-source com enquadramento distinto: "$10K/mês com ferramentas gratuitas do GitHub". Detalhe novo: Claude Ads como auditoria de anúncios por $1.500/cliente; Hyperframes como produção de vídeo automatizada para agentes IA. 3 fontes independentes (paras-madan, bestapps-ai, growai) = padrão consolidado no wiki
- **4ª perspectiva sobre repos — white-label SaaS**: [[harish-bhatt]] documenta o ângulo de "tornar-se o provedor de SaaS" via fork de repos estabelecidos — Cal.com ($5M ARR), Ghost (100% margem), [[n8n]] ($14M captados), Supabase ($116M captados). Não é usar a ferramenta, é revender o acesso. Primeira aparição de [[n8n]] no wiki como alternativa open-source ao Zapier para montar automação agency
- **4ª perspectiva sobre repos confirmada por fonte independente (NOVO)**: [[today-in-ai]] (aitickerdaily/curatedai.net) publica os mesmos 10 repos do ângulo white-label SaaS com nichos verticais explícitos — Cal.com para dentistas/advogados ($200/mês), Plausible para agências ($50/mês), Penpot para agências com restrição de cloud. Fonte totalmente independente de [[harish-bhatt]]: padrão consolidado com múltiplas confirmações
- **5ª perspectiva sobre repos — custo zero pessoal/dev**: segundo post de [[harish-bhatt]] enquadra repos como eliminadores de assinaturas SaaS pessoais — [[ollama]] ($0 vs OpenAI API ~$500/mês), [[whisper]] ($0 vs Otter.ai $20/mês), [[n8n]] ($0 vs Zapier Pro $600/mês). Framing "destroem $50B em receita corporativa". Novidade: [[ollama]] como **primeira entrada de IA local no wiki** — LLMs GPT-4 class offline, privacidade por design; [[whisper]] como modelo de transcrição open-source da OpenAI
- **Solo Founder com Managed Agents** (NOVO): [[artificial-intelligence-business]] / @thewizeai documenta playbook de 7 passos sem código para $10K/mês com Claude Managed Agents — 20 agentes em paralelo (recorde do wiki), MCP como camada de conexão ao stack da empresa, stack encadeada de 3 agentes como produto. Contexto: aposta de Dario Amodei ($1B one-person company até fim de 2026)
- **Tier matrix de nichos para AI agents**: [[derek-gray]] classifica 6 setores de serviços locais por potencial de ROI — Solar (God-Tier) e Window Replacement (S-Tier) são top porque o CAC já é alto ($5K+), treinando os clientes a pagar por aquisição. Gyms (F-Tier) é o primeiro exemplo no wiki de nicho que *parece* óbvio para Maps SEO mas onde o vetor de decisão é social (amigos), não busca. Setup mínimo documentado: $55/mês em software
- **IA local como infraestrutura de custo zero** (NOVO): [[hasan-toor]] documenta guia de 7 passos para rodar modelos open-source (Qwen3, DeepSeek-R1) offline em <20 minutos com [[ollama]] ou [[lm-studio]]. Habilitador técnico: quantização Q4_K_M (140GB → 40GB, qualidade quase idêntica). API OpenAI-compatível em `http://localhost:11434` permite que qualquer pipeline existente aponte para a máquina local sem mudança de código. Conceito central: [[ia-local]]
- **AI Side-Hustle com Ferramentas Pré-construídas** (NOVO): [[bruno-souza]] documenta sistema de 5 passos para cobrar $1–3K/mês de negócios locais implementando ferramentas SaaS de IA existentes (Jasper, Smartlead, Reclaim, Claid) — sem código. Diferencial do Step 4: LLM simula o dono do negócio-alvo para identificar dores repetitivas antes da ligação de vendas — primeiro uso documentado de LLM como *empathy mapping de prospect* no wiki. ⚠️ Contradição com [[derek-gray]]: Gyms são recomendados aqui mas F-Tier para Maps SEO — a diferença é o serviço (automação interna vs. ranqueamento no Google)

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

**3º ângulo:** Pipeline sequencial de screening para seleção de ações de swing trade — 3 prompts em funil (tema → 25 candidatos → top 3 deep dive) em 5 minutos. **Limitação explícita:** IA não substitui leitura de gráfico no timing de entrada. Case: $129K/ano com full-time job, AMD e Palantir como exemplos. ([[bert-no-chase]])

**4º ângulo:** Análise DIY de ações com analista genérico — template ROLE/TASK/STEPS/RULES/OUTPUT com saída estruturada: modelo de negócios → saúde financeira → moat → valuation → bear/bull case → recomendação. Distinto dos ângulos anteriores: sem nomear instituição (vs. [[faria-lima-elevator]]), sem funil de triagem (vs. [[bert-no-chase]]). Mesmo carousel introduz **1º prompt de planejamento fiscal do wiki**: Tax Strategist com checklist de deduções, cenários fiscais e comparação CPA vs. software. ([[ai-fied]])

**5º ângulo:** Pipeline sequencial completo — 10 prompts em ordem replicando o workflow inteiro de analistas institucionais de Wall Street. Alternativa gratuita ao Bloomberg Terminal ($24K/ano): Kickoff Report → Earnings Analysis → Bull/Bear Debate → Forensic Accounting → Valuation Framework → Company Comparison → Investor Summary → Stress Test → Big Business vs Big Stock. **Novidade estrutural**: sequência como metodologia (order > isolation); Forensic Accounting como ângulo inédito no wiki (stock-based comp, contabilidade agressiva, red flags pré-compra); stress test com atribuição de probabilidades aos cenários. ([[artificial-intelligence-business]] / @thewizeai)

**6º ângulo (NOVO):** Claude como **gestor de portfólio autônomo com dinheiro real** ($50.000, sem supervisão humana). Pipeline de 5 etapas: triagem de 1.000 ações → 30 agentes IA debatendo bull vs bear → price targets ponderados por probabilidade → portfólio de 15 ações → rebalanceamento automático na corretora. [[autopilot]] permite espelhar os trades na conta do usuário sem código ou decisão própria. **Distinção fundamental**: é o único ângulo do wiki onde a IA não só analisa, mas *decide e executa*. ([[roman-khaneichuk]])

---

## Mapa de entidades

**Ferramentas e plataformas**: [[claude-code]] · [[claude-skills]] · [[smithery]] · [[apify]] · [[api-file]] · [[markitdown]] · [[linkedin]] · [[google-maps]] · [[career-ops]] · [[graphify]] · [[obsidian]] · [[vibe-prospecting]] · [[simplifying-ai]] · [[context7]] · [[tradingagents]] · [[ruflo]] · [[lovable]] · [[quepo]] · [[n8n]] · [[autopilot]] · [[ollama]] · [[whisper]] · [[lm-studio]]

**Agregadores de conteúdo**: [[ai-developer-js]] · [[bestapps-ai]] (2 fontes) · [[beyond-intelligence]] · [[growai]] · [[ai-researches-ai]] · [[today-in-ai]] (2 fontes)

**Instituições acadêmicas**: [[stanford-digital-economy-lab]]

**Referências externas**: [[paul-graham]] · [[naval-ravikant]] · [[dan-koe]] · [[erik-brynjolfsson]] · [[alvin-wang-graylin]] · [[elisa-pereira]] · [[alex-hormozi]]

**Conceitos de segurança**: [[segurança-com-ia]]

**Pessoas (BR)**: [[lucas-garcia-pit]] · [[hudson-brendon]] · [[bruno-souza]] · [[rafael-brandao]] · [[flavio-rafael]] · [[rony-meisler]] · [[bruno-wambier]] · [[adriano-couto]] · [[eduardo-santos]] · [[castilho]] · [[gustavo-melo]] · [[sidney-rodrigo]] · [[faria-lima-elevator]] · [[allessandra-sinisgalli]] · [[daniel-socrates]]

**Pessoas (Internacional)**: [[evolving-ai]] · [[god-of-prompt]] · [[bashiri]] · [[sabrina-ramonov]] · [[ross-fledderjohn]] · [[michael-kocher]] · [[brandon-lew]] · [[usama-akram]] · [[brycen-wood]] · [[business-bulls]] · [[aashish-pahwa]] · [[luna-vega]] · [[paul-hilse]] · [[marc-cleroux]] · [[andrej-karpathy]] · [[alex-finn]] · [[nate-herk]] · [[pablo-in-public]] · [[sanskaar-singh]] · [[arshman-khalid]] · [[paras-madan]] · [[harry]] · [[yik-chan]] · [[ai-fied]] · [[ai-updater]] · [[manthan-patel]] · [[arising-ai]] · [[starter-story]] · [[coding-ai-fullstack]] · [[derek-gray]] · [[jordan-lee]] · [[your-ai-compass]] · [[bert-no-chase]] · [[duncan-rogoff]] · [[ai-technology]] · [[shimin-mohammadi]] · [[harish-bhatt]] · [[roman-khaneichuk]] · [[hasan-toor]] · [[roshan-krishna]]

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
- **Playbook operacional vs. playbook agêntico — dois níveis da AI Agency**: [[jordan-lee]] tem agora dois documentos complementares no wiki: o primeiro ([[2026-04-15_jordan-lee-vendas-sistema-ia]]) descreve o pipeline agêntico de vendas (3 agentes cobrem todo o funil); o segundo ([[2026-04-30_your-ai-compass-7-prompts-agencia-ia]]) expõe o playbook operacional de 7 prompts — o que o operador humano executa para montar, vender e gerenciar a agência. Juntos formam o único registro completo do wiki de como construir e operar uma AI Agency end-to-end
- **Agent Development Kit — primeira arquitetura completa de infraestrutura de agente no wiki**: [[manthan-patel]] sistematiza 5 camadas — CLAUDE.md (constituição persistente), Skills (conhecimento modular sob demanda), Hooks (shell scripts determinísticos em 5 tipos de evento), Subagents (delegação com contexto isolado) e Plugins (pacotes npm para distribuição em equipe). Hooks são a novidade técnica: a camada que converte intenções do agente em regras obrigatórias executadas pelo sistema, sem participação da IA. Complementa e generaliza o CLAUDE.md de [[boris-cherny]] para o quadro completo de configuração + controle + distribuição
- **Convergência Brasil–EUA no framework de monetização de skills**: [[allessandra-sinisgalli]] reproduz os mesmos 4 prompts de [[sabrina-ramonov]] e documenta o comportamento real do Claude — o modelo faz perguntas de alinhamento antes de responder (95% de confiança em prática), indica [[alex-hormozi]] com justificativa específica e gera artefatos concretos em persona do mentor. Segundo caso confirmando o framework; reforça que "implementação > planejamento" como tese não é específica de uma criadora, mas um padrão convergente
- **Slash-command style activators como notação mnemônica para ativadores semânticos**: [[ai-developer-js]] documenta 13 pseudo-comandos com prefixo "/" (/godmode, /devil, /10x, /scout, /compare…) que funcionam como ativadores informais de modo no Claude. São variações com notação de barra dos mesmos ativadores semânticos já documentados ([[castilhoia]]) e ELI5 ([[adriano-couto]]). O valor é a mnemônica: o "/" torna o ativador visualmente distinto e fácil de lembrar; não são comandos nativos do Claude Code CLI
- **Repos open-source como corte de cinco dígitos — framing de substituição, não de ferramenta**: [[bestapps-ai]] reencadra o tema "repos para monetizar" (já presente em [[paras-madan]]): a pergunta não é "que ferramenta usar?" mas "quanto você economiza vs a alternativa paga?". FinceptTerminal = $24K/ano; Open-Gen-AI = $100+/mês; Claude Ads = $2K/cliente. O modelo de receita emerge automaticamente: entregar o setup como serviço e cobrar uma fração do custo substituído. Convergência temática: Claude Ads e Context Mode aparecem em ambos os posts — dois repos com múltiplas confirmações independentes
- **Taxonomia de 89 comandos como mapa mental de modos de uso**: [[beyond-intelligence]] publica referência mais ampla que os 13 pseudo-comandos de [[ai-developer-js]] — 89 entradas em 11 categorias funcionais. O valor não está nos itens individuais (o post não distingue comandos nativos CLI de pseudo-comandos informais), mas na **taxonomia** em si: Start & Create → Focus & Context → Think & Solve → Write & Edit → Organize & Structure → Code & Tech → Data & Analysis → Automate & Integrate → Personalize & Control → Learn & Research → Collaborate & Share. As 11 categorias mapeiam o espectro completo de intenções de uso do Claude — uma referência de orientação, não de execução
- **IA local elimina o custo de tokens — mais radical que redução**: [[hasan-toor]] documenta que a barreira técnica para rodar LLMs localmente colapsou. Em 20 minutos e 16GB de RAM, qualquer pessoa tem um modelo 7B–8B rodando com qualidade comparável ao Claude Pro ($20/mês) ou ao uso de API. A quantização Q4_K_M ([[ia-local]]) é o enabler: modelos que precisavam de data center cabem agora em hardware de consumidor. Todas as técnicas de [[otimização-de-tokens]] documentadas até aqui tratam de *reduzir* custo; IA local o *elimina*. O impacto no mapa de arquétipos de [[estratégia-de-negócios-com-ia]] é transversal: qualquer negócio baseado em API de LLM pode reconsiderar sua estrutura de custo
- **Pasta `.claude/` como sistema — distinção advisory vs. determinístico**: [[manthan-patel]] ancora as 5 camadas do Agent Development Kit em localizações físicas concretas e formula a distinção operacional mais importante para quem implementa: *"CLAUDE.md is advisory. hooks are deterministic."* O CLAUDE.md é consultado pelo modelo, que *pode* seguir; os hooks são scripts que o *sistema* executa sempre, sem decisão da IA. Regras que o desenvolvedor quer garantir devem estar em hooks, não em CLAUDE.md. Princípio de design: *"The folder structure IS the system"*
- **Screening de ações como caso-modelo de pipeline sequencial em domínio especializado**: [[bert-no-chase]] documenta o uso de 3 prompts encadeados (tema → universo → ranking → deep dive) para triagem de candidatos a swing trade em 5 minutos. O padrão sequencial já documentado em [[geração-de-leads-com-ia]] e em [[finanças-com-ia]] reaparece aqui com a mesma lógica: ampliar → filtrar → aprofundar. Novidade editorial: o autor reconhece explicitamente que IA não substitui análise técnica no timing — a IA faz a triagem fundamentalista; o humano decide *quando* entrar
- **Pipeline de reconstrução de candidatura com ROLEs de elite**: [[your-ai-compass]] documenta 4 prompts encadeados onde Claude assume personas sequenciais de recrutadores de alto nível — Google (triagem de currículo), ATS specialist (compatibilidade automática), McKinsey (quantificação de conquistas) e Robert Half (carta de apresentação). O padrão ROLE-como-instituição confirma-se no domínio de carreira: nomear organizações cujas metodologias o modelo internalizou (Google hiring bar, McKinsey achievement framework) é suficiente para convocar o framework completo sem descrever o método. O ATS Optimization Prompt é a contribuição técnica mais nova — nomear sistemas reais (Workday, Greenhouse, Lever) orienta o modelo para as restrições de parsing específicas de cada plataforma
- **Ruflo como camada de roteamento automático — a automação da escolha de modelo**: [[duncan-rogoff]] apresenta o primeiro registro no wiki de uma infraestrutura externa que automatiza a decisão de qual modelo usar por task (Técnica #3 do [[otimização-de-tokens]]). Diferente das abordagens manuais ([[nate-herk]], [[evolving-ai]]), o Ruflo inspeciona a complexidade do task e faz o roteamento sem intervenção do dev. Padrão novo: **a escolha de modelo deixou de ser decisão de prompt e passou a ser infraestrutura**
- **"Referência famosa como gancho" consolidado como padrão de conteúdo**: [[ai-fied]] confirma a terceira iteração — Munger junta-se a Naval Ravikant e Dan Koe como wrapper de autoridade para coleções de prompts ROLE/TASK/STEPS/RULES/OUTPUT. O conteúdo central são sempre os prompts; a figura histórica é o title card. Padrão emergente na comunidade de criadores de conteúdo de IA.
- **Planejamento fiscal como ponto cego do wiki**: primeiro prompt de tax strategy documentado ([[ai-fied]], Prompt 5 do carousel Munger) — revela que [[finanças-com-ia]] pode expandir de "análise de ações" para "planejamento financeiro pessoal" (impostos, deduções, CPA vs. software).
- **"Nunca mencione IA" como regra de outreach confirmada**: [[derek-gray]] documenta que 90% do outreach falha por mencionar Claude, IA, ou processo técnico. O cliente compra o resultado (mockup funcional, ranking no Maps), não a tecnologia. Padrão convergente com [[nate-herk]] ("vender outcomes, não workflows") e [[jordan-lee]] ("você entrega dinheiro grátis, fica com uma pequena parte") — três fontes independentes confirmam que a ocultação da IA no pitch é *estratégia*, não limitação
- **[[lovable]] entra no wiki como ferramenta de prototipagem para outreach**: primeiro registro de geração de landing page como parte do pipeline de prospecção local — o mockup ao vivo substitui o pitch de venda (o cliente vê a solução antes de qualquer conversa comercial)
- **[[quepo]] como modelo de "agente como serviço recorrente"**: primeiro agente de IA proprietário de um criador documentado no wiki — automatiza 95% do GBP Management, convertendo um serviço ativo em renda passiva recorrente. Padrão distinto do AIaaS de [[bruno-wambier]] (agente empacotado como produto) — aqui o agente opera nos bastidores sem que o cliente saiba
- **Remoção ativa como par complementar ao diagnóstico OSINT**: [[ai-technology]] fecha o ciclo da Dimensão 2 de [[segurança-com-ia]] — as fontes anteriores (OSINT, HaveIBeenPwned, Webmail/My7) ensinavam a *descobrir* a exposição; este guia ensina a *remover*. HaveIBeenPwned aparece em ambos os lados, confirmando sua posição como pivô entre diagnóstico e remediação. Data brokers (Spokeo, Whitepages, BeenVerified) e SimpleLogin são primeiras ocorrências no wiki
- **Amazon FBA como único arquétipo de produto físico**: [[shimin-mohammadi]] introduz o primeiro modelo de e-commerce com produto físico no wiki — todos os arquétipos anteriores (SaaS, agência, infoproduto, GMB, leads) são digitais ou de serviço. O padrão de "5 prompts encadeados com output sequencial" se confirma (4ª iteração independente: [[jordan-lee]], [[derek-gray]], [[luna-vega]], [[shimin-mohammadi]]). Novidade estrutural: Amazon FBA elimina a barreira de logística — o operador pesquisa produto, cria marca e faz listing; a Amazon cuida do resto
- **Tier matrix de nichos como pré-filtro estratégico**: [[derek-gray]] documenta que a escolha do setor precede qualquer prospecção — Solar (God-Tier) tem CAC de $5K+, tornando $500–1K/mês trivial de justificar; Gyms (F-Tier) falham porque a decisão de compra é social, não via Google. Primeiro mapeamento explícito no wiki de setores onde Maps SEO *não funciona*
- **White-label SaaS como 4º ângulo dos repos open-source**: [[harish-bhatt]] (@codingknowledge) introduz a perspectiva de "você vira o provedor" — fork de repos com ARR bilionário de referência (Cal.com, Supabase, Ghost) e revenda do acesso como SaaS próprio. Difere estruturalmente dos três ângulos anteriores: paras-madan (operar canais com repos), bestapps-ai (substituir software caro), growai (monetizar ferramentas de IA). Aqui o repositório **é o produto** vendido ao cliente final, não o meio de construção do serviço. [[n8n]] entra no wiki como alternativa open-source ao Zapier com 400+ integrações e IA nativa
- **5º ângulo dos repos open-source — custo zero para o próprio dev/usuário (NOVO)**: segundo post de [[harish-bhatt]] enquadra os mesmos repos como eliminadores de assinaturas SaaS pessoais — [[ollama]] ($0 vs OpenAI API ~$500/mês), [[whisper]] ($0 vs Otter.ai $20/mês), Penpot ($0 vs Figma $45/editor/mês), [[n8n]] ($0 vs Zapier Pro $600/mês). Framing: "destroem $50B em receita corporativa". Introduz **[[ollama]] como primeira entrada de IA local no wiki** — modelos GPT-4 class offline, privacidade por design, sem quota de API; e **[[whisper]]** como modelo de transcrição OpenAI open-source usado diretamente, sem wrapper pago
- **Gestor autônomo com skin in the game real**: [[roman-khaneichuk]] documenta o primeiro caso no wiki onde Claude *executa trades* com capital real ($50.000, Wharton PhD, sem supervisão humana) — cruzamento entre análise financeira agêntica e execução efetiva. O padrão "30 agentes bull vs bear" é a 3ª confirmação independente do mecanismo de debate como decisão financeira (após [[tradingagents]] e [[artificial-intelligence-business]]). [[autopilot]] como camada de distribuição introduz um modelo novo: qualquer usuário delega a um agente e espelha sua execução, sem código e sem análise própria
- **SEO com IA tem duas abordagens complementares documentadas**: [[brycen-wood]] (técnica, arquivos: llms.txt + Markdown mirrors + sitemap) e [[daniel-socrates]] (dados, otimização de conteúdo existente: GSC → Claude prioriza → ajuste mínimo → solicitar indexação). A primeira prepara o site para ser lido por Google/IA; a segunda identifica e explora oportunidades de ranqueamento via dados reais. Ambas democratizam técnicas que agências cobram caro — conceito consolidado em [[seo-com-ia]]
- **Viagem como novo domínio de "substituto de serviço profissional"**: [[bestapps-ai]] documenta 7 prompts para análise de preços de voos que aplicam o padrão ROLE "analista profissional" a consumo B2C pela primeira vez. O mesmo mecanismo documentado em [[bem-estar-com-ia]] (fitness), [[finanças-com-ia]] (análise de ações) e engenharia (Harish Bhatt) funciona igualmente para viagem — o LLM internalizou know-how de revenue management de companhias aéreas. Novidade de design: Prompt 5 categoriza explicitamente 3 tiers éticos (Legitimate / Against T&Cs / Off-limits) — padrão reutilizável em qualquer domínio onde otimização pode cruzar limites legais. Primeiro conteúdo de viagem do wiki: [[viagem-com-ia]]
- **"Act like a senior engineer" como extensão do Persona Mode para engenharia de software**: [[harish-bhatt]] confirma e especializa o padrão [[Persona Mode e Output Constraints]] ([[yik-chan]]) em 11 variantes de engenharia. Cada prompt estrutura abertura + missão + constraint + entregáveis — tornando o Claude não mais um executador de comandos pontuais, mas um parceiro de nível sênior com responsabilidade de entrega. Novidade singular: Prompt 7 simula 4 papéis em cascata dentro de um único prompt (Architect → Engineer → Reviewer → Optimizer) — auto-review multi-perspectiva sem orquestração externa. 3ª contribuição de [[harish-bhatt]], completamente diferente das duas anteriores (repos open-source) — mesmo criador, segmento diferente
- **Pipeline de carreira completo — da visibilidade à performance na entrevista**: [[roshan-krishna]] fecha a lacuna final do Cluster 3. O wiki agora documenta as 3 fases da jornada de emprego com IA: **otimizar perfil** ([[bruno-souza]], [[sanskaar-singh]]) → **candidatura personalizada** ([[coding-ai-fullstack]], [[your-ai-compass]], [[career-ops]]) → **performance na entrevista** ([[roshan-krishna]]). Novidades técnicas do pipeline de 5 prompts: (1) STAR como instrução explícita ao modelo com limite temporal de 90s para resposta oral — primeira constraint de duração verbal no wiki; (2) `[INSERT YOUR STORY]` como placeholder de delegação parcial — o LLM gera tudo exceto a memória episódica pessoal; (3) "Brutal Mode" (score 0-10 + diagnóstico + versão 9+) como padrão de feedback estruturado anticomplacência

---

## Status do wiki

| Tipo | Quantidade |
|------|-----------|
| Fontes ingeridas | 98 |
| Páginas de fontes | 98 |
| Páginas de conceitos | 20 |
| Páginas de entidades | 104 |
| Páginas de síntese | 2 |
| **Total de páginas** | **230** |

## Adições da ingestão de 2026-05-27 (2 fontes novas)

- **3ª confirmação do sistema Amazon KDP de [[drew-huibregtse]] — coloring books com dashboard real**: carousel de 2026-05-14 foca especificamente em livros de colorir. Novas contribuições: (1) ChatGPT entra no stack de geração de imagem ao lado de Nano Banana — primeira confirmação de ChatGPT como gerador de imagem prático no wiki; (2) prompt canônico para colorir: "Give me 40 detailed interior page descriptions for a [niche] coloring book. Each page should be unique, intricate, and optimized for print."; (3) dashboard real do KDP com datas (abr/2026): $13.392 — dado mais confiável que os números autodeclarados das fontes anteriores; (4) Tiny Gardens: $22.062/30 dias com 2.208 cópias. Atualizado: [[drew-huibregtse]] (source_count 2→3), [[amazon-kdp]] (source_count 2→3, ChatGPT adicionado ao stack), [[helium-10]] (source_count 2→3), [[estratégia-de-negócios-com-ia]] (source_count 31→32, 3ª fonte adicionada à seção Amazon KDP).
- **5 prompts de [[roshan-krishna]] para preparação de entrevistas de emprego**: cobre a fase pós-candidatura — *desempenho durante a entrevista* — que estava faltando no Cluster 3. Pipeline de 5 prompts encadeados: prever perguntas (JD → 15 Qs em 3 categorias + nota do que cada uma testa) → respostas STAR com placeholders para histórias pessoais → identificar 3 pontos fracos + follow-ups difíceis → mock interview com score 0-10 ("Brutal Mode") → cheatsheet de 60 segundos para revisar antes de entrar. Entidade criada: [[roshan-krishna]]. Atualizado: [[busca-de-emprego-com-ia]] (source_count 4→5, nova seção "Preparação para entrevistas"), [[carreira-com-ia]] (source_count 18→19, novo item 11), [[prompt-engineering]] (source_count 38→39, nova seção "STAR como instrução explícita" + "Brutal Mode" como padrão de feedback).

## Adições da ingestão de 2026-05-26 (2 fontes novas)

- **7 prompts de [[bestapps-ai]] para análise profissional de preços de voos**: abre [[viagem-com-ia]] como novo domínio do wiki (análogo a [[bem-estar-com-ia]] e [[finanças-com-ia]]). Padrão ROLE "analista profissional" aplicado a consumo B2C pela primeira vez. Destaque: Prompt 5 (fare rules) categoriza estratégias em 3 tiers éticos — primeira delimitação explícita de ética em otimização de consumo no wiki. Atualizado: [[bestapps-ai]] (source_count 1→2), [[prompt-engineering]] (source_count 37→38, extensão da seção "substitutos de serviços profissionais"). Criado: [[viagem-com-ia]] (novo conceito).
- **11 prompts de [[harish-bhatt]] para Claude como engenheiro sênior** (3ª contribuição, ângulo completamente diferente das anteriores — repos): extensão do padrão "Act like a senior X" exaustivamente aplicado a engenharia de software (audit, debug, performance, arquitetura, frontend, equipe de 4 agentes, AI Technical Lead). Atualizado: [[prompt-engineering]] (source_count 36→37, nova seção "Act like a senior engineer"), [[harish-bhatt]] (source_count 2→3, ângulo 3 documentado).

## Adições da ingestão de 2026-05-24 (1 fonte nova)

- **Segunda fonte de [[drew-huibregtse]] sobre Amazon KDP**: post de 2026-04-23 — overview do sistema de 4 passos com social proof detalhado ($21.626/30 dias, 1 livro). Complementa [[2026-05-09_drew-huibregtse-amazon-kdp]] (pipeline técnico). Retroativamente, a seção "Amazon KDP" em [[estratégia-de-negócios-com-ia]] foi adicionada com o arquétipo completo. Source_count atualizados: [[drew-huibregtse]] 1→2, [[amazon-kdp]] 1→2, [[helium-10]] 1→2, [[estratégia-de-negócios-com-ia]] 28→29.

## Adições da ingestão de 2026-05-20 (4 fontes novas — Daniel Sócrates já ingerido pelo bot)

- **Amazon KDP como arquétipo "low-content digital products"**: [[drew-huibregtse]] introduz primeiro modelo de e-commerce sem produto físico nem supply chain — livros de colorir, journals. Distingue-se de [[shimin-mohammadi]] (Amazon FBA físico) e amplia o cluster e-commerce.
- **Topical authority como 4ª abordagem em [[seo-com-ia]]**: [[matt-diamante]] (findquestions.com → uma página por pergunta) acrescenta dimensão editorial ao cluster SEO já formado por [[brycen-wood]] (técnico), [[daniel-socrates]] (GSC) e guia oficial Google ([[ai-researches-ai]]).
- **Carreira com horizonte de 5 anos**: [[prompt-prism]] é a primeira fonte que organiza carreira em horizonte de 5 anos com framework nominal (Odyssey Plan da Stanford d.school). Complementa Tim Ferriss/[[god-of-prompt]] (DEAL/10 anos) e Naval/[[simplifying-ai]]/[[ai-fied]] (Wealth Protocol).
- **Plugins como remédio de comportamento default**: [[forrest-chang]] (~42k stars no GitHub) é o primeiro autor de plugin Claude Code com tração massiva documentado — corrige 3 falhas crônicas (suposições silenciosas, sobre-engenharia, regressões) que [[boris-cherny]] / CLAUDE.md tentam mitigar via prompt. Divulgado por [[max-kelley]].
- **Padrão "dataset → Claude prioriza"** consolidado: [[google-search-console]] (SEO) + [[helium-10]] (Amazon) + [[google-maps]] ([[derek-gray]]) + balanços ([[faria-lima-elevator]]) = 4 verticais independentes onde Claude opera como **leitor de tabelas estruturadas** copiadas de ferramentas especializadas, não como gerador do zero.
