# Section Patterns

## Contents

- Abstract
- Introduction
- Methods
- Results
- Discussion
- Conclusion
- Figure Captions

## Abstract

Use a compact problem-to-evidence chain:

1. Domain.
2. Specific bottleneck or artifact.
3. Consequence for model, pipeline, diagnosis, or interpretation.
4. Introduced resource and mechanism.
5. Evaluation scope.
6. Quantitative result.
7. Availability if relevant.

For structured abstracts:

- `Motivation` or `Background`: field context plus exact bottleneck.
- `Results`: method/resource, mechanism, evaluation, numerical result.
- `Availability`: package, code, model, data, or web tool.
- `Conclusions`: measured advance plus practical interpretation.

Avoid:

- broad importance without a failure mode;
- `challenges remain`;
- `novel robust framework` without mechanism;
- no numbers when results exist.

## Introduction

Move from field context to technical decision.

Preferred progression:

1. Establish setting.
2. Define the relevant mechanism or prediction task.
3. Describe current approaches.
4. Identify the concrete limitation, bias, artifact, ambiguity, or missing capability.
5. Explain why it matters downstream.
6. Show why existing approaches do not remove it.
7. State the study intervention and what it tests.

The last paragraph should state actions, not aspirations.

Good last-paragraph pattern:

`In this study, we [introduce/curate/evaluate] [resource], which [mechanism]. We evaluate it using [datasets/baselines/controls] and test whether [failure mode] is reduced.`

## Methods

Methods should read as reproducible execution.

Include when applicable:

- dataset names, sources, versions, and access dates;
- inclusion, exclusion, and filtering logic;
- train, validation, and test split logic;
- exact inputs and outputs;
- thresholds and parameters;
- model architecture and optimization details;
- baselines and controls;
- metric definitions and statistical tests;
- what was hidden, held out, or protected from leakage.

Define tasks operationally:

- `Given X, predict Y.`
- `For each sample, compute Z.`
- `A read/item/example is assigned only if conditions A and B are met.`

When a method has a failure state, name it. The user's papers often make conservative uncertainty explicit rather than hiding it.

## Results

Use claim headings.

Good heading forms:

- `[Artifact] can affect [task] performance`
- `[Method] corrects [identified failure mode]`
- `[Representation/pretraining/design choice] improves [specific task]`
- `[Pipeline] mitigates [artifact]`
- `[System] produces [validated artifact]`

Each subsection should:

1. State the test purpose.
2. Describe setup.
3. Name baseline or control.
4. Report result with numbers.
5. Interpret result mechanistically or statistically.
6. State caveat, tradeoff, or remaining ambiguity.

Do not just state that performance improved. Say what the result rules in or rules out.

Good result moves:

- `To evaluate whether...`
- `As a baseline...`
- `This model cannot learn [missing signal], so above-random performance indicates [artifact].`
- `The improvement was consistent across...`
- `The lower sensitivity reflects...`
- `This result is consistent with...`

## Discussion

Synthesize rather than repeat.

Progression:

1. Main finding.
2. Why it matters for the task.
3. Mechanism suggested by the evidence.
4. Tradeoff.
5. Concrete limitations.
6. Future work tied to limitations.

Concrete limitations are preferred:

- single model backbone;
- one input format;
- one reference set at a time;
- limited hardware or runtime;
- possible remaining dataset-specific effects;
- false negatives under specific evidence conditions.

Avoid boilerplate limitations.

## Conclusion

Return to the failure mode and evidence.

Conclusion pattern:

`[Resource] [does action] by [mechanism]. Across [evaluation scope], it [measured result]. This supports [calibrated interpretation], while [specific limitation/tradeoff] remains.`

Avoid ending with generic potential or broad future impact.

## Figure Captions

Captions should explain what is compared and why it matters.

Include:

- dataset or experiment;
- axes, rows, columns, or panels;
- metric definitions when needed;
- primary visual interpretation;
- what ambiguity, artifact, or tradeoff the figure shows.

Do not write captions that only name plot elements.
