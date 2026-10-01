# Cardiac-Tuned Splicing Model Description

## Purpose

The cardiac-tuned model was developed within the myocardium-calibrated splice interpretation framework to estimate splice-disruption-related outcomes in TTN and MYH7.

## Reported input domains

The manuscript describes model inputs including:

- local sequence context;
- exon identity;
- cis-regulatory motifs;
- structural-domain annotations;
- myocardial transcriptomic/splicing features.

## Prediction targets

The reported prediction targets include:

- splice-disruption status;
- exon-level ΔPSI.

The model was not intended to predict HCM or DCM diagnosis directly.

## Historical implementation status

The original executable model, training dataset, split file, hyperparameter record, and prediction export are not currently retained.

The author recalls using a random-forest machine-learning approach incorporating structural DNA features and myocardial gene-expression/splicing information.

However, the manuscript currently contains descriptions of a deep-learning architecture and domain-aware embeddings.

These two descriptions must be reconciled before the repository can claim to contain an exact implementation of the historical model.

## Reproducibility rule

A new model may be developed in the future to reproduce the conceptual workflow, but it must not be labelled as the original model unless it has been demonstrated to reproduce the original implementation and reported results.

## Required information for complete model reproduction

The following historical information is required:

- model algorithm;
- feature matrix;
- target labels;
- sample/variant identifiers;
- train/test split;
- cross-validation folds;
- random seed;
- hyperparameters;
- preprocessing/scaling;
- missing-data handling;
- class balancing;
- probability calibration;
- comparator-score transformation;
- prediction outputs;
- metric calculation code.

