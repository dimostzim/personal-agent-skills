# Rewrite Patterns

Use these patterns to convert generic academic prose into the target manuscript style.

## Generic Field Importance

Weak:

`MicroRNAs are important regulators of gene expression, and accurate prediction of their targets remains challenging.`

Better:

`Although experimentally identified miRNA-target interactions provide positive examples, experimentally confirmed non-binding pairs are difficult to obtain, forcing many training datasets to generate negatives in silico.`

Pattern:

`Although [field/resource] provides [useful signal], [missing evidence/technical constraint] forces [imperfect workaround], which can introduce [failure mode].`

## Vague Model Improvement

Weak:

`Our model improves prediction performance and provides insight into functional targeting.`

Better:

`The pretrained target-site features improved transcript-level repression prediction over the same architecture trained from random initialization, indicating that site-level binding representations carry information relevant to functional repression.`

Pattern:

`[Design choice] improved [specific task] over [control], indicating/suggesting [calibrated mechanism].`

## Promotional Method Claim

Weak:

`This pipeline robustly solves alignment errors in homologous regions.`

Better:

`The pipeline reduces misalignment-driven false variant calls by assigning reads only when sequence-specific positions provide unambiguous evidence for their origin; reads without such evidence are reported separately rather than forced into a locus.`

Pattern:

`[Method] reduces [artifact] by [mechanism]; cases without [evidence condition] are [explicit uncertainty behavior].`

## Unsupported Generalization

Weak:

`These results show that the method generalizes well.`

Better:

`The improvement was observed across datasets generated from independent experimental protocols, suggesting that the model is not only fitting a single data source.`

Pattern:

`The improvement was observed across [independent settings], suggesting [limited generalization claim].`

## Hidden Tradeoff

Weak:

`The method improves variant calling in homologous regions.`

Better:

`The method increased precision by avoiding forced assignments in ambiguous regions, but this conservative rule reduced sensitivity because some true reads lacked unambiguous sequence-specific evidence.`

Pattern:

`[Metric A] improved because [mechanism], but [metric B] decreased because [tradeoff mechanism].`

## Review-Style Prior Work

Weak:

`Several models have been developed for this task, including CNNs, ResNets, and attention networks.`

Better:

`Several models have been developed for this task, but many were trained on datasets where negative examples were generated in silico, making their reported performance sensitive to artifacts in negative-sampling strategy.`

Pattern:

`Several [methods/resources] exist, but [shared assumption or limitation] makes [interpretation/evaluation] sensitive to [failure mode].`

## Empty Future Work

Weak:

`Future work should explore this further.`

Better:

`Future benchmarks should report results separately across experimental protocols, because the remaining performance differences may reflect protocol-specific interaction distributions rather than model architecture alone.`

Pattern:

`Future work should [specific action], because [observed limitation or unresolved alternative explanation].`

## Paragraph Repair Procedure

When rewriting a paragraph:

1. Underline the actual claim.
2. Identify any failure mode or constraint needed to understand the claim.
3. Explain the mechanism or design choice when relevant and supported.
4. Preserve or add the available evidence or comparison; flag missing facts rather than inventing them.
5. Remove promotional adjectives.
6. End where the paragraph's purpose is complete; use a consequence, tradeoff, or calibrated interpretation when it helps.
