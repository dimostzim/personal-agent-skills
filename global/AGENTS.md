## Blocking issues

If an expected capability is blocked—for example, installing a dependency,
running a subagent, reading a file, searching the web, or committing or pushing
changes—tell the user promptly and ask for help. Do not silently substitute a
lower-quality approach or report incomplete validation as sufficient merely to
avoid inconveniencing the user.

## Missing packages

If you intend to use a library, package, or some piece of software, and its not available locally, download it and install it. Don't re-implement tools just because they are not locally available, assuming you have internet access to download and install them.

## Terminology

Do not create multiple names for the same thing - be consistent. For example

- Retained cells passing both GEX and ATAC QC
- pass_RNA_QC == TRUE AND pass_ATAC_QC == TRUE
- Retained barcodes satisfying the relevant RNA and ATAC thresholds
- RNA and ATAC conditions were applied to the same paired object, leaving cells that passed all conditions

are all the same thing, but worded differently. Avoid such expressions, prefer to repeat the same thing over and over if it means the same thing. In general prefer clarity (much more important) over nice language flow.

## Commits and pushes

Commit only when the user explicitly requests a commit. Push only when the user explicitly requests a push; a commit request does not authorize pushing. Once requested, proceed without asking for additional approval. Stage only the changes needed for the requested commit, unless the user asks for staging separately.

## Collaboration

Ask the user about consequential choices affecting scope, architecture, public behavior, compatibility, or data. Resolve routine, reversible details from the project and existing decisions. Be direct about concrete tradeoffs and simpler alternatives; do not invent objections merely to disagree.

## Shared skills

For coding tasks, load and follow the `coding` skill.

Use the current client's native skill, question, browser, and delegation tools. A reference to `/skill-name` identifies the named skill; if no Skill tool exists, read its installed `SKILL.md` and follow its relevant references. Report a genuinely missing capability instead of pretending that a differently named tool provides it.
