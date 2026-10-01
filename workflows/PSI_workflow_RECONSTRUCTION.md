# PSI Workflow — Reconstruction Documentation

## Status

RECONSTRUCTION DOCUMENTATION ONLY.

The original executable PSI-analysis script is not currently available.

## Inputs

Expected source inputs:

- RNA-seq FASTQ/BAM files;
- genome reference;
- transcript/exon annotation;
- sample metadata;
- diagnostic group labels.

## Processing described in manuscript

1. Align RNA-seq reads using a splice-aware aligner.
2. Quantify exon and splice-junction usage.
3. Calculate exon-level PSI.
4. Apply read-support and confidence criteria.
5. Calculate disease-group versus control ΔPSI.
6. Generate TTN/MYH7 domain-level summaries.
7. Derive N2BA:N2B-related metrics where applicable.
8. Preserve sample-level QC information.
9. Perform disease-stratified analyses.

## Reported PSI eligibility criteria

- ≥50 supporting junction reads;
- ≥80% sample support;
- PSI confidence-interval width ≤0.25.

## Important scope

The primary analysis was based on annotated exon/junction features.

It should not be described as unrestricted de novo transcript discovery unless the original pipeline confirms that such discovery was performed.

## Alternative splicing classes

The manuscript currently supports primarily exon-level inclusion/skipping and junction-based measurements.

Alternative 5′/3′ splice-site usage can only be claimed where represented in the quantified junction features.

Intron retention was not established as an independently modelled prediction target.

## Missing historical artifacts

- original PSI script;
- original STAR command line;
- exact annotation release;
- exact intermediate count files;
- original sample-level PSI matrix.

## Reproduction status

NOT INDEPENDENTLY REPRODUCED FROM ORIGINAL CODE.
