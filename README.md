# 🧠 CMPE 256 – Recommender Systems Hackathon (Fall 2025)
### San José State University  
**Instructor:** Prof. Chandrasekar Vuppalapati  
**Course:** CMPE 256 – Recommender Systems  
**Hackathon Dates:** November 1 – 2, 2025  

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
