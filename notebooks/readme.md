# 🚓 RAG-Based QA System Using Local GPT-2 (Notebook Version)

This project implements a Retrieval-Augmented Generation (RAG) system using LangChain and a locally hosted GPT-2 model. It reads traffic stop data from a CSV file and allows users to ask natural language questions about the data.

---

## 📌 Features

- Loads and processes `RIPA_2023_Merged_Cities.csv`
- Builds contextual strings for each row
- Converts rows into vectorized document chunks
- Uses FAISS for similarity search
- Uses HuggingFace's `sentence-transformers` for embeddings
- Loads and uses local GPT-2 model for generation
- Answers user queries based on retrieved context

---

## 🚀 Setup Instructions

1. Clone or download this notebook.
2. Open it in Google Colab or Jupyter.
3. Install the required dependencies:

```bash
pip install -r requirements.txt

4. Upload the dataset: RIPA_2023_Merged_Cities.csv

5. Run the notebook and initialize the class Rag:

## 📁 Files

- `RIPA_2023_Merged_Cities.csv` — dataset file (not included)
- `requirements.txt` — dependencies list

---

## 🛠 Notes

- GPT-2 model runs locally — no API key needed
- Dataset is sampled for performance
- Best used in environments like Google Colab

---

## 📜 License

MIT
