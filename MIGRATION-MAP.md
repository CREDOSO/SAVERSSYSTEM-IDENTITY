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

---

# Migration Batch 7 — Participation, Transaction & Economic Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `participation-model.json` | KEEP | `models/participation-model.json` | Canonical participation pathway |
| `participation.json` | MERGE | `models/participation-model.json` | Earlier participant summary overlaps with the model |
| `participation-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `participation-status.json` | MOVE | `archive/generated-v0/participation-status.json` | Self-declared completion record |
| `participation-activation-model.json` | MERGE | `models/participation-model.json` | Activation sequence belongs in the participation model |
| `participation-activation-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `participation-activation-status.json` | MOVE | `archive/generated-v0/participation-activation-status.json` | Self-declared completion status |
| `ecosystem-participation.json` | MERGE | `models/participation-model.json` | Participation roles belong in the canonical participation model |
| `transaction-model.json` | KEEP | `models/transaction-model.json` | Canonical transaction-recognition model |
| `transaction-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `transaction-status.json` | MOVE | `archive/generated-v0/transaction-status.json` | Self-declared completion record |
| `economic-model.json` | KEEP | `models/economic-model.json` | Canonical economic structure |
| `economic-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `economic-status.json` | MOVE | `archive/generated-v0/economic-status.json` | Self-declared completion record |

## Canonical Result

The authoritative operating models will be:

- `models/participation-model.json`
- `models/transaction-model.json`
- `models/economic-model.json`

The consolidated participation model must preserve:

- Entry through QR, CARD, or LINK;
- meaningful action;
- transaction recognition;
- participation history;
- repeated return activity.

The consolidated transaction model must preserve:

- qualifying activity;
- recognition through the technology layer;
- association with merchant and participant records;
- recorded transaction history;
- connection to economic outcomes.

The consolidated economic model must preserve:

- merchant database value;
- participation-driven activity;
- consumer rewards;
- partner and agent value;
- revenue distribution;
- recurring economic activity.

---

# Migration Batch 8 — Knowledge, Intent & Semantic Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `knowledge-model.json` | KEEP | `models/knowledge-model.json` | Canonical structured knowledge model |
| `knowledge.json` | MERGE | `models/knowledge-model.json` | Earlier knowledge summary overlaps with the model |
| `knowledge-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `knowledge-status.json` | MOVE | `archive/generated-v0/knowledge-status.json` | Self-declared completion status |
| `intent-model.json` | KEEP | `models/intent-model.json` | Canonical intent model |
| `intent.json` | MERGE | `models/intent-model.json` | Earlier intent record overlaps with the model |
| `intent-status.json` | MOVE | `archive/generated-v0/intent-status.json` | Self-declared completion status |
| `semantic-model.json` | KEEP | `models/semantic-model.json` | Canonical machine interpretation model |
| `concept-map.json` | MERGE | `models/semantic-model.json` | Concept relationships belong in the semantic model |
| `semantic-status.json` | MOVE | `archive/generated-v0/semantic-status.json` | Self-declared completion status |
| `learning-context.json` | MERGE | `models/knowledge-model.json` | Source references belong in the knowledge model |
| `learning-model.json` | REVIEW | `models/learning-model.json` | Potential operational learning model; distinct from static knowledge |
| `learning-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `learning-status.json` | MOVE | `archive/generated-v0/learning-status.json` | Self-declared completion status |

## Canonical Result

The authoritative understanding records will be:

- `models/knowledge-model.json`
- `models/intent-model.json`
- `models/semantic-model.json`

`models/learning-model.json` remains under review because it may represent an operational feedback process rather than static identity knowledge.

The consolidated records must preserve:

- the approved SAVERSSYSTEM™ definition;
- system architecture knowledge;
- merchant database monetization intent;
- customer participation intent;
- transaction-recognition concepts;
- revenue-distribution concepts;
- machine-readable semantic relationships;
- clear separation between static knowledge and operational learning.

---

# Migration Batch 9 — Deployment, Publication & Operations Records

| File | Action | Destination | Reason |
|---|---|---|---|
| `deployment-model.json` | KEEP | `operations/deployment-model.json` | Canonical deployment sequence |
| `deployment-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `deployment-status.json` | MOVE | `archive/generated-v0/deployment-status.json` | Self-declared completion record |
| `deployment-checkpoint.json` | MOVE | `archive/generated-v0/deployment-checkpoint.json` | Generated checkpoint declaration |
| `live-deployment-model.json` | MERGE | `operations/deployment-model.json` | Overlapping live deployment sequence |
| `live-deployment-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `live-deployment-status.json` | MOVE | `archive/generated-v0/live-deployment-status.json` | Self-declared live status |
| `publication.json` | MERGE | `operations/deployment-model.json` | Publication state belongs in deployment |
| `publication-channels.json` | MERGE | `operations/deployment-model.json` | Publication channels belong in deployment |
| `publication-status.json` | MOVE | `archive/generated-v0/publication-status.json` | Self-declared completion record |
| `placement-map.json` | MERGE | `operations/deployment-model.json` | Placement map belongs in deployment planning |
| `placement-model.json` | MERGE | `operations/deployment-model.json` | Overlapping placement structure |
| `placement-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `placement-status.json` | MOVE | `archive/generated-v0/placement-status.json` | Self-declared completion record |
| `surface-model.json` | REVIEW | `operations/surface-model.json` | May remain as a distinct discovery-surface model |
| `surface-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `surface-status.json` | MOVE | `archive/generated-v0/surface-status.json` | Self-declared completion record |
| `operational-status.json` | MOVE | `archive/generated-v0/operational-status.json` | Self-declared operational state |
| `operational-complete.json` | MOVE | `archive/generated-v0/operational-complete.json` | Redundant completion record |
| `live-operations-model.json` | KEEP | `operations/live-operations-model.json` | Canonical post-deployment operating cycle |
| `live-operations-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `live-operations-status.json` | MOVE | `archive/generated-v0/live-operations-status.json` | Self-declared live status |
| `activity.json` | MERGE | `operations/live-operations-model.json` | Activity tracking belongs in live operations |
| `performance.json` | MERGE | `operations/live-operations-model.json` | Performance indicators belong in live operations |
| `monitoring-model.json` | KEEP | `operations/monitoring-model.json` | Canonical monitoring and improvement cycle |
| `monitoring-index.json` | MERGE | `index.json` | Navigation belongs in the root index |
| `monitoring-status.json` | MOVE | `archive/generated-v0/monitoring-status.json` | Self-declared completion record |

## Canonical Result

The authoritative deployment and operations records will be:

- `operations/deployment-model.json`
- `operations/live-operations-model.json`
- `operations/monitoring-model.json`

`operations/surface-model.json` remains under review because it may represent a distinct machine retrieval environment rather than a deployment duplicate.

The consolidated deployment model must preserve:

- Prepare → Publish → Connect → Discover → Participate;
- repository publication;
- website and structured-data placement;
- machine discovery pathways;
- public reference channels.

The consolidated live operations model must preserve:

- monitoring;
- maintenance;
- performance review;
- feedback;
- improvement;
- scaling readiness.
