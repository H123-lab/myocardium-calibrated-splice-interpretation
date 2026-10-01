# Comparator Score Transformations — Reconstruction

## Comparators

### SpliceAI

Reported version:

SpliceAI v1.3.1

SpliceAI provides delta scores corresponding to predicted:

- acceptor gain;
- acceptor loss;
- donor gain;
- donor loss.

### MaxEntScan

Reported version:

MaxEntScan Bioconda 0_2004.04.21-4

MaxEntScan provides splice-site scores based on maximum-entropy sequence models.

## Critical reproducibility issue

The manuscript compares comparator outputs with the cardiac-tuned model on a continuous prediction scale.

The exact historical transformation used to convert comparator outputs into that common scale is not currently preserved.

Therefore, no transformation formula is asserted in this repository until the original implementation or analysis record is recovered.

## Required information

The final reproducible implementation must document:

1. raw SpliceAI fields used;
2. whether maximum delta score or another aggregation was used;
3. directionality;
4. raw versus transformed scale;
5. MaxEntScan reference score;
6. MaxEntScan alternate score;
7. delta-score calculation, if used;
8. normalization procedure;
9. clipping or thresholding;
10. missing-value handling.

## Status

Tools and versions documented.

Exact historical score transformation: NOT VERIFIED.

Original transformation script: NOT AVAILABLE.
