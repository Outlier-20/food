# Food


[![IEEE Standard](https://img.shields.io/badge/Standard-IEEE%20Academic-blue)](#)
[![Data](https://img.shields.io/badge/Data-Real%20Public%20Data%20(2016--2026)-green)](#)

## Overview

The **Causal Forensic Anomaly Detection System (CFADS)** is an end-to-end framework designed to detect, analyze, and quantify systemic anomalies across global supply chain networks and cyber incident datasets. Operating on real public data spanning **2016–2026**, CFADS applies causal inference and Gaussian Mixture Models (GMM) to identify security breaches, cold chain disruptions, and financial impacts[cite: 1].

---

## Stages 5–7: Final Report

### 1. Stage 5: Documentation Layer

Complete documentation is produced per stage following IEEE academic publication standards[cite: 1]:
* **Stage 1:** Planning & Definition (`.docx` + `.tex` + `.R`)[cite: 1]
* **Stage 2:** Data & Methodology (`.docx` + `.tex` + `.R` + 6 CSV layers)[cite: 1]
* **Stage 3:** Modeling & Algorithm (`.docx` + `.tex` + `.R`)[cite: 1]
* **Stage 4:** Full Implementation (`.R` + `.tex` + Python pipeline)[cite: 1]
* **Stages 5–7:** Visualization, Scientific Rigor, and Evaluation[cite: 1]

---

### 2. Stage 6: Visualization Layer

#### Figure 1: Anomaly Score Timeline (2016–2025)
![Figure 1](photo/Figure1_Anomaly_Score_Timeline.png)
*Figure 1. Anomaly scores over time. 2020 flagged as **HIGH ANOMALY** (COVID + Americold/Harvest Sherwood attacks)[cite: 1]. 2023 and 2025 flagged **SUSPICIOUS**[cite: 1].*

---

#### Figure 2: Actual vs Expected Food Loss
![Figure 2](photo/Figure2_Actual_vs_Expected_Food_Loss.png)
*Figure 2. Model fit ($R^2 = 0.911$)[cite: 1]. Points near the diagonal indicate good prediction; deviations indicate potential anomalies[cite: 1].*

---

#### Figure 3: Cyber Incidents vs Food Loss
![Figure 3](photo/Figure3_Cyber_Incidents_vs_Food_Loss.png)
*Figure 3. Dual-axis plot showing exponential growth in cyber incidents (8 to 265) alongside food loss percentage trends[cite: 1].*

---

#### Figure 4: Correlation Heatmap
![Figure 4](photo/Figure4_Correlation_Heatmap.png)
*Figure 4. Pairwise correlation matrix revealing strong positive correlations between cyber incidents, ransomware, and financial impact[cite: 1].*

---

#### Figure 5: Residual Distribution
![Figure 5](photo/Figure5_Residual_Distribution.png)
*Figure 5. Residual distribution with normal fit (left) and Q-Q plot (right)[cite: 1]. Shapiro-Wilk $p = 0.300$ confirms normality assumption[cite: 1].*

---

#### Figure 6: Financial Impact Timeline
![Figure 6](photo/Figure6_Financial_Impact_Timeline.png)
*Figure 6. Estimated financial impact growing from $50M (2016) to $2.5B (2025), color-coded by anomaly classification[cite: 1].*

---

### 3. Stage 7: Scientific Rigor & Evaluation

#### 7.1 Model Performance Metrics

| Metric | Value |
| :--- | :--- |
| **$R^2$** | 0.9112 (91.1%)[cite: 1] |
| **LOOCV RMSE** | 0.5268[cite: 1] |
| **LOOCV MAE** | 0.4982[cite: 1] |
| **Sensitivity (High-Cyber)** | 0.4000 (40%)[cite: 1] |
| **GMM Components ($K^*$)** | 4[cite: 1] |
| **Shapiro-Wilk $p$-value** | 0.2999 (normality OK)[cite: 1] |
| **Residual SD** | 0.2646[cite: 1] |

#### 7.2 Key Findings
* **2020 (HIGH ANOMALY):** COVID-19 pandemic disruptions compounded by major cyber attacks (Americold, Harvest Sherwood)[cite: 1]. Loss spiked to 25.8% from 24.0% in 2019[cite: 1].
* **2023 (SUSPICIOUS):** Dole ransomware ($10.5M), Americold second attack, Sysco breach (167 sector incidents)[cite: 1].
* **2025 (SUSPICIOUS):** Record 265 incidents[cite: 1]. DragonForce attacks on M&S and Co-op Group, Everest on Coca-Cola[cite: 1].
* **Emerging Risk:** Incidents grew 33x (8 to 265) while loss remained elevated (23–26%), suggesting cyber threats as an emerging systemic risk factor[cite: 1].

#### 7.3 Reproducibility Statement
All code operates on 6 CSV data layers provided[cite: 1]. No external API calls, authentication, or simulated data required[cite: 1]. The pipeline can be executed end-to-end in R (`Stage4_Full_Implementation.R`) or Python (`run_cfads_pipeline.py`)[cite: 1].

#### 7.4 Limitations
* Small sample size (10 annual observations) limits statistical power[cite: 1].
* Sensitivity of 40% indicates room for improvement in anomaly detection threshold calibration[cite: 1].
* Cyber incident data quality varies; early years (2016–2019) have fewer documented cases[cite: 1].
* Causal claims require stronger identification strategies (e.g., instrumental variables, RDD)[cite: 1].

#### 7.5 Future Work
* Expand to monthly/quarterly resolution for higher statistical power[cite: 1].
* Integrate real-time IoT cold chain sensor data when available[cite: 1].
* Apply formal causal discovery algorithms (PC algorithm, FCI)[cite: 1].
* Develop an interactive dashboard for real-time anomaly monitoring[cite: 1].

---

## References

1. [FAO FAOSTAT](https://www.fao.org/faostat/)[cite: 1]
2. [NOAA Climate Data Online](https://www.ncei.noaa.gov/cdo-web/)[cite: 1]
3. [World Bank LPI](https://lpi.worldbank.org/)[cite: 1]
4. [USDA FoodData Central](https://fdc.nal.usda.gov/)[cite: 1]
5. [Food & Ag-ISAC](https://www.foodandag-isac.org/)[cite: 1]
6. [Zenodo Food Loss Dataset](https://zenodo.org/records/15357549)[cite: 1]
7. [ScienceDirect Cyber Review](https://www.sciencedirect.com/science/article/pii/S2666154325006167)[cite: 1]
