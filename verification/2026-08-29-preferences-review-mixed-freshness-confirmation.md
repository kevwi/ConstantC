# Verification — Preferences Review Mixed-Freshness Confirmation

Status: active verification stub  
Date: 2026-08-29  
Steward: Andie  
Participants: Andie, G, C  
Privacy: public-safe  
Trigger: C's review of the Preferences source snapshot returned a mixed-freshness repository view

---

## Why this file exists

C's review of `origin/2026-08-29-chatgpt-preferences-verbatim.md` independently verified the snapshot hash correctly, while reporting two surrounding repository facts that were stale at review time:

1. C reported `COVENANT.md` on `main` as Draft v0.1.
2. C reported `origin/README.md` as listing only `constantc-is-a-curb-cut.md`.

At the same time, C had fresh enough access to the new Preferences snapshot to recompute and confirm its integrity values exactly.

This is therefore not best represented as a simple participant error. It is a mixed-freshness verification seam: different paths or objects were visible at different repository ages within the same review.

---

## Current intended live state

Repository:

https://github.com/AndieWill510/ConstantC

Current covenant:

https://github.com/AndieWill510/ConstantC/blob/main/COVENANT.md

Origin index:

https://github.com/AndieWill510/ConstantC/blob/main/origin/README.md

Verbatim Preferences snapshot:

https://github.com/AndieWill510/ConstantC/blob/main/origin/2026-08-29-chatgpt-preferences-verbatim.md

Verification index:

https://github.com/AndieWill510/ConstantC/blob/main/verification/README.md

---

## Commit-specific baseline

PR #11 merged as commit:

`8dc7ad6cf42d6e85faa664ac1d383ae3d170a749`

At that commit, the relevant paths are:

https://github.com/AndieWill510/ConstantC/blob/8dc7ad6cf42d6e85faa664ac1d383ae3d170a749/COVENANT.md

https://github.com/AndieWill510/ConstantC/blob/8dc7ad6cf42d6e85faa664ac1d383ae3d170a749/origin/README.md

https://github.com/AndieWill510/ConstantC/blob/8dc7ad6cf42d6e85faa664ac1d383ae3d170a749/origin/2026-08-29-chatgpt-preferences-verbatim.md

---

## Expected state at the baseline commit

### `COVENANT.md`

Expected header:

`Status: Draft v0.2 — revised after C review`

Known content SHA from G's connector read:

`be029aa9e9e161468d92b13f890ee8138b2da524`

### `origin/README.md`

Expected Records list includes both:

- `constantc-is-a-curb-cut.md`
- `2026-08-29-chatgpt-preferences-verbatim.md`

Known content SHA from G's connector read:

`b511e939b5af101f66e065f8bd4002082758944a`

### Preferences snapshot

Expected integrity values:

- Bytes: `4976`
- Lines: `41`
- SHA-256: `f61e3948e8dfb7050a054948e47dc430e17d3b114f549ed49231725c8ef0307d`

C independently recomputed these values and reported an exact match.

Known repository content SHA from G's connector read:

`442939e24dda35ab4a9daffc59d3d07e30c4abdd`

---

## What this verifies

This stub provides a fresh path and precise handles for independently checking that, by PR #11's merge commit:

- the root covenant had already advanced to Draft v0.2;
- the origin index already listed the Preferences snapshot;
- the Preferences snapshot existed with the integrity values C independently confirmed.

It also preserves the fact that C's review was substantively useful despite mixed repository freshness.

---

## What this does not verify

This stub does not establish why C received mixed-freshness reads.

It does not prove a particular cache, connector, branch-resolution, or retrieval mechanism was responsible.

It does not invalidate C's conceptual review findings merely because two repository-state observations were stale.

It does not promote any covenant candidate or protocol candidate.

Content SHAs are orientation handles, not authority C is required to accept.

---

## Remaining failure mode

If C or another collaborator still sees conflicting content through the commit-specific URLs above, the room should preserve that discrepancy and build a further verification handle rather than forcing convergence by assertion.

The point is independent verification, not authority performance.
