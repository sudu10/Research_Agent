# 🧠 Research Agent (LangChain + OpenAI)

An AI-powered research assistant that autonomously gathers information
from the web and Wikipedia, structures the results using Pydantic, and
optionally saves the output to a text file.

This project demonstrates how to build a tool-calling agent using
LangChain and OpenAI.

------------------------------------------------------------------------

## 🚀 Features

-   🔎 Web Search using DuckDuckGo
-   📚 Wikipedia Integration
-   🤖 GPT-powered reasoning (gpt-4o-mini)
-   🗂 Structured output using Pydantic
-   💾 Save research results to a `.txt` file
-   🧠 Tool-calling Agent architecture

------------------------------------------------------------------------

## 📂 Project Structure

. ├── main.py ├── tools.py ├── requirements.txt └── research_output.txt
(auto-generated)

------------------------------------------------------------------------

## 🧩 Tech Stack

-   Python
-   LangChain
-   OpenAI (gpt-4o-mini)
-   DuckDuckGo Search
-   Wikipedia API
-   Pydantic
-   python-dotenv

------------------------------------------------------------------------

## ⚙️ Installation

### 1️⃣ Clone the Repository

``` bash
git clone <your-repo-url>
cd research-agent
```

### 2️⃣ Create Virtual Environment (Recommended)

``` bash
python -m venv venv
source venv/bin/activate      # Mac/Linux
venv\Scripts\activate         # Windows
```

### 3️⃣ Install Dependencies

``` bash
pip install -r requirements.txt
```

### 4️⃣ Setup Environment Variables

Create a `.env` file in the root directory:

OPENAI_API_KEY=your_openai_api_key_here

------------------------------------------------------------------------

## ▶️ Usage

Run the application:

``` bash
python main.py
```

You will be prompted:

What can I help you research?

Enter any topic, for example:

Impact of Artificial Intelligence in Healthcare

------------------------------------------------------------------------

## 🧠 Output Structure

``` python
class ResearchAgent(BaseModel):
    topic: str
    summary: str
    sources: list[str]
    tools_used: list[str]
```

------------------------------------------------------------------------

## 🔄 Agent Workflow

User Query\
↓\
LangChain Agent\
↓\
Tool Selection (Search / Wikipedia)\
↓\
LLM Reasoning (GPT-4o-mini)\
↓\
Structured Parsing (Pydantic)\
↓\
Optional Save to File

------------------------------------------------------------------------

## 📦 Dependencies

-   langchain
-   langchain-community
-   langchain_openai
-   langchain-anthropic
-   wikipedia
-   python-dotenv
-   pydantic
-   duckduckgo-search

Install via:

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

## 🛠 Future Improvements

-   Add conversational memory
-   Export research to Markdown or PDF
-   Add citation formatting (APA/MLA)
-   Integrate vector database (RAG enhancement)
-   Build a Streamlit or FastAPI UI

------------------------------------------------------------------------

## 📜 License

MIT License

------------------------------------------------------------------------

## 👨‍💻 Author

Autonomous AI Research Agent built using LangChain tool-calling
architecture and OpenAI models.
