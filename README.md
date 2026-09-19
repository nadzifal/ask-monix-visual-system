# Ask Monix Visual System

Canonical source of truth for how Ask Monix should **look, read, and guide attention**.

This repository is intentionally separate from the implementation repository.

## Responsibility boundary

Ask Monix is now explicitly split into two authorities:

- **Claude / Monverse data environment owns data truth**
- **This repository owns visual truth**

For database source, schema, canonical field names, entity relationships, metric calculation, query logic, data availability, provenance, and freshness, follow the data environment Claude already uses from the user's local `monverse-app` context.

For information hierarchy, reading flow, visual composition, typography, spacing, color, surfaces, chart treatment, scan-vs-inspect behavior, responsive behavior, and evidence presentation, follow this repository.

Read the full contract:

[governance/DATA_VISUAL_COLLABORATION_CONTRACT.md](governance/DATA_VISUAL_COLLABORATION_CONTRACT.md)

## Important historical note

Some early visual references were created from Layer-2 data captured from the Monix web interface.

Those references are valid for **visual hierarchy and product behavior**, but they are **not canonical database contracts**.

If naming differs, canonical database naming from the Monverse/Claude data environment wins internally, and the UI should map it into the approved human-facing presentation.

## What belongs here

- approved moodboard and visual direction
- typography, color, spacing, line, border, surface, and motion rules
- Dashboard visual contract
- Investigation visual contracts
- information hierarchy and reading flow
- interaction behavior
- responsive rules
- visual references
- implementation handoff guidance for Claude / coding agents

## What does not belong here

- production analytics logic
- database architecture
- source database selection
- schema design
- query implementation
- data-source migration
- capability-engine implementation
- business intelligence semantics that are not visual/presentation rules

## Current product direction

**Dashboard is locked.**

Dashboard is no longer treated as an AIC/free-form adaptive canvas.

Performance Investigation remains flexible in composition, but it is **structured-adaptive**, not free-form:

- History = temporal narrative
- PIC = decomposition field
- Angle = relationship field
- Creator × Account = execution map

## Core maxim

> Pendek di permukaan, dalam di isi.

## Core visual rule

> Moodboard controls visual language. Product reasoning controls composition. Component libraries support both, but do not control either.

## Collaboration rule

> Claude owns what the data actually is. This repository owns how humans should understand it visually.

Start at [START_HERE.md](START_HERE.md).
