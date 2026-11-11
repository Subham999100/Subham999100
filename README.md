<!-- ═══════════════════════════════ BANNER ═══════════════════════════════ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=venom&color=0:0D1117,50:1E1B4B,100:4C1D95&height=260&section=header&text=Subham%20Sekhar%20Patnaik&fontSize=48&fontColor=E9D5FF&fontAlignY=42&desc=GenAI%20Engineer%20%C2%B7%20Building%20AI%20Agents%20that%20actually%20ship&descSize=17&descAlignY=62&descAlign=50&stroke=A78BFA&strokeWidth=1&animation=fadeIn" width="100%" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2600&pause=900&color=C4B5FD&center=true&vCenter=true&width=700&lines=%3E+orchestrating+multi-agent+systems+with+LangGraph;%3E+building+production-grade+RAG+pipelines;%3E+wiring+LLMs+into+reliable+FastAPI+backends;%3E+learning+every+day.+shipping+real+systems." alt="typing" />
</p>

<p align="center">
  <a href="https://github.com/Subham999100?tab=repositories"><img src="https://img.shields.io/badge/Explore-Repositories-4C1D95?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Open%20to-Collaborate-16A34A?style=for-the-badge&logo=handshake&logoColor=white" />
  <img src="https://komarev.com/ghpvc/?username=Subham999100&label=VIEWS&color=6D28D9&style=for-the-badge" />
</p>

<br/>

<!-- ═══════════════════════════════ INTRO ═══════════════════════════════ -->
<h3 align="center">⚡ I build LLM-powered systems, from retrieval pipelines to autonomous multi-agent workflows.</h3>

<p align="center">
  Computer Science graduate turning GenAI concepts into <b>reliable backend services</b>.<br/>
  My focus: <b>Agentic AI</b>, <b>LangGraph</b>, <b>RAG</b>, <b>tool calling</b>, and <b>production deployment</b>.
</p>

<br/>

<table align="center">
<tr>
<td align="center" width="25%">🤖<br/><b>AI Agents</b><br/><sub>Agentic workflows & orchestration</sub></td>
<td align="center" width="25%">📚<br/><b>RAG Systems</b><br/><sub>Chunking, embeddings, retrieval</sub></td>
<td align="center" width="25%">🔧<br/><b>Tool Calling</b><br/><sub>Agents that act, not just talk</sub></td>
<td align="center" width="25%">🐳<br/><b>Production</b><br/><sub>FastAPI, Docker, AWS</sub></td>
</tr>
</table>

<br/>

<!-- ═══════════════════════════════ HOW I BUILD ═══════════════════════════════ -->
## 🧬 How I Build Agents

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

    classDef io fill:#4C1D95,stroke:#A78BFA,color:#fff
    classDef agent fill:#1E1B4B,stroke:#818CF8,color:#E0E7FF
    classDef check fill:#064E3B,stroke:#34D399,color:#D1FAE5
    class Q,O io
    class P,R,K,T,S agent
    class V check
```

<br/>

<!-- ═══════════════════════════════ PROJECTS ═══════════════════════════════ -->
## 🚀 Featured Work

<table>
<tr>
<td width="50%" valign="top">

<h3>🧠 Production RAG Knowledge Worker</h3>

<img src="https://img.shields.io/badge/type-RAG%20System-4C1D95?style=flat-square" />
<img src="https://img.shields.io/badge/stack-FastAPI%20%2B%20pgvector-1E1B4B?style=flat-square" />

<p>Ask questions across organizational documents and get grounded, context-aware answers powered by <b>Retrieval-Augmented Generation</b>.</p>

<b>Pipeline</b><br/>
<code>ingest</code> → <code>chunk</code> → <code>embed</code> → <code>retrieve</code> → <code>generate</code> → <code>evaluate</code>

<br/><br/>

<b>Highlights</b><br/>
✦ Intelligent document chunking<br/>
✦ Vector search with PostgreSQL + pgvector<br/>
✦ LLM response generation with context<br/>
✦ Evaluation & robust error handling<br/>
✦ Fully Dockerized deployment

<br/>

<sub><b>Python · FastAPI · LangChain · OpenAI · PostgreSQL · pgvector · Docker</b></sub>

</td>
<td width="50%" valign="top">

<h3>🤖 Deep Research Multi-Agent System</h3>

<img src="https://img.shields.io/badge/type-Multi--Agent-4C1D95?style=flat-square" />
<img src="https://img.shields.io/badge/stack-LangGraph-1E1B4B?style=flat-square" />

<p>Breaks complex questions into research tasks and coordinates <b>specialized agents</b> to produce verified, structured reports.</p>

<b>Pipeline</b><br/>
<code>decompose</code> → <code>research</code> → <code>extract</code> → <code>verify</code> → <code>synthesize</code>

<br/><br/>

<b>Highlights</b><br/>
✦ Query decomposition & task planning<br/>
✦ Multi-agent orchestration with LangGraph<br/>
✦ Web research with source verification<br/>
✦ Tool calling & structured outputs<br/>
✦ Automated report synthesis

<br/>

<sub><b>Python · LangGraph · OpenAI API · FastAPI · Docker</b></sub>

</td>
</tr>
</table>

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

```yaml
agents:       [Advanced Agentic AI architectures, Advanced LangGraph, Multi-agent systems]
retrieval:    [RAG architecture & optimization, LLM evaluation, Observability]
production:   [Production-grade GenAI systems, AI + Cloud deployment]
```

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
  <img src="https://streak-stats.demolab.com/?user=Subham999100&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=C4B5FD&currStreakLabel=C4B5FD&sideLabels=A5B4FC&dates=8B949E&currStreakNum=E9D5FF&sideNums=E9D5FF" />
</p>

<br/>

<!-- ═══════════════════════════════ FOOTER ═══════════════════════════════ -->
<p align="center">
  <b>🚀 Building with AI. Learning every day. Shipping real-world systems.</b>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:4C1D95,50:1E1B4B,100:0D1117&height=4&section=footer" width="100%" />
</p>
