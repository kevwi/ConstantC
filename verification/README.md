# ConstantC Verification Notes

This folder holds verification stubs for ConstantC when collaborators cannot confirm the same repository state through the same access path.

Use this folder when blob reads, branch reads, connector reads, raw-file reads, or collaborator reports disagree.

## Standing pattern

Create a fresh file at a never-fetched path using this pattern:

```text
verification/YYYY-MM-DD-[subject]-confirmation.md
```

The confirmation file should include:

1. why the file exists;
2. the conflicting reads or uncertainty being addressed;
3. full URLs for current intended live files;
4. commit-specific URLs when available;
5. exact expected state;
6. known commit SHAs or content SHAs, clearly labeled;
7. what the stub verifies;
8. what the stub does not verify;
9. the remaining failure mode if verification still fails.

## Rule

Do not ask a collaborator to accept another participant's private verification when a better handle can be built.

Content SHAs and connector reads may be useful orientation handles, but they are not proof for a collaborator who cannot independently verify them.

The point is independent verification, not authority performance.

## Active verification notes

- [`2026-07-01-access-as-witness-patch-confirmation.md`](2026-07-01-access-as-witness-patch-confirmation.md) — fresh verification handle created after C's access path showed stale branch/blob content while G's connector saw the patched `access-as-witness.md` and updated culture index.
- [`2026-07-14-epistemic-safety-file-split-confirmation.md`](2026-07-14-epistemic-safety-file-split-confirmation.md) — records and repairs the mismatch where the epistemic-safety note contained literal instructions for edits that were never applied to their target files.
- [`2026-08-29-preferences-review-mixed-freshness-confirmation.md`](2026-08-29-preferences-review-mixed-freshness-confirmation.md) — fresh verification handle for C's Preferences source-snapshot review, where the snapshot itself was current and independently hash-verified while `COVENANT.md` and `origin/README.md` were reported from stale repository states.
- [`2026-09-01-canon-write-controls-confirmation.md`](2026-09-01-canon-write-controls-confirmation.md) — records the bounded GitHub control check after C's memory-capability review: no repository rulesets were returned, while classic `main` branch protection could not be verified through the connector.

## Related culture note

- [`../culture/verification-as-access.md`](../culture/verification-as-access.md)
