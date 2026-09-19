# Glanceability Contract

Ask Monix must answer the user's first question within seconds:

> **“White Inc lagi gimana?”**

A screen may contain correct intelligence and still fail if that answer is visually buried.

## 3-second test

Within roughly three seconds, without reading every line, the user should understand:

1. current condition
2. direction of movement
3. strongest evidence
4. next investigative direction

## First-view hierarchy

The first meaningful viewport should contain:

### 1. State signal
A compact, visually distinct condition marker.

Examples:
- strengthening
- weakening
- mixed
- stable

Use a semantic icon/dot/shape plus label. Do not rely on a paragraph alone.

### 2. Analytical claim
One short sentence that explains the state.

### 3. Evidence strip
A compact visual relationship, for example:

`Konten ↑38%  →  Impressions ↓18%`

or another relationship supported by the data.

The relationship should be visually parsed before it is fully read.

### 4. Investigation cue
A clear visual/action cue showing where to go next.

## Text budget

Avoid explaining a simple state with multiple paragraphs.

Whenever a sentence merely repeats what a visual cue can show, prefer the visual cue.

Good:
- state icon
- short claim
- 2–3 evidence signals
- one supporting sentence

Bad:
- headline
- long explanation
- section heading
- another explanation
- list of percentages

## Dashboard

Dashboard must feel like a **state console**, not a report.

The user should visually see:

- current condition
- outcome movement
- output movement
- efficiency/result movement

before entering detail.

## Investigation

Each stage must preserve the same glanceability principle while using a different visual grammar.

- History: temporal movement should be visible before labels are read
- PIC: clusters should reveal where weakening/strengthening is concentrated
- Angle: Output → Hasil relationship should dominate
- Creator × Account: localized execution pattern should be visible spatially

## Acceptance question

Ask:

> “Kalau angka dan kalimat kecilnya aku blur, apakah struktur visualnya masih memberi tahu aku mana yang membaik, mana yang melemah, dan ke mana mata harus bergerak?”

If not, the composition is still too text-based.
