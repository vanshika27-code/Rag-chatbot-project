
RAG Chatbot – AI Ethics Knowledge Assistant

A Retrieval-Augmented Generation (RAG) chatbot built using Flowise, Google Gemini Embeddings, and Mistral AI to answer questions from an AI Ethics research document.

📌 Project Description

This project implements a Conversational Retrieval QA system that allows users to interact with a research paper titled:

“AI Ethics: Integrating Transparency, Fairness, and Privacy in AI Development”

Instead of relying purely on a language model, the system retrieves relevant sections from the document and generates grounded responses, reducing hallucinations and improving factual accuracy.

🧠 System Architecture

The RAG pipeline is built visually in Flowise and consists of the following components:

PDF → Text Splitter → Embeddings → Vector Store → Retriever
                                         ↓
                                   Mistral LLM
                                         ↓
                            Conversational QA Chain
                                         ↓
                                    Final Answer
⚙️ Components Used
1️⃣ Recursive Character Text Splitter
Chunk Size: 1000
Chunk Overlap: 200
Splits document into retrievable segments
2️⃣ File Loader
Uploads and parses PDF
Connects with text splitter
3️⃣ Google Gemini Embeddings
Model: gemini-embedding-001
Converts text chunks into vector embeddings
Optimized for retrieval tasks
4️⃣ In-Memory Vector Store
Stores embeddings temporarily
Top-K retrieval: 4
Performs semantic similarity search
5️⃣ Mistral AI (LLM)
Model: mistral-tiny
Temperature: 0.9
Generates natural language responses
6️⃣ Buffer Memory
Maintains conversation context
Enables follow-up question handling
7️⃣ Conversational Retrieval QA Chain
Integrates retriever + LLM + memory
Produces final grounded answer
🚀 How It Works
Upload the PDF document
Split document into chunks
Generate embeddings for each chunk
Store embeddings in vector database
User asks a question
Retriever fetches top relevant chunks
LLM generates response using retrieved context
Memory stores conversation history
🛠️ Tech Stack
Flowise
Google Gemini Embeddings
Mistral AI
Vector Search (In-Memory)
Conversational Retrieval QA
📂 Example Query

User:

What is the document about?

Response:
A structured summary covering:

Ethical concerns in AI
Transparency principles
Fairness and bias mitigation
Privacy safeguards
Responsible AI deployment
🔍 Why RAG?
Reduces hallucinations
Ensures context-grounded responses
Improves reliability
Supports domain-specific Q&A
Scalable for enterprise knowledge systems
📈 Future Improvements
Replace in-memory store with persistent DB (Chroma / Pinecone)
Add source citations in responses
Deploy via REST API
Add authentication & access control
Multi-document support
📸 Screenshots

(Add your two screenshots here)

/screenshots/rag_pipeline.png
/screenshots/chat_output.png
👩‍💻 Author

Developed as part of an academic project on AI Ethics and RAG Systems.
