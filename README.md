---
title: Wildfire Detection
emoji: 📊
colorFrom: red
colorTo: blue
sdk: gradio
sdk_version: 6.14.0
python_version: "3.13"
app_file: app.py
pinned: false
short_description: WildfireDetectionApp
---

# Wildfire Detection App

**M.Tech Dissertation — VNIT Nagpur | Accepted at FICTA 2026 (Springer SIST, Scopus)**

A Gradio-based web app for wildfire detection from UAV images using deep learning models trained for robustness under real-world degradations like noise, fog, and blur.

## Live Demo
[huggingface.co/spaces/jayeshkumeriya/wildfire-detection](https://huggingface.co/spaces/jayeshkumeriya/wildfire-detection)

## Models
| Model | Description |
|---|---|
| `Model2_Epoch_36_ValAcc_1.0000.keras` | Baseline model, 99.80% accuracy |
| `Model2_Final_2026_v2.h5` | Final robust model |
| `model3_ep_17.keras` | Degradation-retrained model, 99.94% accuracy |

## How to Run Locally
```bash
pip install -r requirements.txt
python app.py
```

## Author
**Jayesh Kumeriya** — [LinkedIn](https://linkedin.com/in/jk999)

## Related Repository
[wildfire-robustness-mhcnnfd](https://github.com/0Jayesh/wildfire-robustness-mhcnnfd) — Jupyter notebooks & research phases
