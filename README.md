# Heart Disease Dataset: Initial Data Exploration

A first look at a heart disease dataset using Python (pandas, NumPy, Seaborn, Matplotlib). The notebook loads the data and checks its structure and summary statistics, as a starting point for further analysis.

## Dataset

`heart.csv`: 303 patient records with 14 columns.

| Column | Meaning |
|---|---|
| `age` | Age in years |
| `sex` | Sex (1 = male, 0 = female) |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol |
| `fbs` | Fasting blood sugar above 120 mg/dl (1 = yes) |
| `restecg` | Resting ECG result |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina (1 = yes) |
| `oldpeak` | ST depression during exercise |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels (0 to 3) |
| `thal` | Thalassemia result |
| `target` | Heart disease present (1) or not (0) |

Source: [add the dataset link here, e.g. the UCI or Kaggle page you downloaded it from]. Column meanings follow the standard description of this dataset, so check them against your source.

## What the notebook does

1. Loads `heart.csv` with pandas.
2. Previews the first rows (`head()`).
3. Produces summary statistics for all columns (`describe()`). All 14 columns have 303 values, and about 54% of records have `target = 1`.

## Tools

Python, pandas, NumPy, Seaborn, Matplotlib, Google Colab / Jupyter.

## Status and next steps

This is an early-stage exploration. Planned next steps:

- Check for missing values and duplicates.
- Plot distributions and compare features by `target`.
- Scale the numeric features.
- Train a simple classifier (for example logistic regression) and report accuracy.

## How to run

1. Open `heart_disease_data_set.ipynb` in Google Colab or Jupyter.
2. Upload `heart.csv` when prompted (or place it in the same folder).
3. Run the cells in order.
