# 🔍 Agentic AI Search Engine 


**Live Demo:** [Streamlit](https://ai-search-engine-project.streamlit.app)

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
````

2. Create a virtual environment and install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   **requirements.txt** should include:

   ```txt
   streamlit
   python-dotenv
   langchain
   langchain-community
   langchain-groq
   ```

3. Set up environment variables:
   Create a `.env` file in the project root with:

   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

---

## 🚀 Usage

Run the app locally with:

```bash
streamlit run app.py
```

Then open the provided local URL (default: `http://localhost:8501`).

---

## 📂 Project Structure

```
.
├── app.py          # Main Streamlit application
├── .env            # Environment variables (ignored in git)
├── requirements.txt
└── README.md
```

---

## 💡 How It Works

1. **LLM Initialization**
   The Groq API loads the `llama-3.3-70b-versatile` model.
2. **Tools Setup**

   * `ArxivQueryRun` (academic papers)
   * `DuckDuckGoSearchRun` (web search)
3. **Agent Orchestration**
   The agent uses `CONVERSATIONAL_REACT_DESCRIPTION` to decide when to search, fetch research, or respond directly.
4. **Memory**
   `ConversationSummaryMemory` ensures past interactions influence new answers without storing the full raw history.
5. **UI**
   Chat-like interface with sidebar configuration for API key.

---

## 📸 Example

1. Ask:

   ```
   What are the latest trends in deep learning?
   ```
2. The agent:

   * Searches Arxiv for recent papers
   * Uses DuckDuckGo for news
   * Summarizes results with context
   * Remembers your previous questions for follow-up

---

## 📝 License

MIT License. See `LICENSE` for details.





Would you like me to also generate the **requirements.txt** alongside this README so you can copy-paste and run directly?
```
