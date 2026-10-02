# Software Environment, Container Specifications, and Version Controls

## 1. Directory Mandate
This directory is strictly reserved for hosting the verified, programmatic computational environment used to run the alternative splicing analysis and execute downstream multivariable statistical workflows. 

Accepted assets permitted in this space include:
- Package manager lockfiles (`poetry.lock`, `package-lock.json`)
- Environment specification files (`environment.yml`, `requirements.txt`)
- Container infrastructure definitions (`Dockerfile`, `singularity.def`)

---

## 2. Rigid Version-Lock Compliance Protocol
To guarantee absolute historical fidelity and prevent the introduction of synthetic computational artifacts during independent reproduction:

1. **Anti-Substitution Rule:** Under no circumstances shall current or guessed sub-minor software versions be substituted for historical tools described in original analysis logs as open-ended versions (e.g., STAR `v2.7.x`, GATK `v4.x`, R `v4.x`, or Python `v3.x`). 
2. **Explicit Fallback Labeling:** Where exact patch versions cannot be recovered from the surviving computing environment metadata, the specific fields must remain flagged as `Version not recovered from the surviving analysis environment` within your local build manifests.
3. **Reconstruction Isolation:** If a forward-engineered environment is constructed using contemporary packages to verify script execution logic, the container image configuration must be explicitly tagged as `[RECONSTRUCTED-FRAMEWORK-ENVIRONMENT]` to maintain a clear line of ancestry for scientific review.

---

## 3. Computational Environment Architecture Matrix

Future operators must structure their local deployment manifests to match the baseline software tool variables verified in the primary study tables:

```yaml
environment_metadata:
  target_genome_assembly: GRCh38 (hg38)
  verified_pipeline_tools:
    - tool_name: SpliceAI
      channel_lock_version: v1.3.1
    - tool_name: MaxEntScan
      channel_lock_version: 0_2004.04.21-4
  partially_verified_pipeline_tools:
    - tool_name: STAR
      manuscript_stated_baseline: v2.7.x
      minor_patch_status: Not recovered from surviving environment
    - tool_name: Dorado
      long_read_basecalling_target: v0.5.x
      signal_processing: RNN / Transformer architecture
  runtime_interpreters:
    - environment_core: R (v4.x)
      primary_packages: [survival]
    - environment_core: Python (v3.x)
      primary_packages: [numpy, pandas, scipy, sklearn]
```

