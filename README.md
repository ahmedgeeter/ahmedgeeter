<div align="center">

# Ahmed Gaiter

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=1200&color=6366F1&center=true&vCenter=true&width=750&lines=AI+%26+Backend+Software+Engineer;Asynchronous+Python+(FastAPI+%26+AsyncIO);Stateful+Agentic+Workflows+(LangGraph);Distributed+Task+Queues+(Redis+%26+Celery);Production+RAG+%26+LLM+Resilience+Routing" alt="Typing Banner" />

<p align="center">
  <a href="https://www.ahmedgaiter.site/"><img src="https://img.shields.io/badge/Portfolio-ahmedgaiter.site-0f172a?style=flat-square&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/ahmed-ai-dev/"><img src="https://img.shields.io/badge/LinkedIn-ahmed--ai--dev-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://github.com/ahmedgeeter"><img src="https://img.shields.io/badge/GitHub-ahmedgeeter-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="mailto:ahmedekramy303@gmail.com"><img src="https://img.shields.io/badge/Email-ahmedekramy303%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

</div>

---

### Specialization & Engineering Principles

While frontier Large Language Models are inherently probabilistic, production systems wrapping them must be deterministic, observable, and resilient. 

I focus on the core backend engineering required to make AI reliable at scale:

- **Asynchronous API Gateways:** Engineering non-blocking API gateways and full-duplex WebSockets using **Python (AsyncIO)** and **FastAPI** to maintain sub-second streaming latencies.
- **Stateful Multi-Agent Workflows:** Developing state machines via **LangGraph**, enforcing strict tool-calling boundaries, state persistence, and dynamic evaluation rubrics.
- **Concurrency & Background Processing:** Offloading compute-heavy inference, document parsing, and scoring jobs to **Celery workers** backed by **Redis** queues and **PostgreSQL**.
- **Deterministic Validation & Safety:** Guaranteeing API payload integrity with **Pydantic v2** schemas, regex-compiled prompt injection filters, and multi-provider fallback routing (Groq ➔ Gemini ➔ OpenAI).

---

### Technologies & Tooling

<div align="center">

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=python,fastapi,postgres,redis,docker,kubernetes,git,linux,typescript,nextjs,react,tailwind&theme=dark" alt="Tech Stack Icons" />
</a>

</div>

<br/>

| Domain | Core Stack & Frameworks |
| :--- | :--- |
| **Backend & Concurrency** | Python (AsyncIO), FastAPI, Full-Duplex WebSockets, Celery, Redis (Pub/Sub & Caching) |
| **AI & Agentic Systems** | LangGraph, RAG Architecture, Tool-Calling Guardrails, LiteLLM, Whisper, Vision LLMs |
| **Databases & Integrity** | PostgreSQL, Alembic Migrations, SQLite, Pydantic v2 Strict Validation |
| **Infrastructure & DevOps** | Docker, Docker Compose, Kubernetes Manifests, GitHub Actions (CI/CD), Linux |
| **Testing & Quality** | Pytest, Async Fixtures, Mock LLM Test Suites, CI Workflow Automation |

---

### Core Production Architectural Patterns

Instead of building brittle direct-API wrappers, my systems implement three proven production patterns:

#### 1. Concurrency Decoupling Pattern
> **Problem:** Running audio processing, LLM evaluation, and scoring inside an open WebSocket connection blocks the event loop and introduces 3–5 second candidate freezes.  
> **Solution:** The WebSocket router handles only streaming communication; transcript scoring and multi-metric evaluations are dispatched asynchronously to Celery workers backed by Redis.

#### 2. Deterministic Agent Sandboxing
> **Problem:** Autonomous LLM agents are prone to hallucinations, unauthorized operations, and schema drift.  
> **Solution:** Agents are modeled as LangGraph state machines restricted to verified, authenticated tool boundaries (`get_shipment_status`, `verify_customer`, `cancel_shipment`) with Pydantic output validation.

#### 3. Multi-Provider Fallback Routing
> **Problem:** Upstream LLM providers encounter rate limits (429), regional outages, or latency spikes during peak load.  
> **Solution:** Primary traffic routes to ultra-fast LPUs (Groq Llama/Qwen) with automated runtime fallback chains to Google Gemini Flash and OpenAI.

---

### Flagship Systems (Live & Open Source)

<table>
  <thead>
    <tr>
      <th width="24%">System</th>
      <th width="44%">Architecture & Highlights</th>
      <th width="18%">Tech Stack</th>
      <th width="14%">Repository</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong>AutoHire</strong><br/>
        <em>Autonomous Technical Interviewer</em>
      </td>
      <td>
        • Full-duplex WebSocket architecture in FastAPI for bi-directional streaming.<br/>
        • Event-driven LangGraph state machine calibrating questions dynamically.<br/>
        • Asynchronous transcript scoring via Celery workers backed by Redis.<br/>
        • Automated provider fallback (Groq ➔ Gemini) for uninterrupted uptime.<br/>
        • Full Pytest test suite covering WebSocket lifecycle and mock fixtures.
      </td>
      <td>
        <code>Python (AsyncIO)</code><br/>
        <code>FastAPI</code> <code>WebSockets</code><br/>
        <code>LangGraph</code> <code>Celery</code><br/>
        <code>Redis</code> <code>Pytest</code>
      </td>
      <td>
        <a href="https://ai-automation-interview.vercel.app/"><strong>Live Demo</strong></a><br/>
        <a href="https://github.com/ahmedgeeter/ai-interview-automation"><strong>GitHub Repo</strong></a>
      </td>
    </tr>
    <tr>
      <td>
        <strong>Meridian</strong><br/>
        <em>Multimodal Document & Vocal Inspector</em>
      </td>
      <td>
        • Vision-language pipeline auditing blueprints and invoices via Llama 3.2 Vision.<br/>
        • Whisper voice integration with intelligent Voice Activity Detection (VAD).<br/>
        • Strict Pydantic v2 schema validation preventing model hallucinations.<br/>
        • Dockerized backend with full Pytest integration test suite.
      </td>
      <td>
        <code>Python</code> <code>FastAPI</code><br/>
        <code>Llama 3.2 Vision</code><br/>
        <code>Whisper</code> <code>Pydantic v2</code><br/>
        <code>React</code> <code>TypeScript</code>
      </td>
      <td>
        <a href="https://ai-auditor-ocr-voice.vercel.app/"><strong>Live Demo</strong></a><br/>
        <a href="https://github.com/ahmedgeeter/ai-auditor-ocr-voice"><strong>GitHub Repo</strong></a>
      </td>
    </tr>
    <tr>
      <td>
        <strong>Shiphny</strong><br/>
        <em>Multi-Agent Logistics Platform</em>
      </td>
      <td>
        • LangGraph cyclic state machine enforcing authenticated tool boundaries.<br/>
        • Decoupled background workflows with Redis sessions and PostgreSQL ledgers.<br/>
        • Automated multi-provider LLM fallback routing across Groq and Gemini.<br/>
        • Automated CI/CD pipeline building Docker images to GHCR with Helm charts.
      </td>
      <td>
        <code>FastAPI</code> <code>LangGraph</code><br/>
        <code>PostgreSQL</code> <code>Redis</code><br/>
        <code>Docker</code> <code>CI/CD</code><br/>
        <code>Terraform</code> <code>Helm</code>
      </td>
      <td>
        <a href="https://shiphny-ai-support.vercel.app/"><strong>Live Demo</strong></a><br/>
        <a href="https://github.com/ahmedgeeter/shiphny-ai-support"><strong>GitHub Repo</strong></a>
      </td>
    </tr>
    <tr>
      <td>
        <strong>AI Guardrail API</strong><br/>
        <em>High-Throughput Safety Middleware</em>
      </td>
      <td>
        • Pre-flight prompt inspection catching injection and jailbreak patterns.<br/>
        • Automated regex-compiled PII redaction (Emails, Phones, Cards, API Keys).<br/>
        • Sub-5ms latency overhead engineered for enterprise API gateways.<br/>
        • Full Pytest test suite covering clean queries, injection attacks, and PII.
      </td>
      <td>
        <code>Python</code> <code>FastAPI</code><br/>
        <code>Pydantic v2</code> <code>Docker</code><br/>
        <code>Regex Automata</code><br/>
        <code>Pytest</code>
      </td>
      <td>
        <a href="https://github.com/ahmedgeeter/LLM-Safety-Guardrail-API"><strong>GitHub Repo</strong></a>
      </td>
    </tr>
  </tbody>
</table>

---

### Professional Experience

- **Software Engineer (AI & Backend) | Independent Contractor** *(Jan 2024 – Present)*
  - Designed and deployed asynchronous RAG pipelines and multi-agent backend APIs using FastAPI and Python.
  - Implemented multi-provider LLM fallback routing to eliminate upstream rate limits and ensure service availability.
  - Architected asynchronous task queues backed by Redis to decouple heavy inference workflows from API response loops.

- **AI Integration Engineer | Springer Capital** *(Remote Contract · May 2025 – Sep 2025)*
  - Developed custom Python automation scripts and LLM endpoints for operational workflow synchronization.
  - Standardized data schemas across ingestion pipelines in collaboration with a remote engineering team.

- **AI Alignment & Code Security Specialist | Atlas Capture** *(Remote Contract · Dec 2024 – Feb 2025)*
  - Audited and debugged complex Python and TypeScript code generated by frontier LLMs for RLHF alignment benchmarks.
  - Evaluated prompt injection vectors and adversarial attack datasets to reinforce model response reliability.

- **B.Sc. in Computer Science** *(Mansoura University, Egypt · 2019 – 2023)*

---

### Contact

- **Portfolio:** [ahmedgaiter.site](https://www.ahmedgaiter.site/)
- **LinkedIn:** [linkedin.com/in/ahmed-ai-dev](https://www.linkedin.com/in/ahmed-ai-dev/)
- **Email:** [ahmedekramy303@gmail.com](mailto:ahmedekramy303@gmail.com)
- **Location:** Cairo, Egypt (Available for Remote worldwide & Relocation)
