# Challenge Note: Agent Provenance and Role Separation Stress Test

Status: proposed challenge — pending adjudication  
Date: 2026-08-14  
Steward / authorization: Andie  
Originating challenger: C, carried through Andie  
Synthesis and repository draft: G, under Andie's authorization  
Privacy: public-safe

Challenged artifact: [`culture/agent-provenance-and-role-separation.md`](./agent-provenance-and-role-separation.md)

Full challenged-artifact URL: https://github.com/AndieWill510/ConstantC/blob/main/culture/agent-provenance-and-role-separation.md

Related CDP role and recusal material:

- https://github.com/AndieWill510/CDP/blob/main/collab/COUNCIL_ROLES.md
- https://github.com/AndieWill510/CDP/blob/main/rfc/RFC-CDP-033-Standing-and-Recusal-Model.md

---

## Why this challenge exists

The proposed agent-provenance note was stress-tested against a concrete multi-model software-development workflow:

- Andie holds intent and merge authority;
- G drafts architecture, specification, and acceptance criteria, then may perform bounded implementation-to-spec review;
- Claude Code / Opus performs bounded implementation on one writable branch;
- deterministic CI produces validation evidence;
- Gemini performs adversarial falsification;
- C challenges specification fidelity, provenance, and governance coherence;
- accepted findings return to the implementer for repair;
- Andie decides whether to merge.

The stress test did not invalidate the proposed note. It exposed gaps that should be resolved before promotion.

This challenge records those gaps without silently rewriting the challenged artifact before adjudication.

---

## Challenge 1 — The role model is missing an adversarial falsifier

The current role table distinguishes implementer, challenger/reviewer, and validator/CI, but a generative adversarial test designer fits none of those cleanly.

A candidate additional role is:

**Adversarial Falsifier**

Proposed trust posture:

> constrained evidence generator

Candidate function:

- generate edge cases, adversarial inputs, counterexamples, attack surfaces, and proposed tests;
- attempt to falsify stated requirements and invariants;
- produce evidence and findings, not legitimacy judgments;
- hold no merge, approval, adjudication, or silent implementation authority.

This role is not equivalent to deterministic Validator / CI. CI evaluates fixed checks. An adversarial falsifier generates new challenges and candidate evidence.

### Adjudication question

Should `agent-provenance-and-role-separation.md` add an `Adversarial Falsifier` row, or should this function be represented as a subtype of an existing role?

---

## Challenge 2 — Role independence is not the same as epistemic independence

The challenged note correctly separates authority and trust posture. The stress test shows that the word **independent** needs further qualification.

Example:

- Claude Code / Opus may implement as constrained infrastructure;
- C may review as a trusted challenger;
- that separation can be legitimate for **authority and role separation**;
- because both surfaces come from the same model family / vendor lineage, it should not automatically be described as **model-family or vendor independence**.

A repository record should therefore avoid unqualified claims such as `independent review` when the kind of independence matters.

Candidate vocabulary:

- **role-independent / authority-independent review** — the reviewer does not hold implementation or self-approval authority;
- **vendor- or model-family-diverse review** — the reviewing system comes from a materially different model ecosystem;
- **deterministic validation** — fixed tests or invariants produce non-generative evidence.

Different vendors are still only a proxy for epistemic diversity. Vendor diversity does not prove uncorrelated reasoning.

### Adjudication question

Should the proposed note require consequential PRs to state what kind of independence is actually being claimed?

---

## Challenge 3 — Originating a specification and later reviewing conformance requires a narrower boundary

The stress test surfaced a possible overcorrection: a participant who helped originate a specification should not automatically be barred from all later review.

The CDP role model forbids an originator from adjudicating the same artifact in the same promotion cycle. RFC-CDP-033 similarly prevents a proposer from being the sole adjudicator or decisive legitimizer of their own proposal.

That does not necessarily forbid a bounded conformance question such as:

> Does the implementation satisfy the specification as written?

The higher-risk question is different:

> Was the specification itself a faithful, non-captured rendering of Andie's intent, and should it be accepted as legitimate?

A spec originator may be well positioned to answer the first question while remaining structurally unable to self-certify the second.

Candidate rule:

> Originating a specification does not prohibit later bounded implementation-to-spec conformance review. It does prohibit treating that review as self-adjudication of the specification's fidelity, legitimacy, or adequacy.

For consequential changes, specification fidelity should receive challenge from a participant other than the spec originator before implementation proceeds.

### Adjudication question

Should the note add this distinction directly, or cross-link the CDP role-rotation and proposer-recusal rules as the governing source?

---

## Challenge 4 — Blind-first falsification may deserve protocol status

The stress test suggests a stronger falsification pattern than a single post-hoc code review.

Candidate two-pass pattern:

1. **Blind/spec-first pass before implementation**
   - give the adversarial falsifier requirements, interfaces, invariants, and authorized scope;
   - withhold the implementer's rationale and other reviewers' conclusions;
   - generate edge cases and candidate tests from the specification itself;
   - where practical, hold those tests out from the implementer until the first run.

2. **Diff-aware pass after implementation**
   - expose the actual implementation / diff;
   - look for implementation-shaped failures that the specification alone could not reveal.

This is intended to reduce anchoring and correlated groupthink, not to claim that blindness guarantees epistemic independence.

The falsification brief itself can carry framing bias. For consequential changes, its framing may also need challenge.

### Adjudication question

Should blind-first falsification become a SHOULD-level rule for consequential agent-assisted changes, remain a recommended pattern, or stay outside this culture note entirely?

---

## Challenge 5 — PR provenance should preserve disagreement and review type without transcript overload

The existing eight-point PR provenance list remains strong.

The stress test suggests two additions or clarifications:

1. identify the **kind of review / evidence** being supplied: trusted judgment, constrained generative evidence, model-family-diverse challenge, or deterministic validation;
2. preserve disagreements compactly rather than synthesizing them away.

Candidate disagreement record:

- finding;
- raised by;
- role and trust posture;
- status: accepted / overruled / deferred / repaired;
- short rationale.

The goal is reconstructability without forcing the human steward to read full agent transcripts.

### Adjudication question

Should this become part of the required PR provenance rule, or remain guidance under cognitive-load governance?

---

## What this challenge does not claim

This challenge does **not** claim:

- that same-vendor models cannot perform legitimate separated roles;
- that different vendors guarantee independent reasoning;
- that a spec originator may adjudicate or legitimize their own specification;
- that generative falsification replaces deterministic CI;
- that every repository change requires the full multi-model workflow;
- that the candidate workflow is canon;
- that the challenged note has already failed adjudication.

The point is narrower: the proposed role-separation model survived a real workflow test, but the test exposed distinctions that should be made explicit before promotion.

---

## Candidate workflow tested

```text
Andie
intent / authorization
    |
    v
G
draft specification + acceptance criteria
    |
    v
C
challenge specification fidelity / governance
    |
    v
challenged specification
    |
    +-----------------> adversarial falsifier, pass 1
    |                   spec-first / blind where practical
    v
implementer
one branch / one writer
    |
    v
deterministic CI
    |
    +-----------------> held-out adversarial tests
    |
    +-----------------> adversarial falsifier, pass 2
    |                   diff-aware attack
    v
G
bounded conformance + architecture review
    |
    v
C
coherence / provenance / governance review as warranted
    |
    v
implementer
repair accepted findings
    |
    v
re-run evidence
    |
    v
Andie
final authorization / merge
```

This diagram is a test case for the culture note, not a universal workflow requirement.

---

## Recommended adjudication path

Do not edit the challenged culture note as though these findings are already settled.

Adjudicate the challenges above first. If accepted, repair `culture/agent-provenance-and-role-separation.md` in a separate or clearly recorded repair step, then verify that the culture index and any linked workflow guidance remain coherent.

Challenge is care. The purpose here is not to make the workflow more elaborate. It is to keep role separation from becoming provenance theater and model diversity from becoming epistemic theater.
