# Verified Analytical Results and Reproducible Outputs Directory

## 1. Directory Mandate
This directory is strictly reserved for verified, reproducible outputs, finalized summary statistics, and publication-ready tabular or graphical assets generated directly by the validated analysis scripts. 

**CRITICAL COMPLIANCE DIRECTIVE:** This directory must contain only genuine, script-derived results that have been programmatically checked against the 450-participant analytic cohort. Under no circumstances shall illustrative, placeholder, or unverified simulation files be placed here as though they were definitive study results.

---

## 2. Rigorous Traceability & Documentation Mandates
To satisfy peer-review standards for extreme computational transparency, every analytical asset committed to this directory must be entirely traceable through a structured data lineage:

1. **Input Traceability:** Each output must map back to an explicit, non-identifying source dataset or a summary feature matrix documented in `processed_data/`.
2. **Algorithmic Lineage:** The specific generating file (e.g., `2.10_phenotype_regression.R` or `generate_supplementary_plots.py`) and its exact version state must be explicitly linked.
3. **Manual Post-Processing Logging:** If an image or table requires manual edits or cosmetic adjustments (such as panel merging, typography resizing, or resolution scaling in vector software), a corresponding `.txt` log file must be placed alongside the asset detailing every post-processing step.

---

## 3. Data Privacy and Safe Harbor Compliance
In strict compliance with international human genomic privacy regulations (such as HIPAA and GDPR) and the data-use agreements of our contributing registries (MAGNet, GSE146621, GSE249925):
- No participant-level raw metrics, unblinded clinical cross-walk tables, or individual patient tracking matrices may be deposited in this public folder.
- All results files must be maintained at the aggregate, cluster, cohort, or variant-level summary tier.

---

## 4. Reproducible Asset Traceability Schema

All completed outputs deposited in this folder must conform to the tracking metadata architecture defined below:

```yaml
result_asset_provenance:
  target_filename: main_table_5_multivariable_regression.csv
  associated_manuscript_locus: Main Table 5 / Supplementary Table S7
  generating_script_reference: 2.10_phenotype_regression.R
  underlying_interpreters: R (v4.x) / survival library suite
  reproducibility_inputs:
    - raw_table2_splicing_atlas.tsv
    - raw_variant_evidence_registry.tsv
  output_typology: OBSERVED_SUMMARY_STATISTICS
  cohort_denominator_lock: Exactly 450 unique individual participants
  post_processing_applied: FALSE
```

