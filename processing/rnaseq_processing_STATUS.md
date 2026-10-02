# RNA-seq Processing Pipeline Core Verification and Status Record

## 1. Executive Summary & Audit Baseline
This record documents the exact bioinformatic processing constraints, quality control thresholds, and baseline alignment parameters described across the manuscript for human left-ventricular transcriptomic files.

**Rigid Compliance Rule:** The original historical command-line processing binaries and exact runtime execution logs are currently classified as **UNRECOVERED**. To protect scientific integrity, a newly generated alignment script must **never be presented as the original historical implementation**. Newly developed pipeline substitutes implemented for reproducibility testing must be explicitly tagged as `[RECONSTRUCTED-FRAMEWORK-PIPELINE]`.

---

## 2. Manuscript-Described Reference Workflow

The primary bioinformatic pipeline utilizes specific filter boundaries to map raw sequence data into the continuous splicing features archived in `raw_table2_splicing_atlas.tsv`:
- **Reference Assembly Anchor:** Standardized alignment to Human Genome Assembly **GRCh38 (hg38)**.
- **Mapping Infrastructure Core:** Splice-aware short-read processing executed via **STAR** (Stated as version framework `v2.7.x`).
- **Pipeline Processing Sequence:** Downstream steps encompass exon/junction quantification, exon-level percent spliced-in (PSI) estimations, disease-stratified cohort differential evaluations (\(\Delta\text{PSI}\)), and technical batch-effect correction.

### Stated Quality Control Ingest Filters
To filter out sequencing artifacts and capture true physiological cardiac signals, the pipeline enforces strict sample-level thresholds:
* **Minimum Sequencing Depth:** Approximately **70 million paired-end reads** per library.
* **Minimum Mapping Rate:** Approximately **90% alignment accuracy** against the hg38 reference genome.

---

## 3. Structural Splicing Eligibility & Metric Criteria

To satisfy peer-review data audits, individual exon elements are locked to a strict filtering schema managed inside the `variable_dictionary.csv` master matrix:

| Quality Parameter Gate | Mandatory Threshold Limit | Functional Role in Splicing Ingest |
| :--- | :---: | :--- |
| **Minimum Junction Read Support** | \(\ge 50\) continuous reads | Prevents false-positive splicing detection in low-coverage ranges. |
| **Cohort Feature Representation** | Supported in \(\ge 80\%\) of testing samples | Eliminates sporadic, non-representative alternative splicing artifacts. |
| **Maximum PSI 95% CI Width** | \(\le 0.25\) internal confidence interval | Enforces tight statistical variance bounds across all processed matrices. |

---

## 4. Current Replication & Version Tracking Status

The software tools and analysis environments are logged below to define the specific version limits of the current computational footprint:

- **STAR Alignment Wrapper:** Stated in manuscript as `v2.7.x`. Exact minor patch and historical shell parameter configurations are **not recovered from the surviving analysis environment**.
- **Exon Quantification Core:** Downstream data consolidation executed via **R** (`v4.x`) and **Python** (`v3.x`). Exact sub-minor dependencies or package namespaces are **not recovered from the surviving analysis environment**.
- **Forward-Engineered Baseline Match:** While raw individual sequence records (`.fastq`, `.bam`) are securely isolated within repository safe-harbors (`DATA_PROVENANCE.md`), the continuous cohort-level group totals match with 100% precision:
  \[\text{Global Reconciled Inclusions} = \text{80 Controls} + \text{160 DCM} + \text{120 HCM} + \text{90 Other-CM} = \text{450 Unique Participants}\]

---

## 5. Required Information for Absolute Core Reconstruction

To transition this tracking log to **Fully Restored and Verified Status**, the following explicit computational parameters must be recovered from historical cluster system backups or laboratory server configuration nodes:
- [ ] The precise, un-reconstructed system script configurations (`.sh` or `.py` files) orchestrating the STAR two-pass mapping loops.
- [ ] The exact command-line string parameter flags deployed for genome indexing, max intron length limits, and multi-mapping read exclusions.
- [ ] The exact, unimputed intermediate sample-level count matrices used prior to batch-effect PCA alignment.




