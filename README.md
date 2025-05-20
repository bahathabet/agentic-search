# Agentic Web Search with Google API

> 🧠 A powerful agent-based AI system that performs real-time, deep web searches using Google Custom Search API and large language models (LLMs) to provide fresh, contextual answers — for free.

## 🚀 Overview

**Agentic Web Search with Google API** is an intelligent assistant that:
- Uses OpenAI Agents SDK
- Uses **Agentic AI architecture** to reason and respond.
- Integrates **Google Custom Search API** to retrieve the most recent online content.
- Leverages multiple agents **LLMs** like GPT, Claude, DeepSeek, and LLaMA (localhost) to analyze and summarize search results.
- Returns professional, source-based answers to user questions.

This project is designed to provide **free**, real-time, deep-search capability — ideal for research, trend tracking, and live information discovery.

## 🧠 Features

- 🔍 Real-time web search powered by Google CSE
- 🕸️ Clean and structured webpage content extraction via `BeautifulSoup`
- 🤖 Agentic AI architecture with support for multiple LLMs
- ⚡ Async execution for fast multi-agent querying
- 📎 Includes full source URLs in responses for transparency

## 📂 Project Structure

```
web-search-agent/
├── agent_search_demo.ipynb          # Main interactive notebook
├── .env                             # Template for environment variables
├── requirements.txt                 # Python dependencies
├── README.md                        # This file
├── LICENSE                          # Open-source license
└── .gitignore                       # Ignore .env and cache files
```

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/agentic-web-search.git
cd agentic-web-search
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up API Keys

Copy the environment example and populate it with your credentials:

```bash
cp .env.example .env
```

**Required keys:**
- `OPENAI_API_KEY`
- `GOOGLE_API_KEY`
- `GSEARCH_API_KEY`
- `SEARCH_ENGINE_ID`
- `ANTHROPIC_API_KEY`
- `DEEPSEEK_API_KEY`

> 🔐 *Never commit your actual `.env` file to version control.*

## ▶️ Running the Notebook

Launch Jupyter:

```bash
jupyter notebook notebook/agent_search_demo.ipynb
```

Choose a prompt like:
> "What are the Agentic AI trends in 2025?"

## 📦 Requirements

Install via:
```bash
pip install -r requirements.txt
```

## 📜 License

This project is licensed under the **MIT License** — feel free to use, modify, and share.

## 🤝 Contributing

Pull requests, ideas, and suggestions are welcome! If you find a bug or have an idea for improvement, feel free to open an issue.
