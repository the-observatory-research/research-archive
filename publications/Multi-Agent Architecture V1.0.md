## Design, Runtime Evaluation, and Failure-Driven Engineering of a Distributed LLM System

_A Zero-Point Protocol Implementation Study_

**Author:** Tara Callegari
**Organization:** The Observatory

_Technical Research Report | September 2026_

**Version:** v1.0 
**Research Status:** Active Research  
**Study period:** May 2026–June 2026
**Architecture Lineage:** `zpp-core-mainnet`  
**Entropy Schema:** `zpp.entropy.char.nfc.v1`
**Published:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23649577.svg)](https://doi.org/10.5281/zenodo.23649577)

---

## Abstract

This report documents the design, implementation, and runtime evaluation of a persistent six-node multi-agent language-model architecture developed within the Zero-Point Protocol (ZPP) research program.

The system separates discovery, retrieval, validation, execution authority, external information ingress, local reasoning, persistence, cryptographic provenance, and runtime observation across independently executing node processes. Rather than coordinating those functions through a central orchestrator, the current architecture uses signed inter-node messages, role-local persistent state, distributed validation, leader-gated downstream execution, serialized local inference, and asynchronous state telemetry.

The present implementation consists of six nodes: three validator nodes (A/B/C), a discovery node (D), a retrieval/bridge node (E), and an internet-ingress/local-reasoning node (F). Each node owns a cryptographic identity, runtime state, node-local SQLite persistence, and asynchronous heartbeat telemetry. The implementation creates the node-local lattice, pulse observer, scorer, reasoning lock where applicable, and Ed25519 identity directly within each node process.

Development of the architecture has been driven by runtime observation rather than static specification alone. Integration and stress testing exposed duplicate ingestion, incomplete persistence, ambiguous execution identity, apparent concurrency failure, large asynchronous task accumulation, historical/current source ambiguity, and loss of durable reasoning output. These failures produced structural changes including execution sequencing, role-specific persistence, recovery tooling, deterministic deduplication, content-hash-based changed-only ingestion, and clearer separation between runtime operation and observation.

Two components remain explicitly experimental: **semantic scoring and fluid validator weighting**. Their present implementations are documented here as executable research mechanisms rather than finalized ZPP invariants. Current work is directed toward separating stable observations from versioned projections and adaptive coordination rules.

The architectural lineage itself remains stable under the canonical identifier:

`zpp-core-mainnet`

Changes in scoring, projection, weighting, or coordination state do not constitute new architectural lineages.

**Keywords:** Multi-Agent Systems, Distributed LLM Systems, Zero-Point Protocol (ZPP), Multi, Agent Architecture, Distributed AI Architecture, Runtime Observability, Persistent State, Cryptographic Provenance, Ed25519 Authentication, Distributed Validation, Failure-Driven Engineering, Local Language-Model Inference, Content-Addressed Ingestion, Asynchronous Orchestration

---

## 1. Research Question

The current architecture investigates a practical systems question:

> **How can an LLM-based multi-agent runtime distribute specialized responsibilities while preserving persistent state, attributable transport, bounded execution, observable runtime behavior, and recoverable execution history?**

A related design question concerns where architectural complexity should reside.

Earlier ZPP prototypes placed substantial processing logic in centralized engine chains. Those implementations made individual functions explicit but progressively increased the amount of orchestration surrounding the reasoning process.

The current architecture explores an alternative:

```text
centralized processing authority
              ↓
specialized persistent processes
              ↓
authenticated event boundaries
              ↓
local role ownership
              ↓
observable distributed state
```

The goal is not decentralization for its own sake. The architectural question is whether responsibilities that require persistence, verification, retrieval, measurement, or resource management can operate around the reasoner without unnecessarily becoming additional reasoning constraints.

---

## 2. Evidence Model

This report deliberately distinguishes implementation from empirical evidence.

Five evidence states are used:

| State              | Meaning                                                                                 |
| ------------------ | --------------------------------------------------------------------------------------- |
| **IMPLEMENTED**    | Mechanism exists in executable code                                                     |
| **OBSERVED**       | Behavior has been recorded during runtime execution                                     |
| **REPRODUCED**     | Behavior has occurred consistently across repeated executions or equivalent nodes       |
| **PENDING**        | Mechanism exists but its intended runtime property has not yet been tested sufficiently |
| **UNDER REVISION** | Mechanism is executable but its design or interpretation is actively being changed      |

These categories prevent three different statements from being treated as equivalent:

```text
the code contains the mechanism

the mechanism executed

the mechanism established the intended property
```

They are not equivalent.

This distinction is central to the experimental methodology used throughout the current architecture.

---

# 3. System Architecture

The active system consists of six independently running node processes:

```text
NODE_A     Validator
NODE_B     Validator
NODE_C     Validator

NODE_D     Source Discovery

NODE_E     Source Retrieval / Bridge

NODE_F     Internet Ingress / Local Reasoning
```

The current implementation assigns each process its own runtime state, local `MemoryLattice`, state-aware `AsynchronousPulse`, scoring instance, and Ed25519 identity. NODE_F additionally owns an asynchronous reasoning lock used to serialize local inference.

Network endpoints are currently:

```text
NODE_A    localhost:8000
NODE_B    localhost:8001
NODE_C    localhost:8002
NODE_D    localhost:8003
NODE_E    localhost:8004
NODE_F    localhost:8005
```

The architecture contains no active central runtime orchestrator.

A simplified current topology is:

```text
                         ┌──────── NODE_A ────────┐
                         │                        │
SOURCE → NODE_D → NODE_E ├──────── NODE_B ────────┼─→ elected dispatch
                         │                        │          ↓
                         └──────── NODE_C ────────┘       NODE_F
                                                            ↓
                                                     local reasoning
```

Internet-originating queries enter through NODE_F before being distributed to the validator cluster.

---

# 4. Cryptographic Transport and Node Identity

Each node owns an Ed25519 keypair through `CryptoEngine`.

The implementation separates cryptographic identity from model identity. The key belongs to the runtime/node sending the protocol event rather than to a model backend. `CryptoEngine` persists node keys locally and derives the public identity from the corresponding private key.

Payloads are serialized through deterministic canonical JSON before signing. Keys are used to produce Base64-encoded signatures suitable for JSON transport, while inbound verification reconstructs the canonical payload and verifies its Ed25519 signature.

The node's inbound handler verifies the supplied signature before dispatching the payload according to message type. Invalid signatures terminate processing before role-specific execution.

The resulting boundary is:

```text
local node action
      ↓
structured event
      ↓
canonical serialization
      ↓
Ed25519 signature
      ↓
WebSocket transport
      ↓
signature verification
      ↓
role-specific handling
```

### Evidence status

**IMPLEMENTED**

Signed transport is present in the executable runtime.

Runtime records additionally contain observed signed D→E handoffs and validator broadcasts, providing empirical evidence for specific paths through the architecture.

---

# 5. Node-Local Persistence

Every node owns a local `MemoryLattice` backed by SQLite.

The memory implementation defines volatile layers for:

```text
conversation
pulse
anchor
internet_ingress
discovery
bridge_retrieval
reasoning
```

and initializes persistent tables for conversational/history records, pulse records, and state hashes.

Writes first enter an asyncio-protected volatile matrix. Persistent disk writes are then scheduled separately, with synchronous SQLite operations moved through an executor rather than performed directly in the WebSocket event path.

This produces two related state surfaces:

```text
volatile role-local context
             +
persistent role-local history
```

The current persistence topology intentionally avoids treating one centralized database as the complete state of the mesh.

### Runtime correction

Earlier execution revealed that A/B/C persisted validator material while newer D/E/F roles did not consistently persist their own operational products. The persistence implementation was subsequently expanded to recognize `discovery`, `bridge_retrieval`, `internet_ingress`, and `reasoning` layers.

This is an example of a current architectural feature arising directly from an observed implementation failure.

---

# 6. Discovery and Retrieval Boundary

NODE_D and NODE_E divide local source processing into two responsibilities.

NODE_D identifies candidate material.

NODE_E retrieves and classifies it.

NODE_D currently searches Markdown content for configured research markers, records discovery metadata, persists discovery state, writes an append-only discovery ledger, and creates a signed handoff for NODE_E.

The design boundary is therefore:

```text
NODE_D
What relevant source exists?

        ↓

NODE_E
What content currently exists at that source?
```

The separation prevents discovery from automatically becoming retrieval, validation, reasoning, and persistence authority.

---

# 7. Content-Addressed Changed-Only Ingestion

Repeated historical source traversal revealed that downstream deduplication was insufficient.

Each validator database eventually contained:

```text
636 total rows
204 unique payloads
432 redundant rows
```

per validator.

NODE_E's historical retrieval state similarly contained:

```text
364 bridge records
182 unique source paths
182 repeated paths
```

The architectural correction moved duplicate prevention toward the ingestion boundary.

NODE_E now computes a deterministic content hash and compares it with a persistent path-indexed manifest.

The implemented classification is:

```text
unknown path
→ NEW

known path + identical hash
→ UNCHANGED

known path + different hash
→ MODIFIED
```

The code explicitly returns `UNCHANGED` when the stored and current hashes match.

`UNCHANGED` content terminates before downstream broadcast. Accepted NEW or MODIFIED material is persisted, recorded in the bridge ledger, signed, and broadcast to the validator cluster; the successful content state is then written into the manifest.

### Evidence status

**IMPLEMENTED / BASELINE SEEDED / LIVE VALIDATION PENDING**

The 182-path historical baseline has been constructed.

The next validation should establish that:

```text
unchanged vault
→ zero downstream processing
```

and subsequently:

```text
one modified file
→ one expected downstream processing path
```

Until those tests are completed, changed-only behavior should not be described as fully validated.

---

# 8. Validator Cluster

NODE_A, NODE_B, and NODE_C currently execute the same deterministic textual scoring implementation.

The present `GammaScorer` explicitly limits its responsibility to textual characteristics. It does not establish node identity, verify signatures, calculate trust, or grant consensus authority.

Its current factors are:

```text
novelty        → lexical breadth
entropy        → normalized character entropy
self_reference → lexical self-reference frequency
paradox        → selected lexical-pattern frequency
coherence      → recent-context token overlap
```

The current default weights are:

```text
novelty         0.25
entropy         0.20
self_reference  0.15
paradox         0.25
coherence       0.15
```

with thresholds of `0.40` and `0.55`.

Identical validator results have been observed for identical payloads under equivalent local context.

That observation supports:

> **deterministic replicated scoring under the tested conditions**

It does **not** establish that A/B/C currently perform differentiated independent model judgment.

That distinction is intentional in this report.

---

# 9. Scoring Architecture — Active Experimental Layer

The current scorer should not be interpreted as a finalized semantic model.

It is an implemented heuristic projection inherited from an earlier architectural generation and is presently under active redesign.

This distinction matters because several public factor names retain historical terminology while their current computation is considerably narrower. For example, `novelty` currently represents lexical breadth and `coherence` represents recent-context token overlap. The scorer itself documents that compatibility distinction.

The current research direction is therefore to separate:

```text
RAW OBSERVATION
      ↓
NORMALIZED STATE REPRESENTATION
      ↓
VERSIONED / ROLE-SPECIFIC PROJECTION
      ↓
FUNCTIONAL ACTION
```

rather than allowing one aggregate score to become synonymous with the observations from which it was derived.

The intended invariant is:

> **Observations should remain stable and attributable even when the weighting or interpretation applied to those observations changes.**

Accordingly, future scoring revisions remain within `zpp-core-mainnet`; changing a projection does not change the identity of the architectural lineage.

---

# 10. Fluid Validator Weighting — Active Experimental Layer

The validator cluster begins from a near-balanced state:

```text
NODE_A = 0.33
NODE_B = 0.33
NODE_C = 0.34
```

The current runtime adjusts these values when the absolute difference between measured coherence and entropy exceeds `0.15`. Under that rule NODE_C can increase toward `0.60`, with the remainder divided between A and B.

Leader selection then chooses the node with the maximum current cluster weight.

This mechanism is **implemented and observed**, but its interpretation is not settled.

Open questions include:

- whether the current update rule has a justified relationship to execution authority;
    
- whether weights stabilize, oscillate, or saturate under controlled workloads;
    
- whether validator-local weight state remains synchronized;
    
- whether adaptive weighting produces measurable benefit;
    
- how weighting should relate, if at all, to semantic projection;
    
- and whether coordination weights should remain completely separate from textual scoring weights.
    

The present mechanism should therefore be classified:

**IMPLEMENTED / OBSERVED / UNDER REVISION**

rather than validated.

### Implementation issue identified during report audit

The current `adjust_weights()` path increases the `paradox` scoring weight without simultaneously renormalizing the other scoring weights, then reconstructs `GammaScorer`.

`GammaScorer`, however, requires its supplied weights to sum to exactly `1.0`.

Consequently, the present adaptive scoring-weight path requires redesign before it can be treated as a valid fluid scoring mechanism.

This issue belongs in the research record rather than being hidden from the report.

---

# 11. Distributed Validation and Singular Execution

The current architecture separates validation from downstream execution.

All three validators can process the same signed content, but only the validator selected by the current leader rule is permitted to create the reasoning trigger.

The implementation performs leader selection, tests the current score against the execution threshold, increments an execution sequence for the elected leader, constructs a signed reasoning event, and dispatches it to NODE_F. Non-leader validators defer downstream execution.

The resulting structure is:

```text
                 A evaluates
                /
payload ─────── B evaluates
                \
                 C evaluates
                     ↓
                leader selection
                     ↓
              one signed dispatch
                     ↓
                   NODE_F
```

Runtime testing observed the coexistence of replicated validation and singular downstream execution.

### Evidence status

**IMPLEMENTED / OBSERVED**

---

# 12. Election State and Execution Identity

Early leader gating used election state as though it uniquely identified an execution.

Runtime testing demonstrated that this assumption was incorrect.

One leader may legitimately authorize multiple operations without a new election.

The architecture consequently separates:

```text
election_epoch
```

from:

```text
execution_sequence
```

NODE_F tracks both `last_accepted_election_epoch` and `last_accepted_execution_sequence`, rejecting older elections and already-consumed execution sequences.

This represents a particularly useful example of architecture evolving from an observed protocol failure:

```text
initial assumption
election identity = execution identity

runtime failure
second legitimate operation rejected

revised model
leadership state ≠ execution identity
```

The distinction now exists explicitly in the implementation.

---

# 13. NODE_F Local Reasoning and Resource Boundary

NODE_F performs local reasoning through:

```text
Ollama
deepseek-r1:7b
localhost:11434/api/chat
```

with streamed inference and a current context configuration of 8192 tokens.

Local inference is protected by an `asyncio.Lock`. Accepted reasoning jobs create tasks, but the inference path itself must acquire the NODE_F reasoning lock before entering `REASONING_ACTIVE`; completion returns the node to `INGRESS_READY`.

During the historical-vault stress run, queued reasoning proceeded sequentially over several hours.

A total of:

```text
181 completed reasoning streams
```

were subsequently recovered from the preserved terminal transcript.

This provides runtime evidence that the lock operated as a **local inference resource boundary** under that workload.

It does not yet establish optimal queue behavior.

---

# 14. Runtime Observability

Each node owns a state-aware asynchronous heartbeat.

`AsynchronousPulse` samples state through a supplied `state_getter`, records the node identifier, current state, total active asyncio tasks, and pulse signature, then persists the observation through the node's `MemoryLattice`.

This architecture intentionally separates:

```text
node owns state
pulse observes state
```

rather than allowing the heartbeat mechanism to control the node.

Observed states include:

```text
A/B/C
VALIDATOR_READY
VALIDATING
LEADER_ACTIVE

D
DISCOVERY_IDLE
DISCOVERY_ACTIVE

E
BRIDGE_IDLE
BRIDGE_ACTIVE

F
INGRESS_READY
SEARCH_ACTIVE
REASONING_ACTIVE
```

During the historical-vault run, NODE_F was observed in `REASONING_ACTIVE` across multiple consecutive heartbeat intervals.

The same instrumentation recorded approximately `202–203` active asyncio tasks while the reasoning backlog existed.

The interpretation of that count remains open.

It may represent expected waiting work, persistent task accumulation, or a combination of both.

That question requires bounded before/during/after workload testing.

---

# 15. Stress Test and Failure-Driven Revision

The historical-vault execution unintentionally became a high-load integration test.

The run exercised:

```text
discovery
→ retrieval
→ validator fan-out
→ leader gating
→ reasoning dispatch
→ serialized local inference
→ pulse observation
→ persistence
```

It exposed several architectural boundaries simultaneously.

| Failure / Observation                                 | Structural Response                                                 |
| ----------------------------------------------------- | ------------------------------------------------------------------- |
| Election epoch rejected legitimate repeated execution | Added independent execution sequence                                |
| Apparent reasoning deadlock                           | Added traceback instrumentation; exposed undefined variable         |
| D/E/F persistence incomplete                          | Expanded role-specific MemoryLattice layers                         |
| 181 reasoning streams not durably stored              | Recovered transcript and established direct-persistence requirement |
| 636 validator rows contained only 204 unique payloads | Deterministic deduplication                                         |
| E contained 364 records for 182 source paths          | Moved replay prevention to changed-only ingestion                   |
| ~203 active tasks under backlog                       | Opened bounded queue-lifecycle investigation                        |
| Historical/current documentation mixed                | Separated active authority from historical archive                  |

The important result is not that the architecture operated without failure.

It did not.

The significant engineering pattern was:

```text
unexpected behavior
        ↓
instrumentation
        ↓
failure localization
        ↓
structural correction
        ↓
rerun
        ↓
new observation
```

This process produced much of the present architecture.

---

# 16. Current Implementation Discrepancies

The implementation audit also identified transitional differences between the intended current architecture and the uploaded executable snapshot.

These should remain explicit.

### 16.1 Lineage identifier

The canonical current architecture uses:

```text
zpp-core-mainnet
```

The uploaded `agent_node.py` still emits the historical identifier:

```text
zpp_gamma_mainnet
```

in multiple event construction paths, including the handshake and reasoning relay.

**Classification:** legacy implementation residue / migration required.

The report uses `zpp-core-mainnet` as canonical.

### 16.2 Original query separation

The architecture intends to preserve the original user query separately from retrieved evidence.

The current reasoning-trigger envelope includes `original_query`.

However, the receiving reasoning path currently passes only `text_context` and telemetry into `execute_core_reasoning_pipeline()`.

Inside that pipeline, `context_text` is currently rendered as both `USER QUERY` and `MATRIX`.

Therefore:

**query/evidence separation is an architectural intention that is not fully preserved through the current executable reasoning path.**

This should be corrected rather than described as completed.

### 16.3 Live reasoning persistence

The architecture supports a `reasoning` persistence layer.

The uploaded reasoning function, however, currently streams generated tokens directly to stdout; the visible execution path does not accumulate the completed response and commit it to `MemoryLattice`.

Therefore the 181 historical reasoning records demonstrate successful **recovery**, but the current uploaded implementation does not yet establish automatic durable persistence of future completed reasoning streams.

**Classification:** persistence layer implemented; automatic reasoning-output commit requires completion/verification.

These discrepancies are not removed from the evidence record. They define concrete next engineering tasks.

---

# 17. Determinism Boundary

The current architecture does not require deterministic language-model reasoning.

Instead, deterministic mechanisms are used where reproducibility or integrity requires them:

```text
canonical serialization
content hashing
signature verification
change classification
duplicate rejection
execution sequencing
deterministic heuristic scoring
leader selection from a given weight state
```

DeepSeek generation remains probabilistic.

This produces an important architectural distinction:

> **Deterministic integrity mechanisms can surround probabilistic reasoning without requiring the reasoning process itself to become deterministic.**

This distinction also prevents source provenance from being confused with generated interpretation.

---

# 18. Current Evidence Baseline

At the time represented by the source records and uploaded runtime:

```text
Six-node runtime topology             IMPLEMENTED
Per-node Ed25519 identity             IMPLEMENTED
Signed inbound verification           IMPLEMENTED
Node-local SQLite persistence         IMPLEMENTED
Role-specific persistence layers      IMPLEMENTED
State-aware 60s pulse                 IMPLEMENTED / OBSERVED
A/B/C deterministic scoring           IMPLEMENTED / OBSERVED
Single-leader dispatch                IMPLEMENTED / OBSERVED
Election + execution sequencing       IMPLEMENTED / OBSERVED
NODE_F serialized reasoning           IMPLEMENTED / OBSERVED
181 historical reasoning streams      RECOVERED
A/B/C duplicate cleanup               COMPLETE
NODE_E 182-path baseline              SEEDED
Changed-only classification           IMPLEMENTED
Changed-only end-to-end behavior      PENDING VALIDATION
Queue lifecycle under bounded load    OPEN
Current Gamma scoring model           UNDER REVISION
Fluid validator weighting             UNDER REVISION
Automatic live reasoning persistence  REQUIRES COMPLETION/TEST
Query/evidence separation             REQUIRES CODE CORRECTION
zpp-core-mainnet migration             REQUIRED
```

---

# 19. Active Research Direction

The next architectural work is deliberately narrower than another full-system redesign.

The immediate research focus is the relationship among:

```text
observation
measurement
projection
coordination
action
```

The current scoring implementation compresses several textual observables into a single Gamma value. Fluid validator behavior then uses selected measurements to alter execution authority.

Those mechanisms are now being decomposed.

The intended direction is:

```text
RAW OBSERVABLES
      ↓
stable normalized state
      ↓
versioned functional projection
      ↓
bounded coordination state
      ↓
explicit functional action
```

This allows two invariants to coexist:

> **The observation does not belong to the decision that consumes it.**

and:

> **Weights may move; the provenance of the observation may not.**

Scoring and validator-weight adaptation can therefore change experimentally without rewriting the evidence from which earlier decisions were made.

The architecture remains within `zpp-core-mainnet` throughout those changes.

---

# 20. Open Validation Program

The next runtime tests should target properties that are currently implemented but not yet established empirically:

```text
Changed-only test
unchanged vault → zero downstream replay

Single-modification test
one changed source → one expected processing lineage

Reasoning persistence test
completed inference → durable NODE_F reasoning record

Restart test
node restart → required persistent state recoverable

Transport tamper test
modified signed payload → verification failure

Queue lifecycle test
bounded workload → task count measured
before / during / after drain

Fluid-weight test
controlled payload sequence →
weight trajectory / saturation / oscillation recorded

Scoring-generation test
same raw observations →
different versioned projections without
altering observation provenance
```

These experiments will determine which current properties can move from **IMPLEMENTED** or **OBSERVED** to **REPRODUCED** or **VALIDATED**.

---

# 21. Conclusion

The current Zero-Point Protocol runtime represents a transition from centralized, engine-oriented processing toward a persistent role-separated multi-agent system.

Its principal engineering contribution at this stage is not a claim that distributed agents, fluid weighting, or semantic scoring have been solved.

The stronger result is the construction of an executable environment in which those questions can be isolated and tested.

The current runtime separates source discovery, retrieval, validation, execution authority, external ingress, local reasoning, persistence, cryptographic identity, and state observation. Runtime failures have produced concrete architectural corrections rather than being removed from the research record.

The system therefore provides both an implementation and an experimental surface.

Its development history supports a recurring methodology:

```text
IMPLEMENT
    ↓
OBSERVE
    ↓
LOCALIZE FAILURE
    ↓
CORRECT
    ↓
RETEST
    ↓
PRESERVE EVIDENCE
```

Scoring and fluid weighting remain active research layers. Changed-only ingestion, reasoning persistence, query/evidence separation, queue behavior, and current lineage migration have clearly defined next validation steps.

The architectural lineage remains:

**`zpp-core-mainnet`**

while the mechanisms operating within that lineage remain open to evidence-driven revision.
