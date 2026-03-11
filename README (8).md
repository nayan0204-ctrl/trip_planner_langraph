# 🌍 AI Travel Planner (LangGraph + TinyLlama + Tavily)

This project is an AI-powered travel planner that generates:

- ✅ 3-day itinerary using a local LLM (TinyLlama)
- ✅ Destination information using Tavily web search
- ✅ Current weather summary
- ✅ Workflow orchestration using LangGraph

---

## 🚀 Features

- LangGraph state-machine workflow
- TinyLlama 1.1B Chat model for itinerary generation
- Tavily API for destination info + weather
- Modular architecture

---

## 📁 Project Structure

.
├── llm.py  
├── workflow.py  
├── helper_func.py  
└── notebook.ipynb  

---

## 🧠 Architecture

1. User preferences  
2. Destination info (Tavily)  
3. Itinerary generation (TinyLlama)  
4. Weather lookup (Tavily)  
5. Final output  

---

## 🔄 LangGraph Flow

See flow_diagram.md

---

## ⚙️ Install (Colab)

pip install transformers torch langgraph tavily-python python-dotenv

---

## 🔑 Tavily API Key

```python
import os
os.environ["TAVILY_API_KEY"] = "YOUR_KEY"
```

---

## ▶️ Run

```python
from workflow import app
from helper_func import clean_itinerary

preferences = {
    "destination": "Delhi",
    "budget": 1000,
    "interests": ["art","food"],
    "dates": "2026-04-01 to 2026-04-03"
}

result = app.invoke({"preferences": preferences})

print(clean_itinerary(result["itinerary"]))
print(result["weather"])
```

---

## ✅ Why LangGraph?

- Deterministic workflows
- Tool chaining
- Easy extension (RAG, agents)

---

Built for learning LangGraph + LLM pipelines.
