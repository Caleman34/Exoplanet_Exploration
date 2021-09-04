# Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

The raw data is preprocessed, the models are tunes, and then compared to see which one is more reliable.

---

### Model-1 Random Forest

* Using `MinMaxScaler` resulted in slightly better results versus the `StandardScaler`.
* For feature selection, all of the supplied features are used. It is noticed that a dramatic drop off in accuracy occurs if any features are left out.
* The results are:
  * Training: 0.568
  * Testing: 0.566
* Using `GridSearch` and attempting to tune `n_estimators`, `max_features`, `max_depth`, `min_samples_split`, `min_samples_leaf`, `bootstrap` improved the results to 0.893.

### Model-2 SVM

* Using `MinMaxScaler` resulted in slightly better results versus the `StandardScaler`.
* For feature selection, all of the supplied features are used. It is noticed that a dramatic drop off in accuracy occurs if any features are left out.
* The results are:
  * Training: 0
  * Testing: 0
* Using `GridSearch` and attempting to tune `C` and `gamma` improved the results to 0.608.

## Final analysis

* All of the models, prior to GridSearch, started off at roughly 0.500 which is selecting the correct result half of the time.
* `GridSearch` helped all three models to a greater or lesser degree.
* Random Forest shows the largest benefit from the `GridSearch`, achieving a final score of 0.893. The score significantly beats out the SVM model.
* Random Forest might be a good enough model to predict new exoplanets, but further data analysis is needed for tuning.