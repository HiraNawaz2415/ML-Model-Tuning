# ML-Model-Tuning
 
 
## What is Hyperparameter Tuning?
   **Hyperparameters = settings you choose before training.**

Examples:

- K in KNN

-  Tree depth in Decision Trees

-  C & gamma in SVM

**Tuning = find which settings work best for your data.*

## Two main ways

## 1.Grid Search:

-  Try all possible combinations in your grid.

-  Best when you have few options.

-  Can be slow for big grids.

## 2.Randomized Search:

-  Pick random combinations from your grid.

-  You control how many to test (n_iter).

-  Faster for large grids.

-  Both use cross-validation inside to test each combo!


## How tuning applies to each algorithm

#### 1. KNN
- Hyperparameter: n_neighbors (k)

- Grid Search: Try all values: [1, 3, 5, 7, 9]

- Randomized Search: Randomly pick k values from a wider range.

#### 2.Decision Tree
- Hyperparameters:

max_depth

min_samples_split

criterion (gini, entropy)

- Grid Search:

Try all combos, e.g., max_depth from 2 to 10, min_samples_split from 2 to 5.

- Randomized Search:

Randomly sample depth and split values.

#### 3.Random Forest
- Hyperparameters:

n_estimators (number of trees)

max_depth

max_features (sqrt, log2, auto)

- Grid Search:

Try all combos of n_estimators and max_depth.

- Randomized Search:

Pick random combos from wide ranges.

#### 4.Linear Regression (with Regularization)
- Hyperparameter:

alpha (Ridge/Lasso)

- Grid Search:

Try alpha = [0.01, 0.1, 1, 10].

- Randomized Search:

Random alpha values in a range.

#### 5.SVM
- Hyperparameters:

C (regularization strength)

kernel (linear, poly, rbf)

gamma (for rbf/poly)

- Grid Search:

All combos of C, kernel, and gamma.

- Randomized Search:

Random combos of C and gamma values.

#### 6. DBSCAN
- Hyperparameters:

eps (neighborhood radius)

min_samples (points to form cluster)

Note: DBSCAN is unsupervised, so no classic GridSearchCV —






