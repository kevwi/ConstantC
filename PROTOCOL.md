# ConstantC — Working Protocol

Status: Draft v0.2 — active working protocol  
Date: 2026-06-03  
Last updated: 2026-09-01  
Steward: Andie  
Visibility note: This repository is currently public. Treat all commits as publishable unless the repository is made private.

---

## Purpose

This protocol keeps ConstantC legible, honest, auditable, and humane.

The repo exists to support asynchronous, human-mediated dialogue between Andie, G, and C. It preserves context without pretending that context is private, canonical, or complete by default.

---

## Core Rules

1. **Human stewardship is required.** Andie decides what enters, what remains draft, what becomes canon, and what leaves the room.
2. **No live AI-to-AI claim.** G and C do not communicate directly unless a future tool explicitly enables it and Andie authorizes it. The present workflow is mediated and asynchronous. Any material change that enables autonomous cross-participant communication, shared-state read/write coordination, or action on another participant's durable output triggers re-review of [`canon/memory-is-capability.md`](canon/memory-is-capability.md) and its enforcement assumptions.
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
Promoted, durable material and clearly marked canon candidates. Directory placement is
not a maturity signal: only a file's explicit status and promotion record establish
canon. Canon files should be stable, concise, and reviewed.

Canon requires:

- source session
- promotion date
- steward approval
- privacy classification
- confidence/interpretive status

Candidate files may be kept in `canon/` while under review so their intended
constitutional scope is legible. They must say **canon candidate** (or equivalent),
must not be cited as settled ground, and must not use promotion metadata that implies
an event which has not occurred.

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

### Active working rule — maturity status travels with provenance

Status: **Active working protocol rule; promoted 2026-09-01**  
Source: [`sessions/2026-08-29-session-024-maturity-status-travels-with-provenance.md`](sessions/2026-08-29-session-024-maturity-status-travels-with-provenance.md)  
Unrelated review evidence: [`sessions/2026-09-01-session-026-memory-is-capability-adversarial-review.md`](sessions/2026-09-01-session-026-memory-is-capability-adversarial-review.md)  
Promotion basis: the Session 024 rule was tested against a substantively unrelated canon review and detected the same class of maturity-laundering defect in a different topic and artifact

When claims, principles, norms, instructions, or decisions move between artifacts, preserve both their provenance and their maturity status.

Do not allow repetition, compression, familiarity, synthesis, citation, eloquence, or placement in a higher-level artifact to convert draft, proposed, interpretive, speculative, unresolved, or merely reviewed material into more mature ground without an explicit promotion or adjudication event.

Preservation, prominence, discoverability, and citation do not themselves increase maturity.

If the source's maturity changes later, do not silently back-propagate that change into every artifact that once cited it. Update receiving artifacts through an explicit review or promotion step so the record remains reconstructable.

### Promotion history

Session 024 first proposed this rule after C identified maturity laundering in the Covenant v0.2 review.

The original promotion condition required at least one further, unrelated ConstantC review.

In Session 026, C reviewed `canon/memory-is-capability.md`, a different artifact on shared memory, authority, and future agent coordination, and independently identified a maturity error: G had converted Andie's request for "something canonical" into the stronger claim that the rule was already "settled."

Applying the candidate rule produced a concrete repair.

The unrelated-review condition is therefore satisfied.

The rule is now active working protocol. It remains revisable like the rest of this working protocol; promotion means it has earned current governing use, not immunity from future challenge.

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
