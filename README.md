# clustering-khmer-mounds
Comparative analysis of four spatial clustering methods (DBSCAN, HDBSCAN, percolation analysis, KDE) applied to LiDAR-derived archaeological mound distributions in the Isaura parcel of the Archaeoscape dataset, Greater Angkor, Cambodia. MA thesis project, ACASA Digital Archaeology.

This repository contains the full analysis pipeline for the MA thesis *Clustering 
Khmer Mounds* (Amber Esha Jarigsma, Vrije Universiteit Amsterdam / Universiteit van Amsterdam, 2026), submitted in partial 
fulfilment of the MA Archaeology - Digital Archaeology and Heritage programme.

---
## Repository structure

```
clustering-khmer-mounds/
├── README.md
├── requirements.txt
├── LICENSE
├── data/
│   └── README.md 
├── notebooks/
│   ├── 00_data_checks.ipynb
    ├── 01_kde.ipynb
│   ├── 02_dbscan.ipynb
│   ├── 03_hdbscan.ipynb
│   ├── 04_percolation.ipynb
│   ├── 05_contextual_overlay.ipynb
│   └── 06_evaluation.ipynb
└── outputs/
    ├── figures/
    │   ├── kde/
    │   ├── dbscan/
    │   ├── hdbscan/
    │   ├── percolation/
    │   ├── contextual_overlay/
    │   └── evaluation/
    └── tables/
```

---
## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/[username]/clustering-khmer-mounds.git
cd clustering-khmer-mounds
```

### 2. Install dependencies

Python 3.11 is recommended. Install all required packages using:

```bash
pip install -r requirements.txt
```

### 3. Obtain the data

The Archaeoscape dataset is distributed under an EFEO licence and cannot be included 
in this repository. See `data/README.md` for acquisition instructions. 

### 4. Run the notebooks

Launch Jupyter and run the notebooks in order (00 through 06). Notebook 00 performs data checks and preliminary spatial characterisation and is the recommended starting point. All notebooks load data independently and can be run in any order, though the numbered sequence reflects the logical progression of the analysis.

---

## Methods summary

| Notebook | Method | Key parameters |
|---|---|---|
| 00_data_checks | Data checks and preliminary spatial characterisation | CRS verification, coordinate unit confirmation, NND statistics |
| 01_kde | Kernel Density Estimation | h = 120m, 360m, 500m; thresholds p75/p90/p95 |
| 02_dbscan | DBSCAN | ε = 120m, 200m, 360m; min_samples = 4 |
| 03_hdbscan | HDBSCAN | min_cluster_size = 4, 10, 20; min_samples = 4 |
| 04_percolation | Percolation analysis | r sweep 50–3000m, 200 steps; r_c = 325m |
| 05_contextual_overlay | Overlay mapping | Temple and hydrology proximity |
| 06_evaluation | Cross-method evaluation | DBCV, sensitivity CV%, TDR |

---

## Dataset

Perron, Y., Sydorov, V., Wijker, A. P., Evans, D., Pottier, C., & Landrieu, L. (2024). Archaeoscape: Bringing aerial archaeology to the age of deep learning. In Proceedings of the 38th Conference on Neural Information Processing Systems (NeurIPS 2024) Track on Datasets and Benchmarks.
Data distributed under EFEO licence.

Data attribution: © École française d'Extrême-Orient (EFEO).

---

## Licence

Code and notebooks: MIT License — see `LICENSE`.  
Dataset: subject to EFEO licence terms.

---

## Citation

If you use this code, please cite:

Jarigsma, A.E. (2026). *Clustering Khmer Mounds* [MA thesis]. 
Vrije Universiteit Amsterdam / Universiteit van Amsterdam.
