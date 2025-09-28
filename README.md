# Predicting Phycocyanin Purity Using Machine Learning  

This repository contains the code, analysis, and results for my research project on predicting the **phycocyanin purity** of four cyanobacteria samples based on extraction parameters.  
The project compares multiple machine learning regression models and demonstrates that ensemble methods can predict purity with accuracy comparable to experimental reproducibility.  

---

## Dataset  
The dataset was obtained from:  
Pispas, K., Tzovenis, I., Aggelopoulos, T., & Chatzikonstantinou, M. (2024).  
*A comparative study of freeze–thaw cycling with various cell disruption methods for the extraction of phycocyanin from wet biomass of four cyanobacteria species.*  
**Marine Drugs, 22(3), 111.** [https://doi.org/10.3390/md22030111](https://doi.org/10.3390/md22030111)  

- License: **Creative Commons Attribution (CC BY 4.0)**  
- Reported values: mean ± experimental uncertainty (maximum ±0.35).  

---

## ⚙️ Methods  
Six regression models were implemented using scikit-learn and XGBoost:  
- Linear Regression  
- Ridge Regression  
- LinearSVR  
- RBF-SVR  
- RandomForest Regressor  
- XGBoost Regressor  

Performance was evaluated using:  
- R² (coefficient of determination)  
- MAE (mean absolute error)  
- RMSE (root mean squared error)
- NMAE (negative mean absolute error)
- NRMSE (negative root mean squared error)

---

##  Results  
| Model              | R²   | MAE   | RMSE  |
|--------------------|------|-------|-------|
| Linear Regression  | 0.493 | –     | –     |
| Ridge Regression   | 0.493 | –     | –     |
| LinearSVR          | 0.499 | –     | –     |
| RBF-SVR            | 0.691 | –     | –     |
| RandomForest       | 0.909 | 0.058 | 0.094 |
| XGBoost            | 0.913 | 0.058 | 0.092 |

- Ensemble methods (RandomForest, XGBoost) achieved **MAE ≈ 0.058**, well below the maximum experimental uncertainty (±0.31).  
- Predictions were effectively as reliable as laboratory measurements.  

---

## Figures  
- **Predicted vs Actual Purity (RandomForest & XGBoost)**  
- **Feature Importance (RandomForest & XGBoost)**  

*(See `figures/` folder for plots.)*  

---

## Usage  
Clone the repository and install requirements:  

```bash
git clone https://github.com/yourusername/phycocyanin-ml.git
cd phycocyanin-ml
pip install -r requirements.txt
