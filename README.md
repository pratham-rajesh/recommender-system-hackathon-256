# 🧠 CMPE 256 – Recommender Systems Hackathon (Fall 2025)
### San José State University  
**Instructor:** Prof. Chandrasekar Vuppalapati  
**Course:** CMPE 256 – Recommender Systems  
**Hackathon Dates:** November 1 – 2, 2025
## Team Members
** 1. Venkata Rama Gowri Preetam
** 2. Pratham Rajesh
** 3. Shreram Palanisamy


---

## 🚀 Overview
This repository contains both projects from the **CMPE 256 Data Science Hackathon**, focused on applying machine-learning and AI techniques to practical recommender-system problems.

### 🧩 Projects Included
| Part | Project | Domain | Core Tech |
|------|----------|---------|-----------|
| **1** | 🛒 Electronic Item Checkout Web Portal | Retail / E-commerce | Apriori Association Rule Mining |
| **2** | 🧬 Clinical AI Assistant | Healthcare / Medical Data | Retrieval-Augmented Generation (RAG) with LLMs |

---

## 🛒 Part 1 – Electronic Item Checkout Web Portal

### 🎯 Goal
Design a **Market Basket Recommendation System** for an electronic retailer’s online checkout page.  
When a customer adds items to the cart, the model recommends additional products **frequently bought together**.

### 🧠 Approach
- **Dataset:** `CMPE256_Hackathon_market_basket_analysis_Release.csv` (synthetic transaction data)  
- **Algorithm:** `Apriori` association rule mining from `mlxtend`  
- **Frontend:** Interactive Streamlit web portal replicating SJSU checkout design  
- **Backend:** Python-based rule generation and dynamic recommendation engine  

### ⚙️ Features
- Dynamic cart management (Add / Clear Items)  
- Real-time recommendations based on Apriori rules  
- Rules filtered strictly by full cart antecedents (no partial matches)  
- Intelligent fallback handling when no rules exist for the combination  
- Beautiful UI styled in SJSU colors  
- Dataset statistics and rule exploration  

### 📊 Tech Stack
`Python 3.10+` | `pandas` | `mlxtend` | `streamlit` | `Jupyter/Colab`

### ▶️ Demo Video
📽️ **YouTube Demo:** [Project 1 – Electronic Item Checkout System](https://youtu.be/xno9zIfFzz4)
📽️ **YouTube Demo:** [Project 2 – Medical AI Assistant]([https://youtu.be/xno9zIfFzz4](https://youtu.be/bfn9KeH422g))

### 🖼️ UI Preview
![Electronic Checkout Portal UI](docs/project1_ui.png)

### 🧾 How to Run Locally
```bash
# Clone repository
git clone https://github.com/<your-github-username>/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py

## Part 2 – Clinical AI Assistant
Goal
Build a clinical question-answering assistant that retrieves evidence from structured clinical trial CSVs and unstructured research PDFs, then generates grounded answers with source citations using RAG (Retrieval-Augmented Generation).
Approach
Dual-path retrieval from structured CSVs (DuckDB/SQL) and unstructured PDFs (ChromaDB vector search with BGE-small embeddings).


LLM generation via Groq (Llama-3.3-70B) with a strict “No Data” policy when evidence is lacking.


Domain-aware routing (e.g., diabetes questions prioritize diabetes datasets first).


Gradio UI with title generation, answer panel, and clickable citations.


⚙️ Features
Hybrid retrieval: semantic (ChromaDB + BGE-small-en-v1.5) + keyword SQL (DuckDB)


Intelligent domain routing across Diabetes, COVID-19, Heart Attack, Knee Injuries


PDF chunking + vector store with HNSW index in ChromaDB


Grounded answers with inline citations to CSV rows and PDF snippets


Dynamic title generation (e.g., “Treatment: Diabetes”, “Diagnosis: COVID-19”)


Production-style Gradio UI with SJSU-themed layout


“No Data” fallback when no supporting evidence is retrieved
Tech Stack
Python 3.10+ | pandas | duckdb | PyPDF2 | sentence-transformers (bge-small-en-v1.5) | chromadb | groq (Llama-3.3-70B) | gradio | Jupyter/Colab
▶️ Demo Video
Coming soon
🖼️ UI Preview
Coming soon

How to Run (Google Colab)

Open the Colab via the badge above.


Mount Drive (the notebook includes a cell):

 from google.colab import drive
drive.mount('/content/drive')


Set API Key for Groq:

 import os
os.environ["GROQ_API_KEY"] = "YOUR_KEY_HERE"


Install dependencies (notebook cell installs: groq, chromadb, sentence-transformers, duckdb, PyPDF2, gradio).


Run all cells to:


Load CSVs into DuckDB


Build/Load ChromaDB vector store with bge-small-en-v1.5


Launch the Gradio app (provides a local and a public URL)


Tip: First run builds embeddings (a few minutes). Later runs reuse cached vectors.
