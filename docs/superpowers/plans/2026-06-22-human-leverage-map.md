# The Human Leverage Map — Implementation (Writing) Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Write a ~13,000–16,000-word integrated small book, *The Human Leverage Map*, that presents an original framework for human value in the AI era and grounds it in verified research.

**Architecture:** Manuscript as one Markdown file per chapter under `manuscript/`, a single verified bibliography (`references.md`), and a `claims-ledger.md` that tracks every load-bearing empirical claim to a real source (or marks it dropped). Research/verification is front-loaded into Task 1 so drafting tasks only consume verified material. A final task compiles and runs a whole-book consistency pass.

**Tech Stack:** Markdown. Live web search for claim verification (WebSearch / WebFetch). No code, no build system, no git (this directory is not a repo — "save file" replaces "commit").

## Global Constraints

Every task implicitly inherits these. Copied verbatim from the spec.

- **Audience/register:** Leaders & practitioners. Mental-model register (Maslow / Dreyfus / Naval). Rigorous but readable. Citations are credibility ballast, not academic apparatus. Endnote style.
- **Through-line (must be defensible in every chapter):** "When intelligence becomes abundant, judgment becomes scarce — and the same AI that grants you leverage can quietly erode the faculty that leverage depends on."
- **Citation rule (non-negotiable):** (a) Original framework/coinages → labeled as ours, NO citation. (b) Borrowed concepts → cite canonical verifiable source. (c) Empirical claims → MUST be verified against a real, locatable source before use; unverifiable claims are dropped or reframed as illustration, NEVER given a fabricated citation. Do NOT reuse the research-dump's citation list on trust.
- **Coinage spellings (use exactly, capitalized as shown):** The Scarcity Inversion · The Human Leverage Map · Cognitive Sovereignty · Steward of Intelligence · "leverage that survives AI".
- **Canonical axis names (use exactly):** X = **AI Capability** (levels: Ignore → Consumer → Practitioner → Collaborator → Builder → Orchestrator → AI-Native). Y = **Human Leverage** (levels: Survival → Productivity → Execution → Expertise → Judgment → Leadership → Multiplication → Stewardship). Z = **Purpose / Scope** (Self → Team → Org → Industry → Society → Humanity). Hidden reading = **Cognitive Sovereignty**.
- **Quadrant persona names (use exactly):** The Resistant (low AI / low leverage) · The Prompt Addict (high AI / low leverage) · The Wise Expert (low AI / high leverage) · The Amplifier / Steward of Intelligence (high AI / high leverage).
- **No-go (YAGNI):** no numeric calibration scale; no emotional primary axis; not two documents; not academic-only; not a short essay.

---

### Task 1: Claims Ledger & Verified References (research pass)

Front-loads all empirical verification so drafting consumes only verified material.

**Files:**
- Create: `claims-ledger.md`
- Create: `references.md`

**Interfaces:**
- Produces: a verified citation for each claim below, addressable by a short key (e.g., `[prediction-machines]`, `[gps-spatial]`). Chapters 2, 8, 9, 10 consume these keys. Each ledger row: `claim · status (VERIFIED/REFRAMED/DROPPED) · source key · 1-line note`.

**Claims to verify (each via web search; record the real source or mark DROPPED):**
1. Cognitive offloading / LLM use reduces critical-thinking or neural engagement (the "Your Brain on ChatGPT" / MIT Media Lab EEG line, Kosmyna et al.).
2. Habitual GPS navigation degrades hippocampal/spatial memory (Maguire taxi-driver work; Dahmani & Bohbot).
3. Negative correlation between AI reliance and critical thinking (Gerlich, *Societies* 2025).
4. *Prediction Machines* economics — cheap prediction raises the value of judgment & data (Agrawal, Gans, Goldfarb).
5. "When execution is no longer scarce, judgment is" / taste-as-framing (Itamar Medeiros — verify the quote is locatable; if not, REFRAME as unattributed paraphrase).
6. Levels-of-autonomy spectrum Operator→Observer (Knight Institute / equivalent).
7. Sheridan & Verplank levels of automation (1978).
8. Extended Mind thesis (Clark & Chalmers, 1998).
9. Distributed cognition (Hutchins).
10. "System 0" pre-cognitive AI layer (Chiriatti et al., *Nature Human Behaviour* 2024) and Kahneman System 1/2.
11. The precise statistics from the research dump — "95% offload Tier-1," "17% Epistemic Confinement," "19.2–22.4% selection overlap." **Default DROPPED** unless an independent real source is found; the *concepts* (Epistemic Confinement, selection-alignment gap) may be used as framework language without the fabricated percentages.

- [ ] **Step 1: Verify claims 1–11** — one web search per claim; capture title, author(s), year, venue, URL.
- [ ] **Step 2: Write `references.md`** — one entry per VERIFIED source with its short key, full citation, URL.
- [ ] **Step 3: Write `claims-ledger.md`** — one row per claim with status + source key + note. Every DROPPED/REFRAMED claim gets a one-line reason.
- [ ] **Step 4: Gate** — confirm: zero claims left UNVERIFIED-but-used; every key in `references.md` resolves to a real reachable URL. Save both files.

---

### Task 2: Front Matter — "Locate Yourself" + Map Figure + Glossary

Establishes the canonical figure, axis labels, and coinage glossary that every later chapter references.

**Files:**
- Create: `manuscript/00-front-locate-yourself.md`

**Interfaces:**
- Produces: the canonical ASCII map figure and the glossary block (coinages + axis level lists). Chapters 3–7 reference this figure; all chapters use the glossary spellings.

- [ ] **Step 1: Draft the map figure** — the 2×2 quadrant ASCII diagram from the spec, with the four persona names placed and both axes labeled.
- [ ] **Step 2: Draft "Locate Yourself"** (~500–700 words) — a short self-assessment: three prompts (your AI Capability level, your Human Leverage level, your current vector vs. last year) so a reader can place a dot and an arrow before Chapter 1.
- [ ] **Step 3: Draft the Glossary** — one-line definitions of the four coinages + the three axis level-lists, verbatim per Global Constraints.
- [ ] **Step 4: Gate** — coinage spellings and axis labels match Global Constraints exactly; figure renders in monospace; word count 500–800. Save file.

---

### Task 3: Chapter 1 — The Faculty AI Automates Now

**Files:** Create `manuscript/01-faculty-ai-automates.md`

**Interfaces:**
- Consumes: none.
- Produces: the historical arc (muscle → calculation → information → execution/expertise) that Chapter 2's inversion depends on.

**Must establish:** (1) the four-epoch arc, each epoch automating one human faculty; (2) AI's departure — it automates *intelligence/expertise itself*, not a peripheral faculty; (3) why "how you feel about AI" (fear/hype) is the perishable, wrong question — every prior technology ran the same emotional cycle. Target 1,200–1,700 words.

- [ ] **Step 1: Outline** the arc as four beats + the "wrong question" turn.
- [ ] **Step 2: Draft** the chapter in register.
- [ ] **Step 3: Verify** any factual/empirical claim used appears VERIFIED in `claims-ledger.md`; if a new claim appears, verify it and add a ledger row (do not draft around an unverified claim).
- [ ] **Step 4: Gate** — through-line defensible; no fabricated cites; opens the book with a hook, not a definition; word band met. Save file.

---

### Task 4: Chapter 2 — The Scarcity Inversion

**Files:** Create `manuscript/02-scarcity-inversion.md`

**Interfaces:**
- Consumes: Ch 1 arc; ledger keys `[prediction-machines]`, `[medeiros]` (or its REFRAMED form).
- Produces: the macro-thesis definition of **The Scarcity Inversion** that Part III's defense relies on.

**Must establish:** (1) define **The Scarcity Inversion** as an original coinage; (2) the economic mechanism — cheap prediction raises the value of its complements (judgment, data) — grounded in `[prediction-machines]`; (3) the drift of scarce value to judgment → taste → trust → responsibility → meaning, using `[medeiros]`; (4) define "leverage that survives AI." Target 1,300–1,800 words.

- [ ] **Step 1: Outline** mechanism → inversion → what becomes scarce → definition of durable leverage.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** every empirical/economic claim resolves to a ledger key; cite borrowed economics canonically; coinage uncited.
- [ ] **Step 4: Gate** — Scarcity Inversion is clearly *ours*; economics cited to real source; word band met. Save file.

---

### Task 5: Chapter 3 — Why a Map, Not a Ladder

**Files:** Create `manuscript/03-map-not-ladder.md`

**Interfaces:**
- Consumes: front-matter figure.
- Produces: the justification for 2D-over-linear that Chapters 4–7 build on.

**Must establish:** (1) maturity ladders (Hawkins, Maslow, Gartner, Dreyfus) imply single-direction movement; reality is multi-directional; (2) two people at equal AI skill can hold opposite human leverage — worked examples (AI researcher with poor judgment; CEO with no AI skills; teacher with high leverage, low AI); (3) the map shows position + vector, not a fixed label. Target 1,000–1,400 words.

- [ ] **Step 1: Outline** ladder critique → examples → map-as-instrument.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** any named model (Dreyfus, Gartner) described accurately; Hawkins framed as metaphor, not science (per `what-exisits` research).
- [ ] **Step 4: Gate** — no claim that the map is "scientific/calibrated"; word band met. Save file.

---

### Task 6: Chapter 4 — The X-Axis: AI Capability

**Files:** Create `manuscript/04-x-axis-ai-capability.md`

**Interfaces:**
- Consumes: glossary level-list for X.
- Produces: defined, exemplified X-axis levels reused by Chapters 6, 8.

**Must establish:** each X level (Ignore → Consumer → Practitioner → Collaborator → Builder → Orchestrator → AI-Native) with a one-paragraph definition and a concrete example (Consumer = ChatGPT/Claude/Copilot use; Builder = MCP/APIs/agents/RAG; Orchestrator = teams of agents/automated workflows; AI-Native = starts from "should AI do this?"). Frame as *how effectively you compose non-human intelligence*. Target 1,000–1,400 words.

- [ ] **Step 1: Outline** the level ladder with one example slot each.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** tool/technique names are current and accurate.
- [ ] **Step 4: Gate** — level names match glossary exactly; every level has a concrete example; word band met. Save file.

---

### Task 7: Chapter 5 — The Y-Axis: Human Leverage

**Files:** Create `manuscript/05-y-axis-human-leverage.md`

**Interfaces:**
- Consumes: glossary level-list for Y; Ch 2 definition of durable leverage.
- Produces: defined Y levels reused by Chapters 6, 11.

**Must establish:** each Y level (Survival → Productivity → Execution → Expertise → Judgment → Leadership → Multiplication → Stewardship) as a *different question answered*; the key turn at Judgment (where AI stops being able to substitute); "value that survives AI" as the axis's measuring stick; why upward is the only AI-proof direction. Target 1,200–1,600 words.

- [ ] **Step 1: Outline** levels as an ascending scarcity gradient.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** any claim about what AI can/can't substitute resolves to a ledger key or is framed as argument, not data.
- [ ] **Step 4: Gate** — level names match glossary; the Judgment inflection is explicit; word band met. Save file.

---

### Task 8: Chapter 6 — The Four Quadrants & Movement Vectors

**Files:** Create `manuscript/06-quadrants-vectors.md`

**Interfaces:**
- Consumes: X levels (Ch 4), Y levels (Ch 5), persona names (Global Constraints).
- Produces: the four personas as reusable shorthand for Chapters 9–11.

**Must establish:** each quadrant as a persona with beliefs/behaviors/risk — The Resistant (fear, replaceable), The Prompt Addict (busy, low durable value, model-chasing), The Wise Expert (proof AI isn't everything), The Amplifier/Steward (where future leaders live); then the dynamic move — vectors over labels ("where were you last year, where now, which way pointed"). Target 1,300–1,700 words.

- [ ] **Step 1: Outline** four personas + the vector turn.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** no empirical claim smuggled in uncited.
- [ ] **Step 4: Gate** — persona names exact; vectors-not-labels stated; word band met. Save file.

---

### Task 9: Chapter 7 — Altitude: The Z-Axis of Purpose

**Files:** Create `manuscript/07-altitude-purpose.md`

**Interfaces:**
- Consumes: glossary Z level-list; the four quadrants.
- Produces: the Purpose dimension that the Coda (Ch 11) elevates.

**Must establish:** Z = Purpose/Scope (Self → Team → Org → Industry → Society → Humanity); the map becomes navigational ("almost like Google Maps") with position + vector + altitude; the worked contrast — high-AI/high-leverage/low-purpose (clickbait AI) vs. moderate-AI/high-leverage/high-purpose (AI for education) — "who creates more meaningful leverage?" Target 1,000–1,400 words.

- [ ] **Step 1: Outline** Z levels → 3D navigation metaphor → the purpose contrast.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** no uncited empirical claims.
- [ ] **Step 4: Gate** — Z levels match glossary; the purpose trade-off is concrete; word band met. Save file.

---

### Task 10: Chapter 8 — Cognitive Sovereignty (the hidden axis)

**Files:** Create `manuscript/08-cognitive-sovereignty.md`

**Interfaces:**
- Consumes: ledger keys `[extended-mind]`, `[distributed-cognition]`, `[system-0]`, `[mit-eeg]`, `[gps-spatial]`, `[gerlich]`.
- Produces: definition of **Cognitive Sovereignty** + the atrophy mechanism reused by Chapters 9–10.

**Must establish:** (1) human+AI as a coupled cognitive system (extended mind, distributed cognition) — cited; (2) **System 0** — the pre-cognitive layer that shapes thought before conscious deliberation — cited; (3) cognitive offloading → atrophy, the evidence (EEG engagement, GPS/spatial memory, AI-reliance vs. critical thinking) — each cited to a ledger key; (4) Epistemic Confinement as the failure of sovereignty (concept usable; fabricated percentages excluded); (5) define **Cognitive Sovereignty** as the original coinage naming the defended faculty. Target 1,400–1,900 words.

- [ ] **Step 1: Outline** coupled system → System 0 → offloading evidence → Epistemic Confinement → coinage.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** EVERY empirical claim cites a VERIFIED ledger key; no "95%/17%" style figures unless independently sourced; coinage uncited.
- [ ] **Step 4: Gate** — this is the most citation-dense chapter: confirm zero fabricated cites, every borrowed concept attributed; word band met. Save file.

---

### Task 11: Chapter 9 — How Leverage Collapses

**Files:** Create `manuscript/09-how-leverage-collapses.md`

**Interfaces:**
- Consumes: personas (Ch 6), Cognitive Sovereignty (Ch 8), ledger keys for autonomy levels.
- Produces: the failure transitions referenced by Chapter 10's defenses.

**Must establish:** the failure modes — Captive of Autonomy (opaque delegation hollows agency), algorithmic monoculture/herding (correlated models → fragile systems), illusion of competence (fluent output inflates confidence above real skill); framed as *transitions* on the map (how an Amplifier decays into a Prompt Addict or a Captive). Target 1,200–1,700 words.

- [ ] **Step 1: Outline** three failure modes as map transitions.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** autonomy-levels and any empirical claim resolve to ledger keys; monoculture framed as argument unless a real source exists.
- [ ] **Step 4: Gate** — each failure mode tied to a specific map movement; no fabricated cites; word band met. Save file.

---

### Task 12: Chapter 10 — Defending the Summit

**Files:** Create `manuscript/10-defending-the-summit.md`

**Interfaces:**
- Consumes: failure modes (Ch 9), Cognitive Sovereignty (Ch 8).
- Produces: the practice set the Coda resolves into a posture.

**Must establish:** concrete defenses across three levels — individual (deliberate cognitive friction, schema-building before offloading, multi-model comparison to resist sycophancy, protected device-free deep work), organizational (human-in/on-the-loop gates, responsibility matrices, context fabric), product/builder (Socratic friction, verification prompts, confidence/source surfacing). Each defense maps to a specific failure mode from Ch 9. Target 1,300–1,800 words.

- [ ] **Step 1: Outline** defenses grouped individual/org/builder, each pointing at a Ch 9 failure.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** any cited technique (HITL/HOTL, levels of automation) resolves to a ledger key.
- [ ] **Step 4: Gate** — every defense answers a named failure mode; actionable for a leader; word band met. Save file.

---

### Task 13: Chapter 11 — Coda: The Steward of Intelligence

**Files:** Create `manuscript/11-coda-steward.md`

**Interfaces:**
- Consumes: Y top levels (Ch 5), Z purpose (Ch 7), defenses (Ch 10).
- Produces: the book's closing posture — terminal deliverable.

**Must establish:** the top-right is a posture, not a destination; the **Steward of Intelligence** defined — uses AI extensively, worships/fears it not, holds judgment as the scarce resource and wisdom as the eventual one; leadership in the AI era = governing human and machine intelligence together; return the through-line and close. Target 1,000–1,400 words.

- [ ] **Step 1: Outline** posture → Steward portrait → judgment→wisdom → close on through-line.
- [ ] **Step 2: Draft.**
- [ ] **Step 3: Verify** no new uncited empirical claim introduced in the close.
- [ ] **Step 4: Gate** — through-line lands; ends on resonance; word band met. Save file.

---

### Task 14: Compile & Whole-Book Consistency Pass

**Files:**
- Create: `the-human-leverage-map.md` (assembled manuscript: front matter → Ch 1–11 → references)
- Modify: any chapter file needing consistency fixes

**Interfaces:**
- Consumes: all chapter files, `references.md`, `claims-ledger.md`.
- Produces: the single finished manuscript.

- [ ] **Step 1: Assemble** front matter + 11 chapters + `references.md` into `the-human-leverage-map.md` with a table of contents.
- [ ] **Step 2: Coinage/axis consistency** — grep the assembled file: every coinage and axis level spelled per Global Constraints; persona names exact; no drifted variants.
- [ ] **Step 3: Citation audit** — every endnote resolves to an entry in `references.md`; cross-check against `claims-ledger.md` that nothing marked DROPPED slipped in; zero future-dated/unreachable URLs.
- [ ] **Step 4: Front-to-back read** — through-line defensible in every chapter; transitions coherent; total length 13,000–16,000 words; register consistent.
- [ ] **Step 5: Gate** — fix issues inline in chapter files, re-assemble, save. Report final word count and citation count.

---

## Self-Review (against the spec)

**Spec coverage:** Thesis → Tasks 4, 13. Scarcity Inversion → Task 4. Map axes X/Y/Z → Tasks 6/7/8 (defs) + 2 (figure). Cognitive Sovereignty bridge → Tasks 10–12. Quadrant personas → Task 8. Coinages → Tasks 2, 4, 10, 13. Self-assessment opener → Task 2. Citation-integrity plan → Task 1 + per-chapter Step 3 + Task 14 Step 3. Three-part structure → Tasks 3–13. Non-goals enforced in Global Constraints. No gaps found.

**Placeholder scan:** No "TBD/TODO"; each task names exact files, exact must-establish content, exact claim keys, and explicit gates. Empirical claims are enumerated, not hand-waved.

**Type/name consistency:** Axis level-lists, persona names, and coinage spellings are pinned once in Global Constraints and referenced by key everywhere — no drift between tasks. Ledger keys introduced in Task 1 are the only citation handles used downstream.
