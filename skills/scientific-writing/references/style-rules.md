# Style Rules

## Contents

- Target Style
- Source Style Fingerprint
- Scientific Argument
- Paragraph Logic
- Claim Calibration
- Evaluation Logic
- Prior Work
- Conceptual Distinctions
- Tone and Vocabulary
- Sentence Style

## Target Style

The target style is not generic polished academic prose. It is scientific reasoning written as a sequence of constrained decisions.

The user's manuscripts repeatedly follow this structure:

1. A useful technology, model, dataset, or experimental protocol exists.
2. A specific artifact or limitation makes the default interpretation unsafe.
3. Existing approaches partially address the issue but leave a measurable gap.
4. The study introduces a method, dataset, benchmark, or model that acts on that gap.
5. The evaluation tests whether the gap was reduced, using controls and baselines.
6. The result is interpreted with tradeoffs and limitations, not only with performance claims.

Write toward this structure even when the topic is not miRNA, read alignment, or agentic ML.

## Source Style Fingerprint

This skill is based on recurring writing patterns in the user's manuscripts: `ParaDISM`, `pre-miRBench`, `miRBench`, `miRBind2`, and `Agentomics`. See [paper-style.md](paper-style.md) for sources and calibration. Preserve their scientific argument while following the user's explicit preference against flowery or promotional language.

The style is recognizable by:

- a broad opening only when it quickly narrows to a concrete technical bottleneck;
- named failure modes, such as frequency bias, misalignment artifacts, ambiguous placement, leakage, or metric hallucination;
- methods justified by what they prevent, isolate, or make measurable;
- explicit task definitions before model or pipeline details;
- evaluation designs that use controls to remove the key signal;
- metric choices justified when common metrics can mislead;
- results interpreted as evidence for or against a mechanism, not only as performance;
- direct acknowledgement of tradeoffs, especially precision vs sensitivity, dataset quality vs size, and validation vs hidden test performance;
- limitations stated as specific operating constraints rather than generic future-work language;
- availability statements for code, data, models, packages, or web tools.

The style is assertive when the evidence is direct and cautious when the claim is interpretive. It avoids decorative transitions and does not use generic academic filler to sound important.

## Scientific Argument

Across the scientific argument, make the relevant relationships clear:

- why the usual approach is insufficient;
- what failure mode matters;
- what the study changes;
- how that change is supposed to work;
- how the study tests whether it worked;
- what remains unresolved.

Use background to establish concepts, context, or a methodological or interpretive decision. Avoid an unrelated literature survey; do not remove context that the intended reader needs.

Strong scientific moves:

- "This artifact can inflate performance without learning the biological interaction."
- "This metric is misleading in this setting because the negative class dominates."
- "The method assigns reads only when unambiguous sequence-specific evidence exists."
- "The left-out set tests whether performance transfers to families absent from training."
- "The gain is moderate but consistent across independent protocols."

Weak scientific moves:

- "This remains an important challenge."
- "This provides valuable insights."
- "This method is powerful and robust."
- "Future research is needed."
- "The model improves performance" without saying where, over what, and by how much.

## Paragraph Logic

A paragraph should have one primary job:

- define a task;
- explain a failure mode;
- distinguish related concepts;
- justify a design choice;
- describe a reproducible method step;
- explain a metric or baseline;
- interpret a result;
- state a tradeoff;
- limit a claim.

Preferred paragraph structure:

1. Topic sentence with the specific claim or problem.
2. Mechanistic or methodological explanation.
3. Evidence, comparison, or example.
4. Consequence for the study.

Avoid a vague importance claim at the end. A consequence, study action, or calibrated interpretation can provide a useful ending when it fits the paragraph's purpose; do not add one mechanically.

Good endings:

- `This isolates frequency imbalance from the interaction signal.`
- `Therefore, precision and sensitivity are more informative than specificity for this comparison.`
- `This suggests transfer across experimental contexts rather than overfitting to a single data source.`
- `Unassigned cases are reported separately instead of being treated as confident negatives.`

## Claim Calibration

Match the verb to the evidence.

- Use `show` or `demonstrate` only for directly tested claims.
- Use `suggest`, `indicate`, or `is consistent with` for interpretations.
- Use `may`, `can`, or `could` for untested mechanisms or applications.
- Use `we found`, `we observed`, or `we measured` for empirical results.
- Use `we hypothesized` only before testing.

Do not claim:

- `generalizable` from one dataset;
- `robust` without independent tests or a precise meaning;
- `state-of-the-art` without named current baselines;
- `better` when the method improves one metric but worsens another.

Say:

- `moderate but consistent improvement`;
- `higher precision at the cost of lower sensitivity`;
- `no conclusive answer, but reduced confidence in the artifact-prone interpretation`;
- `consistent with transfer of learned representations`;
- `limited to the tested datasets and model class`.

## Evaluation Logic

Evaluation is part of the argument.

Across the relevant evaluation passage, explain the applicable items without repeating them in every paragraph:

- what hypothesis or failure mode is being tested;
- which data were used;
- why the baseline or control is appropriate;
- which metric is primary;
- why that metric is valid for the task;
- what result was observed;
- what alternative explanation remains.

Use controls that remove the key signal:

- model with only one side of an interaction;
- random classifier;
- same architecture without pretraining;
- standard method without the corrective step;
- hidden test set;
- left-out family, sample, protocol, or benchmark.

Prefer multiple independent tests before claiming generalization:

- different datasets;
- different protocols;
- simulation plus real benchmark;
- case study after quantitative benchmark;
- external or hidden test set.

Always distinguish:

- train vs validation vs test performance;
- validation score vs hidden test score;
- binding prediction vs functional prediction;
- placement vs downstream calling;
- dataset size vs dataset quality;
- sequence-only prediction vs engineered-feature prediction;
- ambiguity vs negative evidence.

## Prior Work

Organize prior work by constraints, not chronology.

Useful moves:

- `Existing tools solve X but assume Y.`
- `These datasets provide positives, but negatives must be generated in silico.`
- `This model uses engineered features, whereas the present question is whether sequence alone is sufficient.`
- `Long-read sequencing reduces ambiguity, but specialized disambiguation may still be required.`
- `Prior agentic systems can generate code, but reusable artifacts and leakage-resistant evaluation remain unresolved.`

Avoid citation lists that do not lead to a decision. If several methods share a limitation, group them and give one concrete example.

## Conceptual Distinctions

Spell out distinctions when they matter.

Examples:

- Binding site prediction is not transcript-level functional repression prediction.
- Read placement is not variant calling.
- Specificity is not precision in imbalanced settings.
- Larger datasets are not automatically better datasets.
- Sequence-only models answer a different question from feature-engineered models.
- Ambiguous placement is not a confident negative result.
- Benchmark performance on a biased split is not evidence of biological learning.

Pattern:

`A answers [question 1], whereas B answers [question 2]. This distinction matters because [evaluation or biological consequence].`

## Tone and Vocabulary

Use plain scientific language. Remove ornamental metaphors, grand declarations, decorative transitions, and claims of importance that add no scientific information. Replace them with the actual action, mechanism, result, or limitation. Preserve necessary technical terms and supported strong claims. Prefer stable terminology to elegant variation; precision matters more than novelty of phrasing.

Prefer operational verbs:

- measure
- evaluate
- compare
- test
- isolate
- control
- correct
- mitigate
- assign
- align
- filter
- quantify
- benchmark
- retrain
- transfer
- validate

Use promotional words only when the evidence supports them:

- `novel`: genuinely new dataset, method, representation, or pipeline.
- `state-of-the-art`: benchmarked against named current methods.
- `robust`: tested across independent settings or used in a precise statistical sense.
- `generalizable`: evaluated on independent or left-out data.
- `comprehensive`: broad scope is specified.

Avoid:

- powerful
- promising
- unlocks
- bridges the gap
- sheds light
- provides insights
- paves the way
- revolutionary
- seamless
- important challenge, unless immediately made specific

## Sentence Style

Use information-dense sentences. Long sentences are acceptable when they carry exact conditions, comparisons, or caveats.

Mix:

- short sentences for claims;
- longer sentences for methods and qualifications;
- medium sentences for interpretation.

Avoid repeated sentence starts, especially `This`, `Furthermore`, `Moreover`, `In addition`, and `It is important to note`.

Transitions should carry logic:

- `However` for real contrast.
- `Consequently` for consequence.
- `Accordingly` when a result follows from a design choice.
- `In contrast` for comparison.
- `Because` for mechanism.
- `Therefore` only when the conclusion follows directly.
