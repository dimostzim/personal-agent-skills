# Scientific Explanation and Style

## Purpose

Write so that the reader can understand what was studied, follow why a method or comparison was chosen, and assess what the evidence establishes. The user's papers provide examples of evaluation logic; the thesis sources provide examples of sustained explanation. Neither establishes a universal template. Choose the document mode in [document-types.md](document-types.md) first.

## Build the argument in an understandable order

Start with the question, object, observation or definition needed for the passage. Background may establish a biological process, a computational setting or an unresolved question. Do not manufacture a failure mode to satisfy an outline.

Introduce concepts before using them to explain another concept. Give the intermediate reasoning needed to connect a result to its interpretation. One compressed sentence may need two or three sentences; necessary explanation is not filler. Conversely, do not re-explain a definition whenever its name recurs.

A paragraph can define, explain, justify, compare, report, interpret or qualify. These are possible functions, not quotas. A passage may need an example before its general statement. End when its purpose is complete; do not automatically attach importance, future impact or a repeated caveat.

Connect experiments and chapters through the scientific question. A partial answer may justify another test; another study may examine a complementary question. State that relationship without inventing a dependency or telling a false story of inevitable success.

## Explain methods through their operations

Name the inputs, outputs and transformations relevant to understanding the method. Explain consequential design choices, including when one choice creates a constraint that another component resolves. A list of components or adjectives does not explain their interaction.

When useful, start from the existing procedure and identify the exact change. Attribute borrowed methods, reproduced procedures and new extensions accurately. Preserve meaningful names, dimensions, thresholds and conditions.

For a repair or extension, explain what must remain unchanged and what the method is allowed to change. Distinguish a mathematically defined quantity from the estimator or algorithm used to compute it.

For mathematical exposition, identify the quantity and assumptions before relying on a formula. Interpret factors, units or limiting cases where needed. A numerical example can translate a parameter into its practical effect. Distinguish a definition, an exact result, an approximation and an implementation choice; a theoretical property does not automatically hold for a modified implementation.

Write the rationale at the level that changes scientific understanding. Do not turn a manuscript into a history of file names, debugging or internal checks. Exhaustive settings can belong in a table or supplement, with the selection rule and its rationale in the main account.

## Make evaluation part of the explanation

Explain the comparison's purpose: what changes, what is held constant, why the control is informative, and what competing interpretation it addresses. State what the metric measures and the assumptions needed for its interpretation. A change in score can arise from a change in task difficulty, population or label definition; do not assign a cause without the needed comparison.

Keep distinct where relevant:

- training objective, model-selection criterion and test metric;
- training, validation, internal resampling and external evaluation;
- successful execution, predictive quality and experimental confirmation;
- performance evidence and evidence about a mechanism;
- model performance and data or tuning resources used to obtain it;
- biological objects and tasks, such as site recognition, transcript response and precursor classification;
- a real observation and an illustrative or simulated example.

Do not pool incompatible metrics or describe unequal conditions as matched. Explain displayed-setting selection, aggregation, uncertainty and exclusions when they affect interpretation. If failed runs are excluded in an additional summary, name the failures and changed denominator; that summary is conditional, not overall reliability.

Separate the target outcome from a proxy, internal diagnostic or component score. A better component need not improve the complete system. State the level of an equivalence or guarantee: per-sample identity, expected behavior, asymptotic convergence and empirical performance are different claims.

Retain results that challenge the proposed account. Identify the specific observation that a candidate explanation fails to explain. Report null comparisons when they answer a scientific or practical question. Absence of a detected difference does not prove equivalence. An unresolved mechanism should remain unresolved rather than acquire a plausible invented explanation.

For an unexpected result, make the expectation, observation and relevant alternative explanation clear. Describe the discriminating check if one was performed. Matched cases where an effect is absent can define its boundary; do not invent such checks to improve the narrative. Preserve a competing method's relevant advantage even when the proposed method leads the reported comparison.

## Calibrate the claim

Use direct language for direct evidence: `we measured`, `I compared`, `the model achieved`, `the experiment showed` as appropriate to document type. Use `suggests` or `is consistent with` for an interpretation, and `may` or `could` for an untested possibility. Avoid both unsupported certainty and multiple layers of hedging around a clear observation.

State what a method improves, over which comparison, under which conditions. `Robust`, `generalizable`, `novel` and `state-of-the-art` require a precise meaning and supporting evidence; replace them with the actual result when that is clearer. Do not translate a gain in one metric into an overall claim of superiority.

Keep tradeoffs concrete. Name the cost, exception or operating condition. Check whether effort or error was transferred elsewhere rather than removed. Put a qualification where it changes interpretation, then avoid repeating it mechanically in every paragraph.

Separate demonstrated components from an untested combination, and completed contributions from the longer-term research aim. Future work should follow from a specific unresolved question or constraint, not generic claims that more research is needed.

## Use stable terms and ordinary scientific language

Keep one name for the same concept. Repetition of a technical term is preferable to an ambiguous pronoun or a new synonym. Define local usage when the literature uses a term in several ways. Related objects must remain distinct.

Use concrete subjects and verbs: a model predicts, a script computes, an experiment compares, an author measures. Passive voice is useful when the actor is irrelevant or the object should remain the subject; do not ban it mechanically. Avoid dense strings of abstract nouns when verbs can show what happens.

Remove ornamental metaphors, grand declarations, vague importance claims and promotional endings. Phrases such as `unlocks the potential`, `powerful framework`, `sheds light`, `bridges the gap` and `paves the way` usually conceal the operation or result. A term with a precise scientific meaning is not forbidden merely because it is sometimes overused.

Plain language does not require uniformly short or syntactically simple sentences. When consecutive sentences develop one idea, use coordination, relative clauses or subordinate clauses to express genuine relationships among examples, conditions, methods and findings. Retain useful short statements and parallel definitions; do not lengthen sentences merely for variety.

Review repeated `short claim: evidence` constructions and one-line aphorisms when they make prose read like a list. Integrate the explanation where clearer, retaining colons for useful lists, definitions or focused examples. A connector must express a relationship the source supports; never add `because`, `therefore`, `while` or `whereas` solely to vary rhythm. Do not change terminology, add typos or force uneven prose to simulate a human voice.

## Review and revision

Preserve passages that already teach the concept or report the evidence well. Identify the actual reader difficulty before rewriting: undefined object, missing reasoning, ambiguous comparison, unsupported claim, repetition or unclear ownership. Revise that difficulty rather than polishing every sentence into the same rhythm.

Before delivering a substantial edit, compare it with the source for changes in results, numerical values, uncertainty, citations, scope, authorship and research status. Flag missing scientific information; do not fill the gap with invented detail or imply that new analyses were performed.
