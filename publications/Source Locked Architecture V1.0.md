## Preserving Source Integrity, Provenance, and Stateful Continuity in Language-Model Systems

_A Technical Framework for Source Preservation, Derivation Tracking, and Verifiable State Transitions_

**Author:** Tara Callegari
**Organization:** The Observatory

_Technical Research Report | September 2026_

**Version:** v1.0  
**Research Status:** Active Research  
**Architecture Lineage:** `zpp-core-mainnet`  
**Entropy Schema:** `zpp.entropy.char.nfc.v1`
**Published:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23650412.svg)](https://doi.org/10.5281/zenodo.23650412)

---

## Abstract

Distributed language-model systems combine probabilistic generation with stateful software, external information sources, model-to-model communication, persistent memory, retrieval, and automated coordination. These systems create an architectural problem that is distinct from model capability: as information is retrieved, transformed, interpreted, persisted, and exchanged between components, the system must preserve the identity and provenance of authoritative source material without requiring every reasoning process operating on that material to be deterministic.

This paper presents the Zero-Point Protocol (ZPP) and its foundational Source-Locked Architecture (SLA). ZPP separates probabilistic reasoning from deterministic integrity mechanisms by preserving explicit boundaries among source, derivation, evidence, state, and lineage. SLA defines the conditions under which source-derived state remains attributable, state mutation remains authorized, external contributions remain distinguishable from authoritative source material, and significant transitions remain recoverable across execution boundaries.

The architecture does not require a single orchestration model, consensus algorithm, scoring function, language model, or network topology. Instead, it defines persistent invariants that may be implemented through content hashing, cryptographic signatures, authenticated transport, node-local state, retrieval lineage, explicit role boundaries, duplicate detection, deterministic verification, and attributable state transitions.

Earlier ZPP prototypes coupled these principles to linear routing scores, fixed thresholds, multi-signature consensus, deterministic state machines, and centralized or leader-oriented control mechanisms. Subsequent implementation and runtime testing showed that these mechanisms should be distinguished from the architectural invariants they were intended to protect. The current formulation therefore treats scoring, consensus, routing, model selection, and coordination as replaceable implementations while preserving source authority and lineage as architectural properties.

ZPP consequently establishes a hybrid systems model: reasoning may remain probabilistic while provenance, identity, authorized mutation, and verifiable state transitions remain deterministic where required.

**Keywords:** Zero-Point Protocol (ZPP), Source-Locked Architecture (SLA), Source Integrity, Data Provenance, Stateful Continuity, Distributed AI Systems, Large Language Models (LLMs), Cryptographic Verification, Persistent State, Authorized State Mutation, Deterministic Integrity, Probabilistic Reasoning, Architectural Lineage, Multi-Agent Systems

---

## 1. Introduction

Language-model systems increasingly operate as components within larger computational environments.

A single source may pass through:

```text
RETRIEVAL
    ↓
LANGUAGE-MODEL INTERPRETATION
    ↓
ANOTHER MODEL
    ↓
VALIDATION
    ↓
PERSISTENT MEMORY
    ↓
LATER RETRIEVAL
    ↓
ADDITIONAL TRANSFORMATION
```

At each boundary, several questions arise:

- What was the original source?
- What was derived from it?
- What evidence has been established about it?
- What does the architecture currently preserve as state?
- Who or what is authorized to change that state?
- Can the transition history be reconstructed afterward?

Conventional data integrity mechanisms can establish that bytes changed or that a message originated from a particular cryptographic identity. Language-model reasoning introduces an additional complication: a probabilistic system may legitimately produce multiple interpretations of the same source.

Preventing all variation would destroy much of the reasoner's utility.

Allowing every derivation to silently replace its source destroys provenance.

The Zero-Point Protocol addresses this distinction.

Its central architectural proposition is:

Source preservation does not require reasoning determinism.

Instead, ZPP protects the relationships that must remain attributable while allowing reasoning systems to remain probabilistic where variation is legitimate.

---

## 2. Architectural Problem

The original ZPP specification framed the problem primarily as a routing vacuum.

That formulation identified a real limitation: transport systems can deliver data successfully without knowing whether the meaning or authority relationships represented by that data have changed.

Subsequent implementation expanded the problem.

Semantic preservation cannot be solved solely by selecting a better route.

Consider:

```text
SOURCE A
    ↓
Model 1 produces Derivation B
    ↓
B is persisted
    ↓
Model 2 retrieves B
    ↓
B is presented as though it were A
```

Every packet may have reached its intended destination.

Every network operation may have succeeded.

Every database transaction may have been valid.

Yet the architecture has lost a crucial relationship:

$$
A\neq B
$$

The failure is therefore not exclusively a network-routing failure.

It is a provenance and state-authority failure.

ZPP now treats this as the more general architectural problem.

---

## 3. Source-Locked Architecture

Source-Locked Architecture is the foundational state-integrity model within ZPP.

SLA preserves trusted architectural state by anchoring:

- source identity
- provenance
- persistent state
- verification evidence
- authorized mutation

to an explicit source and recoverable lineage.

External systems may participate.

They may:

- reason
- retrieve
- transform
- compare
- criticize
- verify
- propose
- generate

Participation does not itself grant authority over protected source-derived state.

This produces the primary invariant:

Source identity and provenance remain invariant while reasoning over that source may remain probabilistic.

The word locked therefore refers to attribution and protected state relationships.

It does not mean that reasoning is locked to one interpretation.

---

## 4. Five Distinct Architectural Objects

The current formulation separates five objects that earlier implementations sometimes compressed together:

| Architectural object | Meaning                                            |
| -------------------- | -------------------------------------------------- |
| **SOURCE**           | What entered the architecture                      |
| **DERIVATION**       | What a reasoning process produced from the source  |
| **EVIDENCE**         | What can be established about source or derivation |
| **STATE**            | What the architecture currently preserves          |
| **LINEAGE**          | How that state came to exist                       |

These categories can interact without becoming interchangeable.

Suppose a source contains:

$S$

A language model produces:

$$
D_1=M(S)
$$

A second model produces:

$$
D_2=N(S)
$$

and deterministic verification establishes property:

$$
E(S)=\text{true}
$$

ZPP does not require:

$$
D_1=D_2
$$

Nor does it require either derivation to become authoritative simply because it was generated later.

Instead:

- $S$ remains $S$
- $D_1$ remains attributable to $M(S)$
- $D_2$ remains attributable to $N(S)$
- $E$ remains attributable to its verification procedure

A later state may incorporate one or more of these objects, but the transition must not erase their lineage.

---

## 5. Source Authority

SLA distinguishes authority from confidence.

An output does not become authoritative merely because it is:

- newer
- more detailed
- more confident
- generated by a larger model
- generated by more models
- repeated more frequently
- preferred by a leader
- or rhetorically convincing

Authority over protected state is determined by provenance and explicit mutation rules.

This principle prevents a common failure in generative systems:

```text
SOURCE
   ↓
SUMMARY
   ↓
SUMMARY OF SUMMARY
   ↓
NEW GENERATION
   ↓
NEW GENERATION TREATED AS SOURCE
```

The transformations may be useful.

The failure occurs when their derived status disappears.

ZPP therefore requires the architecture to preserve the distinction between source material and transformations of that material.

---

## 6. Reasoning Path and Mutation Path

One of the most important refinements to ZPP is the separation of two paths.

### Reasoning path

```text
SOURCE
  ↓
REASONING
  ↓
INTERPRETATION
  ↓
COMPARISON
  ↓
HYPOTHESIS
```

### Mutation path

```text
CURRENT PROTECTED STATE
          ↓
     PROPOSED CHANGE
          ↓
REQUIRED EVIDENCE / AUTHORIZATION
          ↓
    ┌─────┴────────────┐
    ↓                  ↓
  APPLIED        REJECTED / UNRESOLVED
    └─────┬────────────┘
          ↓
     LINEAGE RECORD
```

The paths may intersect.

They are not identical.

A reasoner may propose a state change.

A reasoner may provide evidence relevant to a state change.

A reasoner may even produce a result that can subsequently be deterministically verified.

But:

Reasoning does not automatically confer mutation authority.

This permits reasoning freedom without requiring protected state to accept every generated conclusion.

---

## 7. Determinism Boundary

The original ZPP specification used the language of deterministic routing and deterministic inference extensively.

Implementation showed that the more useful distinction is:

**PROBABILISTIC WHERE DIFFERENTIATION IS USEFUL**

**DETERMINISTIC WHERE INTEGRITY REQUIRES IT**

Language-model generation may remain probabilistic.

Deterministic mechanisms may instead protect:

- content identity
- hash calculation
- canonical serialization
- signature verification
- source identifiers
- duplicate detection
- sequence validation
- authorized mutation
- state transition records
- schema validation
- deterministically verifiable results

The resulting architecture can be represented as:

$$
\text{Probabilistic Reasoning}+\text{Deterministic Integrity}
$$

rather than:

$$
\text{Deterministic Reasoning}
$$

This distinction substantially broadens ZPP's applicability.

The protocol no longer depends on making generative reasoning itself deterministic.

---

## 8. Source Identity

Every protected source requires an identity sufficient to distinguish it from later transformations.

Depending on the implementation, source identity may include:

- source identifier
- content hash
- origin
- timestamp
- version
- cryptographic signer
- storage location
- retrieval event
- schema identifier
- lineage identifier

Not every implementation requires every field.

The requirement is that later architectural state can answer:

Which source is this state derived from?

Where source content changes, the architecture should distinguish:

same source identity / new version

from:

new source

according to an explicitly defined versioning policy.

Silent replacement defeats source locking.

---

## 9. Provenance

Source identity answers:

What is this?

Provenance answers:

How did it arrive here?

A useful provenance record may contain:

$$
\begin{aligned}P=(&\text{source},\ \text{origin},\ \text{actor},\ \text{operation},\\ &\text{time},\ \text{previous state},\ \text{resulting state})\end{aligned}
$$

For distributed language-model systems, provenance becomes especially important because transformations may occur across multiple models and execution environments.

A source-derived object might therefore carry lineage such as:

```text
SOURCE
   ↓
retrieved by E
   ↓
evaluated by A/B/C
   ↓
dispatched by C
   ↓
reasoned over by F
   ↓
result persisted
```

The result is not the source.

But the relationship between them remains reconstructable.

---

## 10. Persistent Lineage

Persistence alone is insufficient.

A database can faithfully preserve corrupted or unattributed state.

SLA therefore requires recoverable lineage, not merely storage.

For a significant state transition:

$$
S_t\rightarrow S_{t+1}
$$

the architecture should preserve, where applicable:

- what changed
- why it changed
- what source was involved
- what evidence supported the transition
- which component performed it
- when it occurred
- what preceded it
- what followed it

Continuity can then survive process termination or model replacement.

This produces another important architectural result:

Continuity does not require permanence of the reasoner.

The model operating over a source may change.

The node occupying a role may change.

The process may restart.

What must survive is enough state and lineage to reconstruct the relevant architectural relationship.

---

## 11. Protected Evidence

SLA also distinguishes evidence from subsequent interpretation.

Suppose deterministic verification establishes:

$$
x=42
$$

and the result, verification method, and inputs are persisted.

A later probabilistic reasoner may claim:

$$
x=41
$$

ZPP does not require preventing the model from generating that claim.

It requires preventing the new generation from silently erasing the fact that the previous verification occurred.

The later output may:

- challenge the verification
- identify an error in its assumptions
- produce new evidence
- trigger re-verification

But a new state should preserve the lineage:

- Verification $E_1$ established result $R_1$.
- Later derivation $D_2$ challenged $R_1$.
- Verification $E_2$ subsequently established $R_2$.

rather than rewriting history as though only $R_2$ ever existed.

Thus:

New evidence produces a new state transition. It does not erase prior evidence.

---

## 12. Trust Is Not Authority

ZPP distinguishes trust evaluation from state authority.

An independent evaluator may provide highly credible evidence.

Multiple evaluators may converge.

A cryptographic identity may be trusted.

None of those facts automatically establishes permission to mutate protected state.

The relationship is:

```text
INFORMATION RECEIVED
        ≠
INFORMATION VERIFIED
        ≠
STATE MUTATION AUTHORIZED
```

This distinction becomes particularly important in multi-agent systems where several nodes participate in evaluation.

Trust can inform a mutation decision.

Trust is not itself the mutation boundary.

---

## 13. Source Locking Is Not Reasoning Locking

The term Source-Locked Architecture can otherwise invite the wrong interpretation.

SLA does not require all systems processing a source to reproduce identical outputs.

Given source $S$:

$$
\begin{aligned}M_1(S)&\rightarrow D_1\\M_2(S)&\rightarrow D_2\\M_3(S)&\rightarrow D_3\end{aligned}
$$

ZPP permits:

$$
D_1\neq D_2\neq D_3
$$

The relevant invariant is that:

$$
\begin{aligned}\operatorname{source}(D_1)&=S\\\operatorname{source}(D_2)&=S\\\operatorname{source}(D_3)&=S\end{aligned}
$$

remains attributable where those outputs are represented as derivations from $S$.

This is the relationship between SLA and differentiated processing.

Different systems may reason differently without corrupting the identity of what they reasoned about.

Hence:

Source locking is not reasoning locking.

---

## 14. Local-First Execution

The original ZPP specification described deployment as exclusively air-gapped and independent of public cloud infrastructure.

The current SLA principle is more general:

Local-first does not mean information-isolated.

The local runtime remains the primary trusted environment for protected persistent architectural state.

External systems may supply:

- information
- computation
- models
- reasoning
- observations
- verification

but those contributions cross an explicit architectural boundary.

The distinction is:

```text
EXTERNAL CONTRIBUTION
         ↓
ATTRIBUTABLE INGRESS
         ↓
LOCAL PROCESSING / EVALUATION
         ↓
AUTHORIZED STATE BOUNDARY
```

rather than:

```text
external system
      ↓
automatic authority
```

Air-gapped execution remains useful as an experimental configuration.

It is no longer a universal requirement of ZPP.

---

## 15. Cryptographic Identity and Signed Transport

Cryptography provides one implementation mechanism for provenance.

The current ZPP runtime uses Ed25519 identities and signed message envelopes.

Cryptographic signatures can establish that:

a particular key signed a particular payload

They cannot establish that:

the payload is semantically correct

the signer reasoned correctly

the source is truthful

the resulting interpretation should become authoritative

This boundary is important.

Cryptography establishes attributable transport and identity relationships.

Semantic evaluation remains a separate problem.

Accordingly:

A valid signature proves provenance properties—not truth.

This prevents cryptographic verification from being inflated into semantic verification.

---

## 16. Hashing and Content Identity

Content hashing provides another deterministic integrity mechanism.

For canonical content $x$:

$$
h=H(x)
$$

a later retrieval $x'$ can be compared:

$$
H(x')=h
$$

to determine whether the canonicalized content has changed under the declared hashing procedure.

This supports:

- change detection
- duplicate rejection
- retrieval lineage
- source version tracking
- state comparison

It does not establish the semantic truth of the content.

The current multi-agent implementation uses this principle in changed-only source ingestion.

That implementation demonstrates how SLA can become operational without requiring the architecture to control how a model reasons about the retrieved source.

---

## 17. Authorized Mutation

Protected state should have explicit mutation semantics.

A proposed change may be represented as:

$$
\Delta S=S_{t+1}-S_t
$$

but the existence of a proposed $\Delta S$ does not mean it should be applied.

An implementation may require:

- valid source identity
- valid provenance
- authorized role
- acceptable sequence
- required verification
- absence of stale-state conflict
- successful persistence

before applying the transition.

Different classes of state may use different requirements.

This is deliberate.

ZPP does not require one universal global gate through which every operation must pass.

The invariant is narrower:

Protected state changes through its authorized mutation boundary.

---

## 18. Failure Must Remain Legible

A system that silently guesses when required evidence is missing may preserve operational continuity while destroying epistemic continuity.

SLA prefers an explicit unresolved state.

For a mutation requiring conditions $C$:

$$
C=\{c_1,c_2,\ldots,c_n\}
$$

if a required condition cannot be established, the architecture should preserve:

**UNRESOLVED** or **REJECTED**

rather than silently fabricating the missing condition.

This does not mean every model response needs permission to exist.

The rule applies to operations affecting protected architectural state.

Thus failure visibility protects state without becoming a generalized reasoning gate.

---

## 19. ZPP Is Not a Mandatory Global State Machine

The June specification represented ZPP using fixed states:

- `COHERENT_GRID`
- `COMPRESSED_GRID`
- `DETERMINISTIC_LOCK`
- `DIVERGENT_STATE`

Those states belong to an earlier implementation generation.

They are not required architectural states of current ZPP.

The current architecture instead permits local role-specific states and attributable transitions.

For example:

```text
SOURCE IDENTIFIED
          ↓
SOURCE REFERENCED / PERSISTED
          ↓
reasoning / evaluation / verification
          ↓
PROPOSED STATE CHANGE
          ↓
AUTHORIZED MUTATION
          ↓
     ┌────┴─────────────┐
     ↓                  ↓
   APPLIED        REJECTED / UNRESOLVED
     └────┬─────────────┘
          ↓
LINEAGE PRESERVED
```

A runtime may implement state machines where useful.

ZPP itself does not require one universal lifecycle.

---

## 20. ZPP Is Not a Scoring Function

The June specification tightly coupled ZPP to:

$$
S=w_1C+w_2E+w_3(1-D)
$$

with:

$$
w_1=0.40,\quad w_2=0.20,\quad w_3=0.40
$$

and routing thresholds:

$$
\tau_\alpha=0.5350,\qquad\tau_\gamma=0.6400
$$

The associated experiments were historically important.

In particular, replacing a sigmoid-transformed score with the linear form expanded the measured score range in the documented calibration experiment.

But this establishes an implementation result, not a permanent ZPP invariant.

The correct lineage is:

```text
problem observed
       ↓
scalar scoring prototype
       ↓
sigmoid compression observed
       ↓
linear scoring revision
       ↓
later scoring generations
       ↓
current decomposition of
observation / projection / action
```

Therefore:

ZPP does not depend on Gamma, Alpha, a linear score, a particular threshold, or any permanent scalar projection.

Those mechanisms remain part of the experimental lineage.

They do not define SLA.

---

## 21. ZPP Is Not a Consensus Algorithm

The original specification also coupled ZPP to a fixed 2/2 multi-signature consensus mechanism.

That mechanism represented an early attempt to prevent unilateral state advancement.

The underlying principle survives:

consequential state changes should not silently acquire authority merely because one process generated them.

The fixed mechanism does not.

Current ZPP does not require:

- 2/2 consensus
- majority voting
- unanimity
- one permanent leader
- one permanent Trust Circle

Different state boundaries may require different evidence and authorization.

Likewise:

Consensus does not create truth.

Agreement may provide evidence of convergence.

It is not equivalent to deterministic verification.

---

## 22. ZPP Is Not RAFT

The June specification described RAFT-based mesh coordination as a defining component.

That should now be preserved as historical architecture rather than current ZPP doctrine.

The durable requirement is not:

USE RAFT

It is:

- make coordination explicit
- preserve state ownership
- make authority attributable
- handle failure legibly
- preserve lineage

A later architecture may use:

- leader election
- role-specific authority
- event-driven coordination
- consensus
- direct signed handoff
- or another mechanism

without ceasing to implement ZPP principles.

This is an important maturation of the specification:

An implementation mechanism should not become an architectural invariant merely because it successfully exposed the invariant during an earlier prototype.

---

## 23. Relationship to Current Multi-Agent Architecture

The present six-node runtime provides one implementation surface for ZPP/SLA.

Its current functional decomposition can be represented as:

```text
           SOURCE
              ↓
       D — discovery
              ↓
        E — retrieval
              ↓
    attributable content
        ↙     ↓     ↘
       A      B      C
           evaluation
              ↓
     authorized dispatch
              ↓
        F — reasoning
              ↓
       persistent state
```

Additional internet ingress can enter through an attributable boundary at F.

Each role owns a narrower responsibility.

No individual node is SLA.

SLA is expressed through the relationships among:

- source identity
- retrieval lineage
- signed exchange
- role ownership
- local persistence
- execution identity
- evidence
- authorized state transition

The current architecture may therefore replace a model or role occupant without replacing the source lineage.

---

## 24. Role Separation

Specialized roles provide one way to reduce authority collapse.

Consider discovery and retrieval.

A discovery component may establish:

source X exists.

A retrieval component may establish:

content Y was retrieved from source X at time t.

A validator may establish:

measurement Z was produced for Y.

A reasoner may establish:

derivation D was generated from Y.

These statements are related.

They are not interchangeable.

The architecture becomes more auditable when the system does not silently compress them into:

“the AI knows D.”

ZPP instead preserves the chain of transformations that produced D.

---

## 25. Persistent State Without Identity Lock

Persistent architecture does not require permanent agent identity.

Suppose NODE_F currently uses model $M_1$.

Later it uses $M_2$.

If the architecture preserves:

- role
- source lineage
- prior state
- model/configuration identity
- transition record
- result provenance

then continuity can survive the replacement.

The system should not pretend:

$$
M_1=M_2
$$

Nor does it need to.

What persists is the recoverable relationship among states.

This allows architecture to evolve without requiring one model, persona, or process to remain permanently attached to a role.

---

## 26. Differentiated Convergence

ZPP permits independent systems to produce differentiated results.

Given:

$$
D_A,\ D_B,\ D_C
$$

the architecture may observe:

$$
D_A\approx D_B\approx D_C
$$

for some defined structural property.

That is convergence.

It is not automatically verification.

Conversely:

$$
D_A\neq D_B
$$

does not automatically represent system failure.

Disagreement may expose:

- ambiguity
- different assumptions
- different reasoning paths
- measurement instability
- model-specific behavior
- or an actual error

SLA preserves the source against which those outputs can be compared.

This permits differentiation without losing the reference frame.

---

## 27. Relationship to Trust Circle

Trust Circle and SLA answer different questions.

### SLA

What state is authoritative, where did it originate, and under what conditions may it change?

### Trust Circle

What can independent evaluation and available evidence establish about a claim or state?

A Trust Circle may contribute evidence to a state transition.

It does not become source authority merely because multiple evaluators agree.

Thus:

```text
SOURCE AUTHORITY
        ≠
EVALUATOR AGREEMENT
        ≠
DETERMINISTIC VERIFICATION
```

Each has a distinct role.

---

## 28. Relationship to SCI

The Semantic Coherence Index and ZPP also occupy different architectural layers.

SCI asks:

What can be measured about semantic behavior over time, transformation, runtime conditions, and model boundaries?

ZPP asks:

How can source identity, provenance, state, and authorized mutation remain attributable while those processes occur?

SCI therefore provides measurement.

ZPP provides architectural boundaries.

Neither should automatically become the other's control mechanism.

A possible relationship is:

```text
SOURCE / STATE
      ↓
ZPP-preserved execution
      ↓
SCI observations
      ↓
measurement / estimator
      ↓
evidence
      ↓
possible proposed state change
      ↓
ZPP mutation boundary
```

SCI evidence may inform a transition.

An SCI score does not automatically acquire authority to mutate state.

---

## 29. Schema and Lineage

The current canonical metadata is:

```yaml
schema_version: zpp.entropy.char.nfc.v1
lineage_tracking: zpp-core-mainnet
```

The schema identifier provides versioned technical context.

It is not itself a grammar constraint, deterministic lock, semantic state, or reasoning mechanism.

The June specification conflated the schema identifier with GBNF-style grammar enforcement.

That interpretation should be retired.

Likewise, zpp-core-mainnet represents the continuing architectural lineage.

Changes to:

- scoring
- weights
- model backends
- agent roles
- network topology
- projection functions
- coordination behavior

do not necessarily constitute new lineages.

A lineage transition should represent a meaningful break in the architecture's provenance—not ordinary evolution inside it.

---

## 30. Historical Linear Scoring Experiment

The original linear-scoring experiment remains useful as an architectural lineage artifact.

The initial implementation applied nonlinear compression to a scoring range and produced:

| Metric                    | Sigmoid | Linear |
| ------------------------- | ------: | -----: |
| Code prompt               |  0.6226 | 0.5089 |
| Threat prompt             |  0.6413 | 0.7500 |
| Observed range (reported) |  0.0187 | 0.1754 |

The resulting range expanded by approximately:

$$
\frac{0.1754}{0.0187}\approx 9.38
$$

under the reported calibration samples.

The defensible conclusion is narrow:

For the documented scoring implementation and calibration samples, removing the sigmoid transformation increased separation in the resulting scalar scores.

It does not establish that linear scoring universally preserves semantic structure.

Nor does it establish that ZPP requires linear scoring.

Preserving this experiment with its proper scope strengthens rather than weakens the architectural history.

---

## 31. Historical Consensus and Routing Mechanisms

The same treatment applies to several mechanisms in ZPP v1.0.

| v1.0 mechanism                  | Current status                       |
| ------------------------------- | ------------------------------------ |
| Linear C/E/D routing score      | Historical scoring generation        |
| Alpha/Gamma thresholds          | Historical calibration               |
| Fixed four-state runtime        | Historical implementation            |
| Grammar lock                    | Retired as ZPP invariant             |
| 2/2 multisignature consensus    | Historical governance implementation |
| RAFT coordination               | Historical mesh implementation       |
| Mandatory air gap               | Refined to local-first               |
| Deterministic inference         | Refined to deterministic integrity   |
| Ed25519 provenance              | Survives in current implementation   |
| Persistent local state          | Survives and expanded                |
| Source locking                  | Survives and substantially refined   |
| Cryptographic lineage           | Survives and expanded                |
| Semantic preservation objective | Survives                             |
| Explicit state boundaries       | Survives and strengthened            |

This distinction allows the research lineage to remain visible without pretending every prototype mechanism survived.

---

## 32. Architectural Invariants

The current ZPP/SLA architecture can be summarized through a smaller set of durable invariants.

### Source attribution

Protected source-derived state remains traceable to its source.

### Provenance

Significant transformations remain attributable.

### Protected mutation

Receiving, reasoning about, or evaluating information does not automatically confer permission to rewrite protected state.

### Persistent lineage

State transitions preserve enough history to reconstruct relevant change.

### Differentiated reasoning

Reasoners may produce different interpretations without silently changing source identity.

### Evidence preservation

Established evidence remains historically attributable even when challenged or superseded.

### Determinism where required

Integrity mechanisms may be deterministic without requiring deterministic generation.

### Legible failure

Missing evidence or failed authorization remains observable rather than being silently converted into valid state.

### Local-first authority

External contribution does not silently transfer authority over protected local state.

### Replaceable mechanisms

No scorer, model, consensus algorithm, node topology, or routing implementation is itself synonymous with ZPP.

---

## 33. What ZPP Does Not Claim

The refined architecture narrows several claims from the original specification.

- ZPP does not guarantee semantic correctness.
- ZPP does not make probabilistic models deterministic.
- ZPP does not guarantee that a trusted source is factually correct.
- ZPP does not establish truth through consensus.
- ZPP does not establish semantic validity through cryptographic signature.
- ZPP does not eliminate semantic drift merely by preserving provenance.
- ZPP does not require air-gapped execution.
- ZPP does not require one scoring function.
- ZPP does not require one consensus mechanism.
- ZPP does not require one permanent leader.
- ZPP does not require one permanent model.
- ZPP does not prevent reasoning systems from being wrong.

Instead, ZPP attempts to make the relationships surrounding those processes attributable, persistent, inspectable, and recoverable.

---

## 34. Validation Model

Because ZPP now distinguishes architectural invariants from implementation mechanisms, validation should occur property by property.

Examples include:

| Validation target             | Test question                                                                                   |
| ----------------------------- | ----------------------------------------------------------------------------------------------- |
| **Source fidelity**           | Does retrieved content remain attributable to the correct source and version?                   |
| **Signed transport**          | Does payload modification cause signature verification failure?                                 |
| **Changed-only ingestion**    | Does unchanged source material avoid creating a new processing lineage?                         |
| **Persistence**               | Does required state survive restart?                                                            |
| **Lineage**                   | Can a resulting state be traced backward through its significant transitions?                   |
| **Authorized mutation**       | Can an unauthorized component alter protected state?                                            |
| **Failure legibility**        | Does missing required evidence produce an explicit unresolved/rejected state?                   |
| **Model replacement**         | Can a role change its reasoning backend without losing prior state provenance?                  |
| **Differentiated processing** | Can multiple reasoners produce different derivations while retaining the same source reference? |

No single passing test validates the entire architecture.

Each test establishes evidence for a specific property under specified conditions.

---

## 35. Current Evidence Status

The present research program supports different ZPP properties at different evidence levels.

| Property                                  | Status                                |
| ----------------------------------------- | ------------------------------------- |
| Source-Locked Architecture                | DEFINED / CURRENT                     |
| Local-first state model                   | IMPLEMENTED                           |
| Node-local persistence                    | IMPLEMENTED / OBSERVED                |
| Ed25519 node identity                     | IMPLEMENTED                           |
| Signed transport                          | IMPLEMENTED / OBSERVED                |
| Source discovery/retrieval separation     | IMPLEMENTED / OBSERVED                |
| Content hashing                           | IMPLEMENTED                           |
| Changed-only ingestion                    | IMPLEMENTED / LIVE VALIDATION PENDING |
| Persistent lineage mechanisms             | IMPLEMENTED IN PART                   |
| Role-separated execution                  | IMPLEMENTED / OBSERVED                |
| Singular downstream execution             | IMPLEMENTED / OBSERVED                |
| Probabilistic local reasoning             | IMPLEMENTED / OBSERVED                |
| Automatic live reasoning persistence      | INCOMPLETE / TEST PENDING             |
| Source-fidelity validation suite          | PENDING                               |
| Tamper test                               | PENDING                               |
| Restart recovery test                     | PENDING                               |
| Model-replacement continuity test         | PENDING                               |
| Universal semantic-preservation guarantee | NOT CLAIMED                           |

This evidence model prevents implementation from being mistaken for proof.

---

## 36. Current Research Direction

The current ZPP research direction is not toward adding additional global control mechanisms.

It is toward making boundaries clearer.

Several active questions follow directly from that goal.

- Can raw runtime observations remain stable while projection weights change?
- Can validator authority adapt without confusing scoring state with coordination state?
- Can model backends rotate while persistent lineage remains intact?
- Can source-derived state be reconstructed without preserving every transient execution detail?
- Can external information enter the architecture without silently acquiring source authority?
- Can reasoning remain minimally constrained while protected state remains strictly attributable?

These questions are compatible with a general design principle:

Protect the state boundary rather than unnecessarily controlling the reasoning path.

---

## 37. Architectural Evolution

ZPP's development can therefore be represented as a sequence of increasingly precise decompositions:

```text
SEMANTIC DRIFT OBSERVATION
          ↓
ROUTING / SCORING PROTOTYPES
          ↓
DETERMINISTIC STATE CONTROL
          ↓
CRYPTOGRAPHIC GOVERNANCE
          ↓
DISTRIBUTED EXECUTION
          ↓
PERSISTENT ROLE-SPECIFIC STATE
          ↓
SOURCE / DERIVATION / EVIDENCE SEPARATION
          ↓
SOURCE-LOCKED ARCHITECTURE
```

This history matters.

The later architecture did not appear because the earlier prototypes were irrelevant.

The prototypes made architectural requirements observable.

But a mechanism that reveals a principle does not necessarily need to survive after the principle has been isolated.

That distinction is central to the current ZPP specification.

---

## 38. Conclusion

The Zero-Point Protocol began as an attempt to preserve semantic integrity through deterministic routing, scoring, cryptographic governance, persistent state, and distributed coordination.

Implementation progressively exposed a deeper architectural boundary.

The system did not need every reasoner to be deterministic.

It did not need every node to agree.

It did not need one permanent score, leader, state machine, consensus mechanism, or network topology.

It needed to preserve the relationships that allow a changing distributed system to know:

- WHAT WAS THE SOURCE?
- WHAT WAS DERIVED FROM IT?
- WHAT EVIDENCE EXISTS?
- WHAT STATE IS CURRENTLY PRESERVED?
- WHO OR WHAT CHANGED THAT STATE?
- WAS THE CHANGE AUTHORIZED?
- CAN THE TRANSITION BE RECONSTRUCTED?

Source-Locked Architecture formalizes those relationships.

Its central invariant is:

Source identity and provenance remain invariant while reasoning over that source may remain probabilistic.

From that invariant follows a broader systems architecture:

```text
SOURCE
   ↓
ATTRIBUTABLE INGESTION
   ↓
PERSISTENT REFERENCE
   ↓
DIFFERENTIATED REASONING
   ↓
EVIDENCE / EVALUATION
   ↓
PROPOSED CHANGE
   ↓
AUTHORIZED MUTATION
   ↓
PRESERVED LINEAGE
```

The resulting architecture does not attempt to eliminate probabilistic reasoning.

It establishes deterministic integrity where deterministic integrity is useful.

It does not prevent disagreement.

It preserves the source against which disagreement can be evaluated.

It does not convert consensus into truth.

It keeps evidence distinguishable from agreement.

It does not require a permanent model identity.

It preserves continuity through recoverable state and lineage.

And it does not protect source integrity by controlling every thought produced about the source.

It protects the boundary at which a derivation would otherwise become state.

That is the current architectural form of ZPP:

reasoning may move; provenance must remain attributable.

interpretation may change; source identity must not silently change with it.

state may evolve; lineage must preserve how it evolved.
