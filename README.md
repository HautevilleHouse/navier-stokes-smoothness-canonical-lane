# 3D Navier-Stokes Global Regularity via Dissipative Persistence
## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`NS1–NS8`).

Canonical Lane research workspace for the Millennium problem:

the global existence and smoothness of solutions to the 3D incompressible Navier–Stokes equations.

## Main Manuscript

- [paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md](paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md)
- [paper/CANONICAL_ROUTING_INDEX.md](paper/CANONICAL_ROUTING_INDEX.md)

## Structure

- `paper/`: main theorem architecture (`NS1–NS8` chain).
- `notes/`: closure notes (`EG1`–`EG4`) + identification bridge.
- `repro/`: local certificate workflow and rerun protocol.
- `scripts/`: local guard and extraction scripts.
- `artifacts/`: constants registries and stitched constants.

## Local Reproducibility Command

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

## How To Read This Professionally

1. Theorem chain first: read `paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md`.
2. Constants provenance second: audit `paper/EXTRACTION_SPEC.md`, `artifacts/constants_extraction_inputs.json`, `artifacts/constants_extracted.json`, and `artifacts/promotion_report.json`.
3. Pipeline third: run `bash repro/run_repro.sh` to audit hashes/provenance/gates; it is reproducibility infrastructure, not theorem generation.

Release modes:

- `normalized`: `status=normalized_placeholder` allowed when explicitly labeled.
- `fully_extracted`: requires `status=derived_numeric` for all required constants/stitch keys.

Current NS runner policy:

- `repro/run_repro.sh` enforces `fully_extracted` mode.

## Citation

- Metadata: [CITATION.cff](CITATION.cff)
- Manuscript target: [paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md](paper/NAVIER_STOKES_SMOOTHNESS_PREPRINT.md)

## Authorship

- Program author: **HautevilleHouse**
- Canonical attribution source: [`CITATION.cff`](CITATION.cff)
