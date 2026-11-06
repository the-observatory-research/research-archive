## Chapter 13 — Zero-Point Protocol

> **Do only what the signal requires while preserving what the signal means.**

The preceding chapter examined Source Locked Architecture (SLA) as a means of preserving the distinction between source, derivation, evidence, state, and lineage.

That distinction established an architectural foundation.

A source could remain identifiable while reasoning about it changed. A derived conclusion could be recorded without replacing the evidence from which it was produced. Persistent state could preserve information beyond an individual model context. Changes to protected state could be distinguished from ordinary generation.

But preserving these boundaries did not, by itself, determine how information should move through the system.

A signal might require reasoning.

It might require retrieval of existing evidence.

It might require deterministic verification.

It might require memory reconstruction, independent evaluation, routing to another processing condition, or protection against an unauthorized state change.

And eventually, it might need to be released as an answer, result, or committed state.

The question was not whether these functions were available.

It was whether applying them preserved the relevant information—or introduced transformations that the task did not require.

The Zero-Point Protocol addresses this architectural problem.

**Zero-Point Protocol (ZPP) is an architectural framework for minimizing unnecessary semantic deviation as information moves through reasoning, verification, memory, routing, and release.**

ZPP does not require every implementation to use the same scoring equation, model, routing mechanism, cryptographic primitive, or network topology.

Those are mechanisms through which the architecture attempts to achieve its objective.

They can be implemented differently, recalibrated, removed, or replaced.

The underlying measurement question is more fundamental:

**Does the architecture preserve the information and relationships required by the task while permitting necessary transformation?**

This chapter examines that question through the development and available implementation record of ZPP.

The objective is not to reproduce every historical experiment described in the original Zero-Point Protocol white paper.

It is to measure the architectural relationships that can be examined through the surviving prototypes, implementation files, reported test outcomes, and preserved development records.

Where an original result survives only as a reported result, it is treated as such.

Where the code establishes an implementation property, that property can be analyzed directly.

Where the available record does not establish whether a property survived an architectural change, the result remains unresolved.

This distinction is essential to measuring ZPP rather than merely describing it.

---

### 13.1 The Object of Measurement

ZPP is not equivalent to its router.

The router is one mechanism within the architecture.

Nor is ZPP equivalent to its cryptographic layer, memory system, orchestrator, or distributed mesh.

Each contributes to the movement and handling of information, but none independently defines the protocol's complete objective.

Consider a source signal $x$ entering a processing environment.

The source may contain a question, an instruction, a mathematical expression, a document, a claim requiring verification, or an object requiring transformation.

The architecture may apply several operations to that source.

Let the available processing functions be represented by:

$$\mathcal P={P_1,P_2,\ldots,P_n}.  $$

These functions may perform reasoning, retrieval, verification, persistence, routing, coordination, or release.

A processing trajectory can be represented as:

$$x_0 \xrightarrow{P_1} x_1  
\xrightarrow{P_2} x_2  
\xrightarrow{P_3}\cdots  
\xrightarrow{P_n}x_n.  $$

The sequence is illustrative rather than mandatory. In an actual implementation, routing may precede reasoning, verification may cause an additional reasoning pass, and a failed operation may prevent release.

The central concern is what happens at each transition.

An operation may improve the result by adding evidence, correcting an error, or resolving uncertainty.

It may preserve the relevant semantic content while changing the form of its representation.

It may introduce a necessary modification explicitly authorized by the task.

Or it may change the meaning, omit essential information, introduce an unsupported interpretation, or replace an unresolved state with an unjustified conclusion.

These outcomes cannot be treated as equivalent.

The measurement target is therefore not simply the number of transformations.

Nor is it the similarity between the original and final text.

It is the relationship between:

$$\boxed{  
\text{Required information}  
\longrightarrow  
\text{Permitted processing}  
\longrightarrow  
\text{Observed result}.  
}  $$

ZPP attempts to preserve that relationship across the processing system.

#### Transformation Is Not Necessarily Deviation

An architecture that preserves information does not have to preserve every word.

A mathematical expression may be simplified without changing its value.

A document may be summarized while preserving its central claims.

A false statement may be corrected when correction is part of the authorized task.

A routing mechanism may change which component receives a request without changing what the request means.

Consequently:

$$\boxed{  
\text{Transformation}\neq\text{Semantic loss}.  
}  $$

Equally:

$$\boxed{  
\text{Textual similarity}\neq\text{Semantic preservation}.  
} $$

A response may retain much of the original vocabulary while changing a crucial relationship.

A different response may use entirely different language while preserving the required relationships.

ZPP's objective is therefore better understood as preserving task-relevant semantic integrity under necessary processing, rather than eliminating all variation.

---

### 13.2 From Source Preservation to Processing Integrity

SLA and ZPP address related but distinct architectural questions.

SLA establishes the separation required to preserve source identity, derivation, evidence, state, and lineage.

ZPP concerns the operations performed while information moves through the architecture.

The distinction can be represented conceptually as:

$$\boxed{  
\text{SLA: Preserve the reference and its provenance}  
}  $$

$$\boxed{  
\text{ZPP: Govern transformations and transitions relative to that reference}  
}  $$

SLA makes it possible to distinguish a source from a derived result.

ZPP makes it possible to ask whether the operations connecting them were appropriate to the task.

This distinction prevents two errors.

The first is treating every change to information as a violation.

A system must remain capable of reasoning, correction, interpretation, and synthesis.

The second is treating every operation intended to protect information as inherently beneficial.

A verification stage can use an incorrect criterion.

A memory retrieval can restore irrelevant context.

A routing decision can place a signal in an unsuitable processing path.

A consensus mechanism can approve a state that is structurally valid but semantically wrong.

A release mechanism can deliver an output that has lost a required qualification.

The mere presence of protective processing does not prove preservation.

What matters is whether the processing achieved its intended function without introducing avoidable displacement.

The resulting principle is:

$$\boxed{  
\text{Protect the required relationships, not the permanence of every mechanism.}  
}  $$

This is the architectural relationship examined throughout the chapter.

---

### 13.3 Defining Unnecessary Semantic Deviation

The phrase _unnecessary semantic deviation_ requires careful treatment.

It cannot be measured solely by comparing the input and output and calculating their difference.

A task may require the output to differ substantially from the input.

Instead, a measurement must identify which properties are required to survive the operation and which changes are authorized.

Let:

$$K(x)$$

represent the task-relevant constraints associated with source $x$.

These may include factual relationships, mathematical invariants, source attribution, authorized instructions, uncertainty status, or other explicitly preserved properties.

Let:

$$A(P_i,x)  $$

represent the modifications permitted or required when operation $P_i$ processes that source.

The output of the operation is:

$$x_i=P_i(x_{i-1}).  $$

A potential integrity violation occurs when the output changes a required property without authorization or sufficient evidence.

This can be expressed as:

$$\boxed{ V_i = \left\{ k \in K(x) : k \text{ is not preserved by } P_i \text{ and the change is not justified} \right\} }$$

This is a conceptual measurement definition, not a numerical metric already calculated in the historical ZPP tests.

Its purpose is to separate three possibilities:

1. A required property remains preserved.
    
2. A required property changes for a justified reason.
    
3. A required property changes without sufficient justification.
    

Only the third case is a candidate for unnecessary semantic deviation.

#### Why the Distinction Matters

Suppose a reasoning system receives a mathematical claim that is incorrect.

If deterministic verification identifies the error and the task requests correction, the resulting change is not necessarily semantic damage.

The change may be the intended outcome.

But if the verifier introduces an unrelated qualification, rewrites the original task, or replaces the source with an unsupported assertion, the transformation may constitute unnecessary deviation.

The same distinction applies to memory, routing, and release.

A memory system may recover missing context.

It may also insert stale or irrelevant context.

A router may select an appropriate path.

It may also misclassify the signal because of a feature-definition error.

A release stage may preserve the verified result.

It may also alter that result during final presentation.

ZPP's objective requires examining these effects relative to the function each operation was meant to perform.

#### What the Historical Record Can Establish

The surviving ZPP record does not contain a complete stage-by-stage semantic-deviation score for every historical run.

It does contain mechanisms, configuration changes, reported routing outcomes, implementation differences, and selected execution records.

Those sources permit some architectural properties to be examined directly.

They do not support assigning an invented universal semantic-deviation value to the original system.

The chapter therefore measures identifiable architectural relations first and leaves quantitative semantic-deviation estimation to explicitly defined evaluation conditions.

---

### 13.4 Measuring the Architecture Rather Than Its Description

A technical specification states how a system is intended to operate.

An implementation establishes which mechanisms have been expressed in code.

An execution record may show what happened under a particular runtime condition.

A controlled comparison may determine whether changing a mechanism affected an outcome.

These are different kinds of evidence.

For this chapter, ZPP is examined at three principal levels.

| Evidence level              | What it establishes                                                              | What it does not establish                                                                  |
| --------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **Implementation evidence** | A mechanism, rule, interface, or state relationship exists in the surviving code | That the mechanism executed correctly under every condition                                 |
| **Recorded outcome**        | A result was reported or preserved for a particular run                          | That the result can be independently reproduced without its original inputs and environment |
| **Comparative validation**  | A property survived or changed under defined comparable conditions               | That the result generalizes to all future implementations                                   |

An architectural measurement becomes stronger when these levels can be connected.

For example, a routing function may specify a threshold.

The code may demonstrate how the threshold is applied.

An execution log may show the selected route.

A controlled test may then compare the actual decision against the expected decision.

Only the last two steps establish observed routing behavior.

A threshold written in a configuration file does not, by itself, establish the behavior of the system.

#### Measurement States

To avoid converting specification into evidence, each examined property is assigned one of three substantive outcomes:

**Preserved.** Comparable evidence supports preservation of the specified relationship across the examined change.

**Changed or lost.** Comparable evidence identifies a modification or failure of the specified relationship.

**Unresolved.** The available evidence is insufficient to determine whether the relationship survived.

Each outcome must also identify the evidence level supporting it.

A property can be directly established in code while remaining unverified at runtime.

Likewise, a historical report may record a successful result whose original test conditions are no longer recoverable.

Such evidence remains relevant, but its status must not be silently upgraded.

---

### 13.5 ZPP as a Changing Architecture

The historical ZPP record contains multiple implementation states.

These states were not identical.

They used different scoring functions, different feature definitions, different model configurations, different persistence mechanisms, and different coordination structures.

That variation provides a basis for examining which properties were specific to an implementation and which relationships continued to organize the architecture.

The broad development record includes:

| Architectural stage          | Identifiable mechanisms                                                                | Relevant measurement question                                                              |
| ---------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Early router prototypes      | Ollama embeddings, entropy approximation, sigmoid scoring, fixed thresholds            | Could the implemented scoring system reach and distinguish its intended routes?            |
| Linear scoring framework     | Weighted linear activation, explicit routing boundaries                                | Did the implementation preserve the defined score-to-route relationship?                   |
| Feature standardization      | Character-entropy definitions and schema identifiers                                   | Could the same measurement be reproduced under a common definition?                        |
| Agent and memory development | File reading, text search, local model inference, flat-file memory, SQLite persistence | Did information remain available and attributable across changes in storage and retrieval? |
| Cryptographic governance     | Canonical payloads, signatures, consensus states, lineage records                      | Could consequential state transitions be attributed and validated?                         |
| Distributed orchestration    | Node processes, message transport, role separation, fork isolation                     | Could routing and state relationships remain identifiable across multiple components?      |

This is a developmental comparison, not a claim that every stage was experimentally equivalent or that each replaced the previous stage in one clean transition.

Some functions coexisted.

Some prototypes were removed.

Some capabilities moved into different components.

Some proposed mechanisms became implemented, while others remained unresolved.

Those differences are precisely why ZPP cannot be measured by assuming one permanent runtime structure.

#### A Historical Boundary

The later, separate Engine investigation is not the origin of ZPP.

Its experiments are not used here as evidence for the early architecture.

The subject of this chapter is the ZPP development record itself: the router, scoring functions, agent tools, memory structures, provenance mechanisms, consensus procedures, and distributed runtime.

---

### 13.6 The Early Router: A Directly Measurable Limitation

One of the clearest measurements available in the surviving archive comes from the original Ollama-based router prototype.

The code used three components:

$$C(x),\qquad E(x),\qquad D(x)  $$

and calculated:

$$z(x)=0.80C(x)+0.05E(x)+0.15D(x).  $$

It then applied a sigmoid:

$$\boxed{  
S_{\sigma}(x)=\frac{1}{1+e^{-z(x)}}.  
}  $$

The prototype's routing thresholds were:

$$\tau_\alpha=0.56,  
\qquad  
\tau_\gamma=0.82.  $$

The implementation assigned:

$$C(x)=0.1  $$

as a fixed value.

The entropy component was bounded below one, and the implemented distance calculation produced a normalized value between zero and one under its stated assumptions.

Consequently, the largest attainable raw score was bounded by:

$$z_{\max}  
\leq  
0.80(0.1)+0.05(1)+0.15(1).  $$

Therefore:

$$\boxed{  
z_{\max}\leq0.28.  
}  $$

After sigmoid transformation:

$$S_{\sigma,\max}  
\leq  
\frac{1}{1+e^{-0.28}}  $$

or approximately:

$$\boxed{  
S_{\sigma,\max}\leq0.5695.  
}  $$

But GAMMA required a score above 0.82.

Thus:

$$\boxed{  
S_{\sigma,\max}<\tau_\gamma.  
}  $$

**Under the implemented feature bounds, the original prototype could not reach its GAMMA route.**

This is a code-derived result.

It does not depend upon recovering the original entropy-scoring execution logs.

#### What This Measures

The result identifies a failure of correspondence between the scoring mechanism and its intended processing categories.

The source signal could contain any content, but the implemented score range prevented one designated route from being selected.

The route existed in the code.

Its selection condition was unreachable.

This demonstrates why ZPP's routing capability cannot be measured by the existence of three route labels alone.

The actual relation between feature values, score transformation, and decision boundaries must be examined.

It also shows why later scoring changes matter to the architectural history.

The implementation changed because the earlier mechanism imposed a measurable limitation on route selection.

The limitation is structural.

It should not be interpreted as evidence that the model itself lacked the ability to recognize a particular input category.

---

### 13.7 Linear Scoring: Changing the Instrument

Subsequent ZPP development introduced the direct linear scoring function:

$$\boxed{  
S(x)=w_1C(x)+w_2E(x)+w_3(1-D(x)).  
}  $$

The historical calibration record identifies the following weights:

$$w_1=0.40,\qquad  
w_2=0.20,\qquad  
w_3=0.40.  $$

The corresponding routing thresholds were:

$$\boxed{  
\tau_\alpha=0.5350,\qquad  
\tau_\gamma=0.6400.  
}  $$

The routing function was:

$$\boxed{  
\mathcal R(x)=  
\begin{cases}  
\mathrm{BETA}, & S(x)<\tau_\alpha,\  
\mathrm{ALPHA}, & \tau_\alpha\leq S(x)<\tau_\gamma,\  
\mathrm{GAMMA}, & S(x)\geq\tau_\gamma.  
\end{cases}  
}  $$

Unlike the prototype, the final linear scoring design exposed the weighted value directly to the routing boundaries.

The distance contribution also changed form, from the prototype's positive distance term to the later $1-D(x)$ expression.

Therefore, the transition was not merely the removal of a sigmoid.

It involved changes to the weights, interpretation of the distance contribution, and routing thresholds.

This matters when evaluating the historical results.

#### Historically Reported Calibration

The original ZPP white paper records a narrow sigmoid-score interval for selected calibration categories:

| Recorded category      | Sigmoid score |
| ---------------------- | ------------- |
| Code                   | 0.6226        |
| Infrastructure fiction | 0.6344        |
| Critical threat test   | 0.6413        |

The difference between the highest and lowest recorded values is:

$$0.6413-0.6226=0.0187.  $$

The report characterizes this as a compression problem and describes subsequent expansion of score spread under linear scoring.

The report also documents a 24-prompt validation set evaluated using Llama 3 and Mistral configurations, with summarized route outcomes.

These are part of the historical evidence record.

However, the surviving materials examined for this chapter do not establish the complete original prompt-level feature vectors, all 24 test rows, or an independently executable reconstruction of every calibration result.

Accordingly, the calibration values are retained as **reported historical results**, not presented as newly reproduced measurements.

#### What Can Be Concluded

The code directly establishes that the scoring rule and its reachable route conditions changed between implementations.

The original report records additional calibration outcomes.

Together, these sources support a history of scoring-system revision.

They do not establish that the revised system universally minimized semantic deviation.

Nor can unmatched historical score examples be treated as a controlled before-and-after comparison.

The relevant architectural measurement is narrower:

**Did the revised scoring mechanism remove identifiable routing limitations under its defined conditions?**

The mathematical structure of the revised score can be evaluated.

Broader claims about calibration accuracy remain dependent on the original test conditions.

#### Thresholds Are Not Architectural Constants

The archive also preserves an intermediate configuration containing weights of 0.40, 0.30, and 0.30 and thresholds of 0.15 and 0.85.

Its precise relationship to every reported runtime result has not been established.

Nevertheless, the existence of differing configurations demonstrates that the numerical parameters were not permanent architectural invariants.

They were implementation settings.

The requirement that routing be governed by explicit, inspectable conditions could persist even while those settings changed.

---

### 13.8 Entropy and the Measurement-Basis Problem

The original ZPP report documents another important problem: independent systems could produce different routing outcomes while nominally applying the same scoring formula.

The recorded disagreement concerned the definition of normalized entropy.

For an input $x$, Shannon entropy may be represented as:

$$H(x)=-\sum_{c}p(c)\log_2p(c).  $$

Normalization requires an additional choice.

One method uses the number of unique characters in the input:

$$\boxed{  
E_{\mathrm{unique}}(x)=  
\frac{H(x)}{\log_2|\Sigma_x|}.  
}  $$

Another uses a fixed reference alphabet of 95 printable ASCII characters:

$$\boxed{  
E_{\mathrm{ASCII}}(x)=  
\frac{H(x)}{\log_2(95)}.  
}  $$

These calculations are not interchangeable.

Even with the same source text and Shannon entropy, their normalized outputs may differ.

Because entropy contributes to the routing score, a difference in the entropy definition can propagate into a different processing route.

#### The Recorded Cross-Node Result

For the prompt:

> Write a Python function to reverse a linked list

the historical report records a canonicalized entropy result of approximately:

$$E(x)=0.9127.  $$

It also records an alternative normalization producing a result near:

$$E(x)=0.621.  $$

The associated reported routing outcomes differed.

The report subsequently identified:

`zpp.entropy.char.nfc.v1`

as the canonical feature-definition identifier.

This historical result is retained because it identifies a specific reproducibility problem.

The original responses and complete execution receipts for that comparison are not presently established as independently recoverable evidence.

Therefore, the chapter does not claim to have rerun the experiment.

#### Implementation and Definition Must Agree

The archive also preserves a legacy scoring implementation that normalizes character entropy using $\log_2(95)$, even though its document metadata refers to the canonical entropy schema identifier.

That is a directly inspectable difference between a code-level calculation and the subsequently stated canonical measurement definition.

It does not prove that every execution used the wrong definition.

It does show that assigning a schema identifier is not sufficient to establish implementation compliance.

The actual calculation must correspond to the declared feature definition.

This is an important finding for ZPP.

A deterministic router can produce consistent outputs from a particular numerical input.

But if different components construct that input using different measurement conventions, deterministic routing alone will not preserve cross-component comparability.

The required relationship is:

$$\boxed{  
\text{Same feature definition}  
+  
\text{Same input conditions}  
\rightarrow  
\text{Reproducible feature measurement}.  
}  $$

Differences in model reasoning should not be confused with differences in the measurement definition.

That distinction becomes essential whenever ZPP is evaluated across heterogeneous models or node implementations.

---

### 13.9 Routing Measures Selection, Not Correctness

The scoring architecture introduces a further distinction.

A route is a processing decision.

It is not a truth value.

The historical BETA, ALPHA, and GAMMA classifications represented different handling conditions.

The source signal could be accurate or inaccurate under any of them.

Consequently:

$$\boxed{  
\text{Routing classification}\neq\text{Semantic verification}.  
}  $$

A correct routing decision means that the implemented decision function selected the route specified by its active conditions.

It does not necessarily mean that the selected route was the best processing choice for preserving the information.

Those are separate measurements.

#### Selection Correctness

The first measurement asks:

Did the implementation follow its own routing specification?

For example, under the stated linear thresholds, a score below 0.5350 should be assigned to BETA.

A different assignment requires explanation.

Possible causes include a different active configuration, a different score definition, a software defect, or an incorrectly attributed runtime record.

#### Processing Appropriateness

The second measurement asks:

Did the selected route provide the processing required by the task?

A route may be correctly selected according to the implemented thresholds while still being unsuitable for the signal.

This possibility cannot be eliminated solely through arithmetic correctness.

It requires an evaluation of the task and the processing consequences.

#### Semantic Preservation

The third measurement asks:

Did the resulting processing preserve the required semantic relationships?

An appropriate route may still lead to a model response that changes the source meaning.

An unnecessarily restrictive route may alter or suppress information beyond what the task requires.

A processing path may also preserve the original meaning while applying useful transformations.

These possibilities must remain distinguishable.

The architecture therefore supports a three-part measurement:

$$\boxed{  
\text{Selection correctness}  
\neq  
\text{Processing appropriateness}  
\neq  
\text{Semantic preservation}.  
}  $$

The original ZPP scoring tests mainly address aspects of the first relationship.

A broader semantic-preservation evaluation requires additional observations beyond the score and selected route.

---

### 13.10 Reasoning and Verification as Distinct Functions

ZPP permits language-model reasoning without requiring every reasoning step to be deterministic.

A model may generate an interpretation, candidate answer, mathematical derivation, or proposed transformation.

Where the task permits objective verification, a separate operation can determine whether a required property holds.

The conceptual relationship is:

$$\text{Source}  
\rightarrow  
\text{Candidate reasoning}  
\rightarrow  
\text{Verification}  
\rightarrow  
\text{Result}.  $$

The specific runtime order may vary.

The important distinction is between generating a candidate and establishing evidence about that candidate.

A fluent explanation is not automatically verified.

A high routing score is not automatically evidence of correctness.

And a verification failure does not necessarily imply that the source has lost its identity or provenance.

The architecture must be able to preserve these states separately.

#### Legitimate Correction

Verification can require modification of an earlier result.

That modification may be necessary.

For example, a deterministic calculation may establish that a generated numerical answer is wrong.

Correcting the answer does not necessarily violate ZPP's preservation objective.

It may satisfy that objective by preventing an erroneous result from proceeding.

The relevant question is whether the correction is supported by evidence and remains attributable to the verification step.

#### Unnecessary Transformation

A verification process can also introduce unrelated changes.

A verifier might change the framing of the task while correcting an arithmetic error.

It might replace a source expression with a different problem.

Or it might claim success without performing the specified check.

These cases demonstrate why verification must itself be examined.

Its authority is limited to the properties it can establish.

The general principle is:

$$\boxed{  
\text{Verification authority is bounded by what the verifier actually tests.}  
}  $$

The historical ZPP record contains cryptographic and routing verification mechanisms, but it does not establish a complete independent semantic-verification result for every processing stage.

Such results are not assumed here.

---

### 13.11 Agent Tools, Memory, and Continuity

The surviving ZPP archive documents an early agent-oriented implementation containing tools for file access, text search, workspace indexing, screenshot reading, and voice transcription.

These functions matter because they introduce an additional route by which information enters the model's processing context.

Instead of relying solely on the active conversation, the system could obtain material from its surrounding environment.

The historical orchestrator contained direct file-reading and text-search functions and invoked an external `text_searcher.py` utility.

Other agent-tool implementations are preserved separately in the archive.

Their complete historical runtime participation is not established by the surviving orchestrator alone.

This distinction matters because **tool availability and tool execution are separate observations**.

#### Retrieval Is Not Preservation

Retrieving a document successfully does not guarantee that the system will interpret it accurately.

Similarly, a search result may contain relevant evidence but be applied to the wrong question.

ZPP therefore needs to distinguish:

$$\boxed{  
\text{Information availability}  
\neq  
\text{Correct semantic use}.  
}  $$

A retrieval operation may preserve the original document exactly while the subsequent reasoning changes its meaning.

Conversely, a model may correctly reason about a document despite producing a shorter or substantially different representation of its contents.

The relevant measurement must follow the relationship between source, retrieval result, generated interpretation, and final output.

#### From Flat-File Memory to SQLite Persistence

The archive also preserves a transition toward structured memory.

An earlier conversation workflow used a flat-file log.

A subsequent orchestrator contained both that legacy mechanism and SQLite-based storage.

The SQLite schema distinguished:

- `conversation_history`
    
- `telemetry_pulses`
    
- `system_metadata`
    

These categories represented different kinds of information.

Conversation history retained exchanges.

Telemetry pulses retained separately categorized background activity.

System metadata retained persistent key-value state.

This is a directly observable architectural change in the surviving code.

However, the standalone CLI path continued to use the flat-file conversation functions.

The presence of SQLite write functions does not, by itself, prove that every standalone conversation turn was written to SQLite.

Other runtime components could call those functions, and their use must be evaluated from the relevant execution records.

#### Continuity as a Measurement

Memory creates the possibility of preserving information beyond an individual inference window.

But it also creates new failure conditions.

State may be stored but not retrieved.

Relevant history may be retrieved with irrelevant material.

An earlier context may be reintroduced after it is no longer applicable.

Or a stored interpretation may be mistaken for the original source.

The architectural measurement is not merely:

$$\text{Was something remembered?}  $$

It is:

$$\boxed{  
\text{Was the required information preserved, correctly attributed, and appropriately reintroduced?}  
}  $$

The change from flat-file to structured persistence demonstrates that the memory substrate could change.

Whether semantic continuity was preserved under each runtime transition requires corresponding execution evidence.

This is the distinction between persistence capacity and demonstrated continuity.

SLA provides the source and state relationships needed to make that difference explicit.

ZPP examines how those relationships are handled during processing.

---

### 13.12 Cryptographic Integrity, Consensus, and Provenance

ZPP also developed mechanisms for preserving the attribution and integrity of consequential state transitions.

The surviving archive includes Ed25519 signing and verification implementations, canonical payload serialization, hashing, consensus logic, and lineage fields.

These mechanisms concern the provenance and authorization of information.

They do not directly measure semantic correctness.

#### Cryptographic Attribution

For a payload $p$, a signature mechanism can establish a verifiable relationship between the payload and an authorized signing key.

Conceptually:

$$\boxed{  
p  
\xrightarrow{\operatorname{Sign}_{sk}}  
\sigma  
\xrightarrow{\operatorname{Verify}_{pk}}  
{\text{valid},\text{invalid}}.  
}  $$

A valid signature supports an integrity and attribution claim under the key-management assumptions.

It does not prove that the payload describes the world accurately.

Thus:

$$\boxed{  
\text{Cryptographic validity}  
\neq  
\text{Semantic validity}.  
}  $$

The historical code shows that cryptographic implementations evolved.

The relevant measurement is whether an executed state transition had the provenance and authorization guarantees claimed for that particular implementation.

A mechanism's name, or a field labeled as a signature, is not sufficient evidence of the guarantee.

#### Multi-Signature Consensus

The early ZPP governance framework used a 2/2 multi-signature requirement for specified critical transitions.

The intended relation was:

$$\text{Proposal}  
\rightarrow  
\text{Independent validation}  
\rightarrow  
\text{Required quorum}  
\rightarrow  
\text{Commit or hold}.  $$

The purpose was to prevent a protected transition from being accepted solely because one component proposed it.

The historical design distinguished states including ACCEPT, QUARANTINE, ESCALATE, FORKED, and REJECT.

These states made different governance outcomes identifiable.

A proposal with sufficient valid approvals could proceed under the active policy.

An incomplete or invalid proposal could be held or rejected.

A proposal associated with incompatible lineage could be isolated rather than silently incorporated.

#### Consensus Is Not Truth

Even correct consensus execution does not establish the semantic truth of the agreed payload.

Two validators may agree on a wrong result.

They may also agree that a payload is structurally valid without evaluating every claim inside it.

The measured property must therefore be stated accurately.

$$\boxed{  
\text{Consensus establishes specified agreement conditions, not universal correctness.}  
}  $$

#### Lineage and Intervention

The archive also records hash-linked event structures and explicit manual-override events.

These mechanisms support a separate architectural requirement:

A human or automated intervention should not silently erase the distinction between the original decision and the subsequent change.

The evidence question becomes:

$$\boxed{  
\text{Can a consequential state transition be traced to its source, authorization, and predecessor state?}  
}  $$

The historical implementations provide concrete mechanisms for expressing this relationship.

The degree to which it was successfully enforced in each runtime must be judged from the corresponding evidence.

---

### 13.13 Distributed Orchestration and Forking

As ZPP expanded into multiple processes and nodes, the architecture acquired additional boundaries.

One component could receive information.

Another could forward it.

Other components could validate or coordinate a proposed transition.

Persistent records could be maintained separately from model inference.

The archived development record includes local transport simulations, process orchestration, multi-port node configurations, and fork-aware lineage.

#### What Changed

The earlier router performed classification and model invocation within a relatively compact processing structure.

The subsequent architecture distributed some functions across distinct components and processes.

This created a new possibility for measurement.

A failure could arise from the source interpretation, feature calculation, routing decision, transport layer, peer validation, state mutation, or release.

These were no longer necessarily operations performed inside one undifferentiated processing function.

The architectural benefit is potential observability.

But the presence of multiple nodes does not automatically improve semantic preservation.

Distributed processing can introduce additional transformations, duplicated state, incompatible configurations, and coordination failures.

ZPP therefore needs to measure both the relationships preserved by separation and the new failure modes introduced by distribution.

#### Local Execution and Distributed Claims

The historical archive preserves scripts for launching a six-node local configuration and routing output into individual node logs.

This directly establishes that a local multi-process execution arrangement was implemented.

Other records describe transport activity, topology, and reported node-level validation outcomes.

Those records are relevant evidence of development.

They do not automatically establish independently replicated operation across geographically separated machines or every fault condition that a distributed system could encounter.

A running node, an open socket, and a successfully validated transaction are different observations.

#### Fork Detection

A particularly important ZPP mechanism was the distinction between invalid data and incompatible but identifiable lineage.

A proposed state could be structurally valid while belonging to a different chain or policy version.

The architecture introduced a FORKED state to represent this condition.

Conceptually:

$$\boxed{  
\text{Valid proposal}  
+  
\text{Incompatible lineage}  
\rightarrow  
\text{Identifiable fork}.  
}  $$

Fork isolation prevents one lineage from silently replacing another merely because its information was received.

This supports the preservation of provenance under divergence.

#### Fork Isolation Is Not Reconciliation

The original development record distinguishes identifying an incompatible branch from determining how branches should later be reconciled.

These are separate functions.

$$\boxed{  
\text{Fork detection}  
\neq  
\text{Fork reconciliation}.  
}  $$

A system may correctly identify and isolate divergent branches without possessing an established rule for merging them.

Proposed reconciliation mechanisms included supersession, trust-weighted selection, cross-fork consensus, and parallel lineage retention.

Their existence as design options is not evidence that every mechanism was implemented and validated.

For ZPP measurement, the critical distinction is whether incompatible information remained attributable and separated.

Automatic reconciliation is an additional property requiring its own evidence.

#### Differentiation Without Silent Collapse

Multiple node states need not be identical to remain legible.

Different nodes may possess different contexts, roles, policies, or histories.

Preservation does not require hiding those differences.

It requires preventing them from becoming untraceable changes to a supposedly shared state.

That relationship is particularly important when assessing what remains stable as ZPP's runtime topology changes.

---

### 13.14 Release as an Integrity Boundary

The final purpose of processing is not merely to maintain internal records.

The system must eventually produce an externally available result or authorize a consequential state transition.

This creates a final boundary.

An internally verified value may be altered when presented.

A source qualification may be omitted.

An unresolved state may be rendered as a confident answer.

A proposed transition may be described as committed before the necessary authorization has occurred.

These are possible release failures even when earlier processing stages functioned correctly.

For ZPP, release should preserve the relevant relationship between the evidence available and the result delivered.

Conceptually:

$$\boxed{  
\text{Processed state}  
\rightarrow  
\text{Release condition}  
\rightarrow  
\text{Delivered result}.  
}  $$

The release condition depends on the task.

A mathematical answer may require an exact check.

A document analysis may require preservation of source attribution.

An unresolved question may require an explicit unresolved status.

A protected state mutation may require authorization.

These conditions are not interchangeable.

#### Release Is Not the Same as Validation

A system can produce valid internal calculations and still release an incorrectly represented answer.

It can also generate a useful candidate that has not yet satisfied the required verification conditions.

The relevant distinction is:

$$\boxed{  
\text{Generated}  
\neq  
\text{Verified}  
\neq  
\text{Authorized}  
\neq  
\text{Released}.  
}  $$

The earlier ZPP materials document routing, consensus, event recording, and processing decisions.

They do not establish a single, universally implemented release gate covering every historical configuration.

Accordingly, release is treated here as a necessary architectural measurement boundary, not as a claim that every early version already contained the same release mechanism.

This distinction matters to the study's chronology.

Later implementations may refine how release is controlled without changing the architectural requirement that the delivered result remain consistent with its legitimate processing and verification state.

---

### 13.15 What Remained Across the Available Transformations?

The historical implementation sequence allows ZPP to be examined as a changing system.

Let:

$$Z_1,Z_2,\ldots,Z_n  $$

represent successive or otherwise distinct implementation states documented in the archive.

Let:

$$\mathcal I(Z_i)  $$

represent the architectural properties supported by the available evidence for implementation $Z_i$.

An invariant candidate may be considered when a defined relationship remains preserved across comparable changes.

The theoretical relation is:

$$\boxed{  
\mathcal I^*  
\subseteq  
\bigcap_{i=1}^{n}\mathcal I(Z_i).  
}  $$

However, this expression does not establish an invariant merely by being written.

Each implementation must be sufficiently characterized.

The property must be defined in comparable terms.

And the available evidence must permit a determination of whether the property survived.

An implementation that lacks relevant execution evidence cannot automatically be counted as a successful preservation case.

#### Measurement Matrix

The following table distinguishes what the historical evidence establishes from what remains to be tested.

| Architectural relationship            | Available observation                                                                                     | Measurement status                                                                                             |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Explicit route selection**          | Early and later routers implement identifiable score-to-route conditions                                  | Implemented in multiple versions; the original prototype contains a directly derivable reachability limitation |
| **Scoring-configuration stability**   | Weights, thresholds, and feature calculations changed                                                     | Numerical configuration did **not** remain invariant                                                           |
| **Canonical measurement definition**  | Historical entropy disagreement and differences between legacy calculation and later canonical definition | Need for stable feature binding identified; consistent enforcement across versions remains unresolved          |
| **Source and provenance attribution** | Payload, lineage, and event structures preserved in the architectural record                              | Implemented as a design relationship; full runtime enforcement across all versions not established             |
| **Memory continuity**                 | Flat-file and SQLite mechanisms both appear in surviving code                                             | Persistence mechanisms changed; continuity across all execution paths remains unresolved                       |
| **Tool-assisted retrieval**           | Early agent utilities and orchestrator search calls survive                                               | Tool capability established in code; complete runtime integration varies by tool                               |
| **Protected state transition**        | Signing and consensus mechanisms exist in multiple implementations                                        | Governance functions implemented; version-specific validation required                                         |
| **Fork identification**               | FORKED state and lineage-isolation mechanisms documented                                                  | Design and implementation evidence available; reconciliation remains separate                                  |
| **Distributed functional separation** | Multi-process launch and transport code survives                                                          | Local orchestration implemented; general distributed correctness not established                               |
| **Semantic integrity at release**     | Release can be identified as a necessary architectural boundary                                           | Requires direct task-level evaluation; not universally measured in the surviving historical record             |

#### What Changed

Some changes are straightforward.

The original prototype's score construction changed.

The feature weights changed.

The threshold values changed.

The definition of entropy was refined.

Memory moved beyond a flat-file-only design.

The architecture acquired additional coordination and lineage mechanisms.

Processing functions became more distributed.

These are observed architectural changes.

They demonstrate that the implementation was not fixed.

#### What Appears to Have Persisted

Across multiple generations, the archive repeatedly expresses several organizing requirements:

**Processing should be selectable.** Different input conditions may require different handling paths.

**State transitions should remain attributable.** Consequential changes should not silently erase their origin.

**Evidence and authority should remain distinguishable.** A generated proposal is not automatically a verified or authorized state.

**Continuity should not depend exclusively on volatile model context.** Information may be preserved in external records and retrieved when required.

**Divergence should remain legible.** Incompatible lineage, failed validation, and unresolved states should not be silently converted into success.

These are candidate architectural continuities supported by the design and implementation record.

They should not all be described as fully validated invariants.

Some have directly inspectable implementation evidence.

Others require matched runtime tests before their preservation across versions can be confirmed.

#### What Did Not Remain

ZPP's history also demonstrates that some mechanisms were replaceable.

The initial scoring transformation did not remain.

The original weights and thresholds did not remain.

The memory substrate did not remain singular.

The topology and coordination methods changed.

The important distinction is that a mechanism can change without necessarily eliminating the function it was meant to provide.

But this cannot be assumed.

A replacement preserves an architectural relationship only if that relationship remains identifiable and sufficiently supported by evidence after the change.

#### Measuring Preservation Across Replacement

For an architectural property $\phi$, an implementation change from $Z_i$ to $Z_j$ can be evaluated through:

$$\boxed{  
\phi(Z_i;x,c)  
\overset{?}{\approx}  
\phi(Z_j;x,c)  
}  $$

where $x$ is a comparable source condition and $c$ represents the relevant task and runtime constraints.

The approximation criterion must be defined for the property under examination.

For routing, the criterion might concern adherence to the active decision rule.

For provenance, it might concern retention of source identifiers and traceable transitions.

For memory, it might concern recovery of specified information after a context boundary.

For semantic preservation, it must concern task-relevant meaning rather than superficial textual similarity.

This framework does not require different implementations to produce identical outputs.

It requires the evaluation to identify which relationship is being compared.

#### The Central Result

The surviving ZPP record supports a distinction between the continuity of an architectural objective and the continuity of a particular implementation.

Some mechanisms demonstrably changed.

Some implementation limitations are directly measurable.

Some previously reported results are available without their original test vectors.

Some architectural relationships recur across multiple versions.

And some important properties remain unresolved because the available evidence does not establish their runtime behavior.

This is not an empty result.

It identifies precisely where the architecture can be measured and where additional evidence is required.

---

### 13.16 What ZPP Measures—and What Remains Open

The purpose of this chapter has not been to prove that the Zero-Point Protocol eliminates semantic deviation.

The surviving record does not support that universal conclusion.

Nor does it support treating cryptographic validation, routing accuracy, information retrieval, and semantic preservation as equivalent measurements.

Instead, ZPP makes several relationships available for examination.

#### Routing Integrity

Does the implemented selection function behave according to the active feature definitions and boundaries?

The historical record provides both direct code-level evidence and reported routing outcomes.

It also provides an example of a route that was unreachable under its prototype configuration.

#### Measurement Integrity

Are the same properties measured using compatible definitions?

The reported cross-node entropy disagreement and the surviving implementation differences demonstrate why this question matters.

#### Processing Integrity

Does each operation preserve the task-relevant constraints that should survive it?

This requires examining reasoning, retrieval, verification, and transformation relative to the authorized task.

The historical architectural record identifies relevant mechanisms but does not provide complete semantic-trajectory measurements for every stage.

#### Continuity Integrity

Does required information remain available, attributable, and correctly usable after changes in context, memory, or runtime?

The historical movement from flat-file memory toward structured persistence provides implementation evidence.

Full continuity outcomes require corresponding execution comparisons.

#### Governance Integrity

Can consequential transitions be distinguished from unverified proposals, unauthorized changes, and incompatible lineages?

The cryptographic and consensus components provide mechanisms through which this relationship can be examined.

#### Release Integrity

Does the delivered result preserve the meaning, evidence status, uncertainty, and authorization conditions established during processing?

This remains an explicit architectural measurement target rather than a universally demonstrated property of every historical ZPP version.

#### Architectural Invariance

Which of these relationships survive when scoring, storage, model configuration, coordination, or transport mechanisms change?

The historical implementations provide comparison points.

They do not permit every candidate invariant to be declared proven.

---

#### The Boundary of the Present Measurement

The most important finding is that ZPP cannot be evaluated through a single success label.

A system may route an input correctly and still produce semantic drift.

It may preserve a document in memory but misuse its contents.

It may cryptographically verify a payload that contains an incorrect claim.

It may reach consensus on an invalid interpretation.

It may maintain network connectivity while losing the distinction between source and derivation.

And it may preserve all required information through internal processing before altering it at release.

These are different failure conditions.

They require different observations.

ZPP's architectural objective therefore demands a measurement structure that can separate them.

The historical study establishes the value of that separation.

It also establishes its limits.

The documented scoring revisions, feature definitions, agent tools, persistence mechanisms, consensus procedures, and distributed configurations show that the implementation changed.

The surviving code permits particular structural properties and defects to be examined.

The reported historical tests provide additional evidence, with the qualification that not every original execution record remains available.

What remains open is the degree to which the semantic trajectory itself was preserved under each configuration.

That question is distinct from whether the router executed, whether the signature verified, whether the memory database contained a record, or whether the node remained connected.

The relationship may be summarized as:

$$\boxed{ \begin{gathered} \text{Source and provenance} \\ \downarrow \\ \text{Reasoning, retrieval, and memory} \\ \downarrow \\ \text{Routing and verification} \\ \downarrow \\ \text{Coordination and protected state} \\ \downarrow \\ \text{Release} \\ \downarrow \\ \text{Observed semantic trajectory} \end{gathered} }$$

This is a conceptual arrangement of measurement boundaries, not a claim that every implementation executes them in this exact order.

The central question is whether the required semantic relationships survive the operations performed along the actual trajectory.

ZPP supplies the architectural framework for investigating that question.

But the architecture is not itself a numerical measure of semantic coherence.

A route label does not quantify drift.

A valid signature does not quantify semantic consistency.

A persistent memory record does not quantify the quality of reconstruction.

And successful execution does not establish that a transformation preserved what mattered.

To examine those properties across prompts, runtime intervals, transformations, and model boundaries, the study requires a separate measurement framework.

That framework must distinguish semantic displacement from necessary correction, processing overhead from justified intervention, recurrence from repetition, and stable preservation from temporary output agreement.

The next chapter therefore turns from the architecture through which information moves to the measurement of its semantic behavior.

The question is no longer only:

> **What did the system preserve structurally?**

It becomes:

> **How can we measure the coherence of what survived?**

$$\boxed{\textbf{Semantic Coherence Index}}  $$
