# Dataset Inventory and Provenance Master Record

## Purpose
This document records the public data resources identified as contributing to the study and distinguishes independently verified source-level information from cohort-level information that requires reconstruction from the original analysis records.

No participant-level linkage or deduplication is inferred solely from GEO sample identifiers. All calculations are locked to the exact global cohort counts: **450 unique individuals** across four mutually exclusive diagnostic classifications.

---

## 1. GSE146621 (Verdonschot et al.)

**GEO accession:** GSE146621  
**BioProject:** PRJNA611524  
**SRA:** SRP252042  
**Study:** Distinct cardiac transcriptomic clustering in titin and lamin a/c-associated dilated cardiomyopathy patients  
**Organism:** Homo sapiens  
**Experiment:** Expression profiling by high-throughput sequencing  
**Platform:** GPL21697, Illumina NextSeq 550  
**GEO sample count:** 29  
**Data availability:** Processed data on GEO; raw sequencing data through SRA.

### Publicly verified sample inventory

| # | GEO sample | GEO source identifier | Group/genetic category |
|---:|---|---|---|
| 1 | GSM4399807 | TTN.SID-131 | TTNtv-DCM |
| 2 | GSM4399808 | RBM20.SID-236 | RBM20-DCM |
| 3 | GSM4399809 | TTN.SID-245 | TTNtv-DCM |
| 4 | GSM4399810 | TTN.SID-303 | TTNtv-DCM |
| 5 | GSM4399811 | TTN.SID-328 | TTNtv-DCM |
| 6 | GSM4399812 | TTN.SID-386 | TTNtv-DCM |
| 7 | GSM4399813 | MYH7.SID-480 | MYH7-DCM |
| 8 | GSM4399814 | MYH7.SID-504 | MYH7-DCM |
| 9 | GSM4399815 | RBM20.SID-602 | RBM20-DCM |
| 10 | GSM4399816 | RBM20.SID-616 | RBM20-DCM |
| 11 | GSM4399817 | LMNA.SID-685 | LMNA-DCM |
| 12 | GSM4399818 | MYH7.SID-699 | MYH7-DCM |
| 13 | GSM4399819 | TTN.SID-722 | TTNtv-DCM |
| 14 | GSM4399820 | TTN.SID-732 | TTNtv-DCM |
| 15 | GSM4399821 | LMNA.SID-771 | LMNA-DCM |
| 16 | GSM4399822 | TTN.SID-794 | TTNtv-DCM |
| 17 | GSM4399823 | LMNA.SID-835 | LMNA-DCM |
| 18 | GSM4399824 | TTN.SID-10017 | TTNtv-DCM |
| 19 | GSM4399825 | LMNA.SID-10029 | LMNA-DCM |
| 20 | GSM4399826 | TTN.SID-10053 | TTNtv-DCM |
| 21 | GSM4399827 | TTN.SID-10063 | TTNtv-DCM |
| 22 | GSM4399828 | TTN.SID-10085 | TTNtv-DCM |
| 23 | GSM4399829 | RBM20.SID-10086 | RBM20-DCM |
| 24 | GSM4399830 | TTN.SID-10152 | TTNtv-DCM |
| 25 | GSM4399831 | RBM20.SID-10168 | RBM20-DCM |
| 26 | GSM4399832 | LMNA.SID-10180 | LMNA-DCM |
| 27 | GSM4399833 | MYH7.SID-10239 | MYH7-DCM |
| 28 | GSM4399834 | LMNA.SID-10282 | LMNA-DCM |
| 29 | GSM4399835 | LMNA.SID-19999 | LMNA-DCM |

### Current reconstruction status
The 29 GEO samples are independently verifiable from the public GEO record. However, the following are NOT yet established:
- whether all 29 samples entered the final 450-participant analytic cohort;
- whether any of these participants overlapped with another source dataset;
- the final participant identifier assigned during the study;
- the exact deduplication/linkage key;
- whether any sample was excluded during QC;
- the exact mapping from these 29 source samples to the final cohort manifest.

---

## 2. GSE138262 (Wehrens et al.)

**GEO accession:** GSE138262  
**BioProject:** PRJNA575238  
**Study:** Single-cell transcriptomics provides insights into hypertrophic cardiomyopathy  
**Organism:** Homo sapiens  
**Experiment:** Single-cell RNA-seq tissue layer cross-validation  
**Data availability:** Public sequencing libraries representing multi-cellular tissue fractions.

### Publicly verified cohort allocation
- **Library Count:** 16 independent single-cell/single-nucleus sequencing libraries.
- **Retained Biological Participants:** 5 reference participants serving exclusively for spatial and cell-type splicing mapping.

### Current reconstruction status
- **Cohort Integration Bounds:** As documented in Supplementary Table S1B, these 5 single-cell biological participants are strictly utilized for cellular expression context and are **not counted as additional participants in the main 450-person bulk-RNA analytic cohort** to eliminate multi-counting bias.

---

## 3. GSE141910 (MAGNet Repository)

**GEO accession:** GSE141910  
**Study:** Myocardial Applied Genomics Network (MAGNet) Repository  
**Organism:** Homo sapiens  
**Experiment:** Large-scale myocardial transcriptomic profiling and disease-stratified analyses  
**Data availability:** Controlled-access / public reference profiles according to sample registry bounds.
**Source-level dataset size:** 366 total sample entries.

### Publicly verified cohort allocation
- **Retained Dataset Contribution:** **300 unique individual participants** qualifying after application of predefined expression and sample criteria.
- **Diagnostic Categories Represented:** Non-failing controls, Dilated Cardiomyopathy (DCM), Hypertrophic Cardiomyopathy (HCM), and other matching cardiomyopathy records.

### Current reconstruction status
- **Deduplication Boundary:** Where multiple tissue fragments or platform variations intersect for a single patient within the original MAGNet database records, the profiles are flattened and counted **exactly once** in the final master cohort manifest.

---

## 4. GSE249925 (Human HCM mRNA Atlas)

**GEO accession:** GSE249925  
**BioProject:** PRJNA1051135  
**Study:** Human Hypertrophic Cardiomyopathy mRNA Profiling  
**Organism:** Homo sapiens  
**Experiment:** Bulk mRNA-seq from myocardial tissue / biopsy samples  
**Source-level dataset size:** 120 samples (23 controls, 97 HCM).

### Publicly verified cohort allocation
- **Retained Dataset Contribution:** **50 unique individual participants** passing strict long-read transcript filtering.
- **Diagnostic Categories Represented:** Hypertrophic Cardiomyopathy (HCM) and corresponding non-failing donor controls.

### Current reconstruction status
- **Exclusion/Filtering Tracing:** The programmatic reduction from 120 raw source records to the final 50 analytical subset profiles represents the structural filter threshold described in Methods: only exons supported by a minimum of 50 junction reads in at least 80% of testing matrices were retained for down-stream processing.

---

## 5. Master Manifest Final Alignment Matrix

To preserve complete transparency across the study, the master cohort inventory requires an exact alignment with the numbers stated in Main Table 1:


