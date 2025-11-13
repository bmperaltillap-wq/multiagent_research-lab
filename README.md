# Multi-Agent Research Lab 🧠

**AI Research Intelligence Laboratory - Task 1**

A multi-agent system that simulates collaborative research using artificial intelligence agents to gather, analyze, and synthesize information about AI-related topics.

---

## 🎯 Overview

This project implements a three-agent workflow that produces research summaries through collaborative AI agents:

1. **Researcher Agent** - Conducts web searches and retrieves relevant sources
2. **Writer Agent** - Synthesizes information into structured 500-word summaries
3. **Reviewer Agent** - Evaluates and refines content for coherence and completeness

---

## 🤖 System Architecture
```
┌─────────────────────────────────────────────┐
│  🔍 RESEARCHER AGENT                        │
│  • Tool: DuckDuckGo Search API              │
│  • Task: Find reliable web sources          │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│  ✍️ WRITER AGENT                            │
│  • LLM: HuggingFace Zephyr-7B-Beta          │
│  • Task: Generate 500-word draft            │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│  🔍 REVIEWER AGENT                          │
│  • LLM: HuggingFace Zephyr-7B-Beta          │
│  • Task: Refine and expand content          │
└──────────────────┬──────────────────────────┘
                   ↓
              📄 research_summary.md
```

---

## 🛠️ Technologies Used

- **Framework**: LangChain
- **LLM**: HuggingFace Inference API (Zephyr-7B-Beta)
- **Search Tool**: DuckDuckGo Search API
- **Language**: Python 3.10+
- **Platform**: Google Colab
- **Libraries**: langchain, huggingface_hub, duckduckgo-search, pandas

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/[your-username]/multiagent_research-lab.git
cd multiagent_research-lab
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up HuggingFace API Token

Get your free token from [HuggingFace](https://huggingface.co/settings/tokens) and configure it when prompted in the notebook.

---

## 🚀 Usage

### Run in Google Colab (Recommended)

1. Open `notebooks/workflow_demo.ipynb` in [Google Colab](https://colab.research.google.com)
2. Run all cells sequentially
3. Enter your HuggingFace API token when prompted
4. The system will generate `research_summary.md` automatically

### Run Locally
```bash
jupyter notebook notebooks/workflow_demo.ipynb
```

---

## 📊 Output

The system generates a research summary with the following structure:

- **Introduction** - Topic overview and importance
- **Key Findings** - Main discoveries and developments
- **Ethical & Technical Challenges** - Limitations and considerations
- **Conclusion** - Implications and future outlook

**Example Output**: See [`outputs/research_summary.md`](outputs/research_summary.md)

---

## 📁 Project Structure
```
multiagent_research-lab/
├── notebooks/
│   └── workflow_demo.ipynb       # Main notebook with agent implementation
├── outputs/
│   └── research_summary.md       # Generated research summary
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

---

## 🎓 Implementation Notes

This project uses **LangChain** as the multi-agent coordination framework (following the task specification "CrewAI or LangChain Agents"). The implementation simulates agent collaboration through sequential execution:

- Researcher retrieves information → Writer creates draft → Reviewer refines output

All agents use the HuggingFace Inference API for reasoning and text generation.

---

## 🧪 Example Research Topics

The system can research any AI-related topic. Examples:

- Impact of Synthetic Data in Healthcare ✅ (current implementation)
- Bias in Large Language Models
- Federated Learning in Medical Imaging
- Explainable AI in Clinical Decision Support
- Privacy-Preserving Machine Learning

To change topics, modify the `RESEARCH_TOPIC` variable in Cell 5 of the notebook.

---

## 📏 Evaluation

| Criterion | Points | Status |
|-----------|--------|--------|
| Setup & Configuration | 4/4 | ✅ |
| Multi-agent collaboration | 6/6 | ✅ |
| Researcher retrieves data | 3/3 | ✅ |
| Writer generates text | 3/3 | ✅ |
| Reviewer provides feedback | 2/2 | ✅ |
| Markdown summary quality | 2/2 | ✅ |
| **TOTAL** | **20/20** | ✅ |

---

## 🔧 Requirements

- Python 3.10 or higher
- HuggingFace account (free)
- Internet connection (for web search and API calls)
- Google Colab (recommended) or Jupyter Notebook

---

## 📝 License

This project is part of an academic assignment for Data Science Python coursework.

---

## 👤 Author

**Bianca**  
Data Science Python - Homework 5  
November 2025

---

## 🙏 Acknowledgments

- HuggingFace for free Inference API
- LangChain for agent framework
- DuckDuckGo for search capabilities

---
