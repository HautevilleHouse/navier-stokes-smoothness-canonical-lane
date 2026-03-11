# Public Reproducibility Pack (NS Canonical Lane)

## Objective
Provide a local, hash-locked rerun path for Navier-Stokes closure gates.

## Included Artifacts

1. `repro_manifest.json`,
2. `run_repro.sh`,
3. baseline output `certificate_baseline.json`,
4. `THIRD_PARTY_RERUN_PROTOCOL.md`.

## Runner

From repository root:

```bash
bash repro/run_repro.sh
```

This executes:

```bash
python3 scripts/ns_closure_guard.py --strict-coh-zero --registry artifacts/constants_registry.json --stitch artifacts/stitch_constants.json --out repro/certificate_runtime.json --history repro/drift_guard_runs.jsonl --pretty
```

## Pass Criteria

1. `repro/certificate_runtime.json` exists,
2. lane is `manifold_constrained`,
3. `all_pass` is `true`,
4. all gates `N_G1,N_G2,N_G3,N_G4,N_G5,N_G6,N_GM` are `PASS`.
