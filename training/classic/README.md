Here you can find notebooks for the study of processed dataset by means of classic machine learning models.

**How to use notebooks**:
1. just follow the notebook
2. if required you may replace model hyperparameters with those ones from `optuna_classic_ml.ipynb`
3. if required you may change dataset downloaded in the beginning of notebooks (right afther library import)

## Classic ML (`main_classic_ml.ipynb`)
Here `Random Forest Regressor`, `TabNet Regressor` and `XGBoost Regressor` are trained and compared by MSE and R2 metrics. Also, computation time is estimated. Finally, experimental device paratemeters are input into `XGBoost Regressor` obtaining relative error for resonant frequency (1st mode) calculation $\sim 2$%. Also, `Linear Regressor` is trained to show a baseline.

## Cross validation (`cross_validation.ipynb`)
Here custom cross-validation is performed. Visualizations of metrics on all folds are obtained. See instructions in the notebook.

## Optuna classic ml (`optuna_classic_ml.ipynb`)
Hyperparameter tuning of `Random Forest Regressor`, `TabNet Regressor` and `XGBoost Regressor` by means of `Optuna`.

## Shap classic ml (`shap_classic_ml.ipynb`)
Explaining `XGBoost Regressor` model outputs by means of SHAP values.
