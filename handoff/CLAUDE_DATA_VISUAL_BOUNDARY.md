# Claude — Data / Visual Boundary

Before implementing Ask Monix UI, keep this division explicit.

## Your data authority

You are responsible for all data decisions.

Use the database/data environment you already have from the user's local **`monverse-app`** context as the canonical reference for:

- schema
- field names
- entity relationships
- metric definitions
- query logic
- data availability
- provenance
- freshness
- calculation validity

Do **not** assume the visual mockups or GitHub visual repository define the database contract.

Some approved visuals were originally created from Layer-2 data collected from the Monix web interface. Those visuals define presentation, not canonical schema.

If names differ:

> Use the database's canonical names internally, then map them to the approved human-facing visual labels.

Do not modify data semantics to fit a mockup.

## Visual authority

The Ask Monix visual repository owns:

- typography
- color
- spacing
- hierarchy
- composition
- chart/surface behavior
- scan vs inspect
- responsive behavior
- evidence presentation
- visual interaction pattern

Do not redesign these based on the shape of the database.

## Collaboration rule

```
You decide:
What data exists?
What is it called?
How is it computed?
How trustworthy is it?

Visual system decides:
What appears first?
What is emphasized?
How is the relationship shown?
What is hidden until inspect?
How does it behave across screen sizes?
```

## Required implementation pattern

```
Monverse / canonical data
        ↓
analytics/intelligence
        ↓
view model / adapter
        ↓
approved Ask Monix visual component
```

Do not wire raw database structures directly into UI if doing so breaks the approved visual hierarchy.

Do not create new database fields merely because a visual mockup uses a convenient label.

## If data is missing

Report the gap.

Do not fabricate.

The UI must show unknown/incomplete/insufficient evidence when appropriate.

## One sentence to remember

> **You own data truth. This repository owns visual truth.**
