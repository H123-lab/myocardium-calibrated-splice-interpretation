# Final Cohort Composition and Provenance Validation Record

## 1. Executive Summary & Diagnostic Group Distribution
This record documents the definitive analytical cohort footprint utilized throughout the study. All downstream parameter metrics, clinical phenotype regressions, and machine learning evaluations are locked to this master baseline with zero variance.

The mutually exclusive cohort distribution matches Main Table 1 and Results text with 100% precision:

| Diagnostic Subgroup Domain | Unique Participant Count (\(n\)) | Allocation Footprint Percentage |
| :--- | :---: | :---: |
| **Non-failing Controls** | 80 | 17.78% |
| **Dilated Cardiomyopathy (DCM)** | 160 | 35.56% |
| **Hypertrophic Cardiomyopathy (HCM)** | 120 | 26.67% |
| **Other Cardiomyopathies** | 90 | 20.00% |
| **Global Integrated Cohort Denominator** | **450** | **100.00%** |

---

## 2. Mathematical Reconciliation Matrix

The global dataset configuration enforces a strict, mutually exclusive patient allocation check:

\[\text{Total Sample Cohort} = \text{Controls} (80) + \text{DCM} (160) + \text{HCM} (120) + \text{Other CM} (90) = 450\]

- **Manuscript Statement:** The published draft reports an analytic footprint of exactly 450 unique individuals distributed identically across these diagnostic buckets.
- **Verification Audit Result:** The cohort sums balance precisely across all primary statistical tests, multivariable clinical regressions (`2.10_phenotype_regression.R`), and feature extraction models.

---

## 3. Important Provenance & Linkage Limitations

### Current Verification Status: PENDING EXPLICIT LINKAGE RECOVERY
While the aggregate totals match the analytical indices of the main text, the **individual-level source-to-final tracking matrix** has not been independently reconstructed. 

- **Source-to-Participant Mapping:** The original computational cross-walk file mapping raw repository source keys (e.g., dbGaP, SRA, and EGA accession files) directly to the anonymized 450-person cohort map is unrecovered from the surviving analysis logs.
- **Traceability Constraint:** This repository does not claim that every individual participant can presently be traced from the final cohort back to a specific accession/sample identifier. Source-level accession metadata are documented independently in `01_dataset_inventory.csv` and `accession_inventory.csv`.
- **No Speculative Reconstruction:** Under no circumstances should individual participant keys, private clinical markers, or local database serial rows be inferred or generated using aggregate numbers or public sample metadata.

---

## 4. Decoupling of Single-Cell Validation Resources

To prevent dataset inflation and mathematical weighting bias within the primary short-read bulk RNA-seq processing pipelines, strict boundaries are enforced for external single-cell reference libraries:

* **Target Resource:** **GSE138262 / PRJNA575238** (Wehrens et al. / Human HCM Septal Myectomy).
* **Inventory Scale:** Contains **16 independent sequencing libraries** representing **5 distinct biological participants**.
* **Functional Integration Role:** This resource serves exclusively as an orthogonal cell-type expression context marker. In accordance with the study metrics, these 5 reference individuals are **strictly uncounted in the bulk 450-person cohort denominator**.

---

## 5. Required Criteria for Complete Replication Tracing

To transition this tracking document from **Partial Status** to **Fully Reconstructed Status** upon recovery of the original administrative files, the verified participant manifest must conform to the following explicit tracking schema:

```tsv
source_dataset	source_sample_id	participant_id_or_source_identifier	diagnosis	tissue	modality	included	exclusion_reason	duplicate_status	final_cohort_group
```

*Operational Security Reminder: In strict adherence to genomic safe-harbor guidelines and IRB human data restrictions, raw patient cross-walk tracking tables must remain contained inside protected offline processing zones and must never be pushed to public open-access code repositories.*



