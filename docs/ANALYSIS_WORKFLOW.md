# Analysis Workflow

## Status

This document reconstructs the analytical workflow from the manuscript, surviving study documentation, and author recollection.

It is not a claim that the original executable scripts are currently preserved.

## 1. Dataset acquisition

Public cardiac transcriptomic resources were identified using their repository accession identifiers.

The author reports that raw sequencing files, including FASTQ/BAM files, were accessed for portions of the analysis.

Original local raw-data copies are no longer retained.

## 2. RNA-seq processing

The manuscript describes:

- alignment to GRCh38 for the primary harmonized analysis;
- splice-aware alignment using STAR;
- exon-level and junction-level quantification;
- quality control based on sequencing depth and mapping rate;
- TTN/MYH7 junction coverage assessment;
- exon-level PSI calculation;
- disease-stratified ΔPSI estimation;
- batch-effect assessment/correction.

The manuscript reports a minimum sequencing depth of approximately 70 million paired-end reads and a mapping-rate threshold of approximately 90%.

Exact historical command-line parameters and configuration files are not currently available.

## 3. PSI calculation

PSI was used as the primary exon-level splicing measurement.

The manuscript defines PSI as exon inclusion relative to the relevant splice-junction configuration.

The reported eligibility criteria were:

- at least 50 supporting junction reads;
- support in at least 80% of samples;
- PSI confidence-interval width no greater than 0.25.

The original executable PSI calculation script is not currently available.

## 4. Long-read analysis

Oxford Nanopore Technologies sequencing was used for orthogonal assessment of selected transcript structures.

The manuscript describes comparison with a predefined cardiac reference transcript panel.

Long-read detection was not used as an inclusion criterion for the primary short-read PSI matrix.

## 5. Variant analysis

TTN and MYH7 variants were annotated using transcript, genomic coordinate, variant type, population frequency, domain, and prior clinical classification.

The manuscript describes ACMG/AMP-aligned interpretation incorporating transcriptomic and computational evidence.

The original annotation script and exact historical reference-version files are not currently available.

## 6. Splice prediction

The manuscript identifies the following comparator tools:

- SpliceAI v1.3.1
- MaxEntScan Bioconda 0_2004.04.21-4

The original comparator-score transformation code is not currently available and therefore must not be reconstructed from memory and presented as the historical implementation.

## 7. Cardiac-tuned model

The author currently recalls that the cardiac-tuned model involved machine-learning analysis incorporating structural sequence features and myocardial gene-expression/splicing information.

However, the manuscript currently describes the model using deep-learning terminology and an architecture involving sequence attention/domain-aware embeddings.

These descriptions are not equivalent.

Therefore, the exact historical model architecture remains unresolved.

No new model implementation should be presented as the original model until this discrepancy is resolved.

## 8. Validation

The manuscript reports:

- five-fold cross-validation;
- held-out evaluation;
- calibration assessment;
- AUROC;
- PR-AUC;
- RMSE;
- Brier score;
- calibration slope.

The manuscript previously used the term "external validation" for some analyses.

This terminology has been revised where appropriate to distinguish held-out/internal evaluation from genuinely independent external validation.

## 9. Multimodal association analyses

The manuscript describes regression and survival analyses linking splicing-derived features with cardiac structure, function, and clinical outcomes.

The original analysis scripts and model objects are not currently retained.

## 10. Functional/digital-twin analysis

The manuscript describes reduced-order digital-twin simulations linking splicing-derived indices with ventricular mechanical behavior.

The original simulation files are not currently available.

## 11. Therapeutic prioritization

The manuscript describes a composite splice-modulation prioritization score incorporating splicing impact, structural relevance, disease association, and predicted feasibility.

The exact historical scoring implementation must be recovered or documented from surviving supplementary material before executable reproduction is claimed.

## Reproducibility classification

RNA-seq workflow: documented but original scripts unavailable.

PSI workflow: documented but original executable script unavailable.

Variant annotation: documented at methodological level; exact historical implementation unavailable.

Comparator prediction: tools identified; exact score transformation implementation requires recovery/verification.

Cardiac-tuned model: historical implementation requires clarification.

Multimodal statistics: reported results available in manuscript/supplementary materials; original scripts unavailable.

Digital twin: methodological description available; original simulation files unavailable.
