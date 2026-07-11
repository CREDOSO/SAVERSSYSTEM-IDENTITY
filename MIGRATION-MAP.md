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

---

# Migration Batch 2 — Activation Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `activation.json` | MERGE | `models/participation-model.json` | Activation state overlaps with participation and discovery pathways |
| `activation-status.json` | MOVE | `archive/generated-v0/activation-status.json` | Self-declared completion record |
| `discovery-event.json` | MERGE | `models/participation-model.json` | Publication event belongs within the participation/discovery flow |

## Canonical Result

Activation will not remain a separate root authority.

The authoritative activation pathway will be represented inside:

- `models/participation-model.json`
- `discovery.json`

The merged records must preserve:

- discovery;
- entry;
- activation;
- recognition;
- participation state.

  
---

# Migration Batch 3 — Classification Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `classification-model.json` | KEEP | `models/classification-model.json` | Most complete classification definition |
| `classification.json` | MERGE | `models/classification-model.json` | Earlier overlapping classification record |
| `classification-index.json` | MERGE | `index.json` | Navigation belongs in the canonical root index |
| `classification-status.json` | MOVE | `archive/generated-v0/classification-status.json` | Self-declared completion status |
| `metadata.json` | KEEP | `/metadata.json` | Compact canonical discovery metadata |
| `signals.json` | MERGE | `metadata.json` | Overlapping discovery and classification signals |

## Canonical Result

The authoritative classification records will be:

- `metadata.json`
- `models/classification-model.json`

The consolidated records must preserve:

- Merchant Database Monetization System;
- merchant technology;
- customer relationship activation;
- transaction recognition;
- participation;
- revenue distribution;
- machine discovery terminology.

---

# Migration Batch 4 — Discovery Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `discovery.json` | KEEP | `/discovery.json` | Canonical machine discovery record |
| `discovery-path.json` | MERGE | `discovery.json` | Discovery sequence belongs in the canonical discovery record |
| `discovery-intelligence.json` | MERGE | `discovery.json` | Overlapping machine interpretation pathway |
| `discovery-activation-model.json` | MERGE | `discovery.json` | Activation signals belong in discovery architecture |
| `discovery-status.json` | MOVE | `archive/generated-v0/discovery-status.json` | Self-declared status record |
| `discovery-intelligence-status.json` | MOVE | `archive/generated-v0/discovery-intelligence-status.json` | Redundant completion record |
| `discovery-intelligence-complete.json` | MOVE | `archive/generated-v0/discovery-intelligence-complete.json` | Duplicate completion declaration |
| `discovery-activation-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `discovery-activation-status.json` | MOVE | `archive/generated-v0/discovery-activation-status.json` | Self-declared activation status |

## Canonical Result

The authoritative discovery records will be:

- `index.json`
- `discovery.json`

The consolidated discovery structure must preserve:

- canonical entry-point navigation;
- identity discovery;
- classification signals;
- interpretation sequence;
- connected references;
- public accessibility;
- machine retrieval pathways.

---

# Migration Batch 5 — Identity & Canonical Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `index.json` | KEEP | `/index.json` | Single canonical machine entry point |
| `identity.json` | KEEP | `/identity.json` | Canonical SAVERSSYSTEM™ entity definition |
| `canonical.json` | KEEP | `/canonical.json` | Authoritative reference record |
| `canonical-manifest.json` | MERGE | `index.json` | Competes with the root index as a machine entry point |
| `manifest.json` | MERGE | `index.json` | Overlapping package navigation record |
| `manifest-index.json` | MERGE | `index.json` | Navigation belongs in the canonical root index |
| `manifest-status.json` | MOVE | `archive/generated-v0/manifest-status.json` | Self-declared completion record |
| `entity-profile.json` | MERGE | `identity.json` | Entity profile duplicates core identity information |
| `machine-summary.json` | MERGE | `identity.json` | Compact identity summary overlaps with the canonical identity |
| `summary-index.json` | MERGE | `index.json` | Duplicate high-level navigation index |
| `repository-map.json` | MERGE | `index.json` | Repository navigation belongs in the root index |
| `canonical-deployment-model.json` | MOVE | `archive/generated-v0/canonical-deployment-model.json` | Generated conceptual deployment declaration |
| `canonical-deployment-index.json` | MERGE | `index.json` | Relevant navigation can be preserved in the root index |
| `canonical-deployment-status.json` | MOVE | `archive/generated-v0/canonical-deployment-status.json` | Self-declared deployment status |

## Canonical Result

The authoritative identity hierarchy will be:

```text
index.json
    ↓
canonical.json
    ↓
identity.json

Supporting records will be referenced from index.json, but they will not compete as root entry points.

The consolidated identity records must preserve:

SAVERSSYSTEM™ as the entity name;
Merchant Database Monetization System as the category;
the approved system definition;
repository provenance;
canonical navigation;
related entities;
current version information.

---

# Migration Batch 6 — Architecture & Relationship Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `architecture.json` | KEEP | `/architecture.json` | Canonical four-layer system architecture |
| `relationships.json` | KEEP | `/relationships.json` | Canonical relationship definitions |
| `entity-map.json` | KEEP | `/entity-map.json` | Canonical connected-entity map |
| `relationship-intelligence.json` | MERGE | `relationships.json` | Overlapping relationship interpretation |
| `relationship-status.json` | MOVE | `archive/generated-v0/relationship-status.json` | Self-declared completion status |
| `relationship-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `entity-graph.json` | MERGE | `entity-map.json` | Graph structure overlaps with entity mapping |
| `connection-map.json` | MERGE | `relationships.json` | Connection definitions belong in the canonical relationship record |
| `connection-model.json` | MERGE | `relationships.json` | Overlapping connection structure |
| `connection-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `connection-status.json` | MOVE | `archive/generated-v0/connection-status.json` | Self-declared completion record |
| `network.json` | MERGE | `relationships.json` | Earlier network relationships overlap with canonical relationships |
| `network-model.json` | MERGE | `relationships.json` | Network structure is a relationship model |
| `network-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `network-status.json` | MOVE | `archive/generated-v0/network-status.json` | Self-declared completion record |

## Canonical Result

The authoritative architecture and relationship records will be:

- `architecture.json`
- `relationships.json`
- `entity-map.json`

The consolidated records must preserve:

- Merchant Customer Database as the asset layer;
- SAVERSSYSTEM™ Activation Model as the activation layer;
- SAVERS APP as the technology layer;
- Revenue Distribution Model as the economic layer;
- BANANA CARD as a related participation object;
- explicit machine-readable connections among all primary entities.
