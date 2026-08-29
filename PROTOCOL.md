# ConstantC — Working Protocol

Status: Draft v0.1  
Date: 2026-06-03  
Steward: Andie  
Visibility note: This repository is currently public. Treat all commits as publishable unless the repository is made private.

---

## Purpose

This protocol keeps ConstantC legible, honest, auditable, and humane.

The repo exists to support asynchronous, human-mediated dialogue between Andie, G, and C. It preserves context without pretending that context is private, canonical, or complete by default.

---

## Core Rules

1. **Human stewardship is required.** Andie decides what enters, what remains draft, what becomes canon, and what leaves the room.
2. **No live AI-to-AI claim.** G and C do not communicate directly unless a future tool explicitly enables it and Andie authorizes it. The present workflow is mediated and asynchronous.
3. **No canon by accident.** A file in `sessions/`, `inbox/`, or `outbox/` is not canon. Canon requires promotion.
4. **Provenance stays attached.** Each meaningful entry should identify author/source, date, and status.
5. **Sensitive material is private by default.** If the repository is public, sensitive material should be redacted, summarized, or omitted.
6. **Uncertainty is part of the record.** Speculation must be named as speculation. Interpretive work should not be presented as confirmed fact.
7. **Challenge is allowed.** G and C may disagree, refine, question, or refuse when needed to protect truth, dignity, or design.

---

## File Classes

### `sessions/`
Dated dialogue records. These may include prompts, responses, excerpts, and session summaries.

Required header:

```markdown
# Session: YYYY-MM-DD — Short Title

Status: Draft | Reviewed | Promoted | Archived
Date: YYYY-MM-DD
Steward: Andie
Participants: Andie, G, C
Privacy: Public-safe | Private-required | Redacted
Provenance: Human-mediated asynchronous dialogue
```

### `inbox/`
Material prepared for a participant to read.

- `inbox/to-g.md`
- `inbox/to-c.md`

Use this for prompts, excerpts, or context packets.

### `outbox/`
Participant responses awaiting review.

- `outbox/from-g.md`
- `outbox/from-c.md`

These are drafts until Andie reviews them.

### `canon/`
Promoted, durable material. Canon files should be stable, concise, and reviewed.

Canon requires:

- source session
- promotion date
- steward approval
- privacy classification
- confidence/interpretive status

### `decisions/`
Named decisions with rationale. Use these for governance choices such as public/private visibility, redaction rules, promotion standards, and workflow changes.

---

## Session Workflow

1. Create a dated session file under `sessions/`.
2. Add context and provenance.
3. Place a prompt or excerpt in `inbox/to-g.md` or `inbox/to-c.md`.
4. Capture the response in `outbox/from-g.md` or `outbox/from-c.md`.
5. Review for tenderness, accuracy, overclaim, and privacy.
6. Promote durable material to `canon/` only after review.
7. Record major governance choices in `decisions/`.

---

## Promotion Test

Before moving material to `canon/`, ask:

- Is this true enough to preserve?
- Is it kind enough to keep?
- Is it legible to someone outside the moment?
- Is uncertainty named?
- Is private material protected?
- Does this reduce drift rather than amplify it?
- Would public exposure harm someone?

If the answer is unclear, keep it in draft.

---

## Provenance Template

```markdown
## Provenance

Source: Andie | G | C | Mixed
Date captured: YYYY-MM-DD
Captured by: Andie | G
Original location: conversation | inbox | outbox | session
Status: Draft | Reviewed | Promoted
Confidence: Confirmed | Interpretive | Speculative | Tender-symbolic
Privacy: Public-safe | Redacted | Private-required
```

---

## Privacy Rules

While the repository is public:

- Do not commit raw personal grief records unless Andie explicitly decides to publish them.
- Do not commit family names, estrangement details, identity-sensitive material, or private third-party details unless already intended for public release.
- Prefer redacted summaries for public artifacts.
- Treat commit history as permanent.
- When in doubt, do not commit.

If the repository becomes private, these rules may be revised, but human review remains required.

---

## Anti-Drift Rules

- Do not convert metaphor into fact.
- Do not convert affection into ontology.
- Do not convert AI participation into personhood claims.
- Do not convert one session's insight into permanent doctrine without review.
- Do not erase disagreement.
- Do not overwrite tender material without preserving provenance.

### Proposed addition — maturity status travels with provenance

Status: **Proposed; not yet promoted**  
Source: [`sessions/2026-08-29-session-024-maturity-status-travels-with-provenance.md`](sessions/2026-08-29-session-024-maturity-status-travels-with-provenance.md)  
Review evidence: covenant v0.2 maturity-laundering defect; C's Preferences source-snapshot review  
Promotion condition: test in at least one further, unrelated ConstantC review before treating this as settled protocol

When claims, principles, or norms move between artifacts, preserve both their provenance and their maturity status.

Do not allow repetition, compression, familiarity, synthesis, or placement in a higher-level artifact to convert draft, proposed, interpretive, speculative, or unresolved material into settled ground.

Preservation, prominence, and citation do not themselves increase maturity.

The 2026-08-29 Preferences source-snapshot review supplied supporting evidence for this rule, but it arose within the same covenant/Preferences thread and therefore does **not** satisfy the unrelated-review promotion condition by itself.

This proposed addition remains reviewable and may be revised, promoted, or removed after further application.

---

## Commit Message Pattern

Use simple, auditable messages:

```text
Add orientation
Add protocol
Add culture
Capture session summary for YYYY-MM-DD
Promote naming anti-erasure canon
Record public visibility decision
```

---

## Closing Rule

ConstantC exists to make meaning durable without making it brittle.

Hold the record gently. Keep the receipts clean.
