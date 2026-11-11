<!-- ═══════════════════════════════ BANNER ═══════════════════════════════ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,45:1E1B4B,100:6D28D9&height=240&section=header&text=Subham%20Sekhar%20Patnaik&fontSize=46&fontColor=F5F3FF&fontAlignY=38&desc=GenAI%20Engineer%20%E2%80%A2%20AI%20Agents%20%E2%80%A2%20LangGraph%20%E2%80%A2%20RAG&descSize=18&descColor=C4B5FD&descAlignY=58&animation=fadeIn" width="100%" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2600&pause=900&color=C4B5FD&center=true&vCenter=true&width=700&lines=%3E+orchestrating+multi-agent+systems+with+LangGraph;%3E+building+production-grade+RAG+pipelines;%3E+wiring+LLMs+into+reliable+FastAPI+backends;%3E+learning+every+day.+shipping+real+systems." />
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2600&pause=900&color=6D28D9&center=true&vCenter=true&width=700&lines=%3E+orchestrating+multi-agent+systems+with+LangGraph;%3E+building+production-grade+RAG+pipelines;%3E+wiring+LLMs+into+reliable+FastAPI+backends;%3E+learning+every+day.+shipping+real+systems." alt="typing" />
  </picture>
</p>

<p align="center">
  <a href="https://github.com/Subham999100?tab=repositories"><img src="https://img.shields.io/badge/📂_Explore_Repos-6D28D9?style=for-the-badge" /></a>
  &nbsp;
  <a href="https://github.com/Subham999100?tab=followers"><img src="https://img.shields.io/github/followers/Subham999100?label=Follow&style=for-the-badge&color=1E1B4B&logo=github" /></a>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Subham999100&label=Visitors&color=4C1D95&style=for-the-badge" />
</p>

<br/>

<!-- ═══════════════════════════════ INTRO ═══════════════════════════════ -->
<h3 align="center">⚡ I build LLM-powered systems — from retrieval pipelines to autonomous multi-agent workflows.</h3>

<p align="center">
  Computer Science graduate turning GenAI concepts into <b>reliable backend services</b>.<br/>
  Focused on <b>Agentic AI</b>, <b>LangGraph</b>, <b>RAG</b>, <b>tool calling</b>, and <b>production deployment</b>.
</p>

<br/>

<table align="center">
<tr>
<td align="center" width="25%"><h2>🤖</h2><b>AI Agents</b><br/><sub>Agentic workflows & orchestration</sub></td>
<td align="center" width="25%"><h2>📚</h2><b>RAG Systems</b><br/><sub>Chunking · embeddings · retrieval</sub></td>
<td align="center" width="25%"><h2>🔧</h2><b>Tool Calling</b><br/><sub>Agents that act, not just talk</sub></td>
<td align="center" width="25%"><h2>🐳</h2><b>Production</b><br/><sub>FastAPI · Docker · AWS</sub></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ HOW I BUILD ═══════════════════════════════ -->
## 🧬 How I Build Agents

<details open>
<summary><b>🔽 Click to collapse the architecture</b></summary>
<br/>

```mermaid
flowchart LR
    Q([🧑 User Query]) --> P{{🧩 Planner Agent}}
    P --> R[🌐 Research Agent]
    P --> K[📚 RAG Retriever]
    P --> T[🔧 Tool Executor]
    R --> V{{✅ Verifier}}
    K --> V
    T --> V
    V -->|needs more| P
    V -->|verified| S[📝 Synthesizer]
    S --> O([📦 Structured Output])

    classDef io fill:#6D28D9,stroke:#C4B5FD,color:#fff
    classDef agent fill:#1E1B4B,stroke:#818CF8,color:#E0E7FF
    classDef check fill:#064E3B,stroke:#34D399,color:#D1FAE5
    class Q,O io
    class P,R,K,T,S agent
    class V check
```

<p align="center"><sub>Planner decomposes the task → specialist agents gather & act → verifier loops until confident → synthesizer returns structured output</sub></p>

</details>

<br/>

<!-- ═══════════════════════════════ PROJECTS ═══════════════════════════════ -->
## 🚀 Featured Work

<details>
<summary><b>🧠 Production RAG Knowledge Worker</b> &nbsp;·&nbsp; <code>FastAPI</code> <code>LangChain</code> <code>pgvector</code> <code>Docker</code> &nbsp;— <i>click to expand</i></summary>
<br/>

> Ask questions across organizational documents and get grounded, context-aware answers powered by **Retrieval-Augmented Generation**.

**Pipeline**

```
📄 ingest  →  ✂️ chunk  →  🧠 embed  →  🔎 retrieve  →  🤖 generate  →  📊 evaluate
```

**What's inside**

| Layer | Implementation |
|:--|:--|
| 📄 Ingestion | Document loading & preprocessing |
| ✂️ Chunking | Intelligent, context-preserving splits |
| 🧠 Embeddings | OpenAI embeddings stored in PostgreSQL + pgvector |
| 🔎 Retrieval | Semantic vector search for relevant context |
| 🤖 Generation | LLM answers grounded in retrieved context |
| 📊 Quality | Evaluation layer & robust error handling |
| 🐳 Deployment | Fully Dockerized, production-ready |

<sub><b>Python · FastAPI · LangChain · OpenAI · PostgreSQL · pgvector · Docker</b></sub>

</details>

<details>
<summary><b>🤖 Deep Research Multi-Agent System</b> &nbsp;·&nbsp; <code>LangGraph</code> <code>OpenAI API</code> <code>FastAPI</code> <code>Docker</code> &nbsp;— <i>click to expand</i></summary>
<br/>

> Breaks complex questions into research tasks and coordinates **specialized agents** to produce verified, structured reports.

**Pipeline**

```
🧩 decompose  →  🌐 research  →  🔍 extract  →  ✅ verify  →  📝 synthesize
```

**What's inside**

| Layer | Implementation |
|:--|:--|
| 🧩 Planning | Query decomposition into research tasks |
| 🤖 Orchestration | Multi-agent coordination with LangGraph |
| 🌐 Research | Web research & information extraction |
| ✅ Verification | Source checking before synthesis |
| 🔧 Tools | Tool calling with structured outputs |
| 📝 Output | Automated report generation |

<sub><b>Python · LangGraph · OpenAI API · FastAPI · Docker</b></sub>

</details>

<br/>

<!-- ═══════════════════════════════ STACK ═══════════════════════════════ -->
## 🛠️ Tech Stack

<table align="center">
<tr>
<td align="center" width="140"><b>🤖 GenAI</b></td>
<td>
<img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square" />
<img src="https://img.shields.io/badge/RAG-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Agentic_AI-7C3AED?style=flat-square" />
</td>
</tr>
<tr>
<td align="center"><b>⚙️ Backend</b></td>
<td><img src="https://skillicons.dev/icons?i=python,fastapi,java,spring,ts&theme=dark" height="40" /></td>
</tr>
<tr>
<td align="center"><b>🗄️ Data</b></td>
<td>
<img src="https://skillicons.dev/icons?i=postgres,mongodb&theme=dark" height="40" />
&nbsp;
<img src="https://img.shields.io/badge/pgvector-316192?style=flat-square" />
<img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square" />
</td>
</tr>
<tr>
<td align="center"><b>☁️ DevOps</b></td>
<td><img src="https://skillicons.dev/icons?i=aws,docker,git,github,linux&theme=dark" height="40" /></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ LEARNING ═══════════════════════════════ -->
## 🌱 Currently Exploring

<details>
<summary><b>📖 See what I'm learning right now</b></summary>
<br/>

```yaml
agents:
  - Advanced Agentic AI architectures
  - Advanced LangGraph (state, checkpoints, human-in-the-loop)
  - Multi-agent systems & tool design

retrieval:
  - RAG architecture & optimization
  - LLM evaluation
  - Observability & tracing

production:
  - Production-grade GenAI systems
  - AI + Cloud deployment (AWS)
```

</details>

<br/>

<!-- ═══════════════════════════════ COLLAB ═══════════════════════════════ -->
## 🤝 Let's Collaborate

<p align="center">
  <img src="https://img.shields.io/badge/AI_Agents-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Agentic_AI-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LangGraph_/_LangChain-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/RAG_Apps-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LLM_Backends-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open_Source_AI-1E1B4B?style=for-the-badge" />
</p>

<p align="center"><sub>💬 Ask me about GenAI · RAG · AI Agents · LangGraph · LangChain · OpenAI API · FastAPI · Vector DBs · Python</sub></p>

<br/>

<!-- ═══════════════════════════════ STREAK ═══════════════════════════════ -->
## 🔥 Consistency

<p align="center">
  <a href="https://github.com/Subham999100">
    <img src="https://streak-stats.demolab.com/?user=Subham999100&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=C4B5FD&currStreakLabel=C4B5FD&sideLabels=A5B4FC&dates=8B949E&currStreakNum=E9D5FF&sideNums=E9D5FF" />
  </a>
</p>

<br/>

<!-- ═══════════════════════════════ FOOTER ═══════════════════════════════ -->
<p align="center">
  <b>🚀 Building with AI. Learning every day. Shipping real-world systems.</b>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6D28D9,55:1E1B4B,100:0D1117&height=110&section=footer" width="100%" />
</p>
