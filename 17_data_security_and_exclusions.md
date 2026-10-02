# Data Governance, Security, and Material Verification Boundaries

## 1. Protected Health Information (PHI) & Controlled Exclusions
To comply with institutional review board (IRB) mandates and international data privacy regulations (such as HIPAA and GDPR), specific participant-level datasets are strictly excluded from public repository storage:
- **Raw Sequencing Repositories:** Raw data files (`.fastq`, `.bam`, `.cram`) contain identifiable genetic variations and are restricted to authorized dbGaP/EGA repositories. They cannot be hosted in this public architecture.
- **Participant Access Identifiers:** All internal registration codes, names, or localized clinic serial keys are systematically omitted to enforce complete anonymity.
- **Private Clinical Tables:** Granular medical tracking tables or raw intake notes are completely separated from this analytics suite.
- **Access Credentials:** High-security cryptographic tokens, private server addresses, SSH keys, and system database pass-phrases are entirely restricted.

## 2. Generative Context & System Prompt Tracing
- **Prompt Log Boundaries:** System-level artificial intelligence instruction protocols, intermediate query layouts, and algorithmic context prompts utilized during exploration are explicitly decoupled from the software platform framework.
- **Execution Log History:** Raw analytical history streams and runtime execution parameters are treated as auxiliary developer outputs and are not packaged within standard verification bundles.

## 3. Historic Configuration & Execution Script Integrity
- **Script Generation Rule:** This workspace rejects the injection of synthetically back-filled or reconstructed execution scripts masquerading as original historical code.
- **Audit Logging State:** Any structural reconstruction designed to serve as a placeholder for a missing computational asset must be explicitly flagged with an operational warning tag: `[RECONSTRUCTED-FRAMEWORK-SUBSTITUTE]`.
- **True Provenance Compliance:** Reconstructed blocks do not count as verified historical evidence for retroactive replication runs unless backed by an original cryptographic file hash matching the initial repository configuration.
