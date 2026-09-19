# Data × Visual Collaboration Contract

Status: **LOCKED COLLABORATION BOUNDARY**

This document defines who owns what between the data/intelligence side and the visual/product side of Ask Monix.

The purpose is to prevent overlap, conflicting assumptions, and accidental data-model drift.

---

## 1. Two different sources of authority

### Data authority — Claude / Monverse environment

For all matters related to:

- source database
- database schema
- canonical field names
- table/entity relationships
- data extraction
- query logic
- joins
- transformations
- calculation logic
- metric semantics
- source provenance
- availability / missingness
- data freshness
- data validation

**Claude owns the decision.**

Claude must use the database/data environment available from the user's local **`monverse-app`** context as the primary source of truth for data naming and data availability.

The implementation must follow the canonical naming and structure found in that database/environment rather than inventing new names from visual mockups.

### Visual authority — Ask Monix Visual System

For all matters related to:

- information hierarchy
- reading flow
- visual composition
- typography
- spacing
- color semantics
- line/border behavior
- surface/card behavior
- chart presentation
- interaction hierarchy
- responsive behavior
- scan vs inspect behavior
- evidence presentation
- management readability

**This visual-system repository owns the decision.**

---

## 2. Important historical context

Some early Dashboard and Investigation mockups were designed using **Layer-2 data captured from the Monix web interface**.

Those mockups are useful for:

- understanding the information need
- visual hierarchy
- interaction pattern
- composition
- management reading flow

They are **not** the canonical source for:

- database field names
- schema names
- table names
- exact data contracts
- query logic

If a visual reference says something differently from the canonical database naming in the Monverse environment:

> **Use the canonical database naming and map it into the approved visual presentation.**

Do not modify the underlying data naming merely to match an old mockup.

---

## 3. Required data flow

The intended collaboration model is:

```
Monverse / Claude data environment
        ↓
canonical data names + intelligence semantics
        ↓
view model / adapter
        ↓
Ask Monix visual system
        ↓
user-facing product
```

Not:

```
visual mockup
   ↓
invented field names
   ↓
database changes
```

And not:

```
database structure
   ↓
raw dump directly into UI
```

The adapter/view-model layer exists to translate canonical data into a human-readable product without changing the data's meaning.

---

## 4. Naming rule

### Canonical/internal naming

Must follow the names and semantics established in the actual database/intelligence environment Claude is using.

Claude decides:

- which field is canonical
- which entity relationship is correct
- which metric calculation is valid
- which source wins when multiple raw sources exist

### User-facing naming

May be simplified for readability, but only as a presentation label.

Example:

A canonical internal field may remain unchanged in the data layer while the UI uses a clearer human label.

Any such mapping must be explicit and must not alter semantics.

Rule:

> **Rename for humans only at the presentation layer, never by silently redefining the data.**

---

## 5. Responsibility split

### Claude is responsible for

- knowing where the data comes from
- using the correct database/environment
- using canonical schema and naming
- writing queries
- building adapters/view-models
- validating metric definitions
- validating calculations
- identifying unavailable fields
- identifying data quality / freshness limitations
- preserving provenance

### Visual system is responsible for

- deciding what deserves emphasis
- deciding scan vs inspect
- deciding visual hierarchy
- deciding how much is visible at once
- deciding how relationships are spatially represented
- deciding headline grammar
- deciding how uncertainty is displayed
- deciding responsive behavior
- deciding interaction pattern
- preventing UI rigidity and dashboard-like overboxing

---

## 6. Non-overlap rule

### Visual side must NOT

- invent database fields
- prescribe SQL/query implementation
- choose tables
- rename canonical schema
- define data joins
- redefine metric formulas
- assume a visual reference is the source of truth for data

### Claude/data side must NOT

- redesign the approved moodboard
- substitute the visual system with existing legacy UI
- reintroduce neon/cinematic styling
- turn every stage into a generic dashboard
- change visual hierarchy merely because the database returns many fields
- expose all available data just because it exists

---

## 7. When visual needs data that is unavailable

Claude should not fabricate it.

Claude should report:

1. what the visual needs
2. whether the database already contains it
3. whether it can be safely derived
4. evidence/assumptions required
5. whether the visual should adapt because evidence is insufficient

Then the visual layer decides how the absence should appear.

Possible visual states:

- unknown
- unavailable
- incomplete coverage
- immature
- insufficient evidence

Unknown must remain visible as unknown.

---

## 8. When database terminology differs from visual references

Database terminology wins internally.

Visual references win for composition and human presentation.

Use an explicit mapping layer.

Example:

```
canonical database field
        ↓
validated metric/view-model
        ↓
human-facing label
```

Do not use mockup labels as schema definitions.

---

## 9. Final collaboration principle

> **Claude owns data truth. Ask Monix Visual System owns presentation truth.**

Claude determines **what the data actually is**.

The visual system determines **how a human should understand it**.

Neither side should silently take over the other's responsibility.
