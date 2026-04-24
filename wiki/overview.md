---
title: "Overview — IA Knowledge Base"
type: overview
last_updated: 2026-04-24
source_count: 38
---

# Overview — IA Knowledge Base

> Wiki iniciado em 2026-04-21 | 38 fontes ingeridas | Domínio: IA Aplicada a Negócios, Carreira, Gestão e Produto

## Tese atual

O conteúdo de IA consumido até agora orbita em torno de **quatro domínios práticos**:

1. **Como gerar mais leads com menos esforço** — usando LLMs + scraping de Google Maps e APIs
2. **Como usar Claude de forma mais eficiente** — reduzindo consumo de tokens e escolhendo ferramentas certas
3. **Como acelerar carreira e aumentar renda** — LinkedIn, busca de emprego automatizada, certificações, redesenho estratégico
4. **Como construir negócios com IA** — estratégia de mercado, branding, SEO e automação de processos

---

## Clusters de conhecimento

### Cluster 1: Geração de Leads com IA
**Conceito central:** [[geração-de-leads-com-ia]]

Três métodos documentados, padrão similar, ferramentas diferentes:
- **Método 1**: [[claude-code]] + [[api-file]] → [[google-maps]] → leads enriquecidos ([[lucas-garcia-pit]])
- **Método 2**: [[claude-code]] + [[apify]] → [[google-maps]] → leads organizados ([[hudson-brendon]])
- **Método 3**: Skill "lista de alto valor" + API → leads com dados completos incluindo LinkedIn ([[flavio-rafael]])
- **Método 4**: [[vibe-prospecting]] (Conector Claude.ai web) + prompt → leads por nicho/cargo/cidade, gratuito e sem CLI ([[eduardo-santos]])

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
| Redesenho estratégico | 4 prompts Tim Ferriss: vantagem injusta, DEAL, freedom ratio, 10 anos | [[god-of-prompt]] |
| Monetização imediata | 4 prompts para ganhar $1k em 30 dias com skills existentes | [[sabrina-ramonov]] |
| Certificação formal | Claude Certified Architect (grátis, proctored, valorizado pela Deloitte) | [[bashiri]] |
| Filosofia de riqueza | 6 prompts Naval Ravikant — parar de trocar tempo por dinheiro | [[god-of-prompt]] |

---

### Cluster 7: Segurança no Desenvolvimento com IA (novo)
**Conceito central:** [[segurança-com-ia]]

- 5 fundamentos de segurança para apps construídos com Claude Code: API keys no servidor, RLS no Supabase, lógica sensível no back-end, rate limiting e webhooks com assinatura verificada ([[lucas-garcia-pit]])
- Tese central: o risco não é a ferramenta (Claude Code), mas o dev que acelera sem fundamentos de back-end

---

### Cluster 4: Negócios e Estratégia com IA
**Conceito central:** [[estratégia-de-negócios-com-ia]]

- 5 prompts para validar idea de startup com framework Paul Graham: pressure test → problema real → concorrentes → primeiros 10 clientes → MVP em 2 semanas ([[harry]])
- 7 prompts para análise de mercado, oferta e escalonamento ([[evolving-ai]], [[business-bulls]])
- Branding completo em 2h com 120+ agentes ([[rafael-brandao]])
- SEO na primeira página do Google com 3 arquivos de texto ([[brycen-wood]])
- 5 modelos nativos de IA (eBook, YouTube narrado, newsletter, curso online, agente WhatsApp como AIaaS) ([[bruno-wambier]])
- Mini web app focado + Instagram como canal único ([[luna-vega]])
- AI Agency (Dan Martell, Liam Ottley) — agência automatiza outras empresas ([[paul-hilse]])
- Stack de 5 skills open-source para founder solo: Meta Ads + Position Me + LinkedIn Post Generator + Reddit ICP Monitor + Google Trends SEO ([[paras-madan]])

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

## Mapa de entidades

**Ferramentas e plataformas**: [[claude-code]] · [[claude-skills]] · [[smithery]] · [[apify]] · [[api-file]] · [[markitdown]] · [[linkedin]] · [[google-maps]] · [[career-ops]] · [[graphify]] · [[obsidian]] · [[vibe-prospecting]]

**Referências externas**: [[paul-graham]]

**Conceitos de segurança**: [[segurança-com-ia]]

**Pessoas (BR)**: [[lucas-garcia-pit]] · [[hudson-brendon]] · [[bruno-souza]] · [[rafael-brandao]] · [[flavio-rafael]] · [[rony-meisler]] · [[bruno-wambier]] · [[adriano-couto]] · [[eduardo-santos]] · [[castilho]]

**Pessoas (Internacional)**: [[evolving-ai]] · [[god-of-prompt]] · [[bashiri]] · [[sabrina-ramonov]] · [[ross-fledderjohn]] · [[michael-kocher]] · [[brandon-lew]] · [[usama-akram]] · [[brycen-wood]] · [[business-bulls]] · [[aashish-pahwa]] · [[luna-vega]] · [[paul-hilse]] · [[marc-cleroux]] · [[andrej-karpathy]] · [[alex-finn]] · [[nate-herk]] · [[pablo-in-public]] · [[sanskaar-singh]] · [[arshman-khalid]] · [[paras-madan]] · [[harry]]

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
- **Arquétipos de negócio se multiplicando**: já mapeamos 5 — consultoria estratégica, infoprodutos nativos, mini web app + Instagram, AI Agency, stack de skills para founder solo ([[paras-madan]]). Nenhum é "IA só como ferramenta" — todos são **produtos/serviços nascidos da IA**
- **Skills como equipe virtual distribuível**: [[paras-madan]] expande o padrão de [[aashish-pahwa]] (skills para PMs) para canais de crescimento — o founder substitui media buyer, CRO consultant, copywriter, community manager e SEO analyst com 5 skills open-source
- **Claude Code como agente autônomo**: Auto Mode + Frontload + Notificações mudam o paradigma de "babysitting" (aprovação constante) para "delegação real" — o agente trabalha horas sem supervisão ([[alex-finn]])
- **Segurança como ponto cego do desenvolvimento com IA**: Claude Code acelera tanto o desenvolvimento que devs pulam fundamentos clássicos de back-end (RLS, rate limit, server-side secrets) — [[lucas-garcia-pit]] documenta os 5 mais críticos
- **Validação como etapa anterior à estratégia**: o framework [[paul-graham]] (via [[harry]]) documenta a camada pré-estratégia — testar ideia antes de qualquer planejamento de mercado; complementa os 7 prompts de [[evolving-ai]] / [[business-bulls]] que começam depois que o produto existe

---

## Status do wiki

| Tipo | Quantidade |
|------|-----------|
| Fontes ingeridas | 38 |
| Páginas de fontes | 38 |
| Páginas de conceitos | 10 |
| Páginas de entidades | 49 |
| Páginas de síntese | 1 |
| **Total de páginas** | **98** |
