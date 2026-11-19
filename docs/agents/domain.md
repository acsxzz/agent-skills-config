# Domain Docs

How the engineering skills should consume this repo's domain documentation when exploring the codebase.

## Layout: single-context

**This repo is single-context:** one repo, one shared glossary at the root, and one set of architecture decisions in `docs/adr/`. There are no per-package or per-subproject glossaries, and no `GLOSSARY-MAP.md` at the root.

If this repo ever grows into a genuinely multi-package workspace (a `pnpm-workspace.yaml`, a `workspaces` field, or populated `packages/*` with their own `src/`), the layout becomes multi-context: a root `GLOSSARY-MAP.md` pointing at one `GLOSSARY.md` per context, with system-wide decisions in `docs/adr/` and context-scoped decisions in `src/<context>/docs/adr/`. Nothing in this repo needs that today — do not pre-create the structure.

## Before exploring, read these

- **`GLOSSARY.md`** at the repo root.
- **`docs/adr/`**: read ADRs that touch the area you're about to work in. Architecture decisions for this repo live here, including any that would otherwise look package-scoped.

If any of these files don't exist, **proceed silently**. Don't flag their absence; don't suggest creating them upfront. The `/domain-modeling` skill (reached via `/grill-with-docs` and `/improve-codebase-architecture`) creates them lazily when terms or decisions actually get resolved.

`GLOSSARY.md` and `docs/adr/` are both currently absent: no terms or decisions have been written down yet. The first real entry creates them.

## File structure

```
/
├── GLOSSARY.md          ← created lazily, at the first real term
├── docs/
│   ├── adr/             ← architecture decisions, repo-wide
│   │   ├── 0001-....md
│   │   └── 0002-....md
│   └── agents/          ← this skill-set's own config
└── src/
```

## Use the glossary's vocabulary

When your output names a domain concept (in an issue title, a refactor proposal, a hypothesis, a test name), use the term as defined in `GLOSSARY.md`. Don't drift to synonyms the glossary explicitly avoids.

If the concept you need isn't in the glossary yet, that's a signal: either you're inventing language the project doesn't use (reconsider) or there's a real gap (note it for `/domain-modeling`).

## Flag ADR conflicts

If your output contradicts an existing ADR, surface it explicitly rather than silently overriding:

> _Contradicts ADR-0007 (event-sourced orders), but worth reopening because…_