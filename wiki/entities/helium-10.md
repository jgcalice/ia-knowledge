---
title: "Helium 10"
type: entity
category: tool
tags: [amazon, validação-de-nicho, market-research, dados-estruturados]
source_count: 3
last_updated: 2026-05-27
---

# Helium 10

Plataforma de market research para vendedores Amazon — fornece dados de volume de busca mensal, número de concorrentes, preço médio, sazonalidade. Usado como fonte de dados estruturados que alimentam Claude na etapa de validação de nicho.

## Papel no wiki

Primeira ferramenta de validação Amazon documentada. Aparece como **input estruturado** para Claude no Prompt 1 de [[drew-huibregtse]] — formato: "180K monthly searches, 800 competitors, $9.99 average price → é um bom nicho?".

## Padrão de uso

Sempre via **copia-cola dos números do Helium 10 para o Claude**, não via integração direta. Mesmo padrão de [[google-search-console]] ([[daniel-socrates]]) e Yahoo Finance / Bloomberg ([[faria-lima-elevator]]): a ferramenta especializada gera o dataset, a IA prioriza/interpreta.

## Aparições no wiki

- [[2026-04-23_drew-huibregtse-sistema-amazon-kdp]] — Passo 1 do sistema de 4 etapas; critérios: alto volume de buscas + baixo review count + títulos fracos
- [[2026-05-09_drew-huibregtse-amazon-kdp]] — input do Prompt 1 (validação de nicho em 30s)
- [[2026-05-14_drew-huibregtse-livros-colorir-ia]] — Passo 1 do sistema de colorir: alto volume + baixo review count + títulos fracos na página 1

## Relacionado

- [[drew-huibregtse]] — creator que documenta o uso
- [[amazon-kdp]] — plataforma final do pipeline
- [[google-search-console]] — análogo na vertical de SEO (mesmo padrão "dataset → Claude prioriza")
- [[claude-code]] — LLM-base
