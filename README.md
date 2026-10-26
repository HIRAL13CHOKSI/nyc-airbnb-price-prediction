# New York City Airbnb Price Prediction

**Python · pandas · scikit-learn · regression · model evaluation**

How can listing characteristics help explain variation in New York City Airbnb prices? This project explores 2019 listing data and develops regression models to estimate price from location, room type, availability, and other listing features.

**Project type:** Course programming assignment  
**Notebook:** [Explore the original analysis](notebooks/nyc_airbnb_original.ipynb)

## What the analysis covers

- Explore listing prices and relationships with geographic and listing features.
- Prepare numeric and categorical variables using median imputation, scaling, and one-hot encoding.
- Compare linear regression, decision trees, and random forest regression using mean absolute error (MAE).
- Tune a random forest using cross-validation and assess predictions on a held-out test set.
- Examine feature importance and prediction errors.

## Dataset and features

The original analysis reads a local file named `AB_NYC_2019_1.csv`. It uses NYC Airbnb listing data from 2019; the dataset is not included in this repository. A [similarly named 2019 NYC Airbnb dataset on Kaggle](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data) may be suitable, but the exact match with the file used in the notebook has not yet been confirmed.

Features used include neighbourhood group, room type, latitude, longitude, minimum nights, review counts, reviews per month, host listing count, and annual availability. Price is the prediction target.

## Results in the saved notebook

The original notebook reports a **held-out test MAE of approximately 64.08** in the dataset's price units for the selected random forest. This is a saved notebook result and has not yet been independently reproduced.

For context, the notebook records a mean cross-validation MAE of about 74.53 for linear regression and 67.47 for an initial random forest. These are different evaluation stages and should not be treated as a direct comparison with the held-out result.

## Interpretation and current limitations

- The analysis uses a random 80/20 train/test split. Although a notebook heading calls it stratified, the displayed split does not specify stratification.
- The preprocessing pipeline is fitted to the full training set before cross-validation. A future revision should place preprocessing and the estimator in one pipeline so preprocessing is refit within each fold.
- The dataset used in the original run must be checked against the linked candidate before the analysis can be reproduced.
- The notebook contains the original course instructions and exploratory work. Package versions and a clean rerun remain to be verified.

## Running the original notebook

1. Obtain the 2019 NYC Airbnb CSV used in the analysis and place it next to the notebook as `AB_NYC_2019_1.csv`.
2. Open [the notebook](notebooks/nyc_airbnb_original.ipynb) in Jupyter or Google Colab.
3. Install the Python packages used in the notebook, including pandas, NumPy, matplotlib, and scikit-learn, then run the cells in order.

Exact dependency versions and the match to the original dataset are still being established.

## Skills demonstrated

Data exploration · preprocessing · regression · cross-validation · hyperparameter search · feature importance · error analysis

Originally developed as a course assignment and presented here as part of Hiral Choksi's data science portfolio.
