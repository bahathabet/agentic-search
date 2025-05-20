# 🤖 Agentic Web Search with Google API

Agentic Web Search with Google API is an intelligent assistant that uses Agentic AI and the Google Custom Search API to perform live, deep web searches in response to user queries. It integrates multiple LLMs (GPT, Claude, DeepSeek, LLaMA(localhost)) with a deep search tool that extracts and summarizes content from the latest sources on the web.

## 📌 Features

- 🔍 Uses Google Custom Search API for up-to-date web results
- 🧠 Integrates LLMs including GPT, Claude, DeepSeek, and LLaMA(locally in your machine, at no cost and no need for APIs)
- 🌐 Fetches and parses multiple URLs to extract relevant content
- 🛠️ Exposes a `deep_search_tool()` for structured information gathering
- 📥 Automatically appends source URLs in responses
- ⚡ Async execution for fast multi-agent querying
- ✅ Designed to be accurate, current, and grounded in recent web data


This project is designed to provide **free**, real-time, deep-search capability — ideal for research, trend tracking, and live information discovery.
— It is not designed to get local time or weather, you need to add a new @function_tool to do so with APIs keys from a provider. 

## 📂 Project Structure

```
web-search-agent/
├── Agentic_Web_Search.ipynb         # Main interactive notebook
├── requirements.txt                 # Python dependencies
├── README.md                        # This file
├── LICENSE                          # Open-source license
└── .gitignore                       # Ignore .env and cache files
```

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/bahathabet/agentic-search.git
cd agentic-search
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up API Keys

Create a `.env` file with the following variables in the project root directory:

```env
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_key
DEEPSEEK_API_KEY=your_deepseek_key
ANTHROPIC_API_KEY=your_anthropic_key
GSEARCH_API_KEY=your_google_custom_search_key
SEARCH_ENGINE_ID=your_custom_search_engine_id
```
If you would like to use Llama locally then you need only the following API keys:
GSEARCH_API_KEY=your_google_custom_search_key
SEARCH_ENGINE_ID=your_custom_search_engine_id

### 4. (Optional) Create and activate a virtual environment:

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```
### 5. 📦 Requirements

Install dependencies:
```bash
pip install -r requirements.txt
```

## 🔑 How to Get Google Custom Search API Key and Search Engine ID

To enable the Google Custom Search API for this project, follow these steps:

### 1. Create a Google Cloud Project

- Visit the [Google Cloud Console](https://console.cloud.google.com/)
- Sign in with your Google account
- Click **Select a project** > **New Project**
- Enter a project name and click **Create**

### 2. Enable the Custom Search API

- In the Cloud Console, go to **APIs & Services > Library**
- Search for **Custom Search API**
- Click on it and then click **Enable**

### 3. Create API Credentials (API Key)

- Go to **APIs & Services > Credentials**
- Click **Create Credentials** > **API Key**
- Copy the generated API key — this is your `GSEARCH_API_KEY`

### 4. Set Up a Custom Search Engine (CSE)

- Go to the [Google Custom Search Engine page](https://cse.google.com/cse/all)
- Click **Add**
- Under **Sites to search**, enter `www.google.com` or leave it blank to search the entire web (you may need to allow searching the entire web in the control panel)
- Name your search engine and click **Create**

### 5. Find your Search Engine ID

- After creation, go to **Control Panel** for your search engine
- Copy the **Search engine ID** (a string like `012345678901234567890:abcde_fghij`)
- This is your `SEARCH_ENGINE_ID`

### 6. Add keys to your `.env` file

```env
GSEARCH_API_KEY=your_google_api_key_here
SEARCH_ENGINE_ID=your_search_engine_id_here
```

### 🧠 How to Install and Run Ollama Locally

This project supports integration with a locally running [Ollama](https://ollama.com/) server to use models like LLaMA.

### 1. Install Ollama

Follow instructions for your OS from the [Ollama install page](https://ollama.com/download).

For macOS (Homebrew):

```bash
brew install ollama
```

For Windows and Linux, download from the [official site](https://ollama.com/download) and follow platform-specific instructions.

### 2. Start the Ollama Server

Run this command in your terminal to start the local Ollama server:

```bash
ollama serve
```

You can verify it’s working by visiting [http://localhost:11434](http://localhost:11434) in your browser.

### 3. Pull the LLaMA Model

To use LLaMA 3.2, run:

```bash
ollama pull llama3.2
```

Make sure this matches the model name used in the notebook (e.g., `llama3.2:latest`).

### 4. No Additional Setup Required

Once Ollama is running, the agent in your notebook will automatically connect to `http://localhost:11434/v1` using the API key `ollama`.

## 📜 License

This project is licensed under the **MIT License** — feel free to use, modify, and share.

## 🤝 Contributing

Pull requests, ideas, and suggestions are welcome! If you find a bug or have an idea for improvement, feel free to open an issue.
