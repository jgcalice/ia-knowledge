---
title: "Automação da Busca de Emprego com IA — CareerOps Plugin"
type: source
source_file: "2026-04-22_arshman_khalid_DXbCZz4t3iN.md"
author: "@Arshman Khalid"
date: 2026-04-22
format: reel
tags: [busca-de-emprego, career-ops, apify, linkedin, automação, currículo, ats, negociação]
source_url: "https://www.instagram.com/reel/DXbCZz4t3iN/?igsh=c3RtYTFhanU5bGlx"
source_count: 1
---

# Automação da Busca de Emprego com IA — CareerOps Plugin

> **Fonte:** [[2026-04-22_arshman_khalid_DXbCZz4t3iN]] | **Autor:** @Arshman Khalid | **Data:** 2026-04-22 | **Formato:** Reel (94s) | **[↗ Ver post](https://www.instagram.com/reel/DXbCZz4t3iN/?igsh=c3RtYTFhanU5bGlx)**

## TL;DR

CareerOps é um plugin gratuito para Claude (disponível no GitHub) que automatiza toda a busca de emprego — do scraping de vagas no LinkedIn até scripts de negociação salarial.

## Contexto

@Arshman Khalid afirma ter ficado em ambos os lados do processo: contratando em Fortune 500 e Big Four, e sendo contratado. Diz ter aplicado a 518 vagas e obtido 28 entrevistas (incluindo Google). O plugin é apresentado como a ferramenta que ele usaria hoje para garantir emprego.

## O que foi ensinado

**Pipeline completo do CareerOps:**

1. **Puxar vagas do LinkedIn automaticamente** via conector Apify (LinkedIn Jobs Scraper Actor)
2. **Avaliar cada vaga de A a F** contra a experiência real do candidato
3. **Gerar currículo ATS-friendly + carta de apresentação** personalizado para cada vaga A-tier
4. **Identificar lacunas de skills** entre o currículo e a JD, com instruções para corrigir antes da entrevista
5. **Construir histórias STAR** mapeadas para a vaga específica
6. **Redigir mensagem de outreach** para o hiring manager
7. **Entregar scripts de negociação salarial** com framework de salário após receber oferta

**Como instalar:**
1. Baixar o zip do repositório GitHub (link nos comentários do post)
2. Abrir Claude → Novo plugin → Fazer upload do arquivo zip
3. Criar conta gratuita no Apify
4. Ativar o **LinkedIn Jobs Scraper Actor** e copiar o API token
5. No Claude: instalar o conector Apify e colar o token
6. Colar o currículo existente ou descrever o trabalho dos sonhos — o sistema faz o resto

**Frase-chave do autor:**
> "Empresas usam IA para rejeitar seu currículo em 6 segundos. Já é hora de você usar IA para rejeitar a vaga delas em 3 segundos."

## Insights para o wiki

- **Nova forma de distribuição do CareerOps**: aqui é apresentado como **plugin** instalável via zip no Claude (não como script ou projeto Claude Code), ampliando o registro de [[career-ops]] que documentava apenas a versão de script terminal.
- **Apify reaparece**, mas agora com o **LinkedIn Jobs Scraper** especificamente — diferente do uso documentado em [[2026-03-28_prospecção-leads-claude-apify]] (Google Maps). Apify é mais versátil do que o wiki registrava.
- **Negociação salarial** como etapa do pipeline — ponto não documentado anteriormente. O sistema não termina na candidatura, mas acompanha até a oferta.
- **ATS como argumento central**: "empresas usam IA para rejeitar currículos" reforça o argumento de [[busca-de-emprego-com-ia]] sobre por que currículo genérico falha.

## Entidades relacionadas

- [[career-ops]] — plugin central do tutorial
- [[apify]] — scraper de vagas LinkedIn usado no pipeline
- [[linkedin]] — fonte de vagas automatizada via Apify Actor
- [[arshman-khalid]] — autor e criador do conteúdo

## Conceitos relacionados

- [[busca-de-emprego-com-ia]] — expansão significativa: nova versão de plugin + etapas de negociação
- [[carreira-com-ia]] — reforça o padrão de automação de carreira end-to-end
