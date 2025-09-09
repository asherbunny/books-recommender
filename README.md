# Semantic Book Recommender

A simple, end‑to‑end book recommender I built with LLMs and semantic search. It finds books by meaning (not just keywords), tags them as Fiction / Nonfiction, and scores the emotion/mood of descriptions. A small Gradio app lets you search and filter interactively.

# What it does

* Searches books by meaning using text embeddings.
* Classifies books as Fiction or Nonfiction (zero‑shot).
* Extracts emotion signals (e.g., joy, sadness, fear) from descriptions.
* Shows results in a clean web UI with filters.
# Tech & models I used
Shows results in a clean web UI with filters.
* OpenAI — embeddings and (optionally) LLM responses.

* Hugging Face / Transformers

* facebook/bart-large-mnli → zero‑shot classification (Fiction vs. Nonfiction)

* j-hartmann/emotion-english-distilroberta-base → emotion analysis

* LangChain — orchestration and integrations (langchain-community, langchain-openai, langchain-chroma).

* Chroma (chromadb) — vector database for fast similarity search.

* Gradio — lightweight web UI for queries and filters.

* Pandas — data loading/cleaning.

* python-dotenv — keep API keys out of code.

# How it works

1. Clean the data and build a rich description field for each book.

2. Create embeddings (OpenAI) and store them in Chroma.

3. Use zero‑shot (bart-large-mnli) to tag Fiction/Nonfiction.

4. Run emotion analysis to get mood scores per book.

5. The Gradio app performs a vector search, applies filters, and displays ranked results.

# Why I built it

I wanted a practical way to learn LLMs, Hugging Face models, LangChain workflows, and vector search—and to package everything into a small, useful app I can demo.

In order to create your vector database, you'll need to create a .env file in your root directory containing your OpenAI API key. Instructions on how to do this are part of the tutorial.

The data for this project can be downloaded from Kaggle. Instructions on how to do this are also in the repo.

