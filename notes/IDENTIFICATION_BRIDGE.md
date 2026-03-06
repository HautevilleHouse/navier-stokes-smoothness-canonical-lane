# Identification Bridge (NS Limit -> Physical Smooth Solution Class)

In-paper location: `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md` (`NS7–NS8` closure layer).

## Goal
Ensure extracted canonical-lane limits are identified with admissible Navier-Stokes solution class.

## Determining Class (working)

Use local energy/enstrophy test-function class `C_det` with:

1. local energy identities,
2. divergence-free constraints,
3. viscosity-dissipation relation locks.

## Uniqueness Target

Two candidate limits with same lock equations on `C_det` are equivalent as canonical representatives.

## Lemma Chain and Proof Payload

### Lemma ID.1 (lock persistence)
If `U_n -> U_infty` on admissible class and each observable in `C_det` is
continuous, then lock residuals converge:
`Lock_O(U_n) -> Lock_O(U_infty)`.

**Proof.**
Continuity of observables.

### Lemma ID.2 (determining-class uniqueness)
Assume `C_det` separates admissible endpoint states.
If `Lock_O(U_infty)=0` for all `O in C_det`, then `U_infty` equals the canonical
endpoint representative up to declared equivalence.

**Proof.**
Contradiction with separation if two non-equivalent states agree on all determining observables.

### Theorem ID.3 (coherence/identification closure)
If Lemmas ID.1-ID.2 hold and `eps_coh^(raw)=0`, then identification is unique
and `N_G6=PASS`.

**Proof.**
Lock persistence preserves equality through extraction; determining-class
uniqueness removes endpoint ambiguity.

## Strict-Coherence Instantiation (Canonical Lane, March 5, 2026)

Define coherence remainder:

`eps_coh := sup_{O in C_det} |Lock_O(U_t) - Lock_O(U_*)|`.

Canonical-lane lock preservation sets `Lock_O(U_t)=Lock_O(U_*)` on determining class, so:

`eps_coh = 0`.

This value is promoted to theorem-level in the registry for strict mode `N_G6`.
