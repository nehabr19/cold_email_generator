
# 📧 Cold Email Generator for Service-Based Companies

A powerful AI-driven tool designed for business development executives (BDEs) at consulting firms like **AtliQ**. This application automates the process of extracting job requirements from career pages and generating hyper-personalized cold emails that include relevant portfolio links based on the specific tech stack of the job.

## 🚀 The Problem

BDEs often spend hours manually scanning job boards, identifying required skills, and digging through company portfolios to find matching past projects to showcase in a cold email.

## ✨ The Solution

This tool streamlines the entire workflow:

1. **Job Scraping:** Uses `WebBaseLoader` to extract raw data from any job URL.
2. **AI Extraction:** Employs **Llama 3.3 (via Groq)** to parse unstructured text into structured JSON (role, experience, skills, and description).
3. **Vector Search:** Utilizes **ChromaDB** to perform a semantic search on a local portfolio CSV, matching the job's required skills with the most relevant project links.
4. **Personalized Email Generation:** Generates a professional cold email tailored to the specific job, automatically injecting the matched portfolio links.

## 🛠️ Tech Stack

* **Frontend:** Streamlit
* **LLM Orchestration:** LangChain
* **Inference Engine:** Groq Cloud (Llama 3.3 70B)
* **Vector Database:** ChromaDB
* **Data Handling:** Pandas & Regex
* **Language:** Python

## 📦 Project Structure

```text
├── app
│   ├── resource/          # Contains portfolio CSV
│   ├── main.py            # Streamlit UI logic
│   ├── chains.py          # LLM & Prompt templates
│   ├── portfolio.py       # ChromaDB logic
│   └── utils.py           # Text cleaning utilities
├── vectorstore/           # Persistent ChromaDB storage
└── requirements.txt

```

## ⚙️ Setup Instructions

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/cold-email-generator.git

```


2. **Install dependencies:**
```bash
pip install -r requirements.txt

```


3. **Set up API Key:**
Create a `.env` file or use `st.secrets` with your `GROQ_API_KEY`.
4. **Run the app:**
```bash
streamlit run app/main.py

```



---

### Pro-Tip for your GitHub:

Since you fixed those pesky **NumPy** and **Pydantic** errors, I highly recommend including a `requirements.txt` file in your repo with these specific versions to help others avoid the same "dependency hell":

```text
langchain-groq
langchain-community
langchain-core<0.3.0
streamlit
chromadb
pandas
python-dotenv
numpy<2.0.0

```

