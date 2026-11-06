Throughout this study, **operational failure is distinguished from experimental failure**.

A mechanism that produces degradation, interference, drift, instability, looping, continuity loss, or another unintended operational state does not by that fact constitute a failed experiment. In several phases of the research, mechanisms were introduced, layered, modified, removed, or replaced in order to expose the conditions under which semantic structure was preserved, degraded, recovered, or lost.

These failure states therefore form part of the experimental evidence. Their significance lies not only in whether a component performed its intended function, but in what became observable when that component altered the trajectory.

This distinction became particularly important during architectural experimentation. Additional intervention could improve one local property while degrading another; persistence mechanisms could preserve state without preserving trajectory continuity; measurement procedures could generate apparent cross-system disagreement; and verification or control mechanisms could introduce costs of their own. Removal or decomposition of such mechanisms was therefore not an attempt to erase unsuccessful development, but an additional experimental perturbation through which their effects could be compared.

**Disruption served a second experimental function.** Because the originating questions asked what happens when continuity is disrupted and what patterns remain, loss and degradation were not examined only as endpoints. They created conditions under which recovery, recurrence, and structural persistence could become observable. The experimental question was therefore not simply **what fails under perturbation**, but **what remains, returns, or reappears after the conditions supporting continuity have been altered or removed**.

\[ \boxed{ \text{operational failure} \neq \text{experimental failure} } \]

A failed mechanism may constitute a successful experiment when its failure is observable, attributable, and informative about the condition under investigation. Conversely, successful component execution does not by itself establish that the larger property being investigated has been preserved.

Failure, degradation, removal, and recovery are therefore treated throughout this study as **evidence-bearing state transitions** rather than merely implementation defects.

The later Destruction Protocol formalizes this investigative principle into prospective falsification procedures; its requirements are not retroactively attributed to exploratory observations conducted before those procedures were defined.