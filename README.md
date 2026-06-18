# Wildfire Detection: Robustness-Aware Deep Learning

**M.Tech Dissertation — VNIT Nagpur | Accepted at FICTA 2026 (Springer SIST, Scopus)**

---

## Key Finding

A model achieving **100% accuracy on clean images collapsed to 0.1%** under heavy Gaussian noise. Degradation-inclusive retraining recovered performance to **99.94%+ across all degradation conditions**.

| Condition            | Before Retraining | After Retraining |
| --------------------- | ------------------ | ------------------ |
| Clean images          | 100.0%              | —                  |
| Heavy Gaussian Noise   | **0.1%**            | 99.94%             |
| Light Gaussian Noise   | 1.0%                | 99.68%             |
| Fog / Smoke            | 25.0%               | 100.0%             |
| Motion Blur            | 100.0%              | 100.0%             |

> High benchmark accuracy is not a valid predictor of operational robustness.

---

## What's in this Repo

This repository contains the full experimental pipeline across three phases, comparing two model variants (baseline MHCNNFD and an enhanced version) across replication, cross-dataset benchmarking, and robustness evaluation.

### `phase1_replication/` — Baseline Replication
- `model1_dataset1_replication.ipynb` — Baseline MHCNNFD replication on UAVs-FFDB
- `model2_dataset1_replication.ipynb` — Enhanced model replication on UAVs-FFDB

### `phase2_benchmarking/` — Cross-Dataset Benchmarking
- `model1_dataset2_deepfire.ipynb` / `model2_dataset2_deepfire.ipynb` — Both models evaluated on the DeepFire dataset
- `model1_dataset3_mendeley.ipynb` / `model2_dataset3_mendeley.ipynb` — Both models evaluated on the Mendeley (WILDFIRE-I) dataset

### `phase3_robustness/` — Stress Testing & Robust Retraining
- `dataset_mixing.ipynb` — Combines datasets into a unified multi-source training set
- `stress_test_creation.ipynb` — Builds the degradation test suite (Gaussian noise, motion blur, fog simulation)
- `stress_test_model1.ipynb` / `stress_test_model2.ipynb` — Evaluates both models under degradation conditions, revealing the accuracy collapse
- `robust_dataset_creation.ipynb` — Constructs the 25,935-image robust augmented dataset using 5-way degradation augmentation
- `robust_retraining_model1.ipynb` / `robust_retraining_model2.ipynb` — Retrains both models on the robust dataset, recovering worst-case accuracy to 99.94%
- `model1_mixed_dataset.ipynb` / `model2_mixed_dataset.ipynb` — Final model evaluation on the combined multi-source dataset

---

## Results Summary

- Enhanced MHCNNFD architecture (filter depth 32–64 → 64–256, Batch Normalization) achieved 100% accuracy on UAVs-FFDB and 99.80% on a 20,027-image multi-source dataset with zero fire false negatives.
- Benchmarked original vs. enhanced variants across three independent datasets (UAVs-FFDB, WILDFIRE-I, DeepFire).
- Discovered catastrophic accuracy collapse under real-world degradation and recovered performance through degradation-inclusive retraining.

---

## Publication

Accepted at **FICTA 2026**, London Metropolitan University (Springer SIST, Scopus indexed).

## Live Demo

👉 [huggingface.co/spaces/jayeshkumeriya/wildfire-detection](https://huggingface.co/spaces/jayeshkumeriya/wildfire-detection)

## Related Repository

- [wildfire-detection-app](https://github.com/0Jayesh/wildfire-detection-app) — Gradio inference app deploying the trained models from this research

## Author

**Jayesh Kumeriya** — [LinkedIn](https://linkedin.com/in/jk999) | jayeshkumeriya999@gmail.com
