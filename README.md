# default-workspace — agent skills config

This repository holds only the per-repo configuration that the engineering skills
read. It is deliberately a skeleton: the working directory it lives in is a scratch
arena with multi-GB caches, browser profiles, and business documents, and
[`.gitignore`](.gitignore) excludes all of it.

## What's here

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Agent entry point; points at the three docs below. |
| `docs/agents/issue-tracker.md` | Where issues live (GitHub Issues, via `gh`) and how to drive them. |
| `docs/agents/triage-labels.md` | The label vocabulary: triage roles, categories, and `wayfinder:*`. |
| `docs/agents/domain.md` | Domain-doc consumer rules; this repo is single-context. |

## Skills that read this

`/to-tickets`, `/to-spec`, `/triage`, `/wayfinder`, `/implement`, `/code-review`,
`/domain-modeling`, and the rest of the set. They address roles in prose and
translate them through `docs/agents/triage-labels.md` — keep that table and the
tracker's labels in sync.

`GLOSSARY.md` and `docs/adr/` are created lazily by `/domain-modeling` at the first
real term or decision.