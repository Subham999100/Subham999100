<!-- SUBHAM.AI — a GitHub-native interactive profile. No scripts, no fake dashboards. --><div align="center"><img src="./assets/hero.svg" width="100%" alt="Subham Sekhar Patnaik — I build AI that can act. An agent engineering dashboard." />


<a href="#-mission-control"><img src="https://img.shields.io/badge/01-MISSION_CONTROL-7C3AED?style=for-the-badge&labelColor=111827" alt="Mission Control" /></a>
<a href="#-agent-lab"><img src="https://img.shields.io/badge/02-AGENT_LAB-6D28D9?style=for-the-badge&labelColor=111827" alt="Agent Lab" /></a>
<a href="#-featured-builds"><img src="https://img.shields.io/badge/03-PROJECTS-4F46E5?style=for-the-badge&labelColor=111827" alt="Projects" /></a>
<a href="#-tech-stack"><img src="https://img.shields.io/badge/04-STACK-0E7490?style=for-the-badge&labelColor=111827" alt="Tech Stack" /></a>



AI AGENTS · LANGGRAPH · RAG · FASTAPI · PRODUCTION ENGINEERING

An interactive look at how I think, build, and explore AI systems.
</div>🖥 Mission Control
subham@agent-lab:~$ whoami

NAME      Subham Sekhar Patnaik
ROLE      GenAI Engineer
FOCUS     AI Agents · Multi-Agent Systems · RAG · LangGraph
BUILDING  LLM-powered backends and evidence-grounded workflows
MISSION   Turn promising AI prototypes into useful, reliable systems

subham@agent-lab:~$ help
  [1] Enter the Agent Lab
  [2] Inspect the Architecture
  [3] Open the Project Vault
  [4] Discover a Secret
<table>
<tr>
<td align="center" width="25%"><b>🧠 THINK</b><br/><sub>Planning &amp; reasoning</sub></td>
<td align="center" width="25%"><b>📚 REMEMBER</b><br/><sub>RAG &amp; retrieval</sub></td>
<td align="center" width="25%"><b>🔧 ACT</b><br/><sub>Tool execution</sub></td>
<td align="center" width="25%"><b>✅ VERIFY</b><br/><sub>Evidence &amp; evaluation</sub></td>
</tr>
</table>🕹 Agent Lab
Pick a mission to explore. The panels are interactive architecture walkthroughs—not live API executions.

<details>
<summary><b>🟣 MISSION 01 — Start the Research Agent</b> &nbsp; ▸ <i>Click to launch</i></summary>
$ agent run --mission deep-research
[✓] Query received
[✓] Planner initialized
[✓] Research, retrieval and tool paths prepared
[→] Entering evidence-gathering workflow...
<details>
<summary>🧩 <b>STEP 01 — Planner: decide what to investigate</b></summary>The planner breaks a complex question into research tasks, chooses appropriate sources and defines a stopping condition.
input: complex_research_question
plan:
  - decompose_problem
  - identify_required_evidence
  - assign_research_tasks
  - define_verification_checks
</details><details>
<summary>🌐 <b>STEP 02 — Specialists: retrieve, research, use tools</b></summary>Specialized paths collect relevant documents, extract useful details and invoke controlled tools as needed. Each returns structured findings for review.
</details><details>
<summary>🛡️ <b>STEP 03 — Verifier: accept or investigate further</b></summary>if evidence_is_sufficient and claims_are_supported:
    next_step = "synthesize"
else:
    next_step = "research_again"  # with a retry limit
The verifier should identify gaps—not simply declare every answer correct.
</details><details>
<summary>📦 <b>STEP 04 — Reveal the structured output</b></summary>{
  "result": "research_report",
  "sections": ["summary", "findings", "sources", "limitations"],
  "validation": "evidence_reviewed"
}
MISSION COMPLETE · The workflow returns a report with supporting evidence.
</details></details><details>
<summary><b>🔵 MISSION 02 — Open the RAG Memory Core</b> &nbsp; ▸ <i>Click to investigate</i></summary>
DOCUMENTS  →  CLEAN  →  CHUNK  →  EMBED
                                    ↓
QUESTION   →  SEARCH pgvector  →  CONTEXT  →  LLM  →  ANSWER
<details>
<summary>🔎 <b>What happens during retrieval?</b></summary>Documents are preprocessed and chunked. Embeddings are stored in PostgreSQL + pgvector. The question retrieves semantically relevant chunks, which become context for the LLM.
</details><details>
<summary>📏 <b>How do you know it's working?</b></summary>
Evaluate retrieval relevance, source coverage, answer faithfulness, missing-context behavior and failure handling—not just whether the generated text sounds convincing.
</details>
MISSION COMPLETE · Better retrieval produces better-grounded answers.
</details><details>
<summary><b>🟢 MISSION 03 — Inspect the Agent Tool Registry</b> &nbsp; ▸ <i>Click to inspect</i></summary>
from pydantic import BaseModel

class ToolResult(BaseModel):
    success: bool
    data: dict
    error: str | None = None
A conceptual tool-result contract: validate inputs and outputs, constrain permissions, handle timeouts and avoid treating tool output as trusted instructions.

MISSION COMPLETE · Useful agents act through controlled interfaces.
</details>🧬 Architecture
```mermaid
flowchart LR
    U(["USER QUERY"]) --> P{"PLANNER"}
    P --> R["RESEARCH"]
    P --> K["RAG RETRIEVAL"]
    P --> T["TOOLS"]
    R --> V{"VERIFY"}
    K --> V
    T --> V
    V -->|"Need evidence"| P
    V -->|"Sufficient"| S["SYNTHESIZE"]
    S --> O(["STRUCTURED OUTPUT"])

    classDef io fill:#7C3AED,stroke:#DDD6FE,color:#ffffff,stroke-width:2px
    classDef agent fill:#1E1B4B,stroke:#818CF8,color:#ffffff
    classDef verify fill:#064E3B,stroke:#34D399,color:#ffffff
    class U,O io
    class P,R,K,T,S agent
    class V verify
```
<details>
<summary>💡 <b>Design principle: more agents ≠ better agents</b></summary>Use multiple agents when their separation improves reliability, tool permissions or task clarity. Prefer a simpler workflow when coordination overhead adds no measurable value. Give verification loops explicit stopping conditions.
</details>🚀 Featured Builds
<details>
<summary><b>01 / 🧠 Production RAG Knowledge Worker</b> &nbsp; ▸ <i>Open blueprint</i></summary>
Purpose: Ask questions about organizational documents and generate context-aware answers grounded in retrieved knowledge.
INGEST → PREPROCESS → CHUNK → OPENAI EMBEDDINGS
    → POSTGRESQL + PGVECTOR → RETRIEVE → GENERATE → EVALUATE
Layer	Implementation
API	Python · FastAPI
Retrieval pipeline	LangChain · semantic search
Storage	PostgreSQL · pgvector
Generation	OpenAI API + retrieved context
Reliability	Error handling · evaluation
Packaging	Docker


</details><details>
<summary><b>02 / 🤖 Deep Research Multi-Agent System</b> &nbsp; ▸ <i>Open blueprint</i></summary>
Purpose: Decompose complex questions, coordinate specialized research tasks, verify findings and synthesize structured reports.
QUESTION → PLAN → RESEARCH / EXTRACT / TOOLS
                → VERIFY ↻ → SYNTHESIZE → REPORT
Layer	Implementation
Orchestration	LangGraph
Models	OpenAI API
Tools	Research · extraction · tool calling
Validation	Evidence checking + structured output
API & packaging	Python · FastAPI · Docker


</details><p align="center">
  <a href="https://github.com/Subham999100?tab=repositories"><img src="https://img.shields.io/badge/EXPLORE_MY_REPOSITORIES-7C3AED?style=for-the-badge&logo=github&logoColor=white" alt="Explore repositories" /></a>
</p>🛠 Tech Stack
<div align="center">AI / Orchestration
<img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/LangGraph-7C3AED?style=flat-square" />
<img src="https://img.shields.io/badge/RAG-2563EB?style=flat-square" />
Backend · Data · Cloud
<img src="https://skillicons.dev/icons?i=python,fastapi,java,spring,ts,postgres,mongodb,aws,docker,git,github,linux&theme=dark" alt="Tech stack icons" />
pgvector · FAISS · REST APIs · Docker
</div>🌱 Now Exploring
Advanced LangGraph · State, checkpointing, human-in-the-loop

RAG Engineering · Better retrieval, LLM evaluation, tracing

Production GenAI · Reliable APIs, observability, AWS deployment
📡 Live Signals
<details>
<summary>📈 <b>Open GitHub activity telemetry</b></summary>
<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=Subham999100&bg_color=0D1117&color=C4B5FD&line=8B5CF6&point=E9D5FF&area=true&hide_border=true" width="100%" alt="GitHub activity graph" />
<br/>
<img src="https://streak-stats.demolab.com/?user=Subham999100&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=C4B5FD" alt="GitHub contribution streak" />
</div></details><div align="center">
<img src="https://komarev.com/ghpvc/?username=Subham999100&label=VISITORS&color=7C3AED&style=flat-square" alt="Profile visits" />
</div>🤝 Let's Build
<div align="center">Open to discussing AI agents, RAG systems, LangGraph and LLM backends.

<a href="https://github.com/Subham999100"><img src="https://img.shields.io/badge/FIND_ME_ON_GITHUB-7C3AED?style=for-the-badge&logo=github&logoColor=white" alt="GitHub profile" /></a>
</div><details>
<summary>🔐 <b>CLASSIFIED · /secrets/final_message.txt</b> &nbsp; ▸ <i>Not all visitors find this</i></summary>$ cat /secrets/final_message.txt

ACCESS GRANTED.

Most people scroll. Engineers investigate.
Most people consume. Builders ask how it works.
Most people quit. Curious minds keep debugging.

ACHIEVEMENT UNLOCKED: THE CURIOUS ENGINEER
FLAG{STAY_CURIOUS_KEEP_BUILDING}
Thanks for exploring beyond the surface.
</details><div align="center">
BUILD → LEARN → VERIFY → IMPROVE → REPEAT

<sub>SUBHAM.AI / The Agentic Engineering Lab</sub>
</div>
