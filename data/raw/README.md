# Raw Data Safe-Harbor and External Retrieval Directory

## 1. Governance and Storage Mandate
**CRITICAL PROTOCOL:** Raw source sequencing data, raw genomic alignment files (`.fastq`, `.bam`, `.cram`), and unblinded individual-level patient registries are **strictly forbidden** from being stored or uploaded to this version-controlled repository. 

This repository operates entirely under open-access genomic safe-harbor standards to preserve participant privacy bounds and enforce compliance with institutional data-use agreements.

---

## 2. Instructions for Independent Replication
To execute or audit the complete processing and splicing quantification pipelines locally, researchers must reconstruct the raw data layer independently:

1. **Accession Inventory:** Navigate to the master tracking record at `dataset_inventory_provenance.md` to review the precise dataset source lists, publication origins, and cohort allocations.
2. **Open-Access Acquisition:** Obtain the unrestricted underlying cardiac transcriptomic reference blocks directly from the public repositories using their verified accession numbers:
   * **GSE146621** (Verdonschot et al. / Illumina NextSeq short-read RNA-seq)
   * **GSE138262** (Wehrens et al. / Single-cell transcriptomic reference matrix)
   * **GSE249925** (Human Hypertrophic Cardiomyopathy mRNA profiling atlas)
   * **GSE141910** (MAGNet large-scale myocardial tissue bulk database)
3. **Controlled-Access Requests:** For restricted or multi-modal clinical data files, formal applications must be submitted directly to the designated data access committees, steering bodies, or repository governance architectures under their specific institutional licensing terms.

---

## 3. Mandatory Local Curation Checklist (For Independent Operators)
When compiling local source layers inside your offline execution environment, researchers are required to populate their local data manifests with the following discrete tracking parameters:
- [ ] **Retrieval Date:** Record the exact timestamp when the external archive chunk was securely fetched.
- [ ] **Source Accession Locus:** Explicitly link the database reference point.
- [ ] **File Identifiers:** Map all internal raw filenames exactly.
- [ ] **Cryptographic Checksums:** Document secure hash outputs (`MD5` or `SHA-256`) generated immediately post-download to verify that incoming binary files match the original historical records exactly.

