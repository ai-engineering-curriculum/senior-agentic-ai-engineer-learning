# Job Requirements — Senior Agentic AI Engineer

**Role level:** 40 (lead / staff *build* rung — one altitude below `agentic-systems-architect`)
**Track:** `senior-agentic-ai-engineer-learning`
**Research window:** 2026-08-05 → 2026-11-03 (last 90 days)
**Today:** 2026-11-03
**Prior refresh:** 2026-10-07 (30 postings, proposed 0 modules / 0 exercises / 0 projects — see "Previously-proposed items" below)

This file maps verbatim requirements from current L40-altitude agent-engineering job postings to the existing curriculum. Raw normalized data lives in [`.aicg/job-requirements.json`](.aicg/job-requirements.json); the strictly-additive proposal lives in [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).

## Summary

- Postings sampled: **30** (observed 2026-11-03, all in the 2026-08-05 → 2026-11-03 window; cap of 2 postings per employer applied). 27 are new to this cycle; 3 carry over from 2026-10 as still-active anchor roles (Honeycomb, Harvey Secure Execution, Glean) re-observed 2026-11-03.
- Equivalent titles counted per research packet: `Senior Agentic AI Engineer`, `Staff Agentic AI Engineer`, `Senior AI Agent Engineer`, `Lead Applied AI Engineer`, `Agentic Platform Engineer` — plus close matches at senior/staff altitude (`Senior Staff SWE, Agentic Applications`, `Senior Staff SWE, AI Agent Platform`, `Senior Staff SWE, Agentic IT Operations`, `Senior Staff SWE, Agentic AI Harness & Quality`, `Senior SWE, Agent Eval Platform`, `Senior Staff Engineer, Agentic Identity`, `Lead Applied AI Engineer`, `Staff SWE, Agent Evaluation`, `Staff SWE, AI Developer Platform`, `Senior Staff ML Engineer, Agentic AI Platform`, `SWE/Senior SWE, AI Platform (Agent Runtime)`, `Senior Staff SWE, AI`, `Senior Staff AI Engineer, Agentic AI Platform`, `SWE, AI Agents`, `Senior SWE, AI Agent Memory Infrastructure`, `Senior Staff Engineer, Agentic Databases`, `Senior/Staff SWE, Experience`, `SWE (Agent Platform)`, `SWE, Connectors & MCP`, `Distributed Systems Engineer`, `Staff SWE (Orders Platform)`, `Senior Staff SWE, Agent & Partner Experiences`, `Senior SWE, Operational AI`, `Member of Technical Staff (Agents)`, `Product Engineer, Computer Use`, `Staff SWE, Secure Execution`, `SWE, Evals`, `Senior SWE II — Agentic Intelligence`).
- **Proposed delta this cycle: 0 modules, 0 exercises, 0 projects.** No theme crossed the continuity-bias threshold that is not already covered by `mod-401..405` or by a lower-level track linked as prerequisite. Load-bearing themes this cycle (≥ 30%): orchestration (53%), eval infrastructure (43%), observability (37%), reliability (63%), technical leadership (53%), architecture ownership (60%), paved roads (73%), enterprise integration (37%), code-review standards (30% — newly at threshold, already covered by `mod-405/exercise-01`), MCP-at-fleet-scale (30% — at threshold, 2026-09 pending proposal still appropriate). Theme-14 landed at exactly 30% this cycle — at threshold but not clearly above; see "Previously-proposed items" below for how this interacts with the 2026-09 pending proposal.
- The two themes that crossed threshold in the 2026-09 packet and seeded pending exercise proposals continue to not re-trigger on frequency grounds this cycle: `theme-14` MCP-servers-at-fleet-scale is at exact threshold (30% this cycle; 27% last cycle; 35% peak); `theme-15` agent-runtime-sandboxing bounced from 13% → 23% but remains below 30%. Both pending exercise proposals remain in git history on the 2026-09 `.aicg/curriculum-plan-delta.json` artifact awaiting human review.
- **New theme this cycle:** *browser-use / computer-use at production altitude* (`theme-22`, 10%, 3 postings — Browserbase, Perplexity, Anthropic Computer Use). Below elevation floor; watch next cycle.
- **Trending-up sub-threshold signal:** *agent memory as a distinct platform surface* (`theme-21`) climbed from 17% → 27% in one cycle on the strength of ByteDance's dedicated memory-infra role, Teradata's Agent Memory service, Cloudflare's Durable Objects memory primitives, Pinecone's agent-experience redesign, and sustained Databricks / Appian / NVIDIA / SvcNow coverage. Most-credible candidate to cross threshold next cycle.

## Methodology

- **Sources:** `job-boards.greenhouse.io` (bulk), `jobs.lever.co`, `jobs.ashbyhq.com`, `jobs.smartrecruiters.com`, `careers.servicenow.com`, `careers.appian.com`, `jobs.nvidia.com` (JSON only; mirrors used for content), `workday.wd5.myworkdayjobs.com`, direct careers pages (`careers.teradata.com`, `careers.appian.com`, `www.capitalonecareers.com`, `www.brex.com`, `www.arcade.dev`), mirror sites (`zapply.jobs`, `freehire.me`, `somacap.com`, `sapphireventures.com`, `mavenventures.com`, `menlovc.com`, `designerfund.com`, `upfront.com`, `jobs.accel.com`, `builtinsf.com`, `builtinnyc.com`, `remotech.ai`, `www.welcometothejungle.com`, `aijobs.com`) when the primary host 403s or returns JSON only.
- **Per-posting capture:** employer, title, URL, `date_observed`, `date_posted` (explicit when visible — Databricks 2026-11-02, NVIDIA Agent Platform 2026-10-16, NVIDIA Agentic IT Ops 2026-10-30, SvcNow Moveworks Harness 2026-10-09, Cisco 2026-10-30, Appian 2026-10-30, LinkedIn 2026-09-01, Uber 2026-10-22, Workday 2026-10-23, Rippling 2026-10-13, Capital One 2026-09-27, Cloudflare 2026-10-26, ByteDance 2026-10-17, Browserbase 2026-10-19, Brex 2026-10-01, Basis 2026-10-15, Perplexity 2026-08-27, Harvey 2026-09-30; else `estimated:YYYY-MM` from "posted N days/weeks ago" or active-rotation signals), location, 3–6 verbatim/near-verbatim requirement quotes prioritized on L40-distinguishing altitude (ownership, standards, mentoring, infrastructure, SLOs, incidents, cost/latency at scale, code-review leadership, paved roads, MCP catalogs, sandbox platforms, agent memory, browser-use harnesses).
- **Frequency** = distinct in-window postings citing the theme ÷ 30 in-window postings.
- **Threshold for a new curriculum item:** ≥ 3 postings AND ≥ 30% frequency AND no existing module/exercise can be incrementally extended to cover it.
- **Continuity bias applied strictly:** for every above-threshold theme, checked (a) existing L40 coverage first, (b) whether the theme belongs at a lower level per the ownership rule.
- **Sample-composition caveat:** the 2026-11 sample tilts materially platform/infra-heavy (20 of 30 postings describe building a shared agent platform/runtime for other teams) compared to 2026-10's more generalist Applied-AI mix. The large frequency swings in theme-04 (frameworks, -36 pp), theme-13 (RAG, -50 pp), theme-07 (cost/latency, -7 pp), theme-09 (architecture-ownership, +33 pp), theme-11 (paved roads, +33 pp), and theme-08 (leadership, +16 pp) are sample-composition artifacts, not market shifts. The right read: "load-bearing themes are universally still present at ≥ 30%; what has shifted is which lens the market frames them through."

## Ownership rule applied

Where a requirement is genuinely needed at multiple levels, primary ownership sits with the **lowest-level role where it is required**. This L40 track links to the L30 `agentic-ai-engineer` track for build fundamentals and to the L48 `agentic-systems-architect` track for architectural depth, rather than re-teaching either.

## Requirement themes → curriculum ownership

**Bold frequencies** are ≥ 30% (load-bearing under continuity bias). Δ shows change vs 2026-10-07.

| # | Theme | Freq | Δ | Owner role | Coverage |
|---|---|---|---|---|---|
| 1 | Multi-agent orchestration *in production* (topologies under load, handoffs at scale, sub-agent boundaries defended by SLAs) | **53%** | -14 | `senior-agentic-ai-engineer` | [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) |
| 2 | Building evaluation infrastructure (harnesses, LLM-judge rubrics, CI-integrated eval gates) | **43%** | -24 | `senior-agentic-ai-engineer` | [`mod-402/exercise-01-reusable-eval-harness`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md), [`exercise-03-regression-gates`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md) |
| 3 | Observability & tracing infrastructure for agent *fleets* (trajectory visibility, OTel GenAI, quality/drift dashboards) | **37%** | -23 | `senior-agentic-ai-engineer` | [`mod-402/exercise-02-tracing-and-dashboards`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md) |
| 4 | Agent framework fluency (LangGraph, LangChain, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK, LlamaIndex, Semantic Kernel, Strands) | 17% | -36 | `agentic-ai-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks). Sample-composition drop; theme is still a prerequisite. |
| 5 | Reliability for agent systems in production ("holds up under load", state machines with recovery) | **63%** | 0 | `senior-agentic-ai-engineer` | [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) + [`mod-403/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) |
| 6 | Guardrails, prompt-injection defense, agent sandboxing (JD-level, broad) | 27% | -3 | `agentic-ai-engineer` (L30) basics → `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture at L48 [`mod-306`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security). L40 production-hardening lens: [`mod-403/04-hardening-communication`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md) |
| 7 | Cost / latency / token budgets defended with numbers (caching, routing, context-window pruning) | 23% | -7 | `senior-agentic-ai-engineer` | [`mod-403/02-token-and-latency-budgets`](lessons/mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md) + [`exercise-03`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-03-token-and-latency-budgets.md); [`mod-404/02-cost-controls-and-budgets`](lessons/mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md) |
| 8 | Technical leadership: mentoring, setting engineering standards, design/code review at senior-plus altitude | **53%** | +16 | `senior-agentic-ai-engineer` | [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership) |
| 9 | Architecture ownership, build-vs-buy at subsystem level, prototype → production refactoring | **60%** | +33 | `senior-agentic-ai-engineer` | [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) — whole module. [`04-build-vs-buy-and-complexity`](lessons/mod-401-agent-systems-in-practice/04-build-vs-buy-and-complexity.md) + [`exercise-03-prototype-to-production-refactor`](lessons/mod-401-agent-systems-in-practice/exercises/exercise-03-prototype-to-production-refactor.md) |
| 10 | Human-in-the-loop / approval boundaries | 0% | -13 | `agentic-ai-engineer` (L30) basics | Prerequisite: [`agentic-ai-engineer-learning/mod-206/exercises/exercise-04-human-approval-checkpoints`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). L40 hardening lens implicit in [`mod-403/04-hardening-communication`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md) and [`mod-405/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md). |
| 11 | Paved roads / shared services / platform templates for internal agent teams | **73%** | +33 | `senior-agentic-ai-engineer` | [`mod-405/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md), [`mod-402/04-paved-road-adoption`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md) |
| 12 | Enterprise integration & secure tool auth (OAuth 2.0 / 2.1, RBAC, MCP-servers to internal systems, A2A protocols) | **37%** | +7 | `agentic-ai-engineer` (L30) primary; `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture: [`agentic-systems-architect-learning/mod-306/04-oauth-rbac-tokens`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md) |
| 13 | RAG pipelines, retrieval quality, embedding/rerank strategy | 0% | -50 | `agentic-ai-engineer` (L30) / `rag-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory); depth in [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning). Sample-composition drop — platform/infra postings don't re-list RAG mechanics. |
| 14 | MCP servers at *fleet scale* (multi-team, auth-wrapped, versioned catalogs — distinct from single-client authoring) | **30%** | +3 | at-threshold this cycle (prior-cycle proposal pending) | **Pending from 2026-09:** proposed `mod-405 exercise-04-mcp-catalog-paved-road` sits on the 2026-09 `.aicg/curriculum-plan-delta.json` artifact in git history. Not re-triggered on frequency grounds this cycle (30% is exactly at threshold, not clearly above). Single-server MCP authoring remains at L30 [`mod-202-frameworks/exercises/exercise-04-mcp-tool-server`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks). See "Previously-proposed items" below. |
| 15 | Agent-specific code review, standards, "set the bar" for agentic-system quality | **30%** | +10 | `senior-agentic-ai-engineer` | [`mod-405/exercise-01-agent-code-review-standards`](lessons/mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md) — already covers this; no new delta |
| 16 | Agent memory as a distinct platform surface (semantic/episodic/working-memory stores, memory-as-service, "multi-tier memory networks") | 27% | +10 | sub-threshold trending up | See "Trending-up signal" below. Natural home if it crosses 30%: a chapter extension in [`mod-403`](lessons/mod-403-multi-agent-at-scale) or an observability extension in [`mod-402`](lessons/mod-402-eval-observability-infra) for memory-quality drift. |
| 17 | Agent-runtime sandboxing / secure code execution (Firecracker, gVisor, E2B, Modal, Cloudflare Durable Objects, Daytona, WebAssembly, microVMs, K8s multi-tenant isolation) | 23% | +10 | sub-threshold this cycle (prior-cycle proposal pending) | **Pending from 2026-09:** proposed `mod-403 exercise-04-secure-agent-code-runtime` sits on the 2026-09 `.aicg/curriculum-plan-delta.json` artifact in git history. Not re-triggered on frequency grounds this cycle (23% < 30%). Signal recovering half of the 2026-10 drop; dedicated Workday Agent Runtime role is new this cycle. See "Previously-proposed items" below. |
| 18 | AI-native dev tools (Cursor / Claude Code / Codex / Gemini CLI / OpenCode) as core work-style instrument | 10% | -3 | sub-threshold not curriculum-worthy | Not an agent-build skill; a work-style expectation. Uber AIFX makes it a role requirement; still below the 40% elevation threshold to add to [`PREREQUISITES.md`](PREREQUISITES.md). |
| 19 | Incident response for agent failures (runbooks, on-call, RCA, drift-triggered alerts) | 10% | 0 | `senior-agentic-ai-engineer` | [`mod-404/03-incident-response-for-agents`](lessons/mod-404-reliability-cost-incident/03-incident-response-for-agents.md), [`exercise-03`](lessons/mod-404-reliability-cost-incident/exercises/exercise-03-agent-incident-response.md), [`04-postmortems-and-durable-fixes`](lessons/mod-404-reliability-cost-incident/04-postmortems-and-durable-fixes.md) |
| 20 | Regulated / compliance-heavy domain integration (fintech, health, HCM, gov, marketing) | 17% | -6 | `agentic-systems-architect` (L48) architectural depth | Architectural coverage at L48 [`mod-309-governance-compliance-domain-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-309-governance-compliance-domain-architecture). L40 build-lens surfaces this in [`mod-404/01-slos-and-slis-for-agents`](lessons/mod-404-reliability-cost-incident/01-slos-and-slis-for-agents.md). |
| 21 | Durable execution / state machines (pause/resume, versioned trajectories, Temporal, Cloudflare Durable Objects) | 13% | +6 | `senior-agentic-ai-engineer` | [`mod-403/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md), [`exercise-02-durable-execution-in-production`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-02-durable-execution-in-production.md) |
| 22 | Browser-use / computer-use at production altitude (headless-browser harnesses, Anthropic Computer Use, Playwright-based agent runtimes, hosted services like Browserbase/Anchor Browser/Steel Browser) | 10% | *new* | new emerging sub-threshold | See "New emerging signal" below. Natural home if it crosses 30%: a chapter extension in [`mod-403`](lessons/mod-403-multi-agent-at-scale) on browser-use-as-tool-seam-hardening or an exercise extension in [`mod-401`](lessons/mod-401-agent-systems-in-practice) on build-vs-buy between hosted browser services and in-house Playwright harnesses. |

## Posting evidence for load-bearing themes

The tables below list postings anchoring each ≥ 30% theme. All 30 sampled postings were observed 2026-11-03 within 2026-08-05 → 2026-11-03.

### Theme 1 — Multi-agent orchestration *in production* (53%)

Anchored by Databricks (orchestration/memory/retrieval/tool-use/multi-agent coordination as design patterns), NVIDIA Agentic IT Ops (multi-step enterprise workflows end-to-end), SvcNow Moveworks Harness (agent orchestration + sandboxed code execution + agent memory + execution environment simulation), SvcNow Agent Eval Platform (multi-turn agent scenarios end-to-end), Appian (reliable agents and orchestration — planning/tool-use/memory/state), Uber AIFX (durable multi-day agent workflows orchestrate planning/coding/review/verification), Reddit (agentic workflows that help teams design/train/evaluate), Capital One (agents and multi-agent workflows at enterprise scale), Cloudflare (distributed AI workflows), Pinecone (orchestration + agent-to-agent communication patterns), Writer (tool orchestration + MCP clients/servers), Instacart (orchestration layer for commerce + agentic commerce workflows), Brex (orchestrating model calls in business-critical flows), Basis (agent orchestration + MCP + A2A), Perplexity (agent harnesses connecting models with environments and tools), Anthropic Computer Use (agent loops + tool integrations), Honeycomb (multiple agents collaborating on one shared Canvas investigation).

Representative quotes:
- *"Durable, multi-day agent workflows orchestrate planning, coding, review, and verification."* — Uber AIFX
- *"Agent orchestration, sandboxed file systems and code execution, latency optimization, agent memory, LLM self-reflection and improvement, execution environment simulation."* — ServiceNow (Moveworks)
- *"Design reliable agents and orchestration — planning, tool use, memory, and state — with safe, permission-aware boundaries."* — Appian
- *"The runtime that executes multi-turn agent scenarios end-to-end — stand up the environment and user simulator."* — ServiceNow Agent Eval Platform

→ Covered by [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) — orchestration under load, token/latency budgets, durable execution, and hardening inter-agent communication and tool seams. Architecture-level topology *design* stays with L48 [`mod-302`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-302-multi-agent-orchestration).

### Theme 2 — Building evaluation infrastructure (43%)

Anchored by Databricks (own the eval and quality system — LLM-as-judge + human-labeled benchmarks), NVIDIA Agentic IT Ops (define engineering standards for how agentic systems are built/tested/evaluated), SvcNow Moveworks Harness (LLM and agent evaluation fundamentals for action trajectories), SvcNow Agent Eval Platform (whole role — consolidating evals into a single orchestration service, span data model for agent trajectories, foundation for using eval signal to optimize the agent), LinkedIn (whole role — Evaluation Operating System for all AI agents, evaluator models including LLM-as-judge and reward models), Reddit (evaluation harnesses measuring correctness + reproducibility + regressions + cost + latency), Rippling (eval frameworks + harness engineering as explicit charter), Cloudflare (create evals, guardrails, and audits — measure, tune, re-ship fast), Basis (evaluation + observability for agents), Perplexity (AI evaluation + testing + maintenance), Harvey (adversarial tests + evaluations + telemetry that verify containment), Glean (whole Evals team — large-scale evaluation pipelines + agent observability + evaluating frontier model releases), Honeycomb (evals that tell you whether they got better).

Representative quotes:
- *"The Evals & Observability team owns the measurement and quality layer that makes Glean's Assistant and Agents reliably better."* — Glean
- *"Building the Evaluation Operating System (EOS), a foundational Agent Evaluation platform."* — LinkedIn
- *"Consolidating evals that run today as one-off workflows onto a single orchestration service — one source of truth. Getting to self-serve, so any team runs an eval without bespoke integration."* — ServiceNow Agent Eval Platform
- *"Design evaluation harnesses that measure both model outcomes and agent/workflow quality, including correctness, reproducibility, regressions, cost, and latency."* — Reddit

→ Covered by [`mod-402-eval-observability-infra`](lessons/mod-402-eval-observability-infra), especially [`exercise-01-reusable-eval-harness`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md) and [`exercise-03-regression-gates`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md). Architecture-level eval strategy sits at L48 [`mod-304-evaluation-harnesses`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-304-evaluation-harnesses).

### Theme 3 — Observability & tracing infrastructure for agent fleets (37%)

Anchored by NVIDIA Agent Platform (OTEL instrumentation), SvcNow Agent Eval Platform (span data model for agent trajectories — prompts, tool calls, plan updates, outcomes), LinkedIn (tracing infrastructure for all LinkedIn AI Agents + real-time observability for regressions/drift), Workday Agent Runtime (deep observability into runtime behavior, policy decisions, audit traces), Cloudflare (observability for distributed AI workflows + structured logging + end-to-end tracing), Brex (observability of business-critical flows), Aledade (metrics + distributed tracing + logging + alerting + SLOs + dashboards + failure handling), Basis (observability for agents), Harvey (telemetry that verifies containment), Glean (trace enrichment + durable telemetry pipelines + dashboards), Honeycomb (high cardinality data makes agents different).

Representative quotes:
- *"Build deep observability into runtime behavior, policy decisions, and audit traces."* — Workday Agent Runtime
- *"Build agent observability infrastructure, including trace enrichment, durable telemetry pipelines, dashboards, and debugging."* — Glean
- *"The span data model for agent trajectories — prompts, tool calls, plan updates, outcomes — so a trajectory is queryable."* — ServiceNow Agent Eval Platform

→ Covered by [`mod-402-eval-observability-infra/exercise-02-tracing-and-dashboards`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md); OTel GenAI semantic conventions covered in the accompanying chapter. Deeper stable-trace-identity work sits at L48 [`mod-305-observability-tracing`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-305-observability-tracing).

### Theme 5 — Reliability for agent systems in production (63%)

Anchored by SvcNow Moveworks Harness (reliably at scale), SvcNow Agent Eval Platform (reliability floor + SLO for the harness itself), Appian (engineer reliability + latency + efficiency at enterprise scale + retries + idempotency + partial failure + long-running tasks + recovery), LinkedIn (feedback loops that detect regressions, model drift), Reddit (reliable loops for data/label analysis + correctness/reproducibility), Workday Agent Runtime (secure execution platform for enterprise AI agents), Capital One (production AI systems with reliability and scale), Cloudflare (production systems — end-to-end ownership including on call), ByteDance (large-scale, low-latency, and highly reliable memory infrastructure), Teradata (OLTP reliability + agentic capabilities), Instacart (durable platform capabilities + stronger failure isolation + consistency models), Brex (reliability + security + observability in business-critical flows), Aledade (production systems + SLOs + failure handling), Basis (production-grade agentic systems), Perplexity (product reliability), Anthropic (reliability and robustness issues in computer-use agent harness), Harvey (operate a platform for security agents), Glean (reliably better), Honeycomb (production-grade agents trustworthy mid-incident).

Representative quotes:
- *"Runtime substrate that enforces policy by architecture, not by prompt, with deterministic controls."* — Workday Agent Runtime
- *"Strong distributed-systems background, including retries, idempotency, partial failure, long-running tasks, and recovery."* — Appian
- *"Large-scale, low-latency, and highly reliable memory infrastructure."* — ByteDance

→ Covered by [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) (SLOs/SLIs for agents, quality drift, cost controls, incident response, postmortems) and [`mod-403-multi-agent-at-scale/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) (durable execution and resumption for long-running agent workloads).

### Theme 8 — Technical leadership (53%)

Anchored by Databricks (mentor senior and mid-level engineers; raise the engineering bar; lead architecture reviews), NVIDIA Agentic IT Ops (mentor and grow senior and staff engineers through design partnership, code review, and technical coaching), Appian (coach and guide junior engineers), LinkedIn (foundational platform ownership), Uber (set the standards other teams build on), Reddit (set technical direction across teams, mentor engineers, raise the bar for modeling rigor and AI-assisted engineering), Rippling (mentor Staff, Senior, SE II engineers while raising engineering standards), Capital One (mentor senior technical leaders — multi-year platform initiatives), Teradata (mentor engineers on Postgres internals + distributed systems + agentic workload patterns), Writer (set technical direction for identity + auth + trust boundaries), Gusto (Senior Staff — bridge between API and AI world), Brex (mentor engineers through design reviews, code reviews, pairing), Basis (own the team's technical quality bar through design and code reviews + mentor), Aledade (set and uphold the standard for engineering processes + mentor and coach engineers), Harvey (set the technical direction for secure agent execution), Honeycomb (set the bar).

Representative quotes:
- *"Set the standards other teams build on."* — Uber AIFX
- *"Mentor and grow senior and staff engineers through design partnership, code review, and technical coaching."* — NVIDIA Agentic IT Ops
- *"Own the team's technical quality bar through design and code reviews. Onboard new engineers, mentor senior and mid-level engineers."* — Basis
- *"Set and uphold the standard for engineering processes to support high-quality engineering."* — Aledade

→ Covered end-to-end by [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership): agent code review with safety focus, paved roads & standards, design-to-execution translation, scoping & sequencing.

### Theme 9 — Architecture ownership, build-vs-buy, prototype → production (60%)

Anchored by Databricks (define and lead the target technical architecture + lead architecture reviews), NVIDIA Agent Platform (architect multi-tenant Kubernetes execution environments), NVIDIA Agentic IT Operations (own the technical strategy and reference architecture for agentic AI across enterprise IT), Cisco (align identity architecture across cloud/on-prem/hybrid), Appian (architect, build, and optimize production AI systems), LinkedIn (architect scalable data pipelines and platforms), Workday Agent Runtime (runtime substrate design), Capital One (define and steer the technical AI architecture vision), Teradata (full technical ownership of an Agent Service — design the data model, define the API surface, implement the core logic), Pinecone (redesigning product for agent-first use), Writer (platform design, backend service design, trust-boundary architecture), Arcade (runtime and registry for AI/LLM tools), Instacart (architect and evolve event-driven idempotent workflows), Brex (own the technical direction and roadmap of Agents Platform), Aledade (evaluate architectural tradeoffs across reliability/performance/security/cost/scalability/developer-experience), Basis (own the major design decisions), Harvey (design, build, and operate a platform for security agents).

Representative quotes:
- *"Own the technical strategy and reference architecture for agentic AI across enterprise IT; establish them as the standard that partner engineering organizations build on."* — NVIDIA Agentic IT Ops
- *"Full technical ownership of an Agent Service: design the data model, define the API surface, implement the core logic."* — Teradata
- *"Own broad AI Platform charters across multiple systems and teams."* — Rippling

→ Covered by [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) — whole module, especially [`04-build-vs-buy-and-complexity`](lessons/mod-401-agent-systems-in-practice/04-build-vs-buy-and-complexity.md) + [`exercise-03-prototype-to-production-refactor`](lessons/mod-401-agent-systems-in-practice/exercises/exercise-03-prototype-to-production-refactor.md).

### Theme 11 — Paved roads / shared services / platform templates (73%)

Anchored by NVIDIA Agent Platform (reusable pipeline templates + deployment blueprints that standardize how agents are built), NVIDIA Agentic IT Ops (establish the standard that partner engineering organizations build on), SvcNow Agent Eval Platform (self-serve — any team runs an eval without bespoke integration), Cisco (reusable APIs/SDKs/CLI tools/integration patterns), LinkedIn (foundational Agent Evaluation platform), Uber AIFX (single way for engineers to install, configure, and run AI coding agents with consistent settings), Reddit (patterns that other teams build on), Workday Agent Runtime (platform for enterprise AI agents), Rippling (platform primitives that can be reused by product teams), ByteDance (unified platform for memory), Teradata (agentic data layer in a single platform), Pinecone (first-class users alongside humans — redesigning the product), Browserbase (Agent Platform framework with developer-first APIs), Writer (AI integration platforms), Arcade (runtime and registry for AI/LLM tools), Instacart (durable platform capabilities that other product teams can build on), Gusto (platform that allows developers to embed payroll into their own software), Brex (built shared infrastructure, developer tooling, or paved roads), Harvey (reusable controls for agent tool use + code execution + network/filesystem access + resource consumption + workload lifecycle), Glean (measurement and quality layer).

Representative quotes:
- *"Develop and maintain automated CI/CD pipelines using GitLab CI and ArgoCD, including reusable pipeline templates and deployment blueprints that standardize how agents are built."* — NVIDIA Agent Platform
- *"A single way for engineers to install, configure, and run AI coding agents...with consistent settings."* — Uber AIFX
- *"Define technical patterns and platform primitives that can be reused by product teams across Rippling."* — Rippling

→ Covered by [`mod-405-technical-leadership/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md) and [`mod-402-eval-observability-infra/04-paved-road-adoption`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md).

### Theme 12 — Enterprise integration & secure tool auth (37%)

Anchored by Cisco Agentic Identity (whole role on identity + token exchange + credential brokering + workload identity for agents, including A2A), Appian (permission-aware boundaries at enterprise scale), Workday Agent Runtime (policy enforcement for data/context/tool/model boundaries), Teradata (enterprise-governed data), Writer (OAuth, API key, service-to-service for AI integrations), Arcade (governed access with the MCP authorization spec), Instacart (secure APIs), Gusto (API contracts for agent-facing tools + MCP), Basis (A2A integrations + MCP), Harvey (identity and secrets platforms).

Representative quotes:
- *"Design and implement scalable identity and access management frameworks for AI agents, including token exchange, credential brokering, workload identity."* — Cisco Agentic Identity
- *"Set technical direction for identity, auth, and trust boundaries across integrations (OAuth, API key, service-to-service)."* — Writer
- *"Every enterprise agent needs governed access to the systems it acts in. That's the layer we're building."* — Arcade

→ Basics (OAuth 2.0 / 2.1 / RBAC for agent toolchains) owned at L30 by [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture-level at L48 [`mod-306/04-oauth-rbac-tokens`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md). Theme-14 (MCP-at-fleet-scale) is the closely-related sub-signal at exactly 30% this cycle.

### Theme 14 — MCP servers at fleet scale (30%) — exactly at threshold, prior proposal pending

Anchored by Databricks (MCP-style interfaces for governed agent access to pricing/billing/order data), NVIDIA Agent Platform (MCP as a required protocol), Uber AIFX (MCP alongside Claude Agent SDK, Codex, OpenCode in a shared coding-agent platform), Cloudflare (Agent SDK + MCP for tool wiring), Pinecone (MCP + A2A redesign of experience), Writer (whole role on MCP clients/servers + external connectors + auth mediation), Arcade (whole-company MCP runtime + registry + helped write the MCP authorization spec), Gusto (MCP servers + tool/function definitions as part of Agent & Partner Experiences), Basis (MCP servers + A2A integrations).

Representative quotes:
- *"Arcade is the MCP runtime that gives agents the power to do both seamlessly. We connect agents to the systems they act in, then give each one a permission slip and a paper trail."* — Arcade
- *"Practical expertise building AI integration layers (e.g., MCP clients/servers, tool orchestration, external API connectors, auth mediation)."* — Writer
- *"Architect tool-calling and MCP-style interfaces that give agents governed, run-time access to pricing, product catalog, order, contract, subscription and billing data."* — Databricks

Theme-14 landed at exactly 30% this cycle (9/30), up 1 posting absolute from 2026-10 (8/30) and down 1 posting from the 2026-09 peak (9/26 = 35%). Signal is clearly stable at ~1-in-3 postings across three cycles with 26 distinct postings in aggregate; dedicated MCP-platform roles (Writer, Arcade, plus Sumo Logic's "Core AI Platform (MCP & Agent Infrastructure)" role observed just outside this cycle's freshness window) have proliferated. 2026-09 pending proposal (`mod-405 exercise-04-mcp-catalog-paved-road`) is NOT re-triggered on frequency grounds this cycle because 30% is exactly at threshold, not clearly above, and the 2026-10 cycle made the deliberate call not to re-trigger at 27%. The aggregated 3-cycle evidence strongly supports a human-review merge; see "Previously-proposed items" below.

### Theme 15 — Agent code review, engineering standards, "set the bar" (30%)

Theme-15 crossed the 30% threshold this cycle (9/30), up 10 pp from 20% in 2026-10. Platform-heavy sample makes "define engineering standards for how agentic systems are built, tested, evaluated, and operated" (NVIDIA Agentic IT Ops) a frequently-named deliverable at Staff+ altitude. Fresh anchors: Databricks (lead architecture reviews, establish design patterns for agents), NVIDIA Agentic IT Ops (define engineering standards + mentor through code review), Uber AIFX (set the standards other teams build on), Rippling (review critical code paths, raise engineering standards), Brex (design reviews, code reviews, pairing), Aledade (set and uphold the standard for engineering processes), Basis (own the team's technical quality bar through design and code reviews). Honeycomb carryover (set the bar).

Representative quotes:
- *"Define the engineering standards for how agentic systems are built, tested, evaluated, and operated."* — NVIDIA Agentic IT Ops
- *"Own the team's technical quality bar through design and code reviews. Onboard new engineers, mentor senior and mid-level engineers."* — Basis
- *"Set and uphold the standard for engineering processes to support high-quality engineering."* — Aledade

→ **Already covered by** [`mod-405/exercise-01-agent-code-review-standards`](lessons/mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md). The existing exercise is sized correctly for the signal — no new delta needed.

## Themes just below threshold this cycle

### Agent-runtime sandboxing / secure code execution (23%) — recovering, prior proposal pending

Anchored by **7 postings** this cycle:
- **NVIDIA Agent Platform** — *"Architect multi-tenant Kubernetes execution environments with pod lifecycle management, per-tenant namespace isolation, persistent storage, admission policy enforcement."*
- **SvcNow Moveworks Harness** — *"Agent orchestration, sandboxed file systems and code execution, latency optimization."*
- **Workday Agent Runtime** — whole role: *"The Agent Runtime team builds Workday's secure execution platform for enterprise AI agents. Runtime substrate that enforces policy by architecture, not by prompt, with deterministic controls."*
- **Rippling** — *"Sandboxing"* listed alongside *"harness engineering, eval frameworks, model-related infrastructure, scaling, latency, and reliability"* as explicit AI Platform charter areas.
- **Perplexity** — *"Engineer agent harnesses that connect powerful models with the environments and tools required to perform economically valuable work."*
- **Anthropic Computer Use** — whole team: *"The Computer Use team teaches Claude to see and operate computer interfaces, and builds the agent harness and end-user products."*
- **Harvey Secure Execution** — carried over; whole role still active at 2026-09-30: *"Design, build, and operate a platform for security agents to discover and validate vulnerabilities within authorized targets and execution boundaries."*

Signal recovered half the 2026-10 drop (13% → 23%), with Workday's dedicated Agent Runtime role as a new anchor. Not re-triggered on frequency grounds (23% < 30%); see "Previously-proposed items" below for the pending 2026-09 proposal (`mod-403 exercise-04-secure-agent-code-runtime`).

External resources for learners interested now:
- E2B — <https://e2b.dev/docs>
- Modal sandboxes — <https://modal.com/docs/guide/sandbox>
- Daytona sandboxes — <https://www.daytona.io/docs>
- Cloudflare Durable Objects — <https://developers.cloudflare.com/durable-objects/>
- Firecracker microVMs — <https://firecracker-microvm.github.io/>
- gVisor — <https://gvisor.dev/docs/>
- Anthropic Computer Use — <https://docs.anthropic.com/en/docs/build-with-claude/computer-use>
- WebAssembly — <https://webassembly.org/>

## Trending-up signal this cycle

### Agent memory as a distinct platform surface (27%, +10 pp)

Anchored by **8 postings** this cycle — up from 5 in 2026-10 and 0 before:
- **ByteDance** (*Senior SWE, AI Agent Memory Infrastructure*) — whole role: *"Build the core memory systems that power next-generation intelligent agents. Unified platform for long-term, conversational, and task-oriented memory. Large-scale, low-latency, and highly reliable memory infrastructure. Memory representation, retrieval and ranking, conflict resolution, summarization and fusion. Contributions to or deep understanding of open-source memory frameworks such as mem0, memOS, memU."*
- **Teradata** (*Senior Staff Engineer, Agentic Databases*) — *"Own the design and delivery of one or more of our core Agent Services — Agent Memory, LLM Cache, Semantic Context Layer."*
- **Cloudflare** (*SWE, AI Agents*) — *"Build agents on Workers with Durable Objects for state and short term memory. Use Vectorize, KV, R2, and D1 for semantic memory, cache, files, and config."*
- **Pinecone** (*Senior/Staff SWE, Experience*) — *"Redesigning all of it for a world where AI agents are first-class users alongside humans."* Pinecone is explicitly reframing the vector-DB product around agent memory primitives.
- **Databricks** (*Sr. Staff SWE, Agentic Applications*) — *"Lead architecture reviews, establish design patterns for agents (orchestration, memory, retrieval, tool use, multi-agent coordination)."*
- **Appian** (*Lead Applied AI Engineer*) — *"Design reliable agents and orchestration — planning, tool use, memory, and state — with safe, permission-aware boundaries."*
- **NVIDIA Agent Platform** — *"Build framework-agnostic infrastructure supporting multiple agent SDKs and harnesses — lifecycle hooks, skills configuration, memory services, and OTEL instrumentation."*
- **SvcNow Moveworks Harness** — *"Agent orchestration, sandboxed file systems and code execution, latency optimization, agent memory, LLM self-reflection and improvement, execution environment simulation."*

Meets the 3-posting minimum (8 postings) but still at 27% frequency, so **sub-threshold under continuity bias — no delta this cycle**. The reason this gets a dedicated signal rather than being folded into RAG (theme-13, which collapsed to 3% this cycle): the postings explicitly list *memory* alongside *retrieval* as separate platform surfaces, and ByteDance's / Teradata's / Cloudflare's roles treat memory as its own product primitive with its own API surface. This matches the broader market shift — Letta, Mem0, Zep, LangMem, MemGPT, and Cloudflare's managed memory service treat memory as its own platform primitive distinct from both RAG and durable execution. If this crosses 30% next cycle, the natural extension home is a chapter in [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) on *memory-as-shared-infrastructure* or an exercise extension in [`mod-402-eval-observability-infra`](lessons/mod-402-eval-observability-infra) on observing memory-quality drift.

External resources for learners interested now:
- Letta (ex-MemGPT) — <https://docs.letta.com/>
- Mem0 — <https://docs.mem0.ai/>
- Zep — <https://docs.getzep.com/>
- LangMem — <https://langchain-ai.github.io/langmem/>
- Cloudflare Agents memory APIs — <https://developers.cloudflare.com/agents/>

## New emerging signal this cycle

### Browser-use / computer-use at production altitude (10%)

Anchored by **3 postings** this cycle:
- **Browserbase** (*Software Engineer, Agent Platform*) — whole role: *"Build, operate, and grow the Agent Platform framework — developer-first APIs with ~2M monthly downloads. Agent Platform is Browserbase's framework for automating browsers with code. Work with frontier AI labs (OpenAI, Google, and others) to improve models, benchmark capabilities."*
- **Perplexity** (*Member of Technical Staff, Agents*) — *"Develop and leverage cutting-edge AI models, infrastructure, and browser technologies to advance the capability frontier."*
- **Anthropic** (*Product Engineer, Computer Use*) — whole team: *"The Computer Use team teaches Claude to see and operate computer interfaces, and builds the agent harness and end-user products that turn that capability into real tools."*

Also closely adjacent (not counted — pre-window): Commure's OpenClaw browser-agent platform (July 2026 posting). Below the 30% elevation threshold at 10%. Watch next cycle — the Browserbase / Anchor Browser / Steel Browser hosted-service market is growing fast and Anthropic's Computer Use is now in production. If this crosses threshold, natural home is a chapter in [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) on browser-use-as-tool-seam-hardening or an exercise extension in [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) on build-vs-buy between hosted browser services and in-house Playwright harnesses.

External resources for learners interested now:
- Browserbase — <https://docs.browserbase.com/>
- Anthropic Computer Use — <https://docs.anthropic.com/en/docs/build-with-claude/computer-use>
- Playwright — <https://playwright.dev/>
- Steel Browser — <https://steel.dev/>

### Agent-safety red-teaming — adjacent-not-inside (unchanged from 2026-09 / 2026-10)

Harvey Secure Execution still frames the work as "secure execution" and "containment", not "red team". Anthropic's Computer Use adds adversarial-robustness language ("Diagnose and resolve reliability and robustness issues in the computer-use agent harness that block real-world usage") but still as part of a product-engineering role, not a red-team role. No change — belongs in a hypothetical ai-security-engineer track, not here.

### Staged propose–validate–approve–commit — did not spread, dropped from watch list

XPENG was the only posting using this exact phrase in 2026-10; XPENG is not in this cycle's sample. No other posting adopted the phrase this cycle. Drop from watch-list unless multiple postings pick it up next cycle.

## Previously-proposed items (from 2026-09-07 packet)

The 2026-09 packet proposed two exercise additions, both pre-authorized by the 2026-08-07 packet when the underlying themes crossed 30%. Neither has been merged into `lessons/` as of 2026-11-03 (verified: `lessons/mod-403-multi-agent-at-scale/exercises/exercise-04-*.md` and `lessons/mod-405-technical-leadership/exercises/exercise-04-*.md` do not exist). Both pending proposals live in git history on the 2026-09 `.aicg/curriculum-plan-delta.json` artifact.

| Pending proposal | Target module | 2026-09 freq | 2026-10 freq | 2026-11 freq | Reviewer judgment call |
|---|---|---|---|---|---|
| `exercise-04-secure-agent-code-runtime` | mod-403-multi-agent-at-scale | 35% (9/26) | 13% (4/30) | **23% (7/30)** | Signal recovered half the 2026-10 drop. New dedicated role at Workday (Agent Runtime team) is a strong anchor on top of Harvey Secure Execution and NVIDIA's multi-tenant K8s execution environment work. Still below the 30% re-trigger threshold. Reasonable to defer another cycle to see if it crosses 30%; if it does, re-trigger automatically. The 2026-09 proposal remains defensible on first-principles grounds (sandbox platforms as agent-code seams are a real L40 build target) but is not yet frequency-justified. |
| `exercise-04-mcp-catalog-paved-road` | mod-405-technical-leadership | 35% (9/26) | 27% (8/30) | **30% (9/30)** | Signal landed at exactly the 30% threshold this cycle — up 1 posting from 2026-10, down 1 from the 2026-09 peak. Across three cycles, 26 distinct postings cite MCP-at-platform-scope with new dedicated MCP-platform roles at Writer and Arcade. Not re-triggered on frequency grounds this cycle because 30% is exactly at threshold, not clearly above. The aggregated 3-cycle evidence strongly supports a reviewer merge on first-principles grounds; this cycle's data confirms the signal is holding and not collapsing. Human reviewer owns the merge-vs-defer call. |

Neither pending proposal is re-proposed in this cycle's `.aicg/curriculum-plan-delta.json`; the reviewer owns the decision on the 2026-09 artifacts independently.

## Out-of-scope / linked-out themes

For requirements that would belong at another rung per the ownership rule, we link out rather than duplicating.

| Theme | Link |
|---|---|
| Agent framework mechanics (LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK, LlamaIndex, Semantic Kernel, Strands) | [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) |
| RAG pipeline mechanics, embeddings, rerankers, vector DBs | [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory); depth in [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning) |
| Single-agent evaluation / trajectory + tool-call grading | [`agentic-ai-engineer-learning/mod-205-evaluation-observability`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-205-evaluation-observability) |
| Guardrail *implementation* basics (I/O moderation, prompt-injection defenses, tool-permission enforcement, HITL checkpoints) | [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation) |
| Architecture-level orchestration design | [`agentic-systems-architect-learning/mod-302-multi-agent-orchestration`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-302-multi-agent-orchestration) |
| Architecture-level memory + context engineering | [`agentic-systems-architect-learning/mod-303-memory-context-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-303-memory-context-architecture) |
| Architecture-level eval strategy | [`agentic-systems-architect-learning/mod-304-evaluation-harnesses`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-304-evaluation-harnesses) |
| Architecture-level guardrails & threat modeling | [`agentic-systems-architect-learning/mod-306-guardrails-safety-security`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security) |
| Architecture-level cost/latency architecture | [`agentic-systems-architect-learning/mod-307-cost-latency-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-307-cost-latency-architecture) |
| Architecture-level governance, compliance, regulated-domain architecture | [`agentic-systems-architect-learning/mod-309-governance-compliance-domain-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-309-governance-compliance-domain-architecture) |
| Agent modeling / SFT / RLHF / LoRA / synthetic data | [`ml-engineering-curriculum`](https://github.com/ml-engineering-curriculum) tracks |

## Conclusion

<!-- needs-research: monitor theme-21 (agent memory as platform surface — now at 27%, 8 postings, +10 pp this cycle — Letta/Mem0/Zep/LangMem/MemGPT ecosystem + Cloudflare managed memory service + ByteDance dedicated role) frequency in the next cycle; most credible candidate to cross 30% in 2026-12. Also monitor theme-14 (MCP-at-fleet-scale, exactly at 30% this cycle with 3-cycle sustained signal) — if next cycle lands at ≥31%, re-trigger the 2026-09 pending proposal automatically. Also monitor theme-15 (agent-runtime sandboxing, recovered to 23% with Workday's new dedicated Agent Runtime role) — the signal appears to have stabilized at ~20-25%, re-trigger if it crosses 30%. Also monitor theme-22 (browser-use / computer-use, new signal at 10% this cycle — Browserbase whole-role, Perplexity, Anthropic Computer Use) — the hosted-browser-service market is growing fast; watch for ≥30% in Q1 2027. -->

The `mod-401..405` build spine covers every job-market requirement that clears the continuity-bias thresholds at L40 altitude this cycle. Framework / RAG / single-agent-eval / guardrail-implementation / HITL fundamentals stay owned by the L30 `agentic-ai-engineer-learning` track and are named as prerequisites; architecture-level design (topology, memory architecture, threat modeling, cost architecture, governance) stays owned by the L48 `agentic-systems-architect-learning` track and is linked as the natural follow-on. **No delta is proposed this cycle.** Two pending exercise proposals from 2026-09 (sandbox runtime, MCP catalog) remain unmerged in git history; the MCP-catalog proposal now has three cycles of sustained ≥27% evidence and this cycle landed at exactly 30%, strengthening its case for a human-review merge without crossing the clean re-trigger threshold. The sandbox-runtime proposal recovered to 23% with Workday's new dedicated Agent Runtime role but is still below threshold. Re-run on the next quarterly cycle (2026-12) to catch the predicted theme-21 (agent-memory) threshold crossing, continued theme-14 (MCP-at-fleet-scale) stability, and whether theme-22 (browser-use / computer-use) continues to grow.
