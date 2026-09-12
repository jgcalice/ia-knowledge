---
title: "Skills de Design do Claude: Catálogo Verificado e o Conflito de Atenção entre Skills Concorrentes"
type: source
source_file: "2026-09-07_fabiano_carvalho_DdAPdtbjKt2.md"
author: "@Fabiano Carvalho"
date: 2026-09-07
format: carousel
tags: [claude-skills, prompt-engineering, agentes-ia, design, ferramentas-ia]
source_url: "https://www.instagram.com/p/DdAPdtbjKt2/?img_index=9&stkn=b2I5dzY4aHZzc3Nn"
source_count: 1
---

# Skills de Design do Claude: Catálogo Verificado e o Conflito de Atenção entre Skills Concorrentes

> **Fonte:** [[2026-09-07_fabiano_carvalho_DdAPdtbjKt2]] | **Autor:** @Fabiano Carvalho | **Data:** 2026-09-07 | **Formato:** carousel | **[↗ Ver post](https://www.instagram.com/p/DdAPdtbjKt2/?img_index=9&stkn=b2I5dzY4aHZzc3Nn)**

## TL;DR

Instalar várias [[claude-skills|Claude Skills]] de uma vez não soma benefícios — quando duas ou mais disputam a mesma decisão (ex: estética visual), o resultado vira uma loteria não-reprodutível de sessão para sessão; a única forma confiável de avaliar é instalar uma, testar, comparar e só então adicionar a próxima.

## Contexto

@Fabiano Carvalho anuncia um material com "15 skills grátis do Claude" para design, mas o próprio carousel expõe uma inconsistência editorial proposital: o título promete 15, a peça cataloga 10, uma delas (a última, no slide final) retorna 404 ao ser aberta. O autor usa essa checagem manual — abriu cada link um por um — como prova de rigor e como gancho para a lição central do post: a lista de links importa menos do que o comportamento das skills quando combinadas.

## O que foi ensinado

- **Catálogo verificado (10 de 10 slides, 1 fora do ar):**
  - **UI/UX Pro Max** (`skills.sh/nextlevelbuilder/ui-ux-pro-max-skill`) — layouts, tipografia e interfaces melhores
  - **Impeccable** (`skills.sh/pbakaus/impeccable`) — corrige a "cara de IA" feia em interfaces, refina hierarquia
  - **Taste Skill** (`skills.sh/Leonxlnx/taste-skill`) — dá senso de design/estética ao Claude, saída menos genérica
  - **Humanizer** (`skills.sh/blader/humanizer`) — escrita da IA soa mais humana, menos "cara de IA"
  - **Understand Anything** (`skills.sh/Egonex-AI/Understand-Anything`) — simplifica documentos, pesquisas e conceitos complexos
  - **Frontend Slides** (`skills.sh/zarazhangrui/frontend-slides`) — apresentações com código, slides interativos
  - **Diagram Design** (`skills.sh/cathrynlavery/diagram-design`) — diagramas de fluxos, sistemas e processos
  - **Stop Slop** (`skills.sh/hardikpandya/stop-slop`) — saída menos genérica, menos enrolação, raciocínio e execução melhores
  - **Awesome Design MD** (`skills.sh/VoltAgent/awesome-design-md`)
  - **Design.md** (`skills.sh/google-labs-code/design.md`)
- **O problema não é a lista, é a combinação**: três das skills (as de estética/UI) atacam o mesmo ponto de decisão — como uma interface deve ficar. Com as três instaladas, qual delas "vence" muda de sessão para sessão.
- **Explicação técnica**: skill não é plugin nem modelo — é arquivo de instrução que entra no contexto quando a tarefa combina com sua descrição. Uma skill sozinha muda bastante o resultado porque adiciona instrução nova ao contexto; quinze juntas pioram porque todas competem pelo mesmo espaço de atenção do modelo.
- **Consequência prática**: perde-se a única coisa que importa numa skill de gosto/estética — a capacidade de repetir um resultado que deu certo.
- **Método recomendado (branch-and-compare manual)**: instalar uma skill → rodar uma tarefa já conhecida → comparar a saída nova com a saída antiga lado a lado → anotar o que mudou → só então instalar a próxima. Sem essa comparação, o usuário "acha" que melhorou, mas não sabe.
- **Recomendação de ponto de partida**: quem faz interface começa por **Impeccable** ou **Taste Skill** — nunca as duas ao mesmo tempo. Quem escreve texto começa por **Stop Slop**.

## Insights para o wiki

**Confirmação com nova camada**: o wiki já documentava múltiplas fontes de skills de design ([[vinicius-delmonego]]: Milkovalski Design + Impeccable Design + Taste Skill) e o modelo mental de skill como "micro-agente ativado por frase-gatilho" ([[aashish-pahwa]]). Esta fonte é a primeira a nomear e explicar o **modo de falha** desse ecossistema: skills concorrentes que atacam o mesmo ponto de decisão competem pelo espaço de atenção do contexto e produzem resultado não-determinístico entre sessões. Também é a primeira a propor um **protocolo empírico de instalação incremental** (instalar → testar → comparar → só então adicionar a próxima) como prática recomendada — até agora o wiki só documentava "quais skills instalar", não "como avaliar se instalar mais de uma está ajudando ou atrapalhando".

Confirma também, com fonte independente, os links originais de **Impeccable** (pbakaus) e **Taste Skill** (Leonxlnx) já referenciados de forma genérica em [[claude-skills]] via [[vinicius-delmonego]].

## Entidades relacionadas

- [[claude-skills]] — objeto central do post: catálogo verificado + primeiro relato de conflito entre skills
- [[fabiano-carvalho]] — autor, novo criador BR no wiki

## Conceitos relacionados

- [[agentes-ia]] — skills como micro-agentes que competem por espaço de contexto/atenção quando combinadas
- [[prompt-engineering]] — skill como "arquivo de instrução que entra no contexto quando a tarefa combina"
