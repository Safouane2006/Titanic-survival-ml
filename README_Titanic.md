# Titanic Survival Prediction — Machine Learning

A clean end-to-end machine-learning project based on Kaggle's **Titanic - Machine Learning from Disaster** competition.

## Result

**Best Kaggle public leaderboard score achieved during experimentation: 0.80622**

## What the project does

The project predicts whether a Titanic passenger survived using passenger information such as class, sex, age, fare, family relationships, cabin and ticket data.

The workflow includes:

- data loading and inspection
- missing-value analysis
- a Logistic Regression baseline
- feature engineering
- stratified cross-validation
- CatBoost modeling
- probability ensembling
- creation of a Kaggle submission file

## Engineered features

The final model derives additional information from the original dataset:

- passenger title (`Mr`, `Mrs`, `Miss`, `Master`, etc.)
- family size
- whether the passenger traveled alone
- cabin deck and cabin availability
- whether age was missing
- ticket and ticket prefix
- family identifier based on surname and family size
- interaction between sex and passenger class

## Technologies

- Python
- pandas
- NumPy
- scikit-learn
- CatBoost
- Kaggle Notebooks

## Model evaluation

A simple Logistic Regression model is used as a baseline.

The improved model uses CatBoost because it can handle categorical variables effectively. Model quality is checked with stratified 5-fold cross-validation before training on the complete training set.

The final prediction averages the probabilities from two CatBoost models with different tree depths.

## How to run

1. Open the notebook on Kaggle.
2. Attach the **Titanic - Machine Learning from Disaster** competition data.
3. Run all cells.
4. The notebook creates:

```text
/kaggle/working/submission_final.csv
```

5. Submit that file on the Titanic competition page.

## Project structure

```text
Titanic_Survival_Prediction_ML.ipynb
README.md
requirements.txt
```

## CV description

**Titanic Survival Prediction — Kaggle Machine Learning Project**  
Python, pandas, scikit-learn, CatBoost

- Built and evaluated binary-classification pipelines for Titanic survival prediction.
- Engineered family, title, cabin and ticket features and evaluated models with stratified cross-validation.
- Achieved a **0.80622 Kaggle public leaderboard score** during model experimentation.

## Interview explanation

A concise explanation of the project:

> I started with a simple Logistic Regression baseline, then improved the pipeline by engineering features from passenger names, family structure, cabins and tickets. I used stratified cross-validation to compare models and selected a CatBoost ensemble because it handled the categorical features well. I then trained the final models on the complete training set and generated the Kaggle submission.

Be prepared to explain every feature and modeling choice in your own words.
