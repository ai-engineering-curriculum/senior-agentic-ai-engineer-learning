# Job Requirements — Senior Agentic AI Engineer

**Role level:** 40 (lead / staff *build* rung — one altitude below `agentic-systems-architect`)
**Track:** `senior-agentic-ai-engineer-learning`
**Research window:** 2026-07-09 → 2026-10-07 (last 90 days)
**Today:** 2026-10-07
**Prior refresh:** 2026-09-07 (26 postings, proposed 2 exercises — see "Previously-proposed items" below)

This file maps verbatim requirements from current L40-altitude agent-engineering job postings to the existing curriculum. Raw normalized data lives in [`.aicg/job-requirements.json`](.aicg/job-requirements.json); the strictly-additive proposal lives in [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).

## Summary

- Postings sampled: **30** (all in the 2026-07-09 → 2026-10-07 window; cap of 2 postings per employer applied).
- Equivalent titles counted per research packet: `Senior Agentic AI Engineer`, `Staff Agentic AI Engineer`, `Senior AI Agent Engineer`, `Lead Applied AI Engineer`, `Agentic Platform Engineer` — plus close matches at senior/staff altitude (`Staff Software Engineer, AI Agents / Agentic focus`, `Senior Software Engineer, Agentic Platform`, `Senior Software Engineer II — Agentic Intelligence`, `Staff AI Engineer` when JD emphasizes agentic + leadership, `Senior Platform Engineer — AI Agent Infrastructure`, `Staff Software Engineer, Secure Execution`, `Senior Software Engineer, Meta Factory Agent Harness`, `Software Engineer, Evals`).
- **Proposed delta this cycle: 0 modules, 0 exercises, 0 projects.** No theme crossed the continuity-bias threshold that is not already covered by `mod-401..405` or by a lower-level track linked as prerequisite.
- The two themes that crossed threshold in the 2026-09 packet — `theme-14` MCP-servers-at-fleet-scale and `theme-15` agent-runtime-sandboxing — **have reverted below the 30% threshold** this cycle. Those pending exercise proposals (`mod-403 exercise-04 secure-agent-code-runtime`, `mod-405 exercise-04 mcp-catalog-paved-road`) are not re-triggered on frequency grounds. They remain in last cycle's artifact awaiting human review; see "Previously-proposed items" below for the reviewer's judgment call framing.
- One **new emerging sub-threshold signal** this cycle: *agent memory as a distinct platform surface* (`theme-21`, 17%, 5 postings — Inflection, Tebra, Deloitte, Lightning AI, Assent) — treating semantic/episodic/working memory as its own build target rather than folded into RAG. Below the 30% threshold; watch next cycle. Letta / Mem0 / Zep / LangMem ecosystem + Cloudflare's managed memory service may push this across threshold in Q1 2027.

## Methodology

- **Sources:** `job-boards.greenhouse.io` (bulk), `jobs.lever.co`, `jobs.ashbyhq.com` (snippet extraction when 403), direct careers pages (`apply.deloitte.com`, `careers.toasttab.com`, `okta.com/company/careers`, `builtinnyc.com`), mirror sites (`zapply.jobs`, `simplify.jobs`, `jobs.accel.com`) when the primary host 403s.
- **Per-posting capture:** employer, title, URL, `date_observed`, `date_posted` (explicit when visible — Harvey 2026-09-30, Assent 2026-09-30, Okta 2026-09-29, Frame.io 2026-07-28, Deloitte 2026-06-09 valid-through-2026-11-13; else `estimated:YYYY-MM` from "posted N days ago" or active-rotation signals), location, 3–6 verbatim/near-verbatim requirement quotes prioritized on L40-distinguishing altitude (ownership, standards, mentoring, infrastructure, SLOs, incidents, cost/latency at scale, code-review leadership, paved roads, MCP catalogs, sandbox platforms) rather than L30 build fundamentals.
- **Frequency** = distinct in-window postings citing the theme ÷ 30 in-window postings.
- **Threshold for a new curriculum item:** ≥ 3 postings AND ≥ 30% frequency AND no existing module/exercise can be incrementally extended to cover it.
- **Continuity bias applied strictly:** for every above-threshold theme, checked (a) existing L40 coverage first, (b) whether the theme belongs at a lower level per the ownership rule.
- **Sample-composition caveat:** the 2026-10 sample tilts slightly more generalist (Applied-AI titles at mid-sized B2B companies) than 2026-09 (which was heavier on sandbox/agentic-platform roles at frontier labs). Top-theme frequencies dipped 10–30 pp but absolute counts changed little; the right read is "nothing has materially emerged or disappeared at threshold," not "the market retreated."

## Ownership rule applied

Where a requirement is genuinely needed at multiple levels, primary ownership sits with the **lowest-level role where it is required**. This L40 track links to the L30 `agentic-ai-engineer` track for build fundamentals and to the L48 `agentic-systems-architect` track for architectural depth, rather than re-teaching either.

## Requirement themes → curriculum ownership

**Bold frequencies** are ≥ 30% (load-bearing under continuity bias). Δ shows change vs 2026-09-07.

| # | Theme | Freq | Δ | Owner role | Coverage |
|---|---|---|---|---|---|
| 1 | Multi-agent orchestration *in production* (topologies under load, handoffs at scale, sub-agent boundaries defended by SLAs) | **67%** | -18 | `senior-agentic-ai-engineer` | [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) |
| 2 | Building evaluation infrastructure (harnesses, LLM-judge rubrics, CI-integrated eval gates) | **67%** | -10 | `senior-agentic-ai-engineer` | [`mod-402/exercise-01-reusable-eval-harness`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md), [`exercise-03-regression-gates`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md) |
| 3 | Reliability for agent systems in production ("holds up under load", state machines with recovery) | **63%** | -2 | `senior-agentic-ai-engineer` | [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) + [`mod-403/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) |
| 4 | Observability & tracing infrastructure for agent *fleets* (trajectory visibility, OTel GenAI, quality/drift dashboards) | **60%** | -9 | `senior-agentic-ai-engineer` | [`mod-402/exercise-02-tracing-and-dashboards`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md) |
| 5 | Agent framework fluency (LangGraph, LangChain, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK, LlamaIndex, Semantic Kernel) | **53%** | -12 | `agentic-ai-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) |
| 6 | RAG pipelines, retrieval quality, embedding/rerank strategy | **50%** | +12 | `agentic-ai-engineer` (L30) / `rag-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory); depth in [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning) |
| 7 | Paved roads / shared services / platform templates for internal agent teams | **40%** | -6 | `senior-agentic-ai-engineer` | [`mod-405/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md), [`mod-402/04-paved-road-adoption`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md) |
| 8 | Technical leadership: mentoring, setting engineering standards, design/code review at senior-plus altitude | **37%** | -17 | `senior-agentic-ai-engineer` | [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership) |
| 9 | Guardrails, prompt-injection defense, agent sandboxing (JD-level, broad) | **30%** | -32 | `agentic-ai-engineer` (L30) basics → `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture at L48 [`mod-306`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security). L40 production-hardening lens: [`mod-403/04-hardening-communication`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md) |
| 10 | Cost / latency / token budgets defended with numbers (caching, routing, context-window pruning) | **30%** | -28 | `senior-agentic-ai-engineer` | [`mod-403/02-token-and-latency-budgets`](lessons/mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md) + [`exercise-03`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-03-token-and-latency-budgets.md); [`mod-404/02-cost-controls-and-budgets`](lessons/mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md) |
| 11 | Enterprise integration & secure tool auth (OAuth 2.0 / 2.1, RBAC, MCP-servers to internal systems) | **30%** | -12 | `agentic-ai-engineer` (L30) primary; `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture: [`agentic-systems-architect-learning/mod-306/04-oauth-rbac-tokens`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md) |
| 12 | Architecture ownership, build-vs-buy at subsystem level, prototype → production refactoring | 27% | -27 | `senior-agentic-ai-engineer` | [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) — whole module. [`04-build-vs-buy-and-complexity`](lessons/mod-401-agent-systems-in-practice/04-build-vs-buy-and-complexity.md) + [`exercise-03-prototype-to-production-refactor`](lessons/mod-401-agent-systems-in-practice/exercises/exercise-03-prototype-to-production-refactor.md) |
| 13 | MCP servers at *fleet scale* (multi-team, auth-wrapped, versioned catalogs — distinct from single-client authoring) | 27% | -8 | sub-threshold this cycle (prior-cycle proposal pending) | **Pending from 2026-09:** [`.aicg/curriculum-plan-delta.json` (2026-09 artifact)](.aicg/curriculum-plan-delta.json) proposed `mod-405 exercise-04-mcp-catalog-paved-road`. Not re-triggered on frequency this cycle but signal is nearly flat in absolute terms (8/30 vs 9/26). Single-server MCP authoring remains at L30 [`mod-202-frameworks/exercises/exercise-04-mcp-tool-server`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks). See "Previously-proposed items" below. |
| 14 | Regulated / compliance-heavy domain integration (fintech, health, HCM, gov, marketing) | 23% | 0 | `agentic-systems-architect` (L48) architectural depth | Architectural coverage at L48 [`mod-309-governance-compliance-domain-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-309-governance-compliance-domain-architecture). L40 build-lens surfaces this in [`mod-404/01-slos-and-slis-for-agents`](lessons/mod-404-reliability-cost-incident/01-slos-and-slis-for-agents.md) as "cost-of-being-wrong" framing on SLOs. |
| 15 | Agent-specific code review, standards, "set the bar" for agentic-system quality | 20% | -11 | `senior-agentic-ai-engineer` | [`mod-405/exercise-01-agent-code-review-standards`](lessons/mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md) |
| 16 | Agent memory as a distinct platform surface (semantic/episodic/working-memory stores — distinct from RAG and from durable execution) | 17% | *new* | sub-threshold emerging | See "New emerging signal" below. Natural home if it crosses 30%: a chapter extension in [`mod-403`](lessons/mod-403-multi-agent-at-scale) or an observability extension in [`mod-402`](lessons/mod-402-eval-observability-infra) for memory-quality drift. |
| 17 | Agent-runtime sandboxing / secure code execution (Firecracker, gVisor, E2B, Modal, Daytona, WebAssembly, microVMs) | 13% | -22 | sub-threshold this cycle (prior-cycle proposal pending) | **Pending from 2026-09:** proposed `mod-403 exercise-04-secure-agent-code-runtime`. Not re-triggered on frequency this cycle. See "Previously-proposed items" below. |
| 18 | AI-native dev tools (Cursor / Claude Code / Codex / Gemini CLI) as core work-style instrument | 13% | -14 | sub-threshold not curriculum-worthy | Not an agent-build skill; a work-style expectation. Formation Bio has elevated it to explicit JD text; still below the 40% elevation threshold to add to [`PREREQUISITES.md`](PREREQUISITES.md). |
| 19 | Human-in-the-loop / approval boundaries | 13% | -37 | `agentic-ai-engineer` (L30) basics | Prerequisite: [`agentic-ai-engineer-learning/mod-206/exercises/exercise-04-human-approval-checkpoints`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). L40 hardening lens implicit in [`mod-403/04-hardening-communication`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md) and [`mod-405/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md). |
| 20 | Incident response for agent failures (runbooks, on-call, RCA, drift-triggered alerts) | 10% | -21 | `senior-agentic-ai-engineer` | [`mod-404/03-incident-response-for-agents`](lessons/mod-404-reliability-cost-incident/03-incident-response-for-agents.md), [`exercise-03`](lessons/mod-404-reliability-cost-incident/exercises/exercise-03-agent-incident-response.md), [`04-postmortems-and-durable-fixes`](lessons/mod-404-reliability-cost-incident/04-postmortems-and-durable-fixes.md) |
| 21 | Durable execution / state machines (pause/resume, versioned trajectories, Temporal) | 7% | -8 | `senior-agentic-ai-engineer` | [`mod-403/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md), [`exercise-02-durable-execution-in-production`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-02-durable-execution-in-production.md) |

## Posting evidence for load-bearing themes

The tables below list postings anchoring each ≥ 30% theme. All 30 sampled postings fall within 2026-07-09 → 2026-10-07.

### Theme 1 — Multi-agent orchestration *in production* (67%)

Anchored by Honeycomb (multi-agent Canvas investigation), XPENG (agentic layer: multi-agent workflows), Inflection AI (backend systems that power agentic workflows), Sonatype (fleets of agents in parallel), Together AI (distributed services + orchestration framework), PagerDuty (multi-step agents + prompt orchestration), Voya Financial (agentic/multi-step workflows), Weedmaps (coding agent that opens PRs), Tebra (multi-step agentic systems), Deloitte (multi-step reasoning + workflow execution), FourKites (agent workflows in production), Striveworks (LLM-powered agents + agentic workflows), Future (parallel API orchestration), Pagaya (agentic workflows), LTS (multi-agent AI systems), Artefact (orchestration + tool/function calling), Robots and Pencils (agentic systems in production), Assent (sub-agent orchestration), Anthropic (multi-step reasoning primitives), Lightning AI (AI agent orchestration and execution).

Representative quotes:
- *"Multiple agents collaborating on one shared Canvas investigation each claiming a hypothesis."* — Honeycomb
- *"Orchestrate fleets of agents in parallel across planning, coding, testing, and review."* — Sonatype
- *"Build the distributed services, orchestration framework, knowledge graph, and retrieval systems that power infrastructure agents."* — Together AI
- *"Build and evolve the agentic layer: agent lifecycle, tool/MCP integrations, sandboxed execution, multi-agent workflows."* — XPENG

→ Covered by [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) — orchestration under load, token/latency budgets, durable execution, and hardening inter-agent communication and tool seams. Architecture-level topology *design* stays with L48 [`mod-302`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-302-multi-agent-orchestration).

### Theme 2 — Building evaluation infrastructure (67%)

Anchored by Honeycomb (evals that tell you whether they got better), XPENG (agent evaluation + safety guardrails), Inflection (evaluation harnesses as internal platform piece), Sonatype (define the evals, harnesses, guardrails, review rituals), Harvey (adversarial tests + evaluations + telemetry), Together AI (evaluations + production feedback loops), PagerDuty (evaluation harnesses + prompt/version management), Voya (scalable experimentation and evaluation frameworks), Weedmaps (offline test sets + online metrics), Tebra (automated evaluation pipelines), Deloitte (deployment eval gates), Striveworks (evaluation approaches + frameworks for safety), Future (eval harnesses using Langfuse), LTS (testing + evaluation + LLMOps), Artefact (evaluation suites + regression tests), Formation Bio (evaluation + validation), Robots and Pencils (evaluation frameworks + observability), Assent (evaluation harnesses + production observability), Tide (automated evaluation pipelines), Glean (large-scale evaluation pipelines).

Representative quotes:
- *"Define what 'good' means for agents here. Set the bar: measurable against real evals, maintainable, and honest about their limits."* — Honeycomb
- *"The Evals & Observability team owns the measurement and quality layer that makes Glean's Assistant and Agents reliably better."* — Glean
- *"Design and build automated evaluation pipelines to measure agent reasoning accuracy and safety trajectories."* — Tide
- *"Define the evals, harnesses, guardrails, and review rituals that let your team confidently ship code."* — Sonatype

→ Covered by [`mod-402-eval-observability-infra`](lessons/mod-402-eval-observability-infra), especially [`exercise-01-reusable-eval-harness`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md) and [`exercise-03-regression-gates`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md). Architecture-level eval strategy sits at L48 [`mod-304-evaluation-harnesses`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-304-evaluation-harnesses).

### Theme 3 — Reliability for agent systems in production (63%)

Anchored by Honeycomb (production-grade agents, trustworthy mid-incident), XPENG (reliability of agentic layer), BambooHR (safe at scale), Inflection (high-availability inference pipelines), Harvey (operate a platform for security agents), Together AI (production AI agents remediating infrastructure), PagerDuty (serving LLM-based systems in production), Voya (production-grade reliability + SLOs), Weedmaps (production reliability + on-call), Tebra (production AI pipelines), Deloitte (long-horizon reliability + recovery from compounding errors), Frame.io (reliable agentic systems), FourKites (production deployment on K8s), Striveworks (degradation in the real world), Future (reliability + observability), Robots and Pencils (production environments), Assent (production-ready agents), Anthropic (performance + reliability of core serving path), Tide (reliability + safety + scalability), Lightning AI (long-running distributed AI workflows), Cresta Backend (scalability + reliability).

Representative quotes:
- *"Engineer for long-horizon reliability — multi-step task completion, recovery from compounding errors, planning under uncertainty, and robust tool use when individual steps fail."* — Deloitte
- *"Build reliable infrastructure that enables long-running, distributed AI workflows."* — Lightning AI
- *"The models perform in testing, but they degrade in the real world. And when performance drops, trust goes with it."* — Striveworks

→ Covered by [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) (SLOs/SLIs for agents, quality drift, cost controls, incident response, postmortems) and [`mod-403-multi-agent-at-scale/03-durable-execution`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) (durable execution and resumption for long-running agent workloads).

### Theme 4 — Observability & tracing infrastructure for agent fleets (60%)

Anchored by Honeycomb (high cardinality data makes agents different), XPENG (observability + safety guardrails), Inflection (observability as internal platform piece), Sonatype (observability for multi-agent systems), Harvey (telemetry that verifies containment), Together AI (observability + incident management), PagerDuty (tracing and observability), Voya (monitoring for response quality + latency + reliability), Weedmaps (instrument agents with tracing and logging), Tebra (real-time observability), Deloitte (observability + tracing for prompts, tool calls, retrieval quality, drift), Future (monitor traces + iterate), LTS (monitoring + observability), Artefact (monitor cost, latency, and quality), Formation Bio (observability + security), Robots and Pencils (observability tools), Assent (production observability), Glean (trace enrichment + durable telemetry pipelines + dashboards), Lightning AI (platform reliability + observability).

Representative quotes:
- *"Build agent observability infrastructure, including trace enrichment, durable telemetry pipelines, dashboards, and debugging."* — Glean
- *"Implement observability and tracing for prompts, tool calls, retrieval quality, agent traces, failures, drift, latency, and production behavior."* — Deloitte
- *"Instrument agents with tracing and logging so failures can be diagnosed and fixed quickly."* — Weedmaps

→ Covered by [`mod-402-eval-observability-infra/exercise-02-tracing-and-dashboards`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md); OTel GenAI semantic conventions covered in the accompanying chapter. Deeper stable-trace-identity work sits at L48 [`mod-305-observability-tracing`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-305-observability-tracing).

### Theme 5 — Agent framework fluency (53%)

Anchored by XPENG (workflow engines + multi-agent frameworks), Inflection (LangGraph + LlamaIndex + Agent SDKs), Sonatype (LangGraph-style graphs + MCP), PagerDuty (LLMOps tooling + prompt management), Cresta Forward Deployed (general AI agent frameworks + function calling), FourKites (LangGraph non-negotiable), Striveworks (LLM-powered agents + workflows), Future (LangChain/LangGraph), Pagaya (agentic orchestration frameworks), LTS (LangGraph + LangChain + LlamaIndex + Semantic Kernel + AutoGen + CrewAI), Artefact (LangGraph/LangChain + Google ADK + Claude Agent SDK + OpenAI Agents SDK), Deloitte (LangGraph + LangChain), Lightning AI (orchestration frameworks), Tebra (LangChain/LangGraph/LlamaIndex/CrewAI), Robots and Pencils (agentic frameworks), Assent (LangChain/LangGraph/CrewAI/AutoGen/MCP-based), Okta (LangChain/LangGraph/LangSmith), Temporal (agent frameworks + Nexus).

→ Owned at L30 by [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks). Named as a **prerequisite** in [`PREREQUISITES.md`](PREREQUISITES.md); this L40 track does not re-teach framework mechanics. No new frameworks observed beyond the set already in the L30 module.

### Theme 6 — RAG pipelines, retrieval quality, embedding/rerank (50%)

Anchored by Inflection, Cresta Forward Deployed, Together AI (knowledge graph + retrieval), PagerDuty (RAG), Weedmaps (RAG components implicit), Voya (vector search + retrieval), Tebra (vector databases + semantic search + knowledge graph), Deloitte (RAG pipelines), Future (retrieval + evals), Pagaya (RAG architectures), LTS (RAG), Artefact (RAG + embeddings + vector search), Robots and Pencils (RAG: chunking + embedding + vector DBs + rerank), Assent (RAG grounded in Confluence/Jira/Snowflake/Salesforce), Formation Bio (retrieval systems), Okta (RAG on AWS).

→ Owned at L30 by [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory) and by the specialist [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning) track. Named as a **prerequisite**; this L40 track does not re-teach RAG mechanics. The 12 pp increase this cycle is driven by generalist Applied-AI postings adopting RAG as a baseline — it does not change the ownership decision.

### Theme 7 — Paved roads / shared services / platform templates (40%)

Anchored by Inflection (internal platform pieces: service templates, CI/CD, observability, evaluation harnesses, rollout tooling), Sonatype (internal playbooks, tooling, and rituals), Harvey (reusable controls for agent tool use), Together AI (platform for infrastructure agents), BambooHR (patterns multiple teams build on), Voya (reusable platform services, APIs, design patterns), Weedmaps (extend internal MCP server with shared skills, tools, processes), Frame.io (reusable architecture patterns), Robots and Pencils (ML platforms), Tide (shared capabilities across Tide), Assent (reusable patterns in a shared library), Lightning AI (platform APIs + capabilities).

Representative quotes:
- *"Build internal platform pieces: service templates, CI/CD, observability, evaluation harnesses, and rollout tooling that compound engineering velocity."* — Inflection
- *"Extend our internal MCP server with shared skills, tools and processes that other teams can reuse."* — Weedmaps
- *"Shape the shared capabilities that allow AI systems to operate safely, reliably, and at scale across Tide."* — Tide

→ Covered by [`mod-405-technical-leadership/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md) and [`mod-402-eval-observability-infra/04-paved-road-adoption`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md).

### Theme 8 — Technical leadership (37%)

Anchored by Honeycomb (set the bar), BambooHR (own technical direction + specification quality standard), Sonatype (set the bar for how Sonatype engineers work with agents, train Senior engineers), Harvey (set the technical direction, work across Security/Infra/Product), PagerDuty (raise the bar through reviews and mentorship), Tebra (set the standards), Weedmaps (design docs, mentor), Frame.io (shape the technical direction), LTS (mentor engineers through technical leadership), Artefact (end-to-end technical ownership), Robots and Pencils (lead design and implementation end-to-end), Tide (technical leadership across teams), Lightning AI (mentor engineers on system design).

Representative quotes:
- *"Set the bar for how Sonatype engineers work with agents. Shape internal playbooks, tooling, and rituals; train Senior engineers in the craft."* — Sonatype
- *"You own the technical direction of a product area and the patterns multiple teams build on."* — BambooHR
- *"Set the technical direction for secure agent execution, working across Security, Infrastructure, and Product Engineering."* — Harvey

→ Covered end-to-end by [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership): agent code review with safety focus, paved roads & standards, design-to-execution translation, scoping & sequencing.

### Theme 9 — Guardrails, prompt injection, agent sandboxing (30%)

Anchored by XPENG (safety guardrails), BambooHR (security architecture for agentic work), Harvey (robust sandboxing + agent containment), Tebra (enterprise AI guardrails), Deloitte (healthcare-grade safety), Weedmaps (prompt injection, memory poisoning defense, least-privilege tool access), Voya (data security + privacy controls), LTS (guardrails), Robots and Pencils (prompt injection defenses + PII handling).

→ Basics owned at L30 by [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture-level threat modeling owned at L48 by [`agentic-systems-architect-learning/mod-306-guardrails-safety-security`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security). The L40 track's contribution is production hardening of tool + inter-agent seams in [`mod-403-multi-agent-at-scale/04-hardening-communication`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md).

### Theme 10 — Cost / latency / token budgets (30%)

Anchored by Inflection (latency/cost/quality tradeoffs), PagerDuty (serving LLM-based systems at scale), Voya (latency + performance optimization), Weedmaps (route to cheapest model + caching + structured outputs), Tebra (latency/cost monitoring), Future (prompt caching + token budgets + retry logic), Artefact (monitor cost + latency + quality), Robots and Pencils (token economics + caching + model routing + quantization), Assent (cost control + failure handling), Tide (cost-management + routing logic).

Representative quotes:
- *"Advanced cost optimization expertise: token economics, caching strategies, model routing, quantization."* — Robots and Pencils
- *"Drive cost and latency down: route work to the cheapest model that can do it, use caching and structured outputs."* — Weedmaps

→ Covered by [`mod-403-multi-agent-at-scale/02-token-and-latency-budgets`](lessons/mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md), [`exercise-03`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-03-token-and-latency-budgets.md), and [`mod-404-reliability-cost-incident/02-cost-controls-and-budgets`](lessons/mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md). Architecture-level token economics at L48 [`mod-307-cost-latency-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-307-cost-latency-architecture).

### Theme 11 — Enterprise integration & secure tool auth (30%)

Anchored by XPENG (connectors to internal and operational systems), Harvey (integrate with identity and secrets platforms), Together AI (ticketing + source control + chat + fleet inventory), Cresta Forward Deployed (APIs + databases + CRMs), Voya (entitlements + access controls), LTS (enterprise tools), Striveworks (external tools + APIs + MCP servers + enterprise data sources), Artefact (APIs + semantic layers + MCP), Okta (REST/SOAP + A2A + MCP + Workday Agent System of Record).

→ Basics (OAuth 2.0 / 2.1 / RBAC for agent toolchains) owned at L30 by [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture-level in L48 [`mod-306/04-oauth-rbac-tokens`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md).

## Themes just below threshold this cycle

### MCP servers at fleet scale (27%) — reverted below threshold

Anchored by XPENG (tool/MCP integrations), Weedmaps (internal MCP server with shared skills), Deloitte (MCP-style tool/context interfaces), Sonatype (Claude Code + Codex + Cursor + MCP tooling), Striveworks (MCP servers + enterprise data sources), Artefact (APIs + semantic layers + MCP), Assent (MCP-based orchestration), Okta (REST/SOAP + A2A + MCP).

Absolute count is nearly flat vs 2026-09 (8 of 30 vs 9 of 26); the frequency change is denominator-driven. The 2026-09 pending proposal (`mod-405 exercise-04 mcp-catalog-paved-road`) remains in last cycle's artifact; not re-triggered on frequency this cycle but not clearly obsolete either. See "Previously-proposed items" below.

### Agent-runtime sandboxing / secure code execution (13%) — reverted below threshold

Anchored by Harvey Secure Execution (whole role dedicated to it), XPENG (sandboxed execution), Frame.io (Agent Harness runtime), Weedmaps (least-privilege tool access as a runtime concern).

Absolute count dropped from 9 to 4; this is more than a denominator effect — the 2026-09 sandbox-platform hiring cluster (Instabase Agent Harness, Scale AI Sandbox Platform, Scale AI RL Environments, Vercel SWE Agent) has largely closed headcount. The signal is real but softer than theme-14. See "Previously-proposed items" below.

External resources for learners interested now:
- E2B — <https://e2b.dev/docs>
- Modal sandboxes — <https://modal.com/docs/guide/sandbox>
- Daytona sandboxes — <https://www.daytona.io/docs>
- Cloudflare Sandbox — <https://developers.cloudflare.com/durable-objects/>
- Firecracker microVMs — <https://firecracker-microvm.github.io/>
- gVisor — <https://gvisor.dev/docs/>
- Anthropic Computer Use — <https://docs.anthropic.com/en/docs/build-with-claude/computer-use>
- WebAssembly — <https://webassembly.org/>

## New emerging signal this cycle

### Agent memory as a distinct platform surface (17%)

Anchored by **5 postings** this cycle:
- **Inflection AI** (*Staff Engineer, Agentic*) — *"Backend systems that power agentic workflows in production: orchestration, memory, retrieval, and tool integrations."*
- **Tebra** (*Staff SWE, AI Engineering*) — *"Multi-step agentic systems utilizing multi-tier memory networks."*
- **Deloitte** (*Agentic AI Engineer, Healthcare*) — treats memory and control layers as architecture concerns distinct from retrieval.
- **Lightning AI** (*Senior SWE, Agents*) — *"Scalable APIs and platform capabilities for tool use, workflow orchestration, memory, and state management."*
- **Assent** (*Senior Agentic AI Engineer*) — *"Production agent systems using tool calling, sub-agent orchestration, memory and context management."*

Meets the 3-posting minimum (5 postings) but only 17% frequency, so **sub-threshold under continuity bias — no delta this cycle**. The reason this gets a dedicated signal rather than being folded into RAG (theme-6): the postings explicitly list *memory* alongside *retrieval* as separate platform surfaces, not as "RAG memory." This matches the broader market shift — Letta, Mem0, Zep, LangMem, and Cloudflare's recently-GA managed memory service treat memory as its own platform primitive. If this crosses 30% next cycle, the natural extension home is a chapter in [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) on *memory-as-shared-infrastructure* or an exercise extension in [`mod-402-eval-observability-infra`](lessons/mod-402-eval-observability-infra) on observing memory-quality drift.

External resources for learners interested now:
- Letta (ex-MemGPT) — <https://docs.letta.com/>
- Mem0 — <https://docs.mem0.ai/>
- Zep — <https://docs.getzep.com/>
- LangMem — <https://langchain-ai.github.io/langmem/>
- Cloudflare Agents memory APIs — <https://developers.cloudflare.com/agents/>

### Staged propose-validate-approve-commit (3%) — did not spread

The 2026-09 packet flagged XPENG's "staged propose–validate–approve–commit flows" as a specific build pattern to watch. This cycle XPENG is still the only posting using the exact phrase; Deloitte and Tebra reference HITL checkpoints and human review but not a staged commit pipeline. Below the 3-posting elevation floor. Do not elevate; keep watching next cycle.

### Agent-safety red-teaming — adjacent-not-inside (unchanged from 2026-09)

Harvey's Secure Execution role has adversarial-test work and Weedmaps mentions least-privilege and prompt-injection hardening, but neither frames the role as "red team." Red-teaming remains a sibling role family (ai-security-engineer altitude) rather than a requirement inside sr-agentic-engineer postings. No change from 2026-09 position.

## Previously-proposed items (from 2026-09-07 packet)

The 2026-09 packet proposed two exercise additions, both pre-authorized by the 2026-08-07 packet when the underlying themes crossed 30%:

| Pending proposal | Target module | 2026-09 freq | 2026-10 freq | Reviewer judgment call |
|---|---|---|---|---|
| `exercise-04-secure-agent-code-runtime` | mod-403-multi-agent-at-scale | 35% (9/26) | **13%** (4/30) | Signal softened materially. Reasonable to defer merge for another cycle to see whether sandbox-platform hiring returns (Instabase, Scale AI, Vercel's 2026-09 cluster closed headcount this cycle). Harvey's Secure Execution still indicates the role class exists; if a similar cluster re-opens next cycle, re-trigger. |
| `exercise-04-mcp-catalog-paved-road` | mod-405-technical-leadership | 35% (9/26) | **27%** (8/30) | Absolute count nearly flat; frequency change is a denominator artifact. 8 postings this cycle still cite MCP-at-platform-scope (XPENG, Weedmaps, Deloitte, Sonatype, Striveworks, Artefact, Assent, Okta). Reasonable to merge on first-principles grounds — the signal has not collapsed, and MCP-catalog ownership is a defensible sr-level build problem. Not re-triggered on this cycle's frequency math alone. |

Neither pending proposal has been merged into `lessons/` as of 2026-10-07 (both exercise directories still show 3 exercises). This cycle's `.aicg/curriculum-plan-delta.json` is empty and does NOT re-propose these; the reviewer owns the decision on last cycle's artifact independently.

## Out-of-scope / linked-out themes

For requirements that would belong at another rung per the ownership rule, we link out rather than duplicating.

| Theme | Link |
|---|---|
| Agent framework mechanics (LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK, LlamaIndex, Semantic Kernel) | [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) |
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

<!-- needs-research: monitor theme-21 (agent memory as platform surface — Letta/Mem0/Zep/LangMem/Cloudflare ecosystem) frequency in the next cycle; most credible candidate for the first mod-403 or mod-402 extension if it crosses 30%. Also re-check theme-14 (MCP-at-fleet-scale, currently 27% and holding absolute count) and theme-15 (agent-runtime sandboxing, currently 13% but with Harvey's whole-role evidence) — both have pending 2026-09 proposals awaiting human review; a sustained ≥ 30% signal next cycle would re-trigger them automatically. -->

The `mod-401..405` build spine covers every job-market requirement that clears the continuity-bias thresholds at L40 altitude this cycle. Framework / RAG / single-agent-eval / guardrail-implementation / HITL fundamentals stay owned by the L30 `agentic-ai-engineer-learning` track and are named as prerequisites; architecture-level design (topology, memory architecture, threat modeling, cost architecture, governance) stays owned by the L48 `agentic-systems-architect-learning` track and is linked as the natural follow-on. **No delta is proposed this cycle.** Two pending exercise proposals from 2026-09 (sandbox runtime, MCP catalog) remain unmerged and are not re-triggered by this cycle's data — the reviewer's call on last cycle's artifact is independent of this cycle's zero-delta packet. Re-run on the next quarterly cycle (2027-01) to catch shifts in agent-memory-as-platform-surface, a potential re-opening of sandbox-platform hiring, and any sustained sign of MCP-catalog ownership becoming load-bearing.
