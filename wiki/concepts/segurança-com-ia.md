---
title: "Segurança com IA"
type: concept
tags: [segurança, claude-code, desenvolvimento, api, backend, supabase, osint, privacidade]
source_count: 2
last_updated: 2026-04-24
---

# Segurança com IA

> Duas dimensões: segurança no *desenvolvimento* de apps com LLMs + segurança *pessoal/digital* via ferramentas OSINT.

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

## Dimensão 2: Segurança Digital e OSINT (via @Gustavo Melo)

### Tese

A internet expõe muito mais dados pessoais do que a maioria das pessoas percebe. Ferramentas de OSINT (Open Source Intelligence) — usadas por hackers e investigadores — estão disponíveis gratuitamente e permitem mapear a exposição de qualquer pessoa. Conhecer essas ferramentas é a primeira linha de defesa.

### As 7 ferramentas OSINT

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

**Padrão subjacente**: todas as ferramentas exploram dados *já públicos* — a novidade é a agregação e a facilidade de acesso.

---

## Convergência entre as duas dimensões

Ambas as perspectivas compartilham o mesmo princípio de fundo: **a aceleração (pela IA no desenvolvimento, pela internet no acúmulo de dados) cria exposições invisíveis que só são corrigidas com consciência ativa**. O dev que usa Claude Code sem pensar em segurança e o usuário que publica fotos sem verificar metadados EXIF cometem o mesmo erro: subestimar o que está exposto.

## Fontes

- [[2026-04-15_lucas-garcia-pit-seguranca-claudecode]] — 5 pontos de segurança para apps com Claude Code
- [[2026-04-18_gustavo-melo-ferramentas-osint]] — 7 ferramentas OSINT para pesquisa e segurança digital
