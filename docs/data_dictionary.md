# Comprehensive Data Dictionary and Variable Definitions

## 1. Purpose & Core Governance Framework
This document provides a factory-calibrated reference matrix defining the exact variables, engineering scales, missingness handling protocols, and analytical roles utilized throughout the study. 

All structural data fields conform strictly to the global cohort configuration of **450 unique individual participants** (80 Controls, 160 DCM, 120 HCM, 90 Other Cardiomyopathies).

---

## 2. Integrated Multi-Modal Variable Specifications

| Variable | Structural Definition | Precise Unit / Scale | Source or Derivation Pathway | Missing-Data Handling | Primary Analytical Role |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Participant identifier** | Anonymized unique patient linkage key. | Categorical alphanumeric string | Unified cohort manifest harmonization log. | Not applicable (Complete linkage mandatory for entry) | Deduplication, cohort tracking, and baseline matching |
| **Diagnostic group** | Clinical phenotype classification domain. | Categorical: `Control`, `DCM`, `HCM`, `Other-CM` | Clinical intake records and registry adjudication logs. | Complete-case exclusion; no ambiguous labels permitted | Primary stratification axis and multi-model covariate |
| **LVEF** | Left Ventricular Ejection Fraction. | Percentage (%) | Quantitative Transthoracic Echocardiography / Cardiac MRI. | Retained if reported; completely omitted from imputation | Phenotypic structural outcome variable |
| **LVEDVi** | Left Ventricular End-Diastolic Volume Index. | Milliliters per square meter (\(\text{mL/m}^2\)) | Derived: Left ventricular volume divided by Body Surface Area (BSA). | Retained if reported; completely omitted from imputation | Phenotypic structural outcome variable |
| **Global Longitudinal Strain (GLS)** | Peak systolic myocardial longitudinal deformation strain. | Percentage (%) | Echocardiographic speckle-tracking software array. | Secondary structural marker; listwise deletion if missing | Phenotypic functional outcome variable |
| **PSI (Percent Spliced-In)** | Relative proportion of transcripts containing a specific targeted exon feature. | Fraction (\(0.0 \text{ to } 1.0\)) inside models; stated as % (\(0 \text{ to } 100\%\)) in text sheets | Calculated via split-junction read ratio from RNA-seq quantification pipeline. | Programmatic exclusion if junction read coverage drops below 50 reads | Alternative splicing feature measurement variable |
| **\(\Delta\text{PSI}\)** | Absolute alternative splicing shift across cohorts. | Percentage points (\(\text{pp}\)) relative to non-failing controls | Calculated: \(\text{PSI}_{\text{Disease Mean}} - \text{PSI}_{\text{Control Mean}}\) | Omitted if parent exon fails local coverage QC thresholds | Differential splicing effect-size indicator |
| **Junction read support** | Depth of coverage across target exon boundaries. | Integer discrete read count | Raw sequencing alignments parsed via splice-aware STAR pipelines. | Hard boundary: Must maintain \(\ge 50\) reads in \(\ge 80\%\) of samples | Feature eligibility filter and strict data QC gate |
| **PSI confidence width** | Statistical margin of error bounding the calculated PSI output. | Continuous interval fraction (\(0.0 \text{ to } 1.0\)) | Standard error calculation from junction dispersion modeling. | Hard boundary: Must maintain a 95% CI half-width \(\le 0.25\) | Feature eligibility filter and structural QC gate |
| **TTN N2BA:N2B ratio** | Relative expression of spring-domain structural transcript configurations. | Continuous quantitative ratio | Derived: Total aggregated N2BA-specific exon expressions divided by N2B metrics. | Tracked continuously via multi-isoform alignment weights | Central molecular biophysical predictor variable |
| **MYH7 domain PSI score** | Domain-localized aggregate splicing configuration score. | Fraction (\(0.0 \text{ to } 1.0\)) | Derived: Exon identity mapping grouping coordinates by head, neck, and rod domain. | Evaluated if raw component exons pass local coverage filters | Domain-aware biophysical tracking variable |
| **SpliceAI score** | Deep learning variant splice-disruption delta metrics. | Continuous probability matrix score (\(0.0 \text{ to } 1.0\)) | Parsed directly from pre-compiled SpliceAI v1.3.1 neural networks. | Parsed across absolute sequence coordinates; no missing data | Baseline machine learning model comparator |
| **MaxEntScan score** | Motif matrix maximum-entropy splice-site boundary index. | Tool-specific continuous score | Extracted from MaxEntScan Bioconda channel release 0_2004.04.21-4. | Calculated relative to native sequence motifs; no missing data | Baseline motif-strength model comparator |
| **CardioSplice-RU output** | High-performance calibrated splice-disruption probability metrics. | Continuous calibrated probability score (\(0.0 \text{ to } 1.0\)) | Core output from integrated tissue-context sequence attention network. | Handled via domain-aware sequence embeddings | Primary predictor tool endpoint |
| **6MWT** | Six-Minute Walk Test continuous walking distance. | Meters (\(\text{m}\)) | Secondary outcome registries (clinical cohort metadata pools). | Retained strictly as reported; zero mathematical imputation | Secondary functional metric (uncollected in primary bulk assays) |
| **Grip strength** | Quantitative isometric upper-extremity muscle force. | Kilograms (\(\text{kg}\)) | Secondary outcome registries (clinical cohort metadata pools). | Retained strictly as reported; zero mathematical imputation | Secondary functional metric (uncollected in primary bulk assays) |

---

## 3. Strict Reporting & Mathematical Unit Conventions

To achieve flawless data traceability and fulfill peer-review auditing standards, the data extraction layer enforces absolute distinction between the following terms:

*   **Splicing Ratios vs. Text Displays:** Within all predictive model matrices and scripting functions, Percent Spliced-In must be evaluated as a fractional value between \(0.0\) and \(1.0\). Text files and manuscript diagrams convert this value to a percentage (\(0\text{ to }100\%\)) for readability.
*   **Splicing Deviations (\(\Delta\text{PSI}\)):** Changes in alternative splicing between disease cohorts and healthy controls must be presented as **percentage points (pp)** to avoid mathematical confusion with percentage changes of raw fractions.
*   **Denominators:** Individual human participant counts (\(n=450\)) must remain completely distinct from technical library, sample cluster, or sequencing run counts across multi-center source registries.
*   **Missingness Stratification:** A hard boundary isolates *Missing Measurements* (entries that were expected but dropped during processing due to quality controls like low depth) from *Measurements Not Collected* (variables such as functional grip strength or 6MWT distance that were never present in specific source clinical databases like bulk tissue repositories).

---

## 4. Missingness & Non-Imputation Policy

In order to protect statistical validation metrics from synthetic optimization artifacts:
1. **Zero Phenotypic Imputation:** Missing continuous clinical indices, missing echocardiography tracking metrics, and missing outcomes are **never imputed or back-filled** via computational modeling. 
2. **Denominators Modality Locking:** All downstream multivariable linear regressions and time-to-event Cox proportional hazards models use explicit, modality-specific sample denominators that are reported directly on the face of the statistical table.
3. **Exclusion Tracking:** Features or datasets failing quality control boundaries are categorized explicitly under their operational drop vectors (`QC_FAIL_LOW_DEPTH`, `QC_FAIL_LOW_MAPPING`, or `QC_FAIL_LOW_JUNCTION_COVERAGE`) inside the metadata layer.


