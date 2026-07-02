🧠 Medical Chatbot on CPU using LLaMA 2 – 100% Open Source

This project is a fully offline **Medical Chatbot** built with **LLaMA 2**, running entirely on **CPU** using open-source tools. It reads medical PDF documents and answers user questions using a local language model – **no cloud**, **no API keys**, and **no GPU** required.



🚀 Features

- 💬 Ask natural language questions about your own medical PDFs  
- 🧠 Powered by **LLaMA 2 7B GGML** (.bin format)  
- 📄 Embeds content from medical books using sentence-transformers  
- 🔍 Fast vector search with **FAISS (CPU)**  
- ⚡ Interactive chat UI with **Chainlit**  
- ✅ Shows the **actual chunks of data used** to answer your question (retrieval transparency)



🧪 Tech Stack

- **LangChain** – LLM orchestration & document handling  
- **Sentence Transformers** – Efficient embeddings on CPU  
- **FAISS (CPU)** – Fast local vector search  
- **LLaMA 2 (GGML format)** – Local language model  
- **Chainlit** – Real-time, chat-ready frontend for LLMs  

 📁 Pipeline

Medical PDF → LangChain → SentenceTransformer + FAISS → LLaMA 2 (GGML) → Chainlit UI


⚙️ Installation

**1. Clone the Repo**

```
git clone https://github.com/your-username/medical-llama-chatbot.git
cd medical-llama-chatbot
```

**2. Setup Environment**

python -m venv venv
venv\Scripts\activate  (or source venv/bin/activate on Mac/Linux)
pip install -r requirements.txt

Requirements include: langchain, chainlit, ctransformers, faiss-cpu, sentence-transformers, langchain-community, etc.

**3. Download Model**

- Visit https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML  
- Download a `.bin` model like: `llama-2-7b-chat.ggmlv3.q4_0.bin`  
- Place it inside a `/models` folder in your project root

**4. Add Your Medical PDF**

Place your medical book or document inside `/data`

**5. Ingest the Data**


python ingest.py

This creates the vector DB at `vectorstores/db_faiss`

**6. Run the Chatbot**


chainlit run model.py

Then open [http://localhost:8000](http://localhost:8000) in your browser.


🧠 Sample Questions

- What are the symptoms of dengue?  
- How is hypertension treated?  
- What medications are used for asthma?


## 🔐 No API Keys Needed

The chatbot works fully offline using only local models and libraries. You own your data and control the entire pipeline.

## 📚 License

MIT License


## 🤝 Contributions

Pull requests, suggestions, and forks are welcome!

---

## 🙋‍♂️ Author

Built by [https://github.com/muhammadzaidfida1-gif)
Let’s connect!
