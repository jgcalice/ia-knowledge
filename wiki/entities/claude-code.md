---
title: "Claude / Claude Code"
type: entity
category: tool
tags: [llm, claude, anthropic, claude-code, ia, claude-managed-agents]
source_count: 35
last_updated: 2026-05-01
---

# Claude / Claude Code

> **Categoria:** Ferramenta — LLM | **Fabricante:** Anthropic | **Aparece em:** 5 fontes

## O que é

Claude é o modelo de linguagem da Anthropic. Claude Code (referido nos posts como "Cloud Code" ou "CloudCode") é a interface CLI/agente do Claude, capaz de executar código, integrar ferramentas via conectores e fazer scraping. Nas fontes deste wiki, é a ferramenta central em quase todos os workflows.

## Modelos mencionados

| Modelo | Características (conforme [[2026-04-18_7-hacks-tokens-claude]]) |
|--------|----------------------------------------------------------------|
| Haiku | Tarefas simples, classificação, formatação, alto volume |
| Sonnet | Código, análise de dados, Q&A geral — melhor custo-benefício |
| Opus | Arquitetura complexa, debugging profundo, escrita longa — ~5x mais caro que Sonnet |

## Usos documentados no wiki

- **Geração de leads via Google Maps** — com [[api-file]] ([[lucas-garcia-pit]]) e [[apify]] ([[hudson-brendon]])
- **Otimização de perfil LinkedIn** — via prompts estruturados ([[bruno-souza]])
- **Interpretação de documentos** — com pré-processamento via [[markitdown]] ([[rafael-brandao]])
- **Busca de emprego automatizada** — sistema Career Ops avalia 700+ vagas e gera currículos ATS ([[2026-04-07_career-ops-busca-emprego-ia]])
- **Redesenho de carreira** — prompts Tim Ferriss e Naval Ravikant para estratégia de riqueza ([[god-of-prompt]], [[simplifying-ai]])
- **Certificação Architect** — exame formal da Anthropic para AI Engineering ([[bashiri]])
- **Criação de marca completa** — 120+ agentes em pipeline para branding em 2h ([[rafael-brandao]])
- **SEO com IA** — criação de llms.txt e Markdown mirrors para ranking no Google ([[brycen-wood]])
- **Estratégia de negócios** — 7 prompts para análise de mercado, oferta e escalonamento ([[evolving-ai]], [[business-bulls]])
- **Monetização de skills** — prompts para identificar o que vender e plano de 20 dias ([[sabrina-ramonov]])
- **Memória infinita via grafo** — instalação do [[graphify]] mapeia o workspace em grafo de conhecimento → 71,5x menos tokens por sessão ([[marc-cleroux]])
- **Descoberta de skills** — `find-skills` (Vercel Labs): meta-skill instalada via `npx` que busca entre milhares de skills publicadas no GitHub usando linguagem natural ([[pablo-in-public]])
- **Prospecção via Conector** — uso dos Conectores do Claude.ai + [[vibe-prospecting]] para gerar listas de leads por nicho/cargo/cidade, 100% gratuito via browser ([[eduardo-santos]])
- **Produtividade diária sem CLI** — uso conversacional do Claude para emails, resumo de PDFs, tone setting e outros 20+ casos de uso sem instalação ([[yik-chan]])
- **Análise de dados automática** — cookbook oficial da Anthropic: upload CSV → Claude Managed Agents gera relatório HTML interativo com gráficos via `agent_toolset_20260401` ([[ai-updater]])
- **Candidaturas personalizadas** — análise de job descriptions + reescrita de currículo + geração de cover letter por vaga; caso documentado: 6 entrevistas em 7 dias ([[coding-ai-fullstack]])

## Modos de operação

| Modo | Como ativar | Comportamento |
|------|-------------|---------------|
| Auto Mode | `Shift+Tab` 3x no CLI | Claude decide permissões autonomamente — permite sessões contínuas de horas sem interrupção. Recomendado como padrão. |
| Accept Edits | `Shift+Tab` 2x | Aceita edições automaticamente, mas ainda pede aprovação para ações maiores |
| Default | padrão | Pede aprovação a cada passo |

Documentado por [[alex-finn]] em [[2026-04-18_alex-finn-dicas-claude-code]].

## Níveis de esforço (/effort)

Configurado via `/effort` (Boris Cherny / [[alex-finn]]):

| Nível | Quando usar |
|-------|-------------|
| max | Prompt inicial de kickoff de app (frontload completo) |
| extra high | Maioria das tarefas de desenvolvimento |
| high / medium / low | Planos baratos ou tarefas triviais (ex: mudar cor de botão) |

## Adaptive Thinking (Opus 4.7)

Opus 4.7 **removeu o toggle de extended thinking** do Opus 4.6. O controle de profundidade de raciocínio agora é feito via prompt:
- Tarefa complexa: `"think carefully step by step"`
- Tarefa simples: `"prioritize responding quickly rather than thinking deeply"`

Os dois eixos de controle são independentes: `/effort` controla duração total na tarefa; instrução de thinking controla profundidade por microtarefa.

## Comandos built-in (pouco conhecidos)

Documentados por [[sal-shirgaleev]] em [[2026-04-22_sal-shirgaleev-5-comandos-claude]] e [[alex-finn]] em [[2026-04-18_alex-finn-dicas-claude-code]]:

| Comando | Função |
|---------|--------|
| `/init` | Escaneia o projeto e gera CLAUDE.md automaticamente com contexto, convenções e estrutura |
| `#` | Adiciona regra permanente ao rulebook pessoal em 3 segundos (ex: `# Never use var`) |
| `/review` | Auditoria completa do codebase: bugs, edge cases, segurança, code smell |
| `/plan` | Gera mapa de execução (etapas, arquivos, decisões) antes de escrever qualquer código |
| `/compact` | Comprime o histórico da sessão sem perder intenção — evita "esquecimento" em sessões longas |
| `/recap` | Gera resumo de uma linha de tudo que o agente fez na sessão — útil ao retomar sessões longas |
| `/effort` | Configura o nível de esforço por tarefa (low/medium/high/extra high/max) |
| `/re` (Rewind) | Pula para qualquer mensagem anterior e descarta tudo depois; inclui opção "summarize from here" para handoff |
| `/btw` | Overlay para perguntas rápidas que **não entram no histórico** da sessão — mantém contexto limpo |
| `/context` | Mostra o consumo atual de tokens na sessão em percentuais por fonte (system prompts, arquivos, MCP servers) |
| `/voice` | Comando nativo de voz (em rollout); permite ditar instruções direto no terminal |
| `/loop` | Executa um prompt em intervalo recorrente em background; alerta só quando precisa de input; dura até 3 dias |
| `/hooks` | Configura hooks de notificação (ex: som ao terminar sessão) em linguagem natural |

## Segurança ao usar Claude Code

Documentado por [[lucas-garcia-pit]] em [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]]:

- API keys nunca no front-end — sempre no servidor
- RLS (Row Level Security) ativo no Supabase — cada usuário vê apenas seus dados
- Lógica de preço, pagamento e regras de negócio exclusivamente no servidor
- Rate limiting por usuário/minuto nas APIs
- Webhooks com assinatura verificada (zero trust no cliente)

> Ver conceito completo: [[segurança-com-ia]]

## Boas práticas identificadas

- Dar contexto completo sobre o projeto e ICP antes de iniciar scraping de leads
- Usar o mesmo chat para evitar repetição de leads já capturados
- Escolher o modelo certo para cada tarefa (ver tabela acima)
- Usar `/compact` para compactar sessões longas antes de iniciar novo chat (comando built-in)
- Usar `/plan` antes de qualquer feature para evitar retrabalho por desalinhamento
- Ativar Auto Mode para evitar interrupções constantes de permissão em sessões longas
- Frontloading: enviar todas as instruções de uma vez em projetos novos, em vez de incrementalmente
- Configurar notificações via prompt: `"after every piece of work you do, please send me a notification"`
- Session handoff a ~12% da janela (120k/1M no Opus): resumo → `/clear` → nova sessão — [[nate-herk]]
- Subagents Parallel: um único comando pode disparar até 4 agentes trabalhando em tarefas diferentes simultaneamente — [[yik-chan]] confirma dado de [[nate-herk]]
- Usar `/re` (Rewind) após tentativas falhas para não deixar código errado no contexto
- Usar `/btw` para perguntas rápidas sem poluir o histórico da sessão
- Manter CLAUDE.md sob 200 linhas / ~2.000 tokens — carrega a cada sessão, bloat é custo constante
- Usar `.claudeignore` para excluir pastas/arquivos irrelevantes do repo
- Sessions chaining: sessão de discovery → sessão de planning → sessão de execution
- CLAUDE.md de [[boris-cherny]]: codificar Workflow Orchestration + Task Management + Core Principles no arquivo de configuração transforma o agente de "respondedor" em "executor autônomo estruturado"
- Git worktrees: `claude --work-tree [nome-feature]` cria workspace isolado em branch próprio; permite 3–5 sessões paralelas no mesmo projeto sem conflito — [[nate-herk]]
- Compact em ~60% (não esperar estourar); ao compactar, especificar o que preservar: `"/compact, mas mantém decisões de API"` — [[nate-herk]]
- Ultra think: digitar `ultra think` no prompt aloca orçamento máximo de thinking (~32.000 tokens); usar para arquitetura, debugging complexo, refatorações grandes — [[nate-herk]]
- Editar permissões explicitamente (allow list + deny list) como alternativa ao `--dangerously-skip-permissions`; deny list tem prioridade sobre allow list — [[nate-herk]]
- Screenshot self-check loop: build → screenshot → analizar → iterar; 3 passes antes do V1 entregue — [[nate-herk]]
- Agent teams: distintos de sub-agentes — agentes do time comunicam entre si, compartilham task list e podem atribuir trabalho uns aos outros — [[nate-herk]]
- Context7 MCP: injeta documentação atualizada e version-specific de libs no contexto antes de gerar código; resolve problema de training cutoff — [[context7]] via [[nate-herk]]

## Fontes

- [[2026-03-19_leads-infinitos-cloudcode]]
- [[2026-03-28_prospecção-leads-claude-apify]]
- [[2026-04-11_transformacao-linkedin-ia]]
- [[2026-04-11_tokens-markdown]]
- [[2026-04-18_7-hacks-tokens-claude]]
- [[2026-02-25_idea-reality-mcp]]
- [[2026-03-11_ferramentas-dev-essenciais]]
- [[2026-03-22_redesenho-carreira-tim-ferriss]]
- [[2026-03-24_aprender-com-claude-6-prompts]]
- [[2026-03-26_certificacao-claude-architect]]
- [[2026-04-01_claude-fundador-startup-7-prompts]]
- [[2026-04-05_5-videos-especialista-claude]]
- [[2026-04-07_career-ops-busca-emprego-ia]]
- [[2026-04-11_seo-3-arquivos]]
- [[2026-04-14_marca-cloudcode-2horas]]
- [[2026-04-15_leads-qualificados-claudecode]]
- [[2026-04-16_wealth-protocol-naval]]
- [[2026-04-17_claude-update-task-assignment]]
- [[2026-04-17_prompts-renda-rapida]]
- [[2026-04-20_claude-ceo-7-prompts]]
- [[2026-04-12_graphify-memoria-infinita-claude]]
- [[2026-04-14_eduardo-santos-vibe-prospecting]]
- [[2026-04-22_sal-shirgaleev-5-comandos-claude]]
- [[2026-04-18_alex-finn-dicas-claude-code]]
- [[2026-04-20_nate-herk-gerenciar-limites-sessao]]
- [[2026-04-22_pabloinpublic-find-skills]]
- [[2026-04-16_yik-chan-100-recursos-ocultos-claude]]
- [[2026-04-21_ai-updater-cookbook-agente-dados]]
- [[2026-04-17_manthan-patel-claudemd-boris-cherny]]
- [[2026-04-26_coding-ai-fullstack-entrevistas-claude]]
- [[2026-04-27_nate-herk-32-hacks-claude-code]]
