---
title: "5 Ferramentas OSINT que Parecem Ilegais mas São Usadas por Profissionais"
type: source
source_file: "2026-04-08_sidney_analista_de_redes_e_ciberseguranca_DW4BELkjMVb.md"
author: "@sidneyrodrigobr"
date: 2026-04-08
format: carousel
tags: [osint, segurança, privacidade, cibersegurança, ferramentas-ia]
source_url: "https://www.instagram.com/p/DW4BELkjMVb/"
source_count: 1
---

# 5 Ferramentas OSINT que Parecem Ilegais mas São Usadas por Profissionais

> **Fonte:** [[2026-04-08_sidney_analista_de_redes_e_ciberseguranca_DW4BELkjMVb]] | **Autor:** @sidneyrodrigobr | **Data:** 2026-04-08 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DW4BELkjMVb/)**

## TL;DR

Cinco ferramentas OSINT (Sherlock, Maltego, SpiderFoot, Shodan, Google Dorking + Intelligence X) parecem invasivas mas operam exclusivamente com dados públicos — o perigo não é a ferramenta, é o que já está exposto sem que você saiba.

## Contexto

Sidney Rodrigo (@sidneyrodrigobr), analista de redes e cibersegurança, publica um carousel de 8 slides mostrando ferramentas usadas por profissionais de segurança em investigações legítimas. O enquadramento é o mesmo da comunidade OSINT: essas ferramentas não "invadem" — apenas organizam e apresentam o que já está públicamente disponível na internet. O disclaimer é explícito: conteúdo educacional, ferramentas com dados públicos e finalidades legítimas.

## O que foi ensinado

- **Sherlock** — rastreador de perfis: digita um username e varre 400 redes sociais, revelando onde aquela pessoa tem conta — inclusive "cantos obscuros" da internet. Ferramenta Python open-source.
- **Maltego** — mapeador de conexões: insere um e-mail e gera um mapa visual de conexões (domínios, redes sociais, servidores, localização). Usado pela Polícia Federal brasileira. Opera com dados públicos.
- **SpiderFoot** — OSINT automatizado: coloca um alvo, a ferramenta vasculha 200 fontes (leaks, WHOIS, DNS, fóruns, pastebins) e entrega um dossiê em minutos. Criado por Steve Micallef (@binarypool).
- **Shodan** — "Google dos dispositivos vulneráveis": buscador que indexa roteadores, câmeras e servidores expostos na internet. Não invade — revela o que já está "pingando online".
- **Google Dorking + Intelligence X** — busca cirúrgica: comandos especializados para encontrar planilhas, CPFs, e-mails vazados e dados sensíveis já publicados e indexados. Intelligence X é um motor de busca que indexa dados de leaks.
- **Princípio unificador**: todas as ferramentas exploram dados *já públicos* — o problema não é o acesso, é o uso. "Usar mal o que é legal pode te colocar do lado errado da lei."

## Insights para o wiki

- **Segunda fonte de OSINT defensivo**: esta fonte confirma e expande a [[2026-04-18_gustavo-melo-ferramentas-osint]] com um conjunto diferente de ferramentas — a Dimensão 2 de [[segurança-com-ia]] agora tem 12 ferramentas documentadas de duas fontes independentes.
- **Convergência em Shodan e Google Dorking**: [[gustavo-melo]] inclui ZoomEye (similar ao Shodan) e Exploding Database (similar ao Google Dorking). Sidney usa exatamente Shodan e Google Dorking. Mesma categoria de ferramenta, nomes diferentes — sinal de que são as referências consolidadas nesse espaço.
- **Maltego + uso policial**: é a primeira menção a adoção pela Polícia Federal de uma ferramenta OSINT no wiki — dado que valida o uso legítimo para além do contexto educacional.
- **Sherlock como benchmark open-source**: Python tool open-source que varre 400 redes — a menção confirma que OSINT não exige ferramentas pagas; o ecossistema open-source está maduro.

## Entidades relacionadas

- [[sidney-rodrigo]] — autor do conteúdo, analista de redes e cibersegurança
- [[gustavo-melo]] — segunda voz BR sobre OSINT defensivo no wiki (conjunto diferente de ferramentas)

## Conceitos relacionados

- [[segurança-com-ia]] — Dimensão 2 (OSINT/privacidade), expandida com 5 novas ferramentas
