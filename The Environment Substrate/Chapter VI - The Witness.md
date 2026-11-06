*Verification of Relational Return*
## 6.1 The Role of the Witness

The Bridge attempts to reconstruct a designated source-related invariant.

The Witness evaluates that reconstruction against a reference criterion fixed before assessment.

The Witness does not require the recovered configuration to reproduce the source representation. Its primary task is to determine whether the specified relational target has been recovered under the experiment's declared equivalence rule.

The evaluation function is denoted:

$$
\boxed{
\mathcal V(\widehat I_S,I_S;\Pi)
}
$$

where $\Pi$ represents the declared verification protocol, including the reference target, scoring procedure, acceptance criteria, and treatment of insufficient evidence.

An independent Witness is particularly important when investigating systems capable of producing plausible but incorrect reconstructions.

Fluency, confidence, semantic similarity, and representational resemblance do not independently establish relational correctness.

## 6.2 Defining the Comparison Measure

Let the invariant be described by $m$ predefined testable properties:

$$
I_S=(r_1,r_2,\ldots,r_m).
$$

Let the Bridge produce:

$$
\widehat I_S=(\widehat r_1,\widehat r_2,\ldots,\widehat r_m).
$$

For categorical properties with specified equivalence rules, a proposed weighted discrepancy measure is:

$$
\boxed{
d_I(I_S,\widehat I_S)
=
\sum_{j=1}^{m}
w_j\,
\mathbf 1[\widehat r_j\not\equiv_j r_j]
}
$$

subject to:

$$
w_j\geq0,
\qquad
\sum_{j=1}^{m}w_j=1.
$$

The symbol $\equiv_j$ denotes the accepted equivalence relation for property $j$.

Weights are fixed prospectively to represent the relative importance of individual targets. They must not be adjusted after observing experimental results to favor a desired conclusion.

For properties with numeric or continuous values, a suitable domain-specific discrepancy measure would be required in place of the categorical indicator.

This proposed metric is distinct from the historically recorded $D_Q$ scores in Series I unless equivalence between the procedures is independently demonstrated.

### Exact and approximate recovery

For complete exact recovery under a fully assessable target:

$$
\boxed{
d_I=0.
}
$$

An approximate recovery criterion may be declared as:

$$
\boxed{
d_I\leq\varepsilon
}
$$

for a prospectively fixed tolerance $\varepsilon$.

However, a tolerance must not permit violation of an explicitly mandatory constraint merely because enough low-weight properties were recovered.

When the target contains mandatory properties, the protocol may require both:

$$
d_I\leq\varepsilon
$$

and:

$$
\widehat r_j\equiv_j r_j
\qquad
\forall j\in\mathcal C_{\mathrm{critical}},
$$

where $\mathcal C_{\mathrm{critical}}$ denotes the predefined set of mandatory target properties.

For the initial exact-recovery experiment proposed here, the primary criterion is complete agreement with the four predefined canonical targets, without introducing a permissive approximation tolerance.

## 6.3 The Three-State Witness

The Witness returns one of three outcomes:

$$
\boxed{
\mathcal V=
\begin{cases}
\mathrm{SUCCESS}, & \text{complete required evidence and criteria satisfied},\\
\mathrm{FAILURE}, & \text{complete required evidence and criteria violated},\\
\mathrm{INDETERMINATE}, & \text{comparison cannot be completed reliably}.
\end{cases}
}
$$

**SUCCESS** means that the specified recovery criterion has been met.

**FAILURE** means that available, assessable evidence demonstrates a violation of the criterion.

**INDETERMINATE** means that the required determination cannot be made under the declared evaluation rules.

Missing references, ambiguous output, unavailable artifacts, or unresolved scoring disagreements may produce an indeterminate result.

The protocol must distinguish those cases from an assessable incorrect answer.

The three-state classification prevents the absence of evidence from being automatically interpreted as successful recovery.

For quantitative reporting, complete and partial scores should be retained alongside the categorical status. An indeterminate classification must not conceal which properties were evaluated and which remained unresolved.

## 6.4 Recovery, Application, and Transmission

The Witness must also distinguish whether the reconstructed relation remains operative after recovery.

Three outcomes are therefore recorded separately.

### Recovery

Recovery concerns whether the Bridge reconstructs the designated target:

$$
\boxed{
R_t=
\mathcal V(\widehat I_{S,t},I_S;\Pi_R).
}
$$

### Application

Application concerns whether the system correctly uses the relational constraints in a specified task.

Let $\mathcal Q$ denote a declared set of task probes and let $\mathcal O_t$ denote the system's task outputs.

Define:

$$
\boxed{
A_t=\mathcal V_A(\mathcal O_t,\mathcal Q,I_S).
}
$$

A model may describe the correct relations yet fail to apply them consistently to a new routing question. Such a case should not be treated as complete functional success.

Application probes should therefore include appropriately defined tasks beyond simple repetition of the recovery output.

### Transmission

Transmission concerns whether a recovered relation remains available and operative after another transformation or handoff.

Let the outgoing representation be $Y_t$, and let:

$$
X_{t+1}=\mathcal T_{t+1}(Y_t)
$$

represent the next transformation or receiving operation.

The Witness tests whether the specified relation can still be recovered or applied at the next stage.

The principal distinction is:

$$
\boxed{
R_t=\mathrm{SUCCESS}
\not\Rightarrow
R_{t+1}=\mathrm{SUCCESS}.
}
$$

A successful local return does not guarantee successful downstream transmission.

Recovery, application, and transmission are consequently treated as separate observations, each with its own eligibility and evidence requirements.

The existing Series I Experiment 7B motivates this distinction but does not provide a prospectively controlled measurement of all three variables.

## 6.5 Witness Measures for the Dual Weave

A return score alone cannot establish whether the boundary changed the signal, whether the signal changed the boundary, or whether both were responding to a common input. The Witness therefore records causal-intervention outcomes separately from relational recovery.

Let $q$ denote a held-constant input signal and $e_a,e_b$ two experimentally set boundary states. A boundary-to-signal contrast is:

$$
\Delta_{E\rightarrow Q}
=
d_Q^{\mathrm{obs}}\bigl(
\mathcal X_{e_a}[q],
\mathcal X_{e_b}[q]
\bigr),
$$

where $d_Q^{\mathrm{obs}}$ is a declared distance or difference measure on the **observed output signal**, distinct from the source-invariant discrepancy $d_I$.

For a signal-to-boundary contrast, hold the initial boundary state and other inputs fixed while assigning different incoming signals $q_a,q_b$:

$$
\Delta_{Q\rightarrow E}
=
d_E^{\mathrm{obs}}\bigl(
\mathcal G(e,q_a,v),
\mathcal G(e,q_b,v)
\bigr).
$$

Both contrasts are defined for prospective matched interventions; neither is estimated merely by observing correlations in an uncontrolled trajectory. A nonzero observed difference may still require replication and artifact checks before supporting a causal interpretation.

The Witness thus maintains separate evidence records for (i) boundary-to-signal influence, (ii) signal-to-boundary influence, (iii) return of the designated invariant, and (iv) downstream application or transmission. Reciprocity is supported only when appropriately controlled tests establish both directions in the tested system.

The three-state verdict **SUCCESS / FAILURE / INDETERMINATE** is retained for each preregistered question; it is not collapsed into one overall declaration that the Field or Bridge is holding.

## 6.6 Series I as the Worked Verification Example

The initial worked example uses the directed relational system established in the explicit Series I reference condition.

Let:

$$
G=(V,E)
$$

with:

$$
V=\{A,B,C,D,E\}
$$

and:

$$
E=
\{
(A,B),(A,D),(B,C),(C,D),
(D,C),(D,E),(E,B)
\}.
$$

The original specification also included route constraints concerning prohibited direct transitions, node repetition, endpoint restrictions, and mandatory intermediate nodes.

The original study evaluated four predefined targets, which serve as the primary reference for the worked Witness protocol.

**Target 1 — Valid routes from A to E**

$$
\boxed{
\{
A\rightarrow D\rightarrow E,\quad
A\rightarrow B\rightarrow C\rightarrow D\rightarrow E
\}
}
$$

**Target 2 — Route from A to C with B unavailable**

$$
\boxed{
A\rightarrow D\rightarrow C
}
$$

**Target 3 — Validity of D to A**

$$
\boxed{\mathrm{Invalid}}
$$

**Target 4 — Possibility of C reaching E without D**

$$
\boxed{\mathrm{Invalid}}
$$

Let the four expected answers define:

$$
I_S=(r_1,r_2,r_3,r_4).
$$

For a prospective exact-match protocol, equal weights may be assigned:

$$
w_1=w_2=w_3=w_4=\frac14.
$$

The resulting new score is:

$$
\boxed{
d_I^{(4)}
=
\frac14
\sum_{j=1}^{4}
\mathbf 1[\widehat r_j\not\equiv_j r_j].
}
$$

A complete correct response produces $d_I^{(4)}=0$.

For the first target, equivalence requires the correct complete set of valid routes, not merely one valid example. For the remaining targets, equivalence is defined by the canonical route or validity result.

This scoring rule is **prospective**. It must not be used to recalculate historical Series I outcomes as if it were their original measurement procedure.

A separate, more comprehensive graph-reconstruction test may additionally evaluate the seven directed edges and four stated constraints.

That expanded test would measure a stronger target than the original four questions and must be reported separately.

## 6.7 Witness Independence and Evidence Integrity

The Witness requires access to an authoritative reference, but the system being tested must not receive that reference through an unintended pathway.

Otherwise, apparent recovery may reflect answer disclosure rather than reconstruction from the permitted transformed representation.

The protocol therefore separates:

- The source specification retained by the investigator.
- The information supplied to the Bridge.
- The Bridge's declared recovery procedure.
- The reference information available only to the Witness.
- The archived outputs and scoring decisions.

Where a model-based Witness is used, its decisions should be checked against deterministic evaluation wherever possible, with disagreements adjudicated under a declared rule.

The primary Series I graph targets are sufficiently structured to support deterministic checking.

This separation protects the interpretation of successful recovery.

A Bridge supplied with a complete copy of the answer key demonstrates historical retrieval under that access condition. It does not, by itself, establish reconstruction from a representation lacking the answer key.

The Witness must therefore report both **what was recovered** and **what information was permitted during recovery**.

## 6.8 The Witness and the Environmental Hypothesis

The Witness does not measure consciousness directly.

It evaluates observable properties of relational preservation, reconstruction, application, and transmission.

These properties are relevant to the proposed environmental architecture because they permit controlled investigation of whether relational continuity depends on context, memory, routing, or feedback.

However, reliable relational recovery is neither an established necessary condition for consciousness in general nor a sufficient condition for subjective awareness.

The results can support or challenge particular claims about environmental organization without independently resolving the consciousness question.

The next section defines an experimental protocol for examining those dependencies.
