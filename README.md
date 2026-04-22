# Adaptive Multi-Granularity RAG for Academic QA

## Overview
This project presents a modular Retrieval-Augmented Generation (RAG) system for academic paper question answering. It addresses the problem of retrieval scope mismatch by dynamically adapting retrieval granularity and combining hybrid retrieval, reranking, and context expansion.

---

## Problem
Academic QA tasks vary significantly in scope. Some questions require precise factual retrieval, while others require broader contextual understanding. Traditional fixed-size chunking often leads to irrelevant or insufficient evidence.

---

## Solution
This system introduces an adaptive multi-granularity RAG pipeline:

- Multi-granularity chunking (sentence, paragraph, section)  
- Query routing based on question intent  
- Hybrid retrieval (dense + BM25 + sparse)  
- Reciprocal Rank Fusion (RRF)  
- Cross-encoder reranking  
- Context expansion  
- Grounded answer generation  

---

## System Architecture
The system is organized into modular components:

- Chunking  
- Embedding  
- Retrieval  
- RAG pipeline  
- Evaluation  

---

## Key Features

- Adaptive retrieval granularity based on query type  
- Hybrid retrieval combining multiple retrieval strategies  
- Reranking for improved evidence precision  
- Context expansion for better answer completeness  
- Evaluation-driven design with retrieval and generation metrics  

---

## Demo

Below is an example interface of the system:

![Demo](screenshots/demo.png)

Example queries and outputs are available in:  
`demo/example_queries.md`

---

## Evaluation Highlights

- Improved retrieval accuracy (Hit Rate, MRR)  
- Stable generation quality (ROUGE-L, Faithfulness)  
- Better alignment between query type and retrieved context  

---

## Tech Stack

- Python  
- FAISS  
- BM25  
- Sentence Transformers  
- Cross-Encoder Reranker  
- Flask  

---

## How to Run

```bash
pip install -r requirements.txt
python web_app.py
