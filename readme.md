# 🔍 Agentic AI Search Engine

A conversational search engine built with **Streamlit** and **LangChain**, powered by **Groq's LLaMA 3.3 70B** model.  
It combines real-time search tools (DuckDuckGo + Arxiv) with memory-enabled conversations, so the assistant can provide context-aware and up-to-date answers.

---

## ✨ Features
- 🤖 **LLM-powered agent** using Groq’s `llama-3.3-70b-versatile`
- 🔎 **Search integration** with:
  - [DuckDuckGo](https://duckduckgo.com/) for general web results
  - [ArXiv](https://arxiv.org/) for academic research papers
- 🧠 **Memory support** with `ConversationSummaryMemory` for context retention
- 💬 **Chat-like interface** powered by Streamlit’s `st.chat_input` + `st.chat_message`
- ⚡ **Agentic reasoning** (tools + LLM + memory)

---

## 🛠️ Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/agentic-search-engine.git
   cd agentic-search-engine
