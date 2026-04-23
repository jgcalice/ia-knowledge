---
title: "Overview — IA Knowledge Base"
type: overview
last_updated: 2026-04-23
source_count: 30
---

# Overview — IA Knowledge Base

> Wiki iniciado em 2026-04-21 | 30 fontes ingeridas | Domínio: IA Aplicada a Negócios, Carreira, Gestão e Produto

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

---

### Cluster 3: Carreira e LinkedIn com IA
**Conceito central:** [[carreira-com-ia]]

Sistema completo documentado — da visibilidade à estratégia de longo prazo:

| Camada | O que faz | Fonte |
|--------|-----------|-------|
| Visibilidade (LinkedIn) | 5 prompts para reescrever headline, about, skills, experiência | [[bruno-souza]] |
| Busca automatizada | Career Ops: 700+ vagas avaliadas, currículo ATS por vaga | [[career-ops]] |
| Redesenho estratégico | 4 prompts Tim Ferriss: vantagem injusta, DEAL, freedom ratio, 10 anos | [[god-of-prompt]] |
| Monetização imediata | 4 prompts para ganhar $1k em 30 dias com skills existentes | [[sabrina-ramonov]] |
| Certificação formal | Claude Certified Architect (grátis, proctored, valorizado pela Deloitte) | [[bashiri]] |
| Filosofia de riqueza | 6 prompts Naval Ravikant — parar de trocar tempo por dinheiro | [[god-of-prompt]] |

---

### Cluster 4: Negócios e Estratégia com IA
**Conceito central:** [[estratégia-de-negócios-com-ia]]

- 7 prompts para análise de mercado, oferta e escalonamento ([[evolving-ai]], [[business-bulls]])
- Branding completo em 2h com 120+ agentes ([[rafael-brandao]])
- SEO na primeira página do Google com 3 arquivos de texto ([[brycen-wood]])
- 5 modelos nativos de IA (eBook, YouTube narrado, newsletter, curso online, agente WhatsApp como AIaaS) ([[bruno-wambier]])
- Mini web app focado + Instagram como canal único ([[luna-vega]])
- AI Agency (Dan Martell, Liam Ottley) — agência automatiza outras empresas ([[paul-hilse]])

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

**Pessoas (BR)**: [[lucas-garcia-pit]] · [[hudson-brendon]] · [[bruno-souza]] · [[rafael-brandao]] · [[flavio-rafael]] · [[rony-meisler]] · [[bruno-wambier]] · [[adriano-couto]] · [[eduardo-santos]]

**Pessoas (Internacional)**: [[evolving-ai]] · [[god-of-prompt]] · [[bashiri]] · [[sabrina-ramonov]] · [[ross-fledderjohn]] · [[michael-kocher]] · [[brandon-lew]] · [[usama-akram]] · [[brycen-wood]] · [[business-bulls]] · [[aashish-pahwa]] · [[luna-vega]] · [[paul-hilse]] · [[marc-cleroux]] · [[andrej-karpathy]] · [[alex-finn]]

---

## Padrões emergentes

- **Claude como orquestrador**: em todas as fontes, Claude/Claude Code é o centro — não apenas chatbot, mas agente que integra ferramentas externas
- **Carreira com IA é tema central**: 7 das 21 fontes abordam diretamente carreira, LinkedIn ou renda — é o segundo maior cluster
- **Combinação de skills > skill isolada**: padrão recorrente em múltiplas fontes independentes
- **Ação antes de planejamento**: "stop planning, start selling" / "just go build it" — mensagem anti-procrastinação dominante
- **Tokens como recurso escasso**: três fontes abordam → evidência de preocupação real dos usuários
- **Conteúdo duplicado confirmado**: prompts de estratégia de negócios aparecem idênticos em [[evolving-ai]] e [[business-bulls]] — sinal de que são referência consolidada
- **Palavras-gatilho como novo padrão**: [[adriano-couto]] introduz MECE/5 Whys/Invert/ELI5/Artefato como ativadores semânticos — uma palavra muda o pipeline de resposta do Claude, sem precisar explicar o framework
- **Skills formalizam os gatilhos**: [[aashish-pahwa]] + [[smithery]] mostram ecossistema de ~128k Claude Skills — a palavra-gatilho artesanal virou pacote distribuível
- **Arquétipos de negócio se multiplicando**: já mapeamos 4 — consultoria estratégica, infoprodutos nativos, mini web app + Instagram, AI Agency. Nenhum é "IA só como ferramenta" — todos são **produtos/serviços nascidos da IA**
- **Claude Code como agente autônomo**: Auto Mode + Frontload + Notificações mudam o paradigma de "babysitting" (aprovação constante) para "delegação real" — o agente trabalha horas sem supervisão ([[alex-finn]])

---

## Status do wiki

| Tipo | Quantidade |
|------|-----------|
| Fontes ingeridas | 28 |
| Páginas de fontes | 28 |
| Páginas de conceitos | 9 |
| Páginas de entidades | 35 |
| Páginas de síntese | 1 |
| **Total de páginas** | **73** |
