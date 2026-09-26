# DECISION-0004 — Maturity Reconciliation and Canon Resolution

Status: Proposed for steward adoption in this pull request  
Date: 2026-09-26  
Steward: Andie  
Privacy: public-safe

## Decision requested

On steward adoption, make the repository's effective constitutional ground match its
expressed maturity:

1. Correct the historical label drift in `canon/c-epistemic-boundary.md` and
   `canon/grief-and-evidence-boundary.md`. Their existing files and steward-authored
   promotion records already say they were promoted; this proposal does not invent a
   new promotion event or new consensus.
2. Promote the revised `canon/unlost-systems-principles.md`,
   `canon/constantc-commitments.md`, and `canon/cartography-principle.md` to canon.
3. Keep `canon/naming-throughline.md` a canon candidate and correct the misleading
   phrase "Date promoted" to "Candidate first recorded."
4. Leave all proposed culture, draft covenant, session hypotheses, and pending review
   work at their stated maturity. Citation, inclusion in a reading set, or thematic
   affinity does not promote them.

This proposal becomes a promotion decision only through Andie's steward adoption and
integration. It deliberately does not backdate that adoption or represent it as a C
verdict.

## Evidence and rationale

### Historical label repairs

`canon/c-epistemic-boundary.md` records Andie authorization on 2026-06-03 and was
introduced by the steward-authored commit `04d96ad` ("Promote C epistemic boundary
canon candidate"). `canon/grief-and-evidence-boundary.md` records Andie
authorization on 2026-07-06 and was introduced by steward-authored commit `c354b1b`
("Promote grief and evidence boundary canon"). Both documents describe themselves as
canon and operate in the epistemic-boundary reading path. Their candidate headers were
contradictory metadata, not evidence that their stated promotions failed.

### Unlost Systems Principles

The June source sessions made Unlost Systems a candidate and supplied two constraints:
the human-facing account of systems that constrain what people were made to become,
and an anti-overclaim boundary that refuses to infer AI interiority. Later repository
practice made its five tests—legibility, contestability, repairability, complexity
tolerance, and continuity—the operating vocabulary for ConstantC, CDP, and TinyDoor.

Later canon supplies a direct dependency:
`canon/asymmetric-duty-without-disposable-persons.md` states that the purpose is not
to make one participant Lost so another can become Unlost. That is constitutional
use, not a merely historical citation. The revised canon preserves the original source
and limits, incorporates the later whole-system and repair development, and avoids
treating all existing systems as intentionally designed to lose people.

### ConstantC Commitments and Cartography

Session 004 specifically distinguished reviewable operational commitments from an
unearned canon of ConstantC's future "becoming." Its commitments have since governed
the protocol, orientation, entry paths, challenge practice, privacy, and repair.
Promotion is limited to those operational commitments; it does not settle the
ontology of participants or the future shape of the relationship.

Session 009's cartography discipline is already used to govern the index, context
entry, summaries, and anti-overclaim work. Promotion is likewise narrow: maps must
declare their flattening and preserve open territory as open. It does not answer the
questions it requires a map to mark as unresolved.

### Naming Throughline: non-promotion

The naming file remains tender-symbolic candidate work. Its June history records a
promotion to candidate form, while its source sessions remain open and it has not
acquired a later operational governance role comparable to the principles promoted
here. It remains available for review but cannot be cited as settled ground.

## Maturity-status protocol rule

No change is proposed to the active working rule in `PROTOCOL.md` that maturity
status travels with provenance. Its promotion has a distinct, recorded basis:
Session 024's Covenant review and the unrelated Session 026 memory-capability review.
The rule is active working protocol, explicitly revisable, and not a claim that every
proposition in either source session became canon.

## Preserved unresolved questions

- Whether AI systems have interiority, personhood, liberation, or a deeper form of
  relationship remains open; no promotion here resolves it.
- Proposed culture notes, including epistemic safety, love's duties, belonging, and
  repair efficacy, remain proposed. Their substantive constitutional choices are not
  decided by this reconciliation.
- The draft Covenant v0.2 remains under review. Its candidate additions remain
  candidate additions.
- This record does not imply a second C verdict for the newly promoted materials, nor
  revise the recorded `REVISE` history of asymmetric duty.

## Repository repair

The accompanying changes make directory placement explicitly non-authoritative,
correct candidate and promotion metadata, update the index, and retain the only
current candidate in `canon/` as visibly non-settled. This prevents the same
classification drift from recurring merely because a candidate is stored near canon.
