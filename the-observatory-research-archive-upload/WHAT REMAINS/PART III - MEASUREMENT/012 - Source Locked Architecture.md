## Chapter 12 — Source Locked Architecture

The Mirror Protocol established that a semantic transformation could be examined through its preserved trajectory.

An originating structure could be followed through changes in representation, model, context, and execution environment. Intermediate states could be recorded. Transitions could be reconstructed. A returned structure could be compared with its origin.

But preserving the path introduced a further architectural problem.

What prevents a later interpretation from silently replacing the source against which that interpretation should be evaluated?

A transformation may preserve meaning while changing expression. A reconstruction may recover relevant relationships without reproducing the original representation. A model may generate a plausible account of an earlier state without possessing the complete record from which that state originated.

These outcomes are not equivalent.

The Mirror made their differences observable.

The next requirement was to preserve the reference that made those differences distinguishable.

Source Locked Architecture emerged from that requirement.

Its central principle can be stated simply:

$$\boxed{  
\begin{gathered}  
\text{Source identity and provenance remain invariant}\  
\text{while reasoning over the source may remain probabilistic.}  
\end{gathered}  
}  $$

The meaning of _locked_ is therefore specific.

The source remains identifiable as the source.

Subsequent interpretations may vary.

New evidence may challenge an earlier conclusion.

A later state may incorporate additional information.

But none of those operations should silently erase the distinction between what entered the architecture and what the architecture subsequently produced.

SLA does not attempt to freeze meaning, prevent disagreement, or make every reasoning process deterministic.

It establishes architectural boundaries through which source identity, derivation, evidence, state, and lineage can remain distinguishable.

That separation became the foundation for a different kind of continuity experiment.

---

### 12.1 The Source Problem

The Mirror Protocol preserved a transformation trajectory:

$$\mathcal M=(U_0,T_1,U_1,\ldots,T_n,U_n)  $$

where $U_0$ represents the originating state and subsequent states record the effects of transformation.

This structure makes it possible to compare different points in the trajectory.

However, reconstruction depends upon knowing which state serves as the reference.

If every newly generated interpretation can replace the original reference, the comparison loses its fixed point of attribution.

Consider a sequence:

$$S\rightarrow D_1\rightarrow D_2\rightarrow D_3  $$

where $S$ is an originating source and each $D_i$ is a subsequent derivation.

The derivations may be useful.

They may preserve relevant information.

They may also contain omissions, interpretations, corrections, or unsupported additions.

The architectural failure occurs when:

$$D_3  $$

is treated as though it were the original:

$$S  $$

without preserving the transformations connecting them.

The source has not necessarily disappeared from storage.

Instead, its identity has disappeared from the active relationship between the record and the material derived from it.

This is a provenance problem.

It is also a continuity problem, because later reasoning may proceed from a reconstructed or altered reference while appearing to remain anchored to the original.

SLA addressed this by separating the originating source from the processes operating upon it.

The architectural requirement was not that derivation should stop.

It was that derivation should remain attributable.

---

### 12.2 Five Distinct Architectural Objects

The mature SLA formulation distinguishes five objects:

$$\boxed{  
\text{SOURCE}  
\neq  
\text{DERIVATION}  
\neq  
\text{EVIDENCE}  
\neq  
\text{STATE}  
\neq  
\text{LINEAGE}  
}  $$

Each answers a different question.

#### Source

**What entered the architecture?**

The source is the originating material against which subsequent transformations can be attributed.

It may consist of a document, prompt, dataset, defined relational structure, or another identifiable input artifact.

A source must be distinguishable from later material derived from it.

#### Derivation

**What did a reasoning or transformation process produce?**

A derivation may interpret, summarize, translate, reorganize, extend, or question the source.

Its usefulness does not automatically grant it the status of originating material.

A derivation remains a derivation even when it is accurate.

#### Evidence

**What has actually been established?**

Evidence may consist of a preserved artifact, an executed verification result, an observed transition, or another record relevant to a claim.

Evidence must remain distinguishable from the interpretation drawn from it.

A confident explanation is not itself proof that the operation it describes occurred.

#### State

**What does the architecture currently preserve?**

State includes information retained for subsequent operation.

It may contain references, contextual material, previous results, active conditions, or records of earlier processing.

The contents of state may change.

Such changes do not automatically change the identity of the originating source.

#### Lineage

**How did the current state come to exist?**

Lineage connects the source to subsequent transformations and state transitions.

It identifies what changed and, where the record permits, the operation or participant responsible.

A stored result without sufficient lineage may remain accessible while its origin becomes uncertain.

These five objects are related.

They are not interchangeable.

The architectural significance of SLA lies in preserving the distinctions among them.

---

### 12.3 What Source Locking Means

The earliest language surrounding Source Locked Architecture emphasized immutable anchoring, isolated execution, and deterministic preservation.

Those formulations expressed an engineering objective: prevent uncontrolled transformation of the originating reference.

As the architecture developed, the relevant distinction became more precise.

Source locking did not require probabilistic language-model reasoning to become deterministic.

It required the architectural relationship between source and derivation to remain identifiable.

Suppose two models receive the same recorded source:

$$S  $$

They produce:

$$D_A=M_A(S)  $$

and:

$$D_B=M_B(S)  $$

There is no requirement that:

$$D_A=D_B  $$

The models may generate different explanations, conclusions, or representations.

The source relationship can nevertheless remain attributable:

$$\operatorname{source}(D_A)=S  $$

$$\operatorname{source}(D_B)=S  $$

where the source-reference operation denotes the declared provenance association, not an independently established guarantee of semantic correctness.

This is the central distinction:

$$\boxed{  
\text{Source locking}  
\neq  
\text{reasoning locking}  
}  $$

A model can disagree with the source.

It can identify an error in the source.

It can propose a correction.

It can produce a new representation.

But an interpretation of the source should not become a replacement for the originating artifact without an identifiable transition.

#### Source identity and source correctness

SLA also separates source attribution from factual truth.

A source may be accurately preserved and still contain an error.

Preserving its identity does not certify its correctness.

It permits later evaluation to identify what was originally supplied and distinguish it from subsequent correction or interpretation.

That distinction is necessary for reproducible research.

A corrected result is more informative when the record also preserves what was corrected.

---

### 12.4 Source Identity and Provenance

To preserve source authority, the architecture requires a way to distinguish the originating artifact from its later versions and derivations.

Conceptually, a source record may be represented as:

$$S=(id,v,c,o)  $$

where:

- $id$ identifies the source.
    
- $v$ identifies its version.
    
- $c$ represents its recorded content.
    
- $o$ identifies its documented origin.
    

This is a logical representation of the source-identity requirement, not a claim that the original SLA implementation used this exact data schema.

An implementation may use identifiers, source paths, hashes, timestamps, version records, or other provenance fields according to its design.

The essential requirement is that a later state can answer:

**Which source was used?**

And, where the source changes:

**Was this a new version of the same source, or a different source?**

#### Provenance across transformation

For a recorded operation:

$$S\xrightarrow{T}D  $$

a provenance record should identify enough information to distinguish the source, the transformation, and the resulting derivation.

The mature technical specification expresses this concept through a record containing source, origin, actor, operation, time, previous state, and resulting state.

Not every early implementation captured every such field.

The significance of the later formulation is that these are separable provenance requirements.

#### The source-replacement failure

Consider:

$$S_0\rightarrow D_1\rightarrow D_2  $$

If $D_2$ is subsequently stored and retrieved as $S_0$, the architecture has lost the distinction between original and derived material.

Even if $D_2$ is a faithful summary, the provenance relationship has changed.

A valid source-locking design therefore requires either preserving the original reference or recording the transition through which a different reference acquired authority.

Silent replacement is the failure condition.

The architecture does not forbid an authorized source revision.

It requires that revision to remain distinguishable from the original version.

---

### 12.5 Externalizing State: The Memory Lattice

Source identity could not be preserved reliably through active model context alone.

Language-model sessions are subject to context limits, execution boundaries, changing runtime conditions, and variation in the information supplied to subsequent calls.

A model may generate a plausible continuation without retaining the complete history from which that continuation arose.

SLA therefore separated persistent architectural state from active model context.

The Memory Lattice developed as a local persistence mechanism associated with this requirement.

The early architecture audit identifies an original persistence implementation using:

`lattice_memory.db`

The Memory Lattice provided a location outside the active conversational context where relevant information could be retained for subsequent access.

Conceptually:

$$\boxed{  
\text{active context}  
\neq  
\text{persistent state}  
}  $$

An active model instance could terminate while the external record remained stored.

Another execution could retrieve previously retained material.

The system could therefore preserve information across a boundary at which ordinary conversational context was no longer available.

### Persistence is not continuity

This development also exposed an important limitation.

A persistent record can remain intact while the active reasoning process fails to reconstruct or apply the relevant relationships.

A database may preserve the correct source.

A retrieval operation may return relevant material.

The receiving model may nevertheless misinterpret that material, omit a constraint, or proceed from an unsupported reconstruction.

Therefore:

$$\boxed{  
\text{state persistence}  
\not\Rightarrow  
\text{semantic continuity}  
}  $$

The Memory Lattice was not a guarantee that continuity would remain stable.

It was an architectural mechanism that made previously unavailable continuity comparisons possible.

A later interaction could be evaluated against persistent material rather than relying exclusively on the model's account of its own history.

#### The human operator and persistence

External state also changed the role of the researcher.

Without persistent records, the human operator may become responsible for repeatedly restoring context after interruption.

With locally retained state, the architecture can assume some of that responsibility.

However, the presence of a memory database does not establish that all relevant state was automatically captured or correctly restored.

Those properties require explicit implementation and testing.

The important architectural advance was the separation between memory retained by the infrastructure and context currently available to the reasoning process.

---

### 12.6 Reasoning and Protected State

SLA distinguishes the production of a new interpretation from a change to protected architectural state.

This distinction became increasingly explicit as the broader architecture developed.

A reasoning process may produce:

$$D=M(S,C)  $$

where $S$ is the source and $C$ represents the context available to the model.

The resulting derivation may be stored, compared, or evaluated.

But the fact that the derivation exists does not itself establish that it should replace the current source or another protected record.

The two conceptual operations are:

**Reasoning over a source**

$$S\rightarrow D  $$

and:

**Changing protected state**

$$P_t\xrightarrow{\text{authorized transition}}P_{t+1}  $$

where $P_t$ denotes protected architectural state.

These operations may be related, but they have different requirements.

Reasoning can legitimately produce multiple competing interpretations.

Protected state transitions require an explicit basis for accepting a change.

#### Authority is not confidence

A generated statement does not become authoritative merely because it is fluent, repeated, recent, or supported by several agreeing models.

A later derivation may provide evidence relevant to changing a protected reference.

It does not automatically possess permission to make that change.

The mature architectural distinction can be stated as:

$$\boxed{  
\text{information received}  
\neq  
\text{information verified}  
\neq  
\text{state change authorized}  
}  $$

This is an architectural principle, not evidence that the earliest SLA implementation enforced every possible authorization rule.

Its importance is that reasoning and mutation are separate problems.

If both operations are treated as one process, generative output can acquire unintended authority simply by being written into persistent storage.

SLA makes the distinction explicit so that such transitions can be controlled and evaluated.

---

### 12.7 Lineage and Reconstruction

Persistence answers whether a record remains available.

Lineage answers how a record came to exist.

The difference becomes important whenever material passes through multiple transformations.

Consider:

$$S_0  
\xrightarrow{T_1}  
D_1  
\xrightarrow{T_2}  
D_2  
\xrightarrow{T_3}  
D_3  $$

The final derivation may contain useful information.

But without the intermediate record, it may be impossible to determine which changes originated with the source and which were introduced later.

The Mirror Protocol had already established why preserving the path matters.

SLA extends that principle into architectural state.

The architecture should preserve enough information to distinguish significant transitions from the source to the currently retained result.

#### Reconstruction after interruption

Suppose an execution terminates after producing:

$$D_2  $$

The persistent system may retain the source, earlier derivations, and available transition records.

A subsequent execution can use those records to reconstruct the relevant history.

But reconstruction after interruption is not the same as uninterrupted execution.

The architecture must distinguish:

$$\boxed{  
\text{history preserved}  
}  $$

from:

$$\boxed{  
\text{active trajectory continuously maintained}  
}  $$

A process may restart and recover the record.

That does not prove that the reasoning state survived continuously throughout the interruption.

#### Recoverability depends upon the record

SLA makes reconstruction possible only to the extent that the relevant information was actually preserved.

Missing source references, incomplete transition records, overwritten state, or unattributed summaries can prevent reliable reconstruction.

The existence of persistent storage does not guarantee complete lineage.

Accordingly, lineage recoverability is a separately testable architectural property.

---

### 12.8 What SLA Makes Measurable

Source Locked Architecture is not itself a single numerical measurement.

Its importance is that it separates architectural objects and operational conditions that would otherwise be difficult to distinguish.

The Mirror Protocol preserved transformation trajectories.

SLA adds explicit requirements concerning the authority and persistence of the references from which those trajectories are reconstructed.

This makes several independent properties available for evaluation.

| SLA property                    | Experimental question                                                              | Required evidence                                                      |
| ------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Source identity                 | Can the originating artifact be distinguished from subsequent derivations?         | Source reference and comparison with later material                    |
| Source integrity                | Has the designated source changed without an identified transition?                | Source records, versions, or integrity comparisons                     |
| Provenance                      | Can a derived result be attributed to the relevant source and operation?           | Recorded transformation or attribution information                     |
| State persistence               | Does retained information survive a declared execution interruption?               | Before-and-after persistence records                                   |
| Lineage reconstruction          | Can the significant steps connecting source and result be recovered?               | A sufficiently complete transition history                             |
| Source–state separation         | Can active or stored state change while the source reference remains identifiable? | Controlled state changes with preserved source identity                |
| Mutation boundary               | Can a proposed change be distinguished from an accepted protected-state change?    | Implemented acceptance/rejection rules and execution records           |
| Reconstruction after disruption | Can relevant information be recovered after context or runtime loss?               | Documented interruption, recovery inputs, and evaluated reconstruction |

These are distinct properties.

No single successful measurement establishes that the entire architecture is validated.

#### 12.8.1 Source-Integrity Test

A controlled test can record a canonical source and compare it with material retrieved after a transformation or storage operation.

The test must specify what counts as preservation.

Exact content identity requires a different criterion from preservation of selected semantic relationships.

A result satisfying one criterion does not automatically satisfy the other.

#### 12.8.2 Persistence Test

A persistence test can record relevant state, interrupt the execution environment, and determine whether the stored material remains available after restart.

Success establishes persistence for the tested records and execution conditions.

It does not, by itself, demonstrate that a model reconstructs the correct semantic relationships from the retained state.

#### 12.8.3 Provenance Test

A provenance test can introduce distinguishable source and derived records, then determine whether the architecture maintains their attribution.

If a derivation is subsequently treated as the originating source without an identifiable transition, the source-authority condition fails.

#### 12.8.4 Lineage-Recovery Test

A lineage test can examine whether a resulting state can be traced backward through its significant recorded transformations.

The expected result must be defined according to the information the architecture was intended to preserve.

A system cannot be declared deficient for failing to reconstruct details that its declared record never attempted to capture.

#### 12.8.5 State-Mutation Test

Where an implementation includes explicit protected-state controls, a test can propose an unauthorized or otherwise invalid change.

The observed result should be compared against the declared state-transition rule.

The design requirement is that an invalid operation does not silently become an accepted state change.

The property is validated only when the actual mechanism and its expected behavior have been tested.

#### The measurement boundary

These procedures describe what SLA makes testable.

They do not imply that every historical SLA requirement was validated by a completed test.

An implemented persistence mechanism, an observed successful retrieval, and a validated continuity property represent different evidentiary states.

That distinction is essential to the study.

---

### 12.9 What the Architecture Established—and What Remained Open

The development of SLA established a more precise way to organize the continuity problem.

A source could be distinguished from its derivations.

Persistent state could be separated from active model context.

Lineage could be treated as an architectural requirement rather than assumed from a plausible continuation.

Protected evidence could remain distinguishable from later interpretation.

And the conditions under which state changes became accepted could be identified as a separate architectural concern.

These developments did not make semantic continuity automatic.

They made its underlying dependencies more explicit.

#### Source preservation is not semantic accuracy

A preserved source may still be interpreted incorrectly.

#### Persistent memory is not successful reconstruction

Stored material may remain available without being correctly used.

#### Provenance is not proof of truth

Attribution establishes a relationship between an artifact and its documented origin. It does not establish the factual correctness of the artifact.

#### Authorized state is not immutable history

Protected state may change according to declared rules.

The requirement is to preserve the distinction between the change and the record it modifies.

#### Lineage is not uninterrupted execution

A reconstructable history may survive a process boundary without the active model maintaining a continuous internal state.

The importance of these distinctions lies in their independence.

An architecture may satisfy one and fail another.

A stored source may survive a restart while its derived relationships are reconstructed incorrectly.

A correct answer may be generated from incomplete or unattributed information.

A later correction may improve the result while obscuring the original error if provenance is not preserved.

These are different failure conditions.

SLA created the structural vocabulary required to examine them separately.

Its underlying contribution was not the elimination of all possible continuity failures.

It was the separation of the architectural relationships through which those failures could be identified.

---

### 12.10 From Source Protection to Processing Decisions

The Mirror Protocol preserved the transformation path.

Source Locked Architecture addressed the integrity of the reference and the persistent relationships surrounding that path.

Together, these developments provided a foundation for examining semantic transformations under changing computational conditions.

But preserving the source did not determine how every incoming task should be processed.

A system could retain an authoritative reference without knowing which operation should be performed next.

Different tasks could require different forms of processing.

Some might be evaluated through simple retrieval or direct transformation.

Others might require additional interpretation, verification, or a more constrained processing route.

The presence of a protected source did not settle these decisions.

This introduced a distinct architectural question.

**How should processing be selected while maintaining source integrity and recognizable provenance?**

SLA supplied the reference boundary.

It did not, by itself, specify one universal routing decision for every input.

The development of the Zero-Point Protocol addressed that broader problem through routing, scoring, and conditional processing mechanisms.

The two architectural concerns were related but distinct.

Source protection concerns what must remain identifiable.

Processing decisions concern what operation is warranted by the incoming task and the system's declared conditions.

A processing pathway may change.

The originating reference must not silently change with it.

The architectural relationship can therefore be summarized as:

$$\boxed{  
\text{SOURCE INTEGRITY}  
\quad+\quad  
\text{CONDITIONAL PROCESSING}  
}  $$

This is the transition from the source-preservation requirements formalized through SLA toward the broader routing architecture developed through ZPP.

The question was no longer solely whether the architecture could identify and preserve a source.

It was how the architecture should operate over that source without confusing the processing result with the reference that made evaluation possible.

---

### 12.11 What Remained

Source Locked Architecture emerged from the need to preserve the distinction between an originating reference and its transformations.

The Mirror had shown that a path could be reconstructed.

SLA made the integrity of the source and its relationship to persistent architectural state an explicit design problem.

Its enduring principle was:

- Protect the identity and provenance of the source.
    
- Preserve significant state and lineage relationships.
    
- Allow interpretations and reasoning to differ.
    
- Keep changes attributable and recoverable.

This does not require every representation to remain unchanged.

It does not require every model to reach an identical conclusion.

It does not require an uninterrupted active context.

It requires that changes to representation, interpretation, state, and execution do not automatically erase the reference through which those changes can be understood.

That is the distinction introduced by Source Locked Architecture.

**The source can remain identifiable while the system operating over it changes.**

And that distinction provides the foundation for investigating which processing conditions preserve the relationships that matter.