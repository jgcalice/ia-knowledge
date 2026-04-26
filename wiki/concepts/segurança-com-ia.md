---
title: "Segurança com IA"
type: concept
tags: [segurança, claude-code, desenvolvimento, api, backend, supabase, osint, privacidade, shadow-ai, governança, vibecoding, red-team]
source_count: 5
last_updated: 2026-04-26
---

# Segurança com IA

> Quatro dimensões: (1) segurança no *desenvolvimento* de apps com LLMs, (2) segurança *pessoal/digital* via ferramentas OSINT (12 ferramentas documentadas em 2 fontes), (3) segurança *empresarial/governança* (Shadow AI, infraestrutura como enabler), e (4) auditoria red team pré-deploy para apps vibecoded.

## Dimensão 1: Segurança no Desenvolvimento (via @Lucas Garcia Pit)

### Tese

Ferramentas de IA como Claude Code não são inerentemente inseguras — o risco está no desenvolvedor que, acelerado pela IA, pula fundamentos clássicos de segurança back-end. A velocidade de geração de código com LLMs amplia o gap entre "funciona" e "é seguro".

### Os 5 fundamentos

Documentados em [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]]:

| Ponto | Prática | Por quê |
|-------|---------|---------|
| 01 | API keys no servidor, nunca no front-end | Expor no front-end = qualquer um usa sua chave |
| 02 | RLS ativo no Supabase | Sem Row Level Security, usuário A acessa dados de B |
| 03 | Lógica sensível apenas no servidor | Preço, pagamento e regras de negócio não podem vir do cliente |
| 04 | Rate limiting nas APIs | Previne abuso e ataques de negação de serviço |
| 05 | Webhooks com assinatura verificada | Valida que a requisição veio de quem diz que veio |

**Padrão subjacente**: todos os 5 pontos seguem o mesmo princípio: **nunca confiar no cliente**. É o princípio clássico de "zero trust" aplicado a apps construídos com LLMs.

---

## Dimensão 2: Segurança Digital e OSINT

### Tese

A internet expõe muito mais dados pessoais do que a maioria das pessoas percebe. Ferramentas de OSINT (Open Source Intelligence) — usadas por hackers e investigadores — estão disponíveis gratuitamente e permitem mapear a exposição de qualquer pessoa ou infraestrutura. Conhecer essas ferramentas é a primeira linha de defesa. Duas fontes brasileiras independentes documentam 12 ferramentas complementares.

### Fonte A: 7 ferramentas para auditoria pessoal de exposição (via @Gustavo Melo)

Documentadas em [[2026-04-18_gustavo-melo-ferramentas-osint]]:

| Ferramenta | Tipo | Uso defensivo |
|-----------|------|--------------|
| **ZoomEye** | Scanner de dispositivos expostos | Verificar se câmeras/dispositivos próprios estão expostos |
| **Have I Been Pwned** | Verificador de vazamentos | Saber se seus dados foram comprometidos em breaches |
| **Namecheck** | Rastreador de contas por username | Auditoria de sua própria presença em plataformas |
| **Pic2Map** | Extrator de metadados EXIF | Verificar se suas fotos expõem localização |
| **EPA** | Mapeador de contas por e-mail/telefone | Auditar quais serviços estão vinculados ao seu contato |
| **Exploding Database** | Google Dorks avançados | Verificar se arquivos próprios foram indexados indevidamente |
| **Shint Premium Work** | Agregador de dados pessoais | Verificar o que está publicamente associado ao seu CPF/e-mail |

### Fonte B: 5 ferramentas usadas por profissionais de segurança (via @sidneyrodrigobr)

Documentadas em [[2026-04-08_sidney-ferramentas-osint]]:

| Ferramenta | Tipo | Capacidade |
|-----------|------|-----------|
| **Sherlock** | Rastreador de perfis (Python, open-source) | Varre 400 redes sociais a partir de um username |
| **Maltego** | Mapeador de conexões visual | E-mail → mapa de domínios, redes sociais, servidores, localização; usado pela Polícia Federal |
| **SpiderFoot** | OSINT automatizado | Vasculha 200 fontes (leaks, WHOIS, DNS, fóruns, pastebins) → dossiê em minutos |
| **Shodan** | "Google dos dispositivos vulneráveis" | Indexa roteadores, câmeras e servidores expostos na internet |
| **Google Dorking + Intelligence X** | Busca cirúrgica avançada | Localiza planilhas, CPFs, e-mails vazados e dados indexados publicamente |

### Convergências entre as duas fontes

- **Shodan ≈ ZoomEye**: ambos são scanners de dispositivos expostos — Gustavo usa ZoomEye, Sidney usa Shodan. Mesma categoria, ferramentas concorrentes.
- **Google Dorking ≈ Exploding Database**: a Exploding Database é construída sobre Google Dorks; Sidney nomeia a técnica diretamente. Confirmação independente de que dorks são o método padrão para indexação de dados expostos.
- **Princípio unificador**: todas as 12 ferramentas exploram dados *já públicos* — a novidade é a agregação e a velocidade de acesso. "O problema não é o acesso; é o uso."

---

## Dimensão 3: Segurança Empresarial — Shadow AI e infraestrutura como enabler

(Via [[stanford-digital-economy-lab]], [[2026-04-01_enterprise-ai-playbook-stanford]])

### Tese contraintuitiva

> *"Em nenhum dos casos rigorosos a segurança matou o projeto."*

Em todos os 12 casos analisados com dado completo no *Enterprise AI Playbook*, requisitos de segurança que **inicialmente bloqueavam acabaram habilitando** casos de uso impossíveis sem essa infra. **Segurança não é bloqueador — é enabler front-loaded**: alto custo no início, retorno cumulativo nos casos seguintes.

### Shadow AI — a realidade subterrânea

**Shadow AI** = uso de ferramentas IA sem aprovação de IT/security. O *AI-era equivalent* de shadow IT, com riscos amplificados.

| Indicador | Número |
|---|---|
| Funcionários que usam IA com ferramentas não-aprovadas | **70-80%** (multiple surveys) |
| Workers que usam exclusivamente ferramentas providas pelo empregador | **22%** (IBM, 2025) |
| Funcionários com Shadow AI que admitem inserir dado sensível | **57%** (TELUS Digital, 2025) |
| Custo médio de breach associado a IA | **$4.88M/incidente** (IBM, 2025) |

**Dois padrões de Shadow AI observados:**
- **Pattern A — Entusiasmo supera governança**: fabricante de semiconductors descobriu **1.500-1.600 ferramentas IA diferentes** em uso interno antes de qualquer plataforma oficial. Funcionários não eram mal-intencionados; liderança havia sinalizado "use AI" antes de qualquer plataforma existir.
- **Pattern B — Desespero supera burocracia**: hospitais — médicos adotando ambient transcription sem aprovação porque o vendor selection do hospital era lento demais.

→ **Lição**: Shadow AI é sintoma de que a política se move mais devagar que a tecnologia. **Esperar e contar com isso** é mais eficaz que tentar bloquear. Em healthcare, finance e governo, as consequências legais/regulatórias podem ser massivas.

### Infraestrutura de segurança como vantagem competitiva durável

**Caso emblemático**: grande banco varejista (US) sob consent order. Política prévia: "tudo dentro do firewall". Modern AI é cloud-based — política tornava cloud AI impossível.

Solução em 4 componentes:
1. **PII scrubbing on exit** — utterances de cliente perdem nomes, números de conta, valores antes de sair do firewall
2. **Synthetic data substitution** — valores fake substituem reais durante processamento externo
3. **Intent processing externally** — modelo cloud determina intenção e seleciona workflow
4. **Reassembly on return** — valores reais reinseridos internamente antes da resposta

Anos de investimento em segurança viraram **fundação para capabilities que competidores não conseguem replicar rapidamente**. Cada novo caso de uso reusa a infra: o tax é **front-loaded**.

### Quando o tax faz sentido vs é desperdício

- **Faz sentido**: quando habilita casos antes impossíveis (dados financeiros de cliente, registros de saúde, M&A confidencial)
- **É desperdício**: quando bloqueia trabalho sem habilitar solução para problemas reais. Quando processo formal é lento demais, **Shadow AI preenche o gap** — exatamente os riscos que o processo deveria prevenir

### Conexão com a Dimensão 1

Os 5 fundamentos do [[lucas-garcia-pit]] (API keys server-side, RLS, lógica server-side, rate limiting, webhooks assinados) são exatamente o tipo de infra que, **uma vez construída**, vira fundação reutilizável — assim como o pipeline de scrubbing do banco. **Mesmo princípio em escalas diferentes**: segurança bem-feita no dia 1 destrava casos de uso que nunca seriam possíveis depois.

---

## Dimensão 4: Auditoria de Segurança para Vibecoding

(Via [[artificial-intelligence-business]] / @thewizeai, [[2026-04-25_vibecoding-seguranca-auditoria-ia]])

### Tese

> "The dirty secret of vibecoding is that speed and security are inversely correlated."

Apps construídos rapidamente com LLMs não passam por nenhuma revisão de segurança. A maioria não tem auth checks, validação de entrada, nem ideia do que está exposto. Um único prompt pode replicar o processo de uma auditoria red team profissional ($15k+).

### O prompt de 6 blocos

| Bloco | Conteúdo |
|---|---|
| **Role + Scope** | "Act as senior security engineer. Assume hostile environment." Cobertura: frontend, backend, auth, DB, infra, third-party |
| **Core Objectives** | Vulnerabilidades em todos os severidade levels; falhas lógicas não-óbvias; construir threat model com perfis de atacantes |
| **Auth + Input** | Broken auth, privilege escalation, token leakage; SQL/NoSQL/template injection, XSS (stored/reflected/DOM), CSRF, file upload |
| **Data + API Logic** | Sensitive data exposure, hardcoded secrets, insecure storage; IDOR/BOLA, mass assignment, rate limiting, business logic abuse, race conditions |
| **Infra + Supply Chain** | CORS/CSP/HSTS misconfigured, debug endpoints expostos, env vars, cloud misconfig; pacotes vulneráveis, dependências maliciosas |
| **Ameaças Avançadas** | Logic flaws únicos ao sistema, feature abuse, cache poisoning, replay/timing attacks, **multi-step exploit chains** |

### O conceito de Attack Chain

O insight mais importante desta dimensão: **3 vulnerabilidades "low" podem se combinar em 1 "critical"**. Isso muda o modelo mental de segurança de checklist linear para grafo de dependências. O formato de output obriga o agente a mapear essas chains explicitamente.

### Relação com a Dimensão 1

Os 5 fundamentos da Dimensão 1 ([[lucas-garcia-pit]]) são **preventivos** (design-time). O prompt desta dimensão é **detective** (pré-deploy). Os dois são complementares: preventivo evita os erros mais comuns; detective pega o que passou.

---

## Síntese das quatro dimensões

| Dimensão | Quem usa | Princípio | Quando aplicar |
|---|---|---|---|
| 1 — Desenvolvimento preventivo | Dev individual com Claude Code | Zero trust; nunca confiar no cliente | Durante o design/build |
| 2 — Pessoal/OSINT | Usuário comum | Auditar a própria exposição | Periodicamente |
| 3 — Empresarial | Organização inteira | Segurança como infra reutilizável | Antes de habilitar IA enterprise |
| 4 — Vibecoding (pré-deploy) | Dev que vibecoda | Assume já comprometido; pense como atacante | Antes de cada deploy |

**Padrão unificado**: a aceleração cria exposições invisíveis que só são corrigidas com **intenção ativa** — seja no design, na auditoria pessoal, na governança corporativa ou no review pré-deploy.

## Fontes

- [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 pontos de segurança para apps com Claude Code
- [[2026-04-18_gustavo-melo-ferramentas-osint]] — 7 ferramentas OSINT para pesquisa e segurança digital
- [[2026-04-08_sidney-ferramentas-osint]] — 5 ferramentas OSINT usadas por profissionais (Sherlock, Maltego, SpiderFoot, Shodan, Google Dorking)
- [[2026-04-01_enterprise-ai-playbook-stanford]] — Shadow AI, segurança empresarial como enabler
- [[2026-04-25_vibecoding-seguranca-auditoria-ia]] — prompt red team completo para auditoria de apps vibecoded
