---
layout: page
title: ENU Research Finder — Semantic Paper Search
description: Embedding-based search, expert ranking, and co-authorship graphs over ENU research
img: assets/img/5.jpg
importance: 2
category: work
related_publications: false
---

ENU Research Finder is a semantic search tool over research papers from L.N. Gumilyov
Eurasian National University, collected from the OpenAlex API. Built during the
Yessenov Data Lab 2026 bootcamp.

**Highlights**

- Similarity search over paper abstracts using 1024-dimensional text embeddings.
- "More like this" recommendations and expert ranking by topic.
- Co-authorship graphs built with NetworkX.
- LLM-generated keywords and "why is this relevant" explanations for each result.

**Stack:** Python, Transformers (text-1024, gemma4), NetworkX, OpenAlex API, Streamlit.
