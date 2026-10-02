# Software Environment and Computational Version-Control Record

## 1. Computational Ecosystem Overview
This record maps the complete computational stack, basecalling deep learning modules, sequence-alignment programs, and downstream deep learning layers utilized for the *TTN* and *MYH7* splicing analyses.

**Operational Safeguard Rule:** To maintain strict scientific integrity and prevent retroactive reporting errors, current package versions must never be substituted for historical versions and represented as the software originally deployed. Where software parameters are reconstructed for functional testing, they are explicitly tagged as `[RECONSTRUCTED-FRAMEWORK-ENVIRONMENT]`.

---

## 2. Core Software Stack and Dependency Status

The execution layer spans multiple specialized toolkits, mapped programmatically against our active repository infrastructure tables:

### 2.1 Short-Read RNA-seq Alignment & Quantification Layer
- **Alignment Core Engine:** Splice-aware processing executed via **STAR**. 
  * *Version Status:* `v2.7.x` (Exact minor path patch not recovered from the surviving analysis environment).
- **Reference Assembly Coordinates:** Human Genome Assembly Baseline **GRCh38 (hg38)**.
- **Core Scripting Environment:** **R** and **Python** runtime environments.
  * *Version Status:* R `v4.x` / Python `v3.x` (Specific sub-minor environment branches not recovered from the surviving analysis environment).

### 2.2 Splicing path Pathogenicity & Variant-Level AI Comparators
- **Sequence-Based Splice Predictor:** **SpliceAI**.
  * *Version Status:* **v1.3.1** (Independently verified from benchmark partitions).
- **Motif Maximum-Entropy Predictor:** **MaxEntScan**.
  * *Version Status:* **0_2004.04.21-4** (Bioconda channel lock verified).

### 2.3 Long-Read Transcriptomic Validation Layer
- **Orthogonal Evaluation Data:** Oxford Nanopore Technologies (ONT) full-length transcript cDNA sequencing data.
- **Basecalling AI Baseline:** Handled natively via the **Dorado** recurrent neural network (RNN) and transformer framework.
  * *Version Status:* `Dorado v0.5.x` (Configured to support all-context methylation and high-accuracy raw signal processing).
- **Target Transcript Reference Panel:** Predefined canonical reference annotations mapped to Ensembl transcript structures (e.g., *TTN-213* and *MYH7-201*).

### 2.4 Machine Learning & Statistical Computing Suite
- **Downstream Multivariable Association Analysis:** Core **R** and **Python** machine learning packages used for regression scaling, survival calculations, and digital-twin mechanics.
- **Cardiac-Tuned Splice Prediction Network:** Deep learning architecture incorporating sequence attention and domain-aware embeddings, parameterized as documented in `ai_feature_engineering_spec.yaml`.
  * *Version Status:* Exact historical neural network library versions and GPU-accelerated computing environment configurations are **not recovered from the surviving analysis environment**.

---

## 3. Explicit Software Environment Verification Status

| Software Module / Toolkit | Operational Role | Historical Version Verification Status |
| :--- | :--- | :--- |
| **STAR** | Splice-aware short-read mapping | Partially Verified (`v2.7.x`) |
| **Dorado** | Long-read basecalling AI | Reconstructed Variant Target (`v0.5.x`) |
| **SpliceAI** | Splice-disruption comparator | **Fully Verified (`v1.3.1`)** |
| **MaxEntScan** | Motif matrix delta scoring | **Fully Verified (`0_2004.04.21-4`)** |
| **R Environment** | Proportional hazard models / linear regression | Partially Verified (`v4.x`) |
| **Python Environment** | AI performance evaluation / digital twin logic | Partially Verified (`v3.x`) |
| **Core ML Platform** | Sequence attention network weights | **Not recovered from the surviving analysis environment** |

---

## 4. Reconstructed Execution Safeguard Protocol
Independent operators attempting to rebuild or scale this analytical workspace from public data repositories must implement the following version controls:
1. **Verification Trace Isolation:** Any independent reconstruction executed using current software layers (e.g., modern PyTorch, TensorFlow, or tidyverse suites) must be cataloged separately under a `[RECONSTRUCTED-ENVIRONMENT]` execution log block.
2. **Path Schema Alignment:** Future testing arrays must retain structural input constraints (minimum depth of **~70M reads** and a **~90% mapping rate**) to align safely with the quality benchmarks managed inside `16_software_versions_EXAMPLE.tsv` and `raw_table2_splicing_atlas.tsv`.



