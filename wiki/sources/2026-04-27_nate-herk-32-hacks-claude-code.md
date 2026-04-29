---
title: "32 Hacks do Claude Code — do Iniciante ao Pro"
type: source
source_file: "2026-04-27_nate_herk_ai_automation_jqoFP9QapXI.md"
author: "@Nate Herk | AI Automation"
date: 2026-04-27
format: video
tags: [claude-code, hacks, produtividade, tokens, agentes-ia, git, prompt-engineering, mcp, automação]
source_url: "https://youtu.be/jqoFP9QapXI?si=vu594vJhU5INpuYg"
source_count: 1
---

# 32 Hacks do Claude Code — do Iniciante ao Pro

> **Fonte:** [[2026-04-27_nate_herk_ai_automation_jqoFP9QapXI]] | **Autor:** @Nate Herk | AI Automation | **Data:** 2026-04-27 | **Formato:** Vídeo YouTube (975s) | **[↗ Ver vídeo](https://youtu.be/jqoFP9QapXI?si=vu594vJhU5INpuYg)**

## TL;DR

Guia completo de 32 hacks do Claude Code organizado em três níveis — iniciante, intermediário e pro — cobrindo gestão de contexto, produtividade, automação, segurança e arquitetura de agentes.

## Contexto

Nate Herk (@Nate Herk | AI Automation) é criador de conteúdo focado em automação com IA e operador de comunidade no Skool (AI Automation Society). Este vídeo documenta 32 hacks que ele usa no dia a dia, ordenados do básico ao avançado. É a segunda fonte de Nate Herk no wiki — a primeira ([[2026-04-20_nate-herk-gerenciar-limites-sessao]]) focava em gestão de sessão; esta é mais abrangente.

## O que foi ensinado

### Nível Iniciante (Hacks 1–10)

**1. /init em todo projeto**
- Escaneia o codebase e gera `CLAUDE.md` automaticamente (arquitetura, convenções, arquivos-chave)
- Para projetos novos: pedir ao Claude para criar o arquivo explicando objetivo, stack e regras

**2. Status line**
- `/statusline` cria script que fica na base do terminal mostrando modelo, % de contexto, custo
- Mini dashboard de sessão — sempre saber quanto contexto resta para evitar context rot

**3. Voice input**
- `/voice` comando nativo (em rollout); alternativa: app de voice-to-text (ex: Glaido)
- Permite ditar para o terminal e ter código gerado em tempo real

**4. Manter contexto pequeno**
- Dar ao Claude apenas o que é necessário para a tarefa atual
- Quebrar problemas grandes em etapas pequenas e focadas

**5. /context para diagnosticar token bloat**
- Mostra exatamente o que está consumindo tokens em percentuais: system prompts, conteúdo de arquivos, MCP servers
- Permite investigar e reestruturar quando a sessão está inchada

**6. Compact em 60% e /clear entre tarefas**
- Usar `/compact` quando o contexto atingir ~60% (não esperar estourar)
- Pode especificar o que preservar: `"/compact, mas mantém todas as decisões de integração de API"`
- Usar `/clear` ao trocar de tarefa completamente (CLAUDE.md e arquivos ainda persistem)

**7. Sempre começar em plan mode**
- `Shift+Tab` para ciclar entre modos; plan mode: Claude lê, pesquisa, mas não escreve código
- Claude mapeia etapas, faz perguntas, alinha abordagem antes de qualquer linha de código
- Reduz drasticamente o retrabalho por desalinhamento

**8. Tratar Claude como desenvolvedor júnior**
- Dar problemas, não comandos diretos: "Como devemos tratar o rastreamento de crescimento?" vs "Escreva uma função que faça X"
- Quando Claude faz suposições e raciocina, a qualidade melhora — ele pensa antes de agir

**9. Fazer Claude fazer perguntas**
- Invocar a ferramenta `ask user question`: "Faça perguntas continuamente até ter 95% de certeza do que preciso"
- Alinhamento pré-execução elimina rodadas de revisão desnecessárias

**10. Auto-verificação nos to-do lists**
- Bake verification steps no plano: `1. Construir site → 2. Tirar screenshot e checar → 3. Abrir DevTools e verificar erros`
- Instrução complementar: "Não avance para o próximo to-do até ter 95% de confiança que o atual está correto"

### Nível Intermediário (Hacks 11–22)

**11. Sub-agentes para trabalho paralelo**
- Claude spin up sub-agentes isolados com contexto próprio e modelo próprio
- Thread principal fica limpa; sub-agentes pesquisam, escrevem testes, exploram abordagens em paralelo
- Ao terminar, reportam ao agente principal — como ter uma equipe de desenvolvedores

**12. Skills customizadas**
- Criar arquivos de prompt reutilizáveis em `.cloud/skills/` (ex: `techdebt.md`, `codereview.md`)
- Invocar por linguagem natural ou comando `/`; executam workflow completo e consistente
- Commitar no GitHub → toda a equipe acessa; automatiza SOPs

**13. Haiku para sub-agentes**
- Para tarefas simples ou processamento de grande volume de dados, usar Haiku nos sub-agentes
- Exemplos: scraping de artigos, leitura de centenas de milhares de tokens → só o resumo volta ao Opus
- Não faz sentido usar modelo pesado onde só alguns dados são necessários

**14. Atualizar CLAUDE.md constantemente**
- Logar novos padrões, gotchas e convenções descobertos durante a sessão
- Manter entre **150–200 linhas máx** — bloat = custo constante a cada sessão
- Quando ultrapassar o limite: trim

**15. CLAUDE.md apontando para outros arquivos**
- Manter o CLAUDE.md lean: apontar para arquivos externos (style guides, business context, ref docs)
- Claude sabe *onde buscar* sem *carregar* tudo no contexto da sessão

**16. Sair cedo e re-prompar**
- Se Claude começar a ir pelo caminho errado: `Escape` → corrigir → re-prompar
- Tokens gastos na direção errada = contexto desperdiçado; esterçar cedo e cedo

**17. Desafiar outputs agressivamente**
- Push back: "Rasga isso. Faça uma versão mais elegante." / "Não é suficiente. Tente com uma abordagem completamente diferente."
- Segunda tentativa com barra alta geralmente produz output dramaticamente melhor
- Ao receber algo melhor: mandar atualizar a skill ou o CLAUDE.md para não repetir o erro

**18. /rewind para desfazer rapidamente**
- Volta para ponto anterior da conversa sem reiniciar; rápido e limpo

**19. Hooks para notificações**
- `/hooks` para configurar notificação de conclusão de sessão (em linguagem natural)
- Permite trabalhar com 15 sessões simultâneas — som = alguma precisa de input

**20. Screenshots**
- Claude pode ver; usos: erros de UI, sites de inspiração, self-check loop
- Loop de self-check: construir → screenshot → analisar → implementar mudanças → repetir (3 passes antes do V1)
- "O V1 que ele me dá agora é muito melhor do que antes"

**21. Chrome DevTools**
- Claude abre browser, interage com app, verifica funcionalidade, preenche formulários
- Para front-end: verificar botões e erros funcionais (vs screenshot que é visual)

**22. Clonar sites de inspiração**
- Feed de screenshots de sites favoritos: "Faça parecer com isto"
- Claude recria padrões de design sem o "slop" genérico de IA
- Alternativa: pegar HTML/CSS do site como template e dar toque próprio

### Nível Pro (Hacks 23–32)

**23. Sessões paralelas com Git worktrees**
- `claude --work-tree [nome-da-feature]` → cria workspace isolado em branch próprio
- Duas+ sessões no mesmo projeto sem sobrescrever trabalho uma da outra
- 3–5 sessões paralelas possíveis; merge normal ao terminar

**24. Endpoints de API em vez de MCP servers**
- MCP carrega *todas* as definições de tools no contexto; para casos simples, é desperdício
- Hardcodar endpoint direto quando só uma operação é necessária (ex: ler um banco Notion)
- Economia de tokens significativa em projetos de escopo limitado

**25. /loop para tarefas recorrentes**
- Ex: "A cada 5 minutos, cheque o status do deploy"
- Roda em background, interrompe apenas quando algo precisa de atenção
- Reminders one-time: "Me lembre às 15h de checar X"
- Caveat: loops duram até 3 dias; para automações mais longas → usar desktop scheduled tasks (nova sessão a cada disparo, sem memória de contexto)

**26. Hospedar em VPS para sessões always-on**
- Claude Code em servidor remoto → fica rodando com laptop fechado
- SSH para interagir; controle via Telegram a qualquer momento

**27. Controle remoto pelo celular**
- Feature nova: controlar sessões locais pelo phone ou qualquer browser
- Código permanece na máquina local; conexão remota só no celular
- Iniciar task no desktop → continuar do celular em movimento

**28. BigQuery BQ tool — analytics sem SQL**
- Conectar CLI tools (ex: BQ do BigQuery) ao Claude Code
- Perguntas em linguagem natural → query → resposta; sem SQL manual
- Funciona para qualquer ferramenta CLI-based

**29. Ultra think**
- Digitar `ultra think` no prompt → Claude aloca orçamento máximo de thinking (~32.000 tokens antes de responder)
- Para: decisões de arquitetura, debugging complexo, grandes refatorações
- Não usar para fixes simples; reservar para decisões que afetam o sistema inteiro

**30. Editar permissões para autonomia segura**
- Alternativa ao `--dangerously-skip-permissions`: configurar permissões explicitamente
- **Allow list**: comandos sabidamente seguros
- **Deny list**: operações destrutivas (deletes, removes)
- Deny list tem prioridade sobre allow list
- Mesma velocidade do modo perigoso, sem o perigo

**31. Agent teams**
- Sub-agentes não se comunicam entre si; agent teams comunicam
- Compartilham task list, se comunicam, podem atribuir trabalho uns aos outros
- Mais caros e demorados, mas produzem output mais coeso para projetos grandes
- Possível falar diretamente com agentes individuais do time

**32. Context7 MCP**
- Instalar o servidor Context7 MCP; quando precisar de docs, prompar para usar esse servidor
- Problema resolvido: training cutoff do Claude → funções/APIs deprecated sugeridas
- Context7 tem documentação version-specific de milhares de libs populares (Next.js, React, MongoDB, etc.)
- Injeta docs atuais no contexto antes de qualquer geração de código
- "Um comando para instalar, agentes trabalhando com informação muito mais atualizada"

## Insights para o wiki

- **Agent teams** é o conceito mais novo — a distinção clara entre sub-agentes (sem comunicação) e agent teams (com comunicação entre si) ainda não estava documentada no wiki
- **Git worktrees** (`claude --work-tree`) é uma forma de isolamento paralelo que complementa os sub-agentes — paralelo por branch, não por contexto
- **Ultra think** formaliza o que antes era intuitivo: há um modo de pensamento máximo ativável por texto
- **Context7 MCP** endereça uma limitação documentada no wiki (training cutoff) com solução concreta
- **Permissões explícitas** (allow/deny com deny > allow) é alternativa mais segura ao `--dangerously-skip-permissions` citado por outros criadores
- Hack #17 (challenge outputs + update skill/CLAUDE.md) é um **ciclo de aprendizado** — feedback do usuário vira melhoria permanente do comportamento do agente
- Loops com caveat de 3 dias e desktop scheduled tasks como complemento: primeiro criador no wiki a documentar essa limitação explicitamente

## Entidades relacionadas

- [[nate-herk]] — autor do conteúdo
- [[claude-code]] — ferramenta central de todos os 32 hacks
- [[claude-skills]] — mencionados como skills customizadas em `.cloud/skills/`

## Conceitos relacionados

- [[otimização-de-tokens]] — hacks #4, #5, #6, #13, #15, #24
- [[agentes-ia]] — hacks #11, #13, #23, #31
- [[prompt-engineering]] — hacks #7, #8, #9, #10, #17, #29
- [[segurança-com-ia]] — hack #30
