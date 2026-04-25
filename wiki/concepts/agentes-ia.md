---
title: "Agentes de IA"
type: concept
tags: [agentes-ia, claude-code, automação, multi-agent, subagentes, tokens, ia-empresarial]
source_count: 10
last_updated: 2026-04-25
---

# Agentes de IA

> **Fontes:** 10 | **Domínio:** Arquitetura de sistemas de IA

## Definição

Sistemas baseados em LLMs que executam tarefas de forma autônoma, podendo integrar ferramentas externas, chamar outros agentes e tomar decisões sequenciais sem intervenção humana constante.

## O que foi documentado

### Claude como agente executor (não apenas chat)
[[ross-fledderjohn]] documenta mudança fundamental: Claude está migrando de ferramenta de conversa para ferramenta de delegação de trabalho:
- Antes: "converse com Claude"
- Agora: "atribua trabalho ao Claude"
→ [[2026-04-17_claude-update-task-assignment]]

### Arquitetura multi-agent para branding
[[rafael-brandao]] usa 120+ agentes especializados em pipeline para criar marca completa em 2h:
- Time de Brand → essência da marca
- Time de Copy → textos
- Time de Design → brandbook
→ [[2026-04-14_marca-cloudcode-2horas]]

### Agentes para busca de emprego
[[career-ops]] usa Claude Code para orquestrar pipeline de job search: escaneamento, avaliação, customização de currículo, rastreamento
→ [[2026-04-07_career-ops-busca-emprego-ia]]

### Cursos para aprender a construir agentes
- Nick Saarev: subagentes, agent teams, MCP (4h, YouTube)
- Greg Isenberg: "Building AI Agents that actually work"
- KJ Rainey: "Claude Cowork: Zero to Working AI Employee"
→ [[2026-04-05_5-videos-especialista-claude]]

### Agentes como serviço B2B (AIaaS)
[[bruno-wambier]] formaliza o modelo **Agente-as-a-Service**: IA configurada para atender empresas no WhatsApp — responde clientes, agenda, gera leads, vende — cobrada como assinatura mensal (~R$297/mês/cliente). Primeira menção no wiki a agente IA como **produto comercial empacotado**, não como ferramenta interna.
→ [[2026-04-07_5-negocios-automatizados-ia]]

### Claude Skills como micro-agentes distribuíveis
[[aashish-pahwa]] cataloga 6 skills (Feature Forge, Spec Miner, The Fool, Architecture Designer, API Designer, Microservice Architect) — cada uma opera como micro-agente especializado ativado por frase-gatilho. Marketplaces como [[smithery]] têm 128k+ skills — evidência de ecossistema maduro de agentes compartilháveis.
→ [[2026-04-07_claude-skills-product-managers]]

### Sub-agentes como estratégia de token management
([[nate-herk]], [[2026-04-20_nate-herk-gerenciar-limites-sessao]])

Além de paralelizar trabalho, sub-agentes são uma estratégia primária para economizar tokens:
- Cada sub-agente tem **janela de contexto própria e fresca** — o agente principal não acumula o trabalho interno
- Podem usar modelos mais baratos: *"spin up a sub agent to summarize this using Haiku"*
- Analogia: pesquisador interno — o chefe só recebe o resumo, não lê os 50 artigos junto

Prompt simples de delegação: `"Spin up a sub agent to [tarefa] and make sure that sub agent is using Haiku"`

Dado confirmado por [[yik-chan]] ([[2026-04-16_yik-chan-100-recursos-ocultos-claude]]): a feature "Subagents Parallel" suporta **até 4 agentes simultâneos** em tarefas diferentes com um único comando.

### Meta-skill de descoberta: find-skills

([[pablo-in-public]], [[2026-04-22_pabloinpublic-find-skills]])

Com 128k+ skills publicadas, o gargalo deixou de ser "não existir skills" e passou a ser "não saber qual instalar". A `find-skills` (Vercel Labs) é uma meta-skill que resolve isso: busca entre todas as outras usando linguagem natural dentro do Claude Code, eliminando busca cega e leitura de documentações extensivas.

Padrão novo no wiki: **skill como orquestradora de descoberta de outras skills** — uma camada meta no ecossistema de agentes distribuíveis.

### Dado empírico empresarial: agentic = 71% vs 40%

([[stanford-digital-economy-lab]], [[2026-04-01_enterprise-ai-playbook-stanford]])

Primeiro dado empírico em larga escala no wiki sobre uso agêntico de IA em empresas (51 cases, abr/2026):

| Nível | Definição | % dos casos | Ganho mediano |
|---|---|---|---|
| **Agentic** | Ações autônomas, multi-step, end-to-end sem intervenção | **20%** | **71%** |
| High Automation | IA >80%, humano revisa exceções | 34% | 40% |
| Human-in-Loop | IA + humano em cada output | 46% | 22% |

**Características compartilhadas pelos casos agênticos bem-sucedidos:**
1. Alto volume + repetitivo
2. Critérios de sucesso claros (sim/não)
3. Erros recuperáveis
4. Acesso a dados em múltiplos sistemas

**Caso emblemático**: rede de 25 supermercados com IA agêntica que **substituiu o procurement manager** — prevê demanda, decide o que comprar, quando, de qual fornecedor. Resultado: -40% desperdício, -80% stockouts, EBITDA dobrou. *Pequeno varejista alcançando margens próximas do líder de mercado.*

**Horizonte agêntico crescendo exponencialmente** (METR, fev/2026): janela de tarefas que modelos frontier completam autonomamente **dobra a cada ~7 meses**. Em 2026 chegou a **15 horas de trabalho humano experiente** — habilita mais casos para a coluna agêntica.

Padrão emergente: agentic AI **não é uma nova UI**, é **redefinição do papel de humanos e máquinas** no workflow. Companies passaram a tratar IA como extensão do time, não só ferramenta.

## Fontes

- [[2026-04-17_claude-update-task-assignment]]
- [[2026-04-14_marca-cloudcode-2horas]]
- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-05_5-videos-especialista-claude]]
- [[2026-04-07_5-negocios-automatizados-ia]]
- [[2026-04-07_claude-skills-product-managers]]
- [[2026-04-20_nate-herk-gerenciar-limites-sessao]]
- [[2026-04-22_pabloinpublic-find-skills]]
- [[2026-04-16_yik-chan-100-recursos-ocultos-claude]]
- [[2026-04-01_enterprise-ai-playbook-stanford]]
