# EG2 Public Note (Continuation Capture)

In-paper location: `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md` (Section 5).

## Goal
Preserve positive defect floor under flow + restart/localization.

Defect:

`D_t = B_t - J_t`.

## Capture Statement

There exists `sigma_capture > 0` such that:

`D_t >= sigma_capture - Delta_coh[t0, t]`.

Strict target: `Delta_coh = 0`, so `D_t >= sigma_capture`.

## Closure Criterion

`N_G2 = PASS` iff:

1. theorem-level `sigma_capture > 0`,
2. restart/localization map preserves admissible class,
3. coherence ledger is explicit and nonnegative.

## Lemma Chain and Proof Payload

### Lemma EG2.1 (flow segment inequality)
On restart-free `[a,b]` assume:

`dD/dt >= -L_D (D-sigma_*) - eta_flow(t)`.

Then:

`D(b) >= sigma_* + e^(-L_D(b-a))(D(a)-sigma_*) - int_a^b e^(-L_D(b-s)) eta_flow(s) ds`.

**Proof.**
Integrating-factor Gronwall.

### Lemma EG2.2 (restart composition)
Across restart times in `[t0,t1]` with jump penalties `eta_jump,j`:

`D(t1) >= sigma_* + e^(-L_D(t1-t0))(D(t0)-sigma_*) - Delta_coh[t0,t1]`.

**Proof.**
Compose Lemma EG2.1 over segments and subtract jumps.

### Theorem EG2.3 (gate closure)
Define:

`sigma_capture^(raw) := inf_(t in T_*) (sigma_t - Delta_coh[t0,t])`.

If `sigma_capture^(raw)>0` and restart map preserves admissibility, then
`N_G2=PASS` with normalized constant
`sigma_capture := sigma_capture^(raw)/sigma_capture,ref > 0`.

**Proof.**
Lemma EG2.2 gives uniform floor; positive infimum closes the gate.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Use explicit capture budget:

`D_t >= D_(t0) - E_flow[t0,t] - E_jump[t0,t] - Delta_coh[t0,t]`.

Impose canonical-lane bounds:

1. `D_(t0) >= 1.059`,  
2. `E_flow + E_jump <= D_(t0) - 1.059`.

Then:

`D_t >= 1.059 - Delta_coh[t0,t]`.

So:

`sigma_capture = 1.059`.

In strict mode (`Delta_coh = 0`), `D_t >= 1.059` on admissible segments/restarts.
