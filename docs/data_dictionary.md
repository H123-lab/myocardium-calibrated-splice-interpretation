# Data Dictionary and Variable Definitions

## Purpose

This document defines the variables used in the manuscript and identifies their units, source, derivation, missing-data handling, and analytical role.

Definitions below are a working specification. A variable should be marked verified only after comparison with the actual analysis dataset and scripts.

| Variable                      | Definition                                                 | Unit/scale                                                    | Source or derivation                                                         | Missing-data handling                                    | Analysis role               | 
| ----------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------- | --------------------------- | 
| Participant identifier        | Study-specific de-identified linkage key                   | Categorical                                                   | Source data / harmonization log                                              | Not applicable                                           | Deduplication and linkage   | 
| Diagnostic group              | Control, DCM, HCM, or other cardiomyopathy                 | Categorical                                                   | Source diagnosis and adjudication record                                     | Exclusion or modality-specific handling to be documented | Stratification/covariate    | 
| PSI                           | Proportion of transcripts including the specified exon     | 0–1; percentage representation must be stated                 | Junction/exon quantification pipeline                                        | Per prespecified QC; document exact rule                 | Splicing measurement        | 
| ΔPSI                          | Disease-group mean PSI minus control-group mean PSI        | Fraction or percentage points; use one consistently per table | Derived from group means                                                     | Document group/sample inclusion                          | Differential splicing       | 
| Junction read support         | Number of reads supporting the relevant splice junction(s) | Read count                                                    | RNA-seq quantification                                                       | QC threshold specified in Methods                        | Feature eligibility/QC      | 
| PSI confidence interval width | Width of the interval around PSI estimate                  | 0–1                                                           | Statistical estimation method                                                | QC threshold specified in Methods                        | Feature eligibility/QC      | 
| TTN N2BA:N2B ratio            | Ratio of defined TTN isoform measures                      | Ratio                                                         | Derived; exact transcript/exon definitions required                          | Document                                                 | Isoform feature             | 
| MYH7 domain PSI score         | Summary of exon-level PSI for a defined domain             | 0–1 or percentage                                             | Domain/exon mapping                                                          | Document                                                 | Domain feature              | 
| SpliceAI score                | Delta score(s) from SpliceAI                               | 0–1                                                           | SpliceAI v1.3.1; exact aggregation rule required                             | Document                                                 | Comparator                  | 
| MaxEntScan score              | Maximum-entropy splice-site score                          | Tool-specific score                                           | MaxEntScan Bioconda 0_2004.04.21-4; exact ref/alt/delta calculation required | Document                                                 | Comparator                  | 
| Cardiac-tuned prediction      | Model output for the prespecified splice endpoint          | Probability and/or continuous effect; specify                 | Trained model                                                                | Document                                                 | Main predictor              | 
| 6MWT                          | Six-minute walk test distance                              | m                                                             | Source dataset(s); source-specific provenance required                       | Not imputed unless explicitly documented                 | Secondary phenotype if used | 
| Grip strength                 | Grip strength measurement                                  | kg                                                            | Source dataset(s); source-specific provenance required                       | Not imputed unless explicitly documented                 | Secondary phenotype if used | 

## Unit conventions

The manuscript must consistently distinguish:

* PSI as a fraction (0–1) versus percentage (0–100%).
* ΔPSI as a fraction versus percentage points (pp).
* Participant counts versus sample/library counts.
* Missing measurements versus measurements not collected.
* Not applicable values versus values failing quality control.

## Missingness

No missing-value handling procedure should be claimed unless it is confirmed from the analysis scripts or documented analysis records. Modality-specific denominators should be reported where available.

