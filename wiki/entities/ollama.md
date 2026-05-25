---
title: "Ollama"
type: entity
category: tool
tags: [llm, ia-local, open-source, ferramentas-ia, alternativas-saas]
source_count: 2
last_updated: 2026-05-25
---

# Ollama

> **Categoria:** Ferramenta | **Tipo:** Plataforma de execução de LLMs localmente

## O que é

Ollama é uma ferramenta open-source que permite executar modelos de linguagem de grande escala (LLMs) — incluindo modelos de classe GPT-4 como Llama, Mistral, Phi, Gemma, Qwen, DeepSeek — diretamente na própria máquina (laptop ou servidor), sem custo de API e sem enviar dados para nuvem externa.

Disponível para macOS (download nativo), Linux (`curl -fsSL https://ollama.com/install.sh | sh`) e Windows (installer). Slogan oficial: *"Start building with open models."*

## Posição no ecossistema

| Dimensão | OpenAI API | Ollama (local) |
|----------|-----------|---------------|
| Custo por desenvolvedor ativo | ~$500/mês | $0 |
| Privacidade | Dados enviados a servidor externo | Dados ficam na máquina |
| Latência | Depende da rede | Depende do hardware local |
| Disponibilidade | Requer internet | Funciona offline |
| Modelos disponíveis | GPT-4, GPT-4o (fechados) | Llama, Mistral, Phi, Gemma, Qwen, DeepSeek… (abertos) |

## Comandos principais

```bash
# Instalar (Linux/Mac)
curl -fsSL https://ollama.com/install.sh | sh

# Rodar modelo (baixa automaticamente na 1ª vez)
ollama run qwen3:8b         # uso geral, maioria dos laptops
ollama run qwen3.6:27b      # codificação
ollama run deepseek-r1:8b   # raciocínio
```

## API OpenAI-compatível

Ollama expõe automaticamente uma API REST em `http://localhost:11434` com interface compatível com a OpenAI API. Qualquer ferramenta, agente ou script que consome `openai.ChatCompletion` pode apontar para o endereço local sem mudança de código.

## Quantização padrão

Ollama aplica **Q4_K_M** por padrão — reduz o tamanho do modelo à metade com perda quase imperceptível de qualidade. Exemplo: Llama 4 70B passa de ~140GB (full precision) para ~40GB.

## Guia de RAM

| RAM | Modelos recomendados |
|-----|---------------------|
| 8GB | Gemma 4 1B, Qwen3 1.7B |
| 16GB | 7B–8B (ponto ideal) |
| 32GB+ | 14B–30B |
| 64GB+ | 70B class |

## Implicação para arquétipos do wiki

Qualquer arquétipo de negócio documentado em [[estratégia-de-negócios-com-ia]] que incorre em custo de LLM API pode avaliar o Ollama para:
- Tarefas não-críticas (triagem, resumo, categorização) a custo zero
- Dados sensíveis do cliente — sem envio para terceiros
- Ambientes com conectividade restrita ou off-grid

Relevante para [[agentes-ia]]: pipelines de agentes locais não dependem de quotas ou latência de API externa.

Ver conceito central: [[ia-local]]

## Fontes

- [[2026-05-21_harish-bhatt-repos-ilegais]] — mencionado como substituto da OpenAI API ($500/mês → $0) para desenvolvedores; framing "destroem $50B em receita corporativa"
- [[2026-05-24_hasan-toor-modelos-ia-offline]] — guia técnico completo: instalação, comandos de modelo, RAM guide, quantização Q4_K_M e compatibilidade OpenAI API; posicionado como alternativa direta a assinaturas de $20/mês
