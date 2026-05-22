---
title: "Ollama"
type: entity
category: tool
tags: [llm, ia-local, open-source, ferramentas-ia, alternativas-saas]
source_count: 1
last_updated: 2026-05-22
---

# Ollama

> **Categoria:** Ferramenta | **Tipo:** Plataforma de execução de LLMs localmente

## O que é

Ollama é uma ferramenta open-source que permite executar modelos de linguagem de grande escala (LLMs) — incluindo modelos de classe GPT-4 como Llama, Mistral, Phi, Gemma — diretamente na própria máquina (laptop ou servidor), sem custo de API e sem enviar dados para nuvem externa.

Disponível para macOS (download nativo), Linux (`curl -fsSL https://ollama.com/install.sh | sh`) e Windows. Slogan oficial: *"Start building with open models."*

## Posição no ecossistema

| Dimensão | OpenAI API | Ollama (local) |
|----------|-----------|---------------|
| Custo por desenvolvedor ativo | ~$500/mês | $0 |
| Privacidade | Dados enviados a servidor externo | Dados ficam na máquina |
| Latência | Depende da rede | Depende do hardware local |
| Disponibilidade | Requer internet | Funciona offline |
| Modelos disponíveis | GPT-4, GPT-4o (fechados) | Llama, Mistral, Phi, Gemma… (abertos) |

## Implicação para arquétipos do wiki

Qualquer arquétipo de negócio documentado no wiki que incorre em custo de OpenAI API pode avaliar o Ollama como alternativa para:
- Tarefas não-críticas de qualidade (triagem, resumo, categorização) a custo zero
- Dados sensíveis do cliente — sem envio para terceiros
- Ambientes com conectividade restrita ou off-grid

Relevante para [[agentes-ia]]: pipelines de agentes locais não dependem de quotas ou latência de API externa.

## Fontes

- [[2026-05-21_harish-bhatt-repos-ilegais]] — mencionado como substituto da OpenAI API ($500/mês → $0) para desenvolvedores; capacidade: modelos GPT-4 class offline
