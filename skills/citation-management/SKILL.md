---
name: citation-management
description: Find and verify scholarly sources, check that citations support claims, and create or repair bibliographies and BibTeX entries.
license: MIT
metadata:
  attribution: Adapted from the locally installed K-Dense Inc. citation-management skill.
---

# Citation Management

Work at the scope requested: locating one paper does not require a literature review. Use available search, retrieval, and bibliography tools; this skill does not bundle executable scripts.

## Find the right source

- Start from supplied papers, identifiers, claims, and the manuscript's existing bibliography. Use exact title or identifier searches for known works and subject-specific queries for discovery.
- Prefer original research, official datasets or repositories, and authoritative methods documentation for technical claims. Use reviews for synthesis and discovery while checking the primary evidence behind specific results.
- Select sources by relevance, methods, and evidential support. Citation counts and journal prestige do not establish that a source supports a claim.
- Use appropriate scholarly indexes and publisher records. DOI registries, PubMed, Europe PMC, and arXiv can help establish identity and versions. Search results alone are not evidence that a paper says something.

## Verify identity and support

- Confirm title, authors, year, venue, DOI or other identifier, and publication status against authoritative records. Do not invent missing metadata or infer a DOI from a title.
- Identify preprints, revisions, published successors, corrections, or retractions when relevant. Prefer the version supporting the cited claim; distinguish versions when results differ.
- Read the relevant methods, results, or discussion before claiming support. Record a useful section, table, figure, or page locator for non-obvious claims. Distinguish what the paper reports from your interpretation.
- If only an abstract is accessible, restrict claims to what it establishes and disclose that limit. Mark inaccessible or unresolved evidence explicitly; do not treat it as verified or absent.
- Preserve the conditions behind cited results, including the task, dataset, comparator, metric, and evaluation split. Match the citation to the sentence's actual claim.

## Maintain the bibliography

- Preserve established citation keys and the manuscript's bibliography conventions unless a change is requested. Retrieve metadata through authoritative export or content-negotiation facilities when available, then inspect it.
- Deduplicate using identifiers and verified title/author matches. Do not merge distinct papers or materially different versions just because their titles resemble each other.
- Keep BibTeX/BibLaTeX entry types and required fields appropriate to the existing toolchain. Preserve title capitalization where needed, encode names correctly, and check identifier and URL validity. Add no fabricated page numbers, issue numbers, or dates.
- Use installed parsers or the project's bibliography tools for structured edits when useful. Verify any proposed tool is actually available before issuing commands; add dependencies only when the task requires them.
- After changes, check that cited keys resolve, requested sources are present, and bibliography syntax remains valid. Run the existing document build when compilation is part of the task or needed to verify the edit.

## Deliver

Report the sources added or corrected, substantive support problems, and anything unverified. For systematic or reproducible searches, retain the queries, databases, dates, filters, and selection criteria appropriate to that task. For prose style, use `scientific-writing`.
