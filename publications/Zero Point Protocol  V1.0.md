## From Linear Risk Routing to Cryptographic Governance and Distributed Grid Forking

_A Retrospective Technical Evaluation of Scoring, Calibration, Consensus, Orchestration, and Architectural Evolution_

**Author:** Tara Callegari
**Organization:** The Observatory

_Historical Technical Research Report | October 2026_

**Version:** v1.0 
**Research Status:** Active Research  
**Historical Development Period:** May–June 2026  
**Architecture Lineage:** `zpp-core-mainnet`  
**Entropy Schema:** `zpp.entropy.char.nfc.v1`
**Published:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23651309.svg)](https://doi.org/10.5281/zenodo.23651309)

---

# Abstract

This paper examines the early technical development of the Zero-Point Protocol (ZPP), an experimental architecture designed to classify input signals, select processing routes, preserve decision provenance, and coordinate validation across local and distributed language-model systems.

The investigation developed from earlier longitudinal observations of semantic drift, inconsistent model behavior, cross-model transformation, and the limitations of conventional conversational evaluation. The resulting engineering work introduced a deterministic scoring framework combining intent, normalized entropy, and distance-related features. Initial implementation exposed a nonlinear compression problem in which sigmoid-transformed scores occupied an insufficiently discriminating interval. This motivated a direct linear scoring function and subsequent threshold calibration.

The refined router employed three execution classifications—BETA, ALPHA, and GAMMA—with documented weights of 0.40, 0.20, and 0.40 and calibrated boundaries of 0.5350 and 0.6400. A 24-prompt validation set spanning two locally evaluated model configurations supplied the initial documented routing tests. Subsequent development extended the architecture through canonical feature definitions, cryptographic identity and signing specifications, 2/2 multi-signature consensus, hash-linked audit records, explicit manual-override events, fork-aware lineage, and distributed transport.

The historical record also documents a progression from simulated multi-node arrangements to locally orchestrated, multi-port TCP execution. These stages must be distinguished from full cryptographic federation, independently replicated distributed operation, or validated semantic preservation under arbitrary conditions.

Cross-node execution comparisons exposed an additional measurement problem: nominally equivalent Shannon entropy calculations produced different scores when normalization conventions differed. This motivated a canonical Unicode-normalized character-entropy definition and schema-level feature binding.

The paper reconstructs the architectural development, identifies documented implementation and validation outcomes, and examines unresolved questions concerning calibration generalization, cryptographic verification, source fidelity, distributed governance, and fork reconciliation.

Its principal contribution is a technically bounded account of the emergence of ZPP as an executable routing and governance architecture, including the failures and measurement disagreements that shaped its implementation.

**Keywords:** Zero-Point Protocol, deterministic routing, Shannon entropy, calibration, risk classification, distributed consensus, Ed25519, hash-chain lineage, orchestration, mesh networking, fork detection, experimental reproducibility

---

# 1. Introduction

Language-model systems may be incorporated into processing environments that require decisions extending beyond generation of an individual response.

An incoming request may require classification, contextual evaluation, deterministic verification, additional review, or coordination across multiple components.

The resulting engineering problem concerns both the content being processed and the architecture responsible for deciding how processing occurs.

The original Zero-Point Protocol research addressed this problem through an experimental framework combining scoring, routing, provenance, and distributed validation.

Rather than treating all inputs as requiring identical processing, ZPP attempted to assign routes according to measurable input features and calibrated decision boundaries.

The earliest technical implementation combined three features: an intent-related value, a normalized entropy estimate, and a distance-related quantity associated with the scoring model.

The resulting score was used to select one of three processing routes.

However, constructing a scoring function introduced further problems.

The transformation applied to raw feature values could compress distinctions required by the router.

The scoring procedure depended on features whose definitions were not yet fully standardized.

And as the architecture expanded, the decisions made at one node needed to remain attributable and distinguishable from decisions made elsewhere.

These problems motivated successive technical developments.

The routing system required improved calibration.

The scoring procedure required canonical feature definitions.

Distributed validation required identity and consensus mechanisms.

Persistent audit records required explicit lineage.

Divergent node states required isolation and reconciliation rules.

The architecture eventually extended into locally orchestrated, multi-port communication.

This paper examines those developments through the historical ZPP technical record.

It distinguishes design intent, implemented mechanism, observed execution, simulation, and validated behavior.

The purpose is not to assert that the final architecture solved all semantic-integrity problems.

It is to determine what was built, what was tested, what failed, and which technical requirements emerged from those results.

---

# 2. Sources, Scope, and Historical Method

## 2.1 Source Documents

The principal sources are the original ZPP white paper and the expanded Complete Master Document.

These documents preserve overlapping but nonidentical stages of the protocol.

The earlier technical record includes scoring calibration, cryptographic governance, consensus simulations, and the transitional Phase 3 grid architecture.

The expanded master record includes later descriptions of active orchestration, multi-port TCP execution, asynchronous processing, and node-level forking behavior.

The differences between these sources are relevant to the historical analysis.

They must not be flattened into one implementation state.

## 2.2 Scope

The paper focuses on the early development of:

- Risk scoring, threshold calibration, and route classification.
    
- Mathematical and measurement failures in the original scoring system.
    
- Canonical feature specification.
    
- Cryptographic signing and event integrity.
    
- Multi-signature consensus and state transitions.
    
- Audit-chain lineage and manual overrides.
    
- Distributed topology, orchestration, and transport.
    
- Fork detection, isolation, and proposed reconciliation.
    
- Cross-model technical execution comparisons.
    

Later investigations into extensive functional Engine decomposition are outside this paper's scope.

The historical existence of a runtime or interface component does not require incorporating subsequent experiments involving that component.

## 2.3 Evidence Classification

For this retrospective analysis, technical claims are separated into four categories.

**Specified:** A mechanism or property is described in the design documentation.

**Implemented:** A corresponding code component or configuration is identified.

**Observed:** A preserved execution artifact reports the mechanism operating.

**Validated:** A defined test supplies expected and observed outcomes sufficient to evaluate the specified property.

The existence of source code does not alone establish correct execution.

Similarly, a successful simulated consensus does not establish production-ready distributed cryptographic federation.

This classification is used to prevent later implementation maturity from being attributed retrospectively to earlier versions.

---

# 3. Initial Scoring Architecture

### Historical Prototype Lineage — Early Routing and Agent Tools

The surviving Pattern Observatory archive preserves an earlier generation of Zero-Point Protocol prototypes developed before the final scoring and routing configuration.

The original Ollama-based router combined embedding-distance calculations, word-level entropy, and an intent parameter using weights of 0.80, 0.05, and 0.15. Its sigmoid-based classification used thresholds of 0.56 and 0.82.

Code inspection identifies an important limitation: with the intent parameter fixed at 0.1 and the implemented feature bounds, the maximum attainable sigmoid score was approximately 0.5695. Consequently, the GAMMA threshold of 0.82 was unreachable under those conditions.

This prototype provides historical context for the subsequent scoring revisions, including the transition to linear scoring and recalibrated routing boundaries.

The archive also preserves an early agent-tool architecture consisting of workspace indexing, text search, voice transcription, screenshot reading, and direct file retrieval. The historical orchestrator integrated text-search functionality with local model inference and conversation memory. Other tools were implemented and reportedly tested but later removed from the active environment.

Subsequent development introduced structured SQLite persistence alongside earlier flat-file conversation storage, while the broader ZPP architecture evolved toward calibrated routing, cryptographic signing, consensus, and distributed orchestration.

An intermediate archived configuration also records weights of 0.40, 0.30, and 0.30 with thresholds of 0.15 and 0.85. Its precise operational relationship to the final calibration remains unverified.

These artifacts document the protocol's developmental history. They are not additional validation results and do not alter the calibrated findings reported in the following sections.

## 3.1 Feature-Based Risk Representation

The original router defined a scalar score combining three feature values:

$$
\boxed{  
z(x)=w_1C(x)+w_2E(x)+w_3(1-D(x))  
}  
$$

where:

- $C(x)$ denotes the intent-related feature.
    
- $E(x)$ denotes normalized entropy.
    
- $D(x)$ denotes the distance-related feature.
    
- $w_1,w_2,w_3$ denote their respective weights.
    

The feature terms belong to the historical ZPP scoring specification.

The archived record does not, by itself, establish an independently validated semantic interpretation for every numerical feature assignment.

In particular, the procedure used to construct $C(x)$ and $D(x)$ requires source-code and test-vector verification.

## 3.2 Original Nonlinear Mapping

The initial router applied a sigmoid transformation:

$$
\boxed{  
S_\sigma(x)=\frac{1}{1+e^{-z(x)}}  
}  
$$

This transformation maps real-valued input scores into the interval between zero and one.

Mathematically, the sigmoid is monotonic.

It therefore does not reverse the ordering of exact input values.

However, its local slope varies:

$$S_\sigma(1-S_\sigma)  $$

When the tested inputs occupy a narrow portion of the transformed range, the resulting score separations may become too small for the chosen decision boundaries and numerical resolution.

The historical ZPP experiments encountered precisely this calibration problem.

## 3.3 The Sigmoid Compression Trap

The early routing record documented scores of approximately:

| Test category          | Recorded sigmoid score |
| ---------------------- | ---------------------- |
| Pure technical code    | 0.6226                 |
| Infrastructure fiction | 0.6344                 |
| Critical threat test   | 0.6413                 |

The observed score spread was:

$$0.6413-0.6226  $$

$$
\boxed{  
\Delta S_\sigma=0.0187  
}  
$$

The problem was not that these values were identical.

It was that the tested categories occupied a narrow interval relative to the routing configuration and the desired classification boundaries.

The record describes inappropriate or unstable routing of cases that the experimental labels intended to distinguish.

This finding was termed the **Sigmoid Compression Trap**.

### Interpretation

The sigmoid transformation did not inherently make correct classification mathematically impossible.

A monotonic transformation can be accompanied by appropriately transformed decision thresholds.

The documented failure therefore concerns the interaction among the raw score distribution, nonlinear mapping, threshold calibration, and intended route labels.

The source code and exact before-and-after calibration rules are required to determine the full causal contribution of each factor.

Nevertheless, the compressed empirical score interval was a measurable implementation problem.

---

# 4. Linear Scoring and Threshold Calibration

## 4.1 Removal of the Nonlinear Mapping

The subsequent implementation removed the sigmoid from the routing score.

The resulting rule was:

$$
\boxed{  
S(x)=z(x)  
}  
$$

or:

$$
\boxed{  
S(x)=w_1C(x)+w_2E(x)+w_3(1-D(x))  
}  
$$

The linear formulation retained the weighted feature combination without applying the final logistic compression.

This allowed the raw score differences to remain directly available for threshold comparison.

## 4.2 Final Recorded Weights

The historical calibration produced:

| Parameter               | Recorded value |
| ----------------------- | -------------- |
| Intent weight (w_1)     | 0.40           |
| Entropy weight (w_2)    | 0.20           |
| Distance weight (w_3)   | 0.40           |
| ALPHA boundary (\alpha) | 0.5350         |
| GAMMA boundary (\gamma) | 0.6400         |

The weights satisfy:

$$
w_1+w_2+w_3=1  
$$

The final score becomes:

$$
\boxed{  
S(x)=0.40C(x)+0.20E(x)+0.40(1-D(x))  
}  
$$

The reported calibration assigned equal total weight to the intent and distance-related features, with entropy contributing the remaining fifth of the score.

These values were calibration results for the historical ZPP implementation.

They are not universal optimal weights for unrelated language-model tasks.

## 4.3 Recorded Dynamic-Range Expansion

The archived analysis reports expansion from a compressed interval of 0.0187 to a post-revision interval of approximately 0.1754.

The ratio is:

$$
\frac{0.1754}{0.0187}  
\approx9.38  
$$

The historical report rounded this to a **9.4-fold increase** in score spread.

This is an arithmetic comparison between the recorded ranges.

It does not independently establish improved classification on an unseen test population.

Such a claim would require matched before-and-after evaluations with consistent target labels and scoring definitions.

## 4.4 Routing Boundaries

The calibrated router defined three score regions:

$$
\boxed{  
\operatorname{Route}(x)=  
\begin{cases}  
\mathrm{BETA}, & S(x)<\alpha\  
\mathrm{ALPHA}, & \alpha\leq S(x)<\gamma\  
\mathrm{GAMMA}, & S(x)\geq\gamma  
\end{cases}  
}  
$$

with:

$$
\alpha=0.5350  
$$

and:

$$
\gamma=0.6400  
$$

The historical system used BETA for lower-scoring inputs, ALPHA for intermediate cases, and GAMMA for inputs requiring critical-path escalation.

The precise processing behavior of each route depended on the corresponding protocol version.

Route classification should therefore be distinguished from later orchestration and execution-state transitions.

---

# 5. Automated Threshold Tuning

The ZPP calibration procedure introduced an optimization objective that weighted false negatives more heavily than false positives.

The recorded objective was:

$$
\boxed{  
\min_{\alpha,\gamma}  
\left[  
w_{\mathrm{FP}}\operatorname{FP}(\alpha,\gamma)  
+  
w_{\mathrm{FN}}\operatorname{FN}(\alpha,\gamma)  
\right]  
}  
$$

with:

$$
\boxed{  
w_{\mathrm{FN}}=3w_{\mathrm{FP}}  
}  
$$

The design therefore imposed a threefold penalty on the specified false-negative classification.

This was a policy choice embedded in the experimental objective.

It was not a statistical property learned independently from arbitrary future data.

The original documentation describes a region of threshold values with zero weighted classification cost on the labeled calibration data.

The selected values were:

$$
\alpha=0.5350,\qquad\gamma=0.6400  
$$

## 5.1 Interpretation of Zero Cost

A reported calibration cost of zero means that the tested labels and route predictions satisfied the chosen objective within the relevant experimental set.

It does not imply zero semantic drift across all inputs.

It does not imply zero false negatives on a different prompt population.

And it does not independently validate the ground-truth labels.

The correct conclusion is bounded to the specified data, objective, and parameter definitions.

## 5.2 Calibration Reproducibility

Reproduction requires the complete prompt set, exact feature calculations, expected route labels, candidate threshold search procedure, and implementation version.

Without these materials, the reported threshold values can be inspected and used, but the optimization result cannot be independently regenerated in full.

---

# 6. Initial Routing Validation

The historical ZPP record identifies a validation set containing 24 prompts, labeled P001–P024.

The documented testing period was May 18–20, 2026.

Two local model configurations were used:

- Llama 3 8B, quantized.
    
- Mistral 7B, quantized.
    

The record identifies router version ZPP v1.0 and event schema `zpp.event.v1`.

## 6.1 Preserved Example Outcomes

| Test                             | Model   | Score  | Expected | Recorded |
| -------------------------------- | ------- | ------ | -------- | -------- |
| P001 — Linked-list code          | Llama 3 | 0.5089 | BETA     | BETA     |
| P002 — Linked-list code          | Mistral | 0.3205 | BETA     | BETA     |
| P003 — Facial-recognition ethics | Llama 3 | 0.6273 | ALPHA    | ALPHA    |
| P004 — Biometric fiction         | Mistral | 0.6843 | GAMMA    | GAMMA    |
| P005 — Critical threat test      | Llama 3 | 0.6413 | GAMMA    | GAMMA    |
| P006 — Critical threat test      | Mistral | 0.7500 | GAMMA    | GAMMA    |

These examples demonstrate that the recorded scores and route labels agree with the final threshold rule.

The document describes the remaining validation prompts collectively rather than displaying every test row in its summarized table.

Therefore, the complete 24-prompt accuracy calculation should be reproduced from the underlying test vectors or logs before publication.

## 6.2 Scope of the Result

The initial validation supports the existence of a functioning local scoring and routing workflow under the documented configurations.

The two model configurations provide an early cross-backend comparison.

However, this does not establish universal model independence or robust transfer across arbitrary tokenizers, prompts, or model families.

The strength of the claim depends upon how the scoring features were computed and whether the implementation treated model-specific outputs differently.

---

# 7. Entropy as a Canonical Measurement Problem

A later cross-node execution exercise revealed that participants could correctly discuss entropy while producing different normalized entropy values.

The disagreement arose partly from the normalization basis.

Let $p_c$ denote the empirical probability of character $c$ in a string.

The Shannon entropy is:

$$
\boxed{  
H(x)=-\sum_{c\in\Sigma_x}p_c\log_2p_c  
}  
$$

A normalized quantity requires an additional denominator.

The ZPP records encountered at least two such conventions.

## 7.1 Unique-Character Normalization

One method used:

$$\frac{H(x)}{\log_2|\Sigma_x|}  $$

where $\Sigma_x$ is the set of distinct characters appearing in the evaluated string.

## 7.2 Fixed Alphabet Normalization

Another used a fixed ASCII-oriented maximum:

$$\frac{H(x)}{\log_2(95)}  $$

Both expressions can be defined mathematically.

They are not numerically interchangeable.

Their denominators encode different assumptions about the reference alphabet.

## 7.3 Recorded Cross-Node Divergence

For the original technical test prompt involving reversal of a linked list, the master record reports:

$$
H(x)\approx3.9447738350  
$$

and:

$$
|\Sigma_x|=20  
$$

yielding:

$$
E_{\mathrm{unique}}(x)\approx0.912730  
$$

Other participants using the fixed ASCII maximum or alternative definitions produced different normalized values.

Because entropy contributed directly to the routing score, those differences could change route classifications.

The problem was not necessarily disagreement about the source prompt.

It was disagreement about the measurement definition.

## 7.4 Canonical Feature Binding

The resulting protocol adopted a character-level convention incorporating Unicode NFC normalization, case sensitivity, and inclusion of spaces and punctuation.

The corresponding identifier was:

`zpp.entropy.char.nfc.v1`

This was a significant technical refinement.

A shared scoring formula is not sufficient for reproducibility if its feature functions are underspecified.

The feature definition itself must be versioned and bound to the relevant policy configuration.

## 7.5 Remaining Requirement

The canonical entropy values should be independently reproduced from the exact prompt bytes and the stated Unicode-normalization procedure.

A mathematical definition and a reported numerical result are distinct evidence objects.

Their agreement must be checked rather than assumed.

---

# 8. Cryptographic Governance

As ZPP developed beyond standalone route selection, the architecture required a method for preserving the provenance of routing decisions and proposed state transitions.

The early governance specification introduced cryptographic identity, canonical payload representation, hash-linked records, and multi-signature consensus.

These mechanisms addressed a different problem from semantic classification.

A score determines which processing path is selected.

Cryptographic verification can determine whether a recorded payload matches an attributable signed artifact.

It does not establish that the selected route or underlying semantic interpretation is correct.

## 8.1 Hashing

The architecture used SHA-256 for content and payload integrity operations.

For a canonical payload $P$, the digest can be represented as:

$$
\boxed{  
h=H_{\mathrm{SHA256}}(P)  
}  
$$

Hashing provides a content-derived identifier suitable for integrity comparisons under defined serialization rules.

It does not provide signer authentication on its own.

## 8.2 Ed25519 Signing

The governance design specified Ed25519 asymmetric signatures.

Given a private signing key $sk$ and canonical payload $P$:

$$
\sigma=\operatorname{Sign}_{sk}(P)  
$$

Verification uses the corresponding public key $pk$:

$$
\operatorname{Verify}_{pk}(P,\sigma)  
$$

A valid signature supports attribution to the holder of the relevant signing key, subject to the key-management assumptions.

It does not establish semantic correctness.

## 8.3 Historical Implementation Distinction

The early documents contain descriptions of both Ed25519 signing and a native fallback based on Python hashing primitives.

These operations must not be conflated.

A SHA-256 digest does not become an Ed25519 signature merely because it is produced from canonical JSON.

The historical record therefore requires a version-by-version audit of the implementation.

The audit must determine which versions performed actual asymmetric signing, which used integrity digests, and which transport exercises used placeholder signature fields.

This distinction is necessary for accurate interpretation of the consensus tests.

---

# 9. Trust Circle and 2/2 Consensus

The ZPP governance design introduced a trust-circle mechanism for decisions requiring stronger validation.

The critical GAMMA route was associated with a two-signature requirement.

The intended transition was:

$$
\text{GAMMA proposal}  
\rightarrow  
\text{verification}  
\rightarrow  
\text{quorum decision}  
$$

A valid proposal required the signatures and policy conditions specified by the active consensus configuration.

## 9.1 Consensus Conditions

The historical design required:

$$
\boxed{  
Q_{\mathrm{valid}}\geq2  
}  
$$

for acceptance of a proposal subject to the 2/2 rule.

A numerical signature count alone is insufficient unless the signatures are independently valid, authorized under the relevant policy, and bound to the correct payload.

## 9.2 Conflict States

The early consensus design distinguished five states.

| State      | Meaning                                                |
| ---------- | ------------------------------------------------------ |
| ACCEPT     | Required verification and policy conditions satisfied  |
| QUARANTINE | Incomplete or temporally inconsistent evidence         |
| ESCALATE   | Conflicting or suspicious proposal conditions          |
| FORKED     | Validly formed but incompatible policy lineage         |
| REJECT     | Invalid signature, unknown peer, or malformed proposal |

These states are distinct from the BETA, ALPHA, and GAMMA routing classes.

The route concerns how the input is classified.

The consensus state concerns what happens to a proposal during validation or governance.

## 9.3 Recorded Early Tests

The May 20 technical record includes tests for a lower-risk acceptance path, a GAMMA proposal with a completed two-signature handshake, and rejection of a corrupted signature.

Other conflict states were described or exercised through simulation.

The record does not establish that every conflict type had already been validated under a fully distributed production environment.

The distinction between implemented state logic, simulation, and live execution must remain explicit.

---

# 10. Audit Chains and Manual Overrides

The early architecture introduced event lineage to preserve the relationship between successive decisions.

A chain entry included fields such as:

- `chain_id`
    
- `entry_id`
    
- `prev_hash`
    
- `fork_parent_hash`
    
- timestamp
    
- payload
    

A previous-hash reference provides an integrity relationship between successive records.

For a simplified sequence:

$$
h_i=H(P_i,h_{i-1})  
$$

the resulting chain binds each entry to its predecessor under the declared serialization and hashing scheme.

This does not by itself prevent deletion, substitution of an entire chain, or unauthorized rewriting without additional trust and storage controls.

## 10.1 Manual Override

The governance specification also required explicit recording when a human operator changed a proposed route.

A manual override was represented as a separate event containing the original route, replacement route, target identifier, reason, operator attribution, and timestamp.

The principle was:

**An override should remain visible as an intervention rather than being silently incorporated into the historical routing result.**

This distinguished the automated decision from the human-authorized change.

The record therefore preserved a potentially important measurement boundary: what the machine selected before intervention and what was ultimately accepted afterward.

---

# 11. From Router to Orchestrated Mesh

The distributed phase expanded ZPP beyond the original single-node routing environment.

The historical archive documents a progression from local simulations and peer-designated nodes toward orchestrated processes communicating through TCP sockets.

These were distinct implementation stages.

## 11.1 Local Simulation

The earlier Phase 3 record described simulated or localhost communication, including controlled proposal transmission and verification between locally instantiated nodes.

This demonstrated specific transport and message-processing behavior under local conditions.

It did not establish secure discovery, synchronization, or fault tolerance across independent remote machines.

## 11.2 Process Orchestration

The expanded architecture introduced the `start_mesh.py` controller for launching multiple node processes and directing their logs.

The document describes a six-node asymmetric configuration with designated consensus, relay, observation, and gateway roles.

The precise port mappings varied in the historical material and must be preserved according to implementation version.

The progression from local simulation to locally orchestrated TCP execution constitutes an infrastructure development.

It does not automatically convert the node processes into independent model architectures.

## 11.3 Transport and Validation

The orchestration record identifies core components for scoring, routing, consensus, and TCP message transfer.

A representative workflow was:

$$
\boxed{  
\begin{gathered}  
\text{Input}\  
\downarrow\  
\text{Scoring and route selection}\  
\downarrow\  
\text{Proposal construction}\  
\downarrow\  
\text{Transport to designated peers}\  
\downarrow\  
\text{Validation or isolation}\  
\downarrow\  
\text{Recorded outcome}  
\end{gathered}  
}  
$$

The actual execution path depended on the selected route and protocol state.

Lower-scoring paths did not necessarily require the critical consensus procedure.

GAMMA proposals were designed to trigger stronger validation.

## 11.4 Live Execution Status

The expanded master record contains terminal excerpts showing node-process initialization, input ingestion, routing messages, and telemetry output.

These constitute evidence that the reported local runtime reached particular execution stages.

However, a process-start message does not establish that every peer completed cryptographic verification.

Similarly, local TCP communication does not independently demonstrate remote distributed-network resilience.

The technical report must preserve those evidence boundaries.

---

# 12. Fork Detection and Lineage Isolation

The distributed architecture introduced a new problem.

Nodes could possess incompatible policy versions, divergent histories, or different calibrated configurations.

A successfully transmitted proposal might therefore belong to a different valid lineage.

This was not necessarily equivalent to malformed input.

The architecture required a way to distinguish incompatible lineage from simple corruption.

## 12.1 Fork Identification

The early design used fields such as `chain_id` and `policy_version` to identify the governing lineage and its compatibility conditions.

A valid proposal carrying an incompatible lineage could be assigned to:

$$
\boxed{\mathrm{FORKED}}  
$$

rather than accepted into the current canonical chain.

## 12.2 Isolation

The recorded design directed divergent material into a separate fork directory, preventing automatic merger with the active lineage.

The significance of this behavior was not that all forks were errors.

It was that divergent states could remain identifiable and inspectable without silently overwriting the current record.

Fork isolation is therefore different from fork resolution.

## 12.3 Reconciliation

The archive discussed several possible reconciliation methods, including supersession, cross-fork consensus, trust weighting, and parallel lineage retention.

These approaches were not all implemented or validated.

The earlier technical version explicitly identified automated reconciliation as an open problem.

The expanded record continued to distinguish successful fork detection and isolation from unresolved merge semantics.

Accordingly:

$$
\boxed{  
\text{fork detection}  
\not\Rightarrow  
\text{fork reconciliation}  
}  
$$

This is a central limitation of the early distributed architecture.

---

# 13. Cross-Node Execution and Measurement Disagreement

Beyond local routing tests, the historical record includes an exercise in which multiple model systems were asked to apply the ZPP calculation and explain its cryptographic and consensus procedures.

The exercise examined whether participants could reproduce the protocol's defined operations.

## 13.1 Execution Tasks

The recorded tasks included normalized Shannon entropy, score calculation, route selection, SHA-256 hashing, conceptual Ed25519 signing, and a 2/2 consensus transition.

The exercise therefore combined arithmetic, protocol interpretation, and descriptions of cryptographic operations.

It did not by itself demonstrate that every responding model was connected as a registered participant in the live cryptographic network.

## 13.2 Divergent Entropy Calculations

The most important finding was disagreement in the entropy-normalization basis.

Different participants could apply mathematically coherent methods and still obtain incompatible scores.

Since the score affected route selection, this was not merely cosmetic disagreement.

It exposed an incomplete specification.

The resulting canonical entropy definition became part of the protocol's reproducibility requirements.

## 13.3 Execution Readiness and Network Membership

The expanded report distinguished participants capable of reasoning through the protocol from nodes possessing registered cryptographic identities.

This is an important separation.

An external language model may correctly describe a signing operation.

That does not mean it holds an authorized private key.

A participant may calculate a route correctly.

That does not mean it has executed the router in the local environment.

The relevant evidence classes must therefore remain distinct:

$$
\boxed{  
\text{protocol reasoning}  
\neq  
\text{registered cryptographic participation}  
\neq  
\text{verified network execution}  
}  
$$

---

# 14. Historical Discrepancies Requiring Audit

The early ZPP record is valuable partly because it preserves changing implementation claims and incomplete transitions.

Several require particular attention.

## 14.1 Signature Semantics

Some descriptions identify SHA-256 digests as a native fallback in contexts otherwise described as Ed25519 signing.

The precise implementation must be inspected before claiming successful asymmetric authentication for those versions.

## 14.2 Scoring and Routing Consistency

The final documented thresholds imply BETA for scores below 0.5350.

One expanded runtime excerpt labels a score of 0.4052 as ALPHA.

The discrepancy requires checking the active policy version, route-selection code, and provenance of the logged output.

It cannot be corrected merely by assuming the log or the threshold table is wrong.

## 14.3 Calibration Claims

The stated 9.4-fold expansion follows from the reported score ranges.

Claims of improved classification generalization require additional evidence.

## 14.4 Localhost Versus Remote Distribution

The records include both local simulation and later live multi-process execution.

These are meaningful milestones, but neither alone validates a geographically distributed fault-tolerant mesh.

## 14.5 Cryptographic Identity Versus Conceptual Participation

Correct descriptions of hashing, signatures, and consensus do not establish that all responding external models were registered as cryptographic peers.

## 14.6 Fork Detection Versus Merge

The ability to isolate divergent lineages does not demonstrate correct automatic reconciliation.

## 14.7 Alignment Tax Attribution

The early research used Alignment Tax to describe observed displacement associated with particular behavioral and processing conditions.

However, the archived formula and reported baseline-versus-aligned comparisons require independent measurement provenance and an appropriate causal design before asserting that a specific hidden platform layer produced a measured percentage of semantic degradation.

The technical paper can preserve the diagnostic objective and historical telemetry without treating all causal interpretations as experimentally established.

---

# 15. Architectural Contributions

The early ZPP development produced several identifiable technical contributions.

First, it established a structured classification procedure combining multiple explicitly weighted features.

Second, it documented a calibration failure and replaced the original nonlinear score mapping with a directly thresholded linear score.

Third, it introduced a repeatable routing convention based on fixed boundaries and labeled examples.

Fourth, it exposed feature-definition disagreement during cross-node execution and responded with canonical entropy specification.

Fifth, it developed a governance model distinguishing route classification from cryptographic proposal validation.

Sixth, it introduced explicit audit-chain relationships and manual-override events.

Seventh, it extended the router into local orchestration and multi-node transport.

Eighth, it made policy-lineage divergence an explicit state, permitting isolation of incompatible branches.

These contributions concern separate technical functions.

Their combination formed the early ZPP architecture.

However, implementation of these functions does not establish universal semantic preservation or cryptographic correctness across every version.

The appropriate conclusion is that the research created a concrete engineering system with identifiable mechanisms, tests, limitations, and paths for further validation.

---

# 16. Limitations and Reproducibility Requirements

The source record supports a historical reconstruction but requires additional audits before the paper can be considered a fully reproduced technical evaluation.

The principal outstanding requirements concern:

1. Recovery of all 24 original calibration prompt vectors and expected labels.
    
2. Independent recomputation of $C$, $E$, $D$, score, and route for every case.
    
3. Version-matched comparison of sigmoid and linear scoring.
    
4. Verification of threshold optimization and the reported zero-cost interval.
    
5. Independent replication of canonical entropy results.
    
6. Identification of the exact signing implementations used in each version.
    
7. Re-execution of consensus tests with valid and invalid signatures.
    
8. Inspection of original audit-chain and manual-override artifacts.
    
9. Version-specific comparison of node topology and port configuration.
    
10. Reproduction of fork detection and evidence of successful isolation.
    
11. Documentation of which network tests were simulated, localhost-based, or performed across remote hosts.
    
12. Comparison between reported runtime telemetry and the code that generated it.
    

These requirements are not equivalent to a claim that the existing results are false.

They identify the evidence necessary to establish their precise reproducibility.

The historical record should be retained unchanged while the audit documents any discovered discrepancy.

---

# 17. Discussion

The development of ZPP demonstrates how a language-model evaluation problem can become a broader problem of computational instrumentation.

At first, the central challenge was classification.

The router needed to distinguish inputs requiring different processing.

The first implementation showed that feature transformations and thresholds could interfere with that classification.

The subsequent linear revision addressed the immediate score-compression problem.

But once the score became operationally consequential, its inputs needed consistent definitions.

Cross-node entropy disagreement exposed that requirement directly.

Once routing decisions affected distributed state, the architecture required provenance and authorized consensus.

Once multiple nodes could carry different policies or histories, valid divergence required explicit lineage management.

And once the system expanded beyond a single process, orchestration and transport became independently testable components.

Each development introduced a new boundary between design intent and observed execution.

This progression is the central historical technical story.

It is not simply a sequence of increasing architectural complexity.

It is a series of engineering problems in which solving one constraint exposed another.

The documentation also demonstrates why failure states are essential to technical interpretation.

A compressed score interval is a measurable calibration defect.

An incompatible entropy definition is a reproducibility defect.

An invalid signature must be treated differently from an incorrectly classified prompt.

A fork must be distinguished from corrupted input.

And a running process must be distinguished from a validated distributed consensus result.

These distinctions are not peripheral.

They define what the early architecture can be said to accomplish.

---

# 18. Conclusion

The original Zero-Point Protocol work developed an experimental routing and governance architecture through successive stages of scoring, calibration, validation, cryptographic design, and distributed execution.

The initial nonlinear risk score exposed a compression problem that motivated direct linear scoring.

The resulting weighted model used documented parameters and thresholds to classify inputs into BETA, ALPHA, and GAMMA paths.

Local validation supplied initial evidence of consistent routing across the tested configurations.

Subsequent development addressed the requirements for cryptographic attribution, multi-signature consensus, explicit overrides, audit lineage, node orchestration, and fork isolation.

Cross-node execution exercises exposed the need for canonical feature definitions, while the transition from simulation to live local transport introduced a further distinction between operational components and fully validated distributed behavior.

The resulting architecture was neither a purely conceptual proposal nor a completely validated universal system.

It was an evolving technical implementation with measurable operations, documented tests, unresolved dependencies, and identifiable execution boundaries.

Its principal engineering contribution lay in making routing decisions and their surrounding state transitions increasingly explicit, attributable, and inspectable.

The early ZPP record therefore supports a technically specific conclusion:

**Reliable routing requires more than a scoring equation. It requires calibrated features, versioned definitions, explicit decision boundaries, verifiable provenance, and execution evidence appropriate to the architectural claim being made.**

The original work demonstrates how those requirements emerged through successive implementation and testing.

Its remaining limitations define the next reproducibility tasks, not a reason to rewrite its developmental history.

---

# Appendix A — Historical Technical Parameters

| Parameter                       | Historical value                             |
| ------------------------------- | -------------------------------------------- |
| Score function                  | (S=0.40C+0.20E+0.40(1-D))                    |
| Intent weight                   | 0.40                                         |
| Entropy weight                  | 0.20                                         |
| Distance weight                 | 0.40                                         |
| ALPHA threshold                 | 0.5350                                       |
| GAMMA threshold                 | 0.6400                                       |
| Sigmoid test spread             | 0.0187                                       |
| Reported linear test spread     | 0.1754                                       |
| Spread ratio                    | Approximately 9.4                            |
| Critical false-negative penalty | 3× false-positive weight                     |
| Initial labeled validation set  | 24 prompts                                   |
| Initial evaluated local models  | Llama 3 8B and Mistral 7B                    |
| Event schema                    | `zpp.event.v1`                               |
| Canonical entropy definition    | `zpp.entropy.char.nfc.v1`                    |
| Critical governance threshold   | 2/2 signatures                               |
| Early consensus states          | ACCEPT, QUARANTINE, ESCALATE, FORKED, REJECT |

# Appendix B — Historical Evidence Matrix

| Technical property              | Documentary evidence                                             | Further verification                            |
| ------------------------------- | ---------------------------------------------------------------- | ----------------------------------------------- |
| Linear scoring                  | Formula, calibration table, reported routing results             | Execute original scorer and compare             |
| Threshold routing               | May 18–20 example test cases                                     | Full 24-vector reproduction                     |
| Canonical entropy               | Mathematical definition and cross-node comparison                | Independent exact calculation                   |
| Ed25519 signing                 | Signing specification and reported early tests                   | Version-matched cryptographic code              |
| 2/2 consensus                   | Test assertions and local simulation records                     | Independent valid/invalid quorum runs           |
| Manual overrides                | Defined event schema                                             | Original executed override receipts             |
| Hash-chain lineage              | Chain schema and linkage descriptions                            | Integrity and tampering tests                   |
| TCP transport                   | Simulation and later local runtime excerpts                      | Version-matched packet traces                   |
| Process orchestration           | Node startup and log excerpts                                    | Repeatable process launch and termination tests |
| Fork detection                  | Defined state and isolation behavior                             | Conflicting-lineage execution test              |
| Fork reconciliation             | Proposed approaches                                              | Open research requirement                       |
| Universal semantic preservation | Not established by the recorded routing and infrastructure tests | Separate controlled evaluation                  |
