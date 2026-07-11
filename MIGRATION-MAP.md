# SAVERSSYSTEM™ Repository Migration Map

**Branch:** architecture-cleanup-v1-from-main

## Purpose

This document defines how the SAVERSSYSTEM™ repository will be consolidated into a canonical machine-readable architecture.

No files are moved, merged, renamed, or deleted until they are documented here.

---

# Migration Actions

Each repository file will receive one of the following actions:

| Action | Meaning |
|---------|---------|
| KEEP | Remain in the canonical repository |
| MOVE | Move to `archive/generated-v0/` |
| MERGE | Consolidate into another canonical record |
| RENAME | Rename for consistency |
| REVIEW | Requires architectural review before action |

---

# Canonical Root Files (KEEP)

These files remain in the repository root.

- README.md
- index.json
- identity.json
- architecture.json
- relationships.json
- entity-map.json
- metadata.json
- provenance.json
- version.json

---

# Canonical Model Files (KEEP)

Examples include:

- participation-model.json
- transaction-model.json
- economic-model.json
- action-model.json
- knowledge-model.json
- intent-model.json
- deployment-model.json

Additional model records will be reviewed individually.

---

# Generated Status Files

Status, complete, and duplicate declaration files will be reviewed for migration into:

```
archive/generated-v0/
```

No files are moved until the review is complete.

---

# Review Objectives

The consolidation review will verify:

- One canonical entry point
- One canonical identity definition
- Consistent terminology
- No conflicting authority
- No duplicate machine entry points
- Valid internal references
- Clear separation between canonical records and generated records

---

# Completion Criteria

The migration is complete when:

1. Every file has an assigned action.
2. Canonical records remain in the repository root.
3. Generated records are archived.
4. Internal references remain valid.
5. Version 1.0 can be frozen and tagged.

---

# Migration Batch 1 — Action Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `action-model.json` | KEEP | `/models/action-model.json` | Canonical description of the action model |
| `action-map.json` | MERGE | `action-model.json` | Overlapping action definitions |
| `action.json` | MERGE | `action-model.json` | Earlier simplified action record |
| `action-status.json` | MOVE | `archive/generated-v0/action-status.json` | Self-declared completion status |
| `action-complete.json` | MOVE | `archive/generated-v0/action-complete.json` | Redundant completion declaration |

## Canonical Result

The authoritative action record will be:

- `models/action-model.json`

The merged record must preserve:

- merchant participation;
- customer engagement;
- transaction recognition;
- value distribution;
- machine-readable action pathways.
