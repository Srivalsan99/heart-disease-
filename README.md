# Heart Disease Classification

Classification of heart disease from patient data, using Python (pandas, NumPy, scikit-learn, XGBoost, Seaborn, Matplotlib). The notebook scales the features and compares several classifiers, then tunes a random forest.

## Dataset

`heart.csv`: 303 patient records, 13 features and a binary `target` (1 = heart disease present, 0 = not). Features: `age`, `sex`, `cp` (chest pain type), `trestbps` (resting blood pressure), `chol` (cholesterol), `fbs` (fasting blood sugar), `restecg`, `thalach` (maximum heart rate), `exang` (exercise-induced angina), `oldpeak`, `slope`, `ca` and `thal`. About 54% of records have `target = 1`.

Source: [add the dataset link here, e.g. the UCI or Kaggle page you downloaded it from]. Check the column meanings against that source.

## What the notebook does

1. **Explore:** loads the data, checks summary statistics, and plots a correlation heatmap.
2. **Prepare:** separates the features from `target`, standardises the features (`StandardScaler`), and splits the data 80/20 into train and test sets (61 test records).
3. **Compare classifiers** on the test set, with a classification report and confusion matrix for each:

| Model | Test accuracy |
|---|---|
| K-nearest neighbours | **85.2%** |
| AdaBoost | 83.6% |
| XGBoost | 80.3% |
| Random forest (tuned, depth 19) | 80.3% |
| Decision tree | 77.0% |
| Random forest (default) | 75.4% |

4. **Tune:** a 5-fold grid search over random forest depth (1 to 29, 800 trees).

## Tools

Python, pandas, NumPy, scikit-learn, XGBoost, Seaborn, Matplotlib, Google Colab / Jupyter.

## Limitations and next steps

- The test set is small (61 records), so differences of a few percentage points are not reliable. Cross-validation across all models would be better.
- The features are scaled before the train/test split. Fitting the scaler on the training data only would avoid leaking test information.
- For a medical problem, recall on the positive class matters as much as accuracy.

## How to run

1. Open `heart_disease_data_set.ipynb` in Google Colab or Jupyter.
2. Upload `heart.csv` when prompted (or place it in the same folder).
3. Run the cells in order.
