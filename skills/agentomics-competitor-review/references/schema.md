# Agentomics Competitor Review Schema

Schema version: `1.15` (plain-language checks across all explanatory cells; evidence requirements, categories and columns unchanged)

## Categories

Choose one category from the item's primary evaluated output. Categories must not overlap. Record search, memory, tools, validation, and agent arrangement separately under `Main ideas` and the detailed fields.

### Builds ML models

The system receives a dataset, ML task, repository, seed solution, or evaluator and produces or improves an evaluated model, model code, pipeline, predictions, or competition submission. This includes systems that create an initial solution and then improve it. Do not split `builds` and `improves` into separate categories when both are parts of the same ML workflow.

### Improves programs

The system improves general code or algorithms against an evaluator, but its primary evaluation is not an end-to-end ML model-building workflow.

### Runs research workflows

The system primarily plans, executes, records, or reports a broader scientific investigation. Its main evaluated output is a research process, evidence record, or paper rather than an ML model selected for a supplied dataset and metric.

### Provides tools or instructions

The item supplies an agent framework, typed tools, a skill catalog, reusable instructions, or another component used inside a workflow. It does not itself deliver the complete evaluated ML solution.

### Tests or trains ML agents

The item supplies tasks, an environment, a grader, training trajectories, or a controlled comparison for agents. It evaluates or trains builders rather than acting as the builder.

### Excluded

Use for commentary, reviews, social-media leads without a primary source, withdrawn or unreliable work, or systems outside ML model creation. Record why it was considered, why it was excluded, and when to reconsider it.

## Priority tiers and tab placement

Choose the output category above and the priority tier separately. The category says what the item produces. The tab says how useful it is to the current Agentomics comparison.

### Main Competitors

Keep this tab selective. A system belongs here when:

- it builds or improves ML models or pipelines, or has named external evidence that it can do so on Agentomics-relevant tasks;
- its mechanism and relevant results are supported by a primary source or a named external evaluation;
- it is a close domain match, adds a distinct supported mechanism, or provides a particularly useful comparable baseline; and
- it is worth close comparison now rather than being mainly redundant, evidence-limited, or impractical to test under Agentomics constraints.

Direct relevance alone is not enough. This tab is a reading shortlist, not a promise to implement one feature per row.

### Other Competitors & References

Use this tab for non-excluded items that remain worth keeping but should not lead the comparison. This includes:

- direct ML-building systems that substantially overlap a stronger main competitor;
- systems with promising ideas but limited, mismatched, very recent, or hard-to-reproduce evidence;
- systems whose compute or access requirements make a fair Agentomics comparison impractical now; and
- program optimizers, broader research workflows, tools, instructions, benchmarks, and training environments that inform part of Agentomics without being direct competitors.

### Excluded

Use this tab only when the item is outside the defined scope, lacks a usable primary source, is withdrawn or unreliable, or is only a secondary lead. Low priority by itself is not a reason to exclude an otherwise useful reference.

If evidence or project needs change, move the existing canonical row between tabs. Never copy it into a second tab.

## Canonical extraction record

Use these fields as a coverage checklist, not a requirement for a second narrative extraction table. Cover them in the compact evidence record and display row, referencing an existing claim when several fields use it. Keep `paper_fact`, `repository_fact`, `external_evidence`, and `project_inference` distinct in working notes.

| Field | Required extraction |
| --- | --- |
| `system` | Canonical system name and version. |
| `category` | One category above, chosen from the primary evaluated output. |
| `source_version` | Primary URL, publication or preprint version, and access or review date. |
| `input` | What the system receives, such as a dataset, repository, task statement, metric, or seed program. |
| `output` | What it produces, such as model code, trained weights, predictions, pipeline, environment, tool, or report. |
| `tested_domain` | Relevant ML or research domains only. Omit unrelated demonstrations. |
| `evaluation` | Benchmark or datasets, number of tasks, primary metric or success criterion, baseline, and budget. Use `Not reported` for missing parts. |
| `search_topology` | One solution at a time, several retained alternatives, tree, graph, population, parallel workers, fixed workflow, or no solution search. |
| `initial_candidates` | How roots, drafts, priors, retrieved implementations, or seed programs are produced. |
| `change_operators` | What changes in one iteration. |
| `selection_and_retention` | How the next candidate is selected, what is retained, and how pruning, merging, crossover, or backtracking works. |
| `stopping_condition` | Iteration limit, wall-clock or sample budget, convergence rule, fixed schedule, or `Not reported`. |
| `web_and_external_knowledge` | Whether live web, literature, repositories, databases, a curated knowledge base, or no external search is used. State when and for what decision. |
| `initialization` | Data inspection, requirement parsing, retrieved templates, skill creation, warm starts, pretrained models, or fixed seeds used before iteration. |
| `working_context` | What remains in active context during a run and how it is summarized or reduced. |
| `persistent_memory` | What survives a run, how it is retrieved, and whether cross-task benefit was evaluated. |
| `validation` | Syntax, import, execution, split, metric, hidden evaluation, repeated-run, held-out, or human checks. |
| `resources_and_budget` | Runtime, accelerator assumptions, parallelism, training limits, dependency isolation, and caches when reported. |
| `tools_and_execution` | Concrete tools and environments used to edit, run, train, inspect, retrieve, or publish artifacts. |
| `planning` | How goals become steps or experiment hypotheses and when the plan is revised. |
| `orchestration` | Agent roles, controller, scheduler, shared state, and information flow. A single agent is a valid value. |
| `human_role` | General setup and approvals separately from demonstrated human starting solutions, methodological guidance, interventions, expert curation, selection, and final verification. |
| `autonomy_condition` | When the system runs without intervention. Do not use an undefined Low, Medium, or High label. |
| `main_ideas` | Usually two to four short, plain-language behaviors. Preserve every distinct major mechanism relevant to ML model creation; do not omit one to meet a bullet limit. These are not mutually exclusive categories. |
| `limitations` | Source-reported algorithm or workflow failure modes and affected conditions, separately from evidence boundaries, benchmark mismatch, missing ablations, compute mismatch, source status and untested transfer. |
| `agentomics_inference` | A concrete Agentomics change and a matched check that would show whether it helped. |

## Main and reference display

Write every non-excluded item to `Main Competitors` or `Other Competitors & References` using the same 14 columns:

1. `System`
2. `Category`
3. `What it does`
4. `How it was tested`
5. `Main ideas`
6. `What Agentomics can learn`
7. `Evidence, limits and sources`
8. `How it searches`
9. `How it starts`
10. `What it remembers`
11. `How it checks results`
12. `What it can run`
13. `How work is organized`
14. `Human involvement`

Columns A:G are the default reading view. Columns H:N provide focused detail for their own comparison questions and may be grouped or collapsed in the sheet.

### Column rules

`Category` uses exactly one of the five non-excluded categories. Choose from the primary evaluated output, not a feature that also appears in other systems.

`What it does` states the input and output first. For ML builders, name the produced model, code, pipeline, predictions, or submission.

`How it was tested` identifies the evaluated system and configuration, benchmark, task count, metric or success criterion, and budget when available. Lead with the authors' relevant model-building evaluation; state when none is reported. Separate this from named external evaluation and do not substitute unrelated biomedical task scores.

`Main ideas` uses short behavioral phrases separated by bullets. Name the action, its object, and how the output is used. Explain what alternatives are retained, what information is remembered, or which checks are performed; generic phrases alone do not pass. Keep major relevant mechanisms visible here even when detailed columns explain them further.

`What Agentomics can learn` is project inference. Name a concrete Agentomics change and a matched comparison or observable result that would show whether it helped. On `Other Competitors & References`, keep the lesson conditional and do not turn every row into an implementation task.

`Evidence, limits and sources` gives the decision-changing limits and applicability conditions in short, separately grouped caveats, with primary links. Keep each qualification beside the claim it affects here or in `How it was tested`; do not repeat a fully qualified result already there. Preserve important named exceptions, but keep the complete defect inventory, secondary audit details and full locators in the local evidence record outside the workbook rather than this reading-view cell.

`How it searches` explains how alternatives are created, changed, selected, retained, and stopped. If the item does not search competing solutions, say so directly.

`How it starts`, `What it remembers`, `How it checks results`, `What it can run`, `How work is organized`, and `Human involvement` preserve the detailed comparison. Use `Not reported` when the relevant inspected sources are silent, `Not verified` for inaccessible or uninspected evidence, `Unresolved` for conflicts, and `Not applicable` only when the question genuinely does not apply.

## Excluded display

Use six columns:

1. `System`
2. `Type`
3. `Why it was considered`
4. `Why it was excluded`
5. `Reconsider if`
6. `Sources and decision`

One short sentence per explanatory cell is normally sufficient. Do not perform a full architectural extraction for an excluded item.

## Evidence rules

1. Prefer the latest primary paper and official repository.
2. Record the exact source version for evolving preprints and software.
3. Attribute author-reported results as author-reported.
4. Use external benchmark results only for the configuration and domain tested there.
5. A repository demonstrates availability and documented behavior, not comparative effectiveness.
6. Check relevant supplements and figures before an absence claim. `Not reported`, `Not verified`, and `Unresolved` distinguish source silence, incomplete inspection, and conflict; none proves a mechanism is absent.
7. Do not compare headline scores across different benchmarks, subsets, models, budgets, or submission rules without naming the mismatch.
8. Avoid secondary reviews for architectural claims when the primary system paper is available.
9. Keep withdrawn work from supporting factual conclusions.
10. Maintain claim-level source locators and run the mechanism coverage and attribution checks in [extraction-review.md](extraction-review.md). Preserve full locators in the local evidence record outside the workbook, with concise primary links in the evidence column. Do not add cell notes, comments or audit tabs.

## Row acceptance test

A `Main Competitors` or `Other Competitors & References` row passes only when a reader can answer:

- What does the item receive and produce?
- Why is it in this category?
- Where and under what conditions was it tested?
- What are its main ideas in plain language?
- For an ML builder, how are alternatives created, changed, selected, and retained?
- What context or memory persists?
- How are execution validity and result quality checked?
- Which agent or controller makes each decision?
- When must a human intervene?
- What concrete Agentomics change and matched check are proposed?
- Which claims are paper facts, external evidence, and project inference?

If the inspected source set does not answer one of these questions, retain the appropriate missing-evidence status rather than filling the gap with generic agent language.

Tab placement also passes only when a reader can state why the item is a current main comparison, a useful but lower-priority reference, or excluded. Reassess placement when a source, result, successor relationship, or Agentomics priority changes.
