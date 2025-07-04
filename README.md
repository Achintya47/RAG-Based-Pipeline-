<p align="center">
   <img src="https://registry.npmmirror.com/@lobehub/icons-static-png/1.51.0/files/dark/langchain-color.png" alt="LangChain Logo" height="50" style="margin-top:10px;">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HuggingFace Logo" height="80">
</p>

<h1 align="center">🎓 NIT Jalandhar RAG-based Chatbot</h1>

<p align="center">A Retrieval-Augmented Generation (RAG) pipeline using LangChain, HuggingFace, and FAISS to build an intelligent assistant for NIT Jalandhar.</p>

---

### 🚧 Project Status: In Progress

This repository contains an experimental yet functional implementation of a **college-specific chatbot** built for NIT Jalandhar. The system can answer queries based on the **official prospectus** using a lightweight transformer model. While the core pipeline works, improvements and enhancements are planned for future updates.

---

## ✅ Current Progress

- 🔍 **Document Ingestion**:
  - Loaded the NIT Jalandhar prospectus using `PyPDFLoader`
  - Split documents into manageable chunks using LangChain

- 🧠 **Embedding & Indexing**:
  - Used HuggingFace’s `bge-base-en-v1.5` for sentence embeddings
  - Created and stored the embeddings using `FAISS` for vector similarity search

- 🤖 **LLM Integration**:
  - Integrated **TinyLLaMA 1.1B-chat** model from HuggingFace Hub
  - Built a **custom prompt template** and connected everything using LangChain's graph-based composition

- 💬 **Chat Interface**:
  - Successfully answers user queries from the NIT Jalandhar prospectus

---

## 🔮 Future Work & Improvements

1. ### 🎯 **Precise Retrieval**
   - Reduce noise in output by:
     - Lowering `k` (number of top documents retrieved)
     - Increasing similarity threshold to filter less-relevant documents

2. ### 🛡️ **Guardrails**
   - The model may **hallucinate** due to its small size
   - Implement guardrails using the `Guardrails AI` library to:
     - Enforce structured responses
     - Avoid unsafe/untrue outputs

3. ### 🔧 **Fine-tuning (Optional)**
   - Investigate finetuning with **PEFT** and **QLoRA**
   - Although current hardware limits training, exploring adapter tuning for task-specific improvements is a priority

---

## 🛠️ Technologies Used

- [LangChain](https://github.com/langchain-ai/langchain)
- [HuggingFace Transformers](https://huggingface.co)
- [TinyLLaMA 1.1B-chat](https://huggingface.co/cnlp/TinyLlama-1.1B-Chat-v1.0)
- [FAISS](https://github.com/facebookresearch/faiss)
- [PyPDFLoader](https://python.langchain.com/docs/modules/data_connection/document_loaders/pdf)
- [PEFT & QLoRA](https://huggingface.co/blog/peft)
- [Guardrails AI](https://github.com/ShreyaR/guardrails)

---

## 📌 About

This project is part of an initiative to make campus documents and policies more accessible and queryable by students using modern LLM pipelines.

---

## 👤 Author

**Achintya Sharma**  
🔗 [LinkedIn](https://www.linkedin.com/in/achintyasharma47)

---

## 📌 Disclaimer

This is a personal project for educational and exploratory purposes. Not affiliated officially with NIT Jalandhar.
