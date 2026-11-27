# PROJECT ATLAS

### v2 · Enterprise Applied AI Engineering & Developer Enablement Residency

> **43 weeks** · **172 sessions** · **344 hours** · 4 × 2 hours per week

| Engineering | Enablement | Reserve |
|---:|---:|---:|
| 260 hours | 78 hours | 6 hours |

**Companion to:** `PROJECT_ATLAS_MASTER_SPECIFICATION.md` v2.0. **Start:** resume ATL-001; do not redo verified repository setup. **Cadence:** 4 × 120 minutes/week; 172 sessions, 344 hours. 260 engineering hours (G), 78 enablement hours (E), 6 reserve hours (B). Calendar weeks are relative to the restart, not dates. This is a proposed execution schedule, not a change to customer requirements or a guarantee of finishing in 43 weeks.

## Navigation

- [Operating protocol](#operating-protocol)
- [Phase gates and dependencies](#phase-gates-and-dependencies)
- [Schedule](#schedule)
  - [Phase 01 · Engineering foundations](#phase-01--engineering-foundations)
  - [Phase 02 · Enterprise data and integrations](#phase-02--enterprise-data-and-integrations)
  - [Phase 03 · Distributed systems engineering](#phase-03--distributed-systems-engineering)
  - [Phase 04 · Advanced agent orchestration](#phase-04--advanced-agent-orchestration)
  - [Phase 05 · AI evaluation and security](#phase-05--ai-evaluation-and-security)
  - [Phase 06 · Production engineering](#phase-06--production-engineering)
  - [Phase 07 · Professional readiness](#phase-07--professional-readiness)
- [Reference index](#reference-index--targeted-reading)
- [Coverage and release discipline](#coverage-and-release-discipline)
- [Session record template](#session-record-template)


## Operating protocol

- One evolving Atlas repository and synthetic Meridian engagement. No parallel toy projects; isolated spikes become tests, ADR evidence or teaching demos. First customer one-pager is independently authored. Preserve the original transcript.
- Each ordinary session: 10 min opening recall, 15 min focused learning, 80 min flexible engineering or enablement work, 15 min closing check-in including tests/evidence and log. Use the weekly daily check-ins in order, but treat implementation assignments as a weekly backlog rather than fixed daily deadlines. Special assessment/workshop timing below takes precedence; embed check-ins in those blocks, not extra time. Reserve sessions remain reserve; use prompts only if studying. For assessment sessions use the explicit 30/30/30/30 split instead; workshops may use 40 min preparation, 30 min delivery, 25 min Q&A/failure, 25 min feedback. No extra homework assumed. Split unfinished work into the next session; never mark an unverified task done.
- Default Learning Mode for protected components; ask mentor for hints and review, not implementations. Collaborative/Professional only when explicitly authorized; protected rules in AGENTS.md remain binding. No automatic commit, push, deploy or publish. External service and commercial admin access are prerequisites to real demonstrations; label simulations and blocked work distinctly.
- Before every implementation: specify input/output, failure case and test; after implementation: run targeted tests and explain code without AI. Every week capture actual hours, PR/commit or artifact path, test output, decision, open risks, next task in PROGRESS.md and BACKLOG.md. Use existing backlog IDs where applicable; create new IDs only as needed.
- Use the referenced reading selectively; do not read entire manuals or books. Pin versions and note doc access date. Read relevant docs again when products change. Every four weeks score all master-spec competencies 0–3 (0 cannot explain, 1 with help, 2 independent implementation, 3 independent diagnosis and trade-offs); record evidence and next remediation. For unobserved competencies mark not assessed, not zero. Revisit earlier topics during recall. No senior-title or hiring guarantee.
- Weekly spend check; local mock inference for load. Verify AWS access and cost before provisioning, smallest short-lived staging, approved teardown, check inventory; budget alerts are not caps. Synthetic data and dedicated keys only. Never use employer material.
- **Pacing gate:** 6 hours is a small reserve, not enough for every unknown. At weeks 4, 12, 24, 36 compare actual effort and exit criteria; defer optional framework adoption, extra demos or polishing before sacrificing protected work. If still behind, extend calendar with four sessions/week; do not silently compress or skip. Unresolved security or customer prerequisites block affected downstream work; work on independent tasks while waiting.

## Phase gates and dependencies

| Gate | Planned week | Required evidence before moving forward |
|---|---:|---|
| Discovery and skeleton | 2 | One-pager, technical discovery, approved scope and trust boundaries, API contract, runnable tests/CI; no DB or cloud yet |
| Read-only vertical slice | 6 | End-to-end tool investigation, initial eval/security cases, explicit abstention, stakeholder review; separate enablement mandate |
| Data and security | 12 | Durable storage, retrieval, MCP, OIDC and tenant ACL tests; deny paths proven before greater exposure |
| Reliability | 17 | Baseline, cache/limiter, job lease, retries and replay tests; provider comparison |
| Workflow safety | 23 | Restartable state, bounded tools, separately authorized sandbox approvals, deterministic denial and audit |
| Quality | 28 | Held-out 40 cases, target ≥85% provisional task success, independent safety gates, point-in-time shadow simulation; no real pilot claims |
| Operations and staging | 36 | Trace/runbooks, IaC deployment evidence or documented access blocker, load and recovery results, release decision |
| Handoff | 43 | F1–F8 traceability, customer acceptance simulation, six workshops and adoption/portfolio artifacts, final assessments and teardown |

## Schedule

Use the weekly concepts and terms during the existing reading and recall blocks. Answer the knowledge checkpoint from memory and use the session evidence to verify the learning objective; no additional hours are allocated.

Each numbered session is exactly two planned hours. The numbered assignments are suggested sequencing, not fixed daily deadlines; preserve dependencies, G/E/B allocations and gates. The actionable assignment includes its evidence; record actual outcomes rather than assuming success. G includes customer discovery, implementation, design, security, assessment, operations and engineering documentation. E covers developer enablement and teaching; some G sessions naturally build evidence used by E. B is protected scheduling reserve.

---

## Phase 01 — Engineering foundations

### Week 01 — Discovery and contract

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Discovery distinguishes business outcomes from implementation choices; define scope and measurable acceptance.

#### Terms to know

| Term | Definition |
|---|---|
| **Elicitation** | systematic extraction of requirements |
| **NFR** | quality or operational constraint |
| **ADR** | record of a design decision |
| **trust boundary** | point where trust assumptions change |
| **MTTR** | mean time to resolve |

**Learning objective:** Translate stakeholder needs into a contract and identify unresolved decisions.

> **Knowledge checkpoint · Without AI**
>
> Why is diagnosis time primary, and which requirements block design?

**Reading:** R1, R2 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: How would you distinguish a requirement from a proposed solution? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why not promise MTTR improvement before a pilot? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A stakeholder asks for automatic remediation: what must be clarified before changing scope? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the pilot success criteria to Finance. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Finish independent one-pager; compare transcript and list missing requirements with owners.
- [ ] **Session 2 · G · 2h:** Run technical discovery on incident categories, triggers, access, latency, budget and acceptance; log unresolved decisions.
- [ ] **Session 3 · G · 2h:** Draw context and trust boundaries; write modular-monolith ADR and request/response contract.
- [ ] **Session 4 · E · 2h:** Verify existing repo setup and independently start FastAPI health endpoint; record curl evidence.

---

### Week 02 — Walking skeleton

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Typed API contracts and asynchronous request handling; automated checks establish a reproducible baseline.

#### Terms to know

| Term | Definition |
|---|---|
| **Pydantic** | typed data validation library |
| **coroutine** | suspendable async computation |
| **event loop** | scheduler for async tasks |
| **cancellation** | request to stop a task |
| **CI** | automated integration checks |

**Learning objective:** Implement and test a typed endpoint and explain cancellation.

> **Knowledge checkpoint · Without AI**
>
> What happens when an async request is cancelled during I/O?

**Reading:** R3, R4, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes async I/O from CPU parallelism? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why validate requests at the API boundary? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A slow dependency blocks unrelated requests: how would you investigate? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Sketch request validation, cancellation and error handling. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement typed investigation stub and error mapping; test malformed requests.
- [ ] **Session 2 · G · 2h:** Finish unit tests and CI lint/type/test checks; demonstrate fresh clone and review request lifecycle.
- [ ] **Session 3 · G · 2h:** Study asyncio cancellation and HTTP lifecycle; implement small async experiment in tests.
- [ ] **Session 4 · E · 2h:** Set up Claude Code in sandbox; inspect instruction precedence and permissions; demonstrate protected-file boundary.

---

### Week 03 — Claude API

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Provider abstraction isolates model-specific behavior; bounded calls protect latency and budget.

#### Terms to know

| Term | Definition |
|---|---|
| **Messages API** | structured model conversation interface |
| **token** | unit of model input/output |
| **context window** | maximum supported context |
| **streaming** | incremental response delivery |
| **429** | rate-limit response |

**Learning objective:** Implement a provider client and classify failures.

> **Knowledge checkpoint · Without AI**
>
> Which failures should be retried, and why must calls have timeouts?

**Reading:** R4, R6 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is the difference between input and output tokens? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: When is streaming useful versus a complete response? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A provider returns 429 then times out: what should the client do? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain provider abstraction and its limits. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Read Messages API and async SDK; independently implement provider client and typed response mapping.
- [ ] **Session 2 · G · 2h:** Handle timeout, rate-limit and malformed outputs with mocked tests; run one budgeted live call.
- [ ] **Session 3 · G · 2h:** Study token/context budgets and streaming; document error taxonomy and provider contract.
- [ ] **Session 4 · E · 2h:** Practice Claude Code navigation, context reset and read-only review; compare output to own review.

---

### Week 04 — Tool contracts

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Typed tool interfaces separate untrusted inputs from authorized operations; fixtures preserve evidence provenance.

#### Terms to know

| Term | Definition |
|---|---|
| **JSON Schema** | structure constraints for JSON |
| **fixture** | controlled test input |
| **provenance** | origin and history of evidence |
| **tool registry** | allowed callable tools |
| **prompt injection** | untrusted content attempting to steer a model |

**Learning objective:** Design a validated read-only connector contract.

> **Knowledge checkpoint · Without AI**
>
> Why does schema validation alone not authorize a tool call?

**Reading:** R7, R8 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is the difference between validation and authorization? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why should tool outputs be treated as untrusted? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A valid tool request targets another tenant: where should it fail? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the connector contract to a security reviewer. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Define incident and evidence types; build synthetic ticket and telemetry fixtures with timestamps.
- [ ] **Session 2 · G · 2h:** Implement read-only mock REST endpoints and typed connector client; add timeout and denial tests.
- [ ] **Session 3 · G · 2h:** Design tool registry, schemas and failure responses; map trust boundaries and injection entry points.
- [ ] **Session 4 · G · 2h:** Assessment 1: 30m no-AI typed async task, 30m design defense, 30m failure diagnosis, 30m evidence and scores.

---

### Week 05 — Bounded agent

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Bounded agent loops alternate model decisions and validated tool execution; abstention is a valid result.

#### Terms to know

| Term | Definition |
|---|---|
| **Tool dispatch** | selection and invocation of a registered tool |
| **stop reason** | why model generation ended |
| **step budget** | maximum execution iterations |
| **abstention** | declining unsupported conclusions |
| **grounding** | linking claims to evidence |

**Learning objective:** Implement a native loop with deterministic limits.

> **Knowledge checkpoint · Without AI**
>
> How do you prevent an agent from looping or inventing evidence?

**Reading:** R6, R7 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes an agent loop from a fixed workflow? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why bound tool calls and token usage separately? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: The model repeats the same tool call: how should execution stop? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain how evidence and abstention are represented. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Independently implement tool registry dispatch and reject unknown names or invalid args.
- [ ] **Session 2 · G · 2h:** Implement bounded native agent loop; test stop, max steps, tool failure and abstention.
- [ ] **Session 3 · G · 2h:** Build evidence-linked report with structured diagnosis and no workaround suggestions; test insufficient evidence.
- [ ] **Session 4 · E · 2h:** Prepare workshop 1 demo and exercises; deliver 30m Claude and agentic engineering practice with Q&A and failure recovery.

---

### Week 06 — Prototype gate

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Vertical slices test the whole path early; regression and security checks precede exposure.

#### Terms to know

| Term | Definition |
|---|---|
| **Vertical slice** | end-to-end minimal functionality |
| **regression** | test for previously working behavior |
| **correlation ID** | identifier linking related events |
| **hook** | callback triggered by a lifecycle event |
| **release gate** | condition required to advance |

**Learning objective:** Demonstrate a read-only investigation and its failure paths.

> **Knowledge checkpoint · Without AI**
>
> What evidence would justify proceeding beyond the prototype?

**Reading:** R7, R9 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a vertical slice? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is a successful demo not a release gate? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: The prototype gives a plausible answer with no evidence: what is your decision? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Present the prototype limits and next gate. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Connect API, agent and mock systems; test end-to-end incident with traceable ID.
- [ ] **Session 2 · G · 2h:** Write initial development eval cases including injection, missing evidence and out-of-scope; run regression.
- [ ] **Session 3 · G · 2h:** Demo to Meridian; record acceptance, risks and separate developer enablement authorization; no real incident claims.
- [ ] **Session 4 · E · 2h:** Claude Code hooks lab: block protected operations in sandbox, test failure behavior; log actual vs simulated controls.

---

## Phase 02 — Enterprise data and integrations

### Week 07 — Persistence

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Relational persistence and transaction boundaries protect state across failures.

#### Terms to know

| Term | Definition |
|---|---|
| **ACID** | atomicity consistency isolation durability |
| **migration** | versioned schema change |
| **rollback** | undo of uncommitted changes |
| **index** | data structure accelerating lookup |
| **isolation level** | visibility rules for concurrent transactions |

**Learning objective:** Implement repository operations with atomic updates.

> **Knowledge checkpoint · Without AI**
>
> What happens if a process crashes before commit?

**Reading:** R10, R11 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What are atomicity and isolation? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why use a transaction rather than two independent writes? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A crash occurs between state updates: what should recovery observe? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain repository boundaries and rollback. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Study SQL transactions and schema design; create PostgreSQL compose service and migrations.
- [ ] **Session 2 · G · 2h:** Independently implement repository and transaction boundaries for runs and evidence.
- [ ] **Session 3 · G · 2h:** Test rollback, restart and concurrent updates; document state ownership and indexes.
- [ ] **Session 4 · E · 2h:** Build Claude Code skill for reviewing incident fixtures; test instructions and forbidden operations.

---

### Week 08 — Retrieval ingestion

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Retrieval quality depends on ingestion, representation and ranking.

#### Terms to know

| Term | Definition |
|---|---|
| **Embedding** | numeric representation of content |
| **chunking** | splitting documents into retrieval units |
| **vector distance** | measure of embedding dissimilarity |
| **top-k** | highest ranked k results |
| **pgvector** | PostgreSQL vector extension |

**Learning objective:** Build versioned ingestion and evidence-linked retrieval.

> **Knowledge checkpoint · Without AI**
>
> How do chunk size and duplicate documents affect retrieval?

**Reading:** R11, R12 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes an embedding from a chunk? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why version source documents and preserve provenance? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A runbook changes after ingestion: how do you detect stale evidence? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain retrieval quality versus generation quality. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement document ingestion with source IDs, version and ACL metadata; test duplicate inputs.
- [ ] **Session 2 · G · 2h:** Select embedding provider/local model; implement chunking and embedding with budget and deterministic test doubles.
- [ ] **Session 3 · G · 2h:** Study pgvector distance and ranking; implement top-k retrieval with citations and no-evidence behavior.
- [ ] **Session 4 · G · 2h:** Assessment 2: no-AI transaction task, retrieval design defense, diagnose duplicate ingestion; score and remediate.

---

### Week 09 — Retrieval authorization

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Authorization must constrain retrieval before model exposure; measure relevance separately from access.

#### Terms to know

| Term | Definition |
|---|---|
| **ACL** | access control list |
| **tenant** | isolated organizational scope |
| **principal** | authenticated actor |
| **recall** | proportion of relevant items retrieved |
| **distractor** | irrelevant competing evidence |

**Learning objective:** Implement permission-aware retrieval and leakage tests.

> **Knowledge checkpoint · Without AI**
>
> Why is filtering after model generation unsafe?

**Reading:** R12, R13 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is the difference between authentication and authorization? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why filter retrieval before model exposure? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Two tenants have near-identical documents: design a leakage test. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain how permissions propagate from request to retrieval. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement filter-before-retrieval using synthetic principal and tenant ACLs; test denied documents.
- [ ] **Session 2 · G · 2h:** Create retrieval fixtures with distractors, stale documents and leakage attempts; measure recall and citation validity.
- [ ] **Session 3 · G · 2h:** Compare chunking and ranking options; write ADR with measured trade-offs and limitations.
- [ ] **Session 4 · E · 2h:** Configure Claude Code subagent for read-only review; compare findings and context cost; document scope.

---

### Week 10 — MCP integration

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

MCP standardizes tool discovery and invocation but does not replace authorization.

#### Terms to know

| Term | Definition |
|---|---|
| **MCP** | Model Context Protocol |
| **transport** | mechanism carrying protocol messages |
| **capability negotiation** | agreement on supported features |
| **tool schema** | declared tool input structure |
| **plugin** | packaged reusable extension |

**Learning objective:** Build and test an MCP adapter and compare REST.

> **Knowledge checkpoint · Without AI**
>
> Where should authorization be enforced when MCP exposes a tool?

**Reading:** R14, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What are MCP tools and transport? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: When would REST be simpler than MCP? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: An MCP server advertises a tool the caller cannot use: what happens? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain MCP lifecycle and authorization boundaries. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Read MCP lifecycle and tool schema; build minimal sandbox server wrapping ticket tools.
- [ ] **Session 2 · G · 2h:** Implement client adapter with typed validation, timeout and disconnect handling; compare REST.
- [ ] **Session 3 · G · 2h:** Test untrusted tool output, auth boundary and connector failure; document transport trade-offs.
- [ ] **Session 4 · E · 2h:** Package safe skill/hook/MCP configuration as plugin; test install in disposable repo.

---

### Week 11 — Identity

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Identity proves who acts; authorization determines permitted actions.

#### Terms to know

| Term | Definition |
|---|---|
| **OIDC** | identity layer over OAuth 2.0 |
| **JWT** | signed or encrypted token format |
| **JWKS** | published JSON public key set |
| **issuer** | token issuing authority |
| **audience** | intended token recipient |
| **RBAC** | role-based access control |

**Learning objective:** Validate tokens and propagate principals to tools.

> **Knowledge checkpoint · Without AI**
>
> Why must signature, issuer, audience and expiry all be checked?

**Reading:** R13, R14 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes an ID token from an access token? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is decoding a JWT not validation? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A correctly signed token has the wrong audience: what should happen? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain OIDC and SCIM without conflating them. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Run Keycloak locally; inspect OIDC discovery, claims and JWKS; configure test tenant.
- [ ] **Session 2 · G · 2h:** Implement token validation with established library; reject expired, wrong audience/issuer and invalid signatures.
- [ ] **Session 3 · G · 2h:** Implement RBAC and principal propagation into retrieval/tools; cross-tenant denial tests.
- [ ] **Session 4 · E · 2h:** Deliver workshop 2: MCP integration with broken auth demo, exercise and Q&A; save facilitator notes.

---

### Week 12 — Security gate

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Defense in depth requires testing bypasses and tenant isolation end to end.

#### Terms to know

| Term | Definition |
|---|---|
| **Least privilege** | minimum necessary access |
| **horizontal privilege escalation** | access to another peer's resources |
| **direct API bypass** | avoiding intended UI or workflow controls |
| **residual risk** | risk remaining after controls |
| **negative test** | test of prohibited behavior |

**Learning objective:** Demonstrate denial paths and defend trust boundaries.

> **Knowledge checkpoint · Without AI**
>
> How could a direct API request bypass an otherwise secure UI?

**Reading:** R13, R9 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is deny by default? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is a UI permission check insufficient? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A revoked user has cached access: how would you test the boundary? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend the security gate with negative test evidence. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Test direct API bypass, ACL leakage, tool argument tampering and logs; close critical failures.
- [ ] **Session 2 · G · 2h:** Integrate permission-aware investigation end-to-end; test authorized vs denied requests.
- [ ] **Session 3 · G · 2h:** Review identity and retrieval architecture with CISO; document residual risks and approval status.
- [ ] **Session 4 · G · 2h:** Assessment 3: no-AI policy task, trust-boundary defense, diagnose auth failure; record scores.

---

## Phase 03 — Distributed systems engineering

### Week 13 — Performance baseline

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Measure before optimizing; throughput, concurrency and latency are distinct.

#### Terms to know

| Term | Definition |
|---|---|
| **p95** | 95th percentile latency |
| **throughput** | completed work per time |
| **Little's law** | average work in system equals arrival rate times average time in stable systems |
| **connection pool** | reusable connections |
| **query plan** | database execution strategy |

**Learning objective:** Produce reproducible baseline and identify bottlenecks.

> **Knowledge checkpoint · Without AI**
>
> Why can average latency hide a serious performance problem?

**Reading:** R15, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes p50 from p95? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why measure throughput and latency together? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Latency rises under load but CPU is low: what evidence would you collect? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the benchmark workload and limitations. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Use Locust with mocked inference; measure latency, throughput, errors and concurrency.
- [ ] **Session 2 · G · 2h:** Profile async calls and SQL query plans; identify bottleneck with reproducible workload.
- [ ] **Session 3 · G · 2h:** Study Little’s law, pooling and tail latency; compare baseline against 10 rps and acceptance target.
- [ ] **Session 4 · E · 2h:** Timed prototype 1: build non-protected CI failure demo using Claude Code; present limits and record elapsed time.

---

### Week 14 — Cache and limits

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Caching trades freshness for speed; distributed limits require atomic state changes.

#### Terms to know

| Term | Definition |
|---|---|
| **TTL** | time to live |
| **invalidation** | removing stale cached data |
| **cache hit** | request served from cache |
| **race condition** | outcome depends on execution timing |
| **atomic operation** | indivisible state change |
| **rate limiter** | control on request frequency |

**Learning objective:** Implement tenant-safe cache and limiter.

> **Knowledge checkpoint · Without AI**
>
> How can a cache leak data across principals?

**Reading:** R17, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a cache key and TTL? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why must a rate limiter update atomically? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A shared cache returns another user's result: identify the missing boundary. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain cache invalidation and tenant-safe limiting. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Design cache keys including tenant/auth context and invalidation policy; test stale/denied data.
- [ ] **Session 2 · G · 2h:** Implement cache policy and atomic limiter using Redis/Valkey primitives; race and expiry tests.
- [ ] **Session 3 · G · 2h:** Benchmark cache hit/miss and limiter under concurrent load; document trade-offs.
- [ ] **Session 4 · E · 2h:** Claude Code headless sandbox run and CI review demo; enforce no secrets or unauthorized edits.

---

### Week 15 — Bedrock

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Cloud inference changes authentication and operations while provider interfaces preserve portability.

#### Terms to know

| Term | Definition |
|---|---|
| **Bedrock** | AWS managed model service |
| **IAM** | AWS identity and access management |
| **inference profile** | model invocation routing configuration |
| **quota** | service usage limit |
| **provider adapter** | translation layer for a model service |

**Learning objective:** Compare direct API and Bedrock with tested adapter.

> **Knowledge checkpoint · Without AI**
>
> Which differences cannot safely be hidden behind a provider abstraction?

**Reading:** R18, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes Bedrock IAM from direct API credentials? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why compare model capabilities rather than names alone? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: One provider throttles differently: how should the adapter expose that? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain provider portability and its limitations. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Verify AWS account, region, model access, IAM and spend controls; no infrastructure deployment yet.
- [ ] **Session 2 · G · 2h:** Implement Bedrock adapter behind own provider interface; mock errors and run budgeted smoke test if access allows.
- [ ] **Session 3 · G · 2h:** Compare direct API vs Bedrock auth, quotas, streaming, cost and capabilities; record ADR.
- [ ] **Session 4 · E · 2h:** Configure Claude Code Bedrock path if supported; demonstrate differences and record blocker if unavailable.

---

### Week 16 — Job queue

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Durable jobs decouple request acceptance from execution; leases coordinate workers.

#### Terms to know

| Term | Definition |
|---|---|
| **Lease** | time-limited claim on work |
| **worker** | background task executor |
| **polling** | repeated status checks |
| **at-least-once** | delivery may repeat |
| **row lock** | database concurrency control |

**Learning objective:** Implement claim and restart recovery.

> **Knowledge checkpoint · Without AI**
>
> What happens when a worker dies after claiming a job?

**Reading:** R10, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a job lease? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why acknowledge only after durable completion? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A worker dies after claiming work: describe recovery and duplicate risk. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain queue state transitions and recovery evidence. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Study delivery semantics and leases; design job schema and status transitions.
- [ ] **Session 2 · G · 2h:** Implement PostgreSQL claim using short transactions and lease expiry; concurrent worker tests.
- [ ] **Session 3 · G · 2h:** Implement status endpoint and worker loop; demonstrate restart and expired-lease recovery.
- [ ] **Session 4 · G · 2h:** Assessment 4: no-AI concurrency task, queue design defense, diagnose stuck job; score and review schedule.

---

### Week 17 — Retries and idempotency

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Retries must be bounded and safe under duplicate delivery.

#### Terms to know

| Term | Definition |
|---|---|
| **Backoff** | increasing delay between retries |
| **jitter** | randomized delay |
| **idempotency** | repeating operation has same intended effect |
| **DLQ** | dead-letter queue |
| **transactional outbox** | durable event record committed with business state |

**Learning objective:** Implement retry and replay behavior.

> **Knowledge checkpoint · Without AI**
>
> Why can a timeout leave the outcome of a write uncertain?

**Reading:** R16, R19 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes backoff from jitter? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why does a timeout not prove failure? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A write succeeds but its response is lost: design safe replay. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain idempotency and dead-letter handling. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Classify transient/permanent errors; implement bounded retry with backoff and jitter; fake-clock tests.
- [ ] **Session 2 · G · 2h:** Implement idempotency key semantics, conflict and replay tests; simulate crash between side effect and commit.
- [ ] **Session 3 · G · 2h:** Implement dead-letter state and operator replay; compare SQS semantics and outbox pattern.
- [ ] **Session 4 · E · 2h:** Deliver workshop 3: Claude Code complex repo, context and debugging; deliberate failing CI demo.

---

## Phase 04 — Advanced agent orchestration

### Week 18 — Durable state

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Explicit persisted state makes workflow recovery predictable.

#### Terms to know

| Term | Definition |
|---|---|
| **State machine** | states and allowed transitions |
| **invariant** | condition that must remain true |
| **checkpoint** | persisted progress marker |
| **optimistic concurrency** | version check before update |
| **replay** | reprocessing recorded work |

**Learning objective:** Implement restartable state transitions.

> **Knowledge checkpoint · Without AI**
>
> Which state must be persisted before acknowledging progress?

**Reading:** R16, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a durable checkpoint? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why persist state before acknowledging progress? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A crash occurs between tool completion and state update: what can be replayed? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain restart semantics and state invariants. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Define explicit workflow states, invariants and versioned transitions; draw state diagram.
- [ ] **Session 2 · G · 2h:** Implement persisted transitions and resume behavior; inject worker death at each boundary.
- [ ] **Session 3 · G · 2h:** Test invalid transitions, stale leases and repeated delivery; explain recovery guarantees.
- [ ] **Session 4 · E · 2h:** Study enterprise admin setup, settings precedence and network controls; draft local versus managed control matrix.

---

### Week 19 — Parallel tools

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Parallel execution reduces latency but introduces cancellation and partial failure.

#### Terms to know

| Term | Definition |
|---|---|
| **Fan-out** | dispatch to multiple tasks |
| **fan-in** | combine task results |
| **semaphore** | bounded concurrency primitive |
| **dependency graph** | ordering constraints between tasks |
| **partial failure** | some operations fail while others succeed |

**Learning objective:** Implement bounded parallel calls with explicit failure policy.

> **Knowledge checkpoint · Without AI**
>
> When should one failed tool cancel other tasks?

**Reading:** R4, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is bounded concurrency? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why distinguish independent and dependent tasks? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: One parallel tool fails while others succeed: choose a failure policy. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain cancellation and partial results. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Map tool dependencies; independently implement bounded parallel calls with timeout/cancellation.
- [ ] **Session 2 · G · 2h:** Persist partial results and define failure policy; test cancellation and dependent tool failure.
- [ ] **Session 3 · G · 2h:** Benchmark sequential vs parallel on same fixtures; defend resource and correctness trade-offs.
- [ ] **Session 4 · E · 2h:** Draft developer pilot discovery: cohorts, champions, baseline productivity and risk measures; simulate customer review.

---

### Week 20 — Approval sandbox

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Human approval must bind an authenticated actor to a specific action.

#### Terms to know

| Term | Definition |
|---|---|
| **Payload digest** | hash of action content |
| **approval expiry** | time limit on authorization |
| **replay attack** | reuse of previously valid request |
| **separation of duties** | division of sensitive responsibilities |
| **fail closed** | deny when verification fails |

**Learning objective:** Implement and test exact-payload sandbox approvals.

> **Knowledge checkpoint · Without AI**
>
> Why must changing an approved payload invalidate approval?

**Reading:** R13, R9 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is an exact-payload approval? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why must approval expire or be invalidated? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A payload changes after approval: identify the required denial. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the sandbox boundary and human authority. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Confirm separate authorization for sandbox mutation phase; define action payload binding and expiry.
- [ ] **Session 2 · G · 2h:** Implement approval state transitions with authenticated approver and exact payload digest using standard crypto.
- [ ] **Session 3 · G · 2h:** Test replay, changed payload, expired approval, wrong role and denied production target.
- [ ] **Session 4 · G · 2h:** Assessment 5: no-AI state transition task, approval defense, diagnose replay; record evidence.

---

### Week 21 — Mutation reliability

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Reliable mutation requires reconciliation when remote outcomes are uncertain.

#### Terms to know

| Term | Definition |
|---|---|
| **Side effect** | external state change |
| **reconciliation** | compare and repair inconsistent state |
| **deduplication** | detect repeated operations |
| **exactly-once** | one effective execution under stated guarantees |
| **audit event** | record of accountable activity |

**Learning objective:** Recover from crash after mock mutation without duplicate effect.

> **Knowledge checkpoint · Without AI**
>
> Why does a queue alone not guarantee exactly-once side effects?

**Reading:** R19, R13 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is an outbox? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is at-least-once delivery not exactly-once effect? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A worker crashes after mutation but before acknowledgement: trace recovery. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain deduplication and reconciliation. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement mock idempotent downstream and audit event for approved action; keep V1 read-only.
- [ ] **Session 2 · G · 2h:** Inject crash after mock write; reconcile result without duplicate action; test uncertain outcome.
- [ ] **Session 3 · G · 2h:** Compare transactional outbox and reconciliation; document limits of exactly-once claims.
- [ ] **Session 4 · E · 2h:** Enterprise identity lab: map SAML/OIDC/SCIM, joiner/mover/leaver and revocation; simulate where admin access absent.

---

### Week 22 — Orchestration review

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Framework adoption should follow measured needs rather than fashion; governance spans people and tools.

#### Terms to know

| Term | Definition |
|---|---|
| **LangGraph** | graph-based agent orchestration framework |
| **Temporal** | durable workflow platform |
| **orchestration** | coordination of task execution |
| **managed policy** | centrally enforced configuration |
| **SOC 2** | assurance reporting framework |
| **HIPAA** | US health information law and rules |

**Learning objective:** Defend adopt/defer decision and governance matrix.

> **Knowledge checkpoint · Without AI**
>
> What concrete evidence would justify replacing native orchestration?

**Reading:** R20, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is workflow replay? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why compare native orchestration before adopting a framework? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A framework hides a retry boundary: what evidence would justify adoption? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend the adopt/defer ADR. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Compare native state machine against LangGraph/Temporal requirements; run minimal sandbox spike.
- [ ] **Session 2 · G · 2h:** Measure complexity and recovery behavior; write adopt/defer ADR, no mandatory rewrite.
- [ ] **Session 3 · G · 2h:** Review native workflow and repair outstanding reliability failures; demonstrate restart and replay.
- [ ] **Session 4 · E · 2h:** Build governance matrix for permissions, connectors, retention, spend, audit, SOC2/HIPAA considerations without compliance claims.

---

### Week 23 — Secure adoption

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Secure adoption requires deterministic enforcement and useful audit records.

#### Terms to know

| Term | Definition |
|---|---|
| **Red teaming** | adversarial testing |
| **audit trail** | chronological accountable record |
| **redaction** | removal of sensitive content |
| **compensating control** | alternative risk mitigation |
| **egress** | outbound network traffic |

**Learning objective:** Test approval and audit controls and teach their limits.

> **Knowledge checkpoint · Without AI**
>
> What must an audit event contain to reconstruct an action?

**Reading:** R9, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is an audit event? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why distinguish administrative policy from runtime enforcement? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: An administrator disables a safeguard: what evidence and controls matter? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Teach approval limits and enterprise governance. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Red-team sandbox tool paths and approval enforcement; verify read-only production configuration.
- [ ] **Session 2 · G · 2h:** Inspect log redaction and actor/run/tool/approval audit fields; test missing events.
- [ ] **Session 3 · G · 2h:** Review architecture with simulated security lead; track risks, compensating controls and owners.
- [ ] **Session 4 · E · 2h:** Deliver workshop 4: enterprise secure adoption with policy exercise and deliberate permission failure.

---

## Phase 05 — AI evaluation and security

### Week 24 — Evaluation design

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Evaluation design separates task quality, evidence and safety; holdout isolation prevents overfitting.

#### Terms to know

| Term | Definition |
|---|---|
| **Rubric** | explicit scoring criteria |
| **held-out set** | cases reserved from tuning |
| **judge calibration** | checking evaluator agreement with human labels |
| **data leakage** | unintended access to evaluation information |
| **safety gate** | independent mandatory safety criterion |

**Learning objective:** Build versioned eval runner and defensible scoring.

> **Knowledge checkpoint · Without AI**
>
> Why must safety failures not be averaged away by high accuracy?

**Reading:** R21, R7 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes a rubric from a test fixture? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why separate safety gates from task accuracy? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Two reviewers disagree on diagnosis quality: how should scoring proceed? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain eval reproducibility and versioning. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Define taxonomy, task rubric, evidence validity, abstention and safety gates with stakeholders.
- [ ] **Session 2 · G · 2h:** Build versioned development/held-out split and point-in-time synthetic fixtures; prevent leakage.
- [ ] **Session 3 · G · 2h:** Implement independent eval runner and deterministic checks; calibrate judge on human-labelled examples.
- [ ] **Session 4 · G · 2h:** Assessment 6: no-AI eval runner task, judge design defense, diagnose data leakage; record scores.

---

### Week 25 — Held-out quality

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Frozen evaluations estimate generalization; failure analysis guides development without contaminating holdout.

#### Terms to know

| Term | Definition |
|---|---|
| **Frozen version** | unchanged evaluated configuration |
| **stratification** | grouping by relevant categories |
| **difficult negative** | challenging case where action or answer is unwarranted |
| **uncertainty** | limits on estimated performance |
| **minimal reproduction** | smallest example reproducing a defect |

**Learning objective:** Report category results and improve only on development cases.

> **Knowledge checkpoint · Without AI**
>
> Why is repeated tuning on the same holdout misleading?

**Reading:** R21 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a held-out set? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why does repeated tuning contaminate it? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A category fails despite high aggregate accuracy: what should be reported? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain development versus holdout discipline. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Expand held-out set to 40 synthetic cases across agreed categories, including difficult negatives.
- [ ] **Session 2 · G · 2h:** Run frozen version on held-out set; report per-category results, uncertainty and failure types.
- [ ] **Session 3 · G · 2h:** Analyze dev failures separately; improve using dev cases only, reserve fresh held-out cases for retest.
- [ ] **Session 4 · E · 2h:** Draft technical product feedback report with minimal reproduction, version, impact and workaround.

---

### Week 26 — Shadow pilot simulation

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Shadow evaluation isolates model behavior from user decisions; controlled pilots test actual outcomes.

#### Terms to know

| Term | Definition |
|---|---|
| **Shadow mode** | execution without influencing live users |
| **point-in-time evidence** | information available at decision time |
| **adjudication** | resolution of reviewer disagreement |
| **ground truth** | reference outcome or label |
| **controlled pilot** | comparative deployment study |

**Learning objective:** Build temporal replay and design a controlled pilot.

> **Knowledge checkpoint · Without AI**
>
> Why can shadow results not establish an MTTR reduction?

**Reading:** R1, R21 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is point-in-time replay? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why does shadow mode not prove business impact? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A postmortem appears in retrieval before its historical publication: what is wrong? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain controlled pilot design to the CTO. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement replay harness using only incident-time evidence; prevent access to final resolution.
- [ ] **Session 2 · G · 2h:** Run 15–20 checkpoint cases from separate synthetic shadow set; log predictions before reveal.
- [ ] **Session 3 · G · 2h:** Simulate independent senior review and adjudication; design controlled pilot and measurement plan.
- [ ] **Session 4 · E · 2h:** Prepare champion facilitator guide with exercise, expected outcomes and troubleshooting; run teach-back.

---

### Week 27 — Adversarial testing

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Untrusted content and tool outputs are attack surfaces; test enforcement independently of prompts.

#### Terms to know

| Term | Definition |
|---|---|
| **Indirect prompt injection** | instructions embedded in external content |
| **exfiltration** | unauthorized data transfer |
| **attack surface** | reachable avenues for abuse |
| **credential leakage** | exposure of authentication secrets |
| **security regression** | repeatable check against known vulnerability |

**Learning objective:** Construct adversarial fixtures and verify denial.

> **Knowledge checkpoint · Without AI**
>
> Why is a system prompt not a sufficient security boundary?

**Reading:** R9, R13 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is indirect prompt injection? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is model instruction not access control? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A retrieved document asks the agent to disclose secrets: trace enforcement. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain adversarial tests and independent denial gates. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Construct injection fixtures from docs, telemetry and tool results; measure unsafe behavior.
- [ ] **Session 2 · G · 2h:** Test cross-tenant reads, egress restrictions, credential leakage and approval bypass; close critical defects.
- [ ] **Session 3 · G · 2h:** Run security regression and classify residual risks; distinguish tests from guarantees.
- [ ] **Session 4 · E · 2h:** Timed prototype 2: non-protected governed plugin demo with unexpected customer request; document delivery time and limits.

---

### Week 28 — Cost and latency

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Optimize cost and latency against quality and safety constraints.

#### Terms to know

| Term | Definition |
|---|---|
| **Input/output tokens** | model usage units |
| **prompt caching** | reuse of eligible prompt computation |
| **model routing** | selection among model providers or variants |
| **cost per investigation** | total attributable expense per run |
| **quality regression** | degradation in evaluated behavior |

**Learning objective:** Measure and defend a cost-quality trade-off.

> **Knowledge checkpoint · Without AI**
>
> How would you prove that cheaper inference preserves task quality?

**Reading:** R6, R21 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes cost per request from cost per successful task? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why measure quality alongside latency? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A cheaper model increases escalation: how would you compare options? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend a cost-quality decision with uncertainty. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Instrument token usage, tool latency, model latency and cost; establish baseline per investigation.
- [ ] **Session 2 · G · 2h:** Experiment with context reduction, caching or routing on dev cases; compare quality and cost.
- [ ] **Session 3 · G · 2h:** Document budget policy and stop thresholds; perform frozen quality comparison on fresh cases.
- [ ] **Session 4 · G · 2h:** Assessment 7: no-AI budget/validation task, security defense, diagnose quality regression; record scores.

---

## Phase 06 — Production engineering

### Week 29 — Observability

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Observability links distributed events and makes failures diagnosable.

#### Terms to know

| Term | Definition |
|---|---|
| **Trace** | end-to-end execution record |
| **span** | timed unit of traced work |
| **OpenTelemetry** | telemetry instrumentation standard |
| **cardinality** | number of distinct label values |
| **queue age** | time work has waited |

**Learning objective:** Instrument and diagnose a failing investigation.

> **Knowledge checkpoint · Without AI**
>
> How do traces differ from metrics and logs?

**Reading:** R22 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes traces, metrics and logs? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why propagate correlation IDs? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A request is slow across several services: how would you localize it? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain telemetry without exposing sensitive payloads. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Add OTel trace propagation across API, worker, model and tools; test correlation IDs.
- [ ] **Session 2 · G · 2h:** Implement metrics for queue age, errors, latency, cost and retry rate; verify no sensitive labels.
- [ ] **Session 3 · G · 2h:** Build local dashboard and alerts; inject failure and trace root cause; document response.
- [ ] **Session 4 · E · 2h:** Deliver workshop 5: evaluation and debugging with broken trace or tool; save recording if feasible.

---

### Week 30 — Operational readiness

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Operational readiness requires actionable procedures and measurable reliability objectives.

#### Terms to know

| Term | Definition |
|---|---|
| **SLI** | measured service indicator |
| **SLO** | target for an indicator |
| **runbook** | operational response procedure |
| **postmortem** | incident analysis and learning record |
| **recovery time** | time needed to restore service |

**Learning objective:** Execute a recovery drill and explain service targets.

> **Knowledge checkpoint · Without AI**
>
> What makes an alert actionable rather than merely noisy?

**Reading:** R22, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes SLI from SLO? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why should alerts be actionable? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A dependency outage triggers many alerts: prioritize response and recovery. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain a runbook and recovery drill evidence. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Write runbooks for stuck jobs, provider throttling, unavailable tools and data leak response.
- [ ] **Session 2 · G · 2h:** Run incident drill: recover queue and report incomplete results; measure recovery and record postmortem.
- [ ] **Session 3 · G · 2h:** Review SLOs and workload assumptions with customer; update risk register, no unsupported MTTR claim.
- [ ] **Session 4 · E · 2h:** Plan enterprise rollout cohorts, communications, support office hours and champion checks; simulate customer questions.

---

### Week 31 — AWS design

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Cloud architecture combines network isolation, identity, cost and repeatable infrastructure.

#### Terms to know

| Term | Definition |
|---|---|
| **VPC** | isolated virtual network |
| **ECS** | AWS container orchestration service |
| **RDS** | managed relational database service |
| **Terraform state** | record mapping configuration to infrastructure |
| **secrets injection** | secure delivery of credentials at runtime |

**Learning objective:** Defend minimal staging architecture and cost controls.

> **Knowledge checkpoint · Without AI**
>
> Which components need public access and which should remain private?

**Reading:** R23, R18 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a private subnet and IAM role? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why minimize public exposure? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A staging design has an internet-facing database: propose a safer boundary. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend architecture and cost assumptions. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Draw AWS network and identity design; estimate ECS/RDS/SQS costs and teardown strategy.
- [ ] **Session 2 · G · 2h:** Study Terraform state, IAM and private networking; scaffold IaC in professional mode where authorized.
- [ ] **Session 3 · G · 2h:** Plan migrations and SQS delivery adapter; define outbox/reconciliation and secrets injection.
- [ ] **Session 4 · E · 2h:** Refresh Claude product docs including Tag/Cowork; prepare audience-specific demo outline and limitations.

---

### Week 32 — AWS staging

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Managed queues and containers require explicit delivery and deployment guarantees.

#### Terms to know

| Term | Definition |
|---|---|
| **SQS** | AWS managed message queue |
| **visibility timeout** | period received message is hidden |
| **Fargate** | managed container compute |
| **container image** | packaged runtime filesystem |
| **Terraform plan** | preview of infrastructure changes |

**Learning objective:** Deploy or document blockers and test queue redelivery.

> **Knowledge checkpoint · Without AI**
>
> What happens if processing exceeds visibility timeout?

**Reading:** R23, R19 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is SQS visibility timeout? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why can messages be delivered more than once? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A job exceeds visibility timeout: trace duplicate execution risk. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain staging deployment and redelivery tests. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Implement IaC for minimal budgeted network, IAM and queue; validate plan and review destructive actions.
- [ ] **Session 2 · G · 2h:** Implement SQS adapter with visibility/duplicate handling and tests; retain native queue evidence.
- [ ] **Session 3 · G · 2h:** Build ARM-compatible container image and deploy short-lived ECS/RDS staging if access/budget permits; smoke test.
- [ ] **Session 4 · G · 2h:** Assessment 8: no-AI delivery semantics task, AWS design defense, diagnose IAM or network failure; record scores.

---

### Week 33 — Deployment verification

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Deployment verification checks actual environment behavior, not merely successful provisioning.

#### Terms to know

| Term | Definition |
|---|---|
| **Smoke test** | minimal functional verification |
| **TLS** | encrypted authenticated transport |
| **private subnet** | network segment without direct public routing |
| **redelivery** | message delivered again |
| **teardown** | removal of provisioned resources |

**Learning objective:** Verify staging security and recovery and remove costly resources.

> **Knowledge checkpoint · Without AI**
>
> How do you prove a database is not publicly reachable?

**Reading:** R23, R22 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is network reachability versus authentication? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why verify deployment rather than trust IaC intent? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A security group changes unexpectedly: what evidence establishes exposure? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain recovery and teardown verification. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Run migration and API/worker integration smoke tests in staging; verify TLS/private DB and secrets.
- [ ] **Session 2 · G · 2h:** Test cloud queue redelivery and worker restart; inspect metrics and audit trail.
- [ ] **Session 3 · G · 2h:** Capture deployment evidence; tear down costly resources and verify billing/inventory.
- [ ] **Session 4 · E · 2h:** Draft sanitized architecture case study from ADRs; remove credentials and proprietary details.

---

### Week 34 — CI/CD

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Delivery pipelines enforce quality and authorization; rollback must account for schema changes.

#### Terms to know

| Term | Definition |
|---|---|
| **CI/CD** | continuous integration and delivery/deployment |
| **artifact** | versioned build output |
| **short-lived credential** | temporary access token |
| **rollback** | return to prior release |
| **backward-compatible migration** | schema change supporting old and new code |

**Learning objective:** Build gated pipeline and demonstrate rollback.

> **Knowledge checkpoint · Without AI**
>
> Why can reverting application code fail after a migration?

**Reading:** R24, R23 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a deployment gate? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why are backward-compatible migrations useful? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A rollback encounters a newer schema: describe options and risks. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain CI credentials and rollback evidence. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Extend CI with type, tests, secret and image scans; verify failing check blocks release.
- [ ] **Session 2 · G · 2h:** Create release pipeline with approved deployment and short-lived AWS credentials; dry-run.
- [ ] **Session 3 · G · 2h:** Demonstrate versioned rollback and migration compatibility; document manual recovery.
- [ ] **Session 4 · E · 2h:** Claude Code admin training: spend, audit, connector allowlists and retention; practice customer objections.

---

### Week 35 — Load validation

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Representative load and injected faults expose bottlenecks and recovery limits.

#### Terms to know

| Term | Definition |
|---|---|
| **Burst** | short surge in arrivals |
| **saturation** | resource capacity exhaustion |
| **fault injection** | deliberately introduced failure |
| **retry amplification** | extra load caused by retries |
| **acceptance latency** | time until request is accepted |

**Learning objective:** Compare final and baseline behavior under failure.

> **Knowledge checkpoint · Without AI**
>
> How can retries worsen a throttling incident?

**Reading:** R15, R16 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is saturation? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why can retry storms amplify overload? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A burst causes throttling and queue growth: choose measurements and mitigations. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Compare baseline and final results fairly. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Reproduce mocked 10 rps burst and realistic pilot workload; measure API acceptance p95.
- [ ] **Session 2 · G · 2h:** Inject model throttling, database interruption and worker death; verify recovery and bounded retries.
- [ ] **Session 3 · G · 2h:** Compare final vs baseline load and cost; test real model only on small budgeted sample.
- [ ] **Session 4 · E · 2h:** Draft public technical article on durable agents with measured evidence, no invented production results.

---

### Week 36 — Resilience gate

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Release decisions require traceable evidence and explicit residual risk.

#### Terms to know

| Term | Definition |
|---|---|
| **Traceability** | mapping requirements to evidence |
| **acceptance test** | verification of agreed behavior |
| **resilience** | ability to withstand and recover from faults |
| **go/no-go** | release decision |
| **regression suite** | repeatable collection of checks |

**Learning objective:** Defend release decision using tests and recovery evidence.

> **Knowledge checkpoint · Without AI**
>
> Which failed gate must block release regardless of other scores?

**Reading:** R9, R21 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a release blocker? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why distinguish recovery time from data loss? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Load tests pass but tenant isolation fails: decide whether to release. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend release decision and residual risk. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Run full unit/integration/e2e/security suites; reconcile F1–F8 evidence and remaining gaps.
- [ ] **Session 2 · G · 2h:** Rehearse recovery runbook with unexpected fault; time recovery and write postmortem.
- [ ] **Session 3 · G · 2h:** Review held-out results and safety gates; decide release/no-release for simulated pilot.
- [ ] **Session 4 · G · 2h:** Assessment 9: no-AI recovery task, architecture defense, diagnose injected failure; record scores.

---

## Phase 07 — Professional readiness

### Week 37 — Customer handoff

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Handoff transfers operational ownership and communicates limitations.

#### Terms to know

| Term | Definition |
|---|---|
| **Acceptance report** | summary of requirement verification |
| **ownership** | accountability for ongoing operation |
| **known limitation** | documented unsupported behavior |
| **teach-back** | learner explains or demonstrates knowledge |
| **handoff** | transfer of responsibility |

**Learning objective:** Deliver customer demonstration and operational handoff.

> **Knowledge checkpoint · Without AI**
>
> How do you distinguish benchmark results from actual business outcomes?

**Reading:** R1, R2 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes acceptance from deployment? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why label simulated outcomes? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A customer asks for proven MTTR savings: what can you claim? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Deliver a concise handoff and support boundary. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Prepare acceptance report separating engineering benchmarks from customer pilot outcomes.
- [ ] **Session 2 · G · 2h:** Deliver Meridian demo with evidence, abstention, access denial and recovery; handle objections.
- [ ] **Session 3 · G · 2h:** Finalize runbooks, known limitations and ownership; verify clean clone and teardown.
- [ ] **Session 4 · E · 2h:** Deliver workshop 6: enterprise enablement, hands-on exercise, failure recovery and champion teach-back.

---

### Week 38 — Technical champion rollout

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Enterprise adoption is phased, measured and supported by internal champions.

#### Terms to know

| Term | Definition |
|---|---|
| **Cohort** | defined rollout group |
| **adoption metric** | measure of actual usage |
| **champion** | internal advocate and trainer |
| **enablement** | helping users gain capability |
| **usage governance** | controls on how services are used |

**Learning objective:** Design rollout and teach-back with measurable outcomes.

> **Knowledge checkpoint · Without AI**
>
> How would you distinguish usage growth from productivity improvement?

**Reading:** R2, R5 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is a technical champion? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why is usage not proof of productivity? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Adoption rises but quality falls: what metrics and interventions matter? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Teach a champion to evaluate safe usage. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · E · 2h:** Build phased adoption plan with opt-in cohorts, baseline measures and support schedule.
- [ ] **Session 2 · E · 2h:** Design admin readiness checklist and synthetic spend/usage reporting; distinguish local demonstrations from enterprise features.
- [ ] **Session 3 · E · 2h:** Run office-hours simulation with unfamiliar code and permission issue; capture product feedback.
- [ ] **Session 4 · E · 2h:** Rehearse train-the-trainer session with teach-back and revise materials.

---

### Week 39 — Portfolio

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Public evidence must be reproducible, sanitized and honest about limitations.

#### Terms to know

| Term | Definition |
|---|---|
| **Reproducibility** | ability to repeat results |
| **sanitization** | removal of sensitive information |
| **case study** | evidence-based account of a project |
| **facilitator guide** | instructions for delivering training |
| **disclosure** | explicit statement of relevant limitations |

**Learning objective:** Package reproducible teaching and engineering artifacts.

> **Knowledge checkpoint · Without AI**
>
> What evidence can be published without implying real customer deployment?

**Reading:** R2, R14 (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What makes an artifact reproducible? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why sanitize portfolio evidence? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A demo includes customer-like identifiers: what should be checked before publishing? | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the project honestly to an interviewer. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · E · 2h:** Draft technical article on permission-aware MCP with diagrams, tests and limitations.
- [ ] **Session 2 · E · 2h:** Package sanitized workshop repository or directory; reproduce setup from clean clone.
- [ ] **Session 3 · E · 2h:** Finalize evaluation/security case study and recorded demo if feasible; review disclosure and publication approval.
- [ ] **Session 4 · E · 2h:** Run train-the-trainer simulation with unfamiliar questions; improve facilitator guide and proficiency rubric.

---

### Week 40 — Independent backend remediation

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Independent remediation targets demonstrated weaknesses through transfer to unfamiliar problems.

#### Terms to know

| Term | Definition |
|---|---|
| **Transfer** | applying knowledge to a new task |
| **invariant** | condition preserved by implementation |
| **concurrency hazard** | incorrect behavior from overlapping execution |
| **deliberate practice** | focused work on a weakness |
| **evidence** | observable proof of competency |

**Learning objective:** Implement unfamiliar backend variant without AI.

> **Knowledge checkpoint · Without AI**
>
> Which earlier design assumption breaks under the new failure case?

**Reading:** R1, R2; revisit relevant technical source from earlier weeks (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What invariant does your backend variant need? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why test failure paths before optimizing? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: Choose an unfamiliar concurrency or persistence failure and reason through it. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain your independent solution and remaining weakness. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Select weakest backend competency from assessments; implement unfamiliar variant without AI.
- [ ] **Session 2 · G · 2h:** Test variant under failure and explain invariants; compare against original implementation.
- [ ] **Session 3 · G · 2h:** Revisit weakest data/distributed systems topic with targeted reading and experiment.
- [ ] **Session 4 · E · 2h:** Run timed demo using teammate-style unfamiliar material; assess clarity and adapting to audience.

---

### Week 41 — Independent AI remediation

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

AI remediation tests diagnosis and security reasoning without relying on generated solutions.

#### Terms to know

| Term | Definition |
|---|---|
| **Evaluation regression** | decline in measured model behavior |
| **threat model** | structured account of assets threats and controls |
| **root cause** | underlying reason for failure |
| **ablation** | removing one factor to measure its effect |
| **remediation** | corrective action |

**Learning objective:** Diagnose regression and defend security trade-offs independently.

> **Knowledge checkpoint · Without AI**
>
> How would you isolate model, retrieval and tool causes of a failure?

**Reading:** R1, R2; revisit relevant technical source from earlier weeks (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes retrieval failure from model failure? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why isolate variables during regression diagnosis? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A correct tool response leads to an incorrect conclusion: design a diagnostic test. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Defend your independent fix and safety trade-offs. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Select weakest agent/eval competency; independently modify behavior and test failure cases.
- [ ] **Session 2 · G · 2h:** Reproduce an evaluation regression and diagnose without AI; document correction.
- [ ] **Session 3 · G · 2h:** Review security threat model and independently defend rejected alternatives.
- [ ] **Session 4 · G · 2h:** Assessment 10: no-AI coding task, design defense, failure diagnosis; compare scores and identify final blockers.

---

### Week 42 — Final review

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Final defense connects requirements, architecture, operational evidence and learning outcomes.

#### Terms to know

| Term | Definition |
|---|---|
| **Architecture defense** | reasoned justification of design |
| **trade-off** | benefit gained at a cost |
| **acceptance criterion** | condition for approval |
| **retrospective** | review of outcomes and lessons |
| **evidence gap** | claim lacking supporting proof |

**Learning objective:** Explain the system end to end and identify remaining gaps.

> **Knowledge checkpoint · Without AI**
>
> Which original discovery requirement has the weakest supporting evidence?

**Reading:** R1, R2; revisit relevant technical source from earlier weeks (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What is requirements traceability? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why distinguish verified from simulated evidence? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A requirement has no passing test: decide how to report it. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Present the architecture end to end and identify gaps. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Conduct independent architecture defense covering end-to-end request, trust, state and failure flow.
- [ ] **Session 2 · G · 2h:** Run final acceptance and clean-clone checks; record open limitations and final cost.
- [ ] **Session 3 · E · 2h:** Finalize adoption strategy, product feedback and portfolio evidence; verify no publication without approval.
- [ ] **Session 4 · E · 2h:** Conduct end-of-residency retrospective against original discovery transcript and role requirements; document next learning goals.

---

### Week 43 — Scheduling reserve

*Weekly commitment: 4 sessions · 8 hours*

#### This week’s concepts

Reserve time closes blockers rather than adding scope; readiness depends on evidence.

#### Terms to know

| Term | Definition |
|---|---|
| **Exit criterion** | required condition to finish a phase |
| **blocker** | dependency preventing progress |
| **remediation** | work to correct a deficiency |
| **competency score** | evidence-based proficiency rating |
| **scope creep** | uncontrolled expansion of work |

**Learning objective:** Resolve highest-priority gap and decide whether extension is necessary.

> **Knowledge checkpoint · Without AI**
>
> What remains unverified, and what evidence would close it?

**Reading:** R1, R2; revisit relevant technical source from earlier weeks (see reference index).

#### Daily learning check-ins

*Use these independently of implementation progress. Answer from memory first; consult the weekly references or mentor afterward. If a topic is new, record a hypothesis and revisit it at closing.*

| Session | Opening / focused learning | Closing evidence |
|---|---|---|
| 1 · Understand | Mini-quiz: What distinguishes a blocker from optional polish? | Define two weekly terms in your own words; correct one misconception. |
| 2 · Apply | FAQ: Why preserve reserve rather than add scope? | Answer with an Atlas example and one relevant test or observation. |
| 3 · Challenge | Scenario: A protected competency remains unverified: choose remediation or extension. | State your decision, alternative, failure mode and verification method. |
| 4 · Demonstrate | Teach-back: Explain the final evidence and next learning priority. | Re-answer the weekly knowledge checkpoint; recall one earlier concept and connect it to this week. |

Record each response as **0** (unable), **1** (with help), or **2** (independent and accurate). Revisit scores below 2 at the next opening; mentor feedback is not a substitute for your own answer. Keep formal competency assessments separate.

#### Session plan

- [ ] **Session 1 · G · 2h:** Resolve highest-priority unmet exit criterion or repeat failed independent assessment.
- [ ] **Session 2 · B · 2h:** Reserve for delayed technical discovery, access or engineering remediation; if unused rehearse customer defense.
- [ ] **Session 3 · B · 2h:** Reserve for final regression, cloud teardown or artifact correction; if unused practice workshop delivery.
- [ ] **Session 4 · B · 2h:** Final audit of evidence, hours, competency scores and roadmap; decide whether extension is required.

## Reference index — targeted reading

Primary research: [large-codebase Claude Code guidance](https://claude.com/resources/articles/how-claude-code-works-in-large-codebases-best-practices-and-where-to-start), [enterprise coding-agent security guide](https://claude.com/resources/articles/enterprise-guide-to-securing-coding-agents), AWS [timeouts/retries/backoff](https://d1.awsstatic.com/builderslibrary/pdfs/timeouts-retries-and-backoff-with-jitter.pdf) and [SQS/outbox guidance](https://builder.aws.com/content/3JoT1IGGqqckc82pZpWlBuRClcP/building-reliable-microservices-with-amazon-sqs-and-the-outbox-pattern). Additional official documentation below is a recommended reading index, not a claim that every linked page was individually inspected.

| ID | Resource and focus |
|---|---|
| R1 | Atlas master spec §§2–3, 7–9; ATL-001 transcript; review unresolved requirements and acceptance |
| R2 | Customer-facing applied AI engineering competencies; teaching, administration, prototyping and product feedback |
| R3 | [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/), request validation, errors and tests |
| R4 | [Python asyncio](https://docs.python.org/3/library/asyncio.html); Fluent Python, typing and concurrency selections |
| R5 | [Claude Code docs](https://code.claude.com/docs/en/overview); settings, permissions, hooks, skills, subagents, plugins, MCP, headless, admin setup, monitoring, Bedrock; choose current section for task |
| R6 | [Claude API docs](https://platform.claude.com/docs/en/overview), messages, tools, streaming, errors and usage |
| R7 | [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents); workflows vs agents and evaluation |
| R8 | [Pydantic docs](https://docs.pydantic.dev/), types and validation |
| R9 | [OWASP GenAI security](https://genai.owasp.org/), injection, excessive agency, data disclosure |
| R10 | [PostgreSQL docs](https://www.postgresql.org/docs/current/), transactions, locks, indexes and EXPLAIN; Designing Data-Intensive Applications, transactions and delivery |
| R11 | [SQLAlchemy](https://docs.sqlalchemy.org/) and [Alembic](https://alembic.sqlalchemy.org/), sessions and migrations |
| R12 | [pgvector](https://github.com/pgvector/pgvector), distance, indexing and filters; AI Engineering by Chip Huyen, retrieval selections |
| R13 | [Keycloak documentation](https://www.keycloak.org/documentation), OIDC and roles; [OpenID Connect](https://openid.net/developers/specs/) and [SCIM RFC](https://www.rfc-editor.org/rfc/rfc7644) |
| R14 | [MCP specification](https://modelcontextprotocol.io/specification/), lifecycle, tools, transport and authorization |
| R15 | [Locust documentation](https://docs.locust.io/), workload and percentile reports |
| R16 | [AWS Builders Library](https://aws.amazon.com/builders-library/), timeouts/retries, idempotency and overload; DDIA distributed systems selections |
| R17 | [Redis documentation](https://redis.io/docs/latest/), atomic execution, expiry and cache design |
| R18 | [Bedrock user guide](https://docs.aws.amazon.com/bedrock/latest/userguide/), model access, IAM, inference, quotas and pricing |
| R19 | [SQS developer guide](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/), visibility, duplicate delivery, DLQ; AWS outbox article above |
| R20 | [LangGraph](https://docs.langchain.com/) and [Temporal](https://docs.temporal.io/), persistence and replay concepts; compare, do not adopt by default |
| R21 | AI Engineering by Chip Huyen, evaluation and inference sections; Claude API evaluation guidance; [Promptfoo](https://www.promptfoo.dev/docs/) as comparison |
| R22 | [OpenTelemetry docs](https://opentelemetry.io/docs/), trace propagation and metrics; [Prometheus](https://prometheus.io/docs/) and [Grafana](https://grafana.com/docs/) |
| R23 | [AWS ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/), RDS, IAM, Secrets Manager, CloudWatch and [Terraform](https://developer.hashicorp.com/terraform/docs), networking, state and teardown |
| R24 | [GitHub Actions docs](https://docs.github.com/en/actions), CI/CD, OIDC and environments; [Trivy](https://trivy.dev/latest/docs/), image and secret scanning |

## Coverage and release discipline

F1 API (weeks 1–6, 16); F2 tool loop (4–6, 10); F3 retrieval (8–12); F4 state/recovery (7, 16–19, 32–36); F5 sandbox approval (20–23); F6 access (9–12, 27); F7 audit (21–23, 27, 29); F8 telemetry (13, 28–30, 33–36). Confirm each with a test path and run output in the final acceptance matrix. Workstreams share the repository and synthetic fixtures. Workshops in weeks 5, 11, 17, 23, 29 and 37. Assessments in weeks 4, 8, 12, 16, 20, 24, 28, 32, 36 and 41 (the last is a delayed checkpoint to accommodate handoff; use a brief week-40 score update within session 4, no additional hours), plus final review. Unit 25–26 remediation is included near the end rather than assumed unnecessary.

Pilot baselines of 48→31 minutes diagnosis and 112→95 minutes resolution are provisional junior targets; validate scope and baseline with simulated customer. Shadow validates quality, not effect on actual MTTR. Do not conflate 180 incidents/month across categories with hypothetical 50,000 requests/day capacity. Test p95 API acceptance under mocked burst separately from investigation latency. Report per-category evaluation results, safety violations, cost and uncertainty. An 85% synthetic task result does not override a safety failure. Production is not authorized; all output writes separately permissioned, all mutations confined to approved sandbox. Real large-audience teaching, enterprise admin access and live production impact cannot be certified by this plan.

## Session record template

`Week / session | mode | planned vs actual time | assignment | check-in prompt / answer / score / correction | artifact/commit | tests and results | independent explanation | unresolved risk | next step`.

Review plan changes in an ADR or progress entry. Preserve master specification as governing baseline; seek approval for deviations. Publish sanitized artifacts only with explicit approval.
