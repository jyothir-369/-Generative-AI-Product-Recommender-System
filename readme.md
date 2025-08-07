🧠 Generative AI Product Recommender System
This project presents a smart product recommendation system developed as a demonstration of applying Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) pipelines to real-world product discovery scenarios. It allows users to input natural language queries (e.g., job descriptions or role summaries) and receive precise recommendations for relevant SHL products.

🚀 Key Features
🔍 Semantic Search using FAISS over a structured product metadata catalog

🧠 LLM-Based Reranking with Claude 3 Haiku to enhance result precision

📋 Rich Metadata Display:

Duration

Product type

Remote compatibility

Adaptive support

Download availability

🎯 Precision Mode: Retrieves the Top 3 most relevant products

⚙️ FastAPI Backend with a simple /recommend API endpoint

🖼️ Streamlit Frontend for interactive querying

💬 Optional Conversational Chatbot (step1_rag.py) powered by Gemini, DeepSeek, or LLaMA3

📁 Project Structure
bash
Copy
Edit
shl-recommender/
├── data/              # Product metadata and FAISS index
├── recommender/       # Core recommendation logic
│   └── core.py
├── streamlit_app/     # Streamlit-based frontend
│   └── app.py
├── api/               # FastAPI backend server
│   └── main.py
├── scraping/          # Web scraping scripts using Selenium + BeautifulSoup
├── step1_rag.py       # Optional multimodal chatbot integration
├── SHL_Generative_AI_Summary.pdf # Final summary report
├── requirements.txt   # Python dependencies
├── README.md          # Project documentation
└── .devcontainer/     # Dev container config (optional)
🧰 Tech Stack
Component	Tool / Library
Embeddings	BAAI bge-small-en-v1.5
Vector DB	FAISS
Reranker	Claude 3 Haiku (via OpenRouter)
Frontend	Streamlit
Backend	FastAPI
Chatbot	Gemini, DeepSeek, LLaMA3
Scraping	Selenium + BeautifulSoup

▶️ Getting Started
1. Clone the repository
bash
Copy
Edit
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
Test the endpoint:
http://localhost:8000/recommend?q=productivity manager

4. Start the Streamlit Frontend
bash
Copy
Edit
streamlit run streamlit_app/app.py
Access frontend locally at:
http://localhost:8501

Or via network:
http://<your-ip>:8501

🌐 Deployment
Component	URL
Live UI	Streamlit App
API Endpoint	Coming soon
GitHub Repo	SHL-RAG-assignment
