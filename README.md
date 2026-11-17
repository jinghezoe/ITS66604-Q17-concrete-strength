# Concrete Compressive Strength Prediction (ITS66604, Question 17)

Supervised regression of concrete compressive strength (MPa) from seven mix ingredients and curing age.
The notebook compares Linear Regression, Support Vector Regression (RBF kernel) and Random Forest using
cross-validation grouped by mix recipe, tunes the candidates, and evaluates the selected model on unseen recipes.

## Contents

- `Q17_concrete_strength.ipynb` — full analysis, executed with outputs
- `data/concrete_data.csv` — dataset (1,030 rows, 9 columns)
- `figures/` — figures exported by the notebook

## How to run

```bash
pip install -r requirements.txt
jupyter notebook Q17_concrete_strength.ipynb
```

Run all cells from top to bottom. The notebook reads `data/concrete_data.csv` by relative path and writes figures to `figures/`.
Tested with Python 3.13, scikit-learn 1.9, pandas 2.3, matplotlib 3.11; random seed 42.

## Data source

Kaggle: [Concrete Compressive Strength Data Set](https://www.kaggle.com/datasets/elikplim/concrete-compressive-strength-data-set),
a copy of the UCI dataset donated by Prof. I-Cheng Yeh: Yeh, I-C. (1998). *Concrete Compressive Strength* [Dataset].
UCI Machine Learning Repository, https://doi.org/10.24432/C5PK67 (CC BY 4.0).

Original paper: I-Cheng Yeh, "Modeling of strength of high-performance concrete using artificial neural networks,"
*Cement and Concrete Research*, 28(12), 1797–1808 (1998).
