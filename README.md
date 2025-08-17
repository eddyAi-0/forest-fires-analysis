# Forest Fires Analysis (UCI Dataset)

This project analyzes the **Forest Fires dataset** from the UCI Machine Learning Repository.  
The goal is to explore the data, evaluate correlations, and build predictive models to estimate the burned area.

---

## Dataset
- Source: [UCI Machine Learning Repository – Forest Fires](https://archive.ics.uci.edu/ml/datasets/forest+fires)
- Size: 517 observations, 12 features
- Target: `area` (burned area of the forest, in hectares)

---

## Methodology
1. **Exploratory Data Analysis (EDA)**
   - Distribution of the burned area (highly skewed, most values are 0)
   - Correlation matrix of meteorological and environmental variables
   - Temporal and spatial patterns (month, day of week, coordinates X-Y)

2. **Feature Engineering**
   - Log transformation of the `area` target variable
   - Scaling and normalization of features

3. **Modeling**
   - Regression models: Linear Regression, Random Forest, etc.
   - Classification models: Logistic Regression, Decision Trees

4. **Evaluation**
   - Regression metrics: MAE, RMSE, R²
   - Classification metrics: Confusion matrix, Accuracy, Precision, Recall

---

## Results
- **Correlation analysis** showed very weak relationships between predictors and burned area.
- **Regression models** struggled:  
  - RMSE remained high due to skewed distribution  
  - log-transformed target improved stability but limited predictive power
- **Classification models** performed better in distinguishing between "small" and "large" fires, but dataset imbalance reduced accuracy.  
- Example visualization (see `/imgs/` folder for details):  
  - Correlation matrix  
  - Confusion matrix  
  - Burned area distribution  

---

## Limitations
- Dataset is small (517 rows) and highly imbalanced (most fires are negligible).  
- Meteorological features are not sufficient to capture fire dynamics.  
- Models are more **didactic** than **practical**.

---

## Repository Content
- `UCI_Fires_Project.ipynb`: full analysis notebook  
- `imgs/`: visualizations (correlation matrix, confusion matrix, maps, etc.)  
- `README.md`: project documentation  

---

## How to Run
```bash
git clone https://github.com/eddyAi-0/forest-fires-analysis.git
cd forest-fires-analysis
jupyter notebook UCI_Fires_Project.ipynb
