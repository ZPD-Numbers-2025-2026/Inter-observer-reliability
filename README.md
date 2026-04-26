<div align="center">

# Inter-Observer Reliability Analysis

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

![License](https://img.shields.io/badge/Academic_Project-2025--2026-blue?style=flat-square)
![Raters](https://img.shields.io/badge/Raters-3-green?style=flat-square)
![Images](https://img.shields.io/badge/Images_Labeled-800-orange?style=flat-square)
![Agreement](https://img.shields.io/badge/Overall_Agreement-99.8%25-brightgreen?style=flat-square)

**Statistical validation of labeling consistency across three independent raters for a handwritten digit classification dataset.**

*ZPD-Numbers -- 2025/2026*

</div>

---

## About

This repository contains the inter-observer reliability analysis for a handwritten digit classification task. Three raters -- Michal, Olivier, and Vincenzo -- independently labeled 800 images into 10 categories (digits 0 through 9). The goal is to statistically verify that the human annotations are consistent and trustworthy before using them as ground truth.

## Methodology

The analysis applies standard inter-rater reliability metrics:

| Metric | Scope | Result |
|:--|:--|:--|
| **Fleiss' Kappa** | All 3 raters simultaneously | **0.9981** (almost perfect) |
| **Cohen's Kappa** | Michal vs Olivier | **0.9972** |
| **Cohen's Kappa** | Michal vs Vincenzo | **0.9972** |
| **Cohen's Kappa** | Olivier vs Vincenzo | **1.0000** (perfect) |

Out of 800 images, only **2** had any disagreement between raters -- both involving confusion between digits 8 and 9. No image had all three raters disagree.

## Repository Contents

```
inter_observer_reliability.ipynb   Main analysis notebook
inter_observer_reliability.html    Rendered notebook (viewable in browser)
__merged_michal_.csv               Labels from Rater 1
__merged_olivier_.csv              Labels from Rater 2
__merged_vincenzo_.csv             Labels from Rater 3
```

## How to Run

```bash
pip install pandas numpy scikit-learn statsmodels jupyter
jupyter notebook inter_observer_reliability.ipynb
```

## Interpretation

A Fleiss' Kappa of **0.9981** falls into the "almost perfect" agreement range (> 0.81) on the Landis and Koch scale. This confirms that the labeling process is highly reliable and the resulting annotations can be used with confidence as ground truth for downstream tasks.

<div align="center">

| Kappa Range | Interpretation |
|:--|:--|
| < 0.00 | Poor |
| 0.00 -- 0.20 | Slight |
| 0.21 -- 0.40 | Fair |
| 0.41 -- 0.60 | Moderate |
| 0.61 -- 0.80 | Substantial |
| **0.81 -- 1.00** | **Almost Perfect** |

</div>

---

<div align="center">

**ZPD-Numbers-2025-2026** | Michal Tarnowski, Olivier, Vincenzo

</div>
