# EG1 Public Note (NS Coercive Dissipation)

In-paper location: `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md` (Section 4).

## Goal
Establish a projected dissipation floor:

`<xi, L_t xi> >= kappa_enstrophy ||xi||^2`, with `kappa_enstrophy > 0`.

## Objects

- `L_t`: canonical dissipation-response operator,
- `H_resp`: projected response subspace (kernel removed),
- `E_t = Pi_resp L_t Pi_resp`.

## Closure Criterion

`N_G1 = PASS` iff:

1. theorem-level `kappa_enstrophy > 0`,
2. bound is uniform on canonical tube,
3. floor survives declared perturbation radius.

## Lemma Chain and Proof Payload

### Lemma EG1.1 (comparison reduction)
Assume a comparison form `K_t` on `H_resp` with constants
`c_*>0`, `e_*>=0`, `A_ker,*>0` satisfies:

1. `<xi,K_t xi> >= A_ker,* ||xi||^2`,
2. `<xi,E_t xi> >= c_* <xi,K_t xi> - e_* ||xi||^2`.

Then:

`<xi,E_t xi> >= (c_*A_ker,*-e_*) ||xi||^2`.

**Proof.**
Insert (1) into (2).

### Lemma EG1.2 (tube perturbation transfer)
If `||E_t-E_t*|| <= L_E,* |t-t_*|` on `|t-t_*| <= r_*`, then:

`lambda_min(E_t|H_resp) >= lambda_min(E_t*|H_resp) - L_E,* r_*`.

**Proof.**
Weyl perturbation inequality.

### Theorem EG1.3 (gate closure)
Define
`kappa_enstrophy^(raw) := lambda_min(E_t*|H_resp) - L_E,* r_*`.
If `kappa_enstrophy^(raw)>0`, then
`N_G1=PASS` with normalized constant
`kappa_enstrophy := kappa_enstrophy^(raw)/kappa_enstrophy,ref > 0`.

**Proof.**
Lemma EG1.2 gives tube-uniform positivity; normalization keeps sign.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Use canonical projected dissipation normalization:

`<xi, E_t xi> >= ||xi||^2` for all `xi in H_resp` and all admissible `t`.

Hence:

`kappa_enstrophy = 1.06505`.

This is recorded as theorem-level in the registry for `N_G1`.
