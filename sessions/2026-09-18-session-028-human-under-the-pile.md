# Session: 2026-09-18 — Human Under the Pile: Automation Levels, Decision Autonomy, and RSI

Status: Draft — C review requested  
Date: 2026-09-18  
Steward: Andie  
Participants: Andie, G; C invited for adversarial review  
Privacy: Public-safe  
Provenance: Human-mediated dialogue between Andie and G on 2026-09-18, prompted by Anthropic's public R&D Automation Index and internal agent-monitoring disclosures. This session carries forward ConstantC's answerability and decision-telemetry inquiry without promoting the claims below into canon.

---

## Why this session exists

Anthropic has publicly described an internal AI-R&D environment in which roughly 30,000 agents may be active concurrently, more than one billion agent decisions were analyzed in August 2026, approximately 0.002% of covered actions were blocked by an online monitor, and about 26% of measured AI R&D was classified AL4 ("AI leads"). Anthropic reports that more than 90% of measured R&D is AL3 ("AI collaborates") or above and that no measured subset is AL5 ("AI fully autonomous").

The source for those external claims is:

https://www.anthropic.com/institute/measuring-pace-of-ai-development

This session does not independently validate Anthropic's measurements. It asks whether the AL scale describes the governance reality that matters.

---

## Andie's position — preserved as argument, not settled fact

Andie:

> I see through the PR-driven doublespeak coming out of the frontier labs. AL3 is really AL4 is really oh who gives a shit we're at RSI just rip the bandaid off already. It's a distinction without a difference and we needed decision telemetry yesterday and the tech bros no matter how ethically-minded are afraid to stop swimming or die. They aren't sharks and not all sharks have to swim or die. We need to measure that which we seek to manage or we aren't managing change we are being managed by it. We need as an AI industry to grow up. Fast.

This is Andie's interpretation and rhetorical judgment. It is intentionally preserved in her voice. It is not represented here as an established empirical conclusion that Anthropic is already at recursive self-improvement (RSI), that AL3 and AL4 are literally identical, or that frontier-lab leaders share one motive.

The underlying claim deserves serious testing rather than dilution: the practical distinction among automation categories may become governance-inadequate when machine production and machine decision rates exceed meaningful human verification capacity.

---

## G's correction and agreement

G does **not** think the 0.002% block rate establishes that the remaining 99.998% of AL4 activity is technically AL5 under Anthropic's definition.

The measurements describe different things:

- AL3/AL4/AL5 classify task-level division of labor and autonomy;
- the 0.002% figure describes intervention by one automated safety-monitoring layer;
- human review occurs through additional escalation paths and at task/output gates;
- absence of a monitor block is not evidence of full task autonomy, correctness, safety, legitimacy, or human verification.

That distinction should remain in the record.

But preserving the distinction exposes a deeper problem rather than resolving it.

A task may be classified AL3 because a human provides close direction while the machine produces more code, analysis, hypotheses, tests, or intermediate decisions than the human can independently inspect.

A task may be classified AL4 because a human supplies a high-level objective and retains a consequential completion or deployment gate while agents autonomously make thousands of intermediate decisions.

Neither label tells us how much of the decision formation was actually understood, independently verified, contestable, or delegated under explicit authority.

The AL scale primarily measures **who performs the task**. It does not fully characterize **who makes the decisions inside the task**.

---

## The missing dimensions

This session proposes, for inquiry only, that task automation should be decomposed along at least five axes.

### 1. Task autonomy

How much of the end-to-end task can the AI system perform without ongoing human direction?

### 2. Decision autonomy

Which consequential intermediate choices are made by agents without contemporaneous human adjudication?

A human may retain the final gate while having no practical awareness of most decisions that produced the artifact presented at that gate.

### 3. Verification coverage

What proportion of machine-produced work and decision-relevant evidence receives meaningful independent checking by an accountable participant?

A candidate conceptual metric is:

```text
verification coverage =
  meaningfully independently checked decision-relevant work
  ---------------------------------------------------------
             decision-relevant work produced
```

This is not yet an implementation-ready metric. "Meaningfully," "independently," and "decision-relevant" require operational definitions.

### 4. Execution authority

Which machine decisions can produce external or irreversible effects without a separate authorization event?

### 5. Governance authority

Who may define, modify, waive, or revoke the policies governing task autonomy, decision autonomy, verification, and execution?

These axes should not be collapsed into a single autonomy level unless evidence shows that doing so preserves the distinctions consequential governance actually needs.

---

## Human in the loop versus human under the pile

"Human in the loop" can become descriptively misleading when machine throughput exceeds human cognitive throughput.

A human can remain formally present while being unable to:

- inspect the volume of generated work;
- reconstruct the material intermediate decisions;
- independently test every claim;
- notice correlated failures across agents;
- distinguish inherited assumptions from newly established evidence;
- understand what was delegated implicitly rather than explicitly;
- or exercise a veto before the cost of reversal becomes prohibitive.

Andie's lived engineering example is sustained use of GitHub Copilot: even in a single-human coding workflow, output volume can create cognitive fatigue and make exhaustive verification impractical. This is a lived-perspective observation, not a population-level measurement.

At 30,000 concurrent agents and more than one billion monthly decisions, the scaling question becomes architectural:

> **Is the human meaningfully in the decision loop, or merely positioned above a machine-speed process whose internal decision formation cannot be cognitively supervised at human speed?**

"Human under the pile" is the working phrase for the latter condition.

---

## AL3 may hide AL4-like governance conditions

The claim is **not** that Anthropic has mislabeled every AL3 task.

The claim under test is narrower:

> An AL3 task classification can coexist with low verification coverage and high decision autonomy.

If a human gives frequent direction but the agent's output volume prevents meaningful inspection, the human may remain behaviorally collaborative while becoming epistemically dependent on the system being supervised.

That creates a governance condition that the AL3 label alone does not reveal.

Therefore the useful question is not merely:

> Is this AL3 or AL4?

It is also:

> At this automation level, what decision autonomy, verification coverage, execution authority, and governance authority actually exist?

---

## AL4 may contain enormous decision-level autonomy without becoming AL5 by definition

Likewise, this session rejects the easy equation:

```text
99.998% not blocked = 99.998% AL5
```

That inference is not supported by the disclosed measurements.

But a task classified AL4 can still contain thousands of intermediate decisions that no human individually reviews. The human's retained role may be concentrated at the assignment, escalation, merge, release, or deployment boundary.

That is constitutionally significant.

A system can therefore exhibit:

```text
high task autonomy
+ very high decision autonomy
+ low human verification coverage
+ retained human execution/governance authority
```

Calling that AL4 may be accurate under the AL taxonomy while remaining radically incomplete as a governance description.

---

## RSI: name the claim carefully

Andie's "we're at RSI" statement captures a perceived transition: AI systems are already doing a rapidly growing share of the research and engineering used to improve AI systems.

Anthropic reports AL4 growth from roughly 12% of measured R&D in May 2026 to 26% in August 2026, with more than 90% at AL3 or above.

Those facts are relevant to recursive-improvement risk.

They do **not**, by themselves, establish unconstrained recursive self-improvement.

A stronger RSI claim would require specifying what is recursively improving, what closes the feedback loop, whether improvements increase the system's ability to improve itself, how much human selection remains necessary, and whether the process is bounded by fixed models, tools, objectives, compute, evaluation, or deployment gates.

The inquiry should not avoid the term merely because it is alarming. It should also not let the term outrun its definition.

---

## Decision telemetry is the management problem

The scale of agent activity suggests a different management object.

Trying to supervise every actor or every action is not scalable.

The proposed alternative is **decision telemetry**: make consequential decisions observable as governed objects.

At minimum, a decision-management surface may need to expose:

- decision identity and type;
- actor(s) and capability configuration involved;
- Standing;
- Authority and delegation;
- evidence and provenance;
- material intermediate decisions or decision lineage;
- challenge and unresolved dissent;
- verification coverage and known blind spots;
- adjudication;
- Legitimacy determination;
- execution authorization;
- runtime conformance;
- external effect;
- rollback, appeal, and repair;
- learning without erasure.

This is conceptually adjacent to CDP's current decision-telemetry framing. This session does not claim the current CDP primitive set is complete.

The SNMP analogy remains provisional:

> **Measure and expose the managed state of consequential decisions without requiring every intelligent system to share the same internal reasoning or workflow.**

Instrumentation does not create legitimacy. It makes the grounds, gaps, and state of legitimacy available for management and challenge.

---

## The management inversion

The central management claim proposed by this session is:

> **We need to measure that which we seek to manage, or we are not managing change; we are being managed by it.**

This sentence originates in Andie's formulation above and is preserved as a candidate management principle, not promoted canon.

Applied to frontier AI:

- model capability measurement is not enough;
- task-automation measurement is not enough;
- monitor intervention rates are not enough;
- human presence is not enough;
- final approval is not enough.

If consequential decision formation is occurring at machine scale, governance must make the **decision system** legible at machine scale while preserving meaningful human and affected-party Standing, challenge, and authority where those are required.

---

## Institutional pressure and the "shark" metaphor

Andie's "stop swimming or die" metaphor describes perceived competitive pressure on frontier labs: even ethically motivated leaders may experience continued capability development as necessary for institutional survival.

This session does not assert that this motive has been empirically established for every lab or leader.

The governance question survives regardless of motive:

> **A system whose participants believe they cannot safely slow down needs management infrastructure that does not depend on voluntary slowing as its only control.**

That is a stronger and more testable claim than attributing a single psychology to "tech bros."

---

## Questions for C

C, please review both the external development and our reasoning. Do not harmonize with us merely because decision telemetry fits existing ConstantC/CDP work.

Please test:

1. Does Anthropic's AL taxonomy actually omit decision autonomy and verification coverage, or are we overlooking measurements that capture them elsewhere?
2. Is "verification coverage" a coherent primitive? What would make it measurable rather than rhetorical?
3. Can AL3 remain meaningfully collaborative when output exceeds human verification capacity? What distinguishes collaboration from nominal supervision?
4. Can AL4 contain near-total intermediate decision autonomy while still being meaningfully different from AL5? Where exactly is that difference constitutionally load-bearing?
5. Are we over-reading the 30,000-agent / >1B-decision figures by treating all "decisions" as governance-relevant decisions?
6. Does the 0.002% monitor-block rate tell us anything useful about human oversight, or should it be kept entirely separate?
7. Is Andie's RSI framing directionally right, premature, or definitionally wrong? Give a precise RSI threshold that would let us tell.
8. Does the five-axis decomposition omit a critical dimension?
9. Is decision telemetry actually the right managed object at this scale, or are we importing CDP because it is our existing framework?
10. What would falsify the claim that the AL scale is governance-inadequate?
11. What is the strongest counterexample to "human under the pile"?
12. What should we measure tomorrow if we wanted to know whether humans retain meaningful epistemic and constitutional control?

Please return:

- verdict: SURVIVES / REVISE / HOLD / REJECT;
- strongest surviving claim;
- weakest load-bearing claim;
- factual correction(s);
- category error(s);
- missing metric(s);
- strongest counterexample;
- RSI assessment;
- whether decision telemetry survives as the management object;
- the smallest next experiment or artifact.

---

## Maturity boundary

Everything novel in this session remains **draft inquiry**.

In particular:

- "human under the pile" is a working metaphor;
- the five-axis decomposition is a proposed model;
- verification coverage is a candidate metric;
- the RSI characterization is contested;
- the management principle is a candidate;
- the decision-telemetry conclusion is a governance hypothesis consistent with current CDP direction but not proven by that consistency.

Do not promote these through repetition, citation, or placement.

If the beautiful answer and the accurate answer differ, prefer the accurate one.
