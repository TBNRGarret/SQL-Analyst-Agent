# 🤖 Multi-Agent Autonomous Data Analyst

An end-to-end, agentic data analysis pipeline that allows users to chat with their datasets (CSV). This project leverages **LangGraph** to orchestrate multiple specialized agents, using **Google Vertex AI (Gemini)** as the reasoning core.



## 🌟 Key Features
- **Natural Language to SQL**: Automatically generates complex SQLite queries from plain English/Vietnamese.
- **Dynamic Schema Awareness**: Adapts to any uploaded CSV file by building a real-time schema context.
- **Automated Visualization**: Uses AI to decide the best chart type (Bar, Line, Scatter) and renders it via Matplotlib.
- **Business Reasoning**: Provides concise, professional summaries of data findings.
- **State-Driven Workflow**: Built with LangGraph to ensure a reliable, traceable, and error-resilient pipeline.

## 🏗️ Architecture
The system consists of 5 specialized nodes:
1.  **Schema Agent**: Analyzes the dataset to provide metadata and samples for the LLM.
2.  **SQL Agent**: Translates user questions into optimized SQLite queries.
3.  **Execution Tool**: Runs SQL queries safely in an in-memory SQLite environment.
4.  **Visualization Agent**: Determines the optimal visual representation and generates plots.
5.  **Insight Agent**: Synthesizes results into human-readable business insights.

## 🛠️ Tech Stack
- **Core Framework**: LangGraph, LangChain
- **LLM**: Google Vertex AI (Gemini 1.5/2.0 Flash)
- **API Backend**: FastAPI, Uvicorn
- **Frontend**: Streamlit
- **Data Handling**: Pandas, SQLite
- **Visualization**: Matplotlib

## 🚀 Getting Started

### 1. Prerequisites
- Python 3.10+
- A Google Cloud Project with Vertex AI API enabled.
- A Service Account JSON key.

### 2. Installation
```bash
git clone [https://github.com/TBNRGarret/multi-agent-data-analyst.git](https://github.com/TBNRGarret/multi-agent-data-analyst.git)
cd multi-agent-data-analyst
pip install -r requirements.txt
