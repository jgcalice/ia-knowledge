---
title: "Amazon KDP"
type: entity
category: platform
tags: [amazon, kdp, self-publishing, digital-products, distribuição]
source_count: 2
last_updated: 2026-05-24
---

# Amazon KDP (Kindle Direct Publishing)

Plataforma de auto-publicação da Amazon — sobe PDF do interior + PDF da capa + metadados, e a Amazon imprime sob demanda e cuida de logística. Royalties pagos no painel.

## Papel no wiki

Camada de distribuição para o arquétipo **low-content digital products** documentado por [[drew-huibregtse]] — livros de colorir, journals, planners. Difere do Amazon FBA ([[shimin-mohammadi]]) por **eliminar qualquer supply chain**: o operador só produz arquivos.

## Stack típico documentado

| Etapa | Ferramenta | Output |
|-------|------------|--------|
| Validação de nicho | [[helium-10]] + Claude | Veredito de viabilidade |
| Conteúdo | Claude | 60+ páginas/prompts |
| Interior visual | Midjourney / Nanobanana / Higgsfield / Leonardo | PDF interior |
| Listing | Claude | Title + bullets |
| Capa | Claude + Canva | PDF capa |
| Publicação | kdp.amazon.com | URL + royalties |

## Aparições no wiki

- [[2026-04-23_drew-huibregtse-sistema-amazon-kdp]] — sistema de 4 passos; geração de imagem via Gemini/Leonardo/Freepik; case $21.626/30 dias
- [[2026-05-09_drew-huibregtse-amazon-kdp]] — pipeline completo de 5 prompts Claude

## Relacionado

- [[drew-huibregtse]] — criador do método documentado
- [[helium-10]] — validação de nicho complementar
- [[shimin-mohammadi]] — par sobre Amazon FBA (físico) — contraponto estrutural
- [[claude-code]] — LLM-base do pipeline
