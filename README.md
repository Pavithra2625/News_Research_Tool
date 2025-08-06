# News_Research_Tool
RockyBot(News_Research_Tool) is an AI-powered tool that fetches and analyzes news articles from URLs. It uses Groq LLM and HuggingFace embeddings to provide summarized answers with sources. Built with Gradio and FAISS, it enables easy question answering over multiple articles.

RockyBot: News Research Tool (Groq + LangChain + Gradio)
Overview
RockyBot is an AI-powered tool that helps you analyze and summarize news articles from multiple URLs.
It retrieves content from web pages, stores it in a vector database, and uses Groq’s LLM to answer questions and provide summarized insights with sources.

This project does not require OpenAI and works entirely with Groq LLM + HuggingFace embeddings.

Features
Fetches and processes multiple news article URLs

Splits text into chunks for efficient search

Generates embeddings using HuggingFace

Stores and queries data with FAISS vector database

Answers user questions with Groq LLM

Provides sources for transparency

Interactive Gradio web interface

Tech Stack
  Python 3.10+

  LangChain for Retrieval QA

  Groq LLM via langchain-groq

  HuggingFace Sentence Transformers for embeddings

  FAISS for vector storage

  Gradio for UI

  Unstructured for URL content loading

Installation
1. Clone the Repository

       git clone https://github.com/yourusername/rockybot-news-research.git

       cd rockybot-news-research

3. Install Dependencies
      For local environment:

        pip install langchain langchain-community langchain-groq gradio faiss-cpu sentence-transformers unstructured requests
      For Google Colab:

      python

        !pip install langchain langchain-community langchain-groq gradio faiss-cpu sentence-transformers unstructured requests
      Configuration
          Get a Groq API Key from Groq Console.

Set it in your environment:

python

import os
os.environ["GROQ_API_KEY"] = "your_groq_api_key_here"
Usage

Run the program:

python rockybot.py
Gradio will launch a local web interface.

In the UI:

Enter up to 3 news article URLs

Click Process URLs → Data is fetched, embedded, and stored in FAISS

Type a question about the articles

View the answer with sources

Example Questions
“Summarize the main points from these articles.”

“Which companies are mentioned in the news?”

“What are the similarities between the CNN and BBC articles?”

“What dates or events are highlighted?”

Example Output
makefile
Copy
Edit
Answer:
AI companies announced major updates to their LLM platforms. 
The Verge highlighted consumer AI improvements.

Sources:
https://www.bbc.com/news/world-asia-67577425
https://www.theverge.com/2025/08/05/latest-ai-updates
Notes
Only works with public, non-paywalled URLs

Some sites may block scraping or require JavaScript rendering

If a URL fails to load, an error message will be shown

Processed data is saved in faiss_store_groq.pkl

