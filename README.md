<div align="center">

# Hatem Ismail Shalaby

**Operations Architect · AI Systems Engineer · Founder**

</div>

> [!NOTE]
> Deterministic where a decision has consequences, audited so any action can be replayed, and fail-closed by default. On missing input or missing authority, the system refuses rather than guesses.

## The operating rule

I spent three decades on the operational floor — aviation ground control, telecom
support, and contact-centre workforce management. The lesson that survived every one
of those jobs is that the hard part is never the model. It is the handover: who owns
the decision, what evidence supports it, and what happens when the system is wrong.

So everything here is built on one rule. **Deterministic where a decision has
consequences, audited so any action can be replayed, and fail-closed by default** — on
missing input or missing authority, the system refuses rather than guesses. A
generative model may help a person think, but it never sits alone in the path that
executes.

## The founder's story

I spent twenty-eight years in operations. The first fourteen were the foundation:
ground operations and real-time traffic management at Hurghada International
Airport, then Air Berlin, where I directed ground operations through the 2011
regional transition and held SLA compliance under conditions that had no playbook.
Alongside that, international logistics at Shorouk International Bookshop and hybrid
IT operations at Nefertari American School.

The second fourteen were about automation. I built AI-driven automation for contact
centres at ByteDance, Vodafone and Uber: NLP pipelines that turn unstructured
customer language into signal, Erlang C forecasting that turns volume into staffing,
and the reporting layers that made both usable by people on the floor. The hard part
was never the model. It was the handover — who owns the decision, what evidence
supports it, and what happens when the system is wrong.

In April 2026 I left that career and started building full time, alone, teaching
myself to write software as I went. The first four tools were published six weeks
later, in May and June 2026. Each one took a single operational problem and solved
it properly. They were not impressive. They were correct.

Those four tools converged into one idea: **Helix Codex**, an accountable AI
operating organization. Not an autonomous agent. An organization with a
constitution, named roles with bounded authority, evidence trails, and a human at
every consequential boundary. Helix Prime is its operations core.

This work is maintained by one person, with no team and no funding. It has not been
externally audited and it has not made revenue. Where it is unfinished, the
documents say so.

## Helix Prime is the centre

Helix Prime is the operations core of Helix Codex. It is a local-first platform that
owns the parts that must be governed in one place:

- Identity and authentication, with role-based access control (RBAC) that defaults to deny.
- The Erlang C forecasting core — the same staffing maths the May–June 2026 building attempts first sketched.
- The CRM, the workflow engine, and the event-sourced memory that records what happened and why.
- The fail-closed governance gate that evaluates every submission before execution: cost against the acting role's approval limit, data classification against what the role may read, confidence, and engine ownership. It returns dead-letter, awaiting-approval, or executing — and on a miss it refuses, it does not guess.

Everything else in the portfolio is a satellite of this core. Some are components that supply a capability Helix Codex would use. One is a commercial vertical built on the framework. Four are the building attempts whose thinking was absorbed into Prime itself.

## How the satellites relate to the core

Two distinct relationships are in play, and the difference matters.

**Code relationship.** Every repository in this portfolio is a separate codebase by design. Helix Prime enforces "versioned sibling-service event contracts with no cross-repository imports" — the services talk through published contracts, not shared source. That separation is an architecture decision, not a gap: a tangled monolith would have made the fail-closed boundary harder to prove, not easier. Where a repository depends on the framework, it does so as an external client over those contracts, never by embedding Prime's code.

**Data relationship.** Most of these are not wired to each other yet. Where a data flow is real and shipping, it is named as such below. Where it is a design intent — the shape of a future pipeline — it is labelled "designed to; not yet wired" so a reader does not mistake a plan for a live feed.

| Repository | Role in the story | Code relationship | Data relationship to the core | State |
|---|---|---|---|---|
| [Helix Prime](https://github.com/HatemIsmailShalaby1979/Helix-Prime) | The operations core | — | Owns identity, RBAC, forecasting, CRM, the gate | Pre-pilot, production `NOT_READY` |
| [Helix Education](https://github.com/HatemIsmailShalaby1979/Helix-Education) | Component: learning engine | Independent repo | Designed to supply the learning foundation Helix Codex would use; **not yet wired into the core** | Alpha, 447 tests collected, zero failures |
| [Study Studio](https://github.com/HatemIsmailShalaby1979/Study-Studio) | Component: local-first tutor | Independent repo | No pipeline wired to Prime today | Working, 46 suites / 973 tests |
| [L&D Command Center](https://github.com/HatemIsmailShalaby1979/L-D-Command-Center) | Component: desktop workstation | Independent repo | No data flow wired to Prime today | V1 ship in progress |
| [LIVE Support Assistant](https://github.com/HatemIsmailShalaby1979/LIVE-Support-Assistant) | Component: explainable support | Independent repo, no shared code or runtime with Prime | Its operational signals **could** inform Helix Education's curriculum — designed to consume that feed; **not yet wired** | Prototype, shadow-mode pilot ready |
| [Blue Waves](https://github.com/HatemIsmailShalaby1979/Blue-Waves-) | Vertical: content studio | Built on the Helix Codex framework; consumes Prime as an **external client** over its contracts, never embedded | Live client relationship to Prime (HTTP/contracts) | Pre-revenue, pipeline verified |
| [WFM Forecasting Calculator](https://github.com/HatemIsmailShalaby1979/wfm-forecasting-calculator) | Building attempt | Independent repo | Conceptual only — its Erlang C maths became Prime's WFM engine; no shared code | Sketch, engine self-tests pass |
| [RTA Command Center](https://github.com/HatemIsmailShalaby1979/RTA_command_center) | Building attempt | Independent repo | Conceptual only — its adherence thinking became Prime's RTA engine; no shared code | Sketch, engine restored |
| [CX Sentiment Sentinel](https://github.com/HatemIsmailShalaby1979/cx-sentiment-sentinel) | Building attempt | Independent repo | Conceptual only — its KPI-decay risk scorer became Prime's CX engine; no shared code | Sketch, not runnable as committed |
| [Dynamic Ops Automation Engine](https://github.com/HatemIsmailShalaby1979/Dynamic-Ops-Automation-Engine) | Building attempt | Independent repo | Conceptual only — its tenant model and fail-closed config became Prime's B2B and WFM engines; no shared code | Sketch, no tests |

## How I build

- Local-first development. Cloud only when a customer's value justifies it.
- Governance before autonomy.
- Evidence before claims. Verification requires command output that survives review, not a summary.
- A human at every consequential boundary.
- Memory with provenance, classification, and tenant isolation.
- Improvement through evaluated proposals, never silent self-modification.
- Small, measurable pilots before large infrastructure.

## What I am looking for

Senior AI-engineering, ML-platform, and founder-advisor roles where governed, evidence-gated automation matters, especially in contact-centre operations, workforce management, and learning systems. I value teams that treat honest "not-ready" signals, auditability, and local-first privacy as features rather than blockers.

> [!WARNING]
> **Status — gathered in one place.** None of these has been externally audited or certified. No repository has certified data isolation, a signed security review, or an assigned on-call owner. No revenue has been realised anywhere in the portfolio. Stating this once is the point: a portfolio that hides its unfinished edges is worth less to the person reading it.

| Repository | Status | Snapshot |
|---|---|---|
| Helix Prime | Pre-pilot; 1,897 tests passed / 0 failed; 9 production-only gates red by design | 2026-09-27 |
| Helix Education | Alpha; 447 tests collected, zero failures | 2026-09-27 |
| Study Studio | Working; 46 suites / 973 tests; 85.5% statement coverage | 2026-09-24 |
| L&D Command Center | V1 ship in progress; E2E smoke run was mixed (window launch blocked by a tkinter environment problem; generation exceeded the 60 s budget on that hardware) | 2026-09-23 |
| LIVE Support Assistant | Prototype; on-device gate 10/10 checks; deployed-vs-local parity 39/39 identical margins; a contradictory corpus is refused at publish with HTTP 422; backend suites pass but are not wired to the standalone client | 2026-09-28 |
| Blue Waves | Pre-revenue; 125 tests collected (109 project + 16 vendored); one cockpit E2E test intermittently order-dependent | 2026-09-27 |
| The four 2026 building attempts | Historical project context, not audited evidence; two are not runnable as committed | 2026-06 / 2026-09-27 |

## Author

**Hatem Ismail Shalaby** — Operations Architect · AI Systems Engineer · Founder

- GitHub: [HatemIsmailShalaby1979](https://github.com/HatemIsmailShalaby1979)
- LinkedIn: [hatem-shalaby-202902127](https://www.linkedin.com/in/hatem-shalaby-202902127/)
- Email: hatemshalaby2025@gmail.com
- Education: BSc Managerial Sciences (Computer Section), Sadat Academy for Management Sciences; Business Analytics Nanodegree, Udacity

Based in Al Obour City, Al-Qalyubia Governorate, Egypt.

## Licence

MIT
