# Comparator Score Transformations and Baseline Integration Audit Record

## 1. Executive Summary & Algorithmic Mandate
This record details the integration, feature parsing, and scoring transformation logic of external sequence-based splice prediction tools used as benchmarks against the core framework. 

All comparative validation metrics conform strictly to the target performance limits locked within `raw_table3_ai_benchmarks.csv` across the **450 unique individual participants** in the analytic cohort.

---

## 2. Benchmark Model Specifications

The external model baselines are restricted to the exact, tool-specific versions and environment channels documented in `SOFTWARE_ENVIRONMENT.md`:

### 2.1 SpliceAI Sequence Predictor Framework
- **Stated Version:** **SpliceAI v1.3.1**
- **Output Matrix Topology:** Provides four discrete categorical delta probability scores (\(0.0 \text{ to } 1.0\)) tracking sequence variant disruptions:
  * Acceptor Gain (AG)
  * Acceptor Loss (AL)
  * Donor Gain (DG)
  * Donor Loss (DL)

### 2.2 MaxEntScan Motif Strength Predictor
- **Stated Version:** **MaxEntScan Bioconda 0_2004.04.21-4**
- **Output Matrix Topology:** Generates continuous sequence-motif scores based on maximum-entropy alignment models evaluating local splice-site boundary strengths.

---

## 3. Critical Reproducibility Gap & Evaluation Tension

### Current Status: ARCHITECTURAL TRANSFORMATION GAPS IDENTIFIED
The primary manuscript compares the baseline outputs of SpliceAI and MaxEntScan against the performance of the cardiac-tuned network on a uniform, continuous prediction scale (reported across Main Table 3 and Figure 3). However, a formal provenance audit has established that **the exact historical transformation functions or scripts used to map these diverse tools into a single common scale are completely unrecovered**.

### Rigid Data Integrity and Reproducibility Rules
To enforce total academic transparency and eliminate the risk of introducing back-formulated or synthetic reporting artifacts:
1. **No Formula Invention:** No transformation equation, normalization script, or scaling formula will be asserted in this repository from memory or custom re-fitting loops.
2. **Forward-Engineered Substitute Baseline:** This workspace provides a dedicated data configuration file—`ai_feature_engineering_spec.yaml`—which catalogs exactly how these comparator raw layers are parsed as input layers, ensuring that future reconstruction tracks cannot mask original pipeline missingness.
3. **Benchmarking Targets:** Any forward-engineered substitute transformation must be programmatically verified against the target baseline performance statistics archived in your validation folders:
   * **SpliceAI *TTN* Classification AUROC:** `0.82` (95% CI: 0.79–0.85)
   * **SpliceAI *MYH7* Classification AUROC:** `0.78` (95% CI: 0.75–0.81)
   * **MaxEntScan *TTN* Classification AUROC:** `0.75` (95% CI: 0.70–0.80)
   * **MaxEntScan *MYH7* Classification AUROC:** `0.72` (95% CI: 0.66–0.78)

---

## 4. Mandatory Audit Checklist for Baseline Integration

To transition this tracking document from **Transformation Gap Status** to **Fully Restored and Verified Status**, the following exact computational engineering definitions must be recovered from historical cluster logs or scratch analysis scripts:

- [ ] **SpliceAI Aggregation Rules:** Documentation of whether the raw tool layer extracted the absolute maximum delta score (\(\max[\text{AG, AL, DG, DL}]\)), specific directional sub-scores, or a custom joint probability mapping.
- [ ] **Directional Sign Assignments:** Code blocks showing whether delta vectors were signed to signify exon-skipping vs. cryptic inclusion.
- [ ] **MaxEntScan Delta Formulation:** Verification of whether the model used raw score differences (\(\text{Score}_{\text{Reference}} - \text{Score}_{\text{Alternate}}\)), relative log-ratios, or fractional shifts.
- [ ] **Normalization and Scaling Suit:** The precise equations mapping continuous max-entropy values (unbounded real numbers) and deep-learning delta values (bounded 0–1 probabilities) into a standardized interval.
- [ ] **Clipping and Thresholding Parameters:** Explicit filter values used to drop low-scoring neutral variants or cap extreme outlier parameters.
- [ ] **Missing-Value Handling Protocols:** Programmatic default behaviors applied when variants fell outside the native context windows or failed splice-site motif lookups.







