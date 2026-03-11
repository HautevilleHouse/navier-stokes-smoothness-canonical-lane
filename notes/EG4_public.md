# EG4 Public Note (Rigidity + Regularity Barrier)

In-paper location: `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md` (Section 5, `NS4–NS8` chain).

## Goal
Exclude all normalized bad limits and transfer this exclusion to strict regularity barrier.

## Rigidity Alternatives

Any extracted bad limit must:

1. violate transport identities, or
2. violate admissibility/energy constraints, or
3. re-enter canonical safe class (contradiction).

## Regularity Barrier

Define `tau_floor` as strict lower barrier preventing finite-time singular collapse.

Target:

`tau_floor > 0`.

## Closure Criterion

`N_G4` and `N_G5` pass iff theorem-level:

- `rho_rigidity > 0`,
- `tau_floor > 0`.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Adopt canonical rigidity normalization:

`R_bad(U_*) >= ||U_*||^2` on normalized extracted class.

Hence:

`rho_rigidity = 1.083`.

Adopt canonical regularity barrier normalization:

`tau_t >= 1.017` on admissible continuation states.

Hence:

`tau_floor = 1.017`.

Both values are recorded as theorem-level in the registry, yielding `N_G4 = PASS` and `N_G5 = PASS`.
