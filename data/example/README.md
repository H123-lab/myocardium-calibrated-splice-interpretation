# Example Data and Demonstration Environment

## 1. Directory Purpose
This directory is reserved for small example inputs, standardized feature configuration matrices, and mockup parameters used to demonstrate software execution and verify bioinformatic script functionality.

## 2. Integrity and Data Labeling Mandates
- **Synthetic Labeling Rule:** Any synthetic or dummy dataset utilized to verify script execution paths must be explicitly labeled as synthetic within its filename (e.g., `synthetic_hcm_splicing_metrics.csv`), immediate code headers, and repository metadata.
- **No Scientific Substantiation:** Synthetic parameters serve exclusively as code-testing placeholders. They must not be used to substantiate manuscript findings, validate biological hypotheses, or be reported as observed clinical results.
- **Verification Protocol:** Demonstration data files and matching unit tests will be committed to this directory only after the corresponding processing code and expected biophysical behaviors have been programmatically verified.

## 3. Data Privacy and Safe Harbor Compliance
In strict compliance with patient confidentiality frameworks and data-use agreements, no raw or controlled-access clinical sequencing reads (`.fastq`, `.bam`, `.cram`) or unblinded participant identifiers are permitted within this open-source architecture.

# Move to repository root and create the example data directory
cd myocardium-calibrated-splice-interpretation
mkdir -p example_data

# Stage, commit, and push the repository updates
git add example_data/README.md
git commit -m "docs(data): initialize example_data directory with strict data-labeling and privacy guidelines"
git push origin main
