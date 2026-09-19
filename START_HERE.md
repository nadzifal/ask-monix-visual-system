# START HERE

Status: **LOCKED VISUAL DIRECTION / IMPLEMENTATION REFERENCE**

This repository exists so future implementation work does not drift away from the approved Ask Monix product direction.

## First: understand the responsibility split

Before reading visual rules, read:

[governance/DATA_VISUAL_COLLABORATION_CONTRACT.md](governance/DATA_VISUAL_COLLABORATION_CONTRACT.md)

The boundary is simple:

> **Claude owns data truth. Ask Monix Visual System owns visual truth.**

Claude owns:
- source database/environment
- canonical schema and field names
- entity relationships
- query logic
- metric definitions
- calculation validity
- provenance
- freshness
- missingness

This repository owns:
- visual hierarchy
- reading flow
- composition
- typography
- spacing
- color semantics
- line/border/surface behavior
- chart presentation
- scan vs inspect
- responsive behavior
- evidence presentation

Some early mockups were created from Layer-2 data captured from the Monix web interface. Those mockups are **visual references only**. They do not define canonical database naming.

If the canonical database naming in Claude's `monverse-app` data environment differs from a mockup, use the canonical database name internally and map it into the approved human-facing UI.

## Source-of-truth order for VISUAL decisions

1. Approved moodboard
2. Approved Creator × Account direction
3. Visual DNA and anti-rigidity rules
4. Dashboard / Investigation contracts
5. Components and responsive rules
6. Existing production implementation

If production UI conflicts with this repository, do not preserve the old visual behavior merely because it already exists.

## Product character

Ask Monix is a **Calm Modern Intelligence Workspace**.

It should feel:

- calm but alive
- modern but not decorative
- intelligent but not technical-looking
- concise on the surface
- deep underneath
- easy for management to scan
- deep enough for analysts to inspect

## Direction change

Earlier Ask Monix exploration relied heavily on the **Adaptive Intelligence Canvas (AIC)** idea.

That is no longer the governing visual model for Dashboard.

**New direction:**

- Dashboard = fixed, deliberate, locked product surface
- Investigation = one workspace with stage-specific composition
- AIC may still exist as an internal intelligence principle, but it does not control Dashboard layout

Read [decisions/001_DIRECTION_CHANGE_AIC_TO_LOCKED_DASHBOARD.md](decisions/001_DIRECTION_CHANGE_AIC_TO_LOCKED_DASHBOARD.md).

## Hard visual boundaries

Use:

- clean sans-serif typography
- Inter / Geist-class behavior
- crisp warm-white canvas
- deep ink
- botanical green
- restrained muted red / amber / neutral
- active whitespace
- thin local separators only when useful
- minimal shadows
- semantic accent rails
- selective semantic color

Do not use:

- serif display typography
- decorative leaves / botanical illustrations
- lifestyle editorial styling
- neon/cinematic UI
- giant gradients
- glassmorphism
- heavy shadows
- every section inside a card
- large numbered investigation tabs
- repeated dashboard skeletons across all investigation stages

## Approved visual references

- [Moodboard V1](references/moodboard_v1.html)
- [Dashboard direction](references/dashboard_direction.html)
- [History direction](references/history_direction.html)
- [PIC direction](references/pic_direction.html)
- [Angle direction](references/angle_direction.html)
- [Creator × Account approved direction](references/creator_account_approved.html)

These references define visual language and composition, not production data.
