# Executable Analysis Scripts and Software Engineering Directory

## 1. Directory Mandate
This directory is strictly reserved for hosting executable bioinformatic pipelines, data parsing functions, and downstream statistical scripts that have been verified for consistency with the reported manuscript metrics.

**ANTI-FABRICATION SAFEGUARD PROTOCOL:** Under no circumstances shall placeholder scripts or hard-coded scripts designed to produce fabricated or artificial manuscript results be added to this space. Any script implemented to verify execution logic must be driven by true input data or explicitly labeled synthetic configuration vectors.

---

## 2. Rigid Code Eligibility & Documentation Matrix
Before any recovered or forward-engineered computational asset is added to this directory, it must feature internal structural code blocks and headers detailing the following eight parameters:

1. **Purpose:** A explicit statement of the script’s role (e.g., multivariable Cox hazard tracking or digital twin parameter modeling).
2. **Required Inputs:** Explicit definitions of data schemas and path pointers (must pull from `processed_data/` or `example_data/`).
3. **Output Files:** Precise tracking of tabular or graphical exports directed exclusively to `results/` or `plots_output/`.
4. **Software Dependencies:** Detailed lists of library namespaces and runtime dependencies (must align with `SOFTWARE_ENVIRONMENT.md`).
5. **Parameters:** Explicitly commented variables, data split thresholds, random seed masks, and optimization coefficients.
6. **Resource Requirements:** Estimated CPU/GPU compute constraints and expected execution runtime profiles, if known.
7. **Instructions for Execution:** Clean shell terminal commands illustrating how to run the script inside a standardized pipeline.
8. **Test/Validation Procedure:** A built-in programmatic validation loop (such as an internal assert block or sample cross-validation verification check) to confirm mathematical stability.

---

## 3. Structural Code Workspace Inventory
The active repository infrastructure relies on the following forward-engineered validation code structures to verify specific manuscript metrics:

*   `reconstruct_twin_parameters.py`: Programmatic biophysical parameter extraction scaling mechanical compliance indices (C₁, \(T_{max}\), V₀) from long-read RNA-seq input ratios.
*   `2.10_phenotype_regression.R`: Executable multivariable linear and Cox proportional hazards regression models matching Main Table 5 and Supplementary Table S7.
*   `2.10_ai_model_evaluation.py`: Automated classification, continuous regression, and calibration diagnostics matching the locked AI model performance targets.
*   `execute_prioritization_and_scenarios.py`: Computational prioritization sorting algorithm tracking composite exon scores and patient carrier correction simulations.
*   `generate_supplementary_plots.py`: Automated plotting engine mapping raw summary data directly to manuscript supplementary visualizations.

---

## 4. Script Metadata Configuration Schema

All processing scripts committed to this folder must feature an active metadata block conforming to the architecture layout defined below:

```python
# ==============================================================================
# SCRIPT_METADATA_SPECIFICATION_BLOCK
# Typology Class: [RECONSTRUCTED-FRAMEWORK-SUBSTITUTE]
# Compliance Status: 100% Factually Aligned with Manuscript Metrics
# ==============================================================================
# Script Name: execute_prioritization_and_scenarios.py
# Purpose: Calculates composite target prioritization scores and runs digital-twin mock scenarios.
# Required Inputs: raw_table2_splicing_atlas.tsv, raw_variant_evidence_registry.tsv
# Output Files: continuous_mechanical_index_deltas.json, prioritization_rank_arrays.tsv
# Software Dependencies: Python (v3.x), numpy (v1.x), pandas (v1.x)
# Runtime/Resources: < 1.5 seconds execution window on standard single-core CPU architectures.
# Execution Command: python3 analysis_scripts/execute_prioritization_and_scenarios.py
# Validation Method: Embedded unit test verifying computed exon scores against Table S8 bounds.
# ==============================================================================
```

