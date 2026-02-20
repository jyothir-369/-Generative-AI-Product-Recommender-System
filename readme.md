# 🧠 Generative AI Product Recommender System

This project presents a smart product recommendation system that demonstrates the application of **Large Language Models (LLMs)** and **Retrieval-Augmented Generation (RAG)** pipelines in real-world product discovery scenarios. Designed for enhanced user experience and decision-making, the system allows users to input **natural language queries** (e.g., job descriptions or role summaries) and receive precise, metadata-rich recommendations for SHL products.

---

## 🚀 Key Features

- 🔍 **Semantic Search**  
  Uses **FAISS** to perform fast, similarity-based retrieval over structured product metadata.

- 🧠 **LLM-Based Reranking**  
  Enhances precision using **Claude 3 Haiku** (via OpenRouter) to rerank top results intelligently.

- 📋 **Rich Metadata Display**  
  - Product Duration  
  - Product Type  
  - Remote Compatibility  
  - Adaptive Support  
  - Download Availability  

- 🎯 **Precision Mode**  
  Returns the **Top 3** most relevant SHL products per query.

- ⚙️ **FastAPI Backend**  
  Simple RESTful endpoint at `/recommend`.

- 🖼️ **Streamlit Frontend**  
  Clean, interactive user interface for querying and viewing recommendations.

- 💬 **Optional Conversational Chatbot**  
  Integrated multimodal chatbot using **Gemini**, **DeepSeek**, or **LLaMA3** for richer user engagement (`step1_rag.py`).

---


Alternative compact & stylish version (very popular in 2024–2025 repos):

```markdown
## 📁 Project Layout

```text
shl-recommender/
├─ data/                    → product data & FAISS index
├─ recommender/             → core recommendation logic
│  └─ core.py
├─ streamlit_app/           → Streamlit frontend
│  └─ app.py
├─ api/                     → FastAPI backend
│  └─ main.py
├─ scraping/                → data collection scripts
├─ step1_rag.py             → optional RAG / LLM prototype
├─ SHL_Generative_AI_Summary.pdf
├─ requirements.txt
├─ README.md
└─ .devcontainer/           → (optional) dev container config

---

## 🧰 Tech Stack

| Component       | Tool / Library                |
|----------------|-------------------------------|
| Embeddings      | `BAAI/bge-small-en-v1.5`       |
| Vector DB       | FAISS                         |
| Reranker        | Claude 3 Haiku (via OpenRouter) |
| Frontend        | Streamlit                     |
| Backend         | FastAPI                       |
| Chatbot         | Gemini, DeepSeek, LLaMA3      |
| Scraping        | Selenium + BeautifulSoup      |

---

## ▶️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/jyothir-369/SHL-RAG-assignment.git
cd SHL-RAG-assignment
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Launch the FastAPI Backend
bash
Copy
Edit
uvicorn api.main:app --reload
Test endpoint at: http://localhost:8000/recommend?q=productivity manager

4. Start the Streamlit Frontend
bash
Copy
Edit
streamlit run streamlit_app/app.py
Access UI locally at: http://localhost:8501

🌐 Deployment
Component	URL / Status
Live UI	Coming Soon
API Endpoint	Coming Soon
GitHub Repo	SHL-RAG-assignment

🙌 Acknowledgements
Special thanks to OpenRouter, SHL, and the open-source communities for enabling this real-world LLM integration project.

📫 Contact
If you'd like to collaborate or discuss improvements, feel free to reach out via GitHub or connect on LinkedIn.
