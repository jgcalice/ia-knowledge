---
title: "Graphify: Memória Infinita e 71,5x Menos Tokens no Claude"
type: source
source_file: "2026-04-12_marc_cleroux_DXAzOJojLrR.md"
author: "@Marc Cleroux"
date: 2026-04-12
format: carousel
tags: [claude, claude-code, tokens, otimização, knowledge-graph, graphify, obsidian, memória]
source_url: "https://www.instagram.com/p/DXAzOJojLrR/?img_index=5&igsh=MXV0YWptZHJqNWdzOQ=="
source_count: 1
---

# Graphify: Memória Infinita e 71,5x Menos Tokens no Claude

> **Fonte:** [[2026-04-12_marc_cleroux_DXAzOJojLrR]] | **Autor:** @Marc Cleroux | **Data:** 2026-04-12 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DXAzOJojLrR/?img_index=5&igsh=MXV0YWptZHJqNWdzOQ==)**

## TL;DR

Instalar o Graphify no Claude Code transforma todo o workspace em um grafo de conhecimento navegável — reduzindo o consumo de tokens de 20.000 para 280 por sessão (71,5x menos), baseado no sistema de [[andrej-karpathy]].

## Contexto

@Marc Cleroux (Instagram: @tenfoldmarc) apresenta um método de 4 passos para dar "memória infinita" ao Claude usando [[graphify]] — uma skill open-source hospedada em `/github.com/safishamsi/graphify`. A proposta é inspirada no sistema de [[andrej-karpathy]] (ex-OpenAI/Tesla, criador do termo "vibe coding"). O ganho central é drástico: em vez de o Claude ler arquivos brutos inteiros a cada sessão, ele consulta um mapa estruturado do workspace.

## O que foi ensinado

**Antes vs. depois:**
- Sem Graphify: ~20.000 tokens/sessão
- Com Graphify: ~280 tokens/sessão → redução de **71,5x**

**4 passos do método:**

1. **Instalar o Graphify** — acessar `/github.com/safishamsi/graphify`, copiar o comando de instalação do README e colar dentro do Claude Code
2. **Mapear todos os arquivos** — executar `/graphify ~/.claude` dentro da pasta principal do Claude; a ferramenta escaneia tudo e constrói um grafo de conhecimento do workspace
3. **Visualizar o grafo em 3D** — baixar o [[obsidian]] (gratuito), abrir a pasta Claude como vault e clicar em "graph view" para ver o workspace como um mapa galático
4. **Conectar ao CLAUDE.md** — adicionar ao arquivo CLAUDE.md as instruções:
   ```
   ## Context Navigation
   1. ALWAYS query the knowledge graph first
   2. Only read raw files if I explicitly say so
   ```

**Por que funciona:** em vez de o Claude ler o conteúdo integral de cada arquivo para encontrar contexto, o grafo fornece um índice estruturado — Claude consulta o mapa e lê apenas o que é necessário.

## Insights para o wiki

- **Nova técnica de otimização de tokens**: complementa as 6 técnicas já documentadas em [[otimização-de-tokens]] com uma abordagem baseada em grafo de conhecimento — possivelmente a mais poderosa em números absolutos (71,5x vs. 8x do Code Review Graph)
- **Padrão "instrua o Claude a não ler arquivos brutos"**: o passo 4 estabelece que o Claude deve consultar o grafo primeiro — reforça o padrão de [[agentes-ia]] onde o contexto é mediado por estrutura, não por leitura direta
- **Obsidian como visualizador de workspace de IA**: uso não convencional do [[obsidian]] — não para tomar notas, mas para inspecionar a estrutura do workspace do Claude
- **Graphify como ponte entre a epistemologia de Karpathy e o poder user médio**: [[andrej-karpathy]] projetou esse sistema para si mesmo; [[graphify]] o empacotou em uma skill instalável

## Entidades relacionadas

- [[marc-cleroux]] — autor do post, @tenfoldmarc
- [[graphify]] — skill/ferramenta que escaneia o workspace e gera o grafo
- [[andrej-karpathy]] — sistema original de referência; ex-OpenAI/Tesla; criou o termo "vibe coding"
- [[obsidian]] — ferramenta de visualização do grafo em "graph view"
- [[claude-code]] — ambiente onde o Graphify é instalado e executado

## Conceitos relacionados

- [[otimização-de-tokens]] — técnica nova de redução extrema de consumo (71,5x)
- [[agentes-ia]] — padrão de mediação de contexto via estrutura vs. leitura direta
