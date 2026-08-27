# Hatem Shalaby

Operations Architect & AI Systems Engineer

> I build systems that transform manual operational headaches into automated, predictive intelligence. My work spans workforce management, learning & development, and AI-powered desktop applications — all designed to run on modest hardware without cloud dependencies.

---

## The Journey

After 28 years in operations, I kept hitting the same walls: manual forecasting, fragmented tools, reactive firefighting. So I started building solutions.

**Phase 1 — Standalone Prototypes** (June 2026): Built five individual tools to solve specific operational problems — Erlang C forecasting, real-time adherence dashboards, NLP churn prediction, B2B onboarding automation, and workforce modeling experiments. Each lived in its own repository.

**Phase 2 — Helix Prime** (July–August 2026): Realized these should be one system. Consolidated all five engines into a unified operations platform with six domain-specific engines, four AI agents, a content-based orchestrator, and a Streamlit Operations Cockpit.

**Phase 3 — The Learning Ecosystem** (August 2026): Extended the platform into education — Study Studio as the local AI learning engine core, Helix Education as the event-sourced learning state layer, and L&D Command Center as a desktop-first L&D product.

This profile tells that story honestly. The public repos are the current state. The private repos are where it started.

---

## Technical Core

* **Workforce Management (WFM):** Erlang C modeling, interval-based forecasting, shrinkage analysis, and predictive scheduling.
* **AI-Powered Desktop Apps:** Offline-first, local-model applications using LM Studio + PyInstaller for zero-cloud deployment.
* **Data Engineering:** Python (Pandas/SQLAlchemy), SQL, automated data pipeline orchestration, and real-time analytics.
* **Operations Intelligence:** Real-time SLA monitoring, NLP-driven sentiment analysis, and churn prediction.
* **Automation:** End-to-end B2B client onboarding pipelines, automated SOP provisioning, and career development agents.
* **Language Learning:** Bilingual podcast generation, spaced repetition, grammar drills, and interactive HTML learning experiences.

---

## Portfolio — The Helix Ecosystem

### [Helix Prime](https://github.com/HatemIsmailShalaby1979/Helix-Prime) — Try the Cockpit

The unified operations platform. Six business engines (WFM/Erlang C, RTA, CX Churn Sentinel, B2B Onboarding, Personnel, CRM), four AI agents (SAMI, SUBY, PHILI, WILI), content-based orchestration, and a Streamlit Operations Cockpit. **Run it locally:** clone, run `setup.bat`, then `launch.bat` — cockpit opens at `http://127.0.0.1:8501`.

### [Helix Education](https://github.com/HatemIsmailShalaby1979/Helix-Education)

Event-sourced learning state engine. Generates adaptive learning journeys with citation-grounded content generation, sealed quiz scoring, and full state reconstruction from an append-only event store. 447 passing tests. Python, Pydantic, pytest.

### [Study Studio](https://github.com/HatemIsmailShalaby1979/Study-Studio) — Try it Now

Offline-first AI learning application. Turns topics into structured lessons, quizzes, glossaries, and podcasts — all running against local models. **Run it now:** `cd apps/desktop && npm install && npm run dev` — opens at `http://localhost:3000`. Desktop (Tauri) and mobile (Expo) in one monorepo.

### [L&D Command Center](https://github.com/HatemIsmailShalaby1979/L-D-Command-Center)

Desktop-only L&D command center. Learning Journeys, Language Lab (bilingual podcast generator), Career Development (resume tools + job board search), and a universal media playground. Runs on modest hardware via LM Studio. 730+ tests, 93.6% coverage.

### [LIVE Support Assistant](https://github.com/HatemIsmailShalaby1979/LIVE-Support-Assistant) — Try it Now

A working keyword-matching support assistant built with React, Vite, and TypeScript. **Run it now:** `npm install && npm run dev` — opens at `http://localhost:5173`. Paste a customer message, click "Find Answer", see the matched policy and suggested reply. Production build available in `dist/`.

---

## Precursor Work (Private)

These five repositories are the standalone prototypes that were consolidated into Helix Prime. They remain private — the code evolved and was absorbed into the unified platform.

| Repository | What it did |
| --- | --- |
| **wfm-forecasting-calculator** | Erlang C staffing model, shrinkage analysis, interval planning, FTE cost modeling |
| **RTA_command_center** | Real-time adherence dashboard with auto-alert thresholds and anomaly detection |
| **cx-sentiment-sentinel** | NLP-driven churn prediction and sentiment monitoring pipeline |
| **Dynamic-Ops-Automation-Engine** | Intake-to-readiness pipeline: staffing schedules + Notion SOP provisioning in under 60 minutes |
| **META-COGNITIVE-WFM-ENGINE** | Advanced workforce modeling experiments |

---

## Connect

[LinkedIn](https://www.linkedin.com/in/hatem-shalaby-202902127/) · [Portfolio](https://hatemshalaby.com) · [Email](mailto:hatem@shalaby.dev)

---

*Building at the intersection of operational strategy, AI engineering, and human-centered learning.*
