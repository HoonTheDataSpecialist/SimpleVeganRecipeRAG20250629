# 🥗 Vegan Recipe Retrieval with LangChain + ChromaDB

This project demonstrates how to clean, embed, and semantically search through a collection of vegan recipes using a Retrieval-Augmented Generation (RAG) pipeline with LangChain and ChromaDB.

## 📦 Dataset

The recipe data is sourced from Kaggle:

**Vegan Recipes Dataset**  
🔗 https://www.kaggle.com/datasets/rodrigoazs/vegan-recipes  
This dataset contains over 24,000 plant-based recipes including titles, ingredients, and preparation steps.

> 📌 **Note**: Please download the dataset manually from Kaggle and place it in the `Data/` folder.

## 🛠️ Features

- Cleans raw text fields (ingredients and preparation) for consistency
- Preserves paragraph and sentence structure using custom newline normalization
- Converts each recipe section into vector embeddings using `sentence-transformers`
- Stores documents in a persistent Chroma vector store
- Supports semantic search using LangChain’s retriever

## 🧠 Technologies Used

- [LangChain](https://github.com/langchain-ai/langchain)
- [ChromaDB](https://www.trychroma.com/)
- [Sentence-Transformers](https://www.sbert.net/)
- [pandas](https://pandas.pydata.org/)
- [Kaggle Dataset](https://www.kaggle.com/datasets/rodrigoazs/vegan-recipes)

## 🧹 Cleaning Strategy

- `Ingredients\n\n` and `Preparation\n\n` are converted into labeled blocks
- `\n` is replaced with sentence delimiters where appropriate
- Metadata such as `title` and `link` are preserved for context during retrieval

## 📁 Project Structure
.
#### Raw dataset from Kaggle (CSV)
├── Data/
#### Persistent vector store (Chroma)
├── chroma_db/
#### Jupyter Notebook Utilized for Investigation
├── veganRecipeSimpleRAG.ipynb
#### Contains Dependencies Utilized
├── requirements.txt
#### Contains API Keys for Langchasin and OpenAI
├── .env
#### 🧠 This README was generated by ChatGPT to assist with project documentation
└── README.md
