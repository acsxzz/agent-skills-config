# Triage Labels

The skills speak in terms of five canonical triage roles. This file maps those roles to the actual label strings used in this repo's issue tracker.

| Label in mattpocock/skills | Label in our tracker | Meaning                                  |
| -------------------------- | -------------------- | ---------------------------------------- |
| `needs-triage`             | `needs-triage`       | Maintainer needs to evaluate this issue  |
| `needs-info`               | `needs-info`         | Waiting on reporter for more information |
| `ready-for-agent`          | `ready-for-agent`    | Fully specified, ready for an AFK agent  |
| `ready-for-human`          | `ready-for-human`    | Requires human implementation            |
| `wontfix`                  | `wontfix`            | Will not be actioned                     |

When a skill mentions a role (e.g. "apply the AFK-ready triage label"), use the corresponding label string from this table.

Edit the "Label in our tracker" column to match whatever vocabulary you actually use.

## Category roles

`/triage` also assigns exactly one category role per issue:

| Role          | Label in our tracker | Meaning                     |
| ------------- | -------------------- | --------------------------- |
| `bug`         | `bug`                | Something is broken         |
| `enhancement` | `enhancement`        | New feature or improvement  |

## Wayfinder labels

`/wayfinder` uses one label family on top of the triage vocabulary. `wayfinder:map` marks the single map issue; every child ticket carries exactly one type label.

| Label                | Meaning                                                          |
| -------------------- | ---------------------------------------------------------------- |
| `wayfinder:map`      | The map issue — owns Notes / Decisions so far / Fog              |
| `wayfinder:research` | Research ticket                                                  |
| `wayfinder:prototype`| Prototype ticket                                                 |
| `wayfinder:grilling` | Open decision/discussion ticket — drives the discuss action      |
| `wayfinder:task`     | Task ticket                                                      |

## Label inventory

The full set this repo's skills expect on the tracker. Colours and descriptions match the deck's canonical-label contract, so creating them is deterministic.

| Label                | Colour    | Description                                                                  |
| -------------------- | --------- | ---------------------------------------------------------------------------- |
| `bug`                | `d73a4a`  | Something isn't working                                                      |
| `needs-triage`       | `fbca04`  | Maintainer needs to evaluate this issue (unexamined, awaiting diagnosis)     |
| `needs-info`         | `5319e7`  | Waiting on reporter for more information                                     |
| `ready-for-agent`    | `0e8a16`  | Fully specified, ready for an AFK agent to implement                         |
| `ready-for-human`    | `b60205`  | Requires human implementation                                                |
| `wayfinder:grilling` | `9D7CD8`  | Open decision/discussion ticket (wayfinder grilling type)                    |
| `wayfinder:map`      | `8b5cf6`  | The map issue (wayfinder) — owns Notes/Decisions so far/Fog                  |
| `wayfinder:prototype`| `f59e0b`  | Prototype ticket (wayfinder)                                                 |
| `wayfinder:research` | `0ea5e9`  | Research ticket (wayfinder)                                                  |
| `wayfinder:task`     | `10b981`  | Task ticket (wayfinder)                                                      |

`enhancement` ships with a new GitHub repository's default label set; keep it and do not recreate it.

Create any missing label with `gh label create "<name>" --color <colour> --description "<description>"`. Never apply a label that is not in this file — the skills address roles, and this table is the only translation.