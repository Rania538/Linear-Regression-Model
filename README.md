# California Housing Price Prediction

A Machine Learning project that uses **Linear Regression** to predict median house values in California districts based on demographic, housing, and geographical features.

## Project Overview

The goal of this project is to build and evaluate a supervised regression model using the California Housing dataset.

The project covers the main stages of a Machine Learning workflow, starting with data exploration and ending with model evaluation and residual analysis.

## Dataset

- **Dataset:** California Housing
- **Source:** `sklearn.datasets.fetch_california_housing`
- **Number of observations:** 20,640
- **Number of features:** 8
- **Target variable:** `MedHouseVal`

### Features

| Feature | Description |
|---|---|
| `MedInc` | Median income in the district |
| `HouseAge` | Median house age |
| `AveRooms` | Average number of rooms |
| `AveBedrms` | Average number of bedrooms |
| `Population` | District population |
| `AveOccup` | Average household occupancy |
| `Latitude` | Geographic latitude |
| `Longitude` | Geographic longitude |

**Target:** `MedHouseVal` represents the median house value, measured in units of $100,000.

## Technologies & Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Data Loading & Understanding
- Loaded the California Housing dataset.
- Converted the dataset into a Pandas DataFrame.
- Inspected the dataset using `head()`, `tail()`, `shape`, `info()`, and `describe()`.

### 2. Exploratory Data Analysis (EDA)
- Analyzed missing values and duplicate records.
- Examined numerical feature distributions.
- Visualized the target variable distribution.
- Performed univariate and bivariate analysis.
- Created scatter plots to investigate feature-target relationships.
- Used a correlation matrix and heatmap to examine linear relationships.
- Investigated extreme values using the IQR method.

### 3. Data Preprocessing
- Separated input features (`X`) from the target (`y`).
- Split the dataset into training and testing sets.
- Applied `StandardScaler` through a Scikit-learn Pipeline to prevent data leakage.

### 4. Model Building
- Implemented a Linear Regression model using Scikit-learn.
- Combined feature scaling and model training using `make_pipeline()`.
- Examined the learned coefficients and intercept.

### 5. Model Evaluation

Evaluated the model on the test set using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### 6. Model Diagnostics
- Actual vs. Predicted plot.
- Residual distribution.
- Residuals vs. Predicted values.

These visualizations help assess prediction errors and identify potential patterns that the model may not capture.

## Results

Test set performance:

| Metric | Score |
|---|---:|
| MAE | 0.5332 |
| MSE | 0.5559 |
| RMSE | 0.7456 |
| R² Score | 0.5758 |

The model achieved an R² score of approximately **0.576**, meaning it explains around 57.6% of the variance in the target variable on the test set.

Since the target is measured in units of $100,000, the MAE corresponds to approximately **$53,320**.

## Key Findings

- `MedInc` showed the strongest positive linear correlation with the target variable.
- The target distribution contains a noticeable upper-value cap.
- Some features exhibit skewed distributions and extreme observations.
- Correlation does not imply causation.
- Linear Regression provides a useful baseline, but it may not capture complex nonlinear relationships in housing data.

## How to Run

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
cd YOUR_REPOSITORY_NAME
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the notebook

Open `LinearRegression.ipynb` and run the cells in order.

The dataset is fetched through Scikit-learn and may require an internet connection on the first download.


## Future Improvements

- Compare Linear Regression with Ridge and Lasso Regression.
- Apply cross-validation for more robust evaluation.
- Investigate nonlinear relationships and feature transformations.
- Explore spatial train-test splitting.
- Compare the baseline model with tree-based regression models.

## Conclusion

This project demonstrates an end-to-end Linear Regression workflow, including data understanding, exploratory analysis, preprocessing, model training, evaluation, and diagnostics.

It serves as a practical foundation for understanding regression problems and building more advanced Machine Learning models.

---

**Project Focus:** Supervised Learning | Regression | Exploratory Data Analysis | Data Preprocessing | Model Evaluation
