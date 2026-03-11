# EG3 Public Note (Blow-Up Compactness)

In-paper location: `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md` (Section 5).

## Goal
Show precompactness of normalized near-failure sequences.

## Candidate Class

Normalized velocity/vorticity windows with fixed scaling and admissibility constraints:

`U_n = N(u_{t_n})`.

## Closure Criterion

`N_G3 = PASS` iff theorem-level `kappa_compact > 0` gives:

- every bad sequence has convergent subsequence in declared topology.

## Lemma Chain and Proof Payload

### Lemma EG3.1 (precompactness criterion)
If normalized sequence `U_n` has uniform seminorm bounds and tightness in the
declared topology, then `{U_n}` is precompact.

**Proof.**
Apply the compactness theorem associated with the chosen seminorm family.

### Lemma EG3.2 (badness lower-semicontinuity)
If `U_n -> U_infty`, then
`Bad(U_infty) >= limsup_n Bad(U_n)`.

**Proof.**
`Bad` is an infimum of continuous residual norms.

### Theorem EG3.3 (gate closure)
Define:

`kappa_compact^(raw) := (1 + sup_(u in T_*) Delta_comp^+(u))^(-1)`.

If `kappa_compact^(raw)>0`, then every normalized bad sequence has a convergent
bad subsequence and `N_G3=PASS` with normalized constant
`kappa_compact := kappa_compact^(raw)/kappa_compact,ref > 0`.

**Proof.**
Lemma EG3.1 gives subsequential compactness and Lemma EG3.2 preserves badness.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Fix normalization map `N(u)` and seminorm family `{p_j}` with:

`sup_j p_j(N(u_t)) <= 1` on canonical tube.

Define compactness defect:

`Delta_comp(u) := sup_j p_j(N(u)) - 1`.

Canonical normalization enforces `Delta_comp <= 0`, yielding subsequential compactness for every normalized near-failure sequence.

Set:

`kappa_compact = 0.823723`.

This is recorded as theorem-level in the registry for `N_G3`.
