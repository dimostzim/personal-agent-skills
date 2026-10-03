# Extraction and review

Read this before extracting or revising a non-excluded system. Keep the existing taxonomy and columns unless the user requests changes.

## Evidence before summary

Use the live row as a list of claims to check, not as evidence. Verify identity and version across same-named systems, preprints, publications and supplied files. Read the primary methods, architecture figure and caption, relevant experiments, and appendices that explain implementation. Inspect supplementary figures as well as searchable text: a model-building case study may appear only there. A reproducibility checklist is an author declaration and locator, not independent validation of the underlying experiment. Check the current official repository and source version. An abstract or search snippet is insufficient for a mechanism claim.

In working notes, attach each factual claim to:

- `kind`: `paper_fact`, `repository_fact`, or `external_evidence`;
- `subject`: the system and version the claim describes;
- `claim`: one checkable statement;
- `source`: URL and exact paper version or repository revision;
- `locator`: section, figure, table and row, or file and symbol;
- `support`: a short paraphrase of the supporting evidence, including any contradiction or uncertainty.

Keep `project_inference` separately and link recommendations to the mechanism that motivates them. Do not treat proposed Agentomics behavior as something the competitor implemented. Label observed code behavior as `repository_fact` with its revision; a prompt requesting a behavior is not proof that execution enforces it. Retain full source locators in the local evidence record outside the workbook and concise primary links in `Evidence, limits and sources`. Do not add cell notes, comments or a second canonical database.

Keep one compact evidence record per claim. Define shared source/version metadata once, then use a short claim, locator, and any material qualification. Use that record to check field and mechanism coverage without adding duplicate canonical, coverage, and display-to-evidence prose tables. Draft visible cells to answer their own comparison questions concisely, selecting the relevant evaluation, major mechanisms and decision-changing limits. Keep the evidence complete and visible cells readable without evidence IDs or a second extraction ledger in H:N. Keep material conditions, selection, retention and stopping in the search summary; make `How it checks results` summarize checks and `What it can run` capabilities, without repeating protocol and execution inventories across cells. Put secondary procedures, parameters, scores, exact code symbols, minor source conflicts, routine configuration, setup commands, access history, non-decision-changing missing fields and policy inventories, and supporting locators in the local evidence record when they would overwhelm the summary. Retain the context needed to interpret any retained score. If an inherited row height clips the preview, remove repetition and secondary detail without dropping required mechanisms or caveats or imposing a hard text limit. Once the source-supported row is ready, save it and its evidence before optional elaboration; never skip source checking to meet a time limit.

For each evaluation, record **who evaluated which system**, on what tasks, with which model, budget, metric, and result. Keep author evaluation separate from named external evaluation. Check table headers, row labels, footnotes, and whether the result measures completed execution, prediction quality, or an aggregate benchmark score. A result for one system cannot describe another just because both occur in the same paper. Do not silently combine an older system's results with a successor's architecture.

In `How it was tested`, lead with the system authors' relevant model-building evaluation. If none is reported, say that explicitly; do not fill the cell with unrelated QA or wet-lab headline scores. Include an external result only when it directly evaluates this system on relevant ML tasks, and identify the evaluator and tested configuration. Place secondary context and comparability limits in the evidence column. Keep decision-changing comparison exceptions explicit: name the affected baseline and its differing configuration, evaluation protocol, or result provenance rather than saying only that configurations differ. Distinguish authors' approximate budget matching from verified equal total compute, and state the source's publication status explicitly.

## Evaluation scope and evidence conflicts

Check official errata and repository Known Issues for defects affecting labels, splits or grading, not only availability notices. Record each affected task/version and consequence in evidence. In D/G, group related defects by consequence, retain relevant named examples and any exception that changes interpretation of a displayed result, and state the bounded implication. A generic contamination warning is insufficient, but an exhaustive task-by-task catalog belongs in the local evidence record, not the reading view. Keep standardized published results separate from a cleaned subset or corrected rerun, with any changed denominator explicit.

Read source-reported failure analyses and limitations alongside the mechanism description. Preserve adverse algorithm or workflow behavior and the conditions in which it occurs, separately from benchmark defects, cost and missing evidence. Naming a search policy or architecture does not explain its reported failure mode. Put decision-changing intrinsic limitations in D/G even when external-evaluation caveats are numerous.

For every retained result, including secondary examples and numbers only in local evidence records, trace **system/version → model and stage → data available at each stage → selection rule → final metric**. Attach that result's own qualifications, including an unestablished evaluated backbone, run budget or selection-versus-final-test boundary; a comparator's configuration or a neighboring result's caveat is not a substitute. Omit an optional score or example if its conditions cannot be preserved, while retaining required evaluation-design facts. Distinguish developing the agent or its knowledge extractor from the agent training a downstream model, and using a pretrained predictor from fitting or fine-tuning one. A research-workflow system can contain a real model-building case study without its broad primary category changing.

- Identify training, validation and final-test data, and whether a score is used for monitoring, candidate selection, repeated revisions or final reporting. Preserve observed repeated evaluation or monitoring at the relevant stage in D/G, separately from uncertainty about selection use or safeguards. A dataset called held-out is not an untouched final test if it is repeatedly used to choose changes. If train/test separation or contamination controls are not described, say so; do not infer leakage or assume clean separation.
- Apply separation checks to each training stage retained in the summary, including agent or auxiliary-model training, even when its scores are omitted. Attach the appropriate uncertainty to that stage rather than substituting a different downstream case's split limitation.
- Name the evaluated backbone and role, task subset, execution budget, repetitions and aggregation when reported. Distinguish one pass, best-of-N, warm reruns, pooled campaign coverage, macro/micro averages, and exclusions from a comparator's denominator. Record source-reported prompt sensitivity and variability across independent full runs; targeted confirmation or partial reruns do not establish full-run reproducibility. An equal per-run timeout is not equal total search compute.
- Distinguish planned or simulated scores, successful execution, proxy predictions and measured held-out performance. Retain an author case study as such when endpoints, sample count or test protocol are incomplete; do not upgrade it into a controlled benchmark or hide it behind an unrelated QA score.

When sources disagree, preserve both scoped claims and their locators. A paper may describe a separate retrieval LLM while a particular released implementation passes the main agent's model. Report this as a paper/code configuration conflict, not proof that either configuration was used for the published experiment. Reconcile paper, figure, appendix and repository metrics only when versions, populations, filtering and run provenance match; otherwise omit a disputed headline and state the unresolved difference. Do not silently choose the largest or newest-looking number.

Correct an extraction error in the row. Retain a useful system with qualified evidence when a result is mismatched, incomplete or failed; omit an invalid comparative score rather than automatically excluding the whole system. Exclude only under the schema's scope/reliability criteria. Separate failures generated and repaired during a competitor run from errors in our summary or invalid final evidence.

## Preserve the important mechanisms

Before drafting `Main ideas`, list the source's main contributions and the operations that make the ML workflow work, including relevant documented optional capabilities. Check initialization and external retrieval, creation of candidates, code changes, selection and retention, validation, memory, tool execution and planning. Prioritize major capabilities over minor implementation details, and label optional scope without implying benchmarked effectiveness. These are coverage prompts, not requirements that every system implement each one.

Describe each relevant mechanism as **actor → action → object → output/use**. For example, identify which agent searches repositories, what it extracts, and how the resulting code or instructions are used during model building. Name the changed pipeline block rather than saying “component.” Preserve the stage or trigger in the visible summary phrase when ordering changes the mechanism's meaning. For a prominent multi-stage mechanism, make every distinct stage and consequential failure transition recoverable from E, combining related stages into one short behavioral bullet when useful. A role list, a neighboring operation or only the last stage does not substitute for the whole mechanism; detailed columns provide elaboration rather than missing stages.

Verify control-flow ownership from the architecture or algorithm rather than inferring it from role names. Distinguish framework-defined stages and controller transitions from an agent's planning within a stage. Before saving, check prominent actor/action pairs against those sources and keep any decision-changing metric-denominator conflict beside the displayed rate, not only in local evidence records.

Inspect task prompts and demonstrated cases when assessing human involvement. Distinguish general task/setup prerequisites from actual human contributions to evaluated runs: provided or improved starting solutions, model recipes and methodological guidance, intermediate analysis, selection or final expert verification. Running without per-step approval is different from independently designing the scientific workflow. Keep demonstrated contributions that qualify a result beside it in D/G, not only in detailed columns or evidence; generic seed or evaluator requirements do not substitute for those contributions.

Use the existing evidence record to map each major relevant mechanism to a phrase in E and its detailed column, and each decision-changing caveat to D or G beside the claim it qualifies. Include conditions from detailed fields, such as human dependence, evaluator requirements and reproduction limits. For supporting probes or checks, name the system/model actually tested and what the findings leave unresolved beside the displayed result they qualify. Bounded findings do not certify the absence of subtler failure modes or generalize to other or future configurations; a caveat about a different limitation does not substitute for this scope boundary. If a mechanism is omitted, record why it is irrelevant, redundant, or unsupported. Do not let a short bullet limit remove a distinct major mechanism. Read A:G on its own, then check it against the source's methods and architecture again: could a reader recover the important mechanisms and conditions that limit the result without opening collapsed columns or local evidence records?

Separate implementation from effectiveness. A method can implement retrieval without an ablation proving retrieval improves scores. State the mechanism confidently when supported, but qualify the claimed benefit when it was not isolated experimentally. An extension omitted from the main benchmark may still be demonstrated in an appendix; retain the supported mechanism without attributing its benefit to the benchmark results.

Before saving, make a separate editorial pass over D/G. Group independent caveats into short bullets or paragraphs and keep each group's consequence clear. Move secondary examples, repeated results and access/provenance inventories to the existing local evidence records; retain affected comparator names, important defect examples and all qualifications that change the displayed claim. Do not shorten by deleting a required mechanism or failure mode, or by replacing a specific issue with a vague warning. If the cell still reads like an audit transcript, reorganize it rather than append another summary.

## Plain-language reading check

Before publication, read every explanatory cell in C:N (C:F for exclusions) as an ML-literate reader who has not read the paper. Do not limit this pass to evaluation caveats.

- Replace paper-specific shorthand with the action it describes: who chooses or changes what, using which information, and what happens next. If a technical name is useful for source matching, give the explanation first and retain the name in parentheses.
- Explain unfamiliar abbreviations, symbols and overloaded words at their first relevant use. Keep model names, software identifiers and source versions exact. Do not expand familiar terminology mechanically or introduce nested, repeated definitions.
- Use the same term for the same concept across rows, but preserve real differences: model training is not agent training, a validation score is not a final-test score, and an execution check is not a quality guarantee.
- Split dense cells into short behavioral bullets or logically grouped paragraphs. Do not substitute vague prose for a precise mechanism, remove a major stage, or move decision-changing conditions out of the visible reading view.
- Compare the edited cell with its evidence and previous wording. Preserve numerical results, denominators, models, budgets, selection rules, human contributions, uncertainty and sources. Check grammar after terminology changes; blind synonym replacement is not a completed editorial pass.
- If a phrase cannot be explained confidently from the evidence, re-check that phrase's source or retain explicit uncertainty. Do not invent a definition to make it sound simpler.

## Shared terminology

Use these meanings consistently and explain paper-specific terms at first use in the visible cell; put longer explanations in the local evidence record. Preserve real differences between systems rather than forcing them into the same mechanism.

| Term | Meaning to make explicit |
| --- | --- |
| Candidate pipeline | An executable proposed ML solution, including its preprocessing, model, and training code. |
| Pipeline block | A named part of that solution, such as feature preprocessing, model training, or combining predictions. |
| Ablation | Removing or disabling a named part and re-evaluating under the same setup to measure the score change. State the actual intervention used by the paper. |
| Tree search | Retaining candidate pipelines with parent–child links. Explain how parents are selected and what a child changes. |
| Skill | A paper-specific reusable artifact. Specify whether it contains instructions, executable code, dependency setup, or examples. |
| Workflow template | Reusable instructions or a sequence of steps, rather than an executable tool or trained model. |
| Tool | An executable function, program, or API interface with specified inputs and outputs. |
| Working context | Information made available to the agent during the current run. |
| Persistent memory | Information retained for subsequent runs. Name what is stored, how it is retrieved, and whether cross-task benefit was tested. |
| Execution check | A check that code imports or runs and produces expected artifacts; it does not establish predictive quality. |
| Validation score | The metric used to choose among candidate models. Distinguish it from the final held-out test score. |
| Completion rate | The fraction meeting a stated execution or delivery criterion; it is not prediction accuracy. |

## Acceptance and focused human review

A row fails review if a factual statement lacks support, a result has an ambiguous subject, a major relevant mechanism is absent from E, a decision-changing caveat is absent from D/G, or a key phrase cannot be explained without guessing. Re-check the source before replacing uncertainty with fluent prose. For preview-only requests, validate the proposed row and evidence; skip writes and post-write checks.

Preserve claim scope when compressing working evidence into cells: `not checked in this review` does not mean unavailable elsewhere. Before saying a detail is `Not reported`, check relevant examples, figures, and appendices; distinguish an unspecified general policy from a documented case. For branching mechanisms, preserve the condition and fallback in the relevant detailed column, not only the action list.

When evidence remains ambiguous, distinguish `Not reported` (relevant sources inspected but silent), `Not verified` (access or inspection incomplete), and `Unresolved` (conflicting evidence). A human review should ask about that precise mechanism or interpretation, showing the source locator and draft sentence. Do not require a questionnaire for every paper.

When revising this skill after extraction failures, use source-checked expected facts and acceptable uncertainty states for the repaired examples, plus a system outside those examples. Do not use the current sheet as factual ground truth. When an independent agent is available, give it the revised skill, a realistic preview-only candidate request, and raw sources without expected answers, corrected rows or prior summaries. Require the same fourteen-column output, compact evidence locators and no live writes. Judge factual attribution, visible mechanism coverage, evaluation scope, readable cells and a concrete matched Agentomics check, not exact wording. Record failures, repair only demonstrated gaps, and rerun affected cases. Report behavioral tests separately from frontmatter validation and competitor execution; passing these checks is not a guarantee of factual accuracy.
