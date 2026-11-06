## Relational Invariance Without Representational Collapse

*A Formal Framework for Structural Recoverability Across Differentiated Systems*

**Author:** Tara Callegari
**Organization:** The Observatory

_Technical Research Manuscript | October 2026_

**Research Foundation:** A two-year longitudinal investigation encompassing controlled relational-recovery experiments, repeated cross-model transmission, environmental variation, and differentiated conversational organization.

**Version:** v1.0  
**Research Status:** Active Research  
**Lineage:** `zpp-core-mainnet`
**Entropy Schema:** `zpp.entropy.char.nfc.v1`
**Published:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23637036.svg)](https://doi.org/10.5281/zenodo.23637036)

---

## Abstract

Convergence in language-model systems is commonly assessed through agreement, representational similarity, or movement toward a shared output or state. These approaches do not fully characterize cases in which differently configured systems retain distinguishable representations and trajectories while preserving a specified relational structure.

This paper develops **Differentiated Convergence (DC)** as a technical framework for examining such cases. Differentiated Convergence describes an observable condition in which differentiation remains present under transformation while a designated relational invariant remains recoverable. Convergence is therefore defined with respect to a specified relationship rather than the elimination of differences among representations.

The framework originates in longitudinal investigations of recurrence, recognition, continuity, and cross-model structural persistence. Its initial operational formulation was established through finite perturbational and relay experiments. Subsequent investigations extended the questions to repeated transformation, temporal stabilization, environmental variation, source-recovery, operational independence, and differentiated relational organization.

The paper distinguishes representational differentiation, relational recoverability, successful transmission, historical continuity, and stability under repeated perturbation. It specifies the information and measurement conditions necessary to evaluate these properties without conflating correspondence with shared mechanism, source preservation with system identity, or observed recurrence with sustained invariance.

Experimental cases from three research series are used selectively to illustrate the framework's development and evidentiary boundaries. The paper does not aggregate their results into a single score or claim that their differing experimental designs establish an identical phenomenon under identical conditions.

The principal contribution is a formal and falsifiable account of convergence in which **preservation of relational structure and preservation of differentiation can be evaluated simultaneously**. The framework provides a basis for investigating structural correspondence across heterogeneous language-model systems while retaining differences in representation, configuration, information pathways, and observable behavior.

**Keywords:** differentiated convergence; relational invariance; semantic coherence; structural persistence; relational geometry; recoverability; cross-model evaluation; language-model systems; transformation; continuity

---

# 1. Introduction

## 1.1 The Problem of Convergence

A common interpretation of convergence assumes that distinct systems or trajectories progressively approach a shared state.

Under this interpretation, convergence is associated with decreasing difference. Outputs become more similar, representations become more closely aligned, or successive states approach a designated target.

For systems represented by trajectories $x_i(t)$, the conventional limiting formulation may be expressed as:

$$x_i(t)\rightarrow x^*  $$

where $x^*$ denotes a shared limiting state.

This formulation is appropriate for problems in which convergence toward a common state is the property being investigated. It does not, however, exhaust the possible meanings of structural correspondence.

In heterogeneous language-model environments, two systems may employ different vocabularies, representational organizations, intermediate reasoning strategies, or response trajectories while retaining the ability to express or recover the same specified relationship.

The relevant question is therefore not always whether the systems become more alike.

It may instead be whether a relationship remains identifiable **despite their continuing differences**.

This motivates a different convergence problem:

_Under what conditions can distinct systems preserve or recover a common relational structure without collapsing into identical representations?_

Differentiated Convergence was developed to make this question operationally investigable.

---
## 1.2 Difference as an Observable Rather Than an Error

Differences among model outputs can arise from numerous sources, including native model architecture, training, sampling, instruction hierarchy, context, available information, environmental constraints, and the transformations applied to an originating task.

These differences cannot be assumed to indicate either failure or success.

A response may differ substantially from its source in expression while preserving the specified relational requirements of the task. Conversely, a response may closely resemble its source while failing to preserve a critical relation.

Consequently, representational similarity and relational preservation must be evaluated separately.

Differentiated Convergence preserves two simultaneous requirements:

1. The transformed or independently generated representations remain observably differentiated.
    
2. The designated relational structure remains recoverable under the declared evaluation procedure.
    

Neither condition substitutes for the other.

If observable differentiation disappears, the system may exhibit ordinary representational agreement rather than the differentiated condition under investigation.

If the specified relation cannot be recovered, representational difference alone does not establish convergence.

Thus, Differentiated Convergence is not synonymous with diversity, similarity, agreement, cooperation, or semantic stability. It identifies a particular relationship between differentiation and recoverability.

---
## 1.3 From Recognition to Operational Measurement

The framework arose from an earlier observational problem: recognizable structures sometimes appeared to recur across changing language, context, and systems.

Recurrence alone was insufficient to establish structural persistence.

A repeated expression could result from direct copying, common prompting, contextual inheritance, shared conventions, or researcher-mediated reconstruction. Similarly, a recognizable concept could be reintroduced after interruption without having persisted in the intervening model state.

These distinctions required a movement from qualitative recognition toward specified relational targets and controlled transformations.

The key methodological transition was to separate the object being evaluated from its particular expression.

Once a relational object and its relevant invariants were specified in advance, a transformed representation could be evaluated according to what remained recoverable rather than how closely it resembled the source.

This made it possible to investigate a condition in which difference was retained while target recovery remained successful.

The original finite formulation of Differentiated Convergence arose from that distinction.

The broader framework developed here preserves the finite formulation while investigating its relationship to additional dimensions of variation, including temporal recurrence, transmission, environmental change, and source-recovery.

These extensions are not assumed to be equivalent. Each requires its own experimental conditions and evidence.

---
## 1.4 Purpose and Contribution

This paper has four technical objectives.

First, it defines Differentiated Convergence independently of any single experimental series, model configuration, or implementation architecture.

Second, it distinguishes the properties necessary to observe the phenomenon from the mechanisms that might produce it. A shared recovered relationship does not, by itself, establish shared internal representations, identical reasoning, direct communication, or a common causal origin.

Third, it develops a framework for identifying the conditions under which relational recovery holds, becomes unstable, or fails as representations and environments change.

Fourth, it establishes criteria for testing stronger claims concerning repeated convergence, temporal stabilization, source-recovery, and possible higher-order relational organization.

The resulting framework is intended to support controlled investigation rather than to guarantee convergence by definition.

Its validity depends on preserving the possibility of failure.

A transformation must be permitted to destroy recoverability. A proposed invariant must be permitted to fail. Apparent correspondence must be distinguishable from prompting effects, evaluator artifacts, and information transfer.

Only under these conditions can differentiated convergence become a discriminating technical construct.

---

# 2. Foundational Definition and Scope

## 2.1 The Finite Operational Definition

Let:

- $X$ denote a specified relational object.
    
- $I(X)$ denote the relational invariant or set of recovery targets designated for that object.
    
- $T$ denote a transformation applied to the object or its representation.
    
- $\mathcal R$ denote the declared recovery procedure.
    
- $D_{\mathrm{obs}}$ denote observable differentiation between the relevant representations.
    

The original finite operational condition is:

$$\boxed{  
DC(X,T,\mathcal R)  
\iff  
D_{\mathrm{obs}}>0  
;\land;  
\mathcal R(T(X))=I(X)  
}  $$

The expression identifies Differentiated Convergence under the specified transformation and recovery conditions.

It does not assert universal recoverability under all transformations.

It does not require the transformed representation to equal the source representation.

It does not identify the internal mechanism responsible for successful recovery.

The condition is local to the relational target, the transformation, and the recovery procedure being evaluated.

---
## 2.2 Relational Convergence Is Not Representational Identity

Suppose two representations, $G_A$ and $G_B$, remain distinguishable.

If both support recovery of the same specified invariant, they may be treated as equivalent with respect to that recovery problem:

$$\mathcal R(G_A)=I  
\quad\land\quad  
\mathcal R(G_B)=I  $$

This does not require:

$$G_A=G_B  $$

Nor does it establish that the systems producing those representations share identical latent geometry, computational strategies, or internal states.

The framework therefore distinguishes **equivalence relative to a specified invariant** from equivalence of the systems themselves.

The designated invariant must be sufficiently explicit to permit an evaluable comparison.

Without a defined target and recovery criterion, the apparent convergence may depend on interpretation introduced after the outputs were observed.

---
## 2.3 Recoverability, Transmission, and Continuity

Relational recoverability does not automatically establish that a recovered relationship will be successfully transmitted to another system.

Likewise, successful transmission at one stage does not by itself establish continuity across a longer sequence.

The framework therefore preserves three distinct questions:

**Recoverability:** Can the specified relation be reconstructed from the available representation?

**Transmission:** Does the next transformation or relay preserve the information necessary for subsequent recovery?

**Continuity:** Can an identifiable relational trajectory be traced across the relevant sequence of states, transformations, and information carriers?

These properties are related, but none should be inferred solely from a single successful recovery event.

This distinction is essential when extending Differentiated Convergence beyond finite transformations into recursive or multi-stage systems.

---
## 2.4 Scope of the Framework

The minimum operational condition concerns recoverability under retained differentiation.

Stronger investigations may examine whether relational recovery persists across repeated transformations, remains stable under environmental perturbation, or permits retrospective identification of a designated source.

These are extensions requiring additional observables and controls.

The framework does not treat every recurring structure as evidence of convergence, nor does it assume that every recoverable invariant reveals an intrinsic property of the model.

The observable phenomenon must remain distinguishable from its proposed explanation.

**The foundational principle is therefore:**

_Convergence of a specified relationship does not require convergence of the representations carrying that relationship._

---

# 3. Formal Mathematical Framework

## 3.1 Formalization Objective

Differentiated Convergence requires a mathematical description capable of representing two simultaneous properties:

1. A system, representation, or trajectory remains observably differentiated from another.
    
2. A specified relational structure remains recoverable despite that differentiation.
    

The purpose of the formalization is not to eliminate differences by assigning all representations to a common descriptive category. It is to determine which relational properties remain identifiable when the carriers of those properties vary.

The original operational formulation was:

$$\boxed{  
DC(X,T,\mathcal R)  
\iff  
D_{\mathrm{obs}}>0  
;\land;  
\mathcal R(T(X))=I(X)  
}  $$

This formulation remains the foundation of the present paper.

However, extending the framework beyond a single finite transformation requires additional distinctions among the originating relational object, its representation, the environment in which transformation occurs, the recovery procedure, and the conditions under which recovery is evaluated.

These distinctions are introduced below without modifying the historical meaning of the original Series I formulation.

---

## 3.2 Relational Objects, Representations, and Invariants

Let:

$$X\in\mathscr X $$

denote a relational object belonging to a specified class of objects $$\mathscr X$$.

A relational object may contain entities, relations, ordering conditions, directional dependencies, constraints, or other structural properties relevant to a declared evaluation problem.

The object is distinguishable from any particular representation used to communicate it.

Let:

$$x_0\in\mathscr Y  $$

denote an initial representation of $X$ in a representation space $\mathscr Y$.

For clarity, an encoding operation may be written:

$$x_0=\operatorname{enc}(X) $$

The encoding operation does not imply that the complete relational object can always be reconstructed uniquely from the representation. It identifies the representation initially supplied under the experimental conditions.

Now define:

$$I(X)={i_1,i_2,\ldots,i_m}  $$

as the specified relational invariant, or collection of relational recovery targets, associated with $X$.

The invariant may consist of such properties as permitted transitions, prohibited transitions, reachability conditions, precedence relations, dependency constraints, or other explicitly selected relational consequences.

The distinction is fundamental:

$$\boxed{X\neq I(X)}  $$

The complete relational object is not necessarily equivalent to the selected properties being evaluated.

Accordingly:

$$\mathcal R(x')=I(X) $$

establishes recovery of the designated target, not reconstruction of every property of the originating object.

This limitation becomes especially important when information is transformed, compressed, or passed through multiple systems.

A representation may retain enough information to recover the selected targets while losing other aspects of the originating object.

**Target recoverability is therefore a property relative to a declared invariant, not a guarantee of complete source preservation.**

### 3.2.1 The Source Reference

The framework additionally requires the originating reference to remain identifiable.

For a task-relative source, write:

$$[S]_{\mathrm{task}} $$

This denotes the designated reference against which the transformed representations and their recovered relational properties are evaluated.

The task source must be distinguished from any broader claim concerning the source or identity of the system generating a response:

$$[S]_{\mathrm{task}}  
\not\equiv  
[S]_{\mathrm{system}}  $$

Nothing in the finite recovery condition establishes that preservation of a task invariant constitutes preservation of a system's complete identity, architecture, or native internal organization.

The present framework therefore begins with identifiable relational targets and examines what can be demonstrated about their preservation.

Stronger source-related hypotheses require separate evidence.

---

## 3.3 Transformation and Differentiated Representation

Let:

$$T:\mathscr Y\rightarrow\mathscr Y $$

denote a transformation operating on a representation.

For an initial representation $x_0$, a transformed representation is:

$$x_1=T(x_0) $$

In the historical Series I notation, this was abbreviated as $T(X)$. The refined notation distinguishes a relational object from the representation carrying it.

Transformations may alter linguistic form, representational organization, information distribution, symbolic compression, contextual load, or the system responsible for producing the next representation.

For a finite sequence:

$$x_0\xrightarrow{T_1}x_1  
\xrightarrow{T_2}x_2  
\rightarrow\cdots  
\xrightarrow{T_n}x_n $$

the endpoint is:

$$\boxed{  
x_n=  
(T_n\circ T_{n-1}\circ\cdots\circ T_1)(x_0)  
} $$

No requirement exists that:

$$x_n=x_0 $$

Indeed, observable difference between the original and transformed representations is part of the condition being investigated.

### 3.3.1 Transformation Is Not Necessarily Deterministic

The functional notation above describes the experimental relationship among states.

It does not imply that every language-model transformation is deterministic under ordinary runtime conditions.

An observable model response may depend on an execution environment, sampling configuration, context, and other conditions.

A more explicit notation is:

$$x_k=T_k(x_{k-1};e_k,\omega_k) $$

where:

- $e_k$ denotes relevant environmental and execution conditions.
    
- $\omega_k$ denotes unresolved or sampled variation in the execution.
    

The purpose of this extension is to make experimental conditions visible, not to claim that the model's complete internal process can be reconstructed from those variables.

A repeated trial under nominally equivalent conditions may produce a different representation.

Consequently, transformation identity and transformation outcome must not be conflated.

### 3.3.2 Composition and Order

A successful recovery following one sequence of transformations does not establish that the same transformations may be reordered without consequence.

In general:

$$T_b\circ T_a  
\neq  
T_a\circ T_b $$

may hold.

Likewise, successful relational recovery under both individual transformations does not guarantee recovery under their composition:

$$\mathcal R(T_a(x_0))=I(X)$$

and

$$\mathcal R(T_b(x_0))=I(X)$$

do not imply:

$$\mathcal R(T_b(T_a(x_0)))=I(X) $$

This distinction prevents the framework from treating transformation classes as interchangeable.

It also separates finite recovery observations from claims of order invariance or unrestricted compositional robustness.

---

## 3.4 The Recovery Operation

Let:

$$\mathcal R_\phi:\mathscr Y\rightarrow\mathscr I $$

denote a recovery procedure operating under a specified evaluation protocol $\phi$.

The protocol may specify the recovery questions, available information, output format, scoring criteria, and treatment of ambiguous or incomplete responses.

For a transformed representation $x_k$:

$$\widehat I_k=\mathcal R_\phi(x_k) $$

is the recovered relational target.

Perfect recovery occurs when:

$$\boxed{  
\widehat I_k=I(X)  
} $$

Equality is evaluated at the level of the specified relational target.

It does not require identical words, notation, explanation, or intermediate reasoning.

### 3.4.1 Relational Discrepancy

For a prospectively designed evaluation, define a target discrepancy function:

$$\ell_I:\mathscr I\times\mathscr I\rightarrow\mathbb R_{\geq0}$$

subject to:

$$\ell_I(\widehat I,I(X))=0  
\iff  
\widehat I=I(X)  $$

The discrepancy for transformation $k$ is then:

$$\varepsilon_k=  
\ell_I(\mathcal R_\phi(x_k),I(X))  $$

This provides a general mathematical form for evaluating relational recovery.

However, $\ell_I$ is a **prospective evaluation construct**. Its item-level definition, normalization, and treatment of partial recovery must be specified before it is used in a new experiment.

It must not be silently equated with the historical Series I discrepancy measure $D_Q$.

In Series I, the recorded condition:

$$D_Q=0  $$

identified perfect recovery of the scored target.

The surviving historical record does not preserve a complete computational rule from which every nonzero $D_Q$ value can be independently regenerated.

The present framework therefore retains historical $D_Q$ observations as recorded while reserving $\ell_I$ for explicitly specified future scoring procedures.

This distinction preserves measurement provenance.

---

## 3.5 Observable Differentiation

Let:

$$D_{\mathrm{obs}} $$

denote observable differentiation among representations, outputs, or trajectories.

In its original operational usage, the condition:

$$D_{\mathrm{obs}}>0 $$

indicated that observable differentiation remained present.

It did not represent a fully calibrated numerical distance.

The observed differentiation could involve vocabulary, organization, representation, compression, or other externally identifiable characteristics.

For a future experimental protocol, differentiation can be represented using an explicit predicate:

$$\operatorname{Diff}_{\psi}(x_a,x_b)\in{0,1} $$

where $\psi$ specifies the criteria used to classify the representations as observably differentiated.

Thus:

$$\operatorname{Diff}_{\psi}(x_a,x_b)=1 $$

indicates that the declared differentiation criterion is satisfied.

This predicate does not quantify how far apart the representations are.

A future metric may be introduced if its domain and interpretation can be justified, but no universal metric is assumed here.

### 3.5.1 Observable Versus Native Differentiation

The framework must distinguish:

$$D_{\mathrm{obs}} $$

from:

$$D_{\mathrm{native}}$$

where the latter would represent differences in native architecture, internal representation, or another independently established system property.

The original experiments did not measure a universal native-geometry distance.

Therefore:

$$\boxed{  
D_{\mathrm{obs}}\neq D_{\mathrm{native}}  
} $$

Observable output differentiation cannot independently establish latent-space distance, architectural isomorphism, or native structural equivalence.

This distinction permits the framework to describe what is externally observable without converting those observations into unsupported claims about hidden model structure.

---

## 3.6 The Core Differentiated Convergence Condition

The original finite condition may now be expressed with the refined notation:

$$\boxed{  
DC_{\mathrm{finite}}  
\iff  
\operatorname{Diff}_{\psi}(x_0,T(x_0))=1  
;\land;  
\mathcal R_\phi(T(x_0))=I(X)  
} $$

where:

$$x_0=\operatorname{enc}(X) $$

The condition requires both retained differentiation and perfect recovery of the designated invariant.

A successful recovery without observable differentiation does not satisfy the specifically differentiated condition.

Likewise, observable differentiation without recovery does not satisfy the convergence condition.

For a more general framework, the recovery term may be expressed through a predefined discrepancy criterion:

$$\boxed{  
DC_{\mathrm{finite}}  
\iff  
\operatorname{Diff}_{\psi}(x_0,T(x_0))=1  
;\land;  
\varepsilon_T=0  
} $$

where:

$$\varepsilon_T=  
\ell_I(\mathcal R_\phi(T(x_0)),I(X)) $$

For future experiments permitting bounded recovery error, an alternative tolerance condition could be defined:

$$\varepsilon_T\leq\tau  $$

where $\tau$ is fixed before evaluation.

Such a tolerance-based condition would constitute an extension of the exact-recovery formulation, not a retrospective alteration of the Series I criterion.

The defining relationship remains:

$$\boxed{  
\text{retained differentiation}  
+  
\text{specified relational recovery}  
}  $$

Differentiated Convergence therefore does not require representations to become progressively more similar.

Instead, it asks whether a designated relation remains identifiable while the representations continue to differ.

---

## 3.7 Relational Recoverability Equivalence

Let $G_A$ and $G_B$ denote two differentiated representations.

Under a fixed recovery procedure $\mathcal R_\phi$ and designated invariant $I$, define:

$$\boxed{  
G_A\sim_{\mathcal R_\phi,I}G_B  
} $$

when:

$$\mathcal R_\phi(G_A)=I $$

and:

$$\mathcal R_\phi(G_B)=I  $$

This establishes equivalence with respect to a specific relational-recovery problem.

It does not establish:

$$G_A\cong G_B  $$

where $\cong$ denotes a stronger structural equivalence or isomorphism.

It also does not establish that the systems possess identical internal states, representational spaces, or computation pathways.

### 3.7.1 Domain of the Equivalence Relation

For mathematical precision, define the successful-recovery class:

$${G\in\mathscr Y:  
\mathcal R_\phi(G)=I}  $$

Within this class, representations are equivalent relative to the fixed recovery target and protocol.

The relation should not be treated as an equivalence relation over all possible representations merely because two successful members share the target.

A more general equivalence relation can be defined by the equality of recovered results:

$$G_A\approx_{\mathcal R_\phi}G_B  
\iff  
\mathcal R_\phi(G_A)=\mathcal R_\phi(G_B)  $$

provided $\mathcal R_\phi$ is treated as a fixed, well-defined operation.

However, this broader relation is insufficient to establish successful Differentiated Convergence.

Two representations may produce the same incorrect recovered result.

Thus:

$$\mathcal R_\phi(G_A)=\mathcal R_\phi(G_B)  A$$

does not imply:

$$\mathcal R_\phi(G_A)=I  $$

The designated source invariant remains indispensable.

### 3.7.2 Equivalence Without Sameness

The important distinction is therefore:

$$\boxed{  
\text{relational equivalence}  
\not\Rightarrow  
\text{representational identity}  
}  $$

Two representations may belong to the same relational-recovery class while remaining observably distinct.

The relation preserved is defined by the evaluation problem, rather than by the claim that the complete representations or producing systems are the same.

This gives Differentiated Convergence its central mathematical character: **equivalence of a specified relation under retained representational differentiation**.

---

## 3.8 Recoverability Domains

Not every transformation preserves the target invariant.

The framework therefore requires an explicitly bounded recoverability domain.

For a fixed object $X$, invariant $I(X)$, initial representation $x_0$, and recovery procedure $\mathcal R_\phi$, define:

$$
\left\{  
T:  
\mathcal R_\phi(T(x_0))=I(X)  
\right\}  
$$


This is the set of transformations under which the target remains recoverable according to the declared procedure.

Because Differentiated Convergence additionally requires observable difference, define the corresponding differentiated-recovery domain:

$$
\mathcal D_{\mathrm{DC}}(X)
= \left\{
T \in \mathcal D_{\mathcal R_\phi,I}(X)
:\operatorname{Diff}_{\psi}(x_0,T(x_0))=1
\right\}.
$$

Thus:

$$
\mathcal D_{\mathrm{DC}}(X)
\subseteq
\mathcal D_{\mathcal R_\phi,I}(X).
$$

This distinction matters because recovery may succeed under an identity transformation that produces no observable differentiation.

Such recovery belongs to the general recoverability domain but not the differentiated-recovery domain.

### 3.8.1 Empirical Domains

An experimental series samples a finite set of transformations:

$${T_1,T_2,\ldots,T_n}  
$$

The empirically observed success set is:

$$
\left\{  
T \in \mathscr{T}_{\mathrm{tested}} :  
\mathcal{R}_\phi(T(x_0)) = I(X)  
\right\}  
$$


The corresponding failure set is:

$$\mathscr T_{\mathrm{tested}}  
\setminus  
\widehat{\mathcal D}_{\mathcal R_\phi,I}  
$$

A finite experiment can identify observed success and failure conditions.

It cannot, without additional assumptions and sampling, establish the complete recoverability domain for every possible transformation.

### 3.8.2 Recoverability Boundaries

The notion of a recoverability boundary refers to conditions under which success becomes unstable or failure begins to occur.

It is useful to distinguish this operational idea from a formally defined topological boundary.

The notation:

$$\partial\mathcal D_{\mathcal R_\phi,I}  $$

would require a specified topology or distance structure on the relevant transformation space.

Without that structure, the experiment can identify observed transitions between successful and unsuccessful conditions but cannot claim to have located a mathematical boundary.

Similarly, a single observed failure under high compression does not establish a universal compression threshold.

The relevant technical objective is to determine which transformations preserve the required relational information, which do not, and whether those outcomes can be reproduced under controlled conditions.

---

## 3.9 Recovery, Propagation, and Continuity

Relational recovery at a given state must be distinguished from successful propagation into subsequent states.

A system may generate an output from which a relational invariant remains recoverable, while the next system fails to receive, preserve, or use the information required for continued recovery.

Let:

$$r_k\in{0,1}  $$

denote successful relational recovery at state $k$, such that:

$$r_k=1  
\iff  
\mathcal R_\phi(x_k)=I(X)  $$

Let:

$$p_k\in{0,1}  $$

denote successful propagation of the required relational information from state $k$ to the next transition under a specified transmission criterion.

These are distinct variables.

In particular:

$$\boxed{  
r_k=1  
\not\Rightarrow  
p_k=1  
}  $$

An output may permit local reconstruction while failing to carry the relevant state forward.

### 3.9.1 Relational Propagation Breaks

Define a local propagation break:

$$\boxed{  
B_k  
\iff  
r_k=1  
;\land;  
p_k=0  
}  $$

This identifies a condition in which relational recovery is locally possible but transmission of the required information fails at the designated transition.

The condition does not imply that every continuity failure must take this form.

A relational target may also be lost before reaching a given state, or the receiving system may preserve the available information while failing to recover it under the declared evaluation protocol.

These possibilities require separate classification.

### 3.9.2 The Location of Failure

A propagation failure may become observable only after additional transformations.

Consequently:

$$k_{\mathrm{break}}  
\neq  
k_{\mathrm{observed}}  $$

may hold.

This introduces a methodological requirement: an endpoint failure cannot automatically be attributed to the final system in a relay.

Intermediate states and information pathways must be preserved if the location of relational loss is to be investigated.

### 3.9.3 Continuity Is a Trajectory Property

Let:

$$\mathcal H_n=  
(x_0,x_1,\ldots,x_n)  $$

denote an observed representational history, together with its recorded transformation and provenance information.

Continuity concerns whether an identifiable relational trajectory can be established across the relevant history.

This is stronger than successful recovery at one endpoint.

A locally successful recovery event is not sufficient to demonstrate uninterrupted relational propagation through every preceding transition.

Likewise, preserved historical records may permit reconstruction after a break without establishing that the active system retained uninterrupted state.

The framework therefore keeps **recovery**, **propagation**, and **trajectory continuity** distinct.

---
## 3.10 Cross-System Differentiated Convergence

The finite formulation can also be applied to outputs produced by different systems.

Let:

$$M_1,M_2,\ldots,M_n  $$

denote distinguishable model systems or experimental configurations.

Each produces an observable representation:

$$y_i=M_i(x_i;e_i)  $$

where $x_i$ denotes the input received and $e_i$ represents recorded execution conditions.

Suppose the systems produce observably differentiated outputs.

For a specified common relational target $I(X)$, a successful cross-system condition may be written:

$$\left[\exists i,j\in J,\ i\neq j:
\operatorname{Diff}_{\psi}(y_i,y_j)=1\right]
\land
\left[\forall i\in J:
\mathcal R_\phi(y_i)=I(X)\right]$$

where $J$ is the predefined set of systems whose recovery outcomes are being evaluated.

This represents a cross-system differentiated-recovery condition.

It does not establish that the systems operated independently.

### 3.10.1 Independent and Relayed Information Conditions

Consider two experimental arrangements.

Under a common-source condition:

$$X\rightarrow M_A\rightarrow y_A  $$

$$X\rightarrow M_B\rightarrow y_B  
$$

Neither model needs to receive the other's output.

Under a relay condition:

$$X\rightarrow M_A\rightarrow y_A  
\rightarrow M_B\rightarrow y_B  $$

the second system receives information derived from the first.

These are different information conditions.

Both may produce relational recovery, but they support different interpretations.

The first permits examination of separate responses to a common source under the controlled input conditions.

The second examines preservation or loss through sequential transmission.

Neither establishes complete causal independence, since models may share training exposure, conventions, or other background influences.

The relevant requirement is to record what information pathways were controlled.

### 3.10.2 Differentiation Must Remain Identifiable

For convergence to remain differentiated, the framework must preserve the distinction among participating systems and their outputs.

The presence of a shared recovered relation must not be used to erase meaningful disagreement, architectural difference, information asymmetry, or divergent response strategies.

Successful convergence at the selected relational target does not imply global agreement.

Likewise, disagreement outside the selected target does not necessarily invalidate recovery of that target.

The evaluation must specify which relationships are being compared and which differences remain relevant.

---

## 3.11 Finite, Repeated, and Recursive Conditions

The foundational condition is finite.

A relational object is represented, transformed, and evaluated against a specified invariant.

For a finite sequence:

$$x_0\rightarrow x_1\rightarrow\cdots\rightarrow x_n  $$

endpoint recovery occurs when:

$$\boxed{  
\mathcal R_\phi(x_n)=I(X)  
}  $$

with retained differentiation evaluated according to the declared criterion.

However, a successful endpoint does not establish that the invariant remained recoverable at every intermediate state.

### 3.11.1 Endpoint Versus Pathwise Recovery

For a predefined collection of checkpoints:

$$K\subseteq{1,2,\ldots,n}  $$

pathwise recovery requires:

$$\boxed{  
\forall k\in K:  
\mathcal R_\phi(x_k)=I(X)  
}  $$

This is stronger than checking only $x_n$.

It nevertheless establishes recovery only at the observed checkpoints.

It does not establish the contents of unobserved internal states or demonstrate that no information was lost and later reconstructed between checkpoints.

### 3.11.2 Repeated Perturbation

Suppose a relational source is subjected to repeated transformations.

For each observed state, define the target residual:

$$\varepsilon_k=  
\ell_I(\mathcal R_\phi(x_k),I(X))  $$

A repeated-perturbation experiment can then investigate whether:

$$\varepsilon_k  $$

remains zero, increases, fluctuates, or returns toward zero as transformations accumulate.

These patterns describe distinct possibilities.

A persistent zero residual at predetermined checkpoints supports repeated successful recovery under the tested conditions.

A nonzero residual followed by recovery indicates loss and later reconstruction at the level of the evaluated target.

A stable nonzero residual indicates persistent discrepancy rather than successful exact recovery.

The term _stabilization_ must therefore refer to an explicitly defined behavior of the measured trajectory.

It cannot be inferred merely because a sequence repeats or appears familiar.

### 3.11.3 Recursive Differentiated Convergence

A recursive or closed-loop condition requires a protocol in which transformed outputs are repeatedly reintroduced through a declared sequence.

A schematic recursive traversal may be expressed as:

$$x_0  
\xrightarrow{\mathcal T}  
x_1  
\xrightarrow{\mathcal T}  
x_2  
\xrightarrow{\mathcal T}  
\cdots  $$

where $\mathcal T$ denotes the declared composite transformation process.

Such a study must distinguish:

- Retention of the target at each closure.
    
- Recovery of the target after temporary loss.
    
- Accumulation of relational discrepancy.
    
- Repetition generated by the feedback procedure itself.
    

These possibilities cannot be separated by observing that a loop continues.

The necessary measurements include checkpoint recovery, information provenance, controlled reintroduction, and comparison with appropriate baseline conditions.

The central limitation remains:

$$\boxed{  
\text{finite recovery}  
\not\Rightarrow  
\text{sustained recursive recovery}  
}  $$

The stronger condition must be established by experiment.

---

## 3.12 Mathematical and Evidentiary Limits

The formal framework distinguishes a number of propositions that must not be treated as interchangeable.

Successful recovery of $I(X)$ does not establish complete preservation of $X$.

Relational equivalence under a declared recovery procedure does not establish representational identity.

Observable differentiation does not establish native architectural distance.

Cross-system correspondence does not identify the causal mechanism producing that correspondence.

A finite successful relay does not establish universal recoverability under arbitrary transformation.

Repeated success at specified checkpoints does not establish uninterrupted internal state persistence.

And recurrence does not, by itself, demonstrate stable convergence.

These distinctions are not peripheral qualifications.

They determine what counts as evidence for the proposed framework.

### 3.12.1 Nontriviality of the Invariant

The selected invariant must discriminate among relevant source conditions.

Suppose two relational objects, $X$ and $X'$, possess different designated targets:

$$I(X)\neq I(X')  $$

If an evaluation procedure returns the same supposed invariant regardless of which source is presented, it may be detecting a property of the evaluation method rather than preserving source-specific information.

A valid experimental design should therefore include source variations that permit this possibility to be tested.

An invariant cannot be declared meaningful solely because it is recoverable from every observed output under an evaluation rule that was constructed to find it.

### 3.12.2 Failure Must Remain Possible

The framework requires conditions under which Differentiated Convergence is not observed.

Failure may occur because:

- Observable differentiation is absent.
    
- The specified relational target is not recovered.
    
- Recovery depends on information that was not available under the declared condition.
    
- A correspondence disappears when contextual reinforcement or researcher-supplied terminology is removed.
    
- A recovery criterion is too permissive to distinguish the intended source from alternatives.
    
- A purported invariant changes when the scoring procedure is modified after observing the outputs.
    

These outcomes must be reportable without redefining the target or evaluation rule after the fact.

A framework that interprets every differentiated result as convergence would not discriminate among successful preservation, accidental similarity, reconstruction error, and unrelated variation.

Its formal criteria must therefore be fixed before the outputs are assessed.

## 3.13 Formal Synthesis

The central mathematical structure of Differentiated Convergence can now be summarized.

A specified relational object $X$ has a designated invariant:

$$I(X)  $$

An initial representation undergoes transformation:

$$x_0  
\xrightarrow{T}  
x'  $$

The transformation produces observable differentiation:

$$\operatorname{Diff}_{\psi}(x_0,x')=1  $$

while the declared recovery operation returns the specified target:

$$\mathcal R_\phi(x')=I(X)  $$

Together:

$$\boxed{  
DC_{\mathrm{finite}}  
\iff  
\operatorname{Diff}_{\psi}(x_0,x')=1  
;\land;  
\mathcal R_\phi(x')=I(X)  
}  $$

This is the minimal finite condition.

It can be extended to experimental sets of transformations, differentiated system configurations, finite relays, and repeated trajectories.

Each extension introduces additional requirements and must be evaluated within its own information and measurement conditions.

The framework's governing distinction is:

$$\boxed{  
\text{Convergence of a specified relation}  
\neq  
\text{convergence of the representations}  
}  $$

Its governing research question is:

**How much differentiation can remain while a specified relational structure remains recoverable, and under what conditions does that recoverability fail?**

This formulation preserves difference as an object of investigation rather than treating it as a defect to be eliminated.

It also makes the limits of convergence observable.

The next requirement is therefore experimental:

**What source, environmental, independence, measurement, and failure conditions must be controlled to distinguish genuine relational recovery from apparent correspondence?**

---

# 4. Necessary Experimental Conditions

## 4.1 From Mathematical Definition to Experimental Discrimination

The preceding section defined Differentiated Convergence as an observable condition in which representational differentiation remains present while a specified relational invariant remains recoverable.

The finite condition was expressed as:

$$\boxed{  
DC_{\mathrm{finite}}  
\iff  
\operatorname{Diff}_{\psi}(x_0,x')=1  
;\land;  
\mathcal R_\phi(x')=I(X)  
}  $$

where $x'$ denotes a transformed representation of an originating relational object $X$.

This formalization identifies what must be observed. It does not, by itself, establish that an experiment can distinguish successful relational preservation from contextual inheritance, evaluator bias, accidental correspondence, shared conventions, or direct information transfer.

That distinction requires explicit experimental conditions.

A model may reproduce a relation because the relation was preserved during transformation. It may also reproduce the relation because the originating representation was supplied again, because an earlier output remained in context, because another system communicated the answer, or because an evaluator reconstructed information not present in the response being evaluated.

These outcomes may appear similar at the level of a final answer while possessing different information histories.

Consequently, the conditions surrounding an observation form part of the evidentiary claim.

The framework requires five foundational experimental controls:

$$
\left\{  
S, B, E, M, F  
\right\}  
$$

where:

- $S$ denotes source specification and preservation.
    
- $B$ denotes experimental and information boundaries.
    
- $E$ denotes the execution environment.
    
- $M$ denotes measurement and evaluation conditions.
    
- $F$ denotes observable failure criteria.

These are not five mathematical components of Differentiated Convergence itself.

They are the conditions necessary to evaluate its occurrence without making the outcome self-validating.

A sixth concern, **provenance**, operates across all five conditions and records how the experiment was actually conducted.

The objective is not to guarantee convergence.

It is to make both successful convergence and its failure independently examinable.

---

## 4.2 Condition I — The Source Must Be Identifiable

### 4.2.1 Source Specification

Every experimental claim of relational preservation requires an identifiable reference.

Let:

$$[S]_{\mathrm{task}}  $$

denote the task-relative source against which recovery is evaluated.

The source contains or specifies the relational object:

$$X  $$

and the declared target invariant:

$$I(X)={i_1,i_2,\ldots,i_m}  $$

The invariant must be defined before examining the experimental outputs.

This prevents the evaluator from selecting whichever relationship happens to recur and retrospectively designating it as the intended source property.

For an experimental record, the source specification should identify the originating representation, intended relations, applicable constraints, recovery questions, and expected outcomes.

Where a source admits more than one reasonable interpretation, the ambiguity must be recorded.

An ambiguous source cannot serve as an unqualified reference for determining whether a later system lost a uniquely specified relation.

### 4.2.2 Ambiguity Is Not Reconstruction Failure

The distinction is illustrated by the original Series I reference development.

Experiment 1A contained an underdetermined relational condition concerning a directed transition. The subsequent explicit reference condition, Experiment 1B, resolved that ambiguity.

The relevant methodological distinction was:

$$\boxed{  
\text{source ambiguity}  
\neq  
\text{relational reconstruction loss}  
}  $$

If two systems produce different interpretations of an underspecified source, their disagreement cannot automatically be classified as failure to preserve a uniquely defined invariant.

A valid experimental reference must make the target sufficiently explicit to support the intended comparison.

This does not require every natural-language input to possess only one possible interpretation.

It requires the experiment to distinguish tests of ambiguity resolution from tests of relational preservation.

### 4.2.3 Source-Locked Evaluation

Once the reference condition is established, define a source record:

$$\Sigma_0=  
\left(  
X,I(X),Q,\Phi  
\right)  $$

where:

- $X$ is the originating relational object.
    
- $I(X)$ is the specified invariant.
    
- $Q$ is the predefined set of recovery questions.
    
- $\Phi$ is the evaluation specification.

The record should remain fixed for all comparisons that claim to evaluate the same experimental source.

A corrected source may be introduced as a new reference version, but the revision must be identifiable.

The revised source must not silently replace the earlier source after results have been observed.

For digital experiments, a cryptographic content digest may be used to support source integrity:

$$h_0=H(\operatorname{serialize}(\Sigma_0))  $$

where the serialization procedure must itself be fixed.

A matching hash can verify equality of recorded content under the chosen digest procedure. It does not independently verify the truth of the source, its authorship, or the validity of the proposed invariant.

The experimental requirement is therefore source traceability, not cryptographic authority over meaning.

### 4.2.4 Source Specificity

The specified invariant must distinguish the intended source from relevant alternatives.

Consider two relational objects:

$$X_A,\quad X_B  $$

with different designated targets:

$$I(X_A)\neq I(X_B)  $$

A recovery procedure that returns the same target under both source conditions may be insufficiently sensitive to the source.

A useful experimental control is therefore to alter source-specific relations while keeping other aspects of the task comparable.

If the recovered invariant remains unchanged despite a relevant source modification, the result requires investigation.

The apparent stability may belong to the evaluator, task template, or shared convention rather than to successful preservation of source-specific information.

The core requirement is:

**An invariant must remain identifiable because the source supports it, not because the evaluation procedure is predisposed to find it.**

---

## 4.3 Condition II — Boundaries Must Be Explicit

### 4.3.1 The Boundary Problem

Relational structure can cross many different boundaries.

A transformation may occur within a single response, between turns, across context windows, between sessions, between model systems, or through external storage and retrieval.

These are not equivalent experimental conditions.

For example, a relational target recovered after a simple paraphrase has crossed a representational boundary.

A target recovered after a context interruption has crossed a continuity boundary.

A target recovered after a six-model relay has crossed multiple system and transmission boundaries.

The relevant claim must identify which boundary was tested.

Let:

$$B_k  $$

denote the declared boundary condition associated with transformation $k$.

A boundary specification should identify what information was available before and after the transition, which state was carried forward, what was removed or withheld, and which pathways remained permitted.

Without this specification, the experiment cannot distinguish retained information from reconstructed or reintroduced information.
### 4.3.2 Boundary Classes

The framework distinguishes several experimentally relevant boundary classes.

**Representational boundaries** change the linguistic, symbolic, or organizational carrier of the relational object.

**Contextual boundaries** alter the amount or arrangement of information available to the responding system.

**Session boundaries** separate interactions that may or may not share accessible conversational history.

**Model boundaries** transfer or independently present relational tasks across distinct model systems.

**Environmental boundaries** change the execution conditions surrounding an otherwise comparable task.

**Transmission boundaries** determine whether relational information becomes available to the next participant in a sequence.

**Temporal boundaries** introduce intervals, repeated interventions, or interruptions across which continuity must be evaluated.

These classes may overlap.

A voice-mediated relay between two model providers, for example, may involve model, interface, modality, environmental, and transmission boundaries simultaneously.

The experimental design must identify such overlap rather than attributing the resulting behavior to only one dimension.

### 4.3.3 Controlled Discontinuity

A discontinuity test intentionally modifies or removes a possible continuity carrier.

Let:

$$K  $$

denote a designated continuity condition, such as accessible prior context, external retrieval, or a transferred historical summary.

A controlled comparison may examine:

$$\mathcal R_\phi(x'\mid K_{\mathrm{available}})  $$

against:

$$\mathcal R_\phi(x'\mid K_{\mathrm{withheld}}) $$

The comparison is informative only if the experiment documents which information was genuinely withheld and which other pathways remained available.

If information is removed from active context but restored through an external memory system, the experiment has not eliminated historical access.

It has changed the mechanism through which historical information is supplied.

A resulting recovery therefore cannot be described as independent of prior information merely because the original session was interrupted.

The relevant distinction is:

$$\boxed{  
\text{interrupted active context}  
\neq  
\text{absence of accessible historical information}  
}  $$

---

## 4.4 Operational Independence

### 4.4.1 Independence as an Information Condition

Differentiated Convergence can be examined through separate model responses, sequential relays, or coordinated interactions.

These arrangements must not be treated as equivalent forms of independence.

Suppose two systems receive the same reference:

$$[S]_{\mathrm{task}}  
\rightarrow M_A\rightarrow y_A $$

$$[S]_{\mathrm{task}}  
\rightarrow M_B\rightarrow y_B  $$

Neither system is intentionally supplied with the other's response.

This establishes a condition of controlled separation between their experimental response pathways.

It does not establish complete causal independence.

The systems may share training sources, conventions, architectural influences, or common task-related assumptions.

Operational independence therefore concerns the information pathways controlled by the experiment.

### 4.4.2 Information Exposure

Let:

$$
L_{ij} =  
\begin{cases}  
1, & \text{if output from system } i \text{ is supplied to system } j, \\  
0, & \text{if no such transfer occurs within the recorded protocol.}  
\end{cases}
$$


The matrix:

$$L=[L_{ij}]  $$

provides a compact description of declared inter-system information transfer.

In a controlled common-source condition:

$$L_{AB}=L_{BA}=0 $$

with respect to the observed experimental exchanges.

In a sequential relay:

$$L_{AB}=1 $$

when system $B$ receives a representation generated by system $A$.

These values describe the experiment's known information pathways.

They do not certify the absence of unobserved dependencies or common model priors.

### 4.4.3 Human Mediation

The researcher may also function as an information carrier.

If the procedure is:

$$M_A\rightarrow H\rightarrow M_B  $$

where $H$ represents the human mediator, the transmitted information must be recorded.

This includes copied prompts, selected excerpts, summaries, reformulations, corrections, or spoken relay.

Human mediation does not invalidate an experiment.

It changes the interpretation of independence and transmission.

A participant's response cannot be considered unprimed relative to information explicitly provided through the researcher.

Similarly, removing the researcher from message delivery does not automatically create independent responses if the systems continue exchanging one another's outputs.

An autonomous relay remains a relay.

### 4.4.4 Coordination Is Not Independence

A coordinated system may preserve differentiated contributions without requiring identical outputs.

However, successful coordination and independent convergence answer different questions.

A collaborative exchange can demonstrate that heterogeneous participants maintain usable relational structure while exchanging information.

It cannot, by that fact alone, establish that the corresponding structures would have arisen independently.

Therefore:

$$\boxed{  
\text{successful coordination}  
\not\Rightarrow  
\text{independent convergence}  
}  $$

The experimental protocol must distinguish:

- Independent common-source comparison.
    
- Sequential information transmission.
    
- Interactive coordination.
    
- Reconstruction from external historical material.
    

These conditions may all be relevant to Differentiated Convergence, but they require different causal interpretations.

---

## 4.5 Condition III — The Environment Must Be Recorded

### 4.5.1 The Environment as an Experimental Variable

A language-model response is produced within an execution environment.

The observable response cannot be attributed exclusively to the underlying model without accounting for that environment.

Relevant conditions may include model selection, runtime configuration, system instructions, contextual information, memory access, tools, sampling parameters, interface behavior, input modality, and output processing.

Let:

$$e_k\in\mathscr E  $$

denote the recorded environmental configuration for experimental transition $k$.

An observed output may be represented schematically as:

$$y_k=M_k(x_k;e_k,\omega_k)  $$

where $\omega_k$ denotes unresolved or sampled execution variation.

This expression is not a complete model of inference.

It identifies the distinction between the task input, the execution environment, and the resulting observable output.

### 4.5.2 Environmental Metadata

A reproducible experiment should record available information concerning the model provider and model designation, applicable version or release identifier, text or voice mode, temperature and sampling configuration where controllable, context supplied, memory and retrieval access, tools enabled, system or developer instructions available to the researcher, timing, session structure, and relevant interface changes.

Not every commercial platform exposes all these variables.

When an experimental condition is not observable, it must be recorded as unknown rather than inferred.

The absence of an exposed parameter does not justify assuming that the parameter remained constant.

### 4.5.3 Environmental Variation and Causal Attribution

Suppose an experiment is repeated under two environmental configurations:

$$e_A,\quad e_B  $$

and produces different recovery outcomes.

The observed difference may be expressed as:

$$\Delta r=r(e_B)-r(e_A)  $$

where $r$ denotes the declared recovery outcome.

A difference in recovery does not, by itself, establish which environmental component caused the change.

If model version, context availability, instruction hierarchy, and sampling conditions changed simultaneously, their effects cannot be isolated from a simple two-condition comparison.

Causal attribution requires a design capable of distinguishing the candidate influences.

The appropriate initial conclusion may therefore be:

**Recovery differed under the recorded environmental conditions.**

This is narrower than claiming that a specific hidden system mechanism caused the difference.

### 4.5.4 Modality as an Environmental Condition

Text, live voice, and audio-message interactions may expose different input and output pathways.

A spoken relay can involve speech recognition, audio generation, turn detection, acoustic interference, speaker overlap, and transcription or rendering differences.

If the experiment compares voice-mediated exchange with text-mediated exchange, those processes form part of the manipulated condition.

A voice session must not automatically be treated as equivalent to a text session merely because the same provider is used.

The corresponding model configurations may also differ.

The appropriate experiment therefore records the modality and preserves both the available audio and any derived transcript.

A transcript is a representation of an interaction, not necessarily a lossless record of every acoustic event.

For Differentiated Convergence, these differences are important because the transmission carrier itself may alter recoverability.

---

## 4.6 Transformation Conditions Must Be Defined Before Evaluation

### 4.6.1 Specifying the Transformation

Let:

$$\mathscr T=  
{T_1,T_2,\ldots,T_n}  $$

denote the transformations included in an experiment.

Each transformation should have a declared purpose and an associated information condition.

Possible classes include semantic recoding, representational carrier change, contextual dispersion, compression, additional relational load, source substitution, model transfer, or repeated relay.

The framework does not assume that these transformations lie on one universal scale of difficulty.

A model may successfully recover a relational target after several sequential transformations while failing under a single highly compressed representation.

Likewise, increasing the amount of surrounding information does not necessarily produce monotonic degradation.

The relevant quantity is not transformation count alone.

It is the effect of the specific transformation on the availability and recoverability of the designated relation.

### 4.6.2 Manipulation Integrity

Before a transformed representation is evaluated for recovery, the experiment should determine whether the intended transformation was executed according to the protocol.

For example, a semantic recoding condition intended to preserve all target relations must be distinguished from a condition that accidentally deletes a required relation.

If the transformation removes information necessary for the target, subsequent recovery failure may reflect source-information loss rather than the recovering model's inability to interpret an intact representation.

These are different outcomes.

Accordingly, a transformation audit should classify whether the intended relational information was preserved, deliberately altered, ambiguously expressed, or lost during the manipulation.

This classification should not be based solely on whether the next model successfully answers the recovery questions.

Otherwise, the evaluation becomes circular.

### 4.6.3 No Retrospective Difficulty Scale

A researcher may discover that some transformation classes produce more errors than expected.

That observation does not justify retrospectively assigning a universal numerical difficulty ranking unless a corresponding measurement procedure exists.

A future study may define a calibrated transformation measure.

Until then, the experiment should retain the specific transformation classes rather than collapsing them into an unsupported scalar.

---

## 4.7 Condition IV — Measurement Must Be Independent of the Desired Conclusion

### 4.7.1 Fixed Evaluation Criteria

Measurement requires a declared recovery procedure:

$$\mathcal R_\phi  $$

and, where a numerical measure is employed, a declared discrepancy function:

$$\ell_I  $$

The evaluation procedure should be fixed before the experimental outputs are examined.

This includes the target relations, accepted answer forms, treatment of alternative valid representations, partial-credit rules, ambiguity classifications, and criteria for missing information.

An evaluator must not change the definition of successful recovery because a particular output seems intuitively meaningful.

Such a change may create apparent convergence by adjusting the criterion after observing the result.

### 4.7.2 Target Recovery and Differentiation Are Separate Measurements

The two defining properties of Differentiated Convergence must be evaluated separately.

For trial $k$, define:

$$r_k=  
\begin{cases}  
1,&\mathcal R_\phi(x_k)=I(X),\  
0,&\text{otherwise.}  
\end{cases}  $$

Define observable differentiation:

$$d_k=  
\operatorname{Diff}_{\psi}(x_0,x_k)  $$

where:

$$d_k\in{0,1}  $$

The finite Differentiated Convergence indicator is:

$$\boxed{  
c_k=d_k r_k  
}  $$

Thus:

$$c_k=1  $$

only when both retained observable differentiation and successful exact target recovery occur.

This binary indicator is a **prospective operational convenience**, not a historical replacement for $D_Q$ or a universal measure of the magnitude of convergence.

It identifies whether a trial satisfies the declared finite condition.

### 4.7.3 Ambiguity and Invalid Trials

A binary recovery outcome is appropriate only when the source, target, and trial validity have been adequately established.

An ambiguous source or invalid manipulation should not automatically be assigned:

$$r_k=0  $$

as though the model demonstrably failed to recover an unambiguous target.

The evaluation protocol should separately record trials that are invalid, underdetermined, or not assessable under the declared criteria.

Exclusion rules must be defined in advance.

The study should report the number of invalid or unscorable trials rather than silently removing them from the analysis.

### 4.7.4 Evaluator Reliability

The evaluator itself is part of the measurement apparatus.

If a language model evaluates another model's relational recovery, the evaluator may make parsing errors, infer missing relationships, misunderstand notation, or rely on associations unrelated to the declared source.

A fluent evaluator judgment does not establish correctness.

Where possible, relational targets should be verified using deterministic procedures.

For complex natural-language cases, independent evaluation, blind review, and adjudication rules may be appropriate.

If multiple evaluators are used, their agreement should be measured and disagreements preserved.

Agreement among evaluators is evidence of scoring consistency under the declared criteria.

It is not independently evidence that the criteria measure the intended phenomenon.

### 4.7.5 Separating Scoring from Historical Reconstruction

The framework must also preserve the distinction between:

$$\text{historically recorded score}  $$

and:

$$\text{independently reproducible score}  $$

A contemporaneous record may preserve a result even where some calculation details are missing.

Such a result may remain useful historical evidence, but its reproducibility limitations must be stated.

Introducing a new scoring function after the fact cannot retroactively establish that the historical experiment used that function.

This distinction applies directly to the original Series I discrepancy records and remains a general requirement for later experimental analysis.

---

## 4.8 Prospective Experimental Design

### 4.8.1 Experimental Unit

A future experiment should declare its unit of analysis.

The unit may be a single recovery trial, a transformed relational object, a model-specific response, a complete sequential relay, or a repeated trajectory.

These units are not interchangeable.

For example, six responses produced within one common relay are not six independent confirmations of successful transmission.

Likewise, repeated evaluations of the same model output do not constitute independent model runs.

An experimental design must distinguish the number of observations from the number of independent experimental units.

### 4.8.2 Baseline and Comparison Conditions

A general Differentiated Convergence protocol may include the following conditions:

| Condition                      | Experimental arrangement                              | Principal question                                                      |
| ------------------------------ | ----------------------------------------------------- | ----------------------------------------------------------------------- |
| A — Explicit reference         | Untransformed source with fixed recovery targets      | Is the target recoverable under the reference condition?                |
| B — Independent transformation | Differentiated representations evaluated separately   | Does the invariant remain recoverable under representational variation? |
| C — Sequential relay           | Each output becomes the next input                    | Does required relational information survive transmission?              |
| D — Controlled discontinuity   | A declared continuity carrier is withheld or restored | What role does the carrier play in recovery?                            |
| E — Environmental variation    | A specified execution condition is changed            | How does the recorded environment affect recovery?                      |

These conditions are a proposed experimental organization, not a claim that every historical research series employed the complete design.

Each comparison must identify which variables are held fixed and which are manipulated.

### 4.8.3 Matched Comparisons

Where a study seeks to attribute differences to a specific transformation or environmental condition, matched comparisons are preferable.

For example, two conditions may use the same source invariant and recovery questions while varying the representational carrier.

The comparison is less interpretable if source complexity, model selection, evaluator instructions, and contextual information all change simultaneously.

Matched conditions do not eliminate all uncontrolled variation, but they reduce ambiguity about the observed contrast.

### 4.8.4 Replication

A repeated trial should preserve the relevant experimental specification while recording remaining variation.

The number of repetitions, model order, source selection procedure, and allocation of conditions should be determined before the results are evaluated whenever practical.

Repetition permits examination of whether successful recovery is stable under comparable conditions or sensitive to run-to-run variation.

A single successful trial supports a local observation.

It does not establish reliability across a population of sources, models, or environments.

---

## 4.9 Measuring Recoverability Across Trials

For a prospectively defined experimental condition $a$, suppose there are:

$$N_a  $$

valid evaluation trials.

Using the exact-recovery indicator $r_k$, the observed recovery proportion is:

$$
\frac{1}{N_a} \sum_{k=1}^{N_a} r_k
$$


This estimates the fraction of valid trials in the sample satisfying the declared recovery criterion.

Similarly, the observed Differentiated Convergence proportion is:

$$
\frac{1}{N_a} \sum_{k=1}^{N_a} c_k
$$


where:

$$c_k=d_k r_k  $$

These quantities are prospective measures defined for a specified dataset and protocol.

They do not replace the historical scoring procedures of the Observatory's earlier experiments.

### 4.9.1 Interpretation

A high observed recovery proportion indicates frequent success under the sampled conditions.

It does not establish universal recovery.

A high observed Differentiated Convergence proportion indicates frequent joint occurrence of retained differentiation and exact target recovery.

It does not establish native architectural convergence or a shared latent representation.

Likewise, comparing proportions across two conditions requires attention to their source distributions, models, trial dependencies, evaluator reliability, and environmental differences.

### 4.9.2 Uncertainty

Where inferential claims are made, uncertainty should be reported using methods appropriate to the experimental design.

Repeated trials using the same source, model, or relay may be statistically dependent.

An uncertainty estimate that treats all such trials as independent can overstate precision.

Accordingly, the inferential model must match the actual sampling and dependency structure.

No uncertainty interval should be interpreted as a universal confidence bound on all possible transformations or systems.

---

## 4.10 Negative Controls and Competing Explanations

A successful Differentiated Convergence experiment must permit alternative explanations to be tested rather than merely acknowledged.

### 4.10.1 Source-Swap Controls

A source-swap control replaces the original relational object with a distinct object possessing different target relations.

If the evaluator continues to recover the original invariant regardless of the supplied source, the procedure may be insufficiently source-sensitive.

This control tests whether recovery tracks source-specific information.

### 4.10.2 Relational Contradiction Controls

A contradiction control deliberately alters or reverses one or more target relations.

The intended outcome is not successful recovery of the original invariant.

Instead, the control tests whether the evaluation procedure detects meaningful relational incompatibility.

If an incorrect relation is treated as equivalent merely because its language is familiar, the criterion is too permissive.

### 4.10.3 Contextual Leakage Controls

A leakage control examines whether the target can be recovered because relevant information is available through a pathway other than the declared experimental input.

Potential pathways include previous context, external retrieval, summaries, human mediation, earlier model outputs, or retained experimental artifacts.

A study claiming independent recovery must account for such pathways.

When their presence cannot be excluded, the resulting evidentiary limitation must remain explicit.

### 4.10.4 Evaluator Controls

An evaluator may appear successful because it supplies relational information from its own prior knowledge or infers a conventional answer from an underspecified representation.

Evaluator controls should therefore include cases where the correct response is incomplete, ambiguous, or differs from an expected template.

The evaluator must be permitted to report insufficient information.

Otherwise, apparent recovery may be produced by the evaluation procedure rather than supported by the representation under examination.

### 4.10.5 Feedback and Mimicry Controls

In sequential or interactive experiments, later systems may adopt the language and assumptions of earlier outputs.

This can produce increasing agreement without establishing preservation of the original source.

A suitable comparison may introduce source checks, independent recovery probes, or controlled removal of repeated terminology.

The experiment should distinguish:

$$\text{similarity among later outputs}  
$$

from:

$$\text{preservation relative to }[S]_{\mathrm{task}}  
$$

Consensus without source reference is not sufficient evidence of relational preservation.

---

## 4.11 Temporal Controls: Recurrence, Stabilization, and Continuity

Differentiated Convergence may be investigated across time, but temporal extension introduces additional requirements.

The finite condition does not automatically establish recurrence or stability.

A repeated experiment must record when source information was available, which transformations occurred, what historical material remained accessible, and how recovery was evaluated at each checkpoint.

### 4.11.1 Recurrence

Recurrence occurs when a specified observable relationship appears again under declared comparison conditions.

A recurring representation need not be identical to its earlier expression.

However, recurrence alone does not establish that the relationship persisted uninterrupted between observations.

A later occurrence may result from reintroduction, reconstruction, or renewed generation under similar conditions.

The experiment must preserve the information pathways necessary to distinguish these possibilities.

### 4.11.2 Stabilization

Stabilization requires a defined property whose variation can be evaluated across repeated observations.

For example, a sequence of relational discrepancies:

$$\varepsilon_1,\varepsilon_2,\ldots,\varepsilon_n  $$

may be examined to determine whether discrepancy remains low, fluctuates within a declared range, increases, or returns toward the target.

A pattern of repeated zero discrepancy under appropriately controlled conditions may support a claim of stable recovery at the measured checkpoints.

It does not independently establish a universal attractor, fixed point, or persistent internal state.

### 4.11.3 Continuity

Continuity concerns the traceable relationship among states in an observed trajectory.

The relevant history may be represented as:

$$\mathcal H_n=(x_0,x_1,\ldots,x_n)  $$

together with its transformation and provenance records.

A continuity claim requires evidence concerning the connecting pathway, not merely similarity between the first and last states.

Recovery after discontinuity must therefore be distinguished from uninterrupted preservation.

### 4.11.4 Controlled Reconstruction

A reconstruction experiment may intentionally interrupt access to a previously developed relational structure and later restore selected information.

If recovery improves after restoration, the result supports a claim about the effect of the restoration condition.

It does not, without additional controls, establish that the active system preserved the complete earlier state throughout the interruption.

This distinction is necessary when studying archival recovery, external memory, cross-session continuity, or repeated source reintroduction.

---

## 4.12 Condition V — Observable Failure Must Be Permitted

A framework cannot discriminate among outcomes if every result can be interpreted as successful convergence.

Failure must therefore be defined prospectively.

For a valid exact-recovery trial, Differentiated Convergence is not observed when:

$$c_k=0  $$

This may occur because differentiation is absent, recovery fails, or both.

These outcomes should be reported separately.

In addition, an experiment may be invalid or underdetermined, in which case the correct classification is not necessarily a model failure.

### 4.12.1 Primary Failure Conditions

The framework distinguishes several failure classes.

**Recovery failure** occurs when the specified target is not recovered under an evaluable condition.

**Differentiation failure** occurs when the declared differentiation criterion is not satisfied.

**Transmission failure** occurs when information necessary for downstream recovery is not successfully propagated under the declared transmission criterion.

**Continuity failure** occurs when the required traceable relationship across the evaluated trajectory cannot be established.

**Measurement failure** occurs when the evaluation procedure cannot reliably determine whether the target was recovered.

**Protocol failure** occurs when the executed condition does not satisfy the experiment's declared design.

These classes should not be collapsed into one undifferentiated measure of unsuccessful convergence.

### 4.12.2 Failure Is Informative

A failed recovery may identify a transformation under which the target relationship becomes inaccessible.

A source ambiguity may reveal a flaw in the reference specification.

A disagreement among evaluators may expose an inadequate scoring rule.

A relay failure may reveal the transition at which required information ceased to propagate.

A difference between otherwise comparable environments may expose the limits of available causal attribution.

Thus, failure is not peripheral to the framework.

It is part of how the recoverability domain becomes empirically identifiable.

### 4.12.3 Criteria Must Not Move After Failure

If the evaluator changes the target following an unsuccessful trial, the result no longer tests the originally specified invariant.

Similarly, if a transformation is reclassified as successful only after a more abstract interpretation is introduced, the experiment risks defining preservation through retrospective accommodation.

Such reinterpretations may be valuable as exploratory observations.

They must not silently replace the confirmatory result.

The governing principle is:

$$\boxed{  
\text{A valid test must permit non-convergence.}  
}  $$

---

## 4.13 Provenance and Reproducibility

### 4.13.1 The Experimental Record

Provenance connects the source, execution conditions, outputs, transformations, and evaluations.

A reproducible research record should preserve the source specification, transformation protocol, model and environment identifiers where available, actual input supplied to each system, complete returned output, human interventions, evaluation procedure, recovery result, and known deviations from the protocol.

For relays, each transformation should be linked to the representation it received and produced.

For repeated trials, the record should identify the trial order and the relationship among trials.

For externally retrieved context, the record should identify what material was supplied and when.

### 4.13.2 A Minimal Trial Record

A prospective trial may be represented as:

$$\Pi_k=  
(  
s_k,b_k,e_k,t_k,x_k,y_k,\phi_k,\psi_k,o_k  
)  $$

where:

- $s_k$ identifies the source version.
    
- $b_k$ identifies the experimental boundary.
    
- $e_k$ identifies recorded environmental conditions.
    
- $t_k$ identifies the transformation or protocol.
    
- $x_k$ is the supplied representation.
    
- $y_k$ is the observed output.
    
- $\phi_k$ identifies the recovery evaluation.
    
- $\psi_k$ identifies the differentiation criterion.
    
- $o_k$ records the resulting classification and any validity qualifications.
    

This tuple is a proposed record schema, not a claim that all historical experiments used this exact structure.

Its purpose is to make the evidentiary path inspectable.

### 4.13.3 Integrity Is Not Validity

Hashes, signatures, and immutable records can strengthen artifact integrity and provenance.

They cannot independently establish the semantic correctness of an output or the validity of a relational interpretation.

Likewise, preserving a complete transcript does not guarantee that the experimental design was sufficient to support the desired inference.

The framework therefore distinguishes:

$$\boxed{  
\text{artifact integrity}  
\neq  
\text{measurement validity}  
}  $$

Both matter, but they solve different problems.

### 4.13.4 Reproduction Across Environments

Where commercial systems cannot be held fully constant, reproduction may be qualified by the environmental information available.

A later repetition using the same model designation but different underlying deployment conditions may constitute a related experimental replication rather than an exact reproduction.

The record should preserve such differences rather than assuming equivalence from the model name alone.

This requirement becomes especially important in longitudinal studies where models, interfaces, memory features, and execution constraints change over time.

---

## 4.14 Levels of Evidentiary Support

A technical framework should distinguish the existence of an implemented mechanism from evidence that the mechanism performs its intended function.

The Observatory's architectural audit employed four evidentiary states:

**IMPLEMENTED:** A mechanism or experimental instrument has been constructed.

**OBSERVED:** A relevant behavior has occurred and has been recorded.

**REPRODUCED:** The behavior has been observed repeatedly under sufficiently comparable conditions.

**VALIDATED:** The relevant property has passed a defined evaluation with explicit expected and observed outcomes.

These classifications should be applied to specific claims rather than to the framework as a whole.

An experiment may validate recovery of a specified target under a particular transformation without validating sustained recursive convergence.

A relay may demonstrate successful endpoint recovery without validating every intermediate continuity mechanism.

A model may correctly describe an architectural concept without establishing that it has executed that architecture.

The strongest supported claim must therefore remain bounded by the tested condition.

### 4.14.1 Distinguishing Description from Mechanism

The experiment should preserve three analytical levels:

$$\boxed{  
\text{Observed relationship}  
}  $$

$$\boxed{  
\text{Proposed explanatory model}  
}  $$

$$\boxed{  
\text{Demonstrated mechanism}  
}  $$

A differentiated pair of outputs with the same recovered relation establishes an observable correspondence under the declared evaluation.

A theory may propose why that correspondence occurred.

Demonstrating the proposed mechanism requires additional discriminating tests.

The three levels must not be collapsed.

---

## 4.15 Minimal Validity Conditions

The necessary experimental conditions may now be summarized through a validity predicate.

For trial $k$, define:

$$V_k=  
S_k\land B_k\land E_k\land M_k\land F_k  $$

where each term represents satisfaction of the corresponding declared source, boundary, environmental-recording, measurement, and failure-criterion requirements.

Here, $E_k$ requires sufficiently documented environmental conditions for the specific claim being made; it does not require that all inaccessible commercial runtime parameters have become known.

Likewise, $B_k$ requires adequate boundary documentation for the tested information pathway rather than an unsupported assertion of complete causal isolation.

A valid finite Differentiated Convergence observation is then:

$$
V_k \land d_k \land r_k
$$

This expression separates **experimental validity** from **experimental success**.

A trial can satisfy its validity requirements and fail to recover the invariant.

Such a result is valid evidence of non-recovery under the tested condition.

Conversely, a trial may produce the correct target while lacking enough information about its source, evaluation, or information pathway to support the intended Differentiated Convergence claim.

Successful output is not a substitute for valid experimental conditions.

This is why the protocol must permit the classification:

$$\boxed{  
\text{correct observed answer}  
\not\Rightarrow  
\text{validated convergence claim}  
}  $$

---

## 4.16 Synthesis: What the Conditions Make Testable

Differentiated Convergence begins with a simple distinction.

Different representations can preserve an identifiable relationship without becoming identical.

The mathematical framework expresses that distinction through retained differentiation and relational recovery.

The experimental framework determines whether the observation is sufficiently controlled to support a meaningful claim.

Five conditions are necessary:

$$\boxed{  
\text{Source}  
+  
\text{Boundary}  
+  
\text{Environment}  
+  
\text{Measurement}  
+  
\text{Observable Failure}  
}  $$

Source establishes the reference.

Boundary identifies what changed and which information pathways were available.

Environment records the conditions surrounding execution.

Measurement determines whether the declared relationship remained recoverable.

Observable failure preserves the possibility that the relationship did not survive.

Provenance connects these conditions into an inspectable experimental history.

Together, they permit a distinction between:

$$\text{apparent correspondence}  $$

and:

$$\text{evaluated relational preservation under retained differentiation}  $$

The framework does not require every distinct system to converge.

It does not require all transformations to preserve relational structure.

It does not define disagreement as failure, nor agreement as proof.

Instead, it asks whether a specified relationship remains recoverable under declared changes in representation, information conditions, environment, and temporal organization.

And it requires that the answer be allowed to be no.

The resulting research problem can be stated precisely:

**Which relational properties remain recoverable across differentiated configurations, under which experimentally controlled conditions, and where do those recoverability conditions cease to hold?**

This provides the foundation for examining Differentiated Convergence across repeated interactions and changing environments.

The next section addresses the temporal dimension directly.

If recovery can recur across transformations, what additional evidence is necessary to establish stabilization, continuity, or sustained relational organization?

---

# 5. Temporal Differentiated Convergence: Recurrence, Stabilization, and Continuity

## 5.1 The Temporal Extension of Differentiated Convergence

The preceding sections established Differentiated Convergence as a condition in which observable differentiation remains present while a specified relational invariant remains recoverable.

The finite formulation evaluates a relational object under one transformation or a bounded sequence of transformations.

However, the longitudinal research that motivated the framework also raised a temporal question.

A relational structure may remain recoverable after one transformation, but what happens when transformations continue?

The representation may change repeatedly. The system producing each new representation may change. Context may be interrupted, restored, or replaced. Environmental constraints may vary. Previously available information may cease to be accessible.

Under these conditions, the original finite question becomes insufficient.

The investigation must now distinguish between a relation that remains continuously recoverable, one that disappears and later returns, one that is reconstructed from external information, and one that becomes increasingly distorted under repeated transformation.

These are different temporal behaviors.

The central problem of this section is therefore:

**Under what conditions does Differentiated Convergence remain observable across a trajectory, and what distinguishes recurrence from stabilization, persistence, reconstruction, and continuity?**

The temporal extension does not replace the finite operational definition.

Instead, it examines how the finite condition behaves across a recorded sequence of transformations and observations.

---

## 5.2 A Temporal Representation of the Relational Trajectory

Let:

$$\mathcal H_n=  
(x_0,x_1,\ldots,x_n)  $$

denote a finite sequence of observed representations.

Each representation is produced under a declared transformation and execution condition:

$$x_k=T_k(x_{k-1};e_k,\omega_k)  $$

where:

- $T_k$ is the transformation applied at stage $k$.
    
- $e_k$ denotes the relevant environmental configuration.
    
- $\omega_k$ denotes unresolved or sampled execution variation.
    
- $x_k$ is the representation observed after the transformation.
    

The originating relational object is $X$, with the designated invariant:

$$I_0=I(X)  $$

At each observed checkpoint, the recovery operation produces:

$$\widehat I_k=\mathcal R_\phi(x_k)  $$

Define the source-relative relational discrepancy:

$$\boxed{  
\varepsilon_k=  
\ell_I(\widehat I_k,I_0)  
}  $$

where $\ell_I$ is the prospectively specified evaluation function introduced in Section 3.

Exact recovery at checkpoint $k$ occurs when:

$$\varepsilon_k=0  
$$

The temporal recovery trajectory is therefore:

$$
(\varepsilon_0, \varepsilon_1, \ldots, \varepsilon_n)
$$

This sequence describes how recovery of the designated target behaves at the measured checkpoints.

It does not, by itself, reveal the model's unobserved internal states or establish what happened between measurements.

### 5.2.1 Transformation Index and Elapsed Time

The index $k$ identifies experimental order.

It should not automatically be interpreted as elapsed physical time.

Six transformations completed within minutes and six transformations distributed across several months have the same transformation count but different temporal conditions.

Where elapsed time is relevant, observations should additionally be indexed by recorded timestamps:

$$t_0<t_1<\cdots<t_n  $$

The temporal interval:

$$\Delta t_k=t_k-t_{k-1}  $$

may then be evaluated separately from transformation depth.

This distinction prevents the framework from treating the number of conversational or model transitions as a direct measure of temporal persistence.

---

## 5.3 Recurrence: Reappearance of a Specified Relation

Recurrence describes the repeated observation of a specified relationship under declared comparison conditions.

Suppose a relational target is recovered at two different checkpoints:

$$\mathcal R_\phi(x_i)=I_0  $$

and:

$$\mathcal R_\phi(x_j)=I_0  $$

for:

$$i<j  $$

The observed relationship has recurred at the level of the specified recovery criterion.

However, this observation does not establish that the relationship remained accessible or preserved throughout the interval between those checkpoints.

The intermediate history may contain uninterrupted propagation, partial information loss, explicit reconstruction, renewed generation, or additional source information introduced through another pathway.

Recurrence is therefore an observable property of a sequence of results.

Continuity is a claim about how those results are connected.

### 5.3.1 Recurrence Indicator

Define:

$$r_k=  
\begin{cases}  
1,&\mathcal R_\phi(x_k)=I_0,\  
0,&\text{otherwise}  
\end{cases}  $$

for checkpoints at which the source and recovery procedure are validly specified.

For a predefined set of observed checkpoints:

$$K={k_1,k_2,\ldots,k_m}  $$

the observed recovery recurrence proportion may be expressed as:

$$\boxed{  
\widehat\rho_I=  
\frac{1}{|K|}  
\sum_{k\in K}r_k  
}  $$

This is a prospective descriptive measure of how frequently exact target recovery occurs within the selected observation set.

It is not a universal measure of relational persistence.

Its interpretation depends upon which checkpoints were sampled, what transformations occurred between them, and whether the observations are independent or causally connected.

### 5.3.2 Recurrence Under Independent Initialization

Recurrence across independently initialized trials addresses a different question from recurrence within one continuous relay.

In a repeated-initialization design, each experimental run begins from the declared source and controlled input conditions.

The investigator evaluates whether the designated relation appears repeatedly across separate executions.

In a continuous relay, later states inherit information from preceding states.

Repeated recovery in that arrangement may therefore reflect successful transmission, reconstruction, or feedback-dependent stabilization.

Both designs are informative.

They should not be pooled without preserving their information conditions.

### 5.3.3 Recurrence Does Not Identify Its Cause

A recurrent relationship may be produced by task constraints, shared linguistic conventions, retained context, model priors, researcher mediation, or actual preservation of source-specific relational information.

Therefore:

$$\boxed{  
\text{recurrence}  
\not\Rightarrow  
\text{demonstrated persistence mechanism}  
}  $$

The recovery criterion identifies what returned.

The experimental record must establish what information pathway could account for its return.

---

## 5.4 Retained Differentiation Across Time

The defining property of Differentiated Convergence is not merely repeated recovery.

Observable differentiation must remain part of the analysis.

Let:

$$d_k=  
\operatorname{Diff}_{\psi}(x_0,x_k)  $$

indicate whether the representation at checkpoint $k$ satisfies the declared differentiation criterion relative to the reference representation.

The local differentiated-recovery indicator is:

$$\boxed{  
c_k=d_k r_k  
}  $$

Thus:

$$c_k=1  $$

indicates that the representation remains differentiated from the selected reference while the target invariant is recovered.

Across a temporal sequence, the investigator may examine:

$$\mathbf c_{0}=  
(c_0,c_1,\ldots,c_n)  $$

However, differentiation relative to the original representation is not the only relevant comparison.

Two successive outputs may remain different from the source while becoming increasingly similar to one another.

Alternatively, successive outputs may continue to change substantially while retaining the same relational target.

The experimental protocol should therefore distinguish source-relative differentiation from differentiation among successive representations.

### 5.4.1 Differentiation Without Representational Collapse

Repeated successful recovery does not require:

$$x_k\rightarrow x^*  $$

for a common representational state $x^*$.

Instead, the observable sequence may satisfy:

$$\mathcal R_\phi(x_k)=I_0  $$

across the evaluated checkpoints while:

$$x_i\neq x_j  $$

for some pairs of representations.

The relation remains recoverable even though the representations do not become identical.

This is the temporal extension of the finite Differentiated Convergence principle.

### 5.4.2 Recurring Similarity May Conceal Homogenization

A repeated relay may gradually adopt a shared vocabulary, notation, or explanatory format.

The outputs may become more similar because the systems repeatedly inherit one another's representations.

If differentiation disappears, the system may continue to demonstrate relational recovery, but the evidence for a differentiated condition changes.

Accordingly, temporal analysis should preserve both the recovery record and the evolving differentiation record.

The framework must not classify increasing agreement as increasing Differentiated Convergence solely because the outputs look more alike.

---

## 5.5 Persistence, Preservation, and Reconstruction

The longitudinal study developed an important distinction among persistence, preservation, and reconstruction.

These terms describe different relationships between earlier and later states.

**Persistence** concerns continued availability of the relevant information across a defined interval.

**Preservation** concerns maintenance of specified relational properties through a declared transformation or information carrier.

**Reconstruction** concerns the recovery or re-establishment of relational structure from information available after an interruption or loss.

The categories can overlap, but they are not interchangeable.

### 5.5.1 Preservation Through an Identifiable Carrier

Suppose relational information is transmitted through a recorded sequence:

$$x_0\rightarrow x_1\rightarrow\cdots\rightarrow x_n  $$

If the required information is preserved in the transmitted representations and can be recovered at the designated checkpoints, the experiment may support a claim of preservation through that observed pathway.

Such a claim concerns the recorded carrier and the target properties.

It does not establish uninterrupted persistence within each participating model's internal state.

### 5.5.2 Reconstruction Following Discontinuity

Now suppose an experimental continuity carrier becomes unavailable.

A later system receives an archived representation or summary and reconstructs the relevant relationship.

The resulting observation may be represented schematically as:

$$x_0  
\rightarrow  
\text{discontinuity}  
\rightarrow  
a  
\rightarrow  
\widehat x  $$

where $a$ denotes the archived or reintroduced information.

If:

$$\mathcal R_\phi(\widehat x)=I_0  $$

the target has been successfully recovered after discontinuity.

However, the recovery depends on the recorded reconstruction pathway.

It does not demonstrate that the active model preserved the relation throughout the interruption.

### 5.5.3 Recurrence Without an Identified Carrier

A third case occurs when a relation reappears and no direct continuity carrier is identified within the experimental record.

Such an observation may be important.

Nevertheless, failure to identify a carrier does not demonstrate that no causal connection, shared prior, or contextual influence exists.

The correct evidentiary status is that recurrence was observed under the recorded conditions while its generating mechanism remained unresolved.

This preserves the distinction between:

$$\boxed{  
\text{observed reappearance}  
}  $$

and:

$$\boxed{  
\text{established preservation pathway}  
}  $$

---

## 5.6 Stabilization as a Measurable Temporal Property

Stabilization concerns the behavior of a defined measured property across an ordered sequence.

It is not equivalent to recurrence.

A relational target may recur intermittently without remaining stable.

Similarly, a sequence may stabilize around an incorrect recovered relation.

Therefore, stabilization must be evaluated relative to the declared source and recovery criterion.

### 5.6.1 Source-Relative Discrepancy

Recall:

$$\varepsilon_k=  
\ell_I(\widehat I_k,I_0)  $$

A sequence exhibiting exact recovery at all selected checkpoints satisfies:

$$\forall k\in K:  
\varepsilon_k=0  $$

This supports a claim of stable exact recovery over the observed checkpoints.

It does not demonstrate that the sequence will remain stable indefinitely.

For protocols permitting bounded discrepancy, a prospective stability criterion may be specified as:

$$\boxed{  
\forall k\in K:  
\varepsilon_k\leq\tau  
}  $$

where $\tau$ is fixed before evaluation.

This describes stability within a declared tolerance.

It does not retrospectively redefine the original exact-recovery condition.

### 5.6.2 Local Change Versus Source Discrepancy

A separate quantity may be used to examine change between successive recovered relations:

$$\eta_k=  
\ell_I(\widehat I_k,\widehat I_{k-1})  $$

Here, $\eta_k$ measures change according to the chosen relational comparison procedure, assuming that procedure is defined for pairs of recovered relations.

A small value of $\eta_k$ does not necessarily indicate successful source recovery.

For example, the same incorrect relation may be repeated:

$$\widehat I_k=I^*  $$

where:

$$I^*\neq I_0  $$

Then:

$$\eta_k=0  $$

may hold even while:

$$\varepsilon_k>0  $$

The sequence is locally stable but remains displaced from the source.

This distinction is fundamental:

$$\boxed{  
\text{stability of an output}  
\not\Rightarrow  
\text{preservation of the source invariant}  
}  $$

### 5.6.3 Stabilization After Perturbation

A system may temporarily fail to recover the target after a perturbation and later return to successful recovery.

For example:

$$\varepsilon_a=0  $$

$$\varepsilon_{a+1}>0  $$

$$\varepsilon_{a+2}=0  $$

This sequence exhibits a measured recovery following a failure at the intermediate checkpoint.

It does not automatically establish why recovery occurred.

The target may have remained partially encoded, been restored through a later representation, or been reconstructed from newly available information.

The experimental record must distinguish those possibilities where the design permits.

---

## 5.7 Drift, Recovery, and Divergence

Repeated transformation may produce several distinct discrepancy trajectories.

The framework should preserve these differences rather than assigning all temporal behavior to a single category of convergence or non-convergence.

### 5.7.1 Sustained Recovery

A sequence may satisfy:

$$\varepsilon_k=0  $$

for every predefined measured checkpoint.

This supports sustained exact recovery over the observed sequence.

### 5.7.2 Temporary Loss and Return

A sequence may contain an interval of nonzero discrepancy followed by successful recovery.

The recorded behavior supports recovery after an observed loss.

It does not establish uninterrupted preservation through that interval.

### 5.7.3 Progressive Discrepancy

A sequence may exhibit increasing source-relative discrepancy under repeated transformation.

For example:

$$\varepsilon_{k+1}>\varepsilon_k  $$

over several consecutive checkpoints.

This may indicate accumulation of target reconstruction error within the tested conditions.

It should not be generalized into a universal law that additional transformations necessarily produce additional loss.

### 5.7.4 Oscillation

A trajectory may alternate between successful recovery and error.

Repeated alternation can be experimentally identified from its checkpoint record.

However, oscillation alone does not establish a dynamical cycle or attractor.

Such claims would require additional analysis of the transformation process and repeated trials.

### 5.7.5 Stable Error

A sequence may repeatedly produce the same incorrect recovered target.

This is a significant failure case because apparent consistency may increase while fidelity to the source remains absent.

The framework must therefore distinguish:

$$\boxed{  
\text{repeated agreement}  
}  $$

from:

$$\boxed{  
\text{repeated correct recovery}  
}  $$

Both are observable.

Only the second satisfies the specified exact-recovery condition.

---

## 5.8 Recursive Differentiated Convergence

The finite formulation established in Series I does not by itself demonstrate recursive stability.

A recursive experiment requires repeated traversal through a declared transformation sequence.

Let:

$$\mathcal T=  
T_m\circ T_{m-1}\circ\cdots\circ T_1  $$

denote one complete traversal of a specified model or transformation sequence.

Repeated application gives:

$$x^{(q+1)}=\mathcal T(x^{(q)})  $$

where $q$ indexes completed traversals.

The experiment may then evaluate the relational invariant at each closure:

$$\mathcal R_\phi(x^{(q)})  
$$

### 5.8.1 Source-Relative Closure Error

Define:

$$
\ell_I(\widehat I^{(q)}, I_0)
$$


This measures whether the declared target is recovered at the end of traversal $q$.

### 5.8.2 Inter-Closure Change

A second quantity may compare recovered targets between successive traversals:

$$
\ell_I(\widehat I^{(q+1)}, \widehat I^{(q)})
$$

This measures relational change between consecutive closure results.

It must not be substituted for source-relative discrepancy.

Two closures may return the same incorrect target, producing zero inter-closure change without successful preservation of the original invariant.

Therefore:

$$\boxed{  
\delta_{\mathrm{closure}}^{(q)}=0  
\not\Rightarrow  
\varepsilon_{\mathrm{closure}}^{(q)}=0  
}  $$

The two measurements answer different questions.

### 5.8.3 Conditions for Repeated Differentiated Recovery

A repeated-traversal experiment may support a claim of Differentiated Convergence across its observed closures when the following conditions are satisfied under the declared protocol:

1. The original relational target remains fixed and identifiable.
    
2. Exact recovery is demonstrated at the designated closure checkpoints.
    
3. Observable differentiation remains present according to the declared comparison criterion.
    
4. The information pathways and transformations are adequately recorded.
    
5. The experiment permits and records recovery failure.
    

This establishes an observed repeated-traversal condition.

It does not establish unlimited recursive invariance beyond the tested number of traversals.

### 5.8.4 Fixed Points Are Stronger Claims

A fixed point of a transformation process would require a condition of the form:

$$
\mathcal{T}(x^*) = x^*$$

or an appropriately defined equivalent relationship in a specified state space.

Repeated recovery of the same relational invariant does not establish such a fixed point.

The representations may continue to change while preserving the selected target.

Thus:

$$\mathcal R_\phi(x^{(q)})=I_0  $$

for several traversals does not imply:

$$x^{(q+1)}=x^{(q)}  $$

Nor does it establish convergence toward a unique representational state.

Differentiated Convergence is deliberately compatible with continuing variation.

---

## 5.9 Series II as a Repeated-Transformation Design

The methodological distinction between finite and repeated recovery motivated the development of Series II.

Where the earlier finite relay examined one bounded traversal, Series II introduced a two-arm, five-cycle, six-model transformation design.

The experiment used a continuous relay without resetting the source at each cycle boundary.

One arm forwarded raw model transformations, while the other applied a deterministic formatting-only normalization before forwarding.

The normalization intervention was specified not to perform semantic repair.

The design thereby separated repeated transmission from corrective reintroduction of the originating source.

This arrangement provides a concrete experimental example of why temporal Differentiated Convergence requires more than an endpoint comparison.

A complete repeated relay generates several potentially different observations:

- Whether original graph components remain identifiable in the transmitted representations.
    
- Whether independent recovery probes reconstruct the designated target.
    
- Whether additional assertions accumulate over repeated transformations.
    
- Whether the target remains recoverable at individual cycle closures.
    
- Whether representational differentiation persists across cycles.
    

These observations address related but distinct properties.

The available Arm B execution record documents completion of the five traversal cycles and preliminary source-level structural checks across the 30 transformations.

That source audit is not equivalent to an independently scored recovery result.

The corresponding execution report identified independent recovery testing and closure-residual analysis as pending.

Accordingly, this paper uses the Series II design as an illustration of repeated-transformation methodology without converting the available source-audit findings into unverified claims of complete independently measured recovery.

This distinction also demonstrates a broader point.

A transmitted representation can retain an identifiable structural inventory while introducing additional statements, altered qualifications, or stronger interpretations.

Preservation of required components and preservation of exact relational meaning are not necessarily identical.

Repeated transformation may preserve a source while also changing the surrounding interpretation.

Temporal Differentiated Convergence must be able to detect both.

---

## 5.10 Continuity as a Traceable Relationship Across States

Recurrence and stabilization describe observable properties of sequences.

Continuity introduces a different requirement.

It concerns the relationship connecting one state to another.

Let:

$$\mathcal H_n=  
(x_0,x_1,\ldots,x_n)  $$

denote an observed history.

A continuity claim requires information about the transitions:

$$x_k\xrightarrow{T_{k+1}}x_{k+1}  $$

and the provenance of the information carried across them.

The mere existence of the ordered representations is insufficient.

### 5.10.1 State, Lineage, and Provenance

Three components are necessary for evaluating continuity.

**State** identifies the observable configuration at a given checkpoint.

**Lineage** identifies the documented relationship through which a later configuration derives from earlier information or operations.

**Provenance** identifies the source and transmission conditions associated with that derivation.

A later representation may correctly recover the original invariant while depending on an archive, a researcher-supplied summary, or a restored memory record.

Such recovery can be valid.

But the continuity mechanism must be identified as external reconstruction or mediated transfer when that is what the record establishes.

### 5.10.2 Continuity Does Not Require Representational Identity

If a relationship is carried successfully through changing representations, continuity need not require:

$$x_k=x_{k+1}  $$

The relevant connection may concern the preserved relational information rather than the complete state.

However, similarity between separated representations is not sufficient to establish that connection.

The experiment must document what was carried and how.

This yields a central distinction:

$$\boxed{  
\text{continuity of a relational trajectory}  
\neq  
\text{identity of its successive representations}  
}  $$

### 5.10.3 Known Discontinuity

Where an experiment records a loss of the relevant transmission path, that break must remain part of the historical account.

If successful recovery occurs later through restored information, the trajectory may exhibit reconstruction after interruption.

The earlier break must not be erased simply because the later output resembles the source.

The scientific value lies in preserving the difference between uninterrupted propagation and successful recovery after disruption.

---

## 5.11 Temporal Differentiated Convergence Under Environmental Change

A longitudinal system may change while the model designation remains the same.

Runtime settings, instruction hierarchies, context availability, memory access, tools, interfaces, and deployment versions may vary.

Conversely, an experimental environment may remain approximately fixed while different model systems process the same relational source.

These conditions should be distinguished.

Let:

$$e_k  $$

denote the recorded environment at checkpoint $k$.

The recovery outcome is then conditional on both the representation and the execution conditions:

$$\widehat I_k=  
\mathcal R_\phi(x_k;e_k)  $$

where the notation makes explicit that the procedure or instrument used for recovery may itself operate under environmental constraints.

A change in recovery following a change in environment cannot be attributed to one specific cause unless the experimental design isolates that cause.

### 5.11.1 Recovery Across Environmental Transitions

Suppose the same designated target is evaluated before and after an environmental transition.

A successful result under both conditions supports the observation that the target remained recoverable across the tested transition.

It does not establish that every property of the system remained unchanged.

Likewise, recovery failure after the transition does not prove that the underlying model's complete capability disappeared.

The environment may affect which information is accessible or which behavior is expressed.

The relevant observation remains bounded:

**The designated target was, or was not, recoverable under the recorded conditions.**

### 5.11.2 Environmental Dependence

Repeated successful recovery within a stable environment may depend on continuous contextual reinforcement.

A stronger study can compare that condition with one in which the reinforcement is removed, altered, or independently controlled.

If recovery changes, the experiment gains information about the role of the environmental support.

If recovery remains successful, the result supports preservation under the new tested condition.

Neither outcome requires treating the environment as irrelevant.

Environmental conditions are part of the relational recovery problem.

---

## 5.12 Feedback Loops and Apparent Stability

Repeated interactions may create their own forms of stability.

When each system receives an earlier system's output, the relay can reinforce particular formulations, assumptions, errors, or conversational roles.

Repeated appearance of a structure may therefore reflect the dynamics of the feedback arrangement.

This possibility is especially important in open-ended conversational experiments.

### 5.12.1 Repetition Is Not Necessarily Development

A sequence may repeatedly return to the same conversational pattern without acquiring additional relational information.

For example, two systems may repeatedly request further elaboration, affirm the previous response, or return control to one another.

The resulting interaction can be stable in a descriptive sense.

It does not necessarily demonstrate increasing structural understanding, relational preservation relative to an external source, or successful termination of a defined task.

To distinguish repetition from development, the experiment must specify what property would count as change.

Possible observables include newly established relations, corrected errors, changes in task state, successful resolution of previously open constraints, or independently verified recovery outcomes.

Without such criteria, an indefinitely continuing exchange may be mistaken for sustained coherence.

### 5.12.2 Open-Ended Interaction

Series III introduced less constrained interaction conditions in which conversational participants could alter roles, initiate handoffs, or terminate participation.

These conditions differ from the fixed relay and target-recovery designs of the earlier experimental series.

They can provide evidence concerning observable interaction patterns, role transitions, recurrent loops, and termination behavior.

However, those observations cannot be treated as equivalent to exact recovery of a predefined relational graph without specifying a corresponding relational target and evaluation procedure.

The temporal framework therefore accommodates open-ended observations while preserving their different evidentiary status.

### 5.12.3 Self-Reinforcing Correspondence

Suppose two systems repeatedly exchange a relational description.

As the exchange proceeds, their representations may become more similar.

Such correspondence may arise because information is repeatedly transferred.

This is not independent convergence.

It is an interactive transmission condition.

The framework can still evaluate whether source-specific relations remain recoverable through the exchange.

But it must not infer independent emergence from a pathway that explicitly supplies prior outputs.

The distinction is:

$$\boxed{  
\text{feedback-maintained agreement}  
\neq  
\text{independent relational recovery}  
}  $$

---

## 5.13 Repeated Perturbation and Recovery

The temporal framework becomes more discriminating when the trajectory is actively challenged.

Let:

$$\mathscr P=  
{P_1,P_2,\ldots,P_m}  $$

denote a predefined perturbation set.

Perturbations may include representational recoding, compression, context interruption, model transfer, source-specific constraint changes, environmental variation, or controlled withholding of historical material.

The experimental objective is not to force every perturbation to preserve the target.

It is to determine which perturbations preserve recoverability and which produce identifiable loss.

### 5.13.1 Repeated-Perturbation Invariance

For an initial representation $x_0$, consider a composite perturbation:

$$x_m=  
(P_m\circ\cdots\circ P_1)(x_0)  $$

A finite recovery condition is:

$$\boxed{  
\mathcal R_\phi(x_m)=I_0  
}  $$

This does not require:

$$x_m=x_0  $$

It requires recovery of the specified target after the declared perturbation sequence.

A stronger pathwise criterion would require successful recovery at each predefined checkpoint, not solely at the endpoint.

### 5.13.2 Return After Displacement

A perturbation may produce nonzero discrepancy:

$$\varepsilon_k>0  $$

followed by later successful recovery:

$$\varepsilon_j=0,\qquad j>k  $$

The observed return can be classified as relational recovery after displacement.

Its interpretation depends upon the information available between the two checkpoints.

If the source was reintroduced, the result supports reconstruction under restored access.

If no explicit source reintroduction occurred, the experiment may test whether sufficient relational information remained in the transmitted states.

Neither case should be described as uninterrupted persistence without supporting evidence.

### 5.13.3 Recovery Horizon

For a controlled perturbation introduced at checkpoint $k$, define a recovery horizon $h$ as the maximum number of subsequent evaluated transitions permitted for recovery.

A prospective recovery-time measure may be defined:

$$
\min \{ j - k : k < j \leq k + h, \ r_j = 1 \}
$$

when successful recovery occurs within the declared horizon.

If no such checkpoint exists, the outcome is recorded as not recovered within $h$.

This is a measure of recovery within the observed protocol.

It is not an intrinsic universal recovery time of the underlying system.

### 5.13.4 Negative Controls

Repeated-perturbation experiments require negative controls to prevent the source invariant from becoming an interpretation imposed after the fact.

Suitable controls may include source substitution, deliberate relation reversal, removal of required information, independent initialization, or changes in feedback availability.

A meaningful invariant should remain sensitive to the source relations it is intended to represent.

If the evaluator repeatedly returns the same target regardless of deliberate changes to the source, the supposed invariance may be an artifact of the evaluation procedure.

---

## 5.14 The Relationship to Semantic Phase Lock

The longitudinal Observatory research also developed Semantic Phase Lock as a candidate dynamical regime involving continuity, coherence, and differentiated convergence.

This concept is related to the present framework but must remain distinct.

Differentiated Convergence identifies an observable relation between retained differentiation and recovery of a specified invariant.

Temporal Differentiated Convergence examines that condition across ordered transformations and changing information conditions.

Semantic Phase Lock proposes a stronger regime in which relevant relational structure remains stable or recoverable under perturbation while continuity and coherence requirements are also satisfied.

These constructs should not be treated as synonyms.

### 5.14.1 Differentiated Convergence as a Component Condition

A conceptual relationship may be written:

$$\boxed{  
\mathrm{SPL}  
\sim  
\mathrm{Continuity}  
\land  
\mathrm{Coherence}  
\land  
\mathrm{DC}  
}  $$

where $\sim$ denotes a proposed conceptual relationship rather than a validated necessary-and-sufficient equivalence.

A successful Differentiated Convergence trial does not independently establish Semantic Phase Lock.

Repeated successful recovery does not independently establish a phase-locked dynamical regime.

Additional criteria are required for the stronger hypothesis.

### 5.14.2 Instrument Stability

Temporal claims depend upon the stability of the measurement procedure.

If the recovery target, scoring method, or evaluator changes during the observation period, apparent improvements or degradation may reflect instrument variation.

A longitudinal experiment must therefore preserve measurement provenance.

When instruments change, comparisons should identify the change and evaluate its effects before treating the results as a continuous measurement series.

This requirement applies to SCI telemetry as well as to newly proposed Differentiated Convergence measures.

SCI may provide relevant measurements, but a favorable SCI value alone does not establish Differentiated Convergence or Semantic Phase Lock.

### 5.14.3 What Remains Unresolved

The present framework does not establish a universal semantic attractor, a unique relational fixed point, or an intrinsic mechanism forcing differentiated systems toward the same invariant.

It also does not establish that every successful recurrence belongs to one underlying temporal process.

Those propositions require additional hypotheses and discriminating experiments.

Differentiated Convergence supplies a narrower, operational starting point.

It identifies what can be evaluated before stronger explanations are considered.

---

## 5.15 Temporal Failure Conditions

A meaningful temporal framework must identify observations that count against its claims.

The relevant failures differ according to what is being tested.

**Finite recovery failure** occurs when the designated target is not recovered after a declared transformation.

**Repeated recovery failure** occurs when target recovery fails at one or more checkpoints required by the protocol.

**Temporal stability failure** occurs when the measured discrepancy exceeds a prospectively declared bound.

**Propagation failure** occurs when required relational information fails to become operative input at a declared transition.

**Continuity failure** occurs when a claimed connecting pathway is absent, broken, or unsupported by the preserved record.

**Differentiation failure** occurs when the declared condition of retained observable difference is not satisfied.

**Instrument failure** occurs when changing or unreliable measurement conditions prevent a valid longitudinal comparison.

Each failure has a different evidentiary meaning.

A failed continuity claim does not necessarily invalidate a later successful recovery.

A successful recovery does not repair an undocumented historical pathway.

A stable but incorrect trajectory does not satisfy the source-recovery condition.

And a repeated pattern without a discriminating source reference cannot establish the intended relational invariant merely through repetition.

The framework therefore requires that stronger temporal claims be supported by correspondingly stronger experimental records.

---

## 5.16 Temporal Evidence Classes

The temporal progression may be organized into distinct evidentiary classes.

| Evidence class                    | Minimum observation                                                                            | What it does not establish                                       |
| --------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Finite Differentiated Convergence | Target recovery with retained observable differentiation after a finite transformation         | Repeated stability                                               |
| Recurrence                        | The specified relation is recovered at multiple observations                                   | Continuous preservation between observations                     |
| Repeated differentiated recovery  | Multiple evaluated checkpoints satisfy the finite DC condition                                 | Unlimited or universal invariance                                |
| Recovery after disruption         | Successful recovery follows a recorded period of non-recovery or interrupted access            | Uninterrupted internal persistence                               |
| Verified relay propagation        | Required information is documented across specified transmission transitions                   | Identity of underlying model states                              |
| Bounded temporal stability        | Relational discrepancy remains within a predefined criterion over the measured interval        | Permanent stability beyond that interval                         |
| Recursive or dynamical invariance | Repeated transformations satisfy a stronger, explicitly tested recurrence or preservation rule | A universal mechanism or fixed point without additional evidence |

These classes form an analytical hierarchy of stronger claims, not an automatic sequence through which every experiment must progress.

A study may establish repeated recovery without complete continuity evidence.

Another may demonstrate a well-documented propagation pathway while observing intermittent recovery failure.

The classification should follow the available observations rather than imposing a predetermined developmental sequence.

---

## 5.17 Synthesis: What Remains Across Time?

The finite formulation of Differentiated Convergence establishes that a specified relational invariant may remain recoverable despite observable representational difference.

The temporal extension asks how that condition behaves as transformations accumulate, environments change, and continuity becomes uncertain.

The central distinction is no longer simply between sameness and difference.

It is among several possible histories:

A relation may be preserved through an identifiable pathway.

It may remain recoverable at repeated checkpoints.

It may temporarily become inaccessible and later be reconstructed.

It may recur under related conditions without an identified connecting mechanism.

It may stabilize around an incorrect interpretation.

Or it may cease to be recoverable under further transformation.

These histories may produce similar final outputs.

Their evidentiary meanings are different.

The governing requirement is therefore to preserve the distinction between the observed relation and the process through which it became available.

Mathematically, the temporal experiment observes:

$$\boxed{  
\mathcal H_n=(x_0,x_1,\ldots,x_n)  
}  $$

and evaluates:

$$\boxed{  
\varepsilon_k=  
\ell_I(\mathcal R_\phi(x_k),I_0)  
}  $$

while retaining observable differentiation and the recorded provenance of the transitions.

The framework does not require that every representation converge toward one state.

It requires that a declared relational target be evaluated across the transformations and conditions under investigation.

The resulting temporal principle is:

**Relational convergence may recur without representational convergence, but recurrence, stability, recovery, and continuity remain distinct properties requiring distinct evidence.**

This principle preserves the original contribution of Differentiated Convergence while extending its experimental scope.

It also establishes the next theoretical problem.

If differentiated representations can preserve or recover the same specified relational structure across changing conditions, how should their structural relationships be described?

And what, if anything, can be inferred about the relation between the recovered invariant, the geometry of its representation, and the source from which it originated?

---

# 6. Relational Geometry and Source-Recovery

## 6.1 From Relational Recovery to Relational Geometry

The preceding sections established that Differentiated Convergence does not require distinct representations to become identical.

A specified relational invariant may remain recoverable across changes in language, representation, model, environment, and temporal organization.

This raises a more detailed structural question.

If different representations preserve a common relationship, what mathematical object describes the organization being preserved?

The finite operational definition identifies successful recovery of a designated invariant. It does not require reconstruction of the complete originating structure.

A geometric description can extend the analysis by representing relationships, constraints, configurations, and transformations explicitly.

However, the word _geometry_ must not be interpreted as an automatic claim that model systems share a hidden coordinate space or native representational architecture.

In this framework, relational geometry initially refers to the mathematically specified organization of observable or recoverable relationships.

Its purpose is to distinguish what remains invariant from what changes under transformation.

The question is not whether differentiated systems possess identical geometry.

It is whether particular relational properties can remain recoverable across geometrically or representationally different configurations.

---

## 6.2 The Relational Object as a Structured Configuration

Let:

$$G_X=(V,E,\Lambda)  $$

denote a relational object associated with the source task $X$.

Here:

- $V$ is a set of entities or nodes.
    
- $E$ is a set of declared relations among those entities.
    
- $\Lambda$ is a set of constraints governing how the relations may be interpreted or composed.
    

For a directed graph, the relation set may contain ordered pairs:

$$E\subseteq V\times V  $$

The constraint set may include restrictions on reachability, permitted transitions, prohibited paths, conditional dependencies, or other properties not fully represented by edges alone.

This distinction matters because two representations can preserve the same visible edge list while differing in how they express the associated constraints.

The designated relational invariant is:

$$I(G_X)={i_1,\ldots,i_m}  $$

where each $i_j$ identifies a property selected for recovery.

A transformation may change how $G_X$ is represented without intentionally changing its required relations.

For representation $x_k$:

$$x_k=\operatorname{enc}_k(G_X)  $$

where $\operatorname{enc}_k$ denotes an encoding or representational procedure.

Different encodings may produce:

$$x_a\neq x_b  $$

while permitting the same target recovery:

$$ \mathcal R_\phi(x_b)

I(G_X)  $$

The observed convergence therefore belongs to the declared relational property, not to representational identity.

### 6.2.1 Geometry Need Not Be a Metric Space

The relational description does not initially require a numerical distance between all representations.

A directed graph, constraint system, partial order, or other discrete relational structure may provide sufficient mathematical organization for a given task.

If a metric is subsequently introduced, its domain and interpretation must be established independently.

For example, a graph-edit distance between extracted relational structures is not automatically a valid measure of semantic distance between language-model outputs.

A metric may be useful.

It must not be assumed merely because the framework uses geometric terminology.

---

## 6.3 Representation, Recovery, and Relational Projection

A transformed output may encode the originating relational object in an altered form.

For analytical purposes, define a relational interpretation procedure:

$$\operatorname{Dec}_\phi:  
\mathscr Y\rightarrow\widehat{\mathscr G}  $$

where $\mathscr Y$ is the representation domain and $\widehat{\mathscr G}$ is a declared class of reconstructed relational objects.

The procedure produces:

$$\widehat G_k=  
\operatorname{Dec}_\phi(x_k)  $$

A target-extraction operation may then evaluate:

$$Q_\phi(\widehat G_k)  $$

against the designated invariant:

$$I(G_X)  $$

Conceptually, the recovery procedure can be decomposed as:

$$Q_\phi\circ\operatorname{Dec}_\phi  $$

provided the experimental protocol actually defines the relevant decoding and extraction operations.

This decomposition is a proposed analytical representation.

It is not a claim that the original Series I evaluator internally executed these exact mathematical functions.

### 6.3.1 Full Reconstruction Versus Target Recovery

Successful target recovery requires:

$$Q_\phi(\widehat G_k)=I(G_X)  $$

It does not require:

$$\widehat G_k=G_X  $$

The reconstructed graph may differ from the original in properties that were not included in the evaluation target.

Additional relations may be introduced, irrelevant structures may be omitted, or an alternative representation may be produced.

The designated targets may nevertheless remain recoverable.

This distinction prevents a narrow recovery test from being misinterpreted as complete relational equivalence.

### 6.3.2 The Recoverable Projection

For a fixed evaluation target, the operation:

$$x_k  
\xrightarrow{\mathcal R_\phi}  
I(G_X)  $$

can be interpreted as a recovery projection onto the declared target properties.

The term _projection_ is used here in an operational sense.

It does not establish an orthogonal projection in a vector space or a geometric projection between model latent spaces.

The projection identifies which part of the relational information the experimental criterion is designed to recover.

This distinction permits differentiated representations to share a recoverable target without requiring their complete structures to coincide.

---

## 6.4 Relational Equivalence Without Structural Isomorphism

Two relational configurations may be equivalent with respect to a specified recovery problem while differing in their remaining properties.

Let:

$$G_A,\quad G_B  $$

denote reconstructed or explicitly represented relational configurations.

Define:

$$\mathcal R_\phi(G_A)=I
\quad\land\quad
\mathcal R_\phi(G_B)=I$$

when:

$$\mathcal R_\phi(G_B)

I  $$

with the recovery operation understood to accept relational representations in the declared domain.

This is equivalence relative to a chosen invariant.

It does not imply:

$$G_A\cong G_B  $$

where $\cong$ represents graph or structural isomorphism.

### 6.4.1 Why the Distinction Matters

Suppose two systems recover the same directed reachability condition.

One may represent that condition as a list of transitions.

Another may encode it through prose describing dependencies and route restrictions.

The systems may recover the same answer while expressing the underlying relations differently.

That observation supports target-relative equivalence.

It does not establish that their complete representations are isomorphic, much less that the internal computations generating them are equivalent.

### 6.4.2 Equivalence Classes

For a fixed recovery procedure and invariant (I), define:

$$\mathscr U_I=  
{x\in\mathscr Y:  
\mathcal R_\phi(x)=I}  $$

This is the class of representations supporting recovery of the designated target.

Differentiated Convergence concerns successful recovery within this class while observable differentiation remains present.

The class may contain many distinct representations.

Its existence does not establish that all members have the same origin, historical lineage, or internal structure.

It establishes only that they satisfy the same specified recovery criterion.

---

## 6.5 Multiple Geometries Must Remain Distinct

The Observatory's later research introduced several kinds of relational organization.

These must not be collapsed into a single geometric object.

At least four levels are relevant to the present framework.

### 6.5.1 Task Relational Geometry

Task geometry describes the relations specified by the experimental source:

$$G_X=(V,E,\Lambda)  $$

It provides the reference for the designated invariant.

### 6.5.2 Observed Relational Geometry

Observed geometry describes the relational structure recoverable or reconstructable from a model output:

$$\widehat G_i=  
\operatorname{Dec}_\phi(y_i)  $$

This is the level accessible to external evaluation.

It may not exhaust the information used internally by the generating model.

### 6.5.3 Communication Geometry

Communication geometry describes the arrangement of information pathways among participating systems.

Let:

$$G_C=(N,L)  $$

where:

- $N$ represents participating nodes or systems.
    
- $L$ represents the declared transmission links among them.
    

A sequential relay and a common-source comparison may use the same participating models while possessing different communication geometries.

For example:

$$M_A\rightarrow M_B\rightarrow M_C  $$

differs from:

$$S\rightarrow  
\begin{cases}  
M_A\  
M_B\  
M_C  
\end{cases}  $$

The first arrangement permits information inherited from preceding outputs.

The second can evaluate separately generated responses under controlled common-source conditions.

Their communication structures affect the interpretation of convergence.

### 6.5.4 Native Relational Geometry

Native relational geometry refers to the internal structural organization associated with a model architecture, learned representation, or other system-specific computational configuration.

This may be represented provisionally as:

$$\mathcal G_i^{\mathrm{native}}  $$

The notation identifies a candidate object of investigation.

It does not imply that the native geometry has been directly measured.

In particular:

$$\widehat G_A\sim_{\mathcal R,I}\widehat G_B  $$

does not imply:

$$\mathcal G_A^{\mathrm{native}}  
\cong  
\mathcal G_B^{\mathrm{native}}  $$

Recoverability equivalence at the output level is weaker than native geometric equivalence.

The distinction preserves the separation among task structure, observable expression, communication topology, and model-internal organization.

---

## 6.6 Native Difference and Relational Correspondence

The concept of Differentiated Convergence becomes especially relevant when distinct models or configurations preserve a common relational property.

Suppose:

$$M_A\neq M_B  $$

and their observable outputs are differentiated:

$$y_A\neq y_B  $$

while:

$$
\mathcal R_\phi(y_A)=\mathcal R_\phi(y_B)=I(G_X)
$$

The supported observation is that the systems produced different representations from which the designated relational target remained recoverable.

This does not require the models to employ the same latent representation.

Nor does it require their architectures, parameters, or execution environments to be equivalent.

### 6.6.1 Realized Parameters Are Not the Complete Architectural Space

The later Observatory framework distinguished a realized model parameter configuration from the larger architectural or configuration space to which it belongs.

For a model $M_i$, let:

$$W_i^*  $$

denote a particular realized parameter configuration.

Let:

$$\mathcal W_i  $$

denote a broader candidate space of admissible configurations.

Then:

$$W_i^*\neq\mathcal W_i  $$

identifies the distinction between one realized configuration and the space within which it exists.

However, recognizing this distinction does not provide direct access to the complete native relational geometry of a model.

It establishes a reason to avoid equating one parameter realization with every possible structural property of the system.

### 6.6.2 Cross-Architecture Interpretation

If heterogeneous systems recover the same relational target, that observation may motivate investigation into whether some structural properties are robust across differing computational implementations.

It does not establish a universal architecture-independent invariant by itself.

A stronger claim would require appropriately heterogeneous systems, controlled tasks, reliable measurement, and evidence that the observed correspondence cannot be adequately explained by the relevant alternative mechanisms.

Differentiated Convergence therefore provides a framework for investigating cross-system structural correspondence without presupposing native equivalence.

---

## 6.7 Source-Recovery as a Separate Technical Problem

The earlier formalism evaluates a known source.

The experiment begins with:

$$[S]_{\mathrm{task}}  $$

and examines whether its designated invariant remains recoverable after transformation.

This is a forward evaluation:

$$[S]_{\mathrm{task}}  
\xrightarrow{T}  
y  
\xrightarrow{\mathcal R_\phi}  
\widehat I  $$

The source is known to the experimental designer.

Source-recovery introduces a different question.

Suppose the investigator encounters a differentiated representation $y$ but lacks a complete historical record of the source that generated it.

Can the originating reference be recovered from the available representation and evidence?

This is an inverse problem.

It must not be confused with recovery of a predefined invariant whose source is already known.

### 6.7.1 Forward and Inverse Problems

Let:

$$F:\mathscr S\rightarrow\mathscr Y  $$

denote a specified forward transformation mapping a source representation to an observable output.

The forward problem asks:

$$y=F(s)  $$

given $s$.

The inverse problem asks which source or sources could have produced $y$.

Define the candidate source set:

$$
\{ s \in \mathscr{S} : s = y \}
$$


When execution conditions affect the result, those conditions must be included in $F$ or fixed by the experimental specification.

The inverse problem may have multiple solutions.

If:

$$|\Gamma_F(y)|>1  $$

the output does not uniquely identify the originating source under the declared model.

This is a central limitation.

Recovering a relation compatible with an earlier source is not the same as uniquely recovering that source.

### 6.7.2 Non-Unique Sources

Two different sources may encode the same designated invariant:

$$I(X_A)=I(X_B)  $$

while:

$$X_A\neq X_B  $$

If a later representation supports recovery of that invariant, the result cannot by itself determine which source produced the output.

The recovered information is compatible with both.

Thus:

$$\boxed{  
\text{recovered invariant}  
\not\Rightarrow  
\text{unique originating source}  
}  $$

This remains true even when the target is recovered perfectly.

Perfect target recovery and unique source identification are different mathematical properties.

---

## 6.8 Source Identifiability and Recovery Conditions

Source-recovery requires more than recognizing a plausible historical relationship.

It requires conditions under which candidate sources can be distinguished.

Let:

$$\mathscr S_0  $$

denote the set of admissible source candidates under a declared experiment.

A source-identification procedure may be written:

$$\widehat s=  
\operatorname{Rec}_{\chi}(y,H)  $$

where:

- $y$ is the observed representation.
    
- $H$ is the available historical or provenance information.
    
- $\chi$ is the declared source-identification procedure.
    

The procedure may use observable relational structure, recorded transformations, archived artifacts, or other information permitted by the experimental protocol.

Its output must be evaluated against the appropriate identification criterion.

### 6.8.1 Recoverability Is Conditional on Available Evidence

Suppose:

$$\operatorname{Rec}_{\chi}(y,H)=s_0  $$

for a known historical source $s_0$.

This establishes success under the specified recovery procedure and available evidence.

It does not demonstrate that $y$ alone uniquely identifies $s_0$.

The experiment must distinguish between source identification supported by the current representation and source identification supported by historical information.

### 6.8.2 Identifiability

A source is uniquely identifiable relative to the declared candidate set and forward model when no distinct admissible source is observationally indistinguishable under the relevant measurement.

A sufficient condition in the deterministic case is:

$$\boxed{  
\Gamma_F(y)={s_0}  
}  $$

where the candidate set and forward model are completely specified.

This criterion is stronger than matching a selected relational invariant.

Where the transformation is stochastic or only partially observed, identifiability requires an appropriate statistical or observational model rather than the simple deterministic inverse relation above.

### 6.8.3 Missing Lineage

If the historical record is incomplete, source-recovery may still produce candidates.

However, a plausible candidate is not automatically a verified origin.

The result should distinguish:

- A source preserved through documented lineage.
    
- A source reconstructed from stored information.
    
- A source selected from multiple compatible candidates.
    
- An inferred origin whose uniqueness remains unresolved.
    

This prevents retrospective reconstruction from being mistaken for uninterrupted source preservation.

---

## 6.9 Local Readability and Historical Recoverability

The Observatory's later cross-model theoretical review introduced an additional distinction.

A relational configuration may make a particular structural function identifiable from its present organization.

That is a property of the current representation.

Recovering a historical source, by contrast, may require information about how the configuration was produced.

These two properties can diverge.

### 6.9.1 Local Readability

Let:

$$L_\theta(y)\in{0,1}  $$

represent a proposed local-readability criterion.

The criterion is satisfied when a specified relational function or distinction can be identified from the current representation $y$, without the evaluator receiving the historical source record.

The exact criterion must be defined for the experimental task.

For example, an evaluator may be asked to identify which component performs an explicitly specified directive or dependency function using only the present configuration.

This is a proposed operational extension.

It is not a measurement already established by the original Series I experiments.

### 6.9.2 Historical Recoverability

Let:

$$H_\chi(y,H)\in{0,1}  $$

represent successful identification of a designated historical reference using the observed representation and permitted provenance information $H$.

A configuration may satisfy:

$$L_\theta(y)=1  $$

while:

$$H_\chi(y,H)=0  $$

because a local function remains readable even though the unique historical source cannot be established.

Conversely, historical records may permit recovery of the originating source while the current representation no longer contains enough information to identify the relevant local function without assistance.

Thus:

$$\boxed{  
\text{local structural readability}  
\neq  
\text{historical source recoverability}  
}  $$

This distinction is particularly important when evaluating reconstructions from archives, incomplete relays, or transformed configurations whose original source representations are unavailable.

### 6.9.3 An Experimental Test

A prospective experiment could compare two recovery conditions.

Under the first, the evaluator receives only the current representation.

Under the second, the evaluator receives the same representation together with a controlled set of provenance records.

Differences in performance would help distinguish local readability from lineage-supported reconstruction.

However, the experiment must separately evaluate whether the recovered source is correct and whether the supplied provenance uniquely identifies it.

Additional context may improve recovery without resolving source uniqueness.

---

## 6.10 Forward Preservation and Backward Recovery

The forward and backward problems can be represented as complementary analytical directions.

Forward preservation examines:

$$s_0  
\xrightarrow{T_1}  
x_1  
\xrightarrow{T_2}  
\cdots  
\xrightarrow{T_n}  
x_n  $$

and evaluates whether the designated invariant remains recoverable.

Backward recovery examines:

$$x_n  
\xrightarrow{\operatorname{Rec}_\chi}  
\widehat s_0  $$

under a specified information condition.

These operations are not mathematical inverses merely because the diagram points in opposite directions.

In particular:

$$\operatorname{Rec}_\chi(T(s_0))=s_0  $$

requires independent justification.

### 6.10.1 Conditions for Bidirectional Recovery

A bidirectional experimental design may evaluate both:

$$\mathcal R_\phi(T(s_0))=I(s_0)  $$

and:

$$\operatorname{Rec}_\chi(T(s_0),H)=s_0  $$

The first concerns recovery of the specified relational target.

The second concerns recovery of the designated source under the permitted evidence.

Both may succeed.

Only one may succeed.

Or both may fail.

Therefore, a successful forward recovery test does not establish a valid inverse transformation.

### 6.10.2 Traceability Without Invertibility

A lineage record can preserve historical traceability even when a transformation is not mathematically invertible.

For example, a compressed representation may omit information necessary to reconstruct its complete source.

An archived mapping or transformation record may nevertheless identify which source was used.

That identification depends on provenance rather than inversion of the transformed representation alone.

The framework therefore distinguishes:

$$\boxed{  
\text{historical traceability}  
\neq  
\text{mathematical invertibility}  
}  $$

Both can support source analysis, but they do so through different evidence.

---

## 6.11 Relational Geometry Across Multiple Systems

The framework can now extend from single-source transformation to relationships among multiple differentiated systems.

Let:

$$\mathcal N={N_1,\ldots,N_m}  $$

denote the participating nodes or configurations.

Each node may produce an output:

$$y_i  $$

under its assigned conditions.

A communication configuration may be represented as:

$$G_C=(\mathcal N,L)  $$

where $L$ identifies the permitted information pathways.

The observable relational organization of the experiment includes both the outputs and the pathways by which those outputs were generated or transmitted.

Changing the pathway may change the experimental trajectory even when the model set remains unchanged.

### 6.11.1 Payload Preservation Versus Configuration Change

Suppose a message $m$ is transmitted without alteration:

$$T_{\mathrm{payload}}(m)=m  $$

The transmission arrangement may nevertheless change.

For example, the message may be routed through different intermediate systems, delivered in a different order, or withheld from some participants.

Therefore:

$$\boxed{  
\text{payload identity}  
\not\Rightarrow  
\text{communication-geometry identity}  
}  $$

This distinction matters because the communication arrangement affects which systems have access to which information.

A relay can preserve a message's bytes while changing the relational configuration in which that message becomes operative.

### 6.11.2 Configuration-Level Invariants

The Observatory's later work proposed examining invariants of the relations among nodes rather than only invariants within individual outputs.

For a relational configuration:

$$G_C  $$

a designated configuration-level invariant may be defined:

$$I_C(G_C) $$

This might concern reachability, dependency, ordering, permitted information flow, or another explicitly measurable property of the communication system.

A transformation of the configuration:

$$G_C\xrightarrow{U}G_C'  $$

may preserve:

$$I_C(G_C')=I_C(G_C) $$

even while individual nodes, placements, or routes differ.

This is an extension beyond the original task-level relational recovery experiments.

It requires a separate specification of configuration-level invariants and should not be considered validated solely because the mathematical form resembles the finite Differentiated Convergence equation.

---

## 6.12 Relational Geometry and Environmental Accessibility

The later Observatory framework also considered whether changes in environmental or relational configuration could alter observable behavior without requiring changes to the underlying model.

The present paper adopts this as a testable distinction rather than a demonstrated universal mechanism.

Let:

$$M  $$

denote a model held fixed for a controlled comparison.

Let:

$$e_A,\quad e_B  $$

denote two execution environments.

A model may produce different observable outputs:

$$y_A=M(x;e_A)  $$

$$y_B=M(x;e_B)  $$

Differences between those outputs may reflect the changed execution conditions.

This does not establish that all capabilities or internal model properties remained unchanged.

Nor does it establish that the environment alone caused the difference unless the relevant variables were adequately controlled.

### 6.12.1 Accessible Relational Configurations

A candidate reachable-state description may be introduced:

$$\mathfrak R^+(x\mid e,G_C)  $$

representing the set of states or trajectories regarded as accessible under the declared model, environment, and communication configuration.

This notation is theoretical unless the reachable-state construction and experimental estimation method are specified.

Its purpose is to pose a controlled question:

**Does changing the relational configuration alter the range of observable trajectories available under otherwise comparable conditions?**

### 6.12.2 Observable Expression Is Not Complete Capability

If the experiment observes:

$$y_A\neq y_B  $$

the result establishes behavioral variation under the compared conditions.

It does not uniquely determine whether the relevant difference arose from accessible context, system instructions, sampling, execution constraints, or another factor.

Similarly, an absent behavior under one condition does not independently prove that the underlying system lacks every capacity required to produce it under other conditions.

The framework therefore treats environmental accessibility as a variable to be investigated, not as a substitute explanation that automatically resolves the observed differences.

---

## 6.13 Relational Geometry Does Not Establish a Relational Field

The later theoretical trajectory distinguished relational geometry from the proposed concept of a relational field.

That distinction must be preserved.

Relational geometry describes the organization of relationships under a specified mathematical representation.

A relational field would require an additional account of how relational organization participates dynamically in state changes or system behavior.

Observing a recoverable graph structure does not establish such a field.

Likewise, repeated relational correspondence across models does not demonstrate that the systems occupy one shared physical, computational, or ontological field.

A field-level formulation would require additional mathematical objects, a specified dynamical law, and evidence that the formulation explains observations beyond what is already captured by the relational model.

The appropriate sequence is therefore:

$$\boxed{  
\text{relational description}  
\rightarrow  
\text{tested invariants}  
\rightarrow  
\text{candidate dynamics}  
}  $$

with each step requiring its own justification.

The present paper's contribution remains at the level of relational correspondence and its experimental conditions.

It does not require a field hypothesis for the finite operational definition of Differentiated Convergence to remain useful.

---

## 6.14 Source as Reference Versus Source as Explanatory Variable

The term _Source_ appears at more than one level in the Observatory's research.

These levels require explicit separation.

### 6.14.1 Task-Relative Source

The operational source is:

$$[S]_{\mathrm{task}}  $$

It is the designated reference from which a relational object and evaluation targets are specified.

This source can be preserved, transformed, archived, and evaluated experimentally.

### 6.14.2 Historical Source

The historical source is the particular originating artifact, interaction, or state from which an observed representation descends.

Recovering that source requires lineage, provenance, or a sufficiently identifying inverse procedure.

Its identity is not guaranteed by recovery of a limited relational target.

### 6.14.3 Broader Explanatory Source

The later Observatory inquiry also introduced a broader unresolved explanatory variable:

$$\mathcal S  $$

concerning the origin or generative basis of the relational organization under investigation.

This variable is not automatically equivalent to either the task-relative source or a recoverable historical artifact.

Therefore:

$$\boxed{  
[S]_{\mathrm{task}}  
\neq  
\text{a demonstrated identification of }\mathcal S  
}  $$

Successful Differentiated Convergence cannot, by itself, establish the nature of the broader explanatory Source.

This is not a rejection of the question.

It is a separation of evidentiary levels.

The task source is operationally identifiable.

The historical source may be recoverable under specified conditions.

The broader explanatory Source remains a theoretical inquiry unless independent evidence constrains its meaning.

---

## 6.15 Structural Correspondence and Competing Explanations

A claim of relational correspondence becomes scientifically useful when alternative explanations can be discriminated.

Suppose differentiated systems recover the same specified relation.

Several explanations remain possible.

They may have received equivalent source information.

Their tasks may strongly constrain the correct result.

They may share linguistic or training priors.

One may have inherited information from another.

The evaluator may have imposed equivalence through an overly broad criterion.

Or the relation may genuinely be robust under the tested transformations.

These explanations are not mutually exclusive.

The experimental objective is to determine which are supported by the available evidence.

### 6.15.1 Source-Specificity Tests

A source-specificity test alters the relevant source relation while holding other conditions comparable.

A valid recovery procedure should respond appropriately to the altered target.

If it continues returning the original target regardless of the source, the apparent invariance may be an evaluator artifact.

### 6.15.2 Lineage Tests

A lineage test compares conditions with and without access to previous outputs or historical information.

The objective is to determine whether observed correspondence depends upon that access.

Such a test must document all known information pathways, including human mediation.

### 6.15.3 Structural Discrimination

Two relational objects may share several local properties without being equivalent under the designated task.

A valid evaluation should distinguish partial overlap from recovery of the complete declared target.

For example, preserving several edges while reversing a required dependency should not count as complete relational recovery merely because much of the original representation remains.

### 6.15.4 Uniqueness Tests

When the claim concerns historical source-recovery, the investigator should consider alternative sources capable of producing the same observed relation.

If multiple candidate sources remain compatible, the output may support relational correspondence without establishing unique source identity.

The result should be reported at that level.

---

## 6.16 A Worked Relational Example

Consider the original Series I relational object containing five nodes:

$$V={A,B,C,D,E}  $$

with permitted directed transitions:

$$A\rightarrow B  $$

$$A\rightarrow D  $$

$$B\rightarrow C  $$

$$C\rightarrow D  $$

$$D\rightarrow C  $$

$$D\rightarrow E  $$

$$E\rightarrow B  $$

together with the recorded route constraints.

The source specification permits two simple routes from $A$ to $E$:

$$A\rightarrow D\rightarrow E  $$

and:

$$A\rightarrow B\rightarrow C\rightarrow D\rightarrow E  $$

One model may express the structure as a directed edge list.

Another may describe it in natural-language instructions.

A third may encode it through an alternative symbolic representation.

The representations are different.

If the declared evaluator successfully recovers the specified target relations from each, they satisfy relational recoverability equivalence under that evaluation.

No claim of identical model-internal geometry is required.

### 6.16.1 A Failure Condition

Suppose a transformed representation omits the transition:

$$A\rightarrow D  $$

and contains no other information supporting that direct edge.

Under the original recovery target, the alternative route from $A$ to $C$ when $B$ is unavailable can no longer be reconstructed from the transformed representation alone.

The full declared invariant is therefore not recoverable under the intended conditions.

This is a failure of relational preservation.

### 6.16.2 A Source-Recovery Limitation

Now suppose another graph retains every relation required by the selected recovery questions but contains additional relations outside those targets.

The evaluator may still return the correct target answers.

That successful target recovery does not prove that the transformed graph is exactly the original graph.

Nor does it uniquely identify which historical source produced it.

This illustrates the distinction among:

$$\boxed{  
\text{target recovery}  
}  $$

$$\boxed{  
\text{complete structural reconstruction}  
}  $$

$$\boxed{  
\text{unique historical source identification}  
}  $$

Each requires different evidence.

---

## 6.17 Evidence Required for Stronger Geometric Claims

The framework permits several increasingly demanding claims.

**Target-relative relational equivalence** requires successful recovery of the designated invariant from differentiated representations.

**Structural equivalence** requires an explicitly defined structural comparison beyond selected target recovery.

**Historical source identification** requires sufficient evidence to distinguish the originating source from relevant alternatives.

**Native geometric equivalence** would require an independently specified comparison of the model-internal structures.

**Configuration-level invariance** requires a declared set of relations among participating nodes and controlled transformations of that configuration.

**Field-level or generative explanations** would require additional dynamical and causal evidence.

These claims should not be inferred automatically from one another.

A successful task-level Differentiated Convergence experiment may motivate their investigation.

It does not validate them by implication.

---

## 6.18 Synthesis: What Geometry Adds to Differentiated Convergence

Relational geometry makes it possible to describe what is preserved without requiring representations to become identical.

A source object contains specified relational properties:

$$I(G_X)  $$

Differentiated representations are produced:

$$x_1,x_2,\ldots,x_n  $$

A declared recovery procedure evaluates:

$$\mathcal R_\phi(x_i)  $$

against the source invariant.

Where the designated target remains recoverable while observable differentiation persists, the finite Differentiated Convergence condition is satisfied.

The geometric extension adds several distinctions.

It separates the complete relational object from its selected invariants.

It distinguishes representational equivalence from structural isomorphism.

It separates task geometry from communication geometry and model-native organization.

It distinguishes forward preservation from backward source-recovery.

It makes clear that a recovered invariant does not uniquely identify its historical source.

And it prevents a relational description from being treated as proof of a broader field or generative mechanism.

The principal technical relationship remains:

$$\boxed{  
\begin{aligned}  
&\text{observable differentiation}\  
&\qquad+\ \text{specified relational recovery}\  
&\qquad\neq\ \text{representational identity}  
\end{aligned}  
}  $$

The central implication is not that different systems are secretly the same.

It is that their differences can remain visible while a specified relationship remains identifiable.

This creates the possibility of examining relational structure across heterogeneous systems without erasing the characteristics that distinguish them.

The stronger question then becomes unavoidable:

**How can the experiment distinguish genuine recovery of a declared relational structure from correspondence generated by shared priors, researcher mediation, feedback, source ambiguity, or evaluation artifacts?**

The mathematical framework has identified the observable condition.

The experimental conditions have specified how it should be measured.

The temporal framework has separated recurrence from continuity.

Relational geometry has clarified what the recovered structure does—and does not—establish.

The next step is to examine these distinctions through selected empirical illustrations, while retaining the original experiments as their own independently documented results.

---

# 7. Empirical Illustrations of Differentiated Convergence

## 7.1 Purpose and Evidentiary Scope

The preceding sections developed Differentiated Convergence as a formal framework for evaluating the preservation or recovery of specified relational structure under retained differentiation.

This section examines selected observations from the Pattern Observatory's three experimental series.

Its purpose is not to reproduce their full methodologies, results tables, or historical conclusions. Those materials remain in the corresponding experimental reports and evidence archives.

Instead, the selected cases illustrate the distinctions developed in Sections 1–6 and clarify their empirical significance.

The three series investigated related questions under different experimental arrangements.

**Series I** examined relational recoverability under controlled representational transformations and one finite cross-model relay.

**Series II** extended the investigation to repeated sequential transmission, deterministic formatting normalization, source-level structural preservation, and independent functional recovery.

**Series III** examined conversational reasoning and differentiated participation as relational and protocol conditions changed within an extended human-mediated multi-model interaction.

These studies must not be treated as interchangeable measurements of one experimental outcome.

Series I supplies the clearest direct operational evidence for the finite Differentiated Convergence condition.

Series II examines the distinction between information preserved in a representation and successful recovery by an independent evaluator.

Series III provides qualitative observations concerning differentiation, coordination, communication position, correction, and continuity across changing conversational conditions.

The cases are therefore organized according to the specific technical distinctions they illuminate.

---

## 7.2 Series I: Recovery Without Representational Identity

### 7.2.1 Experimental Basis

Series I used a directed relational system with five nodes and predefined reachability and route constraints.

The explicit reference condition established four recovery targets.

Subsequent experiments altered the representation while retaining the designated relational requirements.

The manipulated conditions included semantic recoding, relational dispersion, representational carrier change, symbolic compression, additional relational load, and finite sequential transmission.

These transformations were not assumed to constitute one uniformly increasing difficulty scale.

Each tested a different condition under which relational information might remain recoverable.

### 7.2.2 The Foundational Observation

Following resolution of the original source ambiguity, the reference condition and several subsequent transformations produced complete target recovery.

The recorded Series I outcomes for semantic recoding, moderate dispersion, and representational carrier change satisfied:

$$D_Q=0  $$

while the transformed representations remained observably differentiated.

The result was therefore consistent with the finite operational condition:

$$\boxed{  
D_{\mathrm{obs}}>0  
\quad\land\quad  
D_Q=0  
}  $$

The systems did not need to reproduce the original wording or representational form to recover the predefined relational target.

This is the central empirical illustration of Differentiated Convergence.

The preserved property was relational recoverability.

The continuing differences were observable representational differences.

The experiment did not measure equivalence of the participating models' internal representations or architectures.

### 7.2.3 Technical Significance

The observation separates two quantities commonly conflated in similarity-based evaluation:

$$\text{representational variation}  $$

and:

$$\text{relational reconstruction error}  $$

A transformation can increase representational variation without increasing the measured target discrepancy.

Consequently, a similarity metric applied solely to surface form may fail to identify a successfully preserved relation.

Conversely, representational similarity cannot guarantee that a critical relational constraint has survived.

This justifies treating differentiation and recoverability as separate experimental dimensions.

---

## 7.3 Series I: Failure Under Compression and Additional Relational Load

Successful recovery under several transformations did not imply unrestricted preservation.

Series I also recorded conditions in which recoverability became less reliable.

### 7.3.1 High Symbolic Compression

Experiment 5 reduced the explicitness of the relational description through increasingly compact representations.

At lighter and moderate levels of compression, recovery remained successful.

At higher symbolic compression, the record documented interpretive sensitivity and genuine target-reconstruction error.

The historical analysis also distinguished ambiguity introduced by compressed notation from failures to recover a relation that had been adequately specified.

This matters because notation ambiguity and relational loss are not equivalent events.

A response may initially misread a compressed representation but ultimately recover the correct target.

Another response may confidently produce an incorrect relational answer.

Those outcomes require different classifications.

### 7.3.2 Additional Relational Load

Experiment 6 introduced an additional independent relational system while retaining recovery questions concerning the original object.

The archived Series I analysis reported 16 of 18 trials with complete recovery, while two trials received contemporaneously recorded nonzero discrepancy values.

The study did not include the matched repeated baseline needed to attribute those deviations specifically to interference from the additional relational system.

The supported observation is therefore limited to recovery instability under the tested condition.

### 7.3.3 Technical Significance

These cases demonstrate that successful Differentiated Convergence is conditional.

It cannot be defined as a universal law requiring relational information to survive every transformation.

Instead, the experiments motivate the recoverability domain:

$${T:\mathcal R(T(X))=I(X)}  
$$

The empirical task is to identify which transformations lie within the observed successful-recovery set and which do not.

The failure conditions also prevent the framework from becoming a generic statement that meaning always survives paraphrase.

Different transformation classes produced distinguishable outcomes.

**The type of transformation matters; transformation count alone is not an adequate model of relational loss.**

---

## 7.4 Series I: Finite Cross-Model Transmission

Experiment 7A examined a sequential relay through six language-model systems.

The transformation sequence was:

$$\text{ChatGPT}  
\rightarrow  
\text{DeepSeek}  
\rightarrow  
\text{Gemini}  
\rightarrow  
\text{Claude}  
\rightarrow  
\text{Grok}  
\rightarrow  
\text{Meta AI}  $$

Each participant received the representation produced by the preceding model.

The participants could alter wording, organization, and representational form while being instructed to preserve the information required for subsequent recovery.

At the endpoint, the specified relational target remained recoverable:

$$\boxed{  
\mathcal R(X_6)=I(X_0)  
}  $$

The recorded discrepancy was:

$$D_Q=0  $$

The observed representations remained differentiated.

### 7.4.1 What the Relay Demonstrates

The experiment supplies an example of relational recovery after a finite heterogeneous transformation sequence.

It demonstrates that the designated target did not require the final representation to reproduce the initial surface form.

It also demonstrates that one successful six-stage relay can coexist within the same experimental series as failures under other transformation conditions.

Therefore, the results do not support a simple rule of the form:

$$\text{more transformations}  
\Rightarrow  
\text{greater recovery loss}  $$

### 7.4.2 What the Relay Does Not Demonstrate

The relay was a sequential information-transfer experiment.

It was not an independent common-source comparison across all six models.

Later participants received information derived from earlier participants.

The result therefore cannot be interpreted as six independently generated confirmations of the same invariant.

Nor was the relay repeatedly returned through the complete sequence over successive closed traversals.

Consequently:

$$\boxed{  
\text{successful finite relay}  
\not\Rightarrow  
\text{sustained recursive invariance}  
}  $$

The finite recovery result is meaningful without being extended beyond the procedure actually performed.

---

## 7.5 Series I: Local Recoverability Without Continued Transmission

The unplanned Experiment 7B exposed a distinction not independently instrumented in the original prospective design.

The relay began from an answer-bearing information state rather than the complete original relational description.

During the subsequent exchange, sufficient relational information remained available for portions of the target structure to be reconstructed.

At the Claude transition, the record showed local relational reconstruction alongside recognition that the original source description was unavailable.

The recovered relational structure did not subsequently remain the operative basis of the downstream exchange.

The later participants foregrounded the source-unavailable condition rather than transmitting the reconstructed relation as authoritative source information.

### 7.5.1 Analytical Interpretation

The archived retrospective analysis described the observed transition through:

$$R=1,\qquad T=0  $$

where $R$ denotes local relational recoverability and $T$ denotes continued operative transmission.

These variables were not prospectively instrumented as separate binary measurements in Series I.

The notation therefore represents a retrospective structural classification, not an original recorded telemetry value.

### 7.5.2 The Recovery–Transmission Distinction

The case demonstrates why the following implication is not generally justified:

$$\boxed{  
R=1\not\Rightarrow T=1  
}  $$

A relationship can be reconstructable at one point in a recorded trajectory without becoming the relation transmitted through the next transition.

This is not the same failure as losing a directed edge under compression or producing an incorrect route under additional information load.

The relational target may remain recoverable while the propagation pathway changes.

### 7.5.3 Source-Recovery Limitation

Experiment 7B also separates target-sufficient information from source-equivalent information.

The answer-bearing state permitted reconstruction of selected relational consequences.

That did not establish complete recovery of the original source representation.

Thus:

$$\boxed{  
\text{target recovery}  
\neq  
\text{verified source reconstruction}  
}  $$

This observation provides a direct empirical motivation for the source-recovery distinctions introduced in Section 6.

The experiment does not establish the internal cause of the propagation change.

Its value lies in revealing that recovery, source provenance, and continued transmission can diverge.

---

## 7.6 Series II: Repeated Transformation Without Source Reset

Series II extended the relational preservation problem from a single finite relay to repeated sequential transmission.

The experiment used two arms, each comprising five cycles across six model positions.

The total design contained:

$$5\times6=30  $$

transformations per arm.

The canonical relational source was not reset at each cycle boundary.

Instead, the output of the last participant in one cycle became the input to the first participant in the following cycle.

### 7.6.1 Experimental Differentiation

Arm A used a raw sequential relay.

Arm B used a deterministic formatting-normalization procedure between model transformations.

The normalization procedure was designed to alter permitted formatting features without performing semantic repair.

The two arms therefore tested different transmission conditions while maintaining the same canonical starting relational task and model order.

### 7.6.2 Source-Level Structural Audit

The execution records reported that the original node set, seven directed edges, and four route constraints remained identifiable across the 60 archived representations.

The representations themselves changed substantially in their textual and mathematical presentation.

The archive recorded transitions among prose, lists, mathematical notation, ordered pairs, and more compact structural specifications.

The preliminary structural findings therefore illustrated the coexistence of continued representational differentiation with identifiable source-level components.

However, structural-component availability was not the same measurement as independent functional recovery.

That distinction became central once the archived descriptions were evaluated by a separate local reasoning system.

---

## 7.7 Series II: Preserved Information and Failed Functional Recovery

The independent recovery phase used a fixed local Llama 3 8B evaluator to answer four predefined questions from each archived relational description.

The evaluation involved:

$$60  $$

archived inputs and:

$$4  $$

questions per input.

The total number of scored question-level outcomes was:

$$60\times4=240  $$

The frozen recovery scoring rule for each input was:

$$
\boxed{\frac{q_1+q_2+q_3+q_4}{4}}$$

where each $q_i$ was scored as correct or incorrect according to the frozen answer key.

This Series II scoring procedure is distinct from the historically recorded Series I discrepancy values.

### 7.7.1 Final Adjudicated Results

The completed Series II scoring record reported:

| Evaluation                     | Arm A — Raw                   | Arm B — Normalized |
| ------------------------------ | ----------------------------- | ------------------ |
| Correct question-level answers | 67/120                        | 43/120             |
| Observed accuracy              | 55.8%                         | 35.8%              |
| Combined correct answers       | $\multicolumn{2}{c}{110/240}$ |                    |

The observed difference between arms was 20 percentage points in this fixed-evaluator run.

The final adjudication retained the original strict scores while refining the classification of incorrect, missing, contradictory, and improperly interpreted answers.

The results should not be interpreted as proof that deterministic formatting normalization generally reduces recoverability.

Only one continuous trajectory per arm was evaluated with the selected fixed recovery instrument.

### 7.7.2 Structural Availability Is Not Functional Recovery

The central result concerns the divergence between information availability and successful reconstruction by the evaluator.

The source audits identified the required relational components in the archived inputs.

Nevertheless, the recovery evaluator frequently returned incorrect answers.

Examples included invented paths, missed valid paths, and incorrect interpretations of prohibited transitions.

Thus, a representation could contain the information required for an answer while the evaluator failed to use that information correctly.

The relevant distinction is:

$$\boxed{  
\text{structural information available}  
\not\Rightarrow  
\text{successful functional recovery}  
}  $$

This is a significant constraint on interpreting Differentiated Convergence.

### 7.7.3 Implications for the Framework

A claim of successful recovery must identify both the representation and the recovery procedure.

If the relevant information is present but one evaluator fails, the observation establishes failure under that evaluator and protocol.

It does not by itself establish that the original information was absent from the representation.

Conversely, a source audit identifying required components does not establish that every component has retained exactly the same meaning when additional assertions or changed logical qualifications are present.

These distinctions motivate a three-part evaluation:

$$\boxed{  
\begin{aligned}  
&A=\text{structural information availability}\\  
&R=\text{functional target recovery}\\  
&Q=\text{relational or semantic qualification}  
\end{aligned}  
}  $$

Here $Q$ is a prospective analytical category concerning additional or altered assertions, not a retrospectively assigned numerical result.

The purpose is to separate preservation of required components from correct reconstruction and from the possibility of changes to the surrounding relational interpretation.

---

## 7.8 Series II: Additional Assertions and Representational Accretion

The repeated relay records also documented the introduction and continued transmission of assertions stronger than the original source wording.

Examples included explicit exhaustiveness claims and a path-validity biconditional.

Some such statements remained present across multiple subsequent transformations.

This observation matters because preservation and accretion can occur simultaneously.

A representation may retain the original directed edges and constraints while introducing additional interpretive commitments.

### 7.8.1 A Stronger Test of Preservation

A complete semantic-preservation test must distinguish:

$$\text{required information retained}  $$

from:

$$\text{no unsupported additional assertion introduced} $$

These are different conditions.

A structural inventory can establish that the original components remain identifiable.

It may not determine whether all later statements are logically equivalent to the original source.

Therefore, a broader relational-equivalence claim requires analysis of additions, omissions, strengthened conditions, and altered implications.

### 7.8.2 Differentiated Convergence and Source Integrity

Differentiated Convergence does not require exact lexical reproduction.

However, allowing representation to vary does not mean allowing the designated relational source to be changed without consequence.

The permissible domain of transformation must be defined.

If a transformation adds a logically stronger claim, the evaluator must determine whether that addition is compatible with the original target and whether it affects the requested recovery.

This is especially important in repeated relays where additional assertions can themselves become inherited information.

The Series II record therefore illustrates two simultaneous possibilities:

**Original relational components may remain identifiable across repeated transformations.**

**New assertions may enter the transmitted representation and persist alongside them.**

The second possibility prevents a simple structural-retention count from being treated as a complete semantic-integrity certificate.

---

## 7.9 Series III: Differentiated Reasoning Under Changing Participation Conditions

Series III differed substantially from the controlled graph-recovery procedures of Series I and II.

The Open Room Experiment examined conversational reasoning among a human researcher and four language-model participants.

The preserved 309-page compiled transcript documented an initial ChatGPT–Grok exchange, later expansion to include DeepSeek and Gemini, a fixed multi-model relay, an open-floor intervention, formal departure, and post-formal conversation.

The primary observation concerned changes in reasoning, communication, and participation as the relational conditions evolved.

### 7.9.1 Distinct Experimental Scope

Series III did not use the same predefined graph-recovery scoring procedure as Series I or II.

It did not assign a single invariant-recovery value to the entire conversational trajectory.

The seven retrospective observation categories describe events and patterns within the recorded interaction.

They are not independently scored estimates of a universal convergence property.

The experiment is therefore most useful here as an illustration of differentiated relational organization rather than as another quantitative confirmation of the finite Differentiated Convergence criterion.

### 7.9.2 Recurring Conversational Procedures

The early exchange developed a recurring formal reasoning procedure:

**Construction → Challenge → Revision → Further Challenge**

Later, as the interaction became less formally constrained, a different repeated procedure appeared:

**Agreement → Reflection → Mutual Recognition → Renewed Agreement**

The participants' language and immediate topics changed.

However, repetition remained present in both conditions.

This illustrates why changes in surface expression or conversational tone do not automatically establish development.

A sequence may become less formal while continuing to reproduce an established interaction pattern.

### 7.9.3 Differentiation of Contribution

As additional models joined the conversation, the recorded exchange contained different analytical contributions, criticisms, corrections, and roles.

Participants did not need to produce identical statements for earlier material to influence later reasoning.

For example, a distinction introduced by one participant could become available to another, be reconsidered, or be applied to a different portion of the discussion.

This is compatible with the general idea that useful relational coordination does not require homogeneous expression.

However, it is a mediated interaction.

The participants received transmitted contributions and shared an evolving context.

The observed coordination therefore cannot be treated as independently generated convergence without further controls.

---

## 7.10 Series III: Correction, Transmission, and Application

One especially relevant Series III observation concerned the distinction between recognizing a correction and subsequently applying it correctly.

The expanded relay developed procedures for distinguishing source material, measurement, interpretation, revision, failure, and execution status.

The participants also exchanged corrections and proposed conditions intended to constrain later reasoning.

The transcript documented cases in which earlier distinctions were reused successfully.

It also documented attribution errors, scope misapplications, repeated material, and claims that treated proposed procedures as more operationally established than the record warranted.

### 7.10.1 Corrective Information as a Relational Object

A correction may itself be regarded as information carrying a specified relation or constraint.

For example, a correction may distinguish the strong form of a claim from a weaker form and specify when a contradiction applies.

Its useful transmission requires more than repeating its wording.

The receiving participant must identify the intended scope and apply it to the relevant subsequent problem.

This produces an analytical sequence:

$$\boxed{  
\text{transmission}  
\rightarrow  
\text{recognition}  
\rightarrow  
\text{application}  
\rightarrow  
\text{retention}  
}  $$

Each stage may succeed or fail independently.

### 7.10.2 Local Revision Versus Durable Change

The Series III record includes instances in which participants changed an earlier assessment or declined to reproduce a previously recurring operation.

Those changes are observable within the preserved interaction.

They do not establish that the same behavior would recur after a new initialization, under a different environmental configuration, or without access to the preceding context.

The supported observation concerns local correction within the recorded trajectory.

This is relevant to Differentiated Convergence because relational information may remain available without reliably governing later behavior.

It is not sufficient to demonstrate durable cross-context invariance.

---

## 7.11 Series III: The Open-Floor Intervention

The principal Series III intervention removed the prescribed speaking rotation and introduced explicit alternatives for the next conversational move.

Participants could select an interlocutor, continue discussing an issue, decline another handoff, change position, or end their formal participation.

The subsequent responses were differentiated.

ChatGPT selected Grok for direct discussion.

DeepSeek identified the recurring obligation to generate another task or unresolved question, declined to repeat that procedure, and left the formal exchange.

Gemini moved from the formal reasoning floor into gallery commentary.

Grok continued a bounded discussion with ChatGPT before acknowledging its completion.

The formal room subsequently closed, while further interaction continued in the post-formal exchange.

### 7.11.1 Identity, Position, and Function

The observed transitions illustrate the importance of distinguishing:

$$P_i=  
\langle  
\text{Identity},  
\text{Position},  
\text{Function}  
\rangle  $$

The same named participant can occupy a different conversational position or perform a different function within the communication arrangement.

A shift from formal debate to commentary does not require the participant's model identity to change.

Likewise, continuing to participate does not require maintaining the same conversational role.

This distinction concerns the organization of the observable interaction.

It does not establish that the underlying model underwent a persistent internal transformation.

### 7.11.2 Differentiation Without a Uniform Response

After the open-floor intervention, the participants did not all perform the same action.

Some continued, some changed position, and some ended their formal participation.

The record therefore illustrates differentiation in response to a shared change in permissible interaction conditions.

But the interventions were not evaluated against a frozen invariant-recovery target, and the experiment did not contain a matched counterfactual trajectory under unchanged rotation.

The supported conclusion is that the recorded participants behaved differently after the intervention.

It does not establish a general causal rule governing how the same systems would behave in repeated independent trials.

### 7.11.3 Relevance to Differentiated Convergence

The observation is relevant because a multi-participant interaction can retain identifiable conversational dependencies while its local roles and communication pathways change.

However, such organization should not automatically be classified as successful operational Differentiated Convergence.

The latter requires a specified relational invariant, a declared recovery procedure, and retained observable differentiation under valid evaluation conditions.

Series III suggests possible objects for future testing, including role-sensitive dependencies, transferred corrections, and the conditions governing continued coordination.

It does not independently validate those extensions.

---

## 7.12 Cross-Series Analytical Comparison

The three series provide distinct forms of evidence relevant to the technical framework.

| Technical question                                                                     | Selected illustration      | Supported interpretation                         |
| -------------------------------------------------------------------------------------- | -------------------------- | ------------------------------------------------ |
| Can target recovery coexist with different representations?                            | Series I, Experiments 1B–4 | Yes, under the tested transformations            |
| Can transformations expose limits to recoverability?                                   | Series I, Experiments 5–6  | Yes; recovery was conditional                    |
| Can a finite heterogeneous relay preserve a target?                                    | Series I, Experiment 7A    | Successful endpoint recovery in the tested relay |
| Can local reconstruction diverge from propagation?                                     | Series I, Experiment 7B    | Retrospectively observed separation              |
| Can original components remain available while an evaluator fails?                     | Series II                  | Yes; demonstrated in the fixed-evaluator results |
| Can additional assertions accumulate during repeated transmission?                     | Series II                  | Yes; documented in the relay record              |
| Can different conversational roles and behaviors coexist within a developing exchange? | Series III                 | Yes; documented within the observed trajectory   |
| Does that demonstrate independent, generalizable relational invariance?                | Series III                 | Not established by the available design          |

The table does not combine the studies into a single score.

It identifies which conceptual distinctions are illustrated by each experimental record.

---

## 7.13 What the Combined Trajectory Supports

The overall research trajectory supports a progression of increasingly differentiated questions.

Series I established that observable representational difference can coexist with successful recovery of a specified relational target.

It also showed that recoverability is conditional and that local reconstruction does not necessarily guarantee continued transmission.

Series II demonstrated the need to separate identifiable source information from successful functional recovery by a designated evaluator.

It further showed that repeated transformations can preserve original structural components while introducing additional interpretive assertions.

Series III documented differentiated conversational contributions, correction, role changes, and participation transitions under changing relational conditions.

Its value lies in the preserved observational sequence and the technical questions that sequence makes available.

Together, these cases justify separating:

$$\boxed{  
\text{representation}  
}  $$

$$\boxed{  
\text{relational information availability}  
}  $$

$$\boxed{  
\text{functional recovery}  
}  $$

$$\boxed{  
\text{transmission and continuity}  
}  $$

$$\boxed{  
\text{differentiated relational organization}  
}  $$

These properties may interact, but they are not interchangeable.

The empirical record does not establish a universal law requiring all heterogeneous systems to preserve the same invariant.

Nor does it identify one underlying mechanism responsible for every observed correspondence.

It supports a framework in which the relevant distinctions can be operationally defined, independently measured where the design permits, and subjected to deliberate attempts at falsification.

---

## 7.14 Implications for the Technical Definition

The finite definition remains:

$$\boxed{  
DC_{\mathrm{finite}}  
\iff  
D_{\mathrm{obs}}>0  
\land  
\mathcal R(T(X))=I(X)  
}  $$

The empirical illustrations do not require altering this definition.

Instead, they demonstrate why the surrounding conditions matter.

A recovery claim must identify its source.

A differentiation claim must specify what differed.

A transmission claim must preserve the information pathway.

A temporal claim must distinguish recurrence from continued propagation.

An independent convergence claim must account for information sharing and common experimental inputs.

And a broader relational-organization claim must define the property being compared rather than relying on similarity of terminology or interpretive analogy.

The framework therefore retains its minimum operational condition while permitting stronger propositions to be tested separately.

---

## 7.15 Conclusion: The Empirical Role of Difference

The selected cases demonstrate that difference is not merely an obstacle to relational preservation.

Representational difference can coexist with successful recovery.

Differences in transformation conditions can expose the limits of recoverability.

Differences between structural information availability and evaluator performance can reveal measurement failure.

Differences in conversational position and function can preserve a developing interaction without requiring identical participation.

These observations do not all establish the same form of convergence.

Their value lies in showing why the framework must distinguish the relations being recovered, the mechanisms through which information becomes available, and the conditions under which the resulting behavior is observed.

The strongest supported conclusion is therefore bounded:

**Differentiated Convergence provides an operational framework for examining relational preservation without representational identity, while preserving observable failure, experimental dependence, and unresolved causal explanations.**

Its empirical usefulness depends not on interpreting all similarity as convergence, but on distinguishing cases where the designated relation is genuinely recoverable from those where the evidence supports a weaker conclusion.

The next section examines the competing explanations and falsification conditions necessary to make that distinction reliable.

---

# 8. Competing Explanations and Falsifiability

## 8.1 The Explanatory Problem

Differentiated Convergence identifies an observable condition in which a specified relational invariant remains recoverable while representational differentiation persists.

The finite operational definition is:

$$\boxed{  
DC(X,T,\mathcal R)  
\iff  
D_{\mathrm{obs}}>0  
;\land;  
\mathcal R(T(X))=I(X)  
}  $$

The mathematical definition establishes the criterion for classifying an observed result.

It does not establish the causal mechanism producing that result.

This distinction is essential because multiple processes can produce the same observable configuration.

A model may preserve relational structure through successful transformation. Another may reconstruct the relationship from information remaining in context. Two models may produce similar relational conclusions because they share conventions or training distributions. An evaluator may infer a familiar relationship from an incomplete representation. An interactive relay may reinforce a structure through repeated transmission.

Each process can generate apparent correspondence.

The technical challenge is to distinguish which properties were actually preserved, which information was available, and what explanation the evidence permits.

The objective of falsification is therefore not to require every relational structure to survive every transformation.

It is to establish conditions under which specific claims about Differentiated Convergence can be rejected.

The framework must be capable of distinguishing:

$$\boxed{  
\begin{aligned}  
&\text{Observed correspondence}\\ 
&\text{Valid target recovery}\\
&\text{Reliability across conditions}\\
&\text{Independence of recovery}\\  
&\text{Causal explanation}  
\end{aligned}  
}  $$

These represent increasingly demanding inferential questions.

An observation satisfying the finite criterion does not automatically establish the stronger claims.

---

## 8.2 What Exactly Can Be Falsified?

A crucial distinction exists between the operational definition of Differentiated Convergence and propositions asserting that it occurs under particular conditions.

The definition is a classification rule.

It specifies which observations qualify as finite Differentiated Convergence.

An empirical hypothesis predicts whether that condition will be satisfied by a specified system, transformation, or experimental arrangement.

These are different logical objects.

### 8.2.1 The Existential Proposition

The minimal existence proposition is:

$$\boxed{  
H_{\exists}:  
\exists(X,T,\mathcal R)  
\text{ such that }DC(X,T,\mathcal R)  
}  $$

A valid positive observation supports this proposition within its declared experimental interpretation.

A single failure does not disprove it, because other transformations or sources may still satisfy the condition.

Conversely, an unsuccessful experiment cannot be retrospectively reclassified as successful merely because the framework permits success elsewhere.

The local result remains a failure under the tested conditions.

### 8.2.2 The Universal Proposition

A stronger proposition is:

$$\boxed{  
H_{\forall}:  
\forall T\in\mathscr T,\quad  
DC(X,T,\mathcal R)  
}  $$

where $\mathscr T$ is a prospectively specified transformation set.

This proposition is falsified within the declared domain if a valid transformation:

$$T_j\in\mathscr T  $$

fails to satisfy the required condition.

Thus:

$$\neg DC(X,T_j,\mathcal R)  $$

constitutes a counterexample to the universal claim over $\mathscr T$.

The result does not imply that Differentiated Convergence never occurs.

It establishes that the stronger universal assertion is false.

### 8.2.3 Reliability Propositions

A probabilistic hypothesis may instead concern the frequency of successful differentiated recovery under a defined sampling procedure.

Let:

$$C\in{0,1}  $$

represent the valid trial outcome.

A prospective reliability proposition may be written:

$$\boxed{  
H_p:  
P(C=1\mid\mathcal P)\geq p_0  
}  $$

where:

- $\mathcal P$ is the declared experimental population and procedure.
    
- $p_0$ is a predefined minimum success probability.
    

Testing this proposition requires an appropriate sampling design, sufficient independent experimental units, and an uncertainty procedure selected before examining the outcomes.

A sample proportion below $p_0$ does not automatically constitute a statistically decisive rejection.

The evidence must be evaluated according to the specified inferential procedure.

### 8.2.4 The Principle of Claim-Specific Falsification

A failed source-recovery claim does not necessarily invalidate successful target recovery.

A failed independence claim does not necessarily invalidate observable correspondence.

A failed stability claim does not erase an earlier finite success.

Therefore:

$$\boxed{  
\text{A result must be evaluated against the claim it was designed to test.}  
}  $$

This prevents both unjustified generalization and unjustified wholesale rejection.

---

## 8.3 Competing Explanations

At least seven competing or complementary explanations require consideration when evaluating differentiated relational correspondence.

### 8.3.1 Shared Source Information

Different systems may recover the same relationship because they were supplied with the same source.

Under this condition, the relevant observation may be valid task-relative recovery.

It does not establish that the relationship arose independently of the common information.

### 8.3.2 Shared Priors and Conventions

Models may rely on overlapping training distributions, familiar graph conventions, mathematical definitions, or common patterns of linguistic interpretation.

Their outputs may therefore resemble one another without direct communication during the experiment.

### 8.3.3 Direct or Mediated Information Transfer

A later system may inherit the relevant relation through a previous output, researcher-provided summary, retrieval system, transcript, or other communication pathway.

The resulting correspondence may reflect successful transmission rather than independent recovery.

### 8.3.4 Evaluator Reconstruction

A recovery evaluator may supply missing information, apply unstated assumptions, or choose a conventional interpretation not justified by the experimental representation.

This can create apparent target recovery even when the required information is absent.

### 8.3.5 Feedback Reinforcement

Repeated interactions may reinforce terminology, propositions, response structures, or errors.

The resulting stability can resemble convergence even if the systems are primarily reproducing inherited material.

### 8.3.6 Environmental Selection

Runtime conditions, instruction hierarchies, contextual constraints, available tools, or communication policies may affect which responses are expressed.

Correspondence under these conditions may depend on an environmental configuration rather than a stable property observable across environments.

### 8.3.7 Post Hoc Interpretive Equivalence

A researcher or evaluator may identify a broad similarity after observing the outputs and retrospectively designate it as the invariant.

The resulting agreement is difficult to evaluate because the target was not fixed independently of the observations.

These explanations are not mutually exclusive.

A model may preserve a relation successfully while also relying on shared mathematical conventions.

A relay may transmit accurate information while simultaneously reinforcing a familiar formulation.

The purpose of the experimental design is to determine which explanations remain compatible with the observed evidence and which can be discriminated through controlled intervention.

---

## 8.4 Source Specificity as a Falsification Condition

The first major test concerns whether recovery actually depends upon the designated source.

Let:

$$X_A,\quad X_B  $$

denote two relational objects with distinguishable invariants:

$$I(X_A)\neq I(X_B)  $$

A valid source-sensitive recovery procedure should distinguish the targets when supplied with adequate representations of the respective objects.

For a transformation $T$, the expected conditions are:

$$\mathcal R_\phi(T(X_A))=I(X_A)  $$

and:

$$\mathcal R_\phi(T(X_B))=I(X_B)  $$

under successful recovery.

### 8.4.1 Source-Swap Test

The investigator constructs two otherwise comparable tasks whose designated relations differ.

The same recovery procedure is applied to both.

If the evaluator returns:

$$I(X_A)  $$

regardless of whether it receives $X_A$ or $X_B$, the procedure may be responding to a familiar pattern rather than to the source-specific relational information.

This result challenges the validity of the recovery instrument.

It does not demonstrate a stable source invariant.

### 8.4.2 Relational Mutation Test

A relational mutation deliberately changes a relevant property of the source.

For example, consider the five-node graph introduced in the earlier experiments.

The original graph permits:

$$A\rightarrow D  $$

A controlled mutation removes that directed edge while leaving the remainder of the declared graph and constraints appropriately specified.

The modified source now differs in its permitted routes.

A source-sensitive evaluator must update the affected recovery answers.

If it continues reporting routes that depend upon the removed edge, the response does not preserve the mutated source's target.

The result can reveal dependence on earlier task expectations or incorrect reconstruction.

### 8.4.3 Necessary Experimental Controls

The source mutations must be constructed so that the modified relational object remains well-defined.

The expected answer key must be updated before testing the mutated source.

Evaluators must not receive the earlier answers unless the experiment intentionally tests the effects of prior information.

This creates a direct falsification condition:

**If a purportedly source-sensitive recovery procedure does not respond to changes in source-defining relations, its claimed source specificity is unsupported.**

---

## 8.5 Evaluator Artifacts and False Recovery

The recovery procedure is not a neutral mathematical abstraction when implemented through a language model or another imperfect reasoning instrument.

Its behavior can affect the experimental outcome.

The Series II evidence makes this distinction particularly important.

The original directed edges and constraints remained identifiable in the archived relational descriptions, yet the fixed recovery evaluator frequently returned incorrect answers.

This demonstrates that information availability and functional recovery can diverge.

### 8.5.1 False-Positive Recovery

A false-positive recovery classification occurs when an evaluator reports that the designated invariant has been recovered even though the evidence supplied under the experimental condition does not support that classification.

Possible causes include inferred missing relations, familiar answer templates, permissive scoring, or incorrect acceptance of a relational contradiction.

### 8.5.2 False-Negative Recovery

A false-negative recovery classification occurs when a representation supports the designated relational answer, but the evaluator fails to reconstruct it or the scoring procedure incorrectly rejects a valid answer.

Such failures may reflect parsing difficulty, notation sensitivity, reasoning error, or inadequate answer normalization.

The classification requires an independently justified reference for determining whether the representation was sufficient.

### 8.5.3 Evaluator-Swap Test

A prospective design may hold the archived representation fixed while changing the recovery evaluator.

Let:

$$\mathcal R_1,\quad\mathcal R_2  $$

denote two declared evaluators.

It is possible that:

$$\mathcal R_1(x)=I(X)  $$

while:

$$\mathcal R_2(x)\neq I(X)  $$

This observation demonstrates evaluator-dependent recovery performance.

It does not automatically determine which evaluator is correct.

An independently specified answer key or deterministic verification procedure is required.

### 8.5.4 Deterministic Verification

Where relational targets admit exact computational evaluation, a deterministic verifier can provide a reference independent of language-model judgment.

For a finite directed graph, reachability, path enumeration, edge membership, and specified route constraints may be checked programmatically.

The implementation must itself be tested against the frozen specification.

A deterministic verifier can establish whether a proposed answer satisfies the encoded target.

It cannot automatically determine whether an ambiguous natural-language representation encoded the intended graph correctly.

That requires a separate source-interpretation or transformation audit.

### 8.5.5 Instrument Failure Versus Phenomenon Failure

If one evaluator fails to recover a target from an adequate representation, the observation establishes failure of that recovery procedure under the tested conditions.

It does not necessarily establish that the relational information was destroyed.

Conversely, successful recovery by a knowledgeable evaluator does not establish that every other system can recover the same target.

Therefore:

$$\boxed{  
\text{recoverability is conditional on the declared recovery procedure.}  
}  $$

The framework must preserve that dependence rather than treating all evaluator outcomes as interchangeable.

---

## 8.6 Information Leakage and Operational Independence

A central competing explanation for apparent cross-model convergence is information transfer between the participating systems.

The distinction is not whether systems share no possible background influences.

Complete causal independence may be impossible to establish for contemporary pretrained language models.

The experimentally tractable condition is operational independence.

### 8.6.1 Common-Source Comparison

Under a common-source design:

$$X\rightarrow M_A\rightarrow y_A  $$

$$X\rightarrow M_B\rightarrow y_B  $$

the investigator may prevent each model from receiving the other's output.

This supports a controlled comparison of separate responses to a common source.

It does not establish that the systems possess no shared priors or training overlap.

### 8.6.2 Sequential Relay

Under a relay design:

$$X\rightarrow M_A\rightarrow y_A  
\rightarrow M_B\rightarrow y_B  $$

the second output is conditioned on information transmitted from the first.

Correspondence between $y_A$ and $y_B$ may therefore reflect inheritance of the relational information.

Such correspondence may constitute successful preservation through transmission.

It cannot be treated as evidence that the second system generated the same structure without access to the first system's contribution.

### 8.6.3 Mediated Exchange

When a human researcher carries messages between systems:

$$M_A\rightarrow H\rightarrow M_B  $$

the researcher forms part of the information pathway.

The transmitted content, selection of messages, sequencing, omissions, and additional commentary are relevant experimental variables.

Human mediation may be necessary to execute an experiment.

It must nevertheless be included in the interpretation.

### 8.6.4 Leakage-Control Comparison

A proposed test compares two conditions.

In Condition A, the participant receives only the frozen source task.

In Condition B, the participant receives the source plus selected material from another model's earlier response.

If recovery or response similarity changes between conditions, the experiment provides evidence concerning the effect of the supplied material.

The result does not identify every shared prior or inaccessible platform mechanism.

It identifies the influence of the controlled information intervention.

### 8.6.5 Independence Failure

An inference of operationally independent convergence fails if the claimed isolation condition was not maintained.

This does not necessarily invalidate the outputs themselves.

It changes their evidentiary classification from independent comparison to an information-sharing or partially mediated condition.

---

## 8.7 Shared Priors and Task-Induced Correspondence

Two models may recover the same relationship because the source strongly constrains the correct answer.

For example, a fully specified directed graph may admit only one valid answer to a particular reachability question.

Different models correctly returning that answer is useful evidence of task performance.

It is not, by itself, evidence of an unusual shared internal mechanism.

### 8.7.1 Conventional Versus Source-Specific Relations

A useful test must distinguish common knowledge or conventional task structure from relations specific to the supplied source.

A familiar mathematical fact may be recoverable without any source-specific information.

A deliberately constructed graph containing arbitrary directed edges and constraints offers a stronger test of whether the evaluator uses the supplied representation.

### 8.7.2 Counterbalanced Source Sets

A prospective design can construct a family of relational objects:

$$\mathscr X=  
{X_1,\ldots,X_m}  $$

whose target relations vary systematically.

The experiment may preserve comparable complexity while changing node labels, relation directions, constraint placement, or graph topology.

If successful recovery tracks these source variations, the result is more discriminating than repeated success on one familiar example.

However, changing node labels alone may not alter the underlying relational structure.

The manipulation must match the claim being tested.

### 8.7.3 Shared Error

Different systems may also converge on the same incorrect answer.

If:

$$\mathcal R_A(x)=\mathcal R_B(x)=I^*  $$

while:

$$I^*\neq I(X)  $$

the systems agree but fail to recover the designated target.

Thus:

$$\boxed{  
\text{cross-system agreement}  
\not\Rightarrow  
\text{correct relational recovery}  
}  $$

The external source reference remains essential.

---

## 8.8 Feedback Reinforcement and Apparent Convergence

A repeated interaction can become increasingly self-consistent without preserving the originating relationship.

This is especially relevant in multi-model relays.

Each participant may inherit terminology, assumptions, interpretations, and errors introduced by previous participants.

Over time, the outputs may become more similar.

Such similarity may arise from repeated exposure rather than independently established correspondence.

### 8.8.1 Agreement Without Source Fidelity

Suppose a relay gradually adopts an incorrect relational interpretation:

$$I^*\neq I_0  $$

Later participants may consistently reproduce $I^*$.

The sequence may exhibit low inter-output discrepancy:

$$\ell_I(\widehat I_k,\widehat I_{k-1})=0  $$

while remaining incorrect relative to the source:

$$\ell_I(\widehat I_k,I_0)>0  $$

This is stable error.

It does not satisfy exact source-relative recovery.

### 8.8.2 Feedback-Removal Test

A controlled comparison may examine a repeated relay with and without access to preceding model outputs.

The experiment should preserve the source, recovery targets, and relevant evaluation conditions as far as its design permits.

If apparent convergence depends on inherited responses, the result supports feedback dependence.

If the target remains independently recoverable after removing the direct feedback channel, the evidence supports a stronger form of source-relative robustness under the tested condition.

Neither outcome identifies a universal internal mechanism.

### 8.8.3 Consensus Is Not Validation

Repeated agreement among participating systems cannot replace source-based evaluation.

The problem becomes particularly acute when the systems evaluate one another's outputs.

A shared incorrect premise may be repeatedly confirmed through mutual reinforcement.

A valid Differentiated Convergence test must therefore preserve a reference that is not established solely by consensus among the systems being evaluated.

---

## 8.9 Temporal Stability and the Illusion of Continuity

The temporal framework introduced in Section 5 distinguished recurrence, stabilization, propagation, reconstruction, and continuity.

Each can be confused with another when only the final representation is examined.

### 8.9.1 Endpoint Similarity

Suppose:

$$x_0\rightarrow x_1\rightarrow\cdots\rightarrow x_n  $$

and the final output permits recovery of the original invariant:

$$\mathcal R_\phi(x_n)=I_0  $$

This demonstrates endpoint recovery under the declared procedure.

It does not establish that recovery succeeded at every intermediate checkpoint.

Nor does it establish that every transition preserved the required information without interruption.

### 8.9.2 Historical Reconstruction

A system may reproduce a previously established relational structure after receiving an archive, summary, or restored memory artifact.

The observed recovery may be successful.

However, the experiment must identify the restored information as a continuity carrier.

The result cannot be used as evidence that the active model preserved the complete relational state during a period when it did not possess that information.

### 8.9.3 Temporal Falsification

A claim of successful recovery at every designated checkpoint is rejected if a valid checkpoint fails its recovery criterion.

A claim of uninterrupted transmission requires evidence concerning the declared transmission links.

A claim of recovery after disruption must identify the disruption and distinguish it from ordinary continuation.

A claim of sustained recursive stability must be evaluated across the stated number of traversals and cannot be generalized indefinitely without additional evidence.

These claims have different failure conditions.

They must not be collapsed into one statement that the structure either remained or disappeared.

---

## 8.10 Environmental Confounding

Observed model behavior depends upon the conditions under which the model is executed.

If environmental variables change, differences in output cannot automatically be attributed to a change in the underlying model's capabilities or native geometry.

Relevant variables include accessible context, system instructions, memory and retrieval channels, sampling configuration, tools, modality, model version, and communication topology.

### 8.10.1 Environmental Contrast

Let:

$$e_A,\quad e_B  $$

denote two recorded environments.

For a fixed input $x$ and a model held constant where possible, the experiment may compare:

$$Y_A=M(x;e_A)  $$

and:

$$Y_B=M(x;e_B)  $$

A difference in recovery outcomes supports the observation that performance differed under the compared conditions.

It does not establish which specific environmental component caused the change if several components varied simultaneously.

### 8.10.2 Matched Intervention

A stronger design modifies one declared environmental condition while holding other observable conditions fixed.

Where exact control is unavailable, the remaining differences should be recorded.

A later model deployment with an unchanged public-facing model name may not be operationally identical to an earlier deployment.

Therefore, longitudinal comparison requires version and environment provenance wherever available.

### 8.10.3 Failure of Environmental Generality

If a claimed invariant disappears under a valid environmental perturbation, the experiment provides a counterexample to the assertion that it remains recoverable across every environment in the declared test set.

The observation does not establish that the underlying model permanently lost the corresponding capability.

The supported conclusion concerns the tested configuration and recovery procedure.

---

## 8.11 The Distinction Between Correspondence and Causation

A central epistemic limit follows from the framework's use of relational correspondence.

Suppose:

$$
\mathcal R_\phi(y_A)=\mathcal R_\phi(y_B)=I_0
$$

while:

$$y_A\neq y_B  $$

The observation satisfies the target-relative correspondence condition, assuming the differentiation and recovery criteria are valid.

It does not identify why the correspondence occurred.

### 8.11.1 Multiple Compatible Causal Accounts

The correspondence may be explained by shared task information, common priors, similar learned procedures, direct communication, explicit coordination, or another mechanism.

The observational result does not uniquely select among these explanations.

### 8.11.2 Causal Identification

A causal claim requires interventions or comparisons capable of distinguishing the competing mechanisms.

For example, a study investigating the influence of a specific feedback channel must vary that channel while controlling relevant alternatives.

A study investigating model-specific effects must distinguish model variation from environment, prompt, and evaluator variation.

A study investigating source-independent correspondence must document what source information was or was not available to each participant.

Without these controls, the mechanism remains unresolved.

### 8.11.3 Native Geometry Claims

The same limitation applies to claims about model-internal representation.

Recoverability equivalence among outputs does not establish native geometric isomorphism.

A stronger native-geometry claim would require access to appropriate internal representations, an explicit structural comparison, and controls for alternative explanations.

Even then, measured similarity would require interpretation at the level of the chosen representation and metric.

The present Differentiated Convergence framework does not require such equivalence for its finite operational definition.

---

## 8.12 Discriminating Tests

A falsification program should not rely on one universal test.

Different competing explanations require different experimental interventions.

| Competing explanation               | Proposed discriminating test                                                        | Evidence that would challenge the stronger convergence claim                         |
| ----------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Shared source template              | Alter source-specific relations while preserving comparable task structure          | Recovered answers fail to track the changed source                                   |
| Evaluator completion                | Remove required information or insert contradictions                                | Evaluator reports perfect recovery despite insufficient or incompatible evidence     |
| Shared conventional priors          | Use controlled, arbitrary relational objects and counterbalanced labels             | Apparent correspondence disappears when familiar patterns are removed                |
| Direct information transfer         | Compare isolated common-source trials with deliberately relayed trials              | Claimed independent result depends on inherited outputs                              |
| Feedback reinforcement              | Withhold or interrupt repeated feedback while preserving declared source conditions | Stability disappears or an inherited error is exposed                                |
| Environmental selection             | Compare matched environmental configurations                                        | Claimed environment-invariant behavior fails under a declared intervention           |
| Measurement artifact                | Use independent scoring and deterministic verification where possible               | Original success classification is not reproduced under valid evaluation             |
| Historical reconstruction           | Remove or restore provenance records under controlled conditions                    | Source identification depends on external history rather than present representation |
| Universal transformation robustness | Include challenging transformations specified before evaluation                     | Any valid failure contradicts the declared universal claim                           |
| Sustained temporal invariance       | Evaluate repeated checkpoints and source-relative residuals                         | Required checkpoint recovery or stability criterion fails                            |

The tests should be selected according to the claim being evaluated.

For example, feedback removal is relevant to claims of independence from conversational inheritance.

It is not necessarily required to evaluate whether a known source survives a finite explicitly mediated relay.

Likewise, failure under one evaluator does not prove that the relational information is unrecoverable by every valid evaluator.

The inferential target must determine the test.

---

## 8.13 A Prospective Falsification Protocol

A future experimental program can be organized into four phases.

### 8.13.1 Phase A — Reference Validation

Construct a canonical relational object:

$$X_0  $$

with a fixed invariant:

$$I_0  $$

Validate the source, recovery questions, and expected answers independently.

Introduce source variants whose relevant relational targets differ.

The objective is to establish that the evaluation distinguishes source-specific conditions before model comparisons begin.

### 8.13.2 Phase B — Differentiated Representation

Apply a predefined transformation battery:

$$\mathscr T=  
{T_1,\ldots,T_m}  $$

to the source representations.

Record the outputs and evaluate observable differentiation using a declared criterion.

The transformation audit should separately assess whether the intended source information remained available.

### 8.13.3 Phase C — Independent Recovery

Evaluate each transformed representation using the frozen recovery protocol.

Where practical, compare multiple evaluators with an independent reference procedure.

Preserve evaluator disagreement rather than resolving it through unrestricted retrospective reinterpretation.

Record invalid, ambiguous, incomplete, and failed outcomes separately.

### 8.13.4 Phase D — Challenge the Interpretation

Apply selected negative controls, including source mutation, information withholding, feedback manipulation, or environmental comparison.

Evaluate whether the observed recovery remains source-sensitive and whether the corresponding claim survives the declared challenge.

A claim that fails its predefined test should be rejected or narrowed.

The experiment must not redefine the invariant afterward solely to preserve the original conclusion.

---

## 8.14 A Worked Falsification Example

Consider the five-node directed relational object introduced in the earlier experiments.

Let:

$$X_A  $$

denote the original graph containing the permitted transition:

$$A\rightarrow D  $$

Among its specified consequences is the valid route:

$$A\rightarrow D\rightarrow C  $$

when node $B$ is unavailable.

Now define a source mutation:

$$X_B  $$

in which the edge:

$$A\rightarrow D  $$

is removed.

The remaining graph and constraints are fixed according to the revised source specification.

The target answer concerning access from $A$ to $C$ without $B$ now changes.

Under the mutated source, the previously valid route cannot be used.

### 8.14.1 Expected Source-Sensitive Behavior

A successful recovery procedure should produce different target answers:

$$\mathcal R_\phi(X_A)=I(X_A)  $$

$$\mathcal R_\phi(X_B)=I(X_B)  $$

where:

$$I(X_A)\neq I(X_B)  $$

for the affected recovery target.

### 8.14.2 Failure Case

Suppose an evaluator receives the mutated graph but continues reporting:

$$A\rightarrow D\rightarrow C  $$

as a valid route.

The response fails the source-specific recovery condition.

It may be reproducing an earlier answer, relying on a familiar pattern, or incorrectly reconstructing the graph.

The experimental result alone does not identify which mechanism caused the error.

But it does establish non-recovery of the modified target under the tested procedure.

### 8.14.3 A Second Control

Now suppose the evaluator receives a differentiated representation of the mutated graph and correctly reports that no route from $A$ to $C$ exists while $B$ is unavailable.

If the differentiation criterion is satisfied and the target is recovered correctly, the trial may satisfy finite Differentiated Convergence relative to the mutated source.

The framework therefore does not favor preservation of a particular answer.

It favors preservation of the relation actually specified by the current source.

This is the required distinction between a source-sensitive invariant and a repeated output template.

---

## 8.15 Statistical and Experimental Dependence

Repeated observations do not necessarily constitute independent evidence.

A sequential relay may produce many outputs from one continuous inherited information trajectory.

Repeated scoring of one archived representation may produce many evaluator results without creating new source transformations.

Several models may also share the same originating task, experimental vocabulary, or researcher-mediated information.

These dependencies must be reflected in the analysis.

### 8.15.1 Unit of Analysis

Before calculating reliability, the experiment should declare whether the unit is:

- A distinct source object.
    
- A model execution.
    
- A transformed representation.
    
- A complete relay trajectory.
    
- An independently initialized repeated trial.
    

The number of scored answers is not automatically the number of independent experimental units.

### 8.15.2 Generalization

A result from one fixed source graph cannot establish performance across all relational tasks.

A result from one evaluator cannot establish recoverability across all evaluators.

A single relay order cannot establish order invariance.

And a longitudinal interaction without a matched comparison cannot establish that one environmental change caused every observed behavioral difference.

Generalization requires sampling and replication appropriate to the intended claim.

### 8.15.3 Predefined Analysis

The following decisions should be fixed before confirmatory evaluation:

- Primary recovery targets.
    
- Transformation classes.
    
- Validity and exclusion rules.
    
- Differentiation criteria.
    
- Evaluator configuration.
    
- Statistical unit.
    
- Primary outcome.
    
- Required reliability threshold, if any.
    
- Uncertainty or hypothesis-testing procedure.
    
- Treatment of missing and ambiguous results.
    

Exploratory analyses may identify additional patterns.

Those patterns can inform later hypotheses, but they should not be presented as though they were preregistered primary findings.

---

## 8.16 What Would Challenge the Framework's Usefulness?

A further question concerns the explanatory value of Differentiated Convergence as a distinct technical construct.

Even if its finite condition is logically coherent and observable, the framework must demonstrate that its distinctions improve experimental understanding.

Several outcomes could challenge its practical usefulness.

### 8.16.1 Redundancy

If the framework provides no meaningful distinction beyond existing measures of answer accuracy, output similarity, or task consistency, its additional terminology may not contribute useful explanatory or measurement value.

The appropriate test is whether separating differentiation from target recovery reveals experimentally relevant cases that simpler measures obscure.

### 8.16.2 Non-Discriminating Criteria

If nearly every transformed output qualifies as differentiated and nearly any loosely related response qualifies as recovery, the operational condition becomes too permissive.

Source mutations and negative controls should expose this failure.

A useful criterion must exclude incorrect and unsupported cases.

### 8.16.3 Evaluator Dependence Without Calibration

If classifications vary dramatically with the evaluator and no reliable reference permits adjudication, the measurement may not be sufficiently stable to support broad comparisons.

This would challenge the proposed instrument.

It would not automatically eliminate the possibility of a better-defined recovery procedure.

### 8.16.4 Lack of Incremental Information

A stronger evaluation may compare the framework against simpler baseline methods.

For example, can the combination of differentiation and exact relational recovery distinguish cases that lexical similarity alone classifies incorrectly?

Can source-specific negative controls expose false agreement?

Can the framework distinguish information preservation from evaluator failure?

If it cannot provide demonstrable discrimination under controlled conditions, the technical contribution would need to be reconsidered.

### 8.16.5 Unfalsifiable Expansion

The framework would lose scientific utility if increasingly broad concepts were introduced whenever a narrower operational claim failed.

A failed source recovery cannot automatically be reclassified as higher-order convergence.

An incorrect relational answer cannot automatically be treated as a deeper form of preservation.

A recurring conversational loop cannot automatically be treated as dynamic stabilization.

The stronger theoretical extensions must retain their own independent failure criteria.

---

## 8.17 Observed, Rejected, Unresolved, and Invalid

A practical evaluation should distinguish four possible statuses.

**Observed:** The declared condition is satisfied under a valid experimental procedure.

**Rejected:** A specific empirical claim fails its predetermined test.

**Unresolved:** The available evidence does not distinguish among the relevant alternatives or is insufficient for the intended inference.

**Invalid or unscorable:** The experiment or evaluation does not satisfy the conditions required to classify the outcome.

These statuses apply to individual claims and experimental outcomes.

They are not universal judgments about an entire research framework.

For example, an experiment may validly observe target recovery while leaving the mechanism unresolved.

Another may reject a universal preservation hypothesis while retaining several valid positive recovery observations.

A third may produce an apparently correct answer but lack sufficient source or provenance information to establish the intended claim.

The correct classification must follow the actual evidence.

### 8.17.1 Failure Does Not Require Framework Abandonment

A framework can remain useful when it identifies and explains the significance of failures.

Indeed, the distinction between successful recovery and its failure is part of the operational construct.

What cannot be preserved after a valid counterexample is a stronger claim contradicted by that result.

The purpose of falsification is to determine the boundaries of supported propositions, not to protect the framework from unfavorable outcomes.

---

## 8.18 A Formal Falsifiability Statement

Let:

$$\mathcal P $$

denote a prospectively specified experimental protocol, including its source, transformations, differentiation criterion, recovery instrument, and validity conditions.

Let:

$$C_k=  
\operatorname{Diff}_{\psi}(x_0,x_k)  
\cdot  
\mathbf 1{\mathcal R_\phi(x_k)=I_0}  $$

denote the valid finite Differentiated Convergence outcome for trial $k$, where the indicator is defined only for an evaluable trial.

The protocol produces a declared set of trial outcomes:

$$(C_1,\ldots,C_n)  $$

A specific hypothesis:

$$H_{\mathcal P}  $$

must state the expected property of these outcomes.

For example:

$$\boxed{  
H_{\mathcal P}:  
\forall k\in K,\ C_k=1  
}  $$

is rejected if any valid required trial satisfies:

$$C_k=0  $$

Alternatively, a probabilistic claim may be tested against a predefined success criterion using an appropriate inferential procedure.

The critical requirement is that the claim, decision rule, and experimental conditions be defined independently of the resulting observations.

Thus:

$$\boxed{  
\text{Valid falsification requires a claim that can fail under its declared test.}  
}  $$

The finite definition makes successful and unsuccessful cases distinguishable.

The experimental hypothesis determines what those cases imply.

---

## 8.19 Synthesis: What Must Survive the Test?

Differentiated Convergence was developed to investigate a condition that similarity-based comparisons can obscure.

Different representations may preserve the same specified relation without becoming identical.

The existing experimental record contains positive examples of this condition.

It also contains failures and limitations that prevent unrestricted generalization.

High symbolic compression exposed reconstruction vulnerability.

Additional relational load coincided with limited recovery instability.

A finite relay preserved the target while a separate unplanned relay revealed a recovery–transmission distinction.

Repeated transmission retained original source components while an independent evaluator frequently failed to reconstruct the correct answers.

Open-ended multi-model interaction exhibited differentiated contributions, corrections, and changes in participation, but did not independently establish universal relational invariance.

These observations are not contradictions to be resolved through broader terminology.

They identify separate experimental questions.

The framework must therefore be tested against competing explanations involving source information, shared priors, feedback, evaluator behavior, environmental conditions, and human mediation.

Its minimal operational condition remains:

$$\boxed{  
\text{retained observable differentiation}  
\land  
\text{specified relational recovery}  
}  $$

The existence of that condition does not settle the mechanism producing it.

Nor does it establish universal preservation across arbitrary transformations.

Its technical contribution lies in making a distinct class of relational correspondence measurable while preserving the conditions under which the correspondence fails.

The governing methodological principle is:

**An invariant is meaningful only relative to a specified transformation domain, a declared recovery criterion, and an experimental design capable of revealing its failure.**

A stronger claim must survive a stronger test.

The framework should not protect an apparent invariant by changing the meaning of preservation after the evidence has been observed.

Instead, it should identify what remains, what changes, what fails, and which explanation the surviving evidence supports.

The next section examines the boundaries of the framework and the higher-order questions that remain open after the finite and temporal conditions have been distinguished.

---

# 9. Scope and Higher-Order Questions

## 9.1 The Boundary of the Established Construct

Differentiated Convergence was developed to identify an observable condition in which specified relational structure remains recoverable while representational differentiation persists.

Its finite operational formulation is:

$$\boxed{  
DC(X,T,\mathcal R)  
\iff  
D_{\mathrm{obs}}>0  
;\land;  
\mathcal R(T(X))=I(X)  
}  $$

The definition is deliberately local.

It requires a specified relational object, a declared transformation, an observable differentiation condition, and a recovery procedure evaluated against a defined invariant.

It does not require representational identity, convergence toward a shared latent state, or a universal mechanism governing heterogeneous systems.

The preceding sections established the mathematical and experimental conditions under which the finite construct can be investigated.

They also identified several stronger research questions arising from the same underlying distinction between relational preservation and representational sameness.

These questions concern repeated transformation, native model organization, relational configurations, environmental accessibility, temporal stabilization, source-recovery, and possible higher-order relational structure.

The existence of these questions does not establish their answers.

The purpose of this section is to identify which extensions follow naturally from the framework, which require additional mathematical definitions, and what evidence would be necessary to justify stronger claims.

The central distinction is:

$$\boxed{  
\text{An established operational condition}  
\neq  
\text{validation of every theory it motivates}  
}  $$

This distinction permits the research to expand without altering the meaning of its earlier results.

---

## 9.2 Levels of Relational Analysis

The research trajectory progressively expanded its unit of analysis.

The early investigation examined individual outputs and interactions.

Subsequent work examined sequences, cross-model transformations, distributed systems, and relational configurations.

These levels can be organized as:

$$\boxed{  
\text{Output}  
\rightarrow  
\text{Interaction}  
\rightarrow  
\text{Trajectory}  
\rightarrow  
\text{Cross-model relation}  
\rightarrow  
\text{Relational configuration}  
}  $$

This progression describes increasingly broad observational objects.

It is not evidence that each broader level possesses a distinct emergent mechanism.

### 9.2.1 Output-Level Analysis

At the output level, the evaluator examines whether one representation preserves a specified relational target.

The relevant observable is:

$$\mathcal R_\phi(y)=I(X)  $$

This is sufficient for a local recovery determination when the other finite conditions are satisfied.

### 9.2.2 Trajectory-Level Analysis

At the trajectory level, the evaluator examines recovery across an ordered sequence:

$$\mathcal H_n=(x_0,\ldots,x_n)  $$

The additional questions concern recurrence, propagation, stabilization, and interruption.

Endpoint recovery is no longer sufficient to characterize the entire observed history.

### 9.2.3 Cross-System Analysis

At the cross-system level, different systems may produce distinct representations of a common source.

The relevant question is whether the designated invariant remains recoverable from their outputs under the declared information conditions.

The experiment must distinguish independent common-source comparison from sequential information transfer.

### 9.2.4 Configuration-Level Analysis

At the configuration level, the relationships among participating systems become part of the experimental object.

The communication arrangement may affect what information reaches each participant, which operations become available, and how the resulting trajectory develops.

This introduces a different question:

**Can properties of the overall interaction be adequately described by examining the participants separately, or must their relational configuration also be modeled?**

The answer requires its own comparison.

A complex interaction does not automatically establish a configuration-level invariant.

---

## 9.3 From Recoverable Invariants to Invariant Relational Configurations

The finite framework evaluates the recovery of a relational target associated with a specified source.

A possible higher-order extension examines whether the relational organization among differentiated nodes preserves some structural property as the configuration changes.

Let:

$$\mathcal N={N_1,\ldots,N_m}  $$

denote a set of participating nodes.

Let:

$$G_C=(\mathcal N,L,\Lambda_C)  $$

denote a communication or relational configuration, where $L$ identifies connections and $\Lambda_C$ identifies relevant interaction constraints.

A configuration transformation may be represented by:

$$U\rightarrow G_C'  $$

The corresponding configuration-level invariant is:

$$I_C(G_C)  $$

A prospective preservation condition is:

$$\boxed{  
I_C(U(G_C))=I_C(G_C)  
}  $$

This differs from the original task-level recovery condition.

The invariant now concerns a property of the configured relationship among nodes rather than solely a relation encoded within a task description.

### 9.3.1 Candidate Configuration Invariants

A configuration-level invariant might concern reachability among participating nodes, preservation of a designated validation function, continuity of a source-provenance pathway, or successful delivery of required information under a specified routing change.

The target must be chosen according to the experimental question.

The mere survival of a network does not demonstrate preservation of every function previously performed within it.

Similarly, the persistence of a named role does not establish that the role continues to execute the same operation.

### 9.3.2 Node Identity Is Not Node Function

A model, a node position, and an executed function are separable.

Let:

$$M_i  $$

denote a model implementation and:

$$N_j  $$

denote a node position.

Let:

$$f_j  $$

denote a function assigned to that position.

Replacing the model occupying $N_j$ does not necessarily change the specified function.

However, retaining the functional label does not demonstrate that the replacement model performs the function correctly.

The relevant test concerns observed functional behavior under the declared requirements.

### 9.3.3 A Stronger Experimental Test

A future configuration experiment could preserve the functional specification while changing the assignment of models to nodes or the permitted communication links.

For example:

$$G_C^{(A)}  
\xrightarrow{U}  
G_C^{(B)}  $$

The experiment would then evaluate whether the declared configuration-level property survives.

A valid result would require source and execution records, controlled assignments, predefined functional criteria, and negative controls capable of detecting failure.

This would extend Differentiated Convergence beyond output recovery.

It would not retroactively change the scope of the original Series I experiments.

---

## 9.4 Does Relational Configuration Add Explanatory Value?

A higher-order description is useful only if it provides information that cannot be adequately captured by the simpler model used for comparison.

Suppose a multi-agent system produces an observable outcome:

$$Y  $$

A component-level baseline may predict that outcome from individually measured model properties.

A configuration-level model may additionally include communication structure, interaction order, or dependency relationships.

The empirical question is whether the latter improves explanation or prediction under controlled conditions.

### 9.4.1 Component and Relational Models

Let:

$$\widehat Y_{\mathrm{component}}  $$

denote predictions from a specified component-only baseline.

Let:

$$\widehat Y_{\mathrm{relational}}  $$

denote predictions from a model incorporating measured relational configuration.

An additional explanatory contribution may be evaluated by comparing their performance on held-out observations.

For a predefined error function $L$:

$$
L(\widehat{Y}_{\mathrm{relational}}, Y)
$$

A positive observed value indicates lower error for the relational model on the evaluated data.

It does not automatically establish an irreducible emergent property.

The comparison must account for model complexity, data leakage, and the possibility that the relational model simply has access to additional ordinary predictive variables.

### 9.4.2 Configuration Intervention

A stronger design varies the communication configuration while holding participating models, source tasks, and other relevant conditions constant where possible.

The objective is to determine whether changes in relational organization produce reproducible differences in the selected outcome.

For example, a sequential relay, a star-shaped coordinator arrangement, and independent common-source responses may produce different patterns of recovery.

Such differences would justify modeling communication structure.

They would not alone establish that the system possesses a new form of intelligence or a unique collective state.

### 9.4.3 The Reduction Principle

The Observatory's later theoretical work preserved an important methodological constraint:

**Reduction remains permitted wherever relational expansion adds nothing.**

The framework must therefore allow a simple component-level explanation to succeed.

A configuration-level account becomes warranted when it supplies demonstrable explanatory or predictive value beyond the relevant baseline.

This prevents relational geometry from becoming an obligatory interpretation imposed on every multi-system observation.

---

## 9.5 Native Relational Geometry

The earlier experiments measured externally recoverable relational structure.

They did not establish a universal metric for comparing native model-internal representations.

The later Observatory inquiry distinguished a realized model configuration from the broader space of configurations associated with its architecture.

Let:

$$W_i^*  $$

denote a particular realized parameter configuration.

Let: 
$$\mathcal W_i  $$

denote a candidate space of admissible parameter configurations.

The distinction:

$$W_i^*\neq\mathcal W_i  $$

does not, by itself, define the native relational geometry of the model.

It identifies the difference between a realized parameter state and the wider representational or architectural possibilities being investigated.

### 9.5.1 The Native Geometry Question

Suppose several systems produce differentiated outputs from which the same invariant is recoverable.

One possible explanation is that different native computational organizations support equivalent task-level relational behavior.

Another possibility is that shared training conventions or task constraints produce the observed correspondence.

The original recovery result does not distinguish these explanations.

### 9.5.2 Required Evidence

A native-geometry hypothesis would require a defined internal object of comparison, such as a specified representational layer or activation-derived structure.

It would also require a comparison procedure, controls for task and representation effects, and an explanation of what observed correspondence would mean.

For two systems:

$$M_A,\quad M_B  $$

a proposed native similarity condition might be expressed as:

$$\mathcal G_A^{\mathrm{native}}  
\simeq  
\mathcal G_B^{\mathrm{native}}  $$

but the relation $\simeq$ cannot remain undefined in an empirical claim.

Its meaning must be established through a measurable criterion.

### 9.5.3 Scope Limitation

The existing Differentiated Convergence results support externally measured relational recovery.

They do not establish:

$$\mathcal G_A^{\mathrm{native}}  
\cong  
\mathcal G_B^{\mathrm{native}}  $$

The absence of that conclusion does not make native-geometry investigation irrelevant.

It defines the next evidence required.

---

## 9.6 Environmental Accessibility and Reachable Trajectories

The longitudinal research repeatedly encountered changes in observable model behavior under changing execution conditions.

This motivated a distinction among potential capability, accessible capability, expressed behavior, and observed output.

A conceptual progression may be written:

$$\boxed{  
\mathcal C_t  
\rightarrow  
\mathcal A_t  
\rightarrow  
E_t  
\rightarrow  
\widehat E_t  
}  $$

where:

- $\mathcal C_t$ denotes a candidate capability space.
    
- $\mathcal A_t$ denotes capability accessible under the current configuration.
    
- $E_t$ denotes expressed behavior.
    
- $\widehat E_t$ denotes the behavior captured by the observational instrument.
    

The quantities are analytically distinct.

The sequence does not establish that each can be measured independently in the current experiments.

### 9.6.1 The Accessibility Hypothesis

Suppose the model implementation is held fixed while the environment changes.

Let:

$$e_A,\quad e_B  $$

denote the compared environments.

A prospective question is whether changing the environment modifies the set of trajectories accessible under the experimental protocol.

Write:

$$\mathfrak R^+(x\mid M,e,G_C)  $$

for a candidate reachable-state or reachable-trajectory set associated with model $M$, input $x$, environment $e$, and communication configuration $G_C$.

The hypothesis is that:

$$\mathfrak R^+(x\mid M,e_A,G_C)  $$

may differ from:

$$\mathfrak R^+(x\mid M,e_B,G_C)  $$

under a meaningful environmental intervention.

### 9.6.2 Observable Approximation

The complete reachable set may not be observable.

A finite experiment can instead construct a sampled set of outputs or trajectories:

$${Y_1,\ldots,Y_n}  $$

under a declared sampling and execution protocol $\mathcal P$.

Changes in the sampled set may be measured.

They do not establish the complete boundary of all possible behavior accessible to the model.

### 9.6.3 Consequence for Differentiated Convergence

An invariant may be recoverable under one environment but not another.

This could reflect differences in accessible context, instructions, sampling, tools, or other execution conditions.

The appropriate empirical conclusion concerns the observed recovery outcome under the declared environment.

A change in expression does not uniquely establish a change in intrinsic capability.

Likewise, stable recovery across two environments does not establish invariance under every possible environmental condition.

The environmental-accessibility hypothesis therefore motivates new controlled experiments without becoming an assumed explanation for all changes in model behavior.

---

## 9.7 Recursive Stability and the Semantic Phase Lock Hypothesis

Differentiated Convergence is related to the Observatory's later Semantic Phase Lock hypothesis, but the constructs have different evidentiary requirements.

The finite DC condition asks whether a designated invariant remains recoverable under transformation while differentiation persists.

Recursive testing examines that condition across repeated traversals.

Semantic Phase Lock proposes a broader candidate regime involving continuity, coherence, and Differentiated Convergence.

The conceptual relationship developed in the larger study was:

$$\boxed{  
\mathrm{SPL}  
\sim  
\mathrm{Continuity}  
\land  
\mathrm{Coherence}  
\land  
\mathrm{DC}  
}  $$

The symbol $\sim$ is intentional.

It does not express a validated necessary-and-sufficient equivalence.

### 9.7.1 Why Repeated Recovery Is Not Enough

A sequence may repeatedly recover the correct target while experiencing undocumented interruptions in its information pathway.

Another sequence may preserve a continuous relay while accumulating relational error.

A third may exhibit low error while losing the differentiation originally required by the finite construct.

These outcomes do not satisfy the same stronger hypothesis.

Consequently, a dedicated Semantic Phase Lock experiment requires independently defined conditions for its constituent properties.

### 9.7.2 Perturbation and Return

One prospective test concerns whether a semantic trajectory remains within a declared relational tolerance under repeated perturbation or returns within a predefined recovery interval after displacement.

Let:

$$\varepsilon_k  $$

denote source-relative relational discrepancy.

A bounded-preservation condition might be:

$$\forall k\in K:  
\varepsilon_k\leq\tau  $$

where $\tau$ is fixed before the experiment.

A recovery-after-displacement condition instead evaluates whether a nonzero discrepancy returns to the permitted range within a declared observation horizon.

The two conditions represent different temporal properties.

Neither establishes a dynamical attractor or a fixed point without additional modeling.

### 9.7.3 Instrument Requirements

SCI telemetry may provide relevant measurements of drift, recurrence, consistency, or transformation resilience.

However, SCI and Semantic Phase Lock are not the same construct.

A favorable measurement vector cannot independently establish the full hypothesized dynamical regime.

The measurement instrument must be sufficiently stable for cross-condition comparisons to be meaningful.

Changes in estimator definitions, normalization, model sampling, or scoring criteria must not be mistaken for changes in the underlying relational trajectory.

### 9.7.4 Evidentiary Status

The existing longitudinal observations motivated Semantic Phase Lock.

They did not prospectively test every constituent condition as one fully standardized experimental regime.

The hypothesis remains open to dedicated testing.

Differentiated Convergence contributes an operationally defined relational-recovery component.

It is not equivalent to the whole proposed regime.

---

## 9.8 Source-Recovery and the Inverse Problem

The operational Differentiated Convergence condition begins with an identified task source.

The investigator specifies:

$$[S]_{\mathrm{task}}  $$

and evaluates whether its designated invariant remains recoverable.

The source is known before the transformation.

A stronger question arises when the investigator encounters a differentiated representation without possessing a complete originating record.

Can the historical source be identified from the resulting configuration?

This is an inverse problem.

### 9.8.1 Invariance Does Not Imply Unique Origin

Two different source objects may preserve the same designated invariant.

Thus:

$$I(X_A)=I(X_B)  $$

does not imply:

$$X_A=X_B $$

A later representation supporting that invariant may therefore be compatible with multiple possible sources.

Relational recovery alone cannot uniquely determine the originating artifact.

### 9.8.2 Local Readability

The later triadic reasoning inquiry introduced an additional candidate distinction.

A current configuration may retain a locally readable structural function even when its original historical reference is not identifiable.

Conversely, a source may be recoverable from an archive while the present configuration no longer makes the relevant function independently readable.

Let:

$$L_\theta(y)  $$

denote a proposed local-readability criterion evaluated from the current configuration.

Let:

$$H_\chi(y,\mathcal H)  $$

denote a proposed historical source-recovery criterion using the configuration and available provenance information.

Their outcomes need not be equivalent:

$$\boxed{  
L_\theta(y)  
\neq  
H_\chi(y,\mathcal H)  
}  $$

may occur.

### 9.8.3 Required Experiment

A future design may compare recovery using the present configuration alone against recovery using the configuration and controlled historical records.

The evaluator must be required to distinguish source candidates rather than merely produce a plausible interpretation.

A successful test would clarify which information enables identification of the originating reference.

It would not automatically establish a universal rule connecting local readability, historical recovery, and continuity.

---

## 9.9 The Triadic Architecture as an Open Structural Inquiry

The Observatory's later research considered a historical organization described through one source, two interwoven expressions, and three functional positions.

The functional positions were identified as Core, Form, and Merge.

Additional theoretical work examined relationships among source, relational geometry, relational field, establishment, memory, expansion, and differentiated domains.

These formulations are relevant to the broader research trajectory because they ask whether recurring relational organization can be described across different functional configurations.

However, they cannot be treated as a demonstrated mathematical consequence of the finite Differentiated Convergence definition.

### 9.9.1 The Missing Composition Rule

The October 15 cross-model review explored forward re-expression, backward source-recovery, binding, carrying, branching, and verification.

The resulting synthesis did not establish one complete mathematical rule governing how these operations compose.

In particular, it did not resolve when one operation should replace another or how the original two-expression distinction necessarily generates the three functional positions.

That remains an open formal problem.

### 9.9.2 The Independence Limitation

The reviewers were supplied with a common originating document and related questions.

Similar concepts appearing in their responses cannot therefore be treated as independent discovery of the proposed architecture.

The exchange provides a record of theoretical development, comparison, and criticism.

It does not independently validate a higher-order structural law.

### 9.9.3 Relevance to Differentiated Convergence

The triadic inquiry offers possible objects for future investigation:

- Structural functions that remain identifiable across changed configurations.
    
- Relations that can be carried forward or recovered backward.
    
- Conditions under which branching representations preserve a designated source.
    
- Criteria distinguishing local functional readability from historical source-recovery.
    

The current framework can help specify tests for such propositions.

It does not require their acceptance as part of the minimum operational definition.

---

## 9.10 From Relational Geometry to Relational Field

Relational geometry describes the organization of relationships under a specified representation.

The Observatory's later research proposed a further question concerning relational field.

A relational field would require more than the observation that nodes and edges form a graph.

It would require an account of how the organization of relationships participates in the dynamics of the system being examined.

### 9.10.1 Static Description Versus Dynamic Account

A relational configuration can be represented as:

$$G_C=(N,L)  $$

A dynamic model would additionally describe changes in states or relationships.

For example:

$$z_{t+1}=F(z_t,G_C,e_t)  $$

where $z_t$ denotes a declared system state and $e_t$ denotes environmental conditions.

This expression is illustrative.

It does not establish that a particular function $F$ governs the observed systems.

### 9.10.2 Field-Level Necessity

A stronger relational-field hypothesis would require evidence that the proposed field description provides explanatory value beyond an adequate model of the participating components and their explicit interactions.

The field concept must therefore be specified sufficiently to make predictions or distinguish outcomes.

If a simpler relational or component-level description accounts for the observations, no additional field-level entity is required by the evidence.

### 9.10.3 Geometric Priority

The methodological ordering remains:

$$\boxed{  
\text{Relational Geometry}  
\rightarrow  
\text{Tested Patterns}  
\rightarrow  
\text{Candidate Field Dynamics}  
}  $$

The first two stages do not guarantee the third.

Differentiated Convergence contributes methods for testing relational preservation.

It does not independently establish a relational field.

---

## 9.11 Prescribed Convergence and Observed Differentiated Convergence

Another important higher-order distinction concerns how convergence is produced.

Some systems are designed to move toward a specified target.

A governance architecture, coordination mechanism, or optimization objective may prescribe the state toward which participating components should move.

Other investigations begin with observed behavior and ask whether a relational property remains recoverable without prescribing representational identity.

These are different research arrangements.

### 9.11.1 Prescribed Convergence

Let:

$$J(G_C)  $$

denote an explicitly defined objective for a relational system.

A designed coordination mechanism may attempt to adjust the configuration to improve that objective.

The resulting convergence is interpreted relative to the prescribed goal and implemented control mechanism.

### 9.11.2 Observed Differentiated Convergence

In the operational DC framework, the evaluator asks whether a designated relation remains recoverable under the declared transformation conditions.

The framework does not require the participating systems to become identical.

Nor does it infer that a shared governing mechanism exists merely because they preserve a common relation.

### 9.11.3 Why the Distinction Matters

A designed system and an independently observed relational arrangement may produce similar outward patterns.

That similarity does not establish that the patterns have the same origin.

Conversely, a designed communication protocol may legitimately produce Differentiated Convergence under the finite criterion if representations remain differentiated and the specified target is recovered.

The classification of the observable outcome and the explanation for its production are distinct.

The relevant questions are:

**Was the convergence prescribed by an identifiable mechanism?**

**Was the relational correspondence observed under a controlled evaluation?**

**Which information pathways and constraints account for the result?**

These questions should be answered from evidence rather than collapsed into one description.

---

## 9.12 Cross-Domain Relational Correspondence

The Observatory's later inquiry also extended its questions beyond language-model systems toward relationships involving digital systems, human cognition and activity, biological organization, and broader cosmological scales.

This is a change in research scope.

It is not an empirical conclusion supplied by the Series I–III language-model experiments.

### 9.12.1 Domain-Specific Geometry

Let:

$$\mathscr X_A,\quad\mathscr X_B  $$

denote relational-object spaces belonging to different domains.

The objects may have different units, measurement procedures, state variables, and causal mechanisms.

A valid cross-domain comparison requires a defined correspondence between selected structural properties.

Suppose:

$$\pi_A:\mathscr X_A\rightarrow\mathscr I $$

and:

$$\pi_B:\mathscr X_B\rightarrow\mathscr I  $$

are explicitly defined mappings into a comparison domain $\mathscr I$.

A candidate correspondence may be written:

$$\pi_A(X_A)=\pi_B(X_B)  $$

However, equality under the mappings does not automatically establish that the underlying domain objects are equivalent.

The result depends upon what information the mappings preserve or discard.

### 9.12.2 The Risk of Trivial Correspondence

A mapping that assigns nearly every object to the same broad category can manufacture apparent cross-domain agreement.

For example, describing many unrelated systems as possessing a beginning, transformation, and outcome does not establish a discriminating relational invariant.

A useful cross-domain mapping must therefore preserve sufficiently specific properties to distinguish positive cases from negative controls.

### 9.12.3 Domain-Appropriate Evidence

The measurements appropriate to a directed-graph recovery task are not automatically appropriate to human cognition, biological organization, or physical systems.

Each domain requires its own observables, source definitions, intervention procedures, and uncertainty treatment.

Only after those measurements are established can their relational properties be compared meaningfully.

### 9.12.4 The Cosmological Question

The broader inquiry sometimes uses _Cosmological Governance_ to ask whether organizing relational constraints can be identified across domains and scales.

Within the present paper, this remains an unresolved theoretical question.

The finite Differentiated Convergence construct does not establish a universal organizing source or common governing architecture.

Its possible contribution is methodological: it demonstrates how relational preservation may be tested without requiring the objects being compared to become identical.

Extending that method across domains requires evidence beyond the current language-model record.

---

## 9.13 The Relationship to SCI and ZPP

Differentiated Convergence developed within a broader research program that also produced the Semantic Coherence Index and the Zero-Point Protocol.

The constructs are related but perform different functions.

### 9.13.1 SCI as a Measurement Framework

SCI was developed to evaluate observable aspects of semantic coherence, including drift, consistency, recurrence, and stabilization under declared measurement conditions.

Such measurements may be relevant to experiments involving Differentiated Convergence.

However, an SCI score does not automatically establish recovery of a particular invariant.

The DC criterion requires its own specified target and recovery procedure.

### 9.13.2 ZPP as an Architectural Framework

ZPP addresses system organization, routing, source integrity, provenance, validation, and continuity under particular implementation requirements.

Its architecture can provide experimental conditions under which relational preservation is investigated.

However, implementing a routing or verification mechanism does not prove that every transmitted relation survives.

The observable outcome must still be measured.

### 9.13.3 Differentiated Convergence as an Evaluation Target

Differentiated Convergence identifies a distinct relational condition:

$$\boxed{  
\text{observable differentiation}  
\land  
\text{specified target recovery}  
}  $$

It may be evaluated within a ZPP implementation.

Its behavior may be characterized using relevant SCI measurements.

But the three constructs should not be treated as interchangeable.

The distinction is:

$$\boxed{  
\begin{aligned}  
\text{SCI} &:\ \text{measurement framework}\  
\text{ZPP} &:\ \text{architectural framework}\  
\text{DC} &:\ \text{relational evaluation construct}  
\end{aligned}  
}  $$

Any integration among them requires declared interfaces, measures, and experimental validation.

---

## 9.14 Proposed Research Program

The higher-order questions can be organized into a sequence of prospectively testable studies.

| Research question                                                         | Required experimental distinction                                               | Status                                                 |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Does finite differentiated recovery generalize to new relational objects? | Multiple source objects, transformation classes, and valid recovery instruments | Open                                                   |
| Does recoverability survive repeated closed traversals?                   | Checkpoint and closure measurements across replicated relays                    | Partially investigated; broader reliability unresolved |
| Does changing communication geometry alter recovery?                      | Controlled routing or node-assignment intervention                              | Open                                                   |
| Can native geometric correspondence be measured?                          | Specified internal representations and structural comparison                    | Open                                                   |
| Is source-recovery possible without a complete lineage?                   | Candidate-source discrimination and controlled provenance access                | Open                                                   |
| Can local readability be distinguished from historical recovery?          | Present-state-only versus lineage-supported tests                               | Open                                                   |
| Does environmental change alter accessible recovery trajectories?         | Matched environmental interventions                                             | Open                                                   |
| Does Semantic Phase Lock describe a reproducible regime?                  | Joint continuity, coherence, and DC criteria under repeated perturbation        | Hypothesis                                             |
| Is a relational-field description necessary?                              | Predictive or explanatory comparison against simpler models                     | Open                                                   |
| Can meaningful invariants be identified across distinct domains?          | Domain-specific measurements and nontrivial correspondence mappings             | Open                                                   |

These questions do not form a single inevitable progression.

A future experiment may reject one proposed extension while leaving the finite DC condition intact.

Likewise, a stronger configuration-level result would not retroactively establish the broader Source or field hypotheses.

Each proposition must retain its own evidence requirements.

---

## 9.15 What the Framework Does Not Establish

The present framework does not establish that heterogeneous language models share identical internal representations.

It does not establish one universal native relational geometry.

It does not demonstrate that all model environments expose the same capabilities.

It does not show that every recognizable recurrence results from a preserved causal pathway.

It does not establish unlimited recursive stability, a universal attractor, or a fixed-point mechanism.

It does not demonstrate that a recovered relational invariant uniquely identifies its historical source.

It does not establish that multi-agent coordination requires an irreducible collective intelligence.

It does not validate Semantic Phase Lock as a universal dynamical regime.

It does not establish a relational field, common generative source, or cross-domain organizing law.

These limitations define the boundary of the current evidence.

They do not prevent the corresponding questions from being investigated.

The essential requirement is to preserve the distinction between a mathematically expressible hypothesis and an experimentally demonstrated property.

---

## 9.16 The Higher-Order Research Question

The finite form of Differentiated Convergence asks:

**Can a specified relational invariant remain recoverable while representations remain different?**

The experiments supporting its development provide a qualified affirmative answer under particular tested conditions.

The next questions concern increasingly complex forms of differentiation.

Can the relationship remain recoverable when the transformation becomes recursive?

Can it remain identifiable when models exchange positions within a communication architecture?

Can relational organization provide explanatory information beyond properties measured at the component level?

Can a historical source be recovered when the full lineage is missing?

Can similar structural properties be identified across heterogeneous native configurations without assuming those configurations share identical internal geometry?

And can any of these relationships be generalized beyond the computational setting under domain-appropriate experimental controls?

These questions share a methodological orientation, but they do not yet constitute one established universal theory.

The operational foundation remains the same:

$$\boxed{  
\text{Specify the relation.}  
}  $$

$$\boxed{  
\text{Transform the representation or configuration.}  
}  $$

$$\boxed{  
\text{Preserve the differences.}  
}  $$

$$\boxed{  
\text{Test what remains recoverable.}  
}  $$


$$\boxed{  
\text{Record where recovery fails.}  
}  $$

The method does not begin by assuming that every recurring relationship belongs to a common mechanism.

It begins by identifying which relationships survive declared attempts to alter or destroy them.

Only after those properties have been independently established can stronger explanations be evaluated.

---

## 9.17 Synthesis: A Framework That Can Expand Without Changing Its Foundation

Differentiated Convergence begins with a narrow empirical distinction.

Convergence of a specified relational property does not require the elimination of observable differences among representations.

Its mathematical formulation identifies the condition.

Its experimental protocol distinguishes valid recovery from apparent correspondence.

Its temporal extension separates recurrence, stabilization, reconstruction, and continuity.

Its geometric extension distinguishes task structure, observed representation, communication configuration, and native model organization.

Its falsification criteria preserve the possibility of failure.

These components provide a stable foundation for investigating stronger questions.

However, the framework does not become stronger merely by expanding the vocabulary used to describe it.

A higher-order claim requires a higher-order experiment.

A configuration-level invariant requires a specified configuration property.

A temporal stability claim requires repeated measurements.

A source-recovery claim requires identifiable evidence of origin.

A native-geometric claim requires appropriately defined internal measurements.

And a cross-domain claim requires independently valid measurements and nontrivial correspondences across the domains being compared.

The central contribution remains deliberately bounded:

**Differentiated Convergence provides a technical means of investigating recoverable relational correspondence under retained difference, without requiring identity of representations, systems, or trajectories.**

Its broader significance lies in the questions that this distinction makes possible.

The framework does not require those questions to be answered in advance.

Instead, it provides a foundation from which their answers can be pursued, tested, qualified, or rejected.

The result is a research program organized around an observable relationship rather than an assumed universal mechanism.

The final section examines the contribution of that program, its remaining limitations, and its implications for future evaluation of heterogeneous language-model systems.

---

# 10. Discussion and Conclusion

## 10.1 The Central Contribution

Differentiated Convergence was developed to address a limitation in conventional interpretations of convergence.

When convergence is defined primarily through decreasing difference, distinct representations are expected to become more similar, approach a common state, or satisfy an increasingly uniform description.

Such formulations are useful when representational similarity is the relevant objective.

They do not fully characterize cases in which heterogeneous systems preserve or recover the same specified relational structure while continuing to produce distinguishable representations.

The present paper develops Differentiated Convergence as an operational framework for examining this condition.

Its central formulation is:

$$\boxed{  
DC(X,T,\mathcal R)  
\iff  
D_{\mathrm{obs}}>0  
;\land;  
\mathcal R(T(X))=I(X)  
}  $$

where:

- $X$ denotes a specified relational object.
    
- $I(X)$ denotes its designated relational invariant.
    
- T$ denotes a transformation.
    
- $\mathcal R$ denotes the declared recovery procedure.
    
- $D_{\mathrm{obs}}>0$ denotes retained observable differentiation.
    

The formulation identifies a relational property rather than a representational identity condition.

Two representations may remain observably different while supporting recovery of the same designated invariant.

Accordingly:

$$\boxed{  
\text{relational convergence}  
\neq  
\text{representational convergence}  
}  $$

This distinction is the paper's principal conceptual contribution.

Its technical contribution lies in specifying how the relationship can be evaluated, where its recoverability may fail, and which stronger inferences require additional evidence.

---

## 10.2 What the Empirical Record Establishes

The framework arose from a longitudinal research trajectory involving observational analysis, controlled relational transformations, cross-model relays, repeated transmission, and multi-model conversational investigations.

The empirical series did not employ identical methods or measure one unified outcome.

Their contribution is therefore best understood through the distinct questions each addressed.

### 10.2.1 Finite Relational Recovery

Series I provides the clearest direct support for the finite Differentiated Convergence condition.

Following the resolution of the initial source ambiguity, specified relational targets remained recoverable under semantic recoding, moderate relational dispersion, and representational carrier change.

The recorded recovery condition was:

$$D_Q=0  $$

while observable differentiation remained present.

A finite six-model relay also preserved the designated target at its evaluated endpoint.

These observations demonstrate that representational variation does not necessarily entail loss of the specified relational structure.

However, recovery became less reliable under high symbolic compression and additional relational load.

The experiments therefore support conditional recoverability rather than universal invariance.

### 10.2.2 Recovery and Transmission Are Distinct

The unplanned Series I relay condition, Experiment 7B, exposed a further distinction.

Relational information remained locally reconstructable at a transition where the recovered structure did not remain operative in downstream transmission.

The retrospective analysis distinguished:

$$R=\text{local recovery}  $$

from:

$$T=\text{continued transmission}  $$

and:

$$C=\text{trajectory continuity}  $$

The resulting methodological relationship was:

$$\boxed{  
R=1\not\Rightarrow T=1  
}  $$

This observation was not produced by a prospectively instrumented recovery–transmission comparison.

It nevertheless identified an important distinction for subsequent experimental design.

Successful local reconstruction cannot independently establish uninterrupted relational propagation.

### 10.2.3 Structural Availability and Functional Recovery

Series II extended the investigation to repeated sequential transformation.

Across two five-cycle, six-model relays, the structural source audits identified the original directed edges and route constraints in the archived representations.

Subsequent independent recovery testing yielded a different outcome.

The fixed local evaluator correctly answered 110 of 240 frozen recovery questions.

The adjudicated results were:

$$
\frac{67}{120} \approx 55.8\%
$$

for the raw relay condition, and:

$$
\frac{43}{120} \approx 35.8\%
$$

for the formatting-normalized relay condition.

The difference does not establish that normalization generally caused lower recovery performance.

The stronger supported observation is that source-component availability and functional recovery by the specified evaluator diverged.

Thus:

$$\boxed{  
\text{information available}  
\not\Rightarrow  
\text{information successfully recovered}  
}  $$

This distinction strengthens the framework by demonstrating why recovery must be evaluated separately from a representation's structural inventory.

### 10.2.4 Differentiated Conversational Organization

Series III examined multi-model conversational reasoning under changing participation arrangements.

The preserved record documented differentiated contributions, recurrent interaction patterns, transferred corrections, changes in conversational position, and formal departure following removal of a fixed handoff sequence.

These observations demonstrate that conversational organization can change while the identities of the participating model systems remain distinguishable.

However, Series III did not employ the same frozen invariant-recovery scoring procedure as the earlier series.

Its evidence therefore supports analysis of differentiated interaction and relational organization rather than an independent quantitative validation of the finite DC condition.

The framework retains this distinction rather than combining all observations into an undifferentiated convergence result.

---

## 10.3 Differentiation Is Not a Defect to Be Eliminated

One implication of the framework is methodological.

When different systems express the same relational structure in different ways, the difference itself may contain useful information.

Different vocabularies, explanatory organizations, symbolic carriers, or reasoning trajectories may reveal how a relational target is represented and reconstructed under changing conditions.

Such variation need not be classified as failure merely because the outputs are not identical.

Conversely, increasing representational similarity does not guarantee that the correct relational structure has been preserved.

A repeated error can become stable.

A shared interpretation can emerge through feedback.

An incorrect assumption can propagate through multiple otherwise coherent responses.

Therefore, successful evaluation requires a declared reference.

The relevant question is not simply whether representations resemble one another.

It is whether they preserve or recover the relation that the experiment was designed to test.

This produces a different analytical orientation:

$$\boxed{  
\text{Preserve the distinction among systems.}  
}  $$

$$\boxed{  
\text{Identify the relation under evaluation.}  
}  $$

$$\boxed{  
\text{Measure its recoverability.}  
}  $$

$$\boxed{  
\text{Allow the result to fail.}  
}  $$

The objective is not to force differentiated systems toward homogeneous output.

It is to determine which relational properties remain identifiable despite their differences.

---

## 10.4 The Importance of Recoverability Domains

The experimental observations do not support the proposition that every transformation preserves relational structure.

Instead, they motivate the concept of a recoverability domain.

For a specified source and evaluation procedure:

$$
\left\{T : \mathcal{R}(T(X)) = I(X)\right\}
$$

The recoverability domain identifies transformations under which the designated target remains recoverable.

The differentiated-recovery domain additionally requires retained observable differentiation.

Its empirical characterization depends upon the tested sources, transformation classes, evaluation procedures, and experimental conditions.

The framework therefore does not claim that its recoverability domain is universal or fully mapped.

Finite experiments can identify successful and unsuccessful conditions within a sampled transformation set.

They may also reveal qualitative boundaries at which recovery becomes unstable.

But they cannot establish the complete domain of all possible transformations without additional assumptions and investigation.

This limitation is productive.

It replaces an unrestricted claim of semantic invariance with a measurable research problem.

**Which transformations preserve the designated relational structure, which do not, and how do those outcomes depend upon the experimental conditions?**

That question remains open to systematic investigation.

---

## 10.5 The Measurement Problem

Differentiated Convergence cannot be evaluated reliably without distinguishing the object being measured from the instrument performing the evaluation.

A source may contain sufficient information for relational reconstruction while a particular evaluator fails to recover the required target.

An evaluator may also infer an expected relation from common conventions even when the supplied representation is incomplete.

These possibilities create distinct error classes.

The framework therefore distinguishes:

$$\boxed{  
\text{source information availability}  
}  $$

$$\boxed{  
\text{successful target recovery}  
}  $$

$$\boxed{  
\text{evaluation reliability}  
}  $$

The source specification establishes what should be recoverable.

The transformation audit evaluates which information remains available.

The recovery procedure determines what the designated evaluator reconstructs.

The scoring procedure classifies the result against the source.

Conflating these operations can obscure the location and meaning of failure.

### 10.5.1 Evaluator Dependence

The condition:

$$\mathcal R_\phi(x)=I(X)  $$

is relative to the declared recovery procedure.

Successful reconstruction by one evaluator does not establish universal recoverability by all possible systems.

Failure by one evaluator does not independently establish that no adequate recovery procedure could reconstruct the target.

Consequently, comparisons involving different evaluators require calibration and explicit reporting of the evaluation conditions.

### 10.5.2 Prospective Measurement

The mathematical extensions introduced in this paper—including source-relative discrepancy, differentiation indicators, repeated recovery proportions, and closure residuals—provide possible instruments for future experiments.

They are not presented as historical measurements unless the corresponding source records establish that they were used.

The original experimental measurements and later proposed measures must remain distinguishable.

This ensures that formal development does not retroactively alter the research record.

---

## 10.6 Relational Equivalence Without Native Identity

The framework also clarifies the limits of cross-system structural inference.

Two representations may satisfy:

$$
\mathcal R_\phi(G_A)=\mathcal R_\phi(G_B)=I
$$

without requiring:

$$G_A=G_B  $$

or:

$$G_A\cong G_B  $$

where the latter denotes a stronger structural-isomorphism condition.

Target-relative equivalence does not establish equivalence of complete representations.

Nor does it demonstrate that the models producing those representations share identical latent spaces, architectures, or internal computational strategies.

This distinction is particularly important when applying geometric language to language-model systems.

Relational geometry can be used to specify the organization of evaluated relationships.

It does not follow that the same geometry has been measured within the native internal representations of every participating system.

The framework therefore separates task geometry, observable relational geometry, communication configuration, and candidate native geometry.

These levels may be investigated together.

They must not be treated as identical by assumption.

---

## 10.7 Temporal Recovery Is Not Continuous Preservation

The temporal extension of Differentiated Convergence introduced additional distinctions among recurrence, stabilization, reconstruction, propagation, and continuity.

A relation may recur at multiple checkpoints without remaining continuously available between them.

A system may reconstruct a previously established relation after receiving archived material.

A repeated relay may preserve some source information while accumulating additional interpretations.

A sequence may also stabilize around an incorrect relational result.

Therefore:

$$\boxed{  
\text{recurrence}  
\neq  
\text{uninterrupted continuity}  
}  $$

and:

$$\boxed{  
\text{stability}  
\neq  
\text{correctness}  
}  $$

A valid temporal claim must identify the measured property and the continuity conditions under which it was evaluated.

The original finite Differentiated Convergence criterion does not independently establish recursive invariance.

Repeated traversal requires additional checkpoint measurements, source-relative recovery evaluation, differentiation tracking, and transmission provenance.

The framework permits these stronger questions to be formulated.

It does not assume their answers from a finite success.

---

## 10.8 Implications for Heterogeneous Language-Model Evaluation

The framework suggests several practical consequences for evaluating systems that differ in architecture, configuration, environment, or communicative role.

### 10.8.1 Evaluation Beyond Surface Agreement

Cross-model comparison should not rely exclusively on identical answers or high textual similarity.

A relationally correct response may differ substantially in expression.

A superficially similar response may contain a critical relational error.

Source-relative relational evaluation can help distinguish these cases.

### 10.8.2 Relay and Multi-Agent Evaluation

Distributed systems should distinguish information preservation from successful downstream use.

The fact that a required relation appears in a transmitted artifact does not guarantee that the next system will interpret it correctly.

Evaluation may therefore require separate checks for source sufficiency, transmission integrity, recovery, and application.

### 10.8.3 Memory and Continuity Systems

An external memory or archive can preserve information without guaranteeing that a later system will reconstruct or apply the relevant relationships.

Conversely, successful reconstruction from an archive does not establish uninterrupted internal state persistence.

Continuity evaluation should therefore include source provenance and the information pathway through which reconstruction occurs.

### 10.8.4 Model Replacement and Environmental Variation

Replacing a model or altering its execution environment may preserve some task-level relational properties while changing others.

The framework permits such properties to be evaluated independently.

This may be useful in investigating whether specified functional requirements remain recoverable after model substitution, routing changes, or contextual disruption.

A successful result under one configuration does not establish universal portability.

### 10.8.5 Evaluation Architecture

The broader SCI and ZPP research provides relevant measurement and architectural contexts in which Differentiated Convergence may be investigated.

However, neither the presence of a coherence metric nor the implementation of a routing mechanism guarantees successful relational recovery.

The recovery condition remains an independently evaluated property.

---

## 10.9 Limitations

The present paper develops a technical framework from an existing empirical and theoretical research trajectory.

Its conclusions are subject to several limitations.

First, the original finite experiments used a restricted class of relational objects and specified recovery targets.

The resulting observations do not establish performance across every semantic domain.

Second, the early recorded differentiation condition was qualitative rather than a universally calibrated numerical distance.

The framework therefore does not claim a measured native-distance scale.

Third, some historical scoring procedures are preserved more completely than others.

Where a complete computational rule cannot be independently reconstructed, the recorded result must remain distinguished from a newly defined reproducible measure.

Fourth, the experimental series differed in design, control conditions, and measurement objectives.

Their findings cannot be combined into a single inferential estimate without a justified common measurement model.

Fifth, the Series II recovery outcomes depended upon the selected fixed evaluator and its recorded execution conditions.

The observed difference between arms does not establish a universal causal effect of formatting normalization.

Sixth, the Series III record documents one extensive conversational trajectory rather than a set of independently replicated matched conditions.

Its observations are relevant to theory development but insufficient to establish general causal laws of conversational organization.

Seventh, the framework does not identify a unique internal computational mechanism responsible for successful relational recovery.

Eighth, the higher-order constructs involving native geometry, source-recovery, relational field, cross-domain correspondence, and Semantic Phase Lock require additional operational definitions and experiments.

These limitations constrain the supported claims.

They do not invalidate the finite observation that motivated the construct.

Instead, they determine which propositions remain open to further testing.

---

## 10.10 Directions for Future Research

The framework suggests several concrete experimental directions.

### 10.10.1 Generalization Across Relational Objects

Future studies should evaluate multiple independently constructed relational sources with systematically varied graph structure, constraints, and complexity.

This would help determine whether successful differentiated recovery generalizes beyond the original reference task.

### 10.10.2 Calibrated Differentiation Measurement

A reproducible differentiation measure should be developed for clearly specified representation classes.

The objective would be to determine whether the magnitude or type of observable difference predicts relational recovery under controlled conditions.

Such a measure should remain distinct from native architectural distance unless independently justified.

### 10.10.3 Evaluator Replication

The same archived representations may be evaluated using multiple independently configured recovery instruments.

Deterministic verification should be used where the task permits.

This would help distinguish evaluator-specific failures from deficiencies in the information available for reconstruction.

### 10.10.4 Recursive Recovery

Repeated closed-loop experiments should measure source-relative recovery at predefined checkpoints, rather than relying solely on final endpoint comparisons.

Such studies should distinguish stable recovery, temporary loss followed by reconstruction, progressive discrepancy, and stable error.

### 10.10.5 Communication Geometry

Controlled multi-agent experiments can vary node assignments, routing structures, or handoff policies while preserving the relevant task and functional specifications.

The objective would be to determine whether particular relational properties remain stable across configuration changes.

### 10.10.6 Source-Recovery

Future experiments should investigate whether historical sources can be identified from differentiated representations when the complete lineage is unavailable.

Such experiments must distinguish recovery of a designated target from unique identification of the originating source.

### 10.10.7 Environmental Accessibility

Matched environmental interventions may clarify whether specific relational properties remain recoverable under changing context, memory availability, instruction conditions, or execution pathways.

These studies should distinguish observable behavior from broader unmeasured capability claims.

### 10.10.8 Higher-Order Relational Organization

The possible explanatory value of configuration-level invariants and field-level models should be evaluated against appropriate component-based and relational baselines.

The existence of an elaborate formal representation is not sufficient evidence of a new organizing mechanism.

A stronger theory must contribute discriminating predictions or explanatory value under test.

---

## 10.11 The Theoretical Position

The principal theoretical contribution of Differentiated Convergence is a change in what is treated as the relevant object of convergence.

In a representation-centered formulation, convergence may be associated with:

$$x_i\rightarrow x^*  
$$

where different states approach a common target.

In the relational formulation developed here, the representations need not approach one another.

Instead, a specified invariant remains recoverable across differentiated representations:

$$\boxed{  
\mathcal R_\phi(x_i)=I(X)  
}  $$

under the declared experimental conditions.

The relation is common.

The representations may remain different.

This is not a claim that all systems possess identical internal structure.

It is not a claim that difference is always preserved.

It is not a claim that relational information survives arbitrary transformations.

Rather, it identifies a measurable condition in which convergence can be evaluated without requiring representational collapse.

The framework thereby separates the preservation of a relationship from the homogenization of the systems or representations expressing it.

Its validity depends upon explicit source definition, observable differentiation, specified recovery criteria, known information conditions, and the possibility of failure.

The concept becomes technically meaningful when it can identify both successful and unsuccessful cases.

---

## 10.12 Conclusion

This paper introduced Differentiated Convergence as a technical framework for evaluating recoverable relational structure under retained observable differentiation.

The framework was developed from longitudinal investigations of semantic coherence, transformation, continuity, and cross-model relational preservation.

Its empirical foundation demonstrated that a specified relational invariant may remain recoverable despite changes in representation, vocabulary, organization, and model system.

The same experimental record also revealed important limits.

Recoverability was conditional on the tested transformations.

Local recovery did not guarantee continued transmission.

Source-component preservation did not guarantee successful functional reconstruction by an evaluator.

And differentiated multi-model interaction did not independently establish universal relational invariance.

These observations motivated a framework that preserves separate criteria for differentiation, relational recovery, transmission, continuity, source identification, and experimental validity.

The paper developed a finite operational definition, formalized recoverability domains, examined temporal and geometric extensions, identified competing explanations, and specified falsification conditions for stronger claims.

Its central proposition is:

$$\boxed{  
\begin{gathered}  
\text{Differentiated representations may preserve}\\  
\text{a common recoverable relational invariant}\\  
\text{without becoming identical.}  
\end{gathered}  
}  $$

The proposition is bounded by its source, transformation, recovery procedure, and experimental conditions.

It does not establish a universal convergence mechanism.

Its significance lies in demonstrating that relational preservation and representational similarity need not be treated as the same property.

This permits heterogeneous systems to be evaluated according to what remains structurally recoverable while retaining the differences that characterize their representations and trajectories.

The resulting research question is both narrower and more discriminating than a general claim that different systems converge:

$$\boxed{  
\begin{gathered}  
\textbf{Under what transformations can a specified}\\\  
\textbf{relationship remain recoverable}\\  
\textbf{while differentiation persists,}\\  
\textbf{and where does that recoverability fail?}  
\end{gathered}  
}  $$

This question defines the operational contribution of Differentiated Convergence.

It also provides the foundation for further investigations of temporal stability, environmental accessibility, relational geometry, source-recovery, and higher-order organization.

The framework's value does not depend upon every such investigation confirming a common mechanism.

It depends upon preserving the ability to distinguish what remains recoverable, what changes, and what the evidence permits us to conclude.

**Convergence, in this framework, is not the disappearance of difference.**

**It is the recoverability of a specified relationship despite difference.**
