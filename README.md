<h1 align="center">
  <strong>Ayush Sonu</strong>
</h1>
<p align="center">
  AI Engineer &nbsp;·&nbsp; Backend Systems &nbsp;·&nbsp; LLD / HLD &nbsp;·&nbsp; Agentic AI &nbsp;·&nbsp; RAG Pipelines
</p>
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=AyushSonuu&color=0e75b6&style=flat" alt="profile views"/>
</p>

---

### 🧠 About Me

I build production-grade AI systems that combine modern LLM capabilities with robust backend engineering. My work sits at the intersection of AI infrastructure, distributed systems, and scalable architecture.

- Designed and shipped **agentic pipelines** (LangGraph) for production AI applications
- Built **async backend services** with FastAPI + PostgreSQL + Redis
- Implemented an **MCP host + intelligent tool routing layer** with a Skills Protocol
- Contributed to open-source **LangGraph agent hosting infrastructure** (Aegra)
- Builds **RAG pipelines with evaluation loops** — LangFuse, LangSmith, Ragas
- Thinks in **system design** — LLD patterns + HLD trade-offs, not just code

> _Reliable AI starts with reliable systems._

---

### ⚙️ Tech Stack

#### 🤖 AI
![LangChain](https://img.shields.io/badge/LangChain-1A1A1A?style=flat&logo=langchain&logoColor=00F5D4)
![LangGraph](https://img.shields.io/badge/LangGraph-1A1A1A?style=flat&logo=langgraph&logoColor=00F5D4)
![LangFuse](https://img.shields.io/badge/LangFuse-1A1A1A?style=flat&logo=langfuse&logoColor=00F5D4)
![LangSmith](https://img.shields.io/badge/LangSmith-1A1A1A?style=flat&logo=langsmith&logoColor=00F5D4)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)

#### 🛠️ Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)

#### 🗄️ Data & Infra
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_+_pgvector-336791?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

#### 🔍 Vector & Search
![Qdrant](https://img.shields.io/badge/Qdrant-1A1A1A?style=flat&logo=qdrant&logoColor=00F5D4)
![FAISS](https://img.shields.io/badge/FAISS-1A1A1A?style=flat&logoColor=white)

---

### 💼 Selected Work

**🔹 MCP Host + Intelligent Tool Execution System**
`MCP` · `Skills Protocol` · `LangGraph` · `FastAPI`
- Integrated an **MCP host** as a first-class feature inside a production AI system
- Built a **runtime tool discovery and routing layer** that dynamically selects and executes the most relevant MCP tools for a task — no hardcoded routing
- Implemented a **Skills Protocol** layer: higher-level skills compose MCP tools to perform multi-step workflows
- Architecture: `Task → Skill → MCP Tool(s) → Result` with runtime tool resolution

---

**🔹 Enterprise RAG Platform**
`FastAPI` · `LangGraph` · `PostgreSQL + pgvector` · `Redis` · `Qdrant`
- Hybrid retrieval (semantic + BM25) with metadata filtering
- Streaming responses over SSE
- Agent workflows with tool-use and planning
- Evaluation pipeline via LangFuse + Ragas

---

**🔹 Agentic Workflow Engine**
`LangGraph` · `Redis pub/sub` · `Celery` · `FastAPI`
- Multi-agent orchestration with stateful memory
- Async background task execution with Redis as Celery broker
- Real-time status streaming to clients

---

**🔹 [Aegra](https://github.com/ibbybuilds/aegra) — Open Source Contribution**
`LangGraph Agent Protocol` · `Agent Hosting Infrastructure`
- Contributed to agent hosting layer for reliability at scale
- Focused on production-grade agent serving patterns

---

### ⚡ Backend Architecture

```
              Client
                 │
                 ▼
         FastAPI  (REST · SSE · Auth · Rate Limiting)
                 │
     ┌───────────┼────────────┐
     ▼           ▼            ▼
PostgreSQL     Redis        Celery Worker
(ACID · jsonb  (cache ·      (background tasks)
 · pgvector)    session ·         │
                pub-sub ·         ▼
                rate limit)   LLM APIs
                                  │
                                  ▼
                             LangFuse / Eval
```

---

### 🤖 Agent System Architecture

```
          User Request
               │
               ▼
         FastAPI API
               │
               ▼
       LangGraph Runtime
               │
     ┌─────────┼──────────┐
     ▼         ▼          ▼
 Retrieval   Tools      Memory
     │         │          │
     └────┬────┘──────────┘
          ▼
       LLM APIs
          │
          ▼
   LangFuse / Eval
```

---

### 🏗️ System Design Depth

```
LLD                                    HLD
──────────────────────────────────     ──────────────────────────────────────
SOLID Principles                       Distributed System Principles
GoF Design Patterns                    Horizontal Scaling + Load Balancing
Clean Architecture                     Caching (Redis — cache-aside, write-through)
Repository / Service Layer             Message Queues (Celery + Redis / SQS)
Dependency Injection                   Database Design (Normalization, Indexing, Partitioning)
Domain-Driven Design                   API Gateway + Rate Limiting
Async / ASGI Internals                 CAP Theorem & eventual consistency
```

---

### 🌱 Currently Exploring

`AI Runtime Architecture` &nbsp;·&nbsp; `ASGI Internals` &nbsp;·&nbsp; `Kafka / Redpanda`  
`Kubernetes` &nbsp;·&nbsp; `Event-driven Architectures` &nbsp;·&nbsp; `Distributed Systems`

---

### 🎯 Interested In

`AI Infrastructure` &nbsp;·&nbsp; `Agent Runtime Design` &nbsp;·&nbsp; `MCP` &nbsp;·&nbsp; `Vector Search` &nbsp;·&nbsp; `Retrieval Systems`

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=AyushSonuu&show_icons=true&theme=tokyonight&hide_border=true" height="160"/>
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AyushSonuu&layout=compact&theme=tokyonight&hide_border=true" height="160"/>
</p>

---

### 🌍 Connect

<p align="center">
  <a href="mailto:sonuayush55@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/ayush-s-5a2285201/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white"/></a>
</p>

---

<h3 align="center">"Reliable AI starts with reliable systems."</h3>
