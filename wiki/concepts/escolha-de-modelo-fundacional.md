---
title: "Escolha de Modelo Fundacional"
type: concept
tags: [llm, modelo, comoditização, multi-model, abstração, claude, gpt, gemini, llama, qwen]
source_count: 1
last_updated: 2026-04-25
---

# Escolha de Modelo Fundacional

> **Fonte:** 1 (relatório empírico) | **Domínio:** Decisões arquiteturais sobre qual LLM usar e quando

## A tese da comoditização parcial

| Veredicto sobre o modelo | % dos 51 casos |
|---|---|
| **Commodity (intercambiável)** | **42%** |
| Importância moderada | 39% |
| Diferenciador crítico | 19% |

A fronteira da commodity é definida por **complexidade da tarefa**:
- **Tarefas rotineiras** (triagem de tickets, busca em docs, content marketing, screening de currículos): **71% commodity, 0% crítico**
- **Tarefas avançadas** (coding complexo, compliance, doc clínica, agentic): apenas **18% commodity, 35% crítico**

→ Implicação: para a maior parte dos casos de uso de pequena/média complexidade, escolher entre Claude, GPT-4 ou Gemini **não muda materialmente o resultado**.

## Os 5 padrões emergentes

### 1. Multi-model é a norma, não a exceção

A maioria das implementações usa **múltiplos modelos**. Formas observadas:
- **Routing por tarefa**: modelo rápido/barato (small) para classificação, modelo capable para reasoning. Diferença de custo de **10x ou mais**
- **Validação por redundância**: mesma query em dois modelos; só aceita se concordam
- **Otimização por query**: gateway com 4 dimensões (custo, latência, relevância, accuracy)

> *"We don't use just one. We use Claude and we use OpenAI and we use some Llama. So we use different models. We also sometimes use Bedrock."*
> — Head of Operations, Technology Company

### 2. Camada de abstração é vantagem competitiva

> *"My focus is not so much about the tools. My focus is to build a platform... You have flexibility to pivot between models if and when one gets better or cheaper."*
> — Head of Operations, Technology Company

Empresa de food delivery construiu chatbot próprio sobre OpenAI + Gemini + Claude — chegou a **90-95% de automação em customer service** sem dependência de nenhum provider único.

> The durable advantage is in the **orchestration layer**, not the foundation model.

### 3. Open-source entra por funções especializadas

Não substituindo o core, mas onde **customização e controle** importam mais que capability frontier:
- **NER** (named entity recognition) — security, info-sec
- **Cybersecurity vendor** construiu produto inteiro sobre Llama base e fine-tunou pesado — escolha foi por adaptação a domínio narrow, não por leadership de performance
- Cloud-native software companies às vezes **rejeitam open-source** por razões de privacidade/segurança contratual

### 4. Capability + speed > custo (por enquanto)

Mais de **2/3 das empresas** que discutiram seleção de modelo citaram **capability como razão primária**, não custo. Empresas escolheram o modelo que entrega resultado mais rápido, não o mais barato.

Exemplo: retail company construiu solução custom sobre vendor especializado, depois descobriu que podia replicar em Claude direto. Cancelaram o contrato.

Soberania de dado: **resolvida por contrato com cloud provider**, não por self-hosting. Empresas negociaram proteção contratual em vez de instalar modelos localmente.

### 5. Modelos chineses open-source dominando OpenRouter

Em fev/2026, no OpenRouter (plataforma que roteia API requests por 400+ modelos para 4M+ usuários):
- **4 dos top-5 por volume de tokens são chineses open-source** (Qwen, Kimi, Minimax, GLM)
- Driver: **agentic workloads** consomem exponencialmente mais tokens que chatbots tradicionais
- Empresas US ainda preferem providers americanos (OpenAI, Anthropic, Llama, Gemini) por compliance, suporte e qualifying de vendor

→ Caveat de [[alvin-wang-graylin]]: à medida que open-source fecha o gap, **inferência cost** (tokenomics) vai virar o fator primário, especialmente em agentic.

## A relação entre escolha de modelo e custo

- **Modelos open-source** atingem ~90% da performance de proprietários ao release e convergem rapidamente (MIT, 2025)
- Custo médio: **6x menos por token** em pricing observado (Artificial Analysis, jan/2026)
- Mais de 50% das empresas (McKinsey/Mozilla/McGovern, 2025) já usam open-source em algum lugar do stack; 72% entre tech companies
- **Mas open-source ainda é apenas ~20% do volume de tokens** — closed models dominam por inércia, não por superioridade

## Implicação para o wiki

Contradiz parcialmente a narrativa típica do Instagram (Claude vs ChatGPT vs Gemini como debate central). Os dados sugerem:

1. **Para tarefas rotineiras** (a maioria dos use cases mostrados em criadores de conteúdo): o modelo escolhido importa pouco
2. **A vantagem real** está em construir camada de abstração + RAG + roteamento + dado proprietário ([[dados-como-moat]])
3. **A escolha agêntica** (modelo para reasoning de longo horizonte) é onde capability ainda diferencia — mas é apenas **20% dos casos hoje**

Para criadores como [[evolving-ai]] (que recomendam escolher Haiku/Sonnet/Opus por tarefa) ou [[nate-herk]] (sub-agentes em Haiku), os dados confirmam: **routing por tarefa é a estratégia certa** — e está se tornando padrão na escala empresarial.

## Fontes

- [[2026-04-01_enterprise-ai-playbook-stanford]]
