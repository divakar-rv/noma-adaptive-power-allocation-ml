# Machine Learning Based Adaptive Power Allocation in NOMA

A data-driven power allocation framework for a two-user downlink NOMA (Non-Orthogonal Multiple Access) wireless communication system, using machine learning to dynamically adapt to channel conditions.

## Overview

In NOMA systems, multiple users share the same time-frequency resource, differentiated by power levels. Allocating power well — especially to users on weaker channels — is critical for reliability. This project uses a machine-learning classifier to assess instantaneous channel quality and adjust power allocation in real time, rather than relying on static allocation schemes.

## Dataset

- **DeepSig RML2016.10a** — a benchmark dataset of raw complex I/Q baseband radio signal samples, commonly used in RF signal classification research.

## Methodology

1. **Feature Extraction** — extracted time-domain statistical features from raw I/Q samples:
   - Signal-to-Noise Ratio (SNR)
   - Mean
   - Standard deviation
   - Dynamic amplitude range

2. **Model Training** — trained a **Random Forest classifier** (100 estimators, 80/20 train/test split) to evaluate instantaneous wireless channel quality.
   - Achieved **>95% classification accuracy**

3. **Adaptive Power Allocation** — implemented real-time inference logic that dynamically adjusts power coefficients based on predicted channel state, allocating up to **90% of power to weaker users** during poor link conditions to maximize link reliability.

## Tech Stack

- **Language:** Python
- **ML:** scikit-learn (Random Forest)
- **Signal Processing:** Feature extraction from I/Q baseband samples

## Results

- Random Forest classifier: **>95% accuracy** in channel quality classification
- Adaptive scheme dynamically reallocates up to 90% power to weaker users under poor channel conditions, improving link reliability over static allocation

## Author

Divakar V — B.Tech Electronics and Communication Engineering, VIT Chennai
