# Data Provenance

## Overview

The study used previously generated cardiac transcriptomic, genomic, imaging, clinical, and related multimodal datasets.

No new participants were recruited and no new biological specimens were collected for the present study.

The principal public transcriptomic resources identified during preparation of the manuscript were:

| Resource | Accession | Primary role |
|---|---|---|
| Verdonschot et al. | GSE146621 | LV cardiac RNA-seq / DCM transcriptomic analysis |
| Wehrens et al. | GSE138262 / PRJNA575238 | HCM single-cell cardiac transcriptomic reference |
| MAGNet | GSE141910 | LV myocardial transcriptomic reference |
| Human HCM mRNA Profiling | GSE249925 / PRJNA1051135 | HCM and control cardiac mRNA profiling |

## Verified public-resource information

### GSE146621

GSE146621 is a public human cardiac RNA-seq dataset describing distinct cardiac transcriptomic clustering in TTN- and LMNA-associated dilated cardiomyopathy.

The GEO record reports 29 samples.

Raw sequencing data are available through the associated SRA records, with processed data available through the GEO series.

### GSE138262 / PRJNA575238

GSE138262 is a single-cell transcriptomic resource generated from human hypertrophic cardiomyopathy myectomy tissue.

The GEO record describes five septal myectomy samples from HCM patients.

This resource is treated as a single-cell reference/validation resource and must not be counted as five additional participants in the bulk-RNA cohort unless the corresponding participant-level data were independently incorporated into the bulk analytic cohort.

### GSE141910

GSE141910 is the MAGNet left-ventricular transcriptomic resource containing non-failing donor and heart-failure samples.

The GEO record reports 366 samples and identifies RNA-seq data from left ventricular tissue.

The resource includes non-failing controls and cardiomyopathy groups including DCM, HCM and PPCM.

### GSE249925 / PRJNA1051135

GSE249925 / PRJNA1051135 contains cardiac biopsy mRNA profiles from 23 controls and 97 HCM cases, corresponding to 120 samples.

Raw data are available through SRA and processed count data are available through GEO.

## Source-level versus analytic-cohort counts

Source-level dataset size must not be interpreted as the number of unique participants contributing to the final analytic cohort.

A source may contain:

- multiple sequencing libraries from one participant;
- samples excluded by quality-control criteria;
- participants outside the study's predefined diagnostic groups;
- modality-specific data;
- overlapping participants represented in another dataset.

The final participant-level cohort therefore requires an explicit inclusion and deduplication manifest.

## Provenance status

The following information has been independently verified from public repository records:

- accession identifiers;
- broad dataset descriptions;
- public availability;
- reported source-level sample counts.

The exact mapping from every source sample to the final 450-participant analytic cohort is not currently reconstructed from a surviving participant-level inclusion/linkage file.

Therefore, the final participant-level reconciliation remains an unresolved reproducibility item and is documented separately in `COHORT_RECONCILIATION.md`.

## Raw-data handling

The author previously accessed raw sequencing files including FASTQ/BAM files for portions of the analysis. The original local copies are no longer retained.

Raw sequencing files are not redistributed through this repository.

Users wishing to reproduce the source-data processing should obtain the data directly from the relevant public repository or through the applicable controlled-access mechanism.
