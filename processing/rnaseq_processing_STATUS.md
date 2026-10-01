# RNA-seq Processing Status

## Manuscript-described workflow

The manuscript describes processing of bulk left-ventricular RNA-seq data with:

- alignment to GRCh38;
- STAR-based RNA-seq alignment;
- exon/junction quantification;
- exon-level PSI estimation;
- disease-stratified comparison with controls;
- splice-junction quality control;
- batch-effect assessment/correction.

The manuscript reports the following PSI-related criteria:

- minimum junction read threshold: 50 reads;
- retained in at least 80% of samples;
- PSI confidence interval width <= 0.25.

## Historical implementation status

The original executable RNA-seq processing scripts and exact configuration files are not currently available.

The manuscript indicates use of STAR, R, Python, and related analysis tools, but exact historical software versions and command-line parameters have not been recovered.

## Important restriction

A new STAR script must not be described as the historical script used to generate the manuscript results unless the original implementation can be recovered or the new implementation independently reproduces and is explicitly labelled as a reconstruction.

