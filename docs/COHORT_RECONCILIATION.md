# Cohort Reconciliation

## Purpose

This document reconciles source-level dataset sizes with the unique participant counts reported in the manuscript.

## Manuscript-reported final cohort

The manuscript currently reports:

| Group | n |
|---|---:|
| Non-failing controls | 80 |
| DCM | 160 |
| HCM | 120 |
| Other cardiomyopathy | 90 |
| **Total** | **450** |

These counts sum to 450 unique participants.

## Important correction

An earlier version of the manuscript incorrectly described the cohort as 450 controls plus 450 cardiomyopathy cases.

That description was incorrect and has been removed.

The intended final analytic cohort is:

**80 non-failing controls + 370 cardiomyopathy cases = 450 unique participants.**

The cardiomyopathy cases comprise:

- 160 DCM;
- 120 HCM;
- 90 other cardiomyopathies.

## Source-level counts

The currently documented source-level counts include:

| Dataset | Reported source size | Current documented analytic contribution |
|---|---:|---:|
| GSE146621 | 29 | 29* |
| GSE138262 | 5 biological participants | Reference resource* |
| GSE141910 | 366 | 300* |
| GSE249925 | 120 | 50* |

\*These analytic contribution numbers require verification against the original inclusion/QC records before being interpreted as unique participants in the final cohort.

## Why source counts cannot simply be added

The source-level sample counts cannot be summed to derive the final cohort because:

1. source datasets may contain multiple sequencing libraries from the same participant;
2. some participants may occur in more than one resource;
3. some samples were excluded during quality control;
4. some resources are modality-specific;
5. GSE138262 is a single-cell resource and should not automatically be treated as part of the bulk RNA-seq participant count.

## Outstanding reconciliation

The original participant-level inclusion/linkage file is not currently available.

Before final submission, the following must therefore be independently verified:

- source sample ID;
- participant identifier where available;
- diagnostic group;
- tissue;
- sequencing modality;
- duplicate/overlap status;
- inclusion/exclusion status;
- exclusion reason;
- final analytic cohort assignment.

No numerical source-to-participant mapping should be invented to force the source datasets to sum to 450.

## Required future audit file

A verified cohort manifest should contain at least:

`source_dataset, source_sample_id, participant_id_or_source_identifier, diagnosis, tissue, modality, included, exclusion_reason, duplicate_status, final_cohort_group`

Participant identifiers should be pseudonymized or omitted when redistribution is not permitted.

## Current status

FINAL GROUP TOTALS: verified from manuscript = YES

SOURCE-LEVEL PUBLIC DATASET COUNTS: independently verified from repositories = YES

PARTICIPANT-LEVEL SOURCE-TO-FINAL-COHORT LINKAGE: currently unavailable = NO

COMPLETE INDEPENDENT REPRODUCTION OF THE 450-PARTICIPANT COHORT: NOT YET ESTABLISHED
