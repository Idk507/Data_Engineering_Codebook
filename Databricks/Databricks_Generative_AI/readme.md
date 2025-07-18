Here’s a **comprehensive guide to Generative AI on Databricks**, covering all Mosaic AI features, tools, and workflows—directly sourced from Databricks docs:

---

## 🚀 Core Generative AI Capabilities

### 1. **Foundation Models & Mosaic AI Gateway**

* **Foundation Models APIs**: Access and serve open-source LLMs (DBRX, MPT, Mosaic BERT) and third-party models (OpenAI, Anthropic, Meta, etc.) through a unified API([Databricks Documentation][1]).
* **Mosaic AI Gateway**: Central proxy for model invocation—handles security, logging, model switching, and light guardrails (blocking sensitive data leaking)([Addepto][2]).

---

### 2. **DBRX & Open-Source LLMs**

* **DBRX**: Databricks’ flagship open-source mixture-of-experts LLM (36 B active parameters out of 132 B) released March 27 2024—high-quality, fast, and competitively benchmarked([Databricks][3]).
* **MPT, Mosaic BERT, and Diffusion models**: Alternatives for text and image generation; all supported through Mosaic AI([Databricks][3]).

---

### 3. **Vector Search**

* Built-in **Mosaic AI Vector Search** lets you:

  1. Create and sync vector indexes from Delta tables using LLM-generated embeddings.
  2. Use HNSW approximate nearest neighbor search with optional hybrid keyword-similarity queries, all governed via Unity Catalog([Databricks Documentation][4]).

---

### 4. **AI Playground & No-Code Tools**

* **AI Playground**: No-code environment for prototyping prompts, querying models, fine-tuning inference parameters([Databricks Documentation][1]).
* **Agent Bricks**: Drag-and-drop canvas to build domain-specific agent workflows without coding([Databricks Documentation][5]).

---

### 5. **Mosaic AI Agent Framework & Agents**

* Build **Retrieval-Augmented Generation (RAG)**, tool-calling, or multi-agent systems:

  * Define agents that reason over data, call APIs, and execute tool chains([Databricks Documentation][6]).
  * Supports both simple “monolithic” LLM prompting and complex agent orchestration([Databricks Documentation][6]).

---

### 6. **Agent Evaluation & Quality Monitoring**

* **Mosaic AI Agent Evaluation**:

  * Automated quality assessment with AI judges.
  * Tracks metrics like latency, cost, accuracy, and supports root-cause analysis([Databricks][7], [Medium][8]).

---

### 7. **Model Serving & LLMOps**

* **Mosaic AI Model Serving**:

  * Deploy fine-tuned or third-party models (LLMs, image models) as REST endpoints with auto-scaling/GPU support([Medium][8]).
* **External Model Integration**:

  * Govern and serve external models through AI Gateway, with unified logging, monitoring, and access control([Databricks Documentation][5]).

---

### 8. **PromptOps & RAG Workflow Support**

* Supports end-to-end **RAG pipelines**:

  * Embed documents via Vector Search,
  * Retrieve relevant context dynamically,
  * Inject into prompts for more accurate generation([Databricks Documentation][6], [Databricks Documentation][4]).

---

### 9. **Governance, Monitoring & Compliance**

* **Unity Catalog**: Central governance across data, models, feature stores, and vector indexes([Medium][8]).
* **Lakehouse Monitoring & Model Drift**: Monitor data quality and model performance in production([Databricks Documentation][5]).
* **Audit & Security**: Full log tracking via AI Gateway, Delta Tables, and endpoint ACLs([Addepto][2]).

---

### 10. **Developer to Production Workflow**

The recommended **Generative AI developer workflow** includes stages:

1. PoC & design (models, retrieval sources, agent logic)
2. Build (data prep, RAG pipeline, agent prototype)
3. Evaluate & iterate (feedback, tune, re-evaluate)
4. Deploy & monitor in production([Databricks Documentation][9], [Databricks Documentation][6], [Databricks Documentation][5]).

---

[Databricks Generative AI Fundamentals](https://www.youtube.com/watch?v=_kAP4Wtvauw&utm_source=chatgpt.com)

---

## 🧩 Summary Table

| Capability                       | Description                                      |
| -------------------------------- | ------------------------------------------------ |
| **Foundation Models & DBRX**     | Serve first-class open-source & third-party LLMs |
| **Mosaic AI Gateway**            | Unified secure model routing & governance        |
| **Vector Search**                | Integrated embedding search with ACL support     |
| **AI Playground & Agent Bricks** | No-code prototyping environments                 |
| **Agent Framework**              | Build RAG/tool-augmented/multi-agent systems     |
| **Agent Evaluation**             | AI-driven quality and performance monitoring     |
| **Model Serving / LLMOps**       | Deploy models with auto-scaling & monitoring     |
| **RAG & PromptOps**              | Full retrieval + generation pipelines            |
| **Governance & Monitoring**      | Unity Catalog, audits, drift detection           |
| **Dev→Prod Workflow**            | Guided path from prototype to production         |

---

## 📚 Getting Started

* Try **AI Playground** to experiment with DBRX and foundation models.
* Build a simple **RAG pipeline + agent** using notebooks and Vector Search.
* Use **Agent Bricks** for no-code prototype, then evaluate quality.
* Deploy your model via **Model Serving**, governed by **AI Gateway**.
* Monitor usage, performance, and drift with built-in tools.

Let me know if you’d like sample code snippets, deep dive into any feature, or a learning path to master Generative AI on Databricks!

[1]: https://docs.databricks.com/aws/en/generative-ai/agent-framework/build-genai-apps?utm_source=chatgpt.com "Build gen AI apps on Databricks"
[2]: https://addepto.com/blog/a-comprehensive-overview-of-the-databricks-ai-capabilities/?utm_source=chatgpt.com "A Comprehensive Overview of the Databricks AI Capabilities"
[3]: https://www.databricks.com/research/mosaic?utm_source=chatgpt.com "Databricks Mosaic: Pioneering AI & Open-Source Research"
[4]: https://docs.databricks.com/aws/en/generative-ai/vector-search?utm_source=chatgpt.com "Mosaic AI Vector Search - Databricks Documentation"
[5]: https://docs.databricks.com/aws/en/machine-learning/?utm_source=chatgpt.com "AI and machine learning on Databricks"
[6]: https://docs.databricks.com/aws/en/generative-ai/guide/introduction-generative-ai-apps?utm_source=chatgpt.com "Introduction to generative AI apps on Databricks"
[7]: https://www.databricks.com/product/artificial-intelligence?utm_source=chatgpt.com "Build and deploy quality AI agent systems - Databricks"
[8]: https://billtcheng2013.medium.com/generative-ai-on-databricks-mosaic-ai-c540d0f5d9ee?utm_source=chatgpt.com "Generative AI on Databricks Mosaic AI | by Xin Cheng - Medium"
[9]: https://docs.databricks.com/aws/en/generative-ai/tutorials/ai-cookbook/genai-developer-workflow?utm_source=chatgpt.com "Generative AI app developer workflow - Databricks Documentation"
