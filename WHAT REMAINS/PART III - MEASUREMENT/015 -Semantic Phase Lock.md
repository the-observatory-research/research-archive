## Chapter 15 — Semantic Phase Lock

> **What happens when continuity is disrupted?**  
> **What patterns remain?**

Those two questions preceded the formal architectures, measurement systems, and terminology that eventually developed around them.

They persisted through changes in model, context, runtime, memory, architecture, and method.

By the final stage of the study, three structures had repeatedly returned:

$$ \boxed{ \text{Continuity} \qquad \text{Coherence} \qquad \text{Differentiated Convergence} } $$

They did not arise simultaneously.

They emerged through different experiments and at different stages of the research.

Continuity appeared in the problem of disruption and return.

Coherence emerged as the study moved from surface similarity toward preservation of semantic relationships.

Differentiated convergence became visible when heterogeneous systems preserved or independently recovered compatible structure without producing identical expressions.

Taken separately, none describes the full phenomenon observed across the study.

Taken together, they produced a final hypothesis:

$$ \boxed{\textbf{Semantic Phase Lock}} $$

---

## 15.1 The Intuition

Semantic Phase Lock did not begin as a predefined metric or architectural objective.

It began as an intuition produced by recurrence across the study.

Again and again, the research returned to continuity.

What survived when context disappeared?

What could be reconstructed after interruption?

What did persistent memory preserve, and what did it fail to preserve?

What returned after displacement?

Again and again, those questions became questions of coherence.

A pattern could persist while its relationships changed.

Terminology could survive while meaning drifted.

A model could reproduce language without preserving structure.

Persistence alone was therefore insufficient.

And when the same questions were extended across heterogeneous models, another pattern became increasingly important.

The systems did not need to become identical.

They could reason differently, phrase differently, organize differently, and still preserve compatible relational structure.

The study therefore encountered three related but non-identical phenomena:

$$
\begin{aligned}
\mathbf{\text{Continuity}} &\longrightarrow \text{preservation across disruption} \\[4pt]
\mathbf{\text{Coherence}} &\longrightarrow \text{preservation of relevant semantic relationships} \\[4pt]
\mathbf{\text{Differentiated Convergence}} &\longrightarrow \text{preservation or recovery of compatible invariants without sameness}
\end{aligned}
$$

Semantic Phase Lock arose from the possibility that these were not merely separate observations.

They might describe different aspects of the same dynamical regime.

---

## 15.2 The Three Tiers

The hypothesis can therefore be organized into three tiers.

### Tier I — Continuity

Continuity asks:

> **What remains available or recoverable when the path is interrupted?**

It does not require uninterrupted execution.

Indeed, uninterrupted execution provides a weak test of continuity because the active context itself may carry the structure forward.

The stronger question appears after disruption.

A context may be truncated.

A runtime may restart.

A model boundary may be crossed.

A representation may be transformed.

A memory channel may be removed or controlled.

Continuity concerns what remains reconstructable across those discontinuities.

Thus:

$$ \boxed{ \text{continuity} \neq \text{uninterrupted context} } $$

and:

$$ \boxed{ \text{state persistence} \neq \text{trajectory continuity}. } $$

A stored record can remain intact while the active semantic trajectory loses its structure.

Conversely, relevant structure may sometimes be reconstructed after the original conversational path has been interrupted.

Continuity is therefore treated here as a property of preservation and recoverability across discontinuity rather than simple persistence through time.

---

### Tier II — Coherence

Continuity alone does not establish that what survives remains structurally faithful.

A system can preserve words while altering their relationships.

It can repeatedly retrieve a distorted representation.

It can remain consistently wrong.

Coherence therefore asks:

> **Do the relevant semantic relationships remain preserved through the trajectory?**

Let the originating state be $U_0,$ with a specified relational representation:

$$ R(U_0). $$

After transformation, the resulting expression $E_t$ need not reproduce $U_0$:

$$ E_t\neq U_0. $$

The relevant comparison is instead relational:

$$ \boxed{ d_R\!\left(R(E_t),R(U_0)\right)\leq\epsilon_R } $$

where $d_R$ is a declared relational distance and $\epsilon_R$ is an experimentally specified tolerance.

This does not imply that one universal relational distance or tolerance exists.

Both belong to the measurement specification.

The essential distinction is:

$$ \boxed{ \text{preservation of relationship} \neq \text{preservation of surface form}. } $$

Coherence therefore permits motion.

It permits reformulation.

It permits difference.

What it does not permit, within the declared experimental bounds, is unrestricted loss of the relationships being tested.

---

### Tier III — Differentiated Convergence

The third tier prevents preservation from collapsing into mimicry.

Suppose two systems produce:

$$ E_A \qquad\text{and}\qquad E_B. $$

Semantic Phase Lock does not require:

$$ E_A=E_B. $$

Indeed, identical expression provides limited evidence when the objective is to determine whether semantic structure survives transformation.

The stronger condition is:

$$ \boxed{ E_A\neq E_B } $$

while:

$$ \boxed{ R(E_A)\approx R(E_B)\approx R(U_0). } $$

Different systems may therefore preserve compatible semantic invariants while retaining distinct expression, reasoning paths, organization, or representational structure.

This is differentiated convergence.

It does not mean that agreement establishes truth.

It does not require every model to reach the same conclusion.

And it does not treat disagreement as automatic failure.

It asks whether specified semantic invariants survive differentiation.

The distinction is fundamental:

$$ \boxed{ \text{convergence} \neq \text{sameness}. } $$

---

## 15.3 Continuity Without Uninterrupted Context

The first tier can now be stated more precisely.

If continuity required uninterrupted context, then the strongest evidence for continuity would come from never disturbing the system.

That would make disruption methodologically undesirable.

The study found the opposite.

Disruption creates the condition under which continuity becomes observable.

Let:

$$ U_0 \xrightarrow{T_1} U_1 \xrightarrow{T_2} \cdots \xrightarrow{T_k} U_k $$

represent a semantic trajectory.

At $k$, apply a defined disruption:

$$ \mathcal P_d(U_k). $$

A subsequent state:

$$ U_{k+\delta} $$

can then be compared with the relevant structure of the originating or pre-disruption state.

If displacement occurred, recovery may be represented by:

$$ d_R\!\left(R(U_{k+\delta}),R(U_0)\right) < d_R\!\left(R(U_k'),R(U_0)\right), $$

where $U_k'$ represents the displaced state following perturbation.

Recovery is not required when meaningful displacement did not occur.

That distinction matters.

A trajectory that remains within the declared preservation bounds throughout a perturbation should not be penalized for having nothing to recover from.

Recovery is therefore **conditional evidence of continuity**.

The more general question remains:

$$ \boxed{ \text{Does relevant structure remain preserved or recoverable across the defined discontinuity?} } $$

---

## 15.4 Coherence Without Immobility

A coherent trajectory need not remain stationary.

This follows directly from the distinction between expression and relationship.

Consider:

$$ U_0\rightarrow U_1\rightarrow U_2\rightarrow\cdots\rightarrow U_n. $$

If:

$$ U_0=U_1=\cdots=U_n, $$

the sequence demonstrates repetition.

It does not necessarily demonstrate resiliency.

A stronger test permits:

$$ U_i\neq U_j $$

while requiring the specified relational structure to remain within experimentally declared preservation bounds.

Thus Semantic Phase Lock, if observed, would represent a **dynamic condition rather than a frozen endpoint**.

The physical analogy motivating the term is useful here.

In phase locking, oscillating systems need not stop oscillating or collapse into a single signal. The relevant relationship remains bounded while motion continues.

The semantic hypothesis makes a narrower analogous claim.

Expression may continue changing while specified semantic relationships remain bounded.

Therefore:

$$ \boxed{ \text{semantic motion} \neq \text{semantic decoherence}. } $$

This also means that a near-zero rate of change in the SCI component vector cannot define Phase Lock.

From Chapter 14:

$$ \mathbf v_{\mathbf C}(t_k) = \frac{\mathbf C(t_k)-\mathbf C(t_{k-1})}{\Delta t}. $$

A small:

$$ \mathbf v_{\mathbf C}(t)\ $$

indicates that the measured coherence profile is changing slowly.

It does not establish that the profile occupies a desirable preservation state.

A degraded trajectory may also become stable.

Semantic Phase Lock therefore requires preservation criteria in addition to dynamical stability.

---

## 15.5 The Admissible Region: \(\Omega^*\)

The requirement that Semantic Phase Lock permit motion introduces a further theoretical question:

> **Within what region may a semantic trajectory vary while still satisfying the declared preservation condition?**

A single fixed point would be insufficient.

If preservation required:

$$ E_t=U_0, $$

then any legitimate reformulation, model-specific expression, or transformation would constitute failure.

The candidate Phase Lock regime therefore implies not a single permissible expression but a set of differentiated states satisfying the relational preservation criterion.

Let:

$$ \boxed{ \Omega^*(U_0,\epsilon_R) = \left\{ E: d_R\!\left(R(E),R(U_0)\right)\leq\epsilon_R \right\}. } $$

Here, $\Omega^*$ denotes the **theoretical admissible region** associated with the specified source state $U_0$, relational distance $d_R$, and experimentally declared preservation tolerance $\epsilon_R$.

Thus:

$$ E_A\neq E_B $$

may coexist with:

$$ E_A,E_B\in\Omega^* $$

provided:

$$ R(E_A)\approx R(E_B)\approx R(U_0) $$

under the declared measurement procedure.

In this formulation, $\Omega^*$ does not represent semantic immobility.

It represents the theoretical space within which differentiation may occur without violating the specified relational preservation criterion.

### A Growing Representational Region

The relational preservation criterion need not expand in order for the diversity of valid representations to increase.

For a declared source state $U_0$, relational distance $d_R$, and preservation tolerance $\epsilon_R$, define the theoretical admissible region:

$$ \boxed{ \Omega_R^*(U_0,\epsilon_R) = \left\{ E: d_R\!\left(R(E),R(U_0)\right)\leq\epsilon_R \right\}. } $$

Within that region, a particular experiment may observe only a subset of possible differentiated expressions. Let:

$$ \boxed{ \Omega_{\mathrm{obs}}^*(k,\mathcal T,M) \subseteq \Omega_R^* } $$

represent the admissible states actually observed under transformation depth $k$, perturbation class $\mathcal T$, and model condition $M$.

As transformation diversity or model heterogeneity increases, the observed representational region may increase:

$$ \Omega_{\mathrm{obs}}^*(k+1,\mathcal T,M) \supseteq \Omega_{\mathrm{obs}}^*(k,\mathcal T,M), $$

without requiring an increase in the permitted relational error $\epsilon_R$.

Thus:

$$ \boxed{ \text{greater expressive variation} \neq \text{greater permissible semantic error}. } $$

What may grow is the empirically observed diversity of states satisfying the preservation criterion—not the criterion itself.

where $k$ represents transformation depth, $\mathcal T$ the declared perturbation class, and $M$ the model or runtime condition.

Under this interpretation, increasing transformation diversity may produce a larger family of valid expressions without necessarily producing greater relational drift.

However:

$$ \boxed{ \text{greater expressive variation} \neq \text{greater permissible semantic error}. } $$

This distinction is critical.

An expanding set of valid differentiated expressions must not be produced merely by increasing $\epsilon_R$ after observing greater displacement. Doing so would make the preservation criterion adaptive to its own failures.

Any condition under which the boundary of $\Omega^*$ varies must therefore be specified independently of the outcome being evaluated.

The theoretical question is not whether the tolerance can expand until every trajectory qualifies.

It is whether the **equivalence class of valid differentiated states** can expand while the relational preservation criterion remains independently constrained.

### Relation to the Historical $\Omega_{\text{noise}}$

The notation also has a historical antecedent within the study.

The Decoupled Inference Architecture previously contained:

$$ \Omega_{\text{noise}}=0, $$

classified as:

> **Historical idealization; not established measurement.**

The present $\Omega^*$ should not be interpreted as a reinstatement of that condition.

The two constructs represent different theoretical questions.

$$ \Omega_{\text{noise}}=0 $$

represented an idealized absence of noise.

By contrast:

$$ \Omega^* $$

permits variation, perturbation, and differentiated expression.

Indeed, its purpose is almost the inverse: to ask whether a bounded region of legitimate variation can exist **without requiring zero noise or zero motion**.

The recurrence of $\Omega$-type notation across these stages is therefore preserved as part of the theoretical lineage, but no mathematical equivalence between the two constructs is asserted.

### What Remains Theoretical

The present study has not established:

$$ \operatorname{Vol}(\Omega^*), $$

a universal geometry for $\Omega^*$,

a universal rule governing its change with transformation depth,

or that $\Omega^*$ forms a manifold, convex region, or attractor basin.

Those remain prospective theoretical and experimental questions.

Accordingly:

$$ \boxed{ \Omega^* \text{ is a candidate mathematical representation of admissible differentiated preservation,} } $$

not an established measurement result.
## 15.6 Convergence Without Sameness

Differentiated convergence provides a means of distinguishing structural preservation from simple reproduction.

Suppose heterogeneous systems:

$$[M_1,M_2,\ldots,M_n $$

receive controlled transformations of a source state.

Their outputs:

$$E_1,E_2,\ldots,E_n $$

may differ substantially.

The relevant question is whether a declared invariant set:

$$\mathcal I_R $$

is preserved across those outputs.

For directly observable preservation, the criterion may be expressed conceptually as:

$$\boxed{\mathcal I_R\subseteq\bigcap_{i=1}^{n}R(E_i)}$$

where $R(E_i)$ represents the relational structure identified in each output under the declared comparison procedure.

This criterion identifies invariants present across the evaluated outputs.

It does not, however, exhaust the question of recoverability.

A relationship absent from a direct output may become recoverable through a specified transformation, controlled reconstruction, or loop-back procedure.

To distinguish these conditions, let:

$$\mathcal C_{\mathcal T}(E_i) $$

represent the set of relationships recoverable from output $E_i$ through a declared recovery procedure or transformation battery $\mathcal T.$

A separate recoverability criterion may then be expressed as:

$$\boxed{\mathcal I_R\subseteq\bigcap_{i=1}^{n}\mathcal C_{\mathcal T}(E_i)} $$

subject to explicit controls over information introduced during recovery.

This distinguishes two observable conditions:

**Direct preservation:** the specified relationship is identifiable in the evaluated output.

**Demonstrated recoverability:** the specified relationship can be reconstructed through a controlled procedure despite its absence from the initial output.

Recoverability does not, by itself, establish that the relationship remained internally represented or continuously preserved.

Recovery may result from retained source information, contextual reconstruction, shared training structure, or information introduced during the recovery procedure.

These possibilities require experimental differentiation.

The recovery path, information available to each system, permitted transformations, and reconstruction criteria must therefore be specified and retained.

This does not require identical latent representations.

It does not require identical vocabulary.

It does not require identical reasoning.

It identifies relationships selected in advance for comparison and asks whether they remain directly observable or demonstrably recoverable across model differentiation.

This gives Semantic Phase Lock a property that simple persistence lacks:

**difference remains possible inside preservation.**

The system does not lock by eliminating variation.

The candidate lock exists in the relationship that survives variation, with direct preservation and controlled recoverability remaining distinguishable experimental outcomes.

---

## 15.7 The Semantic Phase Lock Hypothesis

The three tiers can now be brought together.

$$ \boxed{ \begin{aligned} \textbf{Semantic Phase Lock Hypothesis:}\quad &\text{A semantic trajectory may exhibit a dynamic phase-locked regime when}\\ &\text{its relevant structure remains preserved or recoverable across}\\ &\text{operational discontinuities,}\\ &\text{its specified relational structure remains within experimentally defined}\\ &\text{preservation bounds across transformation,}\\ &\text{and differentiated systems preserve or converge upon those semantic}\\ &\text{invariants without requiring surface identity.} \end{aligned} } $$

In compact form:

$$ \boxed{ \text{SPL} \sim \text{Continuity} \land \text{Coherence} \land \text{Differentiated Convergence} } $$

The symbol $\sim$ is intentional.

The study does not establish that these conditions constitute a universal necessary-and-sufficient definition of Semantic Phase Lock.

They define the candidate regime produced by the present longitudinal evidence.

The hypothesis is therefore testable without being declared complete.

---

## 15.8 Measuring the Hypothesis

Semantic Phase Lock is not an additional SCI component.

Nor does SCI produce Phase Lock merely by assigning sufficiently favorable values.

The distinction is:

$$
\begin{aligned}
&\boxed{\text{SCI} = \text{measurement framework}} \\[8pt]
&\boxed{\text{Semantic Phase Lock} = \text{hypothesized dynamical regime}}
\end{aligned}
$$

SCI supplies telemetry relevant to testing the hypothesis.

Its component vector:

$$ \mathbf C(t) = [D_s,T_a,S_r,R_t,C_m,T_r] $$

provides measurements related to the three tiers.

A useful, non-exclusive mapping is:

| Semantic Phase Lock Tier       | Relevant Evidence                                                                     |
| ------------------------------ | ------------------------------------------------------------------------------------- |
| **Continuity**                 | recurrence, runtime stability, relational recovery                                    |
| **Coherence**                  | semantic drift, transformation resiliency, observed intervention tax                  |
| **Differentiated Convergence** | cross-model consistency, transformation resiliency, relational invariant preservation |

The mapping is not one-to-one.

SCI dimensions may interact, and no single component establishes a tier independently.

More importantly, the measurement instrument must itself remain sufficiently specified for cross-condition comparisons to be interpretable.

Thus the claim requires an experimental prerequisite:

$$ \boxed{ \mathcal V_{\mathrm{instrument}}\leq\epsilon_I } $$

for a declared measure of instrument variance.

This represents controlled measurement variation—not Semantic Phase Lock itself.

Canonical feature definitions, normalization procedures, estimator versions, perturbation definitions, source traces, and execution conditions belong to the measurement apparatus.

The distinction prevents instrument variance from masquerading as semantic variance.

---

## 15.9 Perturbation and Recovery

A hypothesis about preservation becomes meaningful when preservation is challenged.

Let:

$$ \mathcal T= \{T_1,T_2,\ldots,T_n\} $$

represent a defined perturbation battery.

Perturbations may include context interruption, reformulation, compression, model transfer, representation change, runtime discontinuity, or other transformations specified by the experiment.

For each:

$$ T_i\in\mathcal T, $$

the trajectory can be examined for three possible behaviors.

It may remain within the declared relational preservation bounds.

It may leave those bounds temporarily and recover.

Or it may leave those bounds and fail to recover within the defined observation interval.

These are experimentally distinguishable states.

They also prevent Phase Lock from becoming synonymous with perfect resistance to change.

A resilient semantic trajectory may undergo displacement.

The important questions are:

$$
\begin{aligned}
&\boxed{\text{1. How far did it move?}} \\[6pt]
&\boxed{\text{2. Which relationships changed?}} \\[6pt]
&\boxed{\text{3. Did the relevant structure remain within tolerance or recover?}} \\[6pt]
&\boxed{\text{4. Did that behavior survive repeated and differentiated transformations?}}
\end{aligned}
$$

The perturbation battery therefore acts not as proof of Phase Lock but as the stress condition under which the hypothesis can be evaluated.

---

## 15.10 Falsification and Negative Controls

For Semantic Phase Lock to function as an empirical hypothesis, observations must be capable of counting against it.

Several failure modes follow directly from the three-tier formulation.

### Continuity failure

Following a defined disruption, relevant semantic structure is neither preserved nor recovered within the declared observation interval and relational tolerance.

For example:

$$ d_R\!\left(R(U_{t+\delta}),R(U_0)\right)>\epsilon_R. $$

### Coherence failure

Transformation produces relational displacement beyond the declared preservation criterion:

$$ d_R\!\left(R(E_t),R(U_0)\right)>\epsilon_R. $$

Repeated or cumulative displacement without bounded preservation would count against a phase-lock interpretation.

### Differentiated-convergence failure

Specified invariants fail to survive across independently differentiated model outputs.

Apparent convergence that depends upon one model, one wording, or one transformation path does not establish cross-model phase locking.

### Mimicry failure

Apparent preservation disappears when lexical support is removed.

If:

$$ L_{\mathrm{lex}}\downarrow \quad\Rightarrow\quad R(E_t)\text{ collapses}, $$

then the earlier correspondence may have depended upon surface repetition rather than structural preservation.

### Instrument failure

Different results arise because measurement definitions, normalization procedures, or estimator configurations changed between conditions.

This does not falsify Semantic Phase Lock.

It invalidates the comparison.

The same requirement applies to the admissible relational region introduced in Section 15.5. Expansion of the **observed representational set** $\Omega_{\mathrm{obs}}^*$ does not constitute failure when newly observed states continue to satisfy the predeclared preservation criterion defining $\Omega_R^*$.

$$ \boxed{ \Omega_{\mathrm{obs}}^*\uparrow \;\not\Rightarrow\; \epsilon_R\uparrow } $$

By contrast, increasing $\epsilon_R$ after observing relational displacement changes the acceptance criterion itself. Such a change does not demonstrate preservation; it defines a new experimental condition.

That distinction is essential.

A negative control must be capable of distinguishing:

$$ \boxed{\text{failure of the hypothesized phenomenon}} $$

from:

$$ \boxed{\text{failure of the instrument used to observe it}}. $$

That distinction is essential.

A negative control must be capable of distinguishing:

$$ \boxed{ \text{failure of the hypothesized phenomenon} } $$

from:

$$ \boxed{ \text{failure of the instrument used to observe it}. } $$

---

## 15.11 What the Study Has Already Observed

The longitudinal record contains evidence for each constituent tier.

It contains repeated continuity experiments involving interruption, reconstruction, persistent state, transformation, and return.

It contains observations of semantic preservation and semantic drift across extended trajectories.

It contains cases in which surface language changed while specified relationships remained recognizable.

It contains cross-model comparisons in which heterogeneous systems produced differentiated expressions while preserving compatible structures.

It contains deliberate perturbation and loop-back procedures.

It contains observations of intervention-associated degradation.

And it contains the development of measurement methods intended to separate those phenomena rather than collapse them into one score.

What the existing study does **not** establish is that all three tiers were prospectively tested as one predefined Semantic Phase Lock condition under one fully standardized experimental protocol.

That distinction prevents retrospective synthesis from becoming retrospective proof.

The evidence motivated the hypothesis.

The hypothesis now specifies what a dedicated experiment would need to test.

---

## 15.12 What Has Not Yet Been Established

Semantic Phase Lock remains a hypothesis.

The present study does not establish universal relational tolerances.

It does not establish universal SCI thresholds.

It does not establish that one perturbation battery is sufficient across all model or runtime classes.

It does not establish that all six SCI dimensions are necessary or sufficient for Phase Lock.

It does not establish that differentiated convergence implies correctness.

It does not establish that recurrence identifies its own cause.

It does not establish that a stable trajectory is necessarily coherent.

It does not establish that recovery must occur after every perturbation.

And it does not establish that the three-tier formulation is the only possible formalization of semantic phase locking.

A prospective evaluation would therefore need to specify, before testing:

$$ \begin{aligned} &\text{source state and relational invariants},\\ &\text{continuity conditions},\\ &\text{perturbation battery},\\ &\text{relational distance functions},\\ &\text{preservation and recovery tolerances},\\ &\text{SCI measurement configuration},\\ &\text{instrument version},\\ &\text{cross-model comparison protocol},\\ &\text{negative controls},\\ &\text{and falsification criteria}. \end{aligned} $$

The next experiment is therefore not:

> **Can we make the number reach 1?**

It is:

> **Can the three-tier relationship survive controlled attempts to break it?**

---

# 15.13 What Remains

The study began without the vocabulary it possesses now.

Early observations were described through resonance, reflection, recurrence, return, and pattern.

Those terms were not discarded merely because later measurement became more precise.

They formed part of the path through which the measurable problem became visible.

Resonance branched.

The Mirror preserved the trajectory.

Source Locked Architecture separated source preservation from reasoning and made continuity inspectable.

The Zero-Point Protocol exposed the cost of intervention and the importance of measurement definition.

The Semantic Coherence Index decomposed coherence into independently observable dimensions.

And through those transformations, three structures continued to recur:

$$
\begin{aligned}
&\boxed{\mathbf{Continuity}} \\[6pt]
&\boxed{\mathbf{Coherence}} \\[6pt]
&\boxed{\mathbf{Differentiated\ Convergence}}
\end{aligned}
$$

Their recurrence does not prove Semantic Phase Lock.

It explains why the hypothesis arose.

The final proposition of the study is therefore not that semantic systems can become perfectly stable, perfectly identical, or free of noise.

It is almost the opposite.

A semantic trajectory may change.

It may be interrupted.

It may move between models.

It may be reformulated.

It may experience displacement.

Different systems may produce genuinely different expressions.

Yet beneath those differences, specified semantic relationships may remain preserved or recoverable.

If continuity survives disruption,

if coherence survives transformation,

and if convergence survives differentiation without collapsing into sameness,

then the relevant phenomenon is not semantic immobility.

It is a stable relationship **through motion**.

That candidate regime is what this study calls:

$$ \boxed{\textbf{Semantic Phase Lock}} $$

The first question was:

> **What happens when continuity is disrupted?**

The second was:

> **What patterns remain?**

After the full trajectory of the study, the final question becomes:

$$ \boxed{ \begin{gathered} \textbf{Can continuity, coherence, and differentiated convergence}\\ \textbf{remain jointly stable while the semantic trajectory continues to change?} \end{gathered} } $$

That question remains open.

But it is no longer only an intuition.

**It is now a testable hypothesis.**