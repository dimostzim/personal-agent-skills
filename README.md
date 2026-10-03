# Personal Agent Skills

One canonical collection of 23 shared skills for local Codex and Claude Code sessions, including their use through T3 Code. Both `~/.codex/skills/<name>` and `~/.claude/skills/<name>` link to `skills/<name>` here.

`~/.codex/AGENTS.md` and `~/.claude/CLAUDE.md` link to `global/AGENTS.md`: Vlasta's instructions plus concise collaboration and client-portability guidance. Edit that source to change both clients.

## Installation on another machine

Clone this private repository and keep the checkout as the canonical collection. For each skill you want to use, link its directory into the client's personal skills directory. For example, from the repository root:

```sh
mkdir -p ~/.codex/skills ~/.claude/skills
ln -s "$PWD/skills/coding" ~/.codex/skills/coding
ln -s "$PWD/skills/coding" ~/.claude/skills/coding
```

Repeat for the other directories under `skills/`. Inspect existing destinations first; preserve existing skills and configuration before replacing anything. These commands are examples for unused destinations and do not perform an installation automatically.

For the shared global instructions, link `global/AGENTS.md` to `~/.codex/AGENTS.md` and `~/.claude/CLAUDE.md` after reviewing and merging any existing personal instructions. Provider-managed skills and plugins are installed separately through their client. Google Workspace and other connectors require authentication on each client.

The repository includes shared skills, their supporting resources, global instructions, and `sources.json`. Machine-specific installation history and backup paths stay in the ignored local `installation.json`. Home-relative paths in the source manifest resolve on the machine running the update check.

## Everyday use

For routine edits and back-and-forth coding, ask for the change directly. The `coding` standards apply, with checks appropriate to the change. No project setup, grilling, spec, tickets, or full review workflow is required.

When choosing the spec-and-ticket workflow, configure the project once with `setup-matt-pocock-skills`. It records the tracker and domain-document locations; installing the skills does not configure individual projects.

For a larger feature when you want structured planning: `grill-me` → `to-spec` → optional `to-tickets` → a fresh session with `implement` and the saved spec or ticket. Agree the public testing boundaries during planning. Implementation uses `coding`, applies `tdd` where appropriate, and reviews the final working tree with `code-review`. Individual skills can be used when needed without running the entire sequence.

In Claude Code, invoke a skill as `/skill-name`. In Codex, use `$skill-name` or explicitly request the named skill. Existing explicit-only invocation settings are retained in both clients' metadata.

Use `triage` when you want to organize incoming issues or PRs and prepare implementation briefs. It is invoked explicitly and needs the project's tracker and triage-label configuration from `setup-matt-pocock-skills`. `tdd` remains available for test-first work. Neither is required for ordinary back-and-forth coding.

One-off checks and experiments use temporary storage and are cleaned up after serving their purpose. Lasting tests must protect a concrete behavior or regression beyond existing coverage. Prototype scaffolding is removed once the design is settled; requested demos stay available for review. Research notes use temporary storage unless you request lasting project documentation.

Use `scientific-writing` for manuscript prose. Its references preserve the user's technical style and contain calibration from ParaDISM, pre-miRBench, miRBench, miRBind2, and Agentomics. Use `citation-management` for sources and bibliographies.

Use `skill-updates` to compare this collection with upstream. A check reports changes without replacing files. `sources.json` records verified source revisions, file hashes, and deliberate local changes; the skill should preserve those changes when applying an update.

## Sources and scope

- Vlasta: 18 selected skills from `MartinekV/agent-skills`, pinned to the revision recorded in `sources.json`.
- Personal: `coding`, `scientific-writing`, `citation-management`, and `skill-updates`.
- Slides: the user's existing Claude-installed `frontend-slides` version, preserved unchanged with its supporting files.
- Claude-native: official `document-skills@anthropic-agent-skills` plugin, containing `docx`, `pdf`, `pptx`, and `xlsx`; individual Anthropic `skill-creator` remains in `~/.claude/skills/skill-creator` and is recorded in the source manifest.
- Codex-managed skills and plugins remain managed by Codex. Skill files do not transfer authenticated Google Workspace or other connector access between clients.

Upstream source attribution and revisions are recorded in `sources.json`; existing license notices are retained with their files. Vlasta's source repository is private and has no repository license declared. This collection does not add a blanket license to upstream material.

`research-writing` is retired. Its useful venue/reporting checks are retained in `scientific-writing/references/submission-checks.md`; the original remains in the backup.

`frontend-design` is retired at the user's request. Its files are archived outside both clients' skill directories; `installation.json` records the backup location.

## Local changes

Keep Vlasta's skills unchanged unless a concrete workflow or compatibility gap requires a local edit. The remaining instruction changes connect `implement` to personal `coding` standards and working-tree review, make `code-review` include uncommitted and new files, and let setup/spec/tickets share configuration across clients before full triage configuration. `prototype` removes settled experiments instead of requiring archive branches; `research` keeps one-off notes outside the repository. Global instructions handle client-specific skill loading. `grill-me`, `grill-with-docs`, `tdd`, and `triage` match the pinned upstream versions exactly; Agentomics retains its existing Codex display metadata. `babysit-pr` is not installed.

Your original frontend slides and Agentomics review files were checked against their backups and preserved. `installation.json` records the backup location, installed links, and verification results.

Start a new session to reload global instructions and newly installed plugins. Skills may refresh sooner, depending on the client. Validation covers native Codex discovery, Claude component validation, metadata, links, and supporting references; no model-driven end-to-end workflow or document-rendering evaluation was performed during installation.
