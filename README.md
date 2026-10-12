# Afnan B.R.

> **AI Product Builder & Systems Engineer** &nbsp;|&nbsp; Bengaluru, India  
> [Portfolio](https://afnan-portfolio-eta.vercel.app/) &nbsp;•&nbsp; [LinkedIn](https://www.linkedin.com/in/afnan-391912363) &nbsp;•&nbsp; [GitHub](https://github.com/Afnan-0206) &nbsp;•&nbsp; [brafnan26@gmail.com](https://mail.google.com/mail/?view=cm&fs=1&to=brafnan26@gmail.com)

```
┌── Engineering Philosophy ──────────────────────────────────────────────────────────────┐
│  • High-concurrency systems, database internals & black-box isolation verification     │
│  • Deterministic multi-agent pipelines & autonomous explainable AI workflows            │
│  • Benchmarking & observability tooling for LLM inference (TTFT, latency percentiles)   │
│  • Local-first, edge architectures & tactile 3D visualization (Three.js)               │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Flagship Systems & Core Engineering

### 1. [IsoCheck — Black-Box Transaction Isolation Checker](https://github.com/Afnan-0206/IsoCheck)
*High-performance verification engine that infers dependency graphs from client histories to detect isolation anomalies.*

```
┌────────────────────────┐      ┌────────────────────────┐      ┌────────────────────────┐
│ Client-Observed Txns   │ ───► │ Dependency Graph       │ ───► │ Iterative Tarjan's SCC │ ───► Minimal Cycle Witness
│ (Concurrent SQL Runs)  │      │ (wr, ww, rw Edges)     │      │ & Shortest BFS Cycle   │      (G0, G1, G-single, G2)
└────────────────────────┘      └────────────────────────┘      └────────────────────────┘
```

- **Stack:** C++20, Python 3.12, PostgreSQL 17, Cloudflare Pages
- **Mechanics:** Analyzes concurrent client execution logs, infers per-key version orders, constructs direct read/write dependency graphs, and discovers isolation anomalies via an explicit heap-allocated DFS Tarjan's SCC and BFS cycle recovery.
- **Performance:** Processes ~142,000 txns/sec single-threaded with sub-millisecond anomaly detection on $10^4$ operations at $< 45\text{ MB}$ memory footprint.
- **Live Tool:** [isocheck.pages.dev](https://isocheck.pages.dev/) &nbsp;|&nbsp; **Interactive Playground:** [isocheck.pages.dev/#/playground](https://isocheck.pages.dev/#/playground)

---

### 2. [InferLoad — LLM Inference Load Testing & Capacity Planner](https://github.com/Afnan-0206/inferLoad)
*Dedicated load-generation and capacity-analysis laboratory designed around the execution mechanics of LLM serving.*

```
┌────────────────────────┐      ┌────────────────────────┐      ┌────────────────────────┐
│ Controlled Workload    │ ───► │ Streaming SSE Client   │ ───► │ High-Precision Clocks  │ ───► Capacity & SLO Report
│ (Ramp-up, Concurrency) │      │ (OpenAI-compatible)    │      │ (TTFT, ITL, Velocity)  │      (p50, p95, p99 Latency)
└────────────────────────┘      └────────────────────────┘      └────────────────────────┘
```

- **Stack:** Python 3.12, FastAPI, AsyncIO, Render, REST / SSE
- **Mechanics:** Sits external to model servers to generate synthetic concurrency while recording monotonic nanosecond timestamps (`perf_counter`). Computes Time to First Token (TTFT), Inter-Token Latency (ITL), token generation velocity, and SLO compliance curves without premature rounding.
- **Live Console:** [inferload.onrender.com](https://inferload.onrender.com/)

---

### 3. [BizPilot AI — Autonomous Multi-Agent Business Copilot](https://github.com/Afnan-0206/BizPilot)
*Autonomous enterprise administrative agent turning unstructured customer inquiries into verified invoices.*

```
Customer Message
       │
       ▼
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Parser Agent │ ──► │ Pricer & DB  │ ──► │ Drafter Agent│ ──► │ QA Reviewer  │ ──► Structured Output
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

- **Stack:** React 19, Node.js, Express, Google Gemini API, Tailwind CSS, Vercel
- **Mechanics:** 4-stage sequential agent pipeline that extracts order intents from unstructured conversations, queries pricing rules, drafts quotes/invoices, and runs an automated QA review pass before persisting to the ledger.
- **Live Demo:** [biz-pilot.vercel.app](https://biz-pilot.vercel.app/)

---

### 4. [Setu — Autonomous AI Payment Reconciliation Engine](https://github.com/Afnan-0206/setu-reconcile)
*The 6-second autonomous UPI & invoice reconciliation platform built for the ChatGPT CODEX Hackathon 2026.*

```
┌────────────────────────┐      ┌────────────────────────┐      ┌────────────────────────┐
│ Raw UPI & Bank Feeds   │ ───► │ 7-Node Explainability  │ ───► │ AI Chartered           │ ───► Audit-Ready Ledgers
│ (Vague SMS / UTR data) │      │ Decision Tree Pipeline │      │ Accountant Agent       │      (6-Sec Auto Resolution)
└────────────────────────┘      └────────────────────────┘      └────────────────────────┘
```

- **Stack:** TypeScript, React, Vite, Tailwind CSS, LLM Decision Trees
- **Mechanics:** Ingests chaotic bank feeds (PhonePe, Google Pay, Paytm, HDFC) and matches them to open invoices using a deterministic 7-node decision tree (`Amount` → `Name` → `Date` → `Narration` → `UTR` → `Duplicate` → `Resolution`) paired with an AI accountant reasoning agent.

---

### 5. [FieldNote — Local-First AI Nature Journal](https://github.com/Afnan-0206/FieldNote)
*Distraction-free nature observation journal engineered for the Hacktoberfest 2026 DEV Challenge ("Touch Grass").*

```
Field Notes / Photos ──► On-Device Local Storage ──► Edge / Local LLM ──► Ecological Synthesis
(Zero Telemetry)          (100% Client-Side)        (Llama 3.2 / Qwen 2.5)   (Structured Field Log)
```

- **Stack:** React, Node.js, Cloudflare Workers AI (`@cf/meta/llama-3.2-3b-instruct`), Ollama (Qwen 2.5 7B), Cloudflare Pages
- **Mechanics:** Local-first privacy architecture with on-device `localStorage`, zero user tracking, and edge AI synthesis that converts fragmented field notes into structured biological records.
- **Live App:** [fieldnote-byg.pages.dev](https://fieldnote-byg.pages.dev/)

---

### 6. [Recoup — Payment Failure Diagnostic & Recovery Agent](https://github.com/Afnan-0206/recoup)
*Intelligent recovery agent developed for the Razorpay AI Buildathon.*

- **Stack:** React 18, Vite, Node.js, SQLite, Anthropic Claude 3.5 Sonnet, Framer Motion
- **Mechanics:** Ingests gateway webhooks, isolates root transaction failure causes (auth timeout, balance, network drop), and calculates adaptive retry schedules alongside contextual customer outreach.

---

### 7. [Cortex — Competitive Mental Athletics Platform](https://github.com/Afnan-0206/Cortex)
*Real-time 1v1 brain training platform replacing doomscrolling with sharp, competitive mental duels.*

- **Stack:** Expo SDK 57, TypeScript 5.x, Supabase Realtime, React Native
- **Mechanics:** Sub-50ms synchronized multiplayer logic and memory duels over Supabase Realtime channels with persistent ELO rating and anti-cheat state verification.

---

### 8. [NammaFix AI — Civic Infrastructure Reporting with 3D Matrix](https://github.com/Afnan-0206/nammafix-ai)
*Civic grievance redressal portal integrating interactive Three.js 3D city ward visualization.*

- **Stack:** React 18, Vite, Three.js, Tailwind CSS, React Router
- **Mechanics:** Classifies municipal defect reports, computes automated severity scores (0–100), and projects live ward-level status over an interactive Three.js 3D infrastructure model.

---

## 🌐 Open Source Contributions

| Repository | Status | Impact & Contribution Details |
| :--- | :---: | :--- |
| **[prometheus/client_js](https://github.com/prometheus/client_js)** | `OPEN` | **[PR #857](https://github.com/prometheus/client_js/pull/857)**: Implemented `zero()` method for `Summary` metric types with comprehensive unit tests (`test/summaryTest.js`) and TypeScript type definitions (`index.d.ts`). |
| **[Create-Node-App/cna-templates](https://github.com/Create-Node-App/cna-templates)** | `MERGED` | **[PR #331](https://github.com/Create-Node-App/cna-templates/pull/331)**: Authored maintainer onboarding guide, environment setup workflow, and configuration documentation for Next.js + Tailwind CSS. |

---

## 💻 Technical Matrix

```
┌──────────────────┬────────────────────────────────────────────────────────────────────────┐
│ Domain           │ Technologies & Tooling                                                 │
├──────────────────┼────────────────────────────────────────────────────────────────────────┤
│ Languages        │ C++20, TypeScript, Python 3.12, JavaScript (ES6+), SQL                 │
│ AI & Agents      │ Multi-Agent DAGs, Google Gemini API, Claude 3.5 Sonnet, Ollama,        │
│                  │ Cloudflare Workers AI (LLaMA 3.2), LangChain, Decision Tree Engines    │
│ Systems & Perf   │ Concurrency Verification (SCC/BFS), LLM Load Testing (TTFT/ITL),      │
│                  │ Server-Sent Events (SSE), WebSockets, AsyncIO                          │
│ Frontend & 3D    │ React 18/19, Next.js, Vite, Three.js, React Native (Expo), Tailwind    │
│ Backend & Data   │ Node.js, Express, FastAPI, PostgreSQL 17, SQLite, Supabase, Redis      │
│ DevOps & Cloud   │ Cloudflare Workers/Pages, Docker, Render, Vercel, Prometheus, Git       │
└──────────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

<div align="center">
  <sub>Designed & engineered by <b>Afnan B.R.</b> — every pixel, every agent, every API.</sub>
</div>
