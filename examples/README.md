# Example Data, Demonstration Inputs, and Testing Governance

## 1. Directory Purpose and Mandate
This directory is strictly reserved for small example inputs, standardized row metrics, and mock parameters used to demonstrate file structures, variable names, expected input/output formats, and bioinformatic script execution paths.

**CRITICAL SAFEGUARD PROTOCOL:** Under no circumstances shall this directory or any sub-branches contain participant-level clinical phenotypes, restricted multi-center registry keys, or raw genomic sequence layers.

---

## 2. Rigid Material Eligibility Criteria
Before any file is added to this demonstration environment, it must meet at least one of the following strict criteria:
1. **Legally Redistributable:** Governed by an open-access public license that permits complete downstream reproduction.
2. **Non-Identifying:** Stripped entirely of all direct and indirect human participant identifiers.
3. **Explicitly Approved:** Formally designated by the originating public repository as a redistributable baseline template.
4. **Explicitly Synthetic:** Cleanly generated from scratch for computational benchmarking and labeled as synthetic across all associated file tracking layers.

---

## 3. Synthetic Data Constraints and Anti-Conflation Rules
To prevent data tracking failures and protect the scientific integrity of the publication:
- **No Scientific Substantiation:** Synthetic parameters serve exclusively as script execution testing markers. They must **never be used to substantiate a manuscript numerical result**, validate an alternative splicing model, or be reported as observed clinical findings.
- **Explicit Filename Mandatory Labeling:** All machine-generated dummy files must include the absolute string prefix `synthetic_` (e.g., `synthetic_hcm_splicing_matrix.tsv`).
- **Required Metadata Headers:** Every placeholder file must contain internal structural headers explicitly identifying its artificial lineage.

---

## 4. Synthetic Verification Schema (Template for Test Data)

All programmatic test arrays committed to this folder must conform to the tracking metadata structure defined below:

```yaml
synthetic_asset_metadata:
  target_filename: synthetic_hcm_splicing_matrix.tsv
  generation_methodology: Deterministic simulation matching cohort mean variances
  parent_validation_script: execute_prioritization_and_scenarios.py
  intended_workflow_demonstration:
    - structural_input_verification
    - row_variable_name_parsing
    - output_dictionary_validation
  manuscript_equivalence_status:
    is_observed_result: FALSE
    reproduces_cohort_totals: FALSE
    audit_safety_classification: [DUMMY-TEST-ASSET-ONLY]
```

