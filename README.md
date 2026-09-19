# Afnan B.R.

> **Software Developer** &nbsp;|&nbsp; Full-Stack Web Development, Multi-Agent Systems & Developer Tooling  
> [Portfolio](https://afnan-portfolio-eta.vercel.app/) &nbsp;•&nbsp; [LinkedIn](https://www.linkedin.com/in/afnan-391912363)

```
┌── Engineering Focus ───────────────────────────────────────────────────────────┐
│  • Deterministic Multi-Agent Pipelines     • 3D Data Visualization (Three.js)  │
│  • Resilient Full-Stack Applications       • Observability & Metric Tooling    │
└────────────────────────────────────────────────────────────────────────────────┘
```

---

## Featured Systems

### [BizPilot AI](https://github.com/Afnan-0206/BizPilot)
*Multi-agent administrative assistant automating message-to-invoice workflows.*

```
Customer Message
       │
       ▼
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Parser Agent │ ──► │ Pricer & DB  │ ──► │ Drafter Agent│ ──► │ QA Reviewer  │ ──► Structured Output
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

- **Stack:** React 19, Node.js, Express, Google Gemini API, Tailwind CSS
- **Mechanics:** 4-stage sequential agent pipeline that extracts order intents from unstructured inquiries, computes pricing tables, drafts quotes/invoices, and applies an automated QA validation pass before saving drafts.
- **Live Demo:** [biz-pilot.vercel.app](https://biz-pilot.vercel.app)

---

### [Recoup](https://github.com/Afnan-0206/recoup)
*Payment failure diagnostic dashboard built for the Razorpay AI Buildathon.*

```
Failed Webhook ──► Error Categorization ──► Adaptive Retry Scheduler ──► Customer Outreach
(Gateway Event)     (Network / Auth / Funds)      (Backoff Windows)           (Claude 3.5 Sonnet)
```

- **Stack:** React 18, Vite, Node.js, SQLite, Anthropic Claude API, Framer Motion
- **Mechanics:** Inspects transaction failure payloads, isolates root failure conditions (insufficient balance, network timeout, authentication drop), and computes targeted retry windows alongside contextual recovery outreach.

---

### [NammaFix AI](https://github.com/Afnan-0206/nammafix-ai)
*Civic infrastructure reporting portal with 3D municipal infrastructure visualization.*

```
Citizen Report ──► Defect Classification ──► Severity Scoring (0–100) ──► Three.js Ward Matrix
```

- **Stack:** React 18, Vite, Three.js, Tailwind CSS, React Router
- **Mechanics:** Streamlines municipal defect reporting (road hazards, water leaks, sanitation) through category triage, numerical severity evaluation, ward-level routing, and an interactive Three.js 3D infrastructure canvas.

---

### [AutoFix AI](https://github.com/Afnan-0206/autofix-ai-incidents)
*AI-assisted DevOps incident triage agent for application error logs.*

```
Log / Stack Trace ──► Semantic Parser ──► Knowledge Retrieval ──► Remediation Patch
```

- **Stack:** React, Node.js, Express, LLM API Integration
- **Mechanics:** Parses error logs and runtime stack traces, queries documentation for root-cause context, formulates targeted remediation steps, and dispatches incident alerts.

---

## Open Source Contributions

| Repository | Status | Contribution Details |
| :--- | :---: | :--- |
| **[prometheus/client_js](https://github.com/prometheus/client_js)** | `OPEN` | **[PR #857](https://github.com/prometheus/client_js/pull/857)**: Added `zero()` method to `Summary` metrics with full test suite in `test/summaryTest.js` and TypeScript definitions in `index.d.ts`. |
| **[Create-Node-App/cna-templates](https://github.com/Create-Node-App/cna-templates)** | `MERGED` | **[PR #331](https://github.com/Create-Node-App/cna-templates/pull/331)**: Authored maintainer setup guide and configuration docs for Next.js + Tailwind CSS template. |

---

## Technical Stack Matrix

```
┌─────────────────┬──────────────────────────────────────────────────────────────┐
│ Domain          │ Technologies & Tooling                                       │
├─────────────────┼──────────────────────────────────────────────────────────────┤
│ Languages       │ JavaScript (ES6+), TypeScript, Python, C++, SQL              │
│ Frontend        │ React 18/19, Vite, Three.js, Tailwind CSS, Framer Motion     │
│ Backend & APIs  │ Node.js, Express, REST APIs, WebSockets                      │
│ AI Systems      │ Multi-Agent Pipelines, Gemini API, Claude API                │
│ Data & DevOps   │ Supabase, SQLite, Docker, Git                                │
└─────────────────┴──────────────────────────────────────────────────────────────┘
```
