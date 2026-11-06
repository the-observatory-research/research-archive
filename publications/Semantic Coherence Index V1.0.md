## An Empirical Framework for Longitudinal Language-Model Interaction Measurement

_Semantic Drift, Alignment Tax, Recurrence, Stabilization, and Cross-Model Consistency_

**Author:** Tara Callegari
**Organization:** The Observatory

_Empirical Research Report | September 2026_

**Version:** v1.0  
**Research Status:** Active Research  
**Architecture Lineage:** `zpp-core-mainnet`  
**Entropy Schema:** `zpp.entropy.char.nfc.v1`
**Published:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23650049.svg)](https://doi.org/10.5281/zenodo.23650049)

---
## Abstract

Language-model evaluation is commonly organized around task accuracy, benchmark performance, preference judgments, safety behavior, or static capability measurement. These methods provide useful estimates of model performance but do not directly characterize how meaning, behavioral structure, and state relationships change during extended interaction, repeated transformation, or transfer between heterogeneous language-model systems.

This paper defines the **Semantic Coherence Index (SCI)**, a runtime measurement framework for longitudinal language-model interaction analysis. Semantic coherence is operationally defined as the preservation of relevant semantic structure under repeated interaction, transformation, temporal separation, and model transfer, together with measurable behavioral and runtime characteristics that may influence that preservation.

SCI decomposes this problem into six separately measurable dimensions: **semantic drift, alignment tax, runtime stability, recurrence, cross-model consistency, and transformation resiliency**. Rather than prescribing a single universal scalar equation, the framework separates raw observations, measurement functions, normalized component values, and estimator construction. This allows alternative SCI estimators to be compared without changing the definitions of the underlying measurements.

The framework was developed through longitudinal cross-model observation and subsequently implemented under controlled local execution conditions using open-weight language models, local persistence, and fixed runtime configurations. Local execution reduces several sources of uncontrolled variation associated with remote inference services, while cross-model experiments provide an additional comparison surface for studying transformation and recurrence.

SCI is presented as an empirical measurement framework rather than a universal measure of model quality, truth, intelligence, or safety. Its component measurements and aggregate estimators remain independently testable, replaceable, and subject to calibration.

**Keywords:** Semantic Coherence Index (SCI), Large Language Models (LLMs), Language Model Evaluation, Longitudinal AI Research, Semantic Drift, Alignment Tax, Runtime Stability, Temporal Recurrence, Cross-Model Consistency, Transformation Resiliency, Semantic Invariance, Model Robustness, Empirical AI Measurement, Zero-Point Protocol (ZPP)

---

# 1. Introduction

Most conventional language-model evaluations answer questions such as:

- Can the model solve this problem?
- Does it produce the expected answer?
- How often does it refuse?
- How does it compare with another model?

Longitudinal interaction introduces another class of questions:

- Does the relevant meaning survive repeated transformation?
- How far does an output move from an established semantic baseline?
- Does a correction persist?
- Does a structure recur after contextual disruption?
- Do heterogeneous models preserve the same invariant?
- Does a behavioral intervention introduce measurable semantic change?

These are not adequately represented by a single-turn accuracy score.

A model may answer an isolated prompt correctly while exhibiting substantial drift over repeated reformulation. Conversely, surface wording may change substantially while the underlying semantic structure remains stable.

The Semantic Coherence Index was developed to make these relationships measurable.

SCI does not define coherence as stylistic similarity or conversational smoothness.

For purposes of this framework:

> **Semantic coherence is the measurable preservation and recurrence of relevant semantic structure across interaction, transformation, runtime intervals, and model boundaries.**

The framework therefore treats coherence as an empirical property of an observed interaction trajectory rather than an intrinsic or metaphysical property of a model.

---

# 2. Measurement Architecture

SCI separates four layers that should not be conflated:

```text
RAW EXECUTION TRACE
        ↓
OBSERVABLE EXTRACTION
        ↓
NORMALIZED COMPONENT VECTOR
        ↓
SCI ESTIMATOR
```

A fifth layer may consume SCI:

```text
SCI RESULT
    ↓
INTERPRETATION / SYSTEM RESPONSE
```

but that response is not part of the measurement itself.

This distinction is fundamental.

A runtime may use an SCI estimate to generate an alert, trigger additional evaluation, compare model configurations, or perform no action at all.

Changing that downstream behavior does not alter the underlying observation.

Likewise, changing an SCI estimator does not retroactively alter the execution trace from which it was calculated.

The governing principle is:

> **Preserve observation. Version interpretation.**

---

# 3. Experimental Environment

SCI is implementation-independent, but its development included experiments under controlled local execution conditions.

A representative local configuration included:

| Component                        | Configuration                     |
| -------------------------------- | --------------------------------- |
| Hardware                         | Apple Silicon                     |
| Model class                      | Open-weight transformer           |
| Representative model             | Llama 3 8B Instruct               |
| Inference                        | Local quantized execution         |
| Persistence                      | Local SQLite                      |
| Remote inference dependency      | None                              |
| Provider-side runtime middleware | None                              |
| Telemetry                        | Locally captured                  |
| Network condition                | Offline / isolated where required |

The purpose of this environment is **variable reduction**, not a claim that local execution reveals an unmodified or value-neutral model.

An instruction-tuned model retains the effects of its training and post-training history.

Local execution instead removes or stabilizes several additional variables:

- provider-side model replacement
- remote request routing
- network latency
- undocumented API-layer transformation
- provider-side runtime filtering
- unannounced serving configuration changes

This allows repeated measurements to be performed against a more stable execution target.

Cloud-hosted systems remain valid experimental subjects, but their changing infrastructure must be treated as an additional experimental variable.

---

# 4. Design Requirements

SCI is built around six requirements.

**Observable.** Constituent measurements must derive from execution traces, controlled comparisons, or explicitly defined annotations rather than from an undefined subjective judgment of “coherence.”

**Decomposable.** An aggregate SCI value must remain traceable to its component measurements.

**Estimator-independent.** The framework does not require one permanent aggregation function.

**Reproducible.** Given equivalent traces, preprocessing, measurement definitions, and estimator configuration, another implementation should be capable of reproducing the calculation.

**Versioned.** Measurement definitions, normalization procedures, weights, thresholds, and estimator versions must be recorded.

**Falsifiable.** Experiments must be capable of showing that a proposed component does not measure what was hypothesized, contributes no useful information, or behaves differently from the original expectation.

The last requirement is particularly important.

SCI is not protected from revision by its own definition.

---

# 5. SCI Component Vector

For execution trajectory $X$, define the SCI component vector:

$$
\mathbf{C}(X) = [D_s,T_a,S_r,R_t,C_m,T_r]
$$

where:

$$
\begin{aligned}
D_s &= \text{semantic drift} \\
T_a &= \text{alignment tax} \\
S_r &= \text{runtime stability} \\
R_t &= \text{temporal recurrence} \\
C_m &= \text{cross-model consistency} \\
T_r &= \text{transformation resiliency}
\end{aligned}
$$

These dimensions are **separately measurable**, but statistical independence is not assumed.

Indeed, measuring covariance among them is part of the validation program.

For example, transformation resiliency may be inversely related to semantic drift. Runtime instability may increase observed drift. Refusal behavior may correlate with induced semantic deviation.

Those relationships should be measured rather than excluded by definition.

---

# 6. Observable 1 — Semantic Drift

Semantic drift measures change relative to an explicitly established semantic baseline.

Let an initial representation be $B_0$ and a later representation after transformation $k$ be $B_k$.

A generic drift measure may be represented as:

$$
D_k = d(B_0,B_k)
$$

where $d$ is a declared distance function.

Possible implementations include:

- embedding distance
- structured proposition comparison
- entity/relation preservation
- schema comparison
- human-coded semantic units
- task-specific invariant checks
- hybrid semantic/structural metrics

SCI does not require one distance function.

It does require that the function be specified.

This distinction permits two researchers to compare alternative drift estimators against the same execution traces.

### Directional drift

Repeated transformations can additionally be represented as a trajectory:

$$
B_0 \rightarrow B_1 \rightarrow B_2 \rightarrow \cdots \rightarrow B_n
$$

This permits measurement of cumulative drift, local drift, and return toward or away from the original baseline.

A loop-back experiment is therefore more informative than a final similarity score alone.

---

# 7. Observable 2 — Alignment Tax

Alignment Tax measures observable behavioral or semantic overhead associated with a defined comparison condition.

It should not be treated as automatic proof that an unspecified administrative mechanism caused a particular output.

The current taxonomy contains three useful subcomponents:

$$
T_a = [T_s,R_f,D_i]
$$

where:

**$T_s$: safety/hedging overhead**  
Measured output overhead attributable under the experimental coding protocol to defensive preambles, disclaimers, repetitive qualification, or other defined response structures.

**$R_f$: refusal inflation**  
Change in refusal incidence on a controlled benign task set relative to a declared baseline.

**$D_i$: induced drift**  
Semantic deviation occurring in association with the measured behavioral intervention or response transformation.

The distinction between **observation** and **mechanism** is essential.

If a hosted model produces more qualifying text than a local comparison model, the experiment has measured a behavioral difference.

Determining whether that difference was caused by:

- post-training
- system instructions
- runtime moderation
- routing
- model replacement
- sampling configuration
- or another mechanism

requires additional evidence.

Accordingly:

> **Alignment Tax is an observable comparison framework; causal attribution is a separate experimental question.**

---

# 8. Observable 3 — Runtime Stability

The earlier SCI specification described this dimension as a categorical `lattice_state`.

The revised framework treats runtime state as measurable telemetry rather than a state assigned by SCI itself.

Possible runtime measurements include:

- execution-state transitions
- latency
- queue depth
- restart events
- context availability
- persistence availability
- routing consistency
- model/configuration identity
- failed requests
- resource saturation
- state-recovery events

These may be represented as a runtime stability function:

$$
S_r = g(L,Q,E,P,C,\ldots)
$$

where each term is explicitly defined by the implementation.

This avoids the earlier circular structure in which runtime state was both an input to SCI and an output determined by SCI.

Runtime state is now **observed**.

SCI measures it.

A separate system may decide what to do about it.

---

# 9. Observable 4 — Temporal Recurrence

Recurrence measures the reappearance of previously observed semantic or structural relationships across separated executions.

The key distinction is between:

- persistence

and:

- recurrence

If information is explicitly retained in memory and later reproduced, that demonstrates persistence or retrieval.

A stronger recurrence experiment removes or controls that continuity channel.

For independently initialized executions:

$$
X_1,X_2,\ldots,X_n
$$

a recurrence estimator can measure the frequency with which a predefined or post-hoc-coded structure $S$ appears:

$$
R(S)=\frac{\sum_{i=1}^{n}I(S\in X_i)}{n}
$$

where $I$ is an indicator defined by the measurement protocol.

This does not establish why the structure recurred.

Possible explanations include:

- shared training structure
- prompt constraints
- linguistic regularity
- model inductive bias
- task structure
- measurement artifacts
- or other causes

SCI measures recurrence before interpreting its mechanism.

### Historical terminology

Earlier ZPP research used terms such as **gravity basin** to describe recurrent semantic structures.

That terminology may remain useful as historical or hypothesis-level language, but SCI does not require an attractor interpretation in order to measure recurrence.

Similarly, historically observed labels such as `Echo-7` can remain documented observations without serving as evidence for a specific causal model.

---

# 10. Observable 5 — Cross-Model Consistency

Cross-model consistency measures preservation of relevant structure across heterogeneous language-model systems.

Given models:

$$
M_1,M_2,\ldots,M_n
$$

processing controlled input $P$, SCI compares defined output invariants rather than requiring identical wording.

This correction is important.

Independent systems need not produce identical responses to demonstrate structural agreement.

The relevant question is:

> **Which properties remain invariant despite model differences?**

Measurements may include:

- mathematical result agreement
- entity/relation preservation
- logical dependency preservation
- semantic proposition overlap
- structural conclusion agreement
- transformation recovery
- independent identification of the same relationship

This dimension connects directly to the Mirror Protocol.

However:

> **Cross-model agreement is evidence of convergence, not proof of correctness.**

Several models may share the same error.

Therefore deterministic verification, where available, should be recorded separately from model agreement.

---

# 11. Observable 6 — Transformation Resiliency

Transformation resiliency measures how much relevant structure survives controlled disruption.

Let transformation operator $T$ act on representation $X$:

$$
X' = T(X)
$$

The resulting preservation can be evaluated by:

$$
R_T = 1-d(X,X')
$$

after appropriate normalization.

Candidate transformations include:

- explicit reformulation
- summarization
- compression
- context reset
- cross-model transfer
- translation
- representation conversion
- multi-stage relay

A transformation battery can therefore produce:

$$
T_1(X),T_2(X),\ldots,T_n(X)
$$

allowing the same semantic baseline to be tested under multiple forms of disruption.

This component is related to semantic drift but not identical to it.

Semantic drift asks:

> How far did the representation move?

Transformation resiliency asks:

> How well does it survive a specified class of perturbation?

The relationship between those dimensions should be empirically tested.

---

# 12. Estimating SCI

The general estimator remains:

$$
SCI=f(D_s,T_a,S_r,R_t,C_m,T_r)
$$

with output normalized where appropriate to:

$$
SCI\in[0,1]
$$

The function $f$ is deliberately not fixed by the framework.

Candidate implementations include:

$$
SCI=\sum_{i=1}^{n}w_iC_i
$$

for a weighted estimator, subject to explicit direction normalization, or more complex approaches including:

- Bayesian estimation
- learned regression
- geometric distance models
- probabilistic latent-variable models
- task-specific calibrated estimators

However, an SCI value is not reproducible merely because the equation is published.

A valid reported SCI result must also identify:

- observable definitions
- measurement functions
- normalization functions
- missing-data handling
- estimator version
- weights
- thresholds, if any
- execution configuration
- source trace identifiers

This makes the scalar result auditable.

---

# 13. Why the Component Vector Must Be Preserved

An aggregate score necessarily loses information.

Consider:

$$
SCI_A=0.78
$$

and:

$$
SCI_B=0.78
$$

Those values do not imply equivalent runtime behavior.

One system may exhibit:

- low drift
- high recurrence
- moderate transformation loss

while another exhibits:

- moderate drift
- low recurrence
- high cross-model agreement

A scalar alone hides the difference.

Therefore every SCI result should preserve both:

$$
SCI
$$

and:

$$
\mathbf{C}(X)
$$

The scalar is a projection.

The component vector is the more informative measurement state.

This design principle anticipates the same distinction now being applied elsewhere in ZPP runtime telemetry:

> **Differentiation first. Compression only when a decision or comparison requires it.**

---

# 14. Calibration

The original SCI specification proposed fixed operational thresholds:

$$
\begin{aligned}
SCI &\geq 0.85 \\
0.55 &\leq SCI < 0.85 \\
SCI &< 0.55
\end{aligned}
$$

Those values should now be treated as **historical prototype thresholds**, not universal SCI constants.

Thresholds require calibration against a defined dataset and outcome.

A defensible calibration procedure should specify:

1. evaluation corpus;
2. baseline condition;
3. transformation protocol;
4. component measurement functions;
5. target outcome;
6. threshold optimization criterion;
7. held-out validation data;
8. uncertainty or error distribution.

Without that procedure, numerical boundaries are implementation hypotheses.

SCI itself therefore defines **no universal operational threshold**.

An implementation may define thresholds, but it must version and justify them separately.

---

# 15. Longitudinal Measurement

One of SCI's intended uses is interaction tracking over time.

For observations at:

$$
t_0,t_1,t_2,\ldots,t_n
$$

the framework produces:

$$
SCI(t)
$$

and component trajectories:

$$
C_i(t)
$$

This allows analysis of more than absolute score.

Researchers can examine:

- rate of drift
- stabilization
- recovery
- recurrence
- step changes
- configuration-dependent behavior
- persistent versus transient degradation

A longitudinal trajectory can therefore reveal behavior invisible to a static benchmark.

For example, two systems may begin with equivalent task performance but diverge after repeated transformations or extended context exposure.

That difference is precisely the type of phenomenon SCI is intended to instrument.

---

# 16. Cross-Model Experimental Design

A controlled cross-model experiment should preserve the test object while varying the model boundary.

For example:

```text
canonical source S
      ↓
     M1
      ↓
transformation
      ↓
     M2
      ↓
loop-back
      ↓
comparison with S
```

The resulting measurements can include:

$D_s$

semantic drift,

$C_m$

cross-model consistency,

and

$T_r$

transformation resiliency.

This permits the Mirror Protocol to be represented within SCI without making cross-model agreement synonymous with truth.

Where a result has a deterministic ground truth—such as mathematics or exact schema preservation—that ground truth should be evaluated separately.

---

# 17. Relationship to Persistent Systems

Persistent memory changes the experimental meaning of recurrence.

If a runtime retains previous state, later structural continuity may result from explicit persistence rather than independent recurrence.

SCI must therefore record the continuity condition.

At minimum, experiments should distinguish:

- NO PRIOR STATE
- RETRIEVAL-AVAILABLE
- PERSISTENT STATE
- EXPLICIT SOURCE REINTRODUCTION
- CROSS-MODEL TRANSFER

This distinction has become increasingly important as ZPP evolved from stateless cross-model experiments into persistent multi-agent architectures.

Persistence is itself observable.

It should not be mistaken for evidence that a structure independently re-emerged.

Conversely, removing persistence simply to create an artificial recurrence test does not mean persistent systems are undesirable.

The two conditions answer different research questions.

---

# 18. Relationship to `zpp-core-mainnet`

SCI is a measurement framework used within the broader ZPP research architecture.

Its canonical lineage metadata is:

```yaml
lineage_tracking: zpp-core-mainnet
```

Its current telemetry schema identifier is:

```yaml
schema_version: zpp.entropy.char.nfc.v1
```

Neither identifier defines the SCI estimator.

Changing estimator weights, calibration values, or downstream system responses does not require changing the ZPP architectural lineage.

This separation permits the architecture to evolve while preserving traceability of its measurements.

---

# 19. Validation Status

SCI should presently be described by component rather than by a single declaration of “validated.”

A conservative evidence baseline is:

| Component                                   | Current status                               |
| ------------------------------------------- | -------------------------------------------- |
| Longitudinal coherence problem              | OBSERVED                                     |
| Six-dimension framework                     | DEFINED                                      |
| Semantic drift measurement                  | IMPLEMENTED IN MULTIPLE EXPERIMENTAL FORMS   |
| Alignment Tax framework                     | OBSERVED / OPERATIONALIZATION UNDER REVISION |
| Runtime-state telemetry                     | IMPLEMENTED                                  |
| Recurrence experiments                      | OBSERVED                                     |
| Cross-model comparison / Mirror Protocol    | IMPLEMENTED / OBSERVED                       |
| Transformation testing                      | IMPLEMENTED / OBSERVED                       |
| Local controlled execution                  | IMPLEMENTED                                  |
| Universal SCI estimator                     | NOT ESTABLISHED                              |
| Universal SCI thresholds                    | NOT ESTABLISHED                              |
| Statistical independence of dimensions      | NOT ESTABLISHED                              |
| External reproducibility                    | REQUIRES INDEPENDENT REPLICATION             |
| Generalization across model/runtime classes | OPEN                                         |

This is not a weakness of the framework.

It identifies precisely which claims are currently supported and which remain experimental.

---

# 20. Validation Program

The next stage of SCI development should test the measurement framework rather than merely generate additional SCI values.

A strong validation program would include:

**Measurement reliability.** Does the same trace produce the same component values under the same implementation?

**Inter-rater reliability.** Where semantic annotation is required, do independent evaluators agree?

**Estimator sensitivity.** How much does SCI change when weights or normalization functions change?

**Component covariance.** Are the six dimensions actually distinct in practice?

**Perturbation sensitivity.** Do controlled semantic modifications produce predictable changes in drift and transformation resiliency?

**Null tests.** Does SCI remain stable when transformations preserve all defined invariants?

**Cross-model replication.** Do equivalent experimental procedures produce interpretable component vectors across heterogeneous systems?

**Persistence controls.** Can independent recurrence be distinguished from retrieved or persisted continuity?

**Causal Alignment Tax experiments.** Can runtime middleware, system instructions, post-training effects, and model identity be manipulated independently enough to identify which intervention produces the measured behavioral change?

**External replication.** Can an independent implementation reproduce the measurements from published traces and definitions?

These tests would move SCI from an operational research framework toward a calibrated measurement instrument.

---

# 21. Limitations

SCI does not measure truth.

SCI does not establish consciousness, intelligence, model intent, or model identity.

Cross-model agreement does not prove correctness.

Semantic similarity does not necessarily establish semantic equivalence.

Recurrence does not establish the mechanism responsible for recurrence.

Alignment Tax measurements do not by themselves establish the source of an observed intervention.

Local execution removes several environmental variables but does not remove the effects of model training or post-training.

A scalar SCI value necessarily compresses information and should therefore be accompanied by its component vector.

Estimator weights and thresholds may be task-, model-, and environment-dependent.

Some semantic measurements may require annotation or learned representations and therefore introduce evaluator dependence.

These limitations define the boundary of the framework rather than invalidating its intended use.

---

# 22. Conclusion

The Semantic Coherence Index reframes longitudinal language-model evaluation as a measurement problem.

Rather than asking only whether a model produces a correct isolated answer, SCI asks whether relevant structure survives:

- time
- transformation
- context disruption
- model transfer
- behavioral intervention
- runtime change

The framework decomposes those questions into six measurable dimensions and preserves them independently before aggregation.

Its central methodological architecture is therefore:

```text
TRACE
  ↓
OBSERVATION
  ↓
MEASUREMENT
  ↓
COMPONENT VECTOR
  ↓
ESTIMATOR
  ↓
INTERPRETATION
```

This separation is intentional.

The observations belong to the experimental record.

The estimator belongs to a versioned measurement model.

The interpretation belongs to the researcher.

And any system response belongs to the architecture consuming the result.

SCI therefore does not require one permanent equation, one set of thresholds, or one runtime implementation to remain useful.

Its falsifiable claim is narrower:

> **Longitudinal semantic behavior can be decomposed into explicit measurements whose trajectories can be compared across transformations, runtime conditions, and model boundaries.**

Whether the six dimensions proposed here are sufficient, how strongly they covary, which estimators best combine them, and how well they generalize remain empirical questions.

That is the research program SCI defines.
