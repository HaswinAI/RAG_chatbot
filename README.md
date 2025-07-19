# 📚 RAG Chatbot – PDF Q&A with LangChain + Groq
# A Retrieval-Augmented Generation (RAG) chatbot that answers questions from uploaded PDFs. Built using LangChain, Groq LLMs (LLaMA 3), FAISS, HuggingFace Embeddings, and Streamlit.

# 🧠 What This Project Does
🗂 Uploads a PDF document

📖 Reads and chunks the content into manageable parts

🔢 Converts chunks into embeddings using HuggingFace models

💾 Stores embeddings in a FAISS vector store

❓ Accepts user queries and retrieves top-matching chunks

🧠 Sends the context to Groq’s LLaMA 3 model to generate an answer

💬 Displays accurate, document-based responses in real-time

# 🔁 Workflow

PDF Upload
 → Text Extraction
   → Chunking
     → Embedding (HuggingFace)
       → FAISS Vector Store

User Query
 → Embedding
   → Search FAISS for Relevant Chunks
     → Generate Answer with Groq LLM
🧰 Tech Stack
Tool	Role
🦜 LangChain	LLM and retrieval framework
🧠 Groq	LLM inference (e.g. llama3-70b-8192)
🧠 HuggingFace	Embedding model (all-MiniLM-L6-v2)
📚 FAISS	Vector search for chunk similarity
📑 PyPDF2	PDF text extraction
⚡ Streamlit	UI to upload and chat
🔐 Dotenv	Secure API key handling

📁 Project Structure

rag-chatbot/
├── app.py              # Streamlit UI
├── rag_chain.py        # Retrieval and LLM logic
├── utils.py            # PDF reading and chunking
├── requirements.txt    # Required packages
├── .env                # API keys (not pushed)
├── data/               # Uploaded PDFs (ignored)
└── README.md           # You are here
🛠 Installation
Clone this repo:


git clone https://github.com/HaswinAI/RAG-chatbot.git
cd rag-chatbot-groq
Create a virtual environment:


python -m venv chatbot
source chatbot/bin/activate  # or chatbot\Scripts\activate on Windows
Install requirements:


pip install -r requirements.txt
Set up .env:


GROQ_API_KEY=your_actual_groq_key_here
▶️ Run the App

streamlit run app.py
Go to localhost in your browser.

💬 Example Use
Upload a whitepaper or article PDF

Ask: "What are the key takeaways?"

Get an instant, AI-generated summary based on the real content

📌 Notes
PDF contents are not stored permanently

.env, .pdf files, and data/ are in .gitignore

Compatible with models like:

llama3-70b-8192

llama3-8b-8192

gemma-7b-it

mixtral-8x22b

📄 License
This project is released under the MIT License

✨ Acknowledgements
LangChain

Groq

FAISS by Meta

HuggingFace Sentence Transformers

Streamlit

# Creator - HASWIN
