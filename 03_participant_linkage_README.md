# Participant Linkage Governance and Verification Status Record

## 1. Executive Summary & Audit Baseline
This record documents the exact data boundaries, identity protection frameworks, and verification constraints governing individual participant tracing within this public analytical framework. 

**Core Governance Mandate:** In strict adherence to open-access human genomic safe-harbor standards and institutional data privacy constraints, no participant-level linkage tables, cross-walk maps, or direct/indirect health identifiers are stored within this public repository architecture.

---

## 2. Manuscript-Reported Cohort Architecture

The study enforces a definitive, mutually exclusive group distribution locked precisely to an aggregate footprint of **450 unique individual participants**:

\[\text{Total Sample Cohort} = \text{Controls} (80) + \text{DCM} (160) + \text{HCM} (120) + \text{Other CM} (90) = 450\]

- **Manuscript Statement:** The published draft reports an analytical footprint of exactly 450 unique individuals distributed identically across these diagnostic buckets.
- **Verification Audit Result:** The cohort sums balance precisely across all primary statistical tests and forward-engineered validation code models.

---

## 3. Linkage Gaps & Non-Inference Protocols

### Current Verification Status: PENDING EXPLICIT LINKAGE RECOVERY
The original participant-level linkage master file mapping raw source-dataset identifiers (such as SRA, dbGaP, or EGA repository numbers) directly to the anonymized, de-identified 450-participant analytic cohort codes is **unrecovered from the surviving analysis logs**. 

To protect study validity and enforce absolute transparency:
1. **No Speculative Reconstruction:** Under no circumstances shall individual participant keys, private clinical markers, or local database serial rows be inferred or generated using aggregate numbers, public sample metadata, or manuscript tables.
2. **Decoupling of Source Metadata:** Publicly available sample-level identifiers provided by open archives serve strictly as *source metadata*. They are not represented in this environment as active evidence that a specific sequence library contributed to the final 450-participant cohort unless that linkage can be independently verified.
3. **Rigid Separation of Data Assets:** Public dataset accession tracking layers are managed independently in `01_dataset_inventory.csv` and `accession_inventory.csv` to ensure structural traceability without data leakage.

---

## 4. Controlled-Access Data Privacy & Security Boundaries
To maintain a bulletproof compliance profile under institutional review board (IRB) and data protection audits (HIPAA/GDPR):
- **Prohibited Data Classes:** No participant names, social identifiers, direct or indirect clinical intake tables, system credentials, API tokens, or individual-level controlled-access genetic read arrays are included in this open repository branch.
- **Traceability Baseline:** Cohort configurations are maintained strictly at the aggregate, cluster, or variant-level summary tier. Source repository file counts and programmatic quality drop metrics are cataloged cleanly in `source_level_counts.tsv`.

---

## 5. Mandatory Criteria for Complete Replication Tracing

To transition this tracking document from **Partial Status** to **Fully Reconstructed Status** upon recovery of the original administrative files, the verified participant manifest must conform to the following explicit tracking schema:

```tsv
source_dataset	source_sample_id	participant_id_or_source_identifier	diagnosis	tissue	modality	included	exclusion_reason	duplicate_status	final_cohort_group
```

*Note: The metadata structure above is intended solely for local offline processing scripts and must remain excluded from public version-controlled history maps.*


