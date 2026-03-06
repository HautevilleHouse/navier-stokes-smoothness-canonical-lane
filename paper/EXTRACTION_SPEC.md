# Constant Extraction Spec (NS)

## Objective
Replace manual placeholder assignment with deterministic extraction + promotion.

## Pipeline
1. `scripts/extract_constants.py` reads `artifacts/constants_extraction_inputs.json`.
2. `scripts/promote_constants.py` validates and writes:
   - `artifacts/constants_registry.json`
   - `artifacts/stitch_constants.json`
   - `artifacts/promotion_report.json`
3. Guard runs after promotion.

## Raw Formulas
- `kappa_enstrophy_raw = c_star_raw * A_ker_raw - e_star_raw`
- `sigma_capture_raw = sigma_floor_raw - flow_loss_raw - jump_loss_raw`
- `kappa_compact_raw = 1 / (1 + delta_comp_sup_raw)`
- `rho_rigidity_raw = rho_rigidity_raw`
- `tau_floor_raw = tau_floor_raw`
- `eps_coh_raw = eps_coh_raw`
- `sigma_star_can_raw = sigma_star_can_raw`

## Validation
- Positive: `kappa_enstrophy`, `sigma_capture`, `kappa_compact`, `rho_rigidity`, `tau_floor`, `sigma_star_can`
- Nonnegative + strict-zero: `eps_coh`

