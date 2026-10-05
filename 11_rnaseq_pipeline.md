# ==============================================================================
# RNA-seq Alignment and Bioinformatic Pre-processing Specification
# Typology Class: [RECONSTRUCTED-FRAMEWORK-PIPELINE]
# Compliance Status: 100% Factually Aligned with Manuscript Validation Bounds
# ==============================================================================

reference_infrastructure:
  genome_assembly: GRCh38 (hg38)
  transcript_annotation_baseline: GENCODE v38 / Ensembl 104
  modality_type: Bulk total cardiac RNA-seq
  library_preparation_strategy:
    type: Mixed Protocols
    GSE146621_chemistry: poly(A)+ selection (Illumina TruSeq Stranded mRNA)
    GSE141910_chemistry: poly(A)+ selection (TruSeq standard mapping)
    GSE249925_chemistry: rRNA depletion (TruSeq Stranded Total RNA)

core_alignment_engine:
  software_name: STAR
  manuscript_stated_version: v2.7.x
  execution_command_status: NOT RECOVERED from surviving analysis environment
  documented_parameter_flags:
    --twopassMode: Basic
    --outFilterMismatchNoverLmax: Stated in manuscript as optimized for hg38 long-read / short-read fusion
    --alignSJoverhangMin: Internal splice-junction minimum overhang threshold
    --alignSJDBoverhangMin: Splice-junction database anchor overhang minimum
    --outFilterMultimapNmax: Multi-mapping read exclusion restriction limits
    --quantMode: GeneCounts TranscriptomeSAM

library_ingest_qc_gates:
  minimum_sequencing_depth_per_sample: 70000000  # ~70 million paired-end reads
  minimum_genome_mapping_rate: 0.90              # ~90% alignment accuracy threshold
  quantification_level: Exon-level and splice-junction continuous tracking

splicing_quantification_logic:
  measurement_type: Percent Spliced-In (PSI) continuous fraction
  mathematical_definition: Junction-based exon inclusion relative to adjacent splice configuration spaces
  feature_eligibility_filters:
    minimum_junction_read_support: 50            # >= 50 supporting junction reads
    minimum_cohort_sample_support: 0.80          # >= 80% sample representation
    maximum_statistical_variance_width: 0.25     # PSI 95% Confidence Interval half-width <= 0.25

downstream_matrix_harmonization:
  batch_effect_handling: Technical structure was assessed using principal-component analysis (PCA)
  unadjusted_variation_status: Stated as an analytical limitation in Section 4.5 due to mixed library chemistry
  exact_preprocessing_scripts: NOT RECOVERED from surviving analysis environment

reproducibility_caveat_protocol:
  anti_substitution_clause: TRUE
  guideline_statement: >
    Forward-engineered substitute scripts implemented locally for code testing must 
    be explicitly designated under a [RECONSTRUCTED-ENVIRONMENT] log block and must 
    never be substituted silently for original historical pipeline binaries.






