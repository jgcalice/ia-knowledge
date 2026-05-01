---
title: "Agentes de IA"
type: concept
tags: [agentes-ia, claude-code, automação, multi-agent, subagentes, tokens, ia-empresarial, claude-managed-agents, agent-teams, git-worktrees, hooks, plugins, skills]
source_count: 16
last_updated: 2026-05-01
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

### CLAUDE.md de Boris Cherny: orquestração como configuração de agente

([[manthan-patel]], [[2026-04-17_manthan-patel-claudemd-boris-cherny]])

[[boris-cherny]] (Anthropic) documenta que sub-agentes no CLAUDE.md têm motivação distinta da economia de tokens de [[nate-herk]]:

- **Contexto limpo**: o agente principal não acumula histórico de trabalho interno dos sub-agentes
- **Paralelismo**: análises e tarefas independentes executadas simultaneamente

Além dos sub-agentes, o arquivo de [[boris-cherny]] codifica um ciclo de autoaperfeiçoamento (auto-improvement loop) como comportamento padrão do agente — atualizar lições e revisar padrões de forma contínua. É o primeiro registro explícito no wiki de um ciclo de melhoria configurado no agente, não só executado manualmente pelo usuário.

**Princípio de impacto mínimo aplicado a agentes autônomos**: "Minimal Impact" — tocar apenas o que a tarefa exige — é especialmente crítico para agentes que operam com Auto Mode, pois reduz o risco de side effects não intencionais em sessões longas sem supervisão.

### Claude Managed Agents: runtime hospedado para agentes com estado

([[ai-updater]], [[2026-04-21_ai-updater-cookbook-agente-dados]])

A Anthropic lançou cookbook oficial demonstrando **Claude Managed Agents** — runtime hospedado que elimina a necessidade de montar stack própria de agentes:

| Conceito | Papel |
|----------|-------|
| **Agent** | Modelo + system prompt + tools + MCP servers + skills |
| **Environment** | Container reutilizável com dependências pré-instaladas (pandas, plotly) |
| **Session** | Instância do agente em execução num environment + arquivos montados |
| **Events** | Troca de mensagens entre app e agente (`user.message`, `agent.message`, tool calls) |

Ferramentas nativas (`agent_toolset_20260401`): `bash`, `read`, `write`, `edit`, `glob`, `grep`, `web_fetch`, `web_search`

**Caso de uso demonstrado**: análise de CSV → relatório HTML interativo com gráficos. Padrão de 5 passos: criar environment → criar agent → upload dataset → criar session + enviar tarefa → stream da execução.

**Impacto arquitetural**: diferente de construir um agente do zero (ferramentas customizadas, gerenciamento de estado manual), Managed Agents fornece plataforma gerenciada com observabilidade nativa via Console (`sessions.events.stream()` mostra tool calls e tokens ao vivo).

### Agent teams: comunicação entre agentes

([[nate-herk]], [[2026-04-27_nate-herk-32-hacks-claude-code]])

Sub-agentes funcionam em paralelo mas **não se comunicam**. Agent teams resolvem isso:
- Todos os agentes do time compartilham task list e podem se comunicar entre si
- Podem atribuir trabalho uns aos outros — não depende do agente principal como intermediário
- É possível falar diretamente com agentes individuais do time, não só com o agente central
- Mais caros e com execução mais longa, mas produzem output mais coeso para projetos grandes e interdependentes

**Distinção clara documentada pela primeira vez no wiki:**
| | Sub-agentes | Agent teams |
|---|---|---|
| Comunicação | Não se comunicam | Comunicam entre si |
| Task list | Cada um tem a sua | Compartilhada |
| Atribuição | Pelo agente central | Qualquer agente pode atribuir |
| Custo | Menor | Maior |
| Melhor para | Tarefas paralelas independentes | Projetos grandes e interdependentes |

### Git worktrees: isolamento por branch para sessões paralelas

([[nate-herk]], [[2026-04-27_nate-herk-32-hacks-claude-code]])

Alternativa/complemento aos sub-agentes para trabalho paralelo no mesmo projeto:
- `claude --work-tree [nome-feature]` cria workspace isolado em branch próprio (eficiente — não copia a pasta)
- Abrir outro terminal com nome de feature diferente = branch diferente, sem conflito
- 3–5 sessões paralelas no mesmo projeto sem sobrescrever trabalho uma da outra
- Merge das branches ao terminar — fluxo Git padrão

**Distinção vs sub-agentes**: worktrees isolam **por branch** (arquivos do filesystem); sub-agentes isolam **por contexto** (janela de tokens). Usos complementares, não excludentes.

### Pipeline de vendas agêntico: SDR + Analisador + Consultor

([[jordan-lee]], [[2026-04-15_jordan-lee-vendas-sistema-ia]])

Primeiro sistema do wiki com **três agentes especializados em sequência cobrindo um funil comercial completo**:

| Agente | Input | Output | Papel no funil |
|--------|-------|--------|---------------|
| **AI SDR** | Lista de prospects | Chamada agendada | Topo — outreach e qualificação |
| **Sales Call Analyzer** | Gravação da chamada | Relatório: dores, objeções, posicionamento do follow-up | Meio — inteligência pós-chamada |
| **AI Consultant** | Transcript da chamada | Proposta personalizada com solução mapeada | Fundo — fechamento |

Padrão convergente com [[stanford-digital-economy-lab]]: os casos agênticos mais eficazes têm critérios de sucesso claros, alto volume, erros recuperáveis e acesso a dados em múltiplos sistemas — todas as características presentes aqui.

**Distinção em relação a AIaaS de [[bruno-wambier]]**: aquele usa agente de WhatsApp como produto empacotado (resposta a clientes existentes); este usa pipeline de agentes para **adquirir novos clientes** — o funil de aquisição é agêntico, não só a entrega.

### Multi-agent debate para trading: TradingAgents

([[paras-madan]], [[2026-04-30_paras-madan-repos-monetizacao]])

[[tradingagents]] é o maior projeto open-source agêntico por stars documentado no wiki (55.700 stars). Diferente dos sistemas anteriores, onde agentes executam tarefas em sequência ou paralelo, aqui o mecanismo central é o **debate**:

- Agentes especializados (fundamentos, sentimento, técnica, gestão de risco) discutem em tempo real
- O consenso emergente via debate — não o output de um agente único — é a decisão de trading
- Suporte multi-plataforma: DeepSeek, Gemini, Anthropic, Qwen, Azure
- `pip install tradingagents`

**HKUDS/AI-Trader** complementa como plataforma: qualquer agente IA se integra lendo um arquivo `SKILL.md` — protocolo análogo ao CLAUDE.md de [[boris-cherny]], mas para sistemas de trading. Backend FastAPI mantém dashboard de preços e histórico de lucros ao vivo.

**Padrão novo**: SKILL.md como **protocolo de integração de agentes em sistemas financeiros** — o arquivo define as capacidades do sistema e qualquer agente que o leia pode participar imediatamente.

### Agent Development Kit: arquitetura em 5 camadas

([[manthan-patel]], [[2026-04-30_manthan-patel-agent-development-kit]])

Primeira taxonomia completa de infraestrutura de agente documentada no wiki — 5 camadas com localização, função e artefatos próprios:

| Camada | Nome | Papel | Onde vive |
|--------|------|-------|-----------|
| 1 | **CLAUDE.md** | Memória/Constituição — carregado sempre, define regras e convenções | `~/.claude/CLAUDE.md` (global) + `.claude/CLAUDE.md` (projeto) |
| 2 | **Skills** | Conhecimento modular — ativado por description-matching, carregado só quando necessário | `~/.claude/skills/` |
| 3 | **Hooks** | Controle determinístico — shell scripts (não-IA) disparados em eventos de agente | Scripts com matcher + command |
| 4 | **Subagents** | Delegação — contexto próprio e fresco; pai só vê o resultado final | Arquivo `*.md` de definição por papel |
| 5 | **Plugins** | Distribuição — pacote npm com manifest.json; agrupa skills + agents + hooks + commands | `plugin.json` → npm |

**Hooks — detalhe técnico (inédito no wiki):**

Cinco tipos de evento disponíveis: `PreToolUse.sh`, `PostToolUse.sh`, `SessionStart.sh`, `Stop.sh`, `SubagentStop.sh`. Cada hook tem um matcher (padrão de chamada de ferramenta — wildcard, regex ou exato) e um command (shell script que define a regra). É a camada que converte intenções em obrigações — o agente não escolhe, o sistema força.

**Distinção Skills vs Subagents**: Skills injetam contexto na sessão principal (o agente principal executa com mais conhecimento); Subagents criam uma sessão filho isolada que retorna uma única mensagem. São complementares: uma skill pode instruir como delegar, um subagent executa a delegação.

**Plugins como ecossistema distribuível**: a analogia npm é intencional — skills e agentes viram artefatos versionados, assinados e instaláveis por toda a equipe. Complementa o marketplace [[smithery]] (128k+ skills): smithery é a camada de descoberta, plugins são a camada de distribuição interna.

## Fontes

- [[2026-04-30_manthan-patel-agent-development-kit]]
- [[2026-04-30_paras-madan-repos-monetizacao]]
- [[2026-04-15_jordan-lee-vendas-sistema-ia]]
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
- [[2026-04-21_ai-updater-cookbook-agente-dados]]
- [[2026-04-17_manthan-patel-claudemd-boris-cherny]]
- [[2026-04-27_nate-herk-32-hacks-claude-code]]
