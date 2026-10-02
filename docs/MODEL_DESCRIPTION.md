# Cardiac-Tuned Splicing Model Architecture and Audit Record

## 1. Algorithmic Mandate & Diagnostic Boundaries
The model was engineered within the myocardium-calibrated splice interpretation framework to predict variant-level splice-disruption probabilities and continuous exon-level percent spliced-in changes (\(\Delta\text{PSI}\)) across *TTN* and *MYH7*. 

**Critical Diagnostic Boundary:** The model evaluates downstream molecular splicing disruption and sequence pathogenicity gradients. It is **not designed to predict clinical HCM or DCM patient diagnoses directly**.

---

## 2. Integrated Feature Spaces & Prediction Targets

The input arrays span multiple biological and sequence layers to capture cardiac-specific context, as mapped out in `ai_feature_engineering_spec.yaml`:
- **Sequence Context Matrix:** Local genomic sequence windows (\(\pm\) 50bp flanking exon/intron boundaries).
- **Cis-Regulatory Elements:** Enriched motif densities (including canonical donor GT, ESE motifs, and *RBM20* binding sites).
- **Exon Topology Map:** Exon lengths, identity features, and evolutionary conservation metrics.
- **Biomechanical Domain Overlay:** Functional structural domain annotations (Z-disc, I-band, PEVK, A-band, and M-line for titin; motor-head, lever-arm, and rod regions for *MYH7*).
- **Myocardial Transcriptomic Features:** Population-level disease-stratified baseline splicing features and cohort \(\Delta\text{PSI}\) summaries.

### Evaluated Model Target Endpoints
1. **Classification Task:** Probabilistic determination of pathogenic vs. benign splice-site variants.
2. **Regression Task:** Quantitative predictive tracking of continuous exon-level \(\Delta\text{PSI}\) variations.

---

## 3. Methodological Reconciliation & Replication Tension

### Current Status: ARCHITECTURAL DISCREPANCY IDENITIFIED
A formal provenance audit has identified a distinct discrepancy between the legacy code paths recalled by the authorship team and the formal descriptions compiled in the final manuscript draft:
- **Author Laboratory Recollection:** Initial code paths are recalled as utilizing a classic **Random Forest Machine Learning framework** incorporating extracted structural DNA properties and localized tissue gene-expression weights.
- **Manuscript Text Layer:** The manuscript text describes a complex, multi-layered **Deep Learning Architecture** utilizing **sequence attention networks and domain-aware embeddings** (Convolutional blocks fused to sequential dependency layers).

### Operational Reproducibility Safeguard Rules
To maintain absolute scientific transparency and prevent post-submission data tracking failures:
1. **No Back-Formulated Substitutes:** No new code assembly will be labeled as the *original historical implementation* unless it programmatically matches the original file checksums or perfectly replicates the published internal weights.
2. **Forward-Engineered Substitute Labeling:** Code blocks designed to substitute for missing segments must be marked with the explicit repository tag: `[RECONSTRUCTED-FRAMEWORK-SUBSTITUTE]`.
3. **Validation Anchoring:** Any future framework reconstruction must match the exact benchmarking statistics locked inside `2.10_ai_model_evaluation.py` (e.g., Held-out *TTN* AUROC = **0.94**, *MYH7* AUROC = **0.92**, and Calibration Slopes near **1.0**).

---

## 4. Mandatory Audit Checklist for Model Reconstruction

To transition this tracking log from **Unresolved/Discrepancy Status** to **Fully Preserved Code Status**, the following structural training records must be physically recovered from the original deep learning compute server or scratch storage folders:

- [ ] **Algorithm Baseline Blueprint:** Final operational file configurations distinguishing the attention embedding layout from the random forest fallback matrix.
- [ ] **Exact Feature Matrix:** The complete, uncompressed training dataset array linking the genomic coordinates to all engineered splicing features.
- [ ] **Target Training Labels:** Ground-truth classification and regression metrics mapped to individual variant rows.
- [ ] **Dataset Partitioning Seed:** The random seed and cross-validation index mapping individual variants to the 5-fold folds without data leakage.
- [ ] **Hyperparameter Configuration:** The exact learning rate schedules, dropout weights, tree counts, depth limits, and optimization weights applied.
- [ ] **Class Balancing & Calibration:** Preprocessing pipelines (such as SMOTE or class-weight adjustment) and Platt scaling or isotonic regression functions used for probability calibration.
- [ ] **Metric Suite Source Code:** The Python/R script lines used to compute the area under the receiver operating characteristic curve (AUROC), precision-recall curve (AUPRC), and root mean squared error (RMSE) values reported in the primary tables.

---

## 5. Performance Targets Verification Array
Any future model iteration must validate against the locked, peer-reviewed evaluation metrics managed inside the `2.10_ai_model_evaluation.py` tracking script:

[Verification Bounds] 
──► TTN Variant Classification AUROC : 0.94 (0.92 - 0.96)
──► MYH7 Variant Classification AUROC: 0.92 (0.90 - 0.94)
──► TTN Exon Splicing RMSE           : 0.045
──► MYH7 Exon Splicing RMSE          : 0.052





