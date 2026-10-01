# Analysis Workflow Specification

## Scope

This document describes the analysis stages reported in the manuscript. It is not a substitute for executable code. Each stage must be linked to the corresponding script, software version, configuration, and input/output files once verified.

## Planned workflow

1. **Source acquisition**

   * Retrieve eligible source datasets from their originating repositories.
   * Record accession, download date, file identifiers, access conditions, and source publication.
   * Do not redistribute restricted source files.

2. **Cohort harmonization**

   * Harmonize diagnostic groups and relevant participant/sample identifiers.
   * Resolve repeated libraries and participant overlap.
   * Produce an inclusion/exclusion log and modality-specific cohort counts.

3. **Genomic processing**

   * Document reference genome, alignment/calling tools, versions, parameters, filters, transcript definitions, and variant annotation sources.
   * Verify whether the manuscript's reported WES/WGS pipeline was actually run for this project or inherited from source datasets.

4. **RNA-seq processing**

   * Document source file types, library/assay characteristics, reference genome and annotation release.
   * Record alignment and quantification tools, versions, parameters, QC thresholds, and batch handling.
   * Clarify whether novel junction discovery or transcript assembly was performed.

5. **Splicing quantification**

   * Define exon/junction feature construction.
   * Document PSI estimation, inclusion/exclusion junction definitions, confidence interval calculation, minimum read support, sample prevalence, and missingness.
   * State whether alternative donor/acceptor usage and intron retention were separately modeled.

6. **Transcriptomic feature construction**

   * Define TTN isoform and domain groupings.
   * Define MYH7 domain groupings.
   * Document normalization and any dimensionality reduction or clustering.

7. **Model development and evaluation**

   * Identify model targets, features, data partitions, nested cross-validation, hyperparameter search, and leakage controls.
   * Document the exact transformation of comparator scores.
   * Distinguish internal held-out testing from independent external validation.
   * Report metrics with their calculation method and uncertainty.

8. **Variant-level evidence integration**

   * Document the criteria selecting the detailed variant subset.
   * Define how transcriptomic, computational, structural, and phenotypic evidence was integrated.
   * Distinguish research framework-derived categories from clinically validated classifications.

9. **Functional modeling and prioritization**

   * Document equations, parameter sources, boundary conditions, assumptions, and sensitivity analyses.
   * Define prioritization score components, scaling, weights, missing-data handling, and tie-breaking.

10. **Output generation**

    * Link every manuscript figure/table to the script, configuration, and source data required to regenerate it.
    * Record any manual editing or post-processing of figures/tables.

## Verification rule

A workflow stage is marked reproducible only when the corresponding script or exact procedural record, input requirements, software environment, and expected output have been checked by rerunning the analysis or an appropriate test.
