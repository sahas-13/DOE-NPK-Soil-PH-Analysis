# 📊 Data

This folder contains two datasets used in the DoE analysis.

---

## 1. Crop_recommendation.csv

| Property | Detail |
|---|---|
| **Source** | [Kaggle — Crop Recommendation Dataset](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset) |
| **Rows** | 2200 |
| **Columns** | 8 |

### Columns

| Column | Description |
|---|---|
| `N` | Nitrogen content ratio in soil |
| `P` | Phosphorus content ratio in soil |
| `K` | Potassium content ratio in soil |
| `temperature` | Temperature in °C |
| `humidity` | Relative humidity in % |
| `ph` | pH value of soil ← **Response Variable** |
| `rainfall` | Rainfall in mm |
| `label` | Recommended crop name |

---

## 2. factorial_doe_table.csv

| Property | Detail |
|---|---|
| **Rows** | 8 |
| **Columns** | 4 |
| **Created by** | `DOE_Analysis.ipynb` — Cell 2 |

### Columns

| Column | Description |
|---|---|
| `N` | Coded Nitrogen level (−1 = Low, +1 = High) |
| `P` | Coded Phosphorus level (−1 = Low, +1 = High) |
| `K` | Coded Potassium level (−1 = Low, +1 = High) |
| `PH` | Mean soil pH for that treatment combination |

### How it was created

- N, P, K values split into **Low/High** using their **median** as cutoff
- Mean pH calculated for each of the **8 treatment combinations**
- This forms the **2³ Full Factorial Design table**

### Median Cutoffs Used

| Factor | Median (Cutoff) |
|---|---|
| `N` | 37.0 |
| `P` | 51.0 |
| `K` | 32.0 |
