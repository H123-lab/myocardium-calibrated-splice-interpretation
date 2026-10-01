# Myocardium-Calibrated Splice Interpretation Framework

This repository accompanies the manuscript:

**A Myocardium-Calibrated Framework for Splice Variant Interpretation Using Cardiac Transcriptomics: Application to TTN and MYH7 in Cardiomyopathy**

## Purpose

This repository provides the data provenance information, dataset accession inventory, analysis workflow documentation, model description, software information, variable definitions, and reproducibility documentation associated with the study.

The study integrates cardiac transcriptomic data, splice-related genomic variation, myocardial splicing features, computational prediction, and multimodal cardiac phenotypes to evaluate a myocardium-calibrated framework for splice-variant interpretation in TTN and MYH7.

## Data availability

The analyses were based on previously generated datasets and publicly available and/or controlled-access resources. No new participants were recruited and no new biological specimens were collected for this study.

Raw participant-level sequencing data are not redistributed in this repository. Where permitted, the repository provides accession identifiers and links to the originating repositories so that users can obtain the source data directly under the applicable access conditions.

Controlled-access data, if applicable, remain subject to the access conditions of the originating repository or study.

## Repository contents

- `docs/` — provenance, workflow, model, software, ethics, and reproducibility documentation.
- `metadata/` — dataset accession inventory, cohort reconciliation records, variable definitions, and figure/table mapping.
- `workflows/` — reconstruction of the analytical workflow based on the methods and surviving study documentation.
- `examples/` — verified non-sensitive or clearly synthetic example data, where available.
- `results/` — documentation of manuscript-derived results and their reproducibility status.
- `reproduction/` — reproduction status, unresolved items, and verification records.

## Important reproducibility statement

Some original analysis scripts, intermediate files, prediction exports, model outputs, and computational logs are no longer available.

Accordingly, this repository distinguishes between:

1. analyses that can be directly reproduced from preserved code and data;
2. analyses that can be reconstructed from documented methods and publicly available source datasets;
3. manuscript results for which original computational outputs are no longer available for independent rerun.

No reconstructed workflow is presented as the original executable analysis unless the corresponding original code or independently verified equivalent implementation is available.

## Source datasets

The current study documentation identifies the following major public resources:

- GSE146621
- GSE138262 / PRJNA575238
- GSE141910
- GSE249925 / PRJNA1051135

Dataset-level details, source sizes, analytic contributions, and access status are documented in `metadata/dataset_inventory.csv`.

## Model and comparator documentation

The manuscript evaluates a myocardium-calibrated splice prediction model against established splice prediction approaches including:

- SpliceAI v1.3.1
- MaxEntScan Bioconda 0_2004.04.21-4

The exact original implementation of the cardiac-tuned model is being documented separately because the original executable model files and training records are no longer available.

## Reproducibility status

This repository should not be interpreted as claiming complete computational reproducibility of every numerical result in the manuscript.

The purpose is to make the study's provenance, analytical decisions, data sources, computational dependencies, and remaining reproducibility limitations transparent.

## Contact

Corresponding author:
Hassa Iftikhar

Wuhan, China

Corresponding email: hassabatool@yahoo.com
