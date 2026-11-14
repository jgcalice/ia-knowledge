---
title: "Claude: 7 prompts para diagnosticar Wi-Fi lento"
type: source
source_file: "2026-11-09_harish_bhatt_tech_and_ai_DfhVoM6ElZQ.md"
author: "@Harish Bhatt | Tech and Ai"
date: 2026-11-09
format: carousel
tags: [claude, prompt-engineering, ferramentas-ia, automação]
source_url: "https://www.instagram.com/p/DfhVoM6ElZQ/?img_index=7"
source_count: 1
---

# Claude: 7 prompts para diagnosticar Wi-Fi lento

> **Fonte:** [[2026-11-09_harish_bhatt_tech_and_ai_DfhVoM6ElZQ]] | **Autor:** @Harish Bhatt | Tech and Ai | **Data:** 2026-11-09 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DfhVoM6ElZQ/?img_index=7)**

## TL;DR
Sete prompts para o Claude Desktop (com acesso ao computador) atuar como técnico de rede: medir a velocidade, achar consumo de banda, analisar quedas, sinal, dispositivos, configurações e monitorar o provedor semanalmente. Todos exigem aprovação antes de qualquer mudança.

## Contexto
Carousel de 8 slides do criador @codingknowledge (ver [[harish-bhatt]]), com gancho de "técnico de rede de $100/hora" e a promessa de provar ao provedor que a velocidade contratada não é entregue. CTA: comentar "ai" para receber os prompts. Os slides 1-6 estão em inglês e os slides 7-8 em português.

## O que foi ensinado
1. **Diagnóstico de velocidade:** testar download, upload e ping contra o plano `[X Mbps]` e indicar se o gargalo é computador, Wi-Fi, roteador ou provedor.
2. **Auditoria de banda:** listar apps, downloads, sincronizações e atualizações em segundo plano, ordenados por consumo, sem encerrar nada.
3. **Quedas de Wi-Fi:** analisar logs dos últimos 7 dias (contagem, horário, duração, padrões, drivers, economia de energia).
4. **Sinal e canal:** checar intensidade, banda, canal e redes vizinhas; comparar 2.4 GHz e 5 GHz; passo a passo no roteador.
5. **Dispositivos desconhecidos:** listar hostname, fabricante, IP e MAC; a pessoa digita as credenciais do roteador; o Claude nunca adivinha senhas nem desconecta nada.
6. **Auditoria de configurações:** DNS, adaptador e driver, economia de energia, VPN/proxy, erros; explicar o impacto antes de alterar.
7. **Monitoramento semanal:** teste toda segunda-feira às 9h, registro em planilha, alerta se o download ficar abaixo de 50% do plano por 3 semanas seguidas e rascunho de e-mail de reclamação (sem envio automático).

**Padrão comum:** cada prompt termina com uma restrição "não altere / não envie sem minha aprovação". O aviso final diz que dependem das permissões de computer use do Claude Desktop e de acesso aos logs do sistema.

## Insights para o wiki
- Aplica o padrão de prompts parametrizados (`[X Mbps]`) ao suporte técnico doméstico, um serviço profissional a mais que a IA substitui.
- Reforça o princípio de **human-in-the-loop** em prompts agênticos: leitura e diagnóstico livres, ações destrutivas ou externas só com aprovação.
- Usa computer use do Claude Desktop, não o Claude Code, ampliando as superfícies do Claude já vistas no wiki.
- O "$100/hora" é gancho de marketing, não verificado. Funcionalidades dependem de permissões e ferramentas disponíveis no ambiente do usuário.

## Entidades relacionadas
- [[harish-bhatt]] — autor
- [[claude-code]] — página do ecossistema Claude (aqui, Claude Desktop com computer use)

## Conceitos relacionados
- [[prompt-engineering]] — prompts com restrição explícita de aprovação e placeholders
- [[agentes-ia]] — agente com acesso ao computador e rotina agendada
