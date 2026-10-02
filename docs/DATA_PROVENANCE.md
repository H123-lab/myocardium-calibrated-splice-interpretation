# Data Provenance and Bioinformatic Base-Resolution Record

## 1. Multi-Modal Data Ingest Framework
This framework operates entirely under open-access genomic safe-harbor standards. The study utilizes previously generated, de-identified human cardiac transcriptomic, genomic, imaging, and clinical datasets. 

**Core Governance Mandate:** No new human participants were recruited, and no new biological tissue specimens were collected for this study. All downstream parameters are calibrated against a global pool of **450 unique individual participants**.

---

## 2. Primary Public Transcriptomic Resources

The primary data layers are trace-mapped directly to their repository architectures and accession coordinates as validated in the study manifest:

| Core Resource / Study Origin | Repository Accessions | Primary Role in Analytics Pipeline |
| :--- | :--- | :--- |
| **Verdonschot et al.** | GEO: `GSE146621` <br>BioProject: `PRJNA611524` | Left-ventricular (LV) myocardial short-read RNA-seq; DCM structural splice-variant analysis. |
| **Wehrens et al.** | GEO: `GSE138262` <br>BioProject: `PRJNA575238` | Human septal myectomy scRNA-seq tissue matrix; cell-type specific alternative expression context mapping. |
| **MAGNet Repository** | GEO: `GSE141910` | Large-scale LV cardiac transcriptomic reference atlas; disease-stratified baseline quantification matrices. |
| **Human HCM mRNA Profiling** | GEO: `GSE249925` <br>BioProject: `PRJNA1051135` | High-depth cardiac biopsy mRNA profiles mapping clinical HCM variants and matching controls. |

---

## 3. Verified Public-Resource Profiles & Quality Boundaries

### 3.1 GSE146621
- **Methodological Context:** Human left-ventricular short-read sequencing evaluating transcriptomic clustering in *TTN*- and *LMNA*-associated dilated cardiomyopathy.
- **Inventory Metrics:** Contains **29 independent samples**. Raw sequencing layers are accessed through the Short Read Archive (SRA) via execution run `SRP252042`, with static processed tables tracked through the corresponding GEO series.

### 3.2 GSE138262 / PRJNA575238
- **Methodological Context:** Single-cell/single-nucleus transcriptomic processing derived from human hypertrophic cardiomyopathy septal myectomy samples.
- **Inventory Metrics:** Comprises **16 sequencing libraries** originating from **5 biological participants**.
- **Integration Boundary:** This resource serves as an orthogonal cell-type validation marker. In accordance with the study metrics, these 5 reference individuals are **strictly excluded from the bulk RNA-seq participant count** to ensure no overlapping data inflation occurs.

### 3.3 GSE141910 (MAGNet)
- **Methodological Context:** Large-scale left-ventricular biobank tissue resource spanning non-failing donor matrices and advanced heart-failure cohorts.
- **Inventory Metrics:** Contains **366 raw sample profiles**. This database encapsulates non-failing controls and distinct cardiomyopathy groups (including DCM, HCM, and peripartum cardiomyopathy).

### 3.4 GSE249925 / PRJNA1051135
- **Methodological Context:** Cardiac biopsy mRNA profiling mapping targeted variant outcomes against corresponding baseline cohorts.
- **Inventory Metrics:** Consists of **120 total samples** (23 non-failing controls and 97 clinical HCM cases). Raw binary layers are stored via SRA, with count tables hosted on the public GEO portal.

---

## 4. Source-Level Versus Analytic-Cohort Filtration Mechanics

Source-level dataset size must not be interpreted as equivalent to the final unique participant denominator (\(n=450\)). Raw database entries undergo strict bioinformatic quality filtering to account for structural variances:
1. **Multi-Library Configurations:** Source files frequently contain duplicate technical sequencing replicates from single individual donor structures.
2. **Programmatic Quality Drops:** Low-depth libraries failing to match the study's mapping thresholds (minimum sequencing depth of **~70 million paired-end reads** and a **~90% mapping rate**) are dropped during pre-processing.
3. **Splice Junction Filters:** Exons are systematically excluded from the downstream percent spliced-in (PSI) data matrices if they fail to meet the strict requirement of **\(\ge 50\) supporting junction reads in \(\ge 80\%\) of samples**.

---

## 5. Functional Provenance & Pipeline Replication Status

The following framework layers have been independently verified against public repository records:
- [x] Primary accession numbers and BioProject identifiers.
- [x] Broad tissue/assay descriptions and experimental design context.
- [x] Source-level repository sample counts and data availability pathways.

### Current Audit Classification: PARTIAL STATUS
The aggregate group distributions (**80 Controls, 160 DCM, 120 HCM, and 90 Other Cardiomyopathies**) are 100% verified and locked with zero variance. However, the exact patient-level source-to-final tracking manifest is currently unrecovered from a surviving cross-walk file. Independent participant-level replication steps are managed transparently within `COHORT_RECONCILIATION.md`.

---

## 6. Raw Data Handling and Safe Harbor Framework
- **Retrieval and Retention:** Historical analysis was executed utilizing raw sequencing reads (FASTQ/BAM formats). In compliance with data-sharing mandates and genomic safe-harbors, raw binary source files are not redistributed through this code repository.
- **Independent Execution:** Researchers wishing to execute the alternative splicing quantification pipelines locally must pull the raw sequence chunks directly from the originating archives under their native access conditions.
- **Basecalling and Prediction Environment:** Basecalling for orthogonal long-read structures relies on **Dorado v0.5.x**. Deep-learning variant interpretation is evaluated using pre-compiled networks anchored to **SpliceAI v1.3.1** and **MaxEntScan Bioconda 0_2004.04.21-4**. Command parameters are locked programmatically inside `16_software_versions_EXAMPLE.tsv`.









