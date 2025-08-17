# Analisi incendi UCI
# Forest Fires Analysis (UCI Dataset)

This project analyzes the **Forest Fires dataset** from the UCI Machine Learning Repository.  
The main goal is to explore the data, understand the relationships between meteorological and environmental variables, and build predictive models for the burned area.

---

## Dataset
- Source: [UCI Machine Learning Repository – Forest Fires](https://archive.ics.uci.edu/ml/datasets/forest+fires)
- Size: 517 observations, 12 features
- Target variable: `area` (burned area of the forest, in hectares)

---

## Objectives
1. Perform **exploratory data analysis (EDA)**:
   - Distribution of burned areas
   - Correlation matrix between meteorological variables and the target
   - Visualization of temporal and spatial patterns
2. Apply **feature engineering** (e.g., log transformation of the target, scaling)
3. Train and evaluate different **machine learning models**:
   - Regression models to predict burned area
   - Classification models to predict whether a fire will spread significantly
4. Evaluate results with:
   - Confusion matrix
   - Error metrics (MAE, RMSE, R²)

---

## Results
- **Correlation analysis**: very low correlation between meteorological variables and the burned area, highlighting the complexity of the problem.
- **Model performance**: regression models struggled due to the skewness of the target variable. Applying a log transformation improved results slightly, but predictions remained limited.
- **Classification**: models can roughly distinguish between "small fires" and "large fires", but accuracy is constrained by the dataset imbalance.

---

## Limitations
- The dataset is relatively small and unbalanced (many cases with zero burned area).
- Meteorological variables alone are insufficient to capture the complexity of forest fire behavior.
- Models are useful for educational purposes but not directly applicable to real-world fire prediction.

---

## Repository Content
- `UCI_Fires_Project.ipynb`: Jupyter notebook with the full analysis
- `imgs/`: folder containing visualizations (correlation matrix, confusion matrix, maps, etc.)
- `README.md`: project description

---

## How to Run
Clone this repository and open the notebook:

```bash
git clone https://github.com/eddyAi-0/forest-fires-analysis.git
cd forest-fires-analysis
jupyter notebook UCI_Fires_Project.ipynb
