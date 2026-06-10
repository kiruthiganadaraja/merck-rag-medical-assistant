# merck-rag-medical-assistant
A Retrieval-Augmented Generation (RAG) system built on the Merck Manuals that helps healthcare professionals get fast, reliable answers to clinical questions on diagnoses, treatments, and emergency protocols.
Medical RAG Assistant — Merck Manual Knowledge System

Healthcare professionals operate under constant information overload, navigating thousands of pages of medical literature while making time-sensitive decisions. Quick, trustworthy access to authoritative medical knowledge is essential for accurate diagnoses, effective treatment planning, and consistent standards of care — especially in critical and emergency settings.

This project develops a Retrieval-Augmented Generation (RAG) based AI assistant grounded in the Merck Manuals (4,000+ pages across 23 sections of trusted clinical reference material). The system streamlines access to verified medical knowledge, supports faster clinical decision-making, and helps standardize care practices by ensuring every answer is anchored in renowned medical literature.

Key objectives

Reduce information overload for healthcare professionals
Enable fast, accurate retrieval of clinical knowledge from trusted sources
Support diagnostic and treatment decision-making with grounded, citation-backed answers
Demonstrate the feasibility of RAG-based AI assistants in real-world clinical workflows
Sample clinical questions answered

Protocol for managing sepsis in a critical care unit
Symptoms, medical vs. surgical management of appendicitis
Causes and treatment of sudden patchy hair loss (e.g., alopecia areata)
Treatment recommendations for traumatic brain injury (TBI)
Precautions, treatment, and recovery for a leg fracture sustained during hiking
Approach

PDF ingestion and parsing of the Merck Manual corpus (4,000+ pages, 23 sections)
Text chunking with overlap to preserve clinical context
Embedding generation using a sentence-transformer / OpenAI embedding model
Vector storage and similarity search via a vector database (FAISS / ChromaDB)
Retrieval pipeline that fetches the most relevant manual excerpts per query
LLM-based answer generation grounded strictly in retrieved context (RAG)
Prompt engineering to enforce medical accuracy, citation of sources, and safe-response behavior
Evaluation on the provided clinical question set for relevance, correctness, and completeness
Tech stack: Python, LangChain, OpenAI / Hugging Face LLMs, Sentence-Transformers, FAISS / ChromaDB, PyPDF / PyMuPDF, Tiktoken, Google Colab (T4 GPU), Jupyter Notebook

Deliverables: End-to-end RAG pipeline, vector index built from the Merck Manuals, working prototype that answers clinical queries with cited sources, and demonstrated responses to the benchmark clinical question set.

⚠️ Disclaimer: This project is a research prototype intended to demonstrate the feasibility of RAG in clinical knowledge retrieval. It is not a substitute for professional medical advice, diagnosis, or treatment. All clinical decisions must be made by qualified healthcare professionals.

Tech Stack (detailed)
Programming Language

Python 3
LLM & RAG Framework

LangChain — orchestration of retrieval and generation pipelines
OpenAI API (GPT models) / Hugging Face Transformers — large language model backbone
Prompt templates for grounded, citation-aware responses
Embeddings & Vector Search

Sentence-Transformers (e.g., all-MiniLM-L6-v2) or OpenAI text-embedding-ada-002
FAISS / ChromaDB — vector database for semantic similarity search
Tiktoken — token counting and chunk-size management
Document Processing

PyPDF / PyMuPDF (fitz) / pdfplumber — PDF parsing of the Merck Manuals
LangChain RecursiveCharacterTextSplitter — context-preserving chunking
Data Manipulation

Pandas — managing chunk metadata and evaluation results
NumPy — numerical operations on embeddings
Development Environment

Jupyter Notebook
Google Colab with T4 GPU runtime
Google Drive integration for storing the Merck Manual PDF and vector index
Techniques Applied

Retrieval-Augmented Generation (RAG) architecture
Document chunking with overlap for context retention
Dense vector embeddings and semantic search
Top-k retrieval with similarity scoring
Prompt engineering for clinical accuracy and source citation
Grounded generation to minimize hallucinations
Qualitative evaluation against benchmark clinical questions

Quick mentions:
Python · LangChain · OpenAI / Hugging Face LLMs · Sentence-Transformers · FAISS / ChromaDB · PyPDF · Tiktoken · Google Colab (T4 GPU) · Jupyter Notebook
