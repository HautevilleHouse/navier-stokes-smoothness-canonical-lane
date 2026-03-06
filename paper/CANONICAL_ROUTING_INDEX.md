# Canonical Routing Index (Navier-Stokes)

This file is the single routing map for where each proof package lives in:

- main preprint sections,
- mirror note files,
- certificate/artifact keys.

## Gate Routing

| Gate | Main preprint location | Mirror note | Registry/artifact key(s) |
|---|---|---|---|
| `N_G1` (coercivity) | `Section 4/5` (`NS1`) | `notes/EG1_public.md` | `kappa_enstrophy` |
| `N_G2` (capture) | `Section 4/5` (`NS2`,`NS3`) | `notes/EG2_public.md` | `sigma_capture` |
| `N_G3` (compactness/no-Zeno) | `Section 5` (`NS4`) | `notes/EG3_public.md` | `kappa_compact` |
| `N_G4` (rigidity) | `Section 5` (`NS5`) | `notes/EG4_public.md` | `rho_rigidity` |
| `N_G5` (regularity floor) | `Section 5` (`NS8`) | `notes/EG4_public.md` | `tau_floor` |
| `N_G6` (strict coherence) | `Sections 3/4` | `notes/IDENTIFICATION_BRIDGE.md` | `eps_coh` |
| `N_GM` (final strict margin) | `Section 3` margin formula | derived | all above keys |

## Identification Routing

| Topic | Main preprint location | Mirror note |
|---|---|---|
| Determining-class lock and strict coherence | `Sections 3/4/8` | `notes/IDENTIFICATION_BRIDGE.md` |

## Repro Routing

| Artifact | Path |
|---|---|
| Runner | `repro/run_repro.sh` |
| Guard | `scripts/ns_closure_guard.py` |
| Runtime certificate | `repro/certificate_runtime.json` |
| Baseline certificate | `repro/certificate_baseline.json` |
| Registry | `artifacts/constants_registry.json` |
| Stitch constants | `artifacts/stitch_constants.json` |
| Third-party rerun protocol | `repro/THIRD_PARTY_RERUN_PROTOCOL.md` |
