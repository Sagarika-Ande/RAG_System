# RAG System
RAG (Retrieval-Augmented Generation) combines information retrieval with generative AI models.
• Retrieves relevant documents from a knowledge base.
• Uses them to augment the input prompt for a language model.
• Generates accurate, context-rich responses.

# Types of RAG
1️⃣ Basic RAG-Retrieves documents based on the query and generates an answer using them.
2️⃣ Semantic RAG-Retrieves documents based on semantic (meaning-based) similarity, not just keywords.
3️⃣ Agentic RAG-Uses intelligent agents to plan, retrieve, and generate answers by deciding the best actions.

# 1.Basic RAG Architecture
User Query 
      │
Retriever (BM25 / Vector DB like FAISS)
      │
Retrieved Documents (text chunks)
      │
LLM (e.g. GPT-4, LLaMA) + Documents as Context
      │
Generated Response

# Semantic RAG Architecture 
User Query
      │
Semantic Retriever (e.g. Sentence-BERT embeddings)
      │
Ranked Documents / Multi-source Knowledge (could be docs, metadata, APIs)
      │
LLM + Retrieved Knowledge as Context
      │
Generated Response

# Agentic RAG Architecture 
User Query
      │
Agent (LangChain Agent, CrewAI, or AutoGen)
      │
[Dynamic Decision: retrieve docs? call API? query DB?]
      │
Tool Calls / Document Retrieval / API calls
      │
Intermediate Results
      │
Agent Decision (optional multi-hop reasoning)
      │
LLM Final Response Generation

# Real-World Examples
Traditional RAG:
      Customer Support Chatbots
      Medical Information Assistant
Semantic RAG:
      Multilingual Knowledge Assistant
      Contextual News Summarizer
Agentic RAG:
      Healthcare Diagnostic AI
      Smart Travel Planning Assistant

# Agentic RAG:
# Library / Tool	                                                                                        Description
LangChain TextSplitters(RecursiveCharacterTextSplitter)                          Most popular, supports fixed, recursive, token-based, semantic splitters                  
Sentence Transformers	                                                           Can be used for semantic chunking via similarity scores


# Database	
FAISS	                                                                            Facebook AI, super fast, in-memory/local
