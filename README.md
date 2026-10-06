# RAG para Análise de Ativos

## Problema

Modelos de linguagem podem não possuir informações sobre acontecimentos recentes do mercado. Isso dificulta a geração de análises atualizadas sobre ativos financeiros.

## Solução

Criar uma base de notícias recentes de 3 ativos, utilizando 10 notícias por ativo. As notícias foram resumidas por IA, transformadas em embeddings e armazenadas no ChromaDB.

Durante uma consulta, as notícias semanticamente mais relevantes serão recuperadas e fornecidas como contexto para o modelo Qwen gerar a análise do ativo.

## Objetivo

Validar se a utilização de notícias recentes como contexto permite ao Qwen gerar análises mais relevantes e fundamentadas sobre ativos financeiros.

## Stack

* **Python**
* **Qwen** — geração das análises
* **ChromaDB** — armazenamento e recuperação dos embeddings
* **Embeddings** — representação semântica dos resumos
* **JSON** — armazenamento inicial das notícias
