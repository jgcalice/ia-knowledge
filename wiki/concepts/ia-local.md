---
title: "IA Local — Execução de LLMs sem Nuvem"
type: concept
tags: [ia-local, ollama, lm-studio, open-source, ferramentas-ia, custo-zero, quantização, llm]
source_count: 2
last_updated: 2026-05-25
---

# IA Local — Execução de LLMs sem Nuvem

> **Fontes:** 2 | **Domínio:** Infraestrutura de IA — rodar modelos abertos no próprio hardware

## Definição

Execução de Large Language Models (LLMs) diretamente no hardware local — laptop, desktop ou servidor próprio — sem envio de dados para APIs externas. Custo por token: $0.

## Por que isso importa em 2026

Os modelos open-source (Llama, Qwen, DeepSeek, Gemma) alcançaram qualidade próxima à dos serviços comerciais ($20/mês Claude, OpenAI API ~$500/mês para devs ativos), e a tooling tornou o setup acessível a não-técnicos em menos de 20 minutos.

## Runners disponíveis

| Runner | Interface | Perfil ideal |
|--------|-----------|--------------|
| **[[ollama]]** | CLI | Power users, devs, integração com scripts e agentes |
| **[[lm-studio]]** | GUI completa | Iniciantes, quem prefere evitar o terminal |

"Mesmos modelos. Mesma qualidade. Portas diferentes para o mesmo quarto." — @hasantoxr

## Guia de RAM vs modelo

| RAM | Faixa de modelos | Qualidade estimada |
|-----|------------------|--------------------|
| 8GB | 1B–4B (Gemma 4 1B, Qwen3 1.7B) | Funcional para tarefas simples |
| 16GB | 7B–8B | **Ponto ideal** para a maioria dos laptops |
| 32GB+ | 14B–30B | "Claude quality começa aqui" |
| 64GB+ | 70B class | Frontier genuíno |

Regra prática: "A 7B running fast beats a 70B swapping to disk. Fit it, don't force it."

## Quantização: o cheat code

Modelos grandes em precisão completa são impraticáveis no hardware comum:
- Llama 4 70B full precision: ~140GB
- Llama 4 70B em **Q4_K_M**: ~40GB

**Q4_K_M** é a quantização padrão do Ollama — reduz o peso à metade com perda quase imperceptível de qualidade. Isso é o que permite rodar modelos de calibre enterprise em laptops comuns.

## Interfaces de chat (além do terminal)

| Interface | Tipo | Destaque |
|-----------|------|----------|
| Open WebUI | Docker | "Clone do ChatGPT" para modelos locais |
| LM Studio | App nativo | Chat embutido, zero setup |
| Jan | App nativo | Open-source |
| Enchanted / Misty | App nativo | Hook nativo no Ollama |

## Compatibilidade com o ecossistema

[[ollama]] expõe uma **API OpenAI-compatível** em `http://localhost:11434`. Qualquer ferramenta, agente ou script que consome a OpenAI API pode apontar para o endereço local sem mudança de código.

Implicação: a máquina local se torna a API. Sem chaves, sem cobranças, sem dados saindo.

## Impacto nos arquétipos do wiki

Todos os arquétipos documentados em [[estratégia-de-negócios-com-ia]] que dependem de LLM em produção podem usar IA local para:
- Tarefas de triagem, resumo e categorização a custo zero
- Dados sensíveis do cliente sem envio a terceiros
- Ambientes offline ou com conectividade restrita

Ver também [[otimização-de-tokens]]: IA local elimina custo de tokens completamente — uma solução mais radical que as técnicas de compressão e roteamento já documentadas.

## Fontes

- [[2026-05-24_hasan-toor-modelos-ia-offline]] — guia passo-a-passo de 7 etapas: setup Ollama, seleção de modelo, RAM guide, quantização Q4_K_M, UI options, API compatibility
- [[2026-05-21_harish-bhatt-repos-ilegais]] — Ollama mencionado como substituto da OpenAI API ($500/mês → $0) para devs; framing "destroem $50B em receita corporativa"
