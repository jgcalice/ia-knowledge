---
title: "Google Search Console"
type: entity
category: tool
tags: [seo, google, analytics, dados-estruturados]
source_count: 1
last_updated: 2026-05-20
---

# Google Search Console

Ferramenta gratuita do Google que mostra como o próprio Google enxerga um site — queries de busca, posição média, cliques, impressões, indexação. Pivô para qualquer otimização SEO baseada em dados (não em achismo).

## Papel no wiki

Aparece como **fonte de dados estruturados** que alimentam prompts de Claude no pipeline de [[daniel-socrates]] — copia-cola da tabela "Consultas" filtrada por posição vira input do Claude para priorização de ganhos rápidos.

## Funções operacionais documentadas

| Função | Como usar |
|--------|-----------|
| Identificar keywords latentes | Desempenho → ativar Posição Média → filtrar por posição 8–20 |
| Descobrir página ranqueando | Clicar na keyword → ver URL associada |
| Forçar reindexação | Cole URL no campo de busca → Solicitar indexação |

## Aparições no wiki

- [[2026-04-08_daniel-socrates-seo-gsc-claude]] — base do pipeline de otimização

## Relacionado

- [[daniel-socrates]] — criador que documenta o método
- [[google-maps]] — outra fonte de dados Google usada como dataset estruturado
- [[claude-code]] — LLM que lê e prioriza os dados copiados do GSC
- [[seo-com-ia]] — conceito guarda-chuva (Abordagem 2)
