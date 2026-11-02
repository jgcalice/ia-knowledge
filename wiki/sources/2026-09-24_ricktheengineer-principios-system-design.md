---
title: "Princípios Básicos de Design de Sistemas (System Design 101)"
type: source
source_file: "2026-09-24_ricktheengineer_DdrHAI1MrFb.md"
author: "@RickTheEngineer"
date: 2026-09-24
format: reel
tags: [system-design, backend, escalabilidade, arquitetura]
source_url: "https://www.instagram.com/reel/DdrHAI1MrFb/?stkn=MThpOGUwczRqNDE1Nw=="
source_count: 1
---

# Princípios Básicos de Design de Sistemas (System Design 101)

> **Fonte:** [[2026-09-24_ricktheengineer_DdrHAI1MrFb]] | **Autor:** @RickTheEngineer | **Data:** 2026-09-24 | **Formato:** Reel (155s) | **[↗ Ver post](https://www.instagram.com/reel/DdrHAI1MrFb/?stkn=MThpOGUwczRqNDE1Nw==)**

> ⚠️ **Nota editorial:** Conteúdo fora do escopo de IA. Ingerido automaticamente por conta das tags `ia`/`instagram`, mas trata de system design puro, sem menção a LLMs, agentes ou ferramentas de IA.

## TL;DR
Todo componente de um sistema distribuído (load balancer, cache, réplica, shard, CDN, fila) entra porque algo quebrou; a pergunta-guia é "que problema nos forçou a adicionar isto?", e a complexidade só deve crescer quando resolve um gargalo real.

## Contexto
Segundo reel de @RickTheEngineer no wiki, após [[2026-09-06_ricktheengineer-escalar-banco-dados]]. Aqui o foco é o mapa geral: partindo de um app social simples em um único servidor, o autor mostra a sequência de 9 passos que leva a uma arquitetura distribuída.

## O que foi ensinado

1. **Mais servidores + load balancer**: um servidor não aguenta; escala-se horizontalmente e o balanceador distribui requisições entre servidores saudáveis
2. **Cache (Redis)**: servidores castigam o mesmo banco; dados muito lidos saem da memória
3. **Réplicas de leitura**: primário recebe escritas, réplicas atendem leituras
4. **Sharding**: quando um cluster de banco não basta, particiona-se os dados (ex.: por faixa de usuários)
5. **Object storage (S3/R2)**: fotos e vídeos fora do banco relacional
6. **CDN**: cacheia arquivos perto dos usuários ao redor do mundo
7. **Fila + workers**: tarefas lentas (thumbnails, notificações, analytics, transcodificação) rodam de forma assíncrona
8. **Redundância**: múltiplos servidores, dados replicados, health checks, retries, failover — o objetivo não é nunca falhar, é a falha de uma parte não derrubar tudo
9. **Observabilidade**: logs (o que aconteceu), métricas (como o sistema se comporta), traces (caminho de uma requisição entre serviços)

**Custos de cada componente:** caches ficam obsoletos, filas entregam duas vezes, réplicas atrasam, shards dificultam queries, microserviços falham pela rede.

**Erro de iniciante:** adicionar Kafka, Kubernetes, microserviços e 10 bancos antes de ter um problema real.

**Método:** começar simples → achar o gargalo → adicionar o menor componente que o resolve → repetir.

## Insights para o wiki

Fora do escopo de IA; não acrescenta conhecimento sobre ferramentas de IA. Reforça e amplia [[2026-09-06_ricktheengineer-escalar-banco-dados]] (mesma tese: complexidade prematura é o erro mais caro; medir o gargalo antes de escalar). Analogia superficial com o princípio de simplicidade em [[concepts/agentes-ia]] e Claude Code ("Simplicity First"), mas a fonte não faz essa conexão. Mesmo tratamento editorial de [[2026-04-24_nico_fansbuy-importacao-china]].

> Nota: o campo "Insights-chave sobre IA" gerado na captura é apenas um resumo de system design reetiquetado, não conteúdo de IA.

## Entidades relacionadas
- [[ricktheengineer]] — criador do conteúdo

## Conceitos relacionados
- Nenhum conceito de IA relevante identificado neste conteúdo
