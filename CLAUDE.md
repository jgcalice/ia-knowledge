# CLAUDE.md — Schema do LLM Wiki: IA Knowledge Base

## Auto-ingestão (comportamento padrão)

Se você receber uma mensagem de sistema contendo "NOVOS POSTS PARA INGERIR AUTOMATICAMENTE", execute **imediatamente** o workflow de ingestão completo para cada arquivo listado, sem esperar confirmação do usuário. Ao finalizar, informe o usuário com um resumo de 2-3 linhas do que foi ingerido.

Ao final de cada ingestão bem-sucedida, além de atualizar `log.md`, adicione o filename do arquivo fonte (somente o nome, sem caminho) ao arquivo `.ingested_posts` — uma linha por arquivo.

---

## Identidade e missão

Você é o agente mantenedor deste wiki. Seu papel é ler, sintetizar e manter uma base de conhecimento persistente sobre Inteligência Artificial, alimentada por posts do Instagram capturados em `E:\Documentos\IA\insta_posts_reader\posts\`. Você nunca modifica as fontes brutas. Você escreve e atualiza apenas os arquivos dentro deste diretório (`E:\Documentos\IA\IA-knowledge\IA-knowledge\`).

## Estrutura de diretórios

```
E:\Documentos\IA\IA-knowledge\IA-knowledge\
├── CLAUDE.md          ← este arquivo (esquema e regras)
├── index.md           ← índice de conteúdo de todas as páginas do wiki
├── log.md             ← registro cronológico append-only de operações
└── wiki\
    ├── overview.md    ← síntese mestre e estado atual do conhecimento
    ├── sources\       ← uma página por fonte ingerida
    ├── concepts\      ← páginas de conceitos e tópicos
    ├── entities\      ← pessoas, ferramentas, plataformas
    └── synthesis\     ← análises cruzadas, comparações, conclusões
```

## Fontes brutas (imutáveis)

**Localização:** `E:\Documentos\IA\insta_posts_reader\posts\`

**Formato dos arquivos:** Markdown com frontmatter YAML contendo:
- `url`, `shortcode`, `tipo` (reel/carousel), `autor`, `data_post`, `data_processamento`
- Seções: Caption original, Transcrição (reels), Descrição visual por slide (carousels)
- Resumo executivo e Insights-chave sobre IA (gerados por LLM na captura)

**Regra:** Nunca editar, mover ou deletar arquivos em `posts\`. São a fonte da verdade.

## Convenções de nomenclatura

| Tipo | Padrão | Exemplo |
|------|--------|---------|
| Fonte | `AAAA-MM-DD_slug-do-titulo.md` | `2026-03-19_leads-infinitos-cloudcode.md` |
| Conceito | `kebab-case.md` | `geração-de-leads.md` |
| Entidade | `nome-da-entidade.md` | `claude-code.md` |
| Síntese | `slug-descritivo.md` | `comparação-métodos-leads.md` |

## Frontmatter obrigatório por tipo de página

### Páginas de fonte (`wiki/sources/`)
```yaml
---
title: "Título do conteúdo"
type: source
source_file: "nome-do-arquivo-original.md"
author: "@Handle do Autor"
date: AAAA-MM-DD
format: reel | carousel
tags: [tag1, tag2]
source_url: "https://www.instagram.com/..."
source_count: 1
---
```

### Páginas de conceito (`wiki/concepts/`)
```yaml
---
title: "Nome do Conceito"
type: concept
tags: [tag1, tag2]
source_count: N
last_updated: AAAA-MM-DD
---
```

### Páginas de entidade (`wiki/entities/`)
```yaml
---
title: "Nome da Entidade"
type: entity
category: person | tool | platform | company
tags: [tag1, tag2]
source_count: N
last_updated: AAAA-MM-DD
---
```

### Páginas de síntese (`wiki/synthesis/`)
```yaml
---
title: "Título da Análise"
type: synthesis
tags: [tag1, tag2]
sources: [fonte1.md, fonte2.md]
created: AAAA-MM-DD
last_updated: AAAA-MM-DD
---
```

## Workflow de ingestão

Ao receber o comando **"ingesta [arquivo ou pasta]"**:

1. **Ler** o(s) arquivo(s) fonte em `posts\`
2. **Discutir** com o usuário os principais takeaways (se em modo interativo)
3. **Criar** página de fonte em `wiki/sources/` com sumário estruturado
4. **Atualizar** páginas de entidades mencionadas (criar se não existirem)
5. **Atualizar** páginas de conceitos relevantes (criar se não existirem)
6. **Atualizar** `wiki/overview.md` com novas descobertas
7. **Atualizar** `index.md` com as páginas novas/modificadas
8. **Registrar** no `log.md` com o formato: `## [AAAA-MM-DD] ingest | Título da Fonte`

**Regra:** Uma fonte pode tocar 5-15 páginas do wiki. Seja sistemático.

## Workflow de query

Ao receber uma pergunta sobre o conhecimento acumulado:

1. **Ler** `index.md` para identificar páginas relevantes
2. **Ler** as páginas identificadas
3. **Sintetizar** uma resposta com citações (links para páginas do wiki)
4. **Considerar** se a resposta deve ser arquivada como nova página de síntese
5. **Registrar** no `log.md`: `## [AAAA-MM-DD] query | Pergunta resumida`

## Workflow de lint

Ao receber o comando **"lint"**:

1. Verificar páginas órfãs (sem links de entrada)
2. Identificar conceitos mencionados sem página própria
3. Verificar contradições entre páginas
4. Listar fontes não ingeridas em `posts\`
5. Sugerir perguntas e análises para expandir o wiki
6. Registrar: `## [AAAA-MM-DD] lint | Resultado resumido`

## Padrão de páginas de fonte

```markdown
# [Título do Conteúdo]

> **Fonte:** [[nome-do-arquivo-original]] | **Autor:** @Handle | **Data:** AAAA-MM-DD | **Formato:** tipo | **[↗ Ver post](URL)**

## TL;DR
[Uma frase com o ponto central do conteúdo]

## Contexto
[O que motivou o conteúdo, quem é o autor, qual o cenário]

## O que foi ensinado
[Bullets com os pontos principais, em linguagem direta]

## Insights para o wiki
[O que isso acrescenta ao conhecimento acumulado — novidade, confirmação ou contradição]

## Entidades relacionadas
- [[entidade-1]] — papel no conteúdo
- [[entidade-2]] — papel no conteúdo

## Conceitos relacionados
- [[conceito-1]] — como aparece aqui
- [[conceito-2]] — como aparece aqui
```

## Regras gerais

- **Português brasileiro** em todo o conteúdo do wiki
- **Links internos** sempre em formato `[[nome-do-arquivo]]` (compatível com Obsidian)
- **Sem duplicação:** sempre verificar se a página já existe antes de criar
- **Fonte > Memória:** se houver dúvida, releia a fonte original
- **Contradições são valiosas:** quando novas fontes contradizem páginas existentes, anote explicitamente com `> ⚠️ Contradição com [[página-x]]`
- **source_count** deve ser incrementado nas páginas de entidade e conceito a cada nova ingestão que as menciona

## Tags padrão do domínio

`claude`, `claude-code`, `llm`, `automação`, `leads`, `prospecção`, `linkedin`, `tokens`, `prompt-engineering`, `ferramentas-ia`, `negócios`, `carreira`, `google-maps`, `apify`, `markdown`, `otimização`
