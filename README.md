# Mini-RAG-Chatbot: A Localized Q&A System with Open LLMs
Mini-RAG-Chatbot is a lightweight Retrieval-Augmented Generation (RAG) system that allows users to ask questions based on a custom knowledge base (e.g., documents, articles, research papers). It combines vector similarity search (via FAISS) with open-source large language models (LLMs) to deliver contextually accurate, natural language answers.


## Features
* Context-Aware Q&A using Retrieval-Augmented Generation

* Open-Source LLMs (e.g., Mistral-7B) via Hugging Face Transformers

* FAISS for fast vector-based document retrieval

* Sentence-Transformers for efficient embedding

* Gradio UI for a clean and simple chatbot interface

* Modular code structure for easy customization and scaling


## Tech Stack
* Python

* PyTorch

* Hugging Face Transformers

* Sentence Transformers

* FAISS

* LangChain / LlamaIndex (optional)

* Gradio / Streamlit (Gradio used here)



## Project Structure
```
mini-rag-chatbot/
│
├── data/                  # Custom knowledge base files (e.g., .txt, .pdf)
├── src/
│   ├── embedder.py        # Loads documents, computes embeddings, builds FAISS index
│   ├── retriever.py       # Retrieves top-k context chunks using semantic search
│   ├── chatbot.py         # LLM-based answer generation using Hugging Face
│   └── app.py             # Gradio app for user interaction
├── requirements.txt       # Dependencies
├── README.md              # Project overview and documentation
└── .gitignore
```

## How It Works
1. Document Ingestion: Loads .txt files from the data/ directory

2. Embedding: Converts text into vector representations using Sentence Transformers

3. Indexing: Stores vectors in a FAISS index for fast similarity search

4. Query Handling: Takes a user question and retrieves relevant documents

5. Generation: Feeds the context + query into a LLM to generate a natural answer

6. Interface: Outputs the answer in a simple chatbot UI


## Setup Instructions

1. Clone the repo
   
```bash
git clone https://github.com/yourusername/mini-rag-chatbot.git
cd mini-rag-chatbot
```


2. Create a virtual environment

* On macOS / Linux:

```bash   
python3 -m venv venv
source venv/bin/activate
```

* On Windows (CMD):

```bash
python -m venv venv
venv\Scripts\activate
```

3. Add your documents

```bash
Place your .txt files inside the data/ folder.
```

4. Install required packages

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

5. Run the project

```bash
python src/embedder.py     # Build FAISS vector index
python src/app.py          # Launch Gradio chatbot interface
```


## Future Work
 * Add support for .pdf or .docx ingestion

 * Swap Mistral-7B with a quantized version for smaller environments

 * Add feedback collection (thumbs up/down)

 * Explore LoRA or QLoRA fine-tuning

 * Expand to multimodal RAG (image + text)


## What I Learned
* Built an end-to-end RAG pipeline using open tools

* Explored document embedding and vector search with FAISS

* Integrated custom context into LLM prompts

* Learned how to create usable AI interfaces with Gradio

* Practiced clean, modular Python design for reproducibility


## License
This project is open-source under the MIT License.

