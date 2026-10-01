# Reproducibility Status

## Overall status

The repository provides a transparent documentation layer for the study.

Complete computational rerun of the historical manuscript analysis is not currently possible because the original executable scripts, intermediate files, prediction exports, model objects, and analysis logs are no longer retained.

## Component-level status

| Component | Documentation | Original executable available | Independent rerun |
|---|---|---:|---:|
| Dataset accession inventory | Yes | Not applicable | Yes, source-level |
| Source-level dataset sizes | Yes | Not applicable | Yes |
| Final 450-participant reconciliation | Partial | No | No |
| RNA-seq alignment | Methods documented | No | No |
| PSI calculation | Methods documented | No | No |
| Long-read analysis | Methods documented | No | No |
| Variant annotation | Methods documented | No | No |
| SpliceAI comparator | Tool/version documented | No original wrapper | Partial |
| MaxEntScan comparator | Tool/version documented | No original wrapper | Partial |
| Cardiac-tuned model | Concept documented | No | No |
| Cross-validation | Reported | Original split files unavailable | No |
| Held-out evaluation | Reported | Original prediction files unavailable | No |
| Calibration | Reported | Original prediction files unavailable | No |
| Clinical regression | Reported | Original scripts unavailable | No |
| Digital-twin modeling | Described | Original model unavailable | No |
| Therapeutic prioritization | Described | Original scoring implementation unavailable | No |
| Figure generation | Outputs retained | Scripts unavailable | No |

## What this repository does establish

The repository establishes:

- the identified source datasets;
- the public accession identifiers;
- the methodological workflow described in the manuscript;
- the comparator tools and versions reported;
- the distinction between source-level samples and the final analytic cohort;
- the limitations of the surviving computational record.

## What it does not establish

The repository does not claim that all manuscript numerical results can currently be regenerated exactly from the preserved files.

## Future reconstruction

Independent reconstruction may be performed using the public source datasets and the documented workflow.

Any newly generated results must be explicitly labelled as reconstructed analyses and must not be substituted silently for the original manuscript results.
