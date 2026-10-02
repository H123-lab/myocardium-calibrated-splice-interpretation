# Cohort Manifest and Replication Verification Status

## 1. Executive Summary Table

| Metric | Specification Matrix |
| :--- | :--- |
| **Target Framework** | Left-Ventricular Myocardium Splicing Interpretation Framework |
| **Final Analytic Cohort** | 450 Unique Individual Participants |
| **Aggregate Distribution** | 80 Controls \| 160 DCM \| 120 HCM \| 90 Other Cardiomyopathies |
| **Observed Output Match** | Complete alignment with Main Table 1 and Results text |
| **Current Provenance Status** | **PARTIAL** — Aggregate group metrics match; patient-level linkage map pending recovery |

---

## 2. Mathematical Alignment Matrix

The global dataset configuration enforces a strict, mutually exclusive patient allocation check:

$$\text{Total Sample Cohort} = \text{Controls} (80) + \text{DCM} (160) + \text{HCM} (120) + \text{Other CM} (90) = 450$$

- **Manuscript Statement:** The published draft reports an analytic footprint of exactly 450 unique individuals distributed identically across these diagnostic buckets.
- **Verification Audit Result:** The cohort sums balance precisely across all primary statistical tests and feature extraction models.

---

## 3. Replication Status & Methodological Caveats

### Status: PARTIAL RECONSTRUCTION
While the aggregate totals match the analytical indices of the main text, the **individual-level source-to-final tracking matrix** has not been independently reconstructed. 

### Data Governance Guidelines
1. **No Speculative Reconstruction:** Under no circumstances should individual participant keys, localized database serial integers, or source linkage rows be filled in from memory or generated using synthetic configurations.
2. **True Provenance Compliance:** Full independent reconstruction requires the physical recovery of the original master configuration tables mapping raw repository source keys (e.g., dbGaP, SRA, and EGA accession files) directly to the anonymized 450-person cohort map.
3. **Data Protection Bounds:** In compliance with genomic safe-harbor guidelines, all participant-level tracking data must remain within local access environments and must not be committed to this open-access branch.

---

## 4. Current Work Action Items

To transition this tracking document from **PARTIAL** to **VERIFIED** verification status, the pipeline execution profile must be updated with:
- [ ] Recovered explicit file manifests mapping the exact 29 samples from GSE146621 into the DCM bucket.
- [ ] Explicit QC filtration tables tracing the exact library drop patterns for the 50 selected high-depth tracks from GSE249925.
- [ ] Verified deduplication hash identifiers confirming individual participant exclusions across the primary MAGNet (GSE141910) inputs.
