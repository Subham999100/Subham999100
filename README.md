<!-- ═══════════════════════════════ HERO ═══════════════════════════════ -->
<p align="center">
  <img src="./hero.svg" width="100%" alt="Subham Sekhar Patnaik — GenAI Engineer building agentic systems" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2600&pause=900&color=C4B5FD&center=true&vCenter=true&width=760&lines=I+don't+build+chatbots.+I+build+systems+that+think.;planner+%E2%86%92+specialists+%E2%86%92+verifier+%E2%86%92+ship;RAG+that+grounds+every+answer+in+real+context;agents+that+act%2C+not+just+talk;from+notebook+to+production.+every+time." />
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2600&pause=900&color=6D28D9&center=true&vCenter=true&width=760&lines=I+don't+build+chatbots.+I+build+systems+that+think.;planner+%E2%86%92+specialists+%E2%86%92+verifier+%E2%86%92+ship;RAG+that+grounds+every+answer+in+real+context;agents+that+act%2C+not+just+talk;from+notebook+to+production.+every+time." alt="typing" />
  </picture>
</p>

<p align="center">
  <a href="https://github.com/Subham999100?tab=repositories"><img src="https://img.shields.io/badge/Explore_My_Work-7C3AED?style=for-the-badge&logo=github&logoColor=white" /></a>
  &nbsp;
  <a href="https://github.com/Subham999100?tab=followers"><img src="https://img.shields.io/github/followers/Subham999100?label=Follow&style=for-the-badge&color=1E1B4B&logo=github" /></a>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Subham999100&label=Profile+Views&color=4C1D95&style=for-the-badge" />
</p>

<br/>

<!-- ═══════════════════════════════ SOURCE CODE OF ME ═══════════════════════════════ -->
<h2 align="center">⚙️ My Source Code</h2>
<p align="center"><sub>if I were a LangGraph, this is how I'd compile</sub></p>

```python
from langgraph.graph import StateGraph, START, END
from subham import think, retrieve, act, verify, ship, Engineer

me = StateGraph(Engineer)

me.add_node("think",    think)     # break the problem into solvable pieces
me.add_node("retrieve", retrieve)  # ground every answer in real context
me.add_node("act",      act)       # tools, APIs, code — agents that do things
me.add_node("verify",   verify)    # trust, but check
me.add_node("ship",     ship)      # FastAPI · Docker · AWS

me.add_edge(START, "think")
me.add_edge("think", "retrieve")
me.add_edge("retrieve", "act")
me.add_edge("act", "verify")
me.add_conditional_edges("verify", lambda s: "ship" if s.confident else "think")
me.add_edge("ship", END)

subham = me.compile(checkpointer=curiosity)   # state persists. learning never resets.
subham.invoke({"problem": "yours"})           # → production-grade AI
```

<table align="center" width="100%">
<tr>
<td align="center" width="25%">🤖<br/><b>AI Agents</b><br/><sub>Planners, specialists & verifiers that cooperate</sub></td>
<td align="center" width="25%">📚<br/><b>RAG Systems</b><br/><sub>Chunk · embed · retrieve · ground · evaluate</sub></td>
<td align="center" width="25%">🔧<br/><b>Tool Calling</b><br/><sub>Structured outputs that drive real actions</sub></td>
<td align="center" width="25%">🐳<br/><b>Production</b><br/><sub>FastAPI · Docker · AWS — not just notebooks</sub></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ ARCHITECTURE ═══════════════════════════════ -->
<h2 align="center">🧬 Anatomy of an Agent I Build</h2>

```mermaid
flowchart LR
    Q([🧑 User Query]) --> P{{🧩 Planner}}

    subgraph SPECIALISTS [" ⚡ specialists run in parallel "]
        direction TB
        R[🌐 Research Agent]
        K[📚 RAG Retriever]
        T[🔧 Tool Executor]
    end

    P --> R & K & T
    R & K & T --> V{{✅ Verifier}}
    V -.->|"↺ not confident — re-plan"| P
    V ==>|verified| S[📝 Synthesizer]
    S --> O([📦 Structured Output])

    classDef io fill:#7C3AED,stroke:#DDD6FE,color:#fff,stroke-width:2px
    classDef agent fill:#1E1B4B,stroke:#818CF8,color:#E0E7FF
    classDef check fill:#064E3B,stroke:#34D399,color:#D1FAE5
    class Q,O io
    class P,R,K,T,S agent
    class V check
    style SPECIALISTS fill:#0D1117,stroke:#4C1D95,stroke-dasharray:5 5,color:#C4B5FD
```

<details>
<summary><b>▶ Watch a single run, step by step</b> &nbsp;<sub>(illustrative trace)</sub></summary>
<br/>

```diff
  $ agent.invoke("Compare vector DB options for a 10M-doc RAG system")

+ [planner]     decomposed query → 3 sub-tasks
+ [research]    gathering benchmarks & docs ............. done
+ [rag]         retrieved top-k chunks from knowledge base  done
+ [tools]       structured comparison table generated ...... done
! [verifier]    claim about latency has no source → re-plan
+ [research]    fetched supporting source ................ done
+ [verifier]    all claims grounded ✓
+ [synthesizer] structured report ready

  ✔ status: verified · output: report.json
```

</details>

<br/>

<!-- ═══════════════════════════════ PROJECTS ═══════════════════════════════ -->
<h2 align="center">🚀 Featured Builds</h2>

<details open>
<summary><b>🧠 Production RAG Knowledge Worker</b> &nbsp;·&nbsp; <code>FastAPI</code> <code>LangChain</code> <code>pgvector</code> <code>Docker</code></summary>
<br/>

> **The problem:** organizations drown in documents nobody can search. <br/>
> **The build:** ask a question in plain language, get an answer **grounded in your own documents** — not hallucinated.

```mermaid
flowchart LR
    A[📄 Ingest] --> B[✂️ Chunk] --> C[🧠 Embed] --> D[(🐘 pgvector)]
    U([❓ Question]) --> E[🔎 Retrieve] 
    D --> E --> F[🤖 Generate] --> G[📊 Evaluate] --> H([💬 Grounded Answer])

    classDef s fill:#1E1B4B,stroke:#818CF8,color:#E0E7FF
    classDef io fill:#7C3AED,stroke:#DDD6FE,color:#fff
    class A,B,C,E,F,G s
    class U,H io
```

| Layer | What it does |
|:--|:--|
| 📄 **Ingestion** | Loads and preprocesses organizational documents |
| ✂️ **Chunking** | Context-preserving splits so meaning survives retrieval |
| 🧠 **Embeddings** | OpenAI embeddings stored in PostgreSQL + pgvector |
| 🔎 **Retrieval** | Semantic vector search surfaces the most relevant context |
| 🤖 **Generation** | LLM answers constrained to retrieved context |
| 📊 **Quality** | Evaluation layer + robust error handling |
| 🐳 **Deployment** | Fully Dockerized, production-ready |

<sub><b>Python · FastAPI · LangChain · OpenAI · PostgreSQL · pgvector · Docker</b></sub>

</details>

<details open>
<summary><b>🤖 Deep Research Multi-Agent System</b> &nbsp;·&nbsp; <code>LangGraph</code> <code>OpenAI API</code> <code>FastAPI</code> <code>Docker</code></summary>
<br/>

> **The problem:** hard questions need more than one search and one answer. <br/>
> **The build:** a team of **specialized agents** that plans, researches, fact-checks itself, and writes a structured report.

```mermaid
sequenceDiagram
    autonumber
    participant U as 🧑 User
    participant P as 🧩 Planner
    participant R as 🌐 Researchers
    participant V as ✅ Verifier
    participant S as 📝 Synthesizer
    U->>P: complex question
    P->>R: decomposed research tasks
    R->>V: extracted findings + sources
    alt weak or unsourced claim
        V-->>P: re-plan that branch
        P->>R: targeted follow-up
        R->>V: new evidence
    end
    V->>S: verified findings
    S->>U: structured report
```

| Layer | What it does |
|:--|:--|
| 🧩 **Planning** | Decomposes the question into focused research tasks |
| 🤖 **Orchestration** | Multi-agent coordination with LangGraph state |
| 🌐 **Research** | Web research and information extraction |
| ✅ **Verification** | Checks sources before anything reaches the report |
| 🔧 **Tools** | Tool calling with structured outputs |
| 📝 **Output** | Automated, structured report generation |

<sub><b>Python · LangGraph · OpenAI API · FastAPI · Docker</b></sub>

</details>

<br/>

<!-- ═══════════════════════════════ STACK ═══════════════════════════════ -->
<h2 align="center">🛠️ The Arsenal</h2>

<table align="center">
<tr>
<td align="center" width="140"><b>🤖 GenAI</b></td>
<td>
<img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/RAG-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Agentic_AI-7C3AED?style=flat-square" />
<img src="https://img.shields.io/badge/Tool_Calling-4C1D95?style=flat-square" />
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
<img src="https://img.shields.io/badge/pgvector-316192?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" />
</td>
</tr>
<tr>
<td align="center"><b>☁️ DevOps</b></td>
<td><img src="https://skillicons.dev/icons?i=aws,docker,git,github,linux&theme=dark" height="40" /></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ ACTIVITY ═══════════════════════════════ -->
<h2 align="center">🔥 Proof of Work</h2>

<p align="center">
  <a href="https://github.com/Subham999100">
    <img src="https://streak-stats.demolab.com/?user=Subham999100&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=C4B5FD&currStreakLabel=C4B5FD&sideLabels=A5B4FC&dates=8B949E&currStreakNum=E9D5FF&sideNums=E9D5FF" />
  </a>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Subham999100&bg_color=0D1117&color=C4B5FD&line=7C3AED&point=E9D5FF&area=true&area_color=7C3AED&hide_border=true&custom_title=Commits%20over%20time" width="100%" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Subham999100/Subham999100/output/github-snake-dark.svg" />
    <img src="https://raw.githubusercontent.com/Subham999100/Subham999100/output/github-snake.svg" alt="snake eating my contributions" width="100%" />
  </picture>
</p>

<br/>

<!-- ═══════════════════════════════ LEARNING ═══════════════════════════════ -->
<h2 align="center">🌱 Currently Training On</h2>

<details>
<summary><b>📖 See what's in my context window right now</b></summary>
<br/>

```yaml
epoch: current
loss: decreasing 📉

agents:
  - Advanced agentic AI architectures
  - Advanced LangGraph (state, checkpoints, human-in-the-loop)
  - Multi-agent systems & tool design

retrieval:
  - RAG architecture & optimization
  - LLM evaluation
  - Observability & tracing

production:
  - Production-grade GenAI systems
  - AI + cloud deployment (AWS)
```

</details>

<br/>

<!-- ═══════════════════════════════ COLLAB ═══════════════════════════════ -->
<h2 align="center">🤝 Let's Build Something That Thinks</h2>

<p align="center">
  <img src="https://img.shields.io/badge/AI_Agents-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Agentic_AI-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LangGraph_/_LangChain-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/RAG_Apps-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LLM_Backends-1E1B4B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open_Source_AI-1E1B4B?style=for-the-badge" />
</p>

```bash
$ ask subham --about "GenAI · RAG · AI Agents · LangGraph · LangChain · OpenAI API · FastAPI · Vector DBs · Python"
> response: always happy to talk. open an issue, star a repo, or just say hi 👋
```

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,55:1E1B4B,100:0D1117&height=130&section=footer&text=Building%20with%20AI.%20Learning%20every%20day.%20Shipping%20real%20systems.&fontSize=16&fontColor=DDD6FE&fontAlignY=72&animation=twinkling" width="100%" />
</p>
