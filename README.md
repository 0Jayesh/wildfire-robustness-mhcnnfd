# Wildfire Detection: Robustness-Aware Deep Learning
**M.Tech Dissertation — VNIT Nagpur | Accepted at FICTA 2026 (Springer SIST, Scopus)**

---

## Key Finding

A model achieving **99.80% accuracy on clean images collapsed to 0.1%** under real-world sensor noise. Degradation-inclusive retraining fully recovered performance to **99.94% across all conditions**.

| Condition | Before Retraining | After Retraining |
|---|---|---|
| Clean images | 99.80% | 99.96% |
| Heavy Gaussian Noise | **0.1%** | 99.94% |
| Light Gaussian Noise | 1.0% | 99.68% |
| Fog / Smoke (70%) | 25.0% | 100.0% |
| Motion Blur | 100.0% | 100.0% |

> High benchmark accuracy is not a valid predictor of operational robustness.

---

## What's in this Repo

- `phase1_replication/` — MHCNNFD baseline replication on UAVs-FFDB
- `phase2_benchmarking/` — Cross-dataset evaluation (DeepFire, WILDFIRE-I)
- `phase3_robustness/` — Mixed dataset, stress testing, robust retraining

---

## Publication
Accepted at **FICTA 2026**, London Metropolitan University (Springer SIST, Scopus indexed).

## Live Demo
👉 [huggingface.co/spaces/jayeshkumeriya/wildfire-detection](https://huggingface.co/spaces/jayeshkumeriya/wildfire-detection)

## Author
**Jayesh Kumeriya** — [LinkedIn](https://linkedin.com/in/jk999) | [jayeshkumeriya999@gmail.com](mailto:jayeshkumeriya999@gmail.com)
