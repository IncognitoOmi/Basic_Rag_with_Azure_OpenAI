# Basic RAG using LangChain & Azure OpenAI

This repository demonstrates a **Basic Retrieval-Augmented Generation (RAG) pipeline** using **LangChain** and **Azure OpenAI**. The goal is to retrieve relevant information from Azure AI Search and generate responses using OpenAI's GPT models.

## 🚀 Features
- Uses **LangChain** for building the RAG pipeline.
- Integrates **Azure OpenAI** (GPT-4o-mini) as the LLM.
- Supports **environment variable-based configuration**.
- Includes **LangSmith tracking** for monitoring queries.

## 📦 Installation & Setup

### 1️⃣ Clone the Repository
```sh
git clone <repository_url>
cd <repository_folder>
```

### 2️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

### 3️⃣ Configure Environment Variables
Create a `.env` file and set the following variables:
```ini
AZURE_OPENAI_API_KEY=your_openai_api_key
AZURE_OPENAI_ENDPOINT=your_azure_endpoint
LANGCHAIN_API_KEY=your_langchain_key
LANGCHAIN_PROJECT=your_project_name
```

## ⚡ Usage
Run the notebook using Jupyter:
```sh
jupyter notebook basic_rag.ipynb
```

## 📝 Example Query
```python
from langchain_openai import AzureChatOpenAI

llm = AzureChatOpenAI(model="gpt-4o-mini", api_version="2024-05-01-preview")
response = llm.invoke("What is Azure AI Search?")
print(response)
```

## 📌 Notes
- Ensure you have access to **Azure OpenAI** services.
- Modify the **retriever and pipeline** as per your use case.
- Enable **LangSmith tracing** for debugging and performance tracking.

## 🤝 Contributing
Feel free to submit issues or pull requests to improve this project.


