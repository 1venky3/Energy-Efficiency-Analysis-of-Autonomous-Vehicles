# Energy Efficiency Analysis of Autonomous Vehicles
### A Machine Learning Project | Data Analytics Assignment

---

## 📌 Project Overview

This project analyzes how vehicle parameters — **Speed**, **Acceleration**, and **Distance** — affect energy consumption in autonomous electric vehicles. A **Linear Regression** model is built to predict energy usage, and results are compared with a **Random Forest** model.

**Model Performance:**
- R² Score: **0.9789** (explains 97.89% of variance)
- RMSE: **4.05 kWh** (average prediction error)

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `energy_efficiency_av.py` | Main Python ML script (data gen, EDA, model, plots) |
| `ev_dataset.csv` | Generated synthetic dataset (150 rows) |
| `ev_analysis_plots.png` | Visualization output (4 plots) |
| `EV_Energy_Analysis_Report.docx` | Full academic report (10 pages) |
| `EV_Energy_Analysis_Presentation.pptx` | Slide deck (10 slides) |
| `README.md` | This file |

---

## ⚙️ Requirements

Install the required Python libraries using pip:

```bash
pip install pandas numpy matplotlib scikit-learn
```

**Python Version:** 3.8 or higher recommended.

---

## 🚀 How to Run

**Step 1:** Navigate to the project folder
```bash
cd path/to/project-folder
```

**Step 2:** Run the main Python script
```bash
python energy_efficiency_av.py
```

**What happens when you run it:**
1. A synthetic dataset (`ev_dataset.csv`) is generated with 150 rows
2. Data is loaded, checked for missing values, and summarized
3. Features (X) and target (y) are separated
4. Data is split 80% training / 20% testing
5. A Linear Regression model is trained
6. A Random Forest model is trained for comparison
7. Both models make predictions on test data
8. RMSE and R² Score are calculated and printed
9. 4 plots are saved as `ev_analysis_plots.png`
10. A summary of what the model learned is printed

---

## 📊 Dataset Description

The dataset is synthetically generated using EV physics:

| Column | Type | Description |
|--------|------|-------------|
| `Speed` | float | Vehicle speed in km/h (range: 20–120) |
| `Acceleration` | float | Rate of speed change in m/s² (range: 0.5–4.0) |
| `Distance` | float | Trip distance in km (range: 5–100) |
| `Energy_Consumed` | float | Total energy used in kWh **(target variable)** |

**Generation Formula:**
```
Energy = 0.15×Speed + 2.5×Acceleration + 0.8×Distance + 0.003×Speed² + noise
```

---

## 📈 Expected Output

```
============================================================
  ENERGY EFFICIENCY ANALYSIS OF AUTONOMOUS VEHICLES
============================================================

✅ Synthetic dataset generated and saved as 'ev_dataset.csv'

--- STEP 1: DATA LOADING ---
Dataset Shape: 150 rows x 4 columns

--- STEP 2: DATA PREPROCESSING ---
✅ No missing values found. Dataset is clean!

--- STEP 3: TRAIN-TEST SPLIT ---
Training samples : 120
Testing  samples : 30

--- STEP 4: MODEL BUILDING ---
✅ Linear Regression model trained successfully!

Model Coefficients:
  Speed          : 0.5582
  Acceleration   : 2.2463
  Distance       : 0.7911
  Intercept      : -10.2506

--- STEP 6: MODEL EVALUATION ---
Model                    RMSE    R² Score
Linear Regression      4.0524    0.9789
Random Forest          5.4167    0.9624

✅ Excellent fit! The model performs very well.

--- STEP 7: GENERATING VISUALIZATIONS ---
✅ Visualizations saved as 'ev_analysis_plots.png'
```

---

## 🔍 Key Findings

1. **Acceleration** is the most energy-intensive factor (+2.25 kWh per m/s²)
2. **Distance** has a consistent linear cost (+0.79 kWh per km)
3. **Speed** adds +0.56 kWh/km/h + quadratic aerodynamic drag at high speeds
4. **Best driving strategy:** Moderate speed (60–80 km/h) + gentle acceleration

---

## 📚 Libraries Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations and data generation |
| `matplotlib` | Creating visualizations and plots |
| `scikit-learn` | ML models, train-test split, evaluation metrics |

---

## 🎓 Academic Use

This project is designed for academic submission. All code is:
- Fully commented and beginner-friendly
- Ready to run without modification
- Reproducible (fixed random seed: 42)

---

## 📞 Troubleshooting

**Problem:** `ModuleNotFoundError: No module named 'sklearn'`
**Fix:** Run `pip install scikit-learn`

**Problem:** Plot window doesn't open
**Fix:** The plot is saved as `ev_analysis_plots.png` — open it directly from your file explorer.

**Problem:** Permission denied when saving files
**Fix:** Run the script from a folder where you have write permissions.

---

*Energy Efficiency Analysis of Autonomous Vehicles | Data Analytics Assignment | 2024–2025*
