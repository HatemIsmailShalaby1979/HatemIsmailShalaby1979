<div align="center">

# Hatem Ismail Shalaby

**Operations Architect · AI Systems Engineer · Founder**

</div>

> [!NOTE]
> Deterministic where a decision has consequences, audited so any action can be replayed, and fail-closed by default. On missing input or missing authority, the system refuses rather than guesses.

## Status at a glance

[![CI](https://github.com/HatemIsmailShalaby1979/Helix-Prime/actions/workflows/ci.yml/badge.svg)](https://github.com/HatemIsmailShalaby1979/Helix-Prime/actions/workflows/ci.yml)

- **Helix Prime, the flagship:** pre-pilot, production **`NOT_READY`**. CI green on all 17 steps; 1,897 tests passed / 0 failed at 86.9% coverage; all six engines drive a real computation end-to-end. Snapshot 2026-09-30.
- **The portfolio:** one person's self-funded work — no revenue, no external audit. Where it is unfinished, the documents say so.
- **Looking for one design partner for a shadow-mode pilot.** The [pilot protocol](https://github.com/HatemIsmailShalaby1979/Helix-Prime/blob/main/docs/release/pilot-protocol.md) defines the boundaries; the [evidence pack](https://github.com/HatemIsmailShalaby1979/Helix-Prime/blob/main/docs/portfolio/00_INDEX.md) shows what exists today.

## A two-minute tour

A narrated two-minute walkthrough of the portfolio — the core, the components, and the evidence standard. If the player does not render, [watch the file directly](assets/portfolio-2min-narrated.mp4).

<video src="assets/portfolio-2min-narrated.mp4" controls muted width="100%"></video>

## The operating rule

I spent twenty-eight years on the operational floor — aviation ground control, telecom
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

The second fourteen were about automation. At ByteDance, Vodafone and Uber I built
AI-driven automation for contact centres — inside other people's stacks: NLP
pipelines that turn unstructured customer language into signal, Erlang C forecasting
that turns volume into staffing, and the reporting layers that made both usable by
people on the floor. I owned the handover in those systems, but the platform, the
codebase and the roadmap were never mine.

In April 2026 I left that career. The switch was not from operations to software — I
had been building inside operational software for fourteen years. It was from
building inside other people's stacks to owning a full system end to end: my own
architecture, my own code, my own consequences. I taught myself the remaining craft
as I built. The first four tools were published six weeks later, in May and June
2026. Each one took a single operational problem and solved it properly. They were
not impressive. They were correct.

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

**Data relationship.** Most of these are not wired to each other yet. Where a data flow is real and shipping, it is named as such in the details below. Where it is a design intent — the shape of a future pipeline — it is labelled "designed to; not yet wired" so a reader does not mistake a plan for a live feed.

## The portfolio

| Repository | Role in the story | State |
|---|---|---|
| [Helix Prime](https://github.com/HatemIsmailShalaby1979/Helix-Prime) | The operations core | Pre-pilot, production `NOT_READY` |
| [Helix Education](https://github.com/HatemIsmailShalaby1979/Helix-Education) | Component: learning engine | Alpha, 447 tests collected, zero failures |
| [Study Studio](https://github.com/HatemIsmailShalaby1979/Study-Studio) | Component: local-first tutor | Working, 46 suites / 973 tests |
| [L&D Command Center](https://github.com/HatemIsmailShalaby1979/L-D-Command-Center) | Component: desktop workstation | V1 ship in progress |
| [LIVE Support Assistant](https://github.com/HatemIsmailShalaby1979/LIVE-Support-Assistant) | Component: explainable support | Prototype, shadow-mode pilot ready |
| [Blue Waves](https://github.com/HatemIsmailShalaby1979/Blue-Waves-) | Vertical: content studio | Pre-revenue, pipeline verified |
| The four 2026 building attempts | History — thinking absorbed into Prime | Historical context; two not runnable as committed |

### Details

**[Helix Prime](https://github.com/HatemIsmailShalaby1979/Helix-Prime)** — the operations core. Owns identity and RBAC, the Erlang C forecasting core, the CRM, the workflow engine, the event-sourced memory, and the fail-closed governance gate. Pre-pilot; CI green on all 17 steps; 1,897 tests passed / 0 failed at 86.9% coverage; all six engines drive a real computation end-to-end; 9 production-only gates red by design; release `v1.1.0`. Snapshot 2026-09-30.

**[Helix Education](https://github.com/HatemIsmailShalaby1979/Helix-Education)** — component: learning engine. Independent repo. Designed to supply the learning foundation Helix Codex would use; **not yet wired into the core**. Alpha; 447 tests collected, zero failures. Snapshot 2026-09-27.

**[Study Studio](https://github.com/HatemIsmailShalaby1979/Study-Studio)** — component: local-first tutor. Independent repo. No pipeline wired to Prime today. Working; 46 suites / 973 tests; 85.5% statement coverage. Snapshot 2026-09-24.

**[L&D Command Center](https://github.com/HatemIsmailShalaby1979/L-D-Command-Center)** — component: desktop workstation. Independent repo. No data flow wired to Prime today. V1 ship in progress; the E2E smoke run was mixed (window launch blocked by a tkinter environment problem; generation exceeded the 60 s budget on that hardware). Snapshot 2026-09-23.

**[LIVE Support Assistant](https://github.com/HatemIsmailShalaby1979/LIVE-Support-Assistant)** — component: explainable support. Independent repo, no shared code or runtime with Prime. Its operational signals could inform Helix Education's curriculum — designed to consume that feed; **not yet wired**. Prototype; on-device gate 10/10 checks; deployed-vs-local parity 39/39 identical margins; a contradictory corpus is refused at publish with HTTP 422; backend suites pass but are not wired to the standalone client. Snapshot 2026-09-28.

**[Blue Waves](https://github.com/HatemIsmailShalaby1979/Blue-Waves-)** — vertical: content studio. Built on the Helix Codex framework; consumes Prime as an **external client** over its contracts, never embedded. Live client relationship to Prime (HTTP/contracts). Pre-revenue; 125 tests collected (109 project + 16 vendored); one cockpit E2E test intermittently order-dependent. Snapshot 2026-09-27.

**The four 2026 building attempts** — [WFM Forecasting Calculator](https://github.com/HatemIsmailShalaby1979/wfm-forecasting-calculator), [RTA Command Center](https://github.com/HatemIsmailShalaby1979/RTA_command_center), [CX Sentiment Sentinel](https://github.com/HatemIsmailShalaby1979/cx-sentiment-sentinel), [Dynamic Ops Automation Engine](https://github.com/HatemIsmailShalaby1979/Dynamic-Ops-Automation-Engine). Historical project context, not audited evidence; two are not runnable as committed. Their Erlang C maths, adherence thinking, KPI-decay risk scoring, and tenant/fail-closed configuration became Prime's WFM, RTA, CX, and B2B engines respectively — conceptual lineage, no shared code. Snapshot 2026-06 / 2026-09-27.

## How I build

- Local-first development. Cloud only when a customer's value justifies it.
- Governance before autonomy.
- Evidence before claims. Verification requires command output that survives review, not a summary.
- A human at every consequential boundary.
- Memory with provenance, classification, and tenant isolation.
- Improvement through evaluated proposals, never silent self-modification.
- Small, measurable pilots before large infrastructure.

## What I am looking for

**Looking for one design partner for a shadow-mode pilot.** If you run a contact
centre, an academy, or any operation where an AI-assisted decision has
consequences, I will deploy a governed pilot in shadow mode: the system proposes,
your people approve, every action is replayable. The [pilot
protocol](https://github.com/HatemIsmailShalaby1979/Helix-Prime/blob/main/docs/release/pilot-protocol.md)
defines the boundaries; the [evidence
pack](https://github.com/HatemIsmailShalaby1979/Helix-Prime/blob/main/docs/portfolio/00_INDEX.md)
shows what exists today.

Beyond the pilot: solutions and systems architect, AI-governance, and
ops-automation lead roles in contact-centre operations, workforce management, and
learning systems — remote or freelance. I value teams that treat honest "not-ready"
signals, auditability, and local-first privacy as features rather than blockers.

## Author

**Hatem Ismail Shalaby** — Operations Architect · AI Systems Engineer · Founder

- GitHub: [HatemIsmailShalaby1979](https://github.com/HatemIsmailShalaby1979)
- LinkedIn: [hatem-shalaby-202902127](https://www.linkedin.com/in/hatem-shalaby-202902127/)
- Email: hatemshalaby2025@gmail.com
- Education: BSc Managerial Sciences (Computer Section), Sadat Academy for Management Sciences; Business Analytics Nanodegree, Udacity

Based in Al Obour City, Al-Qalyubia Governorate, Egypt.

## Licence

MIT
