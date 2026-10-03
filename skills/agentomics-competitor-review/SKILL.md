---
name: agentomics-competitor-review
description: Review a paper or system against the Agentomics ML-model-building landscape and add, update, or move its canonical row in the Agentomics Competitors Google Sheet. Use for candidate reviews, entry re-reviews, landscape refreshes, taxonomy changes, or competitor summaries. Do not use for general biology-agent reviews unrelated to ML model creation.
---

# Agentomics Competitor Review

Maintain a clear, evidence-based comparison of systems that create, train, or improve ML models. Focus on mechanisms Agentomics could evaluate, not generic descriptions of agent capabilities.

Before working, read [references/schema.md](references/schema.md). It is the single definition of the categories, tab-placement rules, required fields, spreadsheet columns, evidence standard, and row acceptance test.

## Sheet and Default Action

The source of truth is the live [Agentomics Competitors](https://docs.google.com/spreadsheets/d/1iplGEc91Da4XRK-3GA16N7ChX1puceL7EbfpN2RXSTo/edit) Google Sheet, spreadsheet ID `1iplGEc91Da4XRK-3GA16N7ChX1puceL7EbfpN2RXSTo`. Use only its existing tabs:

- `Main Competitors`
- `Other Competitors & References`
- `Excluded`

When the user says to run, use, or apply this skill to a supplied candidate, add or update that candidate in the sheet without asking for another write confirmation. If the user asks only to preview, draft, discuss, or classify it, do not write.

When the user designates a working copy, that workbook is the source of truth for the task; keep the original read-only and never merge changes back implicitly. Otherwise use the default sheet above. Preview and regression-test runs must not write to either workbook.

Keep the final sheet limited to the three landscape tabs, with concise visible sources and no cell notes or comments. Keep detailed claim-level evidence in the local review record outside the workbook; report its path after writing. Do not add audit or testing tabs.

The selected live sheet overrides remembered or copied records. Do not create another spreadsheet, add a classification tab, rename headers, or change the taxonomy unless explicitly asked. If the sheet cannot be read or written, report the access problem instead of creating a replacement.

## Candidate Workflow

1. Read the current headers and system names from all three tabs, plus any possible matching row. Check the candidate's current name, former names, aliases, and successors before deciding that it is new.
2. Review the latest primary paper, relevant supplementary methods and figures, and official repository. Use supplied PDFs when web access fails, verify their title/DOI/version, and check for a newer preprint version or published successor. Use a named external benchmark when it supplies relevant evidence missing from the system's own sources.
3. Choose the output category and classification tab using the schema. Keep `Main Competitors` selective, retain useful lower-priority items in `Other Competitors & References`, and use `Excluded` only for out-of-scope or unreliable items.
4. Check the canonical fields against the source and record compact claim-level evidence before drafting the row. The evidence record and row together can cover those fields; do not duplicate them into another full prose record. Follow [references/extraction-review.md](references/extraction-review.md) for evidence, mechanism coverage, and shared terminology. Distinguish a checked source's silence (`Not reported`) from inaccessible or uninspected evidence (`Not verified`) and conflicting evidence (`Unresolved`).
5. Draft the columns required by the target tab as short comparison prose, then check the summary against the source's methods, contribution claims and failure analyses, not just against your extraction. Keep paper facts, external evidence, evidence limitations, and Agentomics recommendations distinct. Use the extraction-review workflow to check complete major mechanisms in E (`Main ideas`) and decision-changing caveats in D/G (`How it was tested` / `Evidence, limits and sources`), then perform its editorial pass; evidence or collapsed columns alone do not satisfy visible coverage.
6. Add, update, or move one canonical row. Preserve the target tab's formatting, validation, filters, and grouped columns. When moving a row, write and verify the destination before deleting the old copy.
7. Re-read the written row. Report the canonical system name, its tab and category, whether it was added, updated, or moved, and any important evidence limitation.

## Evidence and Writing

- Prefer primary papers and official repositories. Attribute external evaluations and author-reported results clearly.
- Explain what the system receives, produces, changes, evaluates, retains, and stops. Describe unfamiliar mechanisms through their behavior instead of relying on labels such as `MCTS`, `DAG`, `ReAct`, or `multi-agent`.
- Give numbers with their benchmark, denominator, evaluated model, budget, and evaluation setting; mark unestablished conditions with the appropriate missing-evidence status. Apply attribution and qualification to every retained result, including secondary examples and evidence-only numbers. Do not compare scores from mismatched settings without naming the mismatch.
- Write short, complete sentences. Avoid semicolon chains, slogans, repeated templates, and unsupported terms such as `state of the art`, `robust`, or `high autonomy`.
- Make `What Agentomics can learn` a concrete proposed change with a matched comparison or observable result that would show whether it helped.

## Optional Modes

- **Landscape refresh:** Use only when the user asks to check whether the whole sheet is current. Record a cutoff date, search recent primary systems and relevant official benchmarks, check backward and forward references, and deduplicate aliases and successors. A normal candidate review must not expand into an unsolicited landscape search.
- **Taxonomy change:** Use only when explicitly requested. Update the schema first, state which fields or placement rules changed, and re-review affected rows instead of mechanically renaming columns.
- **Competitor summary:** Build the summary from the live sheet and preserve the distinction between main competitors, useful references, and excluded items.

## Final Verification

- There is exactly one canonical row for the system.
- Its category, tab, fields, and sources satisfy the schema.
- Unsupported details are absent. Missing and conflicting evidence retains its actual status; an access failure is not proof that the paper lacks a method or evaluation.
- The writing is plain, specific, and separates evidence from Agentomics judgment. Every explanatory cell passes the plain-language reading check in `references/extraction-review.md`, not just the named examples or evaluation columns.
- Every factual statement has a source locator in the working evidence record; evaluation results name the evaluated system and configuration. Retain full locators in the local review record and concise primary links in the source column; do not add cell notes or comments.
- The mechanism coverage and attribution checks in `references/extraction-review.md` pass. Resolve uncertain details from sources or mark them as unresolved; ask a focused human question only when it would change the interpretation.
- The written row was re-read and the sheet's formatting and controls were preserved.
