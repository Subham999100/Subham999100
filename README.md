<!-- ═══════════════════════════════ HERO ═══════════════════════════════ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,40:1E1B4B,100:7C3AED&height=250&section=header&text=Subham%20Sekhar%20Patnaik&fontSize=48&fontColor=F5F3FF&fontAlignY=36&desc=I%20build%20AI%20agents%20that%20think%2C%20retrieve%2C%20act%20and%20ship.&descSize=19&descColor=DDD6FE&descAlignY=56&animation=twinkling" width="100%" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2400&pause=800&color=C4B5FD&center=true&vCenter=true&width=720&lines=GenAI+Engineer+%7C+Agentic+AI+%7C+LangGraph;orchestrating+multi-agent+systems+%F0%9F%A4%96;building+production-grade+RAG+pipelines+%F0%9F%93%9A;wiring+LLMs+into+reliable+FastAPI+backends+%E2%9A%A1;learning+every+day.+shipping+real+systems.+%F0%9F%9A%80" />
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2400&pause=800&color=6D28D9&center=true&vCenter=true&width=720&lines=GenAI+Engineer+%7C+Agentic+AI+%7C+LangGraph;orchestrating+multi-agent+systems+%F0%9F%A4%96;building+production-grade+RAG+pipelines+%F0%9F%93%9A;wiring+LLMs+into+reliable+FastAPI+backends+%E2%9A%A1;learning+every+day.+shipping+real+systems.+%F0%9F%9A%80" alt="typing" />
  </picture>
</p>

<p align="center">
  <a href="https://github.com/Subham999100?tab=repositories"><img src="https://img.shields.io/badge/📂_Explore_My_Work-7C3AED?style=for-the-badge" /></a>
  &nbsp;
  <a href="https://github.com/Subham999100?tab=followers"><img src="https://img.shields.io/github/followers/Subham999100?label=Follow&style=for-the-badge&color=1E1B4B&logo=github" /></a>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Subham999100&label=Visitors&color=4C1D95&style=for-the-badge" />
</p>

<br/>

<!-- ═══════════════════════════════ TERMINAL INTRO ═══════════════════════════════ -->
<div align="center">

```bash
┌──(subham㉿genai)-[~/profile]
└─$ whoami

  name      : Subham Sekhar Patnaik
  role      : GenAI Engineer
  focus     : [ AI Agents, Agentic AI, RAG, LangGraph ]
  builds    : LLM-powered backends that actually run in production
  status    : learning every day · shipping real-world systems

┌──(subham㉿genai)-[~/profile]
└─$ █
```

</div>

<table align="center">
<tr>
<td align="center" width="25%"><h2>🤖</h2><b>AI Agents</b><br/><sub>Agentic workflows & orchestration</sub></td>
<td align="center" width="25%"><h2>📚</h2><b>RAG Systems</b><br/><sub>Chunking · embeddings · retrieval</sub></td>
<td align="center" width="25%"><h2>🔧</h2><b>Tool Calling</b><br/><sub>Agents that act, not just talk</sub></td>
<td align="center" width="25%"><h2>🐳</h2><b>Production</b><br/><sub>FastAPI · Docker · AWS</sub></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ ARCHITECTURE ═══════════════════════════════ -->
<h2 align="center">🧬 How I Build Agents</h2>

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

    classDef io fill:#7C3AED,stroke:#DDD6FE,color:#fff,stroke-width:2px
    classDef agent fill:#1E1B4B,stroke:#818CF8,color:#E0E7FF
    classDef check fill:#064E3B,stroke:#34D399,color:#D1FAE5
    class Q,O io
    class P,R,K,T,S agent
    class V check
```

<p align="center"><sub>Planner decomposes → specialists gather & act → verifier loops until confident → synthesizer returns structured output</sub></p>

<br/>

<!-- ═══════════════════════════════ PROJECTS ═══════════════════════════════ -->
<h2 align="center">🚀 Featured Work</h2>

<details>
<summary><b>🧠 Production RAG Knowledge Worker</b> &nbsp;·&nbsp; <code>FastAPI</code> <code>LangChain</code> <code>pgvector</code> <code>Docker</code> &nbsp;— <i>click to expand</i></summary>
<br/>

> Ask questions across organizational documents and get grounded, context-aware answers powered by **Retrieval-Augmented Generation**.

```
📄 ingest  →  ✂️ chunk  →  🧠 embed  →  🔎 retrieve  →  🤖 generate  →  📊 evaluate
```

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

```
🧩 decompose  →  🌐 research  →  🔍 extract  →  ✅ verify  →  📝 synthesize
```

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
<h2 align="center">🛠️ Tech Stack</h2>

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
<h2 align="center">🌱 Currently Exploring</h2>

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

<!-- ═══════════════════════════════ TROPHIES ═══════════════════════════════ -->
<h2 align="center">🏆 Trophy Shelf</h2>

<p align="center">
  <a href="https://github.com/Subham999100">
    <img src="https://github-profile-trophy.vercel.app/?username=Subham999100&theme=discord&no-frame=true&no-bg=true&margin-w=8&column=7" />
  </a>
</p>

<!-- ═══════════════════════════════ STREAK ═══════════════════════════════ -->
<h2 align="center">🔥 Consistency</h2>

<p align="center">
  <a href="https://github.com/Subham999100">
    <img src="https://streak-stats.demolab.com/?user=Subham999100&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=C4B5FD&currStreakLabel=C4B5FD&sideLabels=A5B4FC&dates=8B949E&currStreakNum=E9D5FF&sideNums=E9D5FF" />
  </a>
</p>

<!-- ═══════════════════════════════ SNAKE ═══════════════════════════════ -->
<h2 align="center">🐍 Contribution Snake</h2>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Subham999100/Subham999100/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Subham999100/Subham999100/output/github-contribution-grid-snake.svg" />
    <img alt="contribution snake" src="https://raw.githubusercontent.com/Subham999100/Subham999100/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

<br/>

<!-- ═══════════════════════════════ COLLAB ═══════════════════════════════ -->
<h2 align="center">🤝 Let's Collaborate</h2>

<p align="center">
  <img src="https://img.shields.io/badge/AI_Agents-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Agentic_AI-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LangGraph_/_LangChain-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/RAG_Apps-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LLM_Backends-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open_Source_AI-1E1B4B?style=for-the-badge" />
</p>

<p align="center"><sub>💬 Ask me about GenAI · RAG · AI Agents · LangGraph · LangChain · OpenAI API · FastAPI · Vector DBs · Python</sub></p>

<!-- ═══════════════════════════════ FOOTER ═══════════════════════════════ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,55:1E1B4B,100:0D1117&height=130&section=footer&text=Building%20with%20AI.%20Learning%20every%20day.%20Shipping%20real%20systems.&fontSize=16&fontColor=DDD6FE&fontAlignY=72" width="100%" />
</p>
