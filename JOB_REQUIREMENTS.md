# Job Requirements — Senior Agentic AI Engineer

**Role level:** 40 (lead / staff *build* rung — one altitude below `agentic-systems-architect`)
**Track:** `senior-agentic-ai-engineer-learning`
**Research window:** 2026-05-09 → 2026-08-07 (last 90 days)
**Today:** 2026-08-07
**Prior refresh:** none — this is the first job-requirements pass for this role.

This file maps verbatim requirements from current L40-altitude agent-engineering job postings to the existing curriculum. Raw normalized data lives in [`.aicg/job-requirements.json`](.aicg/job-requirements.json); the strictly-additive proposal lives in [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).

## Summary

- Postings sampled: **26** (all in the 2026-05-09 → 2026-08-07 window).
- Equivalent titles counted per research packet: `Senior Agentic AI Engineer`, `Staff Agentic AI Engineer`, `Senior AI Agent Engineer`, `Lead Applied AI Engineer`, `Agentic Platform Engineer` — plus close matches at senior/staff altitude (`Staff Software Engineer, AI Agents`, `Senior Software Engineer, Agentic Platform`, `Senior Software Engineer II — Agentic Intelligence`, `Staff AI Engineer` when JD emphasizes agentic workflows + leadership, `Senior Platform Engineer — AI Agent Infrastructure`, `Senior Staff Engineer, Agentic Databases`, `Senior Staff Software Engineer, Agentic Platform`).
- **Proposed delta this cycle: 0 modules, 0 exercises, 0 projects.** Every requirement above the continuity-bias threshold (≥ 3 distinct postings AND ≥ 30% frequency AND no incremental extension possible) is already owned by an existing module in `mod-401..405`, an existing L30 module linked as prerequisite, or an existing L48 module linked as follow-on.
- The strongest **emerging sub-threshold signal** is *agent-runtime sandboxing / secure code execution as an infrastructure primitive* — 3 postings (Instabase, Scale AI, Flex) name Firecracker / gVisor / E2B / Modal / Cloudflare-Sandboxes / Daytona as the concrete build target for isolating agent-generated code. Meets the 3-posting minimum but only 12% frequency; sub-threshold, tracked for next cycle. If this crosses 30% next quarter, propose extending `mod-403 exercise-04 hardening communication` (which currently focuses on inter-agent messaging and tool-call seams) with a fifth exercise on secure agent-code execution runtimes.
- Sub-threshold new signals also tracked: AI-native dev-tool fluency as a work-style expectation (Cursor / Claude Code as *user*) — 2 postings (SecurityScorecard, nCino), 8%. MCP server infra at scale — 5 postings, 19%, already owned by L30 mod-202 exercise-04.

## Methodology

- Sources: `greenhouse.io/job_boards` (bulk), `jobs.ashbyhq.com`, `jobs.lever.co` (403 to WebFetch — snippet extraction), `builtin.com`, `careers.gevernova.com`, `careers.teradata.com`, `jobs.smartrecruiters.com`, `apply.ukg.com`, `jobs.insightpartners.com`, `jobs.accel.com` (mirror), `jobright.ai` (mirror).
- Per-posting capture: employer, title, URL, `date_observed`, `date_posted` (marked `estimated:YYYY-MM` when inferred from "posted N days/weeks ago" or active-rotation signals), location, 4-8 verbatim/near-verbatim requirement quotes prioritized on L40-distinguishing altitude (ownership, standards, mentoring, infrastructure, SLOs, incidents, cost/latency at scale, code-review leadership) rather than L30 build fundamentals.
- Frequency = distinct in-window postings citing the theme ÷ 26 in-window postings.
- Threshold for a new curriculum item: ≥ 3 postings AND ≥ 30% frequency AND no existing module/exercise can be incrementally extended to cover it.
- Continuity bias applied strictly: for every above-threshold theme, checked (a) existing L40 coverage first, (b) whether the theme belongs at a lower level per the ownership rule.
- Source caveats documented in `summary.source_quality_caveats` in `.aicg/job-requirements.json`.

## Ownership rule applied

Where a requirement is genuinely needed at multiple levels, primary ownership sits with the **lowest-level role where it is required**. This L40 track links to the L30 `agentic-ai-engineer` track for build fundamentals and to the L48 `agentic-systems-architect` track for architectural depth, rather than re-teaching either.

## Requirement themes → curriculum ownership

**Bold frequencies** are ≥ 30% (load-bearing under continuity bias).

| # | Theme | Freq | Owner role | Coverage |
|---|---|---|---|---|
| 1 | Multi-agent orchestration *in production* (topologies under load, handoffs at scale, sub-agent boundaries defended by SLAs) | **85%** | `senior-agentic-ai-engineer` (this) | [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) |
| 2 | Technical leadership: mentoring, setting engineering standards, design/code review at senior-plus altitude | **69%** | `senior-agentic-ai-engineer` | [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership) |
| 3 | Building evaluation infrastructure (harnesses, LLM-judge rubrics, CI-integrated eval gates, "measurable against real evals") | **54%** | `senior-agentic-ai-engineer` | [`mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md), [`exercise-03-regression-gates.md`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md) |
| 4 | Observability & tracing infrastructure for agent *fleets* (trajectory visibility, OTel GenAI, quality/drift dashboards) | **54%** | `senior-agentic-ai-engineer` | [`mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md) |
| 5 | Agent-specific code review, standards, "set the bar" for agentic-system quality | **50%** | `senior-agentic-ai-engineer` | [`mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md`](lessons/mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md) |
| 6 | Paved roads / shared services / platform templates for internal agent teams | **50%** | `senior-agentic-ai-engineer` | [`mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md), [`mod-402-eval-observability-infra/04-paved-road-adoption.md`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md) |
| 7 | Reliability for agent systems (production traffic, "hold up under load", state machines with recovery) | **50%** | `senior-agentic-ai-engineer` | [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident), [`mod-403-multi-agent-at-scale/03-durable-execution.md`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) |
| 8 | Agent framework fluency (LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK) | **46%** | `agentic-ai-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) — linked, not re-taught |
| 9 | Guardrails, prompt-injection defense, agent sandboxing | **38%** | `agentic-ai-engineer` (L30) basics → `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture-level threat modeling in [`agentic-systems-architect-learning/mod-306-guardrails-safety-security`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security). L40 lens (production hardening of tool/inter-agent seams): [`mod-403-multi-agent-at-scale/04-hardening-communication.md`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md) |
| 10 | RAG pipelines, retrieval quality, embedding/rerank strategy | **35%** | `agentic-ai-engineer` (L30) / `rag-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory); depth in [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning) |
| 11 | Architecture ownership, build-vs-buy at subsystem level, prototype → production refactoring | **31%** | `senior-agentic-ai-engineer` | [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) — the whole module. `04-build-vs-buy-and-complexity.md` + `exercise-03-prototype-to-production-refactor.md` |
| 12 | Cost / latency / token budgets defended with numbers (caching, routing, context-window pruning) | **31%** | `senior-agentic-ai-engineer` | [`mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md`](lessons/mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md), [`exercise-03-token-and-latency-budgets.md`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-03-token-and-latency-budgets.md), [`mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md`](lessons/mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md) |
| 13 | Regulated / compliance-heavy domain integration (fintech, health, HCM, gov, marketing) | **31%** | `agentic-systems-architect` (L48) architectural depth | Out of scope here — link to [`agentic-systems-architect-learning/mod-309-governance-compliance-domain`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-309-governance-compliance-domain-architecture) for architectural coverage. L40 build-lens surfaces this in [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) as "cost-of-being-wrong" framing on SLOs. |
| 14 | Enterprise integration & secure tool auth (OAuth 2.0, RBAC, MCP-servers to internal systems) | **31%** | `agentic-ai-engineer` (L30) primary; `agentic-systems-architect` (L48) architecture | Prerequisite: [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation) tool-permission enforcement. Architecture: [`agentic-systems-architect-learning/mod-306/04-oauth-rbac-tokens.md`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md) |
| 15 | Durable execution / state machines (pause/resume, versioned trajectories, workflow engines like Temporal) | 23% | `senior-agentic-ai-engineer` | [`mod-403-multi-agent-at-scale/03-durable-execution.md`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md), [`exercise-02-durable-execution-in-production.md`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-02-durable-execution-in-production.md) |
| 16 | MCP servers (authoring, integration to enterprise systems) | 19% | `agentic-ai-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-202-frameworks/exercises/exercise-04-mcp-tool-server.md`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks/exercises/exercise-04-mcp-tool-server.md) |
| 17 | Incident response for agent failures (runbooks, on-call, RCA, drift-triggered alerts) | 15% | `senior-agentic-ai-engineer` | [`mod-404-reliability-cost-incident/03-incident-response-for-agents.md`](lessons/mod-404-reliability-cost-incident/03-incident-response-for-agents.md), [`exercise-03-agent-incident-response.md`](lessons/mod-404-reliability-cost-incident/exercises/exercise-03-agent-incident-response.md), [`04-postmortems-and-durable-fixes.md`](lessons/mod-404-reliability-cost-incident/04-postmortems-and-durable-fixes.md) |
| 18 | Agent-runtime sandboxing / secure code execution (Firecracker, gVisor, E2B, Modal, Cloudflare Sandboxes, Daytona) | 12% | sub-threshold | See "Emerging signals" — 3-posting minimum met (Instabase, Scale AI, Flex) but 12% frequency; no delta this cycle. Extend `mod-403 exercise-04 hardening communication` if it crosses 30% next cycle. |
| 19 | Human-in-the-loop / approval boundaries | 8% | `agentic-ai-engineer` (L30) | Prerequisite: [`agentic-ai-engineer-learning/mod-206/exercises/exercise-04-human-approval-checkpoints.md`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation/exercises) |
| 20 | AI-native dev tools (Cursor / Claude Code) as core work-style instrument | 8% | sub-threshold | Not curriculum-worthy for the agent-build track — this is a work-style expectation for engineers, not a build skill; consider adding to `PREREQUISITES.md` if it crosses 40% next cycle. |

## Posting evidence for load-bearing themes

The tables below list postings anchoring each ≥ 30% theme. All 26 sampled postings fall within 2026-05-09 → 2026-08-07.

### Theme 1 — Multi-agent orchestration *in production* (85%)

| Employer | Title | URL | Date observed | Posted |
|---|---|---|---|---|
| LTS | Senior Agentic AI Software Engineer | https://job-boards.greenhouse.io/lts/jobs/4340374009 | 2026-08-07 | est:2026-07 |
| LTS | Senior Applied AI Engineer | https://job-boards.greenhouse.io/lts/jobs/4340498009 | 2026-08-07 | est:2026-08 |
| LTS | Senior Front-End Agentic AI Engineer | https://job-boards.greenhouse.io/lts/jobs/4340405009 | 2026-08-07 | est:2026-07 |
| Honeycomb.io | Senior Software Engineer II — Agentic Intelligence | https://job-boards.greenhouse.io/honeycomb/jobs/5373987008 | 2026-08-07 | est:2026-07 |
| Tenable | Senior Software Engineer — Agentic AI Platform | https://job-boards.greenhouse.io/tenableinc/jobs/5104542008 | 2026-08-07 | est:2026-06 |
| Grafana Labs | Staff AI Engineer — Grafana AI/ML | https://job-boards.greenhouse.io/grafanalabs/jobs/6100672004 | 2026-08-07 | est:2026-07 |
| Instabase | Software Engineer — Agent Harness | https://job-boards.greenhouse.io/instabase/jobs/8635719002 | 2026-08-07 | est:2026-07 |
| Rayda | Senior Agentic AI Engineer | https://builtin.com/job/senior-agentic-ai-engineer/10368060 | 2026-08-07 | 2026-07-24 |
| GE Vernova | Staff Software Engineer — AI Backend & Agent Frameworks | https://careers.gevernova.com/staff-software-engineer-ai-backend-agent-frameworks/job/R5048627 | 2026-08-07 | 2026-07-29 |
| SecurityScorecard | Staff AI Engineer | https://job-boards.greenhouse.io/securityscorecard/jobs/7779124 | 2026-08-07 | est:2026-07 |
| airSlate | Senior Software Engineer — Agentic AI | https://jobs.lever.co/airslate/7fb7e6ed-4d5d-437f-bb8f-35005f67f41b | 2026-08-07 | est:2026-07 |
| Jobgether (client-branded) | Senior Software Engineer, Agents | https://jobs.lever.co/jobgether/2ea59041-4559-4d01-9b91-b80be3ff213c | 2026-08-07 | est:2026-07 |
| FourKites | Senior AI Engineer | https://job-boards.greenhouse.io/fourkites/jobs/7981512 | 2026-08-07 | est:2026-07 |
| Lantern (Employer Direct Healthcare) | Senior AI Engineer | https://job-boards.greenhouse.io/employerdirecthealthcare/jobs/5098462007 | 2026-08-07 | est:2026-08 |
| Cresta | Senior Forward Deployed Engineer (AI Agent) — UK | https://job-boards.greenhouse.io/cresta/jobs/5097513008 | 2026-08-07 | est:2026-05 |
| nCino | Senior Software Engineer — Agentic Platform | https://jobs.insightpartners.com/companies/ncino/jobs/77782032-senior-software-engineer-agentic-platform | 2026-08-07 | 2026-05-07 |
| Podium | Staff AI Engineer | https://job-boards.greenhouse.io/podium81/jobs/7367363 | 2026-08-07 | est:2026-07 |
| Tide | Senior Staff Software Engineer, Agentic Platform | https://job-boards.greenhouse.io/tide/jobs/7702555003 | 2026-08-07 | est:2026-06 |
| Teradata | Senior Staff Engineer, Agentic Databases | https://careers.teradata.com/jobs/220390/senior-staff-engineer-agentic-databases | 2026-08-07 | est:2026-07 |
| Visa | Staff Software Engineer — AI Agent/Agentic Focus | https://jobs.smartrecruiters.com/Visa/744000118208067-staff-software-engineer-ai-agent-agentic-focus | 2026-08-07 | est:2026-06 |
| Flex | Staff Software Engineer, AI Platform | https://job-boards.greenhouse.io/flex/jobs/4696189005 | 2026-08-07 | est:2026-05 |
| UKG | Staff Software Engineer (Agentic AI) | https://apply.ukg.com/careers/job/893394984892 | 2026-08-07 | est:2026-05 |
| Amplitude | Staff AI Engineer | https://job-boards.greenhouse.io/amplitude/jobs/8562414002 | 2026-08-07 | est:2026-06 |
| PayPay Card | AI Platform Engineer | https://job-boards.greenhouse.io/paypaycard/jobs/5271910008 | 2026-08-07 | 2026-06-24 |
| Yuno | Senior Platform Engineer — AI Agent Infrastructure | https://jobs.lever.co/yuno/33309adb-efb0-414c-9e9a-da13435a0242 | 2026-08-07 | est:2026-07 |
| Scale AI | AI Infrastructure Engineer, Sandbox Platform | https://job-boards.greenhouse.io/scaleai/jobs/4716453005 | 2026-08-07 | est:2026-07 |

Representative quotes:
- *"Architect and implement the backend services that power multi-agent workflows."* — Tenable
- *"Ship AI-powered features that contribute to improving infrastructure and observability quality through automation … high-performance AI features to help users detect, triage, and resolve incidents."* — Grafana Labs
- *"Scale the platform to support a growing catalog of agents, skills, and MCP integrations across Flex while maintaining performance, reliability, and cost efficiency."* — Flex
- *"Design, develop, and deploy autonomous and multi-agent AI systems capable of reasoning, planning, tool use, workflow automation."* — LTS

→ Covered by [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) — orchestration under load, token/latency budgets, durable execution, and hardening inter-agent communication and tool seams. Architecture-level topology *design* stays with L48 [`mod-302`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-302-multi-agent-orchestration).

### Theme 2 — Technical leadership: mentoring, standards, code review at senior-plus altitude (69%)

Anchored by LTS×3, Rayda, Instabase, Lantern, Tide, SecurityScorecard, Amplitude, Bluefish AI-adjacent, nCino, GE Vernova, Visa, Flex, UKG, Teradata, Yuno, Honeycomb, Podium.

Representative quotes:
- *"Mentor engineers through technical leadership, architecture discussions, design reviews, and collaborative problem solving. Help establish engineering standards, reusable frameworks, and best practices across the AI engineering organization."* — LTS
- *"Set the technical bar in code review, design review, and on-call. Mentor engineers on Postgres internals, distributed systems design, and the agentic workload patterns."* — Teradata
- *"Set the standard for how the engineering organization builds with AI, including development practices, tooling choices, and quality bars."* — SecurityScorecard
- *"Set the bar for AI-assisted engineering practices and responsible AI use across Flex, mentor engineers on how to design, build, and operate agentic systems."* — Flex
- *"Set the engineering standard for AI development practices … Mentor and grow junior and mid-level engineers through pairing, design reviews, knowledge-sharing."* — Lantern

→ Covered end-to-end by [`mod-405-technical-leadership`](lessons/mod-405-technical-leadership): agent code review with safety focus, paved roads & standards, design-to-execution translation, scoping & sequencing.

### Theme 3 — Building evaluation infrastructure (54%)

Anchored by LTS×2, Honeycomb, Tenable, TRM-Labs-adjacent, Rayda, Podium, Tide, SecurityScorecard, Amplitude, Flex, airSlate, Yuno, PayPay Card, Grafana, Teradata, UKG.

Representative quotes:
- *"Define what 'good' means for agents here. Set the bar: measurable against real evals, maintainable, and honest about their limits."* — Honeycomb
- *"Design and build automated evaluation pipelines to measure agent reasoning accuracy."* — Tide
- *"Practical experience designing and implementing evaluations for LLM behavior — including accuracy, safety, reliability."* — Podium
- *"Champion best practices for MLOps, agent evaluation, and system observability."* — Tenable
- *"Shaping evaluation strategy, and influencing the long-term roadmap."* — Amplitude

→ Covered by [`mod-402-eval-observability-infra`](lessons/mod-402-eval-observability-infra), especially [`exercise-01-reusable-eval-harness`](lessons/mod-402-eval-observability-infra/exercises/exercise-01-reusable-eval-harness.md) and [`exercise-03-regression-gates`](lessons/mod-402-eval-observability-infra/exercises/exercise-03-regression-gates.md). Trajectory/tool-call/LLM-judge grading rubrics inherited from L30 [`mod-205-evaluation-observability`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-205-evaluation-observability). Architecture-level eval strategy sits at L48 [`mod-304-evaluation-harnesses`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-304-evaluation-harnesses).

### Theme 4 — Observability & tracing infrastructure for agent fleets (54%)

Anchored by LTS×2, Tenable, TRM-Labs-adjacent, Rayda, Podium, Tide, SecurityScorecard, Amplitude, Flex (agent-trace visibility, sandbox runtime monitoring), Grafana, airSlate, Yuno (monitoring, tracing, alerting), PayPay Card, Honeycomb (real evals + production traffic), Teradata (instrument critical paths), Visa (Prometheus/Grafana observability).

Representative quotes:
- *"Continuously improve daily operations with automation, tooling, design evolution, and observability, including agent-trace visibility, evaluation pipelines, and sandbox runtime monitoring."* — Flex
- *"Build the monitoring, tracing, and alerting that keeps the platform healthy."* — Yuno
- *"Build and support monitoring and evaluation capabilities for GenAI systems, including usage, cost, reliability."* — PayPay Card
- *"Champion best practices for MLOps, agent evaluation, and system observability."* — Tenable

→ Covered by [`mod-402-eval-observability-infra/exercise-02-tracing-and-dashboards`](lessons/mod-402-eval-observability-infra/exercises/exercise-02-tracing-and-dashboards.md); OTel GenAI semantic conventions covered in the accompanying chapter. Deeper stable-trace-identity work sits at L48 [`mod-305-observability-tracing`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-305-observability-tracing).

### Theme 5 — Agent-specific code review / "set the bar" (50%)

Anchored by LTS, Lantern (set engineering standard, code reviews), SecurityScorecard (set the standard, drive architecture reviews), Tide (set standards for reliability/safety/scalability/DX), Podium, Flex (set the bar), Visa (set coding standards, lead design reviews), Teradata (set the technical bar in code review), Amplitude (set technical direction), FourKites (code reviews as team responsibility), GE Vernova (lead code quality), UKG (drive technical strategy), nCino (guide team members around best practices).

Representative quote: *"Write production-quality, modular, and well-tested code; set the technical bar through rigorous design and code reviews."* — Lantern

→ Covered by [`mod-405-technical-leadership/exercise-01-agent-code-review-standards`](lessons/mod-405-technical-leadership/exercises/exercise-01-agent-code-review-standards.md) — the module chapter explicitly targets the review-failure-modes that generic review misses (tool authority, prompt-injection surface, loop bounds, non-determinism).

### Theme 6 — Paved roads / shared services / platform templates (50%)

Anchored by LTS Senior Agentic (reusable frameworks), LTS Applied (partner with platform engineers), Tenable (Agentic AI Platform as a shared layer), Tide (context APIs, tool layers, policy controls as shared services), Amplitude (platform infrastructure beneath products), Flex (agent platform, MCP integrations, skill/tool registries), SecurityScorecard (define architecture), Podium (AI Agent platform), UKG (Agentic AI platform), Visa (multi-agent orchestration layer), PayPay Card (reusable platform templates, self-service, standard deployment patterns), Yuno (platform infrastructure), Teradata (agentic data layer as first-class product).

Representative quotes:
- *"Drive the design of shared services such as context APIs, tool layers, policy controls."* — Tide
- *"Build and maintain reusable platform templates, deployment patterns and integrations for GenAI applications … Provide self-service capabilities and standard deployment patterns for developers."* — PayPay Card
- *"Help establish engineering standards, reusable frameworks, and best practices across the AI engineering organization."* — LTS

→ Covered by [`mod-405-technical-leadership/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md) and [`mod-402-eval-observability-infra/04-paved-road-adoption.md`](lessons/mod-402-eval-observability-infra/04-paved-road-adoption.md) — "make eval/observability a paved road other engineers adopt because it's easier than not."

### Theme 7 — Reliability for agent systems in production (50%)

Anchored by Honeycomb (production traffic), Tenable (implicit reliability), Instabase (state machines with pausing/resuming/versioning trajectories), Podium (reliability in production), Tide (reliability/safety/scalability), Amplitude (real reliability constraints), Flex (reliability), Yuno (reliability), Scale AI (respond to incidents, RCA), Grafana (incident lifecycle), Teradata (SLOs, instrument critical paths, write runbooks, on-call), airSlate (LLM system reliability), UKG (production-grade), PayPay Card (reliability + recovery capabilities).

Representative quotes:
- *"Ensure your components are production-ready: define SLOs, instrument critical paths, write runbooks."* — Teradata
- *"Build reliable state machines capable of pausing, resuming, and versioning agent trajectories."* — Instabase
- *"Take one from rough first version to something that holds up under production traffic."* — Honeycomb
- *"Own the cloud infrastructure, automate provisioning with IaC, and ensure the platform scales reliably."* — Yuno

→ Covered by [`mod-404-reliability-cost-incident`](lessons/mod-404-reliability-cost-incident) (SLOs/SLIs for agents, quality drift, cost controls, incident response, postmortems) and [`mod-403-multi-agent-at-scale/03-durable-execution.md`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) (durable execution and resumption for long-running agent workloads).

### Theme 8 — Agent framework fluency (46%)

Anchored by LTS, FourKites (LangGraph non-negotiable), Rayda (LangGraph/CrewAI/AutoGen/OpenAI Agents SDK), Cresta (agent frameworks + RAG + function calling), Visa (LangChain/LangGraph/Autogen), Flex (LangGraph, custom planners, sub-agent patterns, MCP-based integrations), UKG (Google ADK, Anthropic Claude SDK, LangGraph), airSlate (agent orchestration), Amplitude (agent frameworks + evals + retrieval), Podium (implicit), Instabase (LLM orchestrators, tool-calling frameworks), Lantern (implicit).

→ Owned at L30 by [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) (build the same agent across LangGraph/CrewAI/AutoGen; benchmark OpenAI Agents SDK / Google ADK / Claude Agent SDK / smolagents). Named as a **prerequisite** in [`PREREQUISITES.md`](PREREQUISITES.md); this L40 track does not re-teach framework mechanics.

### Theme 9 — Guardrails, prompt injection, agent sandboxing (38%)

Anchored by LTS Senior Agentic (guardrails), Tenable (guardrails + safety), Instabase (guardrails against prompt injection + sandboxing agent-generated code), Rayda (guardrail mechanisms), Podium (guardrail strategies), Tide (safety), SecurityScorecard (implicit), Scale AI (sandboxing platform, Linux isolation primitives), Flex (sandbox runtime, Firecracker/gVisor), airSlate (LLM system reliability).

Representative quote: *"Engineer robust system-level guardrails to detect and mitigate prompt injection, defend against jailbreak attempts, and ensure strict compliance."* — Instabase

→ Basics owned at L30 by [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation) (I/O moderation, prompt-injection defenses, tool-permission enforcement, human-approval checkpoints). Architecture-level threat modeling owned at L48 by [`agentic-systems-architect-learning/mod-306-guardrails-safety-security`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-306-guardrails-safety-security). The L40 track's contribution is production hardening of tool + inter-agent seams in [`mod-403-multi-agent-at-scale/04-hardening-communication.md`](lessons/mod-403-multi-agent-at-scale/04-hardening-communication.md).

### Theme 10 — RAG pipelines, retrieval quality, embedding/rerank (35%)

Anchored by LTS Applied (RAG pipelines, retrieval, embeddings, reranking, grounding), Cresta (RAG), Visa (RAG), UKG (implicit), airSlate (RAG in production), Amplitude (retrieval), PayPay Card (RAG systems), SecurityScorecard (retrieval infrastructure), Lantern (advanced RAG pipelines).

→ Owned at L30 by [`agentic-ai-engineer-learning/mod-203-rag-and-memory`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-203-rag-and-memory) and by the [`rag-engineer-learning`](https://github.com/ai-engineering-curriculum/rag-engineer-learning) specialist track. Named as a **prerequisite**; this L40 track does not re-teach RAG pipeline mechanics.

### Theme 11 — Architecture ownership / build-vs-buy / prototype → production (31%)

Anchored by Amplitude (build-vs-buy calls, shape roadmap, "when to prototype, when to harden, when to invest in durable infrastructure"), Tenable (define roadmap, "from prototype to production-grade"), Instabase (align cross-functional engineering on technical roadmap), SecurityScorecard (define technical architecture, shape roadmap), Tide (define architecture for platform), UKG (drive technical strategy), Grafana (highly iterative process), Teradata (full technical ownership of an Agent Service), Honeycomb (rough prototype to production-grade), airSlate (beyond simple model usage to reliable systems).

Representative quote: *"Set technical direction for AI systems … making thoughtful build vs. buy calls, shaping evaluation strategy, and influencing the long-term roadmap."* — Amplitude

→ Covered by [`mod-401-agent-systems-in-practice`](lessons/mod-401-agent-systems-in-practice) — full module. Chapter `04-build-vs-buy-and-complexity.md` and [`exercise-03-prototype-to-production-refactor`](lessons/mod-401-agent-systems-in-practice/exercises/exercise-03-prototype-to-production-refactor.md).

### Theme 12 — Cost / latency / token budgets (31%)

Anchored by Instabase (context-window pruning + caching, "minimize round-trip latencies"), Tenable (implicit), Podium (implicit reliability includes cost/latency), Grafana (high-performance), Amplitude (implicit), airSlate (latency, cost), Yuno (implicit), Scale AI (cold-start latency, memory footprint), UKG (implicit), Visa (latency reduction, cost optimization), Flex (cost efficiency), PayPay Card (cost, reliability).

Representative quote: *"Implement advanced routing, context window pruning, and context caching strategies to optimize LLM token usage, minimize round-trip latencies."* — Instabase

→ Covered by [`mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md`](lessons/mod-403-multi-agent-at-scale/02-token-and-latency-budgets.md), [`exercise-03-token-and-latency-budgets`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-03-token-and-latency-budgets.md), and [`mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md`](lessons/mod-404-reliability-cost-incident/02-cost-controls-and-budgets.md) + [`exercise-02-cost-controls-in-production`](lessons/mod-404-reliability-cost-incident/exercises/exercise-02-cost-controls-in-production.md). Architecture-level token economics at L48 [`mod-307-cost-latency-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-307-cost-latency-architecture).

### Theme 13 — Regulated / compliance-heavy domain integration (31%)

Anchored by Tide (fintech / highly regulated), Visa (finance), UKG (HCM), Teradata (enterprise-governed data), Lantern (healthcare / Employer Direct Healthcare), Instabase (SOC/HIPAA compliance implied), Cresta (customer-facing regulated), PayPay Card (financial services in Japan), plus Bluefish AI (marketing regulated).

→ Architectural coverage sits at L48 [`agentic-systems-architect-learning/mod-309-governance-compliance-domain-architecture`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-309-governance-compliance-domain-architecture). This L40 build track surfaces domain constraints as "cost-of-being-wrong" framing on SLOs in [`mod-404-reliability-cost-incident/01-slos-and-slis-for-agents.md`](lessons/mod-404-reliability-cost-incident/01-slos-and-slis-for-agents.md); no L40-specific compliance module is warranted at build altitude.

### Theme 14 — Enterprise integration & secure tool auth (31%)

Anchored by Instabase (compliance), Tenable (JVM microservices integration layer), Podium (implicit), Tide (regulated / auth-heavy), Scale AI (implicit), Visa (Visa enterprise infrastructure), UKG (MCP servers into HCM), Flex (skill registries, MCP integrations), Teradata (enterprise-governed data), PayPay Card (secure and governed infrastructure).

→ Basics (OAuth 2.0 / RBAC for agent toolchains) owned at L30 by [`agentic-ai-engineer-learning/mod-206-guardrails-implementation`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation). Architecture-level in L48 [`mod-306/04-oauth-rbac-tokens.md`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/blob/main/lessons/mod-306-guardrails-safety-security/04-oauth-rbac-tokens.md).

## Themes just below threshold this cycle

### Durable execution / state machines (23%)

Anchored by Instabase (pausing/resuming/versioning trajectories), Tenable (workflow engines + HITL systems), Yuno (durable async messaging replacing sync patterns), Flex (implicit sandbox runtime), Scale AI (implicit isolation), plus TRM Labs (agent framework — near-edge of window).

→ Already covered by [`mod-403-multi-agent-at-scale/03-durable-execution.md`](lessons/mod-403-multi-agent-at-scale/03-durable-execution.md) and [`exercise-02-durable-execution-in-production`](lessons/mod-403-multi-agent-at-scale/exercises/exercise-02-durable-execution-in-production.md). No delta.

### MCP servers at scale (19%)

Anchored by Honeycomb (MCP server + Canvas Skills), Flex (MCP integrations), UKG (MCP servers into enterprise systems), Amplitude (MCP as part of ecosystem), Instabase (implicit tool-calling frameworks). 

→ Authoring already owned at L30 by [`agentic-ai-engineer-learning/mod-202-frameworks/exercises/exercise-04-mcp-tool-server`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks). If MCP-server-at-fleet-scale (multiple internal teams, auth-wrapped, versioned) crosses 30% next cycle, propose extending [`mod-405-technical-leadership/exercise-02-paved-roads-and-standards`](lessons/mod-405-technical-leadership/exercises/exercise-02-paved-roads-and-standards.md) with an MCP-catalog paved-road case study.

### Agent-runtime sandboxing / secure code execution (12%) — NEW EMERGING SIGNAL

Anchored by 3 postings:
- **Instabase** (*Software Engineer, Agent Harness*) — *"Design and scale highly secure, isolated, and ephemeral environments to execute agent-generated code safely without putting host infrastructure at risk."*
- **Scale AI** (*AI Infrastructure Engineer, Sandbox Platform*) — *"Deep understanding of Linux internals: process isolation, memory management, cgroups, namespaces."*
- **Flex** (*Staff SWE, AI Platform*) — *"Tech stack: … Modal, E2B, Cloudflare Sandboxes, Daytona, Firecracker/gVisor runtimes."*

Meets the 3-posting minimum but only 12% frequency, so **sub-threshold under continuity bias — no delta this cycle**. Distinct from the L30 mod-206 guardrails coverage: those postings are building the *sandbox platform* other agents consume, not consuming a sandbox. If this crosses 30% next cycle, the natural extension is a 5th exercise on secure agent-code execution runtimes inside [`mod-403-multi-agent-at-scale`](lessons/mod-403-multi-agent-at-scale) (its `04-hardening-communication.md` chapter is the nearest home).

External resources for learners interested now:
- E2B — https://e2b.dev/docs
- Modal sandboxes — https://modal.com/docs/guide/sandbox
- Daytona sandboxes — https://www.daytona.io/docs
- Cloudflare Sandbox — https://developers.cloudflare.com/durable-objects/
- Firecracker microVMs — https://firecracker-microvm.github.io/
- gVisor — https://gvisor.dev/docs/
- Anthropic Computer Use — https://docs.anthropic.com/en/docs/build-with-claude/computer-use

### AI-native dev tools as core work-style instrument (8%)

Anchored by SecurityScorecard (*"using AI-native development tools like Cursor and Claude Code as core instruments"*) and nCino (*"Leverage AI tools and techniques to enhance software development activities, including code generation, testing, debugging"*). Not curriculum-worthy for the agent-build track — this is a work-style expectation for engineers, not an agent-build skill. If it crosses 40% next cycle, add to [`PREREQUISITES.md`](PREREQUISITES.md) as an assumed entry expectation.

### Human-in-the-loop / approval boundaries (8%)

Anchored by Tenable (*"Design scalable workflow engines and 'human-in-the-loop' systems"*) and Podium (implicit via guardrails). Sub-threshold. Already covered at L30 by [`agentic-ai-engineer-learning/mod-206/exercises/exercise-04-human-approval-checkpoints`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-206-guardrails-implementation) and architecturally at L48 [`mod-308-deployment-durable-execution`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning/tree/main/lessons/mod-308-deployment-durable-execution).

## Out-of-scope / linked-out themes

For requirements that would belong at another rung per the ownership rule, we link out rather than duplicating.

| Theme | Link |
|---|---|
| Agent framework mechanics (LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Claude Agent SDK) | [`agentic-ai-engineer-learning/mod-202-frameworks`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning/tree/main/lessons/mod-202-frameworks) |
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

<!-- needs-research: monitor agent-runtime sandboxing (Firecracker/gVisor/E2B/Modal/Daytona/Cloudflare-Sandboxes) frequency in the next cycle. Also watch MCP-server-at-fleet-scale (auth-wrapped, versioned, multi-team) as MCP-authoring adoption climbs. Both are the most credible candidates for the first mod-403 or mod-405 exercise addition; both are sub-threshold today. -->

The `mod-401..405` build spine covers every job-market requirement that clears the continuity-bias thresholds at L40 altitude. Framework/RAG/single-agent-eval/guardrail-implementation fundamentals stay owned by the L30 `agentic-ai-engineer-learning` track and are named as prerequisites; architecture-level design (topology design, memory architecture, threat modeling, cost architecture, governance) stays owned by the L48 `agentic-systems-architect-learning` track and is linked as the natural follow-on. **No delta is proposed this cycle.** Re-run on the next quarterly cycle (2026-11) to catch shifts in agent-runtime sandboxing, MCP-at-fleet-scale, and any hardening of "AI-native dev-tool fluency" from a work-style expectation into a testable engineering skill.
