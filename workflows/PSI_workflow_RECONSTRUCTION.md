# Percent Spliced-In (PSI) Processing Workflow Tracking and Trace Record

## 1. Executive Summary & Audit Baseline
This document details the programmatic pipeline architecture, filter gates, and data transformations described across the manuscript to quantify alternative splicing metrics in human left-ventricular myocardium tissue.

**Operational Boundary Announcement:** This is a **RECONSTRUCTION MANIFEST ONLY**. The original historical executable PSI-quantification script is classified as **UNRECOVERED**. To protect computational integrity, newly forward-engineered pipelines designed to evaluate script interfaces must be labeled with the explicit repository tag: `[RECONSTRUCTED-FRAMEWORK-PIPELINE]`.

---

## 2. Theoretical Ingest Features & Processing Flow

The reference bioinformatic pipeline transforms raw molecular signals into the continuous structural values archived inside `raw_table2_splicing_atlas.tsv` using a nine-step sequence:
1. **Splice-Aware Mapping:** Raw short-read libraries are aligned to the GRCh38 (hg38) reference genome using **STAR v2.7.x**.
2. **Junction Quantification:** Exon-exon splice-junction coordinates and read counts are extracted from alignment arrays.
3. **Exon-Level PSI Scoring:** Fractional ratio metrics are computed: \(\text{PSI} = \frac{\text{Inclusion Reads}}{\text{Inclusion Reads} + \text{Exclusion Reads}}\).
4. **Eligibility Filtering:** Structural validation metrics are evaluated against strict read-depth and variance boundaries.
5. **Disease-Stratified Contrast:** Group-level variations (\(\Delta\text{PSI} = \text{PSI}_{\text{Disease Mean}} - \text{PSI}_{\text{Control Mean}}\)) are computed relative to non-failing controls.
6. **Domain-Level Aggregation:** Splicing variables are compiled into functional biomechanical overlays (Z-disc, I-band, PEVK, and M-line matrices).
7. **Isoform Ratio Extraction:** The core *TTN* N2BA:N2B compliant-to-stiff transcript ratio is calculated.
8. **Sample-Level QC Auditing:** Individual library metadata tracks are evaluated for mapping rate and technical batch preservation.
9. **Phenotypic Association:** final summary features are forwarded to multivariable linear and Cox proportional hazards regression engines.

---

## 3. Stated Quality Control Ingest Filters

To ensure robust estimation and filter out background transcription artifacts, individual alternative splicing events are subjected to strict mathematical filtering criteria managed in `variable_dictionary.csv`:

| Quality Gate Dimension | Mandatory Threshold Boundary | Technical Operational Role |
| :--- | :---: | :--- |
| **Minimum Junction Support** | ≥ 50 continuous reads | Eliminates false-positive variant calls in low-coverage space. |
| **Cohort Sample Support** | Present in ≥ 80% of samples | Enforces feature consistency across the entire analytic population. |
| **Maximum 95% CI Width** | ≤ 0.25 interval half-width | Filters out highly volatile, unstable transcript estimations. |

---

## 4. Methodological Scope, Boundaries, and Exclusions

To prevent computational drift during future reproduction efforts, the alternative splicing analytical scope is anchored to three rigid constraints:
*   **Targeted Annotation Dependency:** The pipeline parses pre-annotated exon and splice-junction features matching canonical reference definitions (GENCODE v38 / Ensembl 104). It **must not be described as unrestricted de novo transcript discovery** unless an original assembly script is recovered.
*   **Alternative Splicing Classes:** The workflow maps exon inclusion/skipping (SE) and distinct alternative 5′/3′ splice-site variations represented inside the quantified junction feature space. 
*   **Intron Retention Exclusion:** Intron retention (RI) was **not established as an independently modeled prediction target** or structural parameter input for downstream tissue models.

---

## 5. Computational Trace Gaps & Replication Status

The historical files and intermediate logs listed below are currently missing from the surviving analytical environment:
- The original primary execution script calculating localized index ratios.
- The command-line string parameter flags deployed for the STAR mapping runs.
- The exact sub-minor GENCODE/Ensembl GTF annotation release file.
- The un-imputed intermediate sample-by-exon raw junction count files.
- The individual-level patient-by-exon master PSI matrix.

### Status: NOT INDEPENDENTLY REPRODUCED
The aggregate cohort-level continuous statistics match the reported tables with 100% precision. However, because individual-level cross-walk manifests are pending recovery, complete independent reproduction directly from the raw sequence tracks remains **NOT YET ESTABLISHED**.


