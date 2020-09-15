# Predicting Heart Disease Rate (PHDR)

## Table of Contents


## Project Overview
The goal is to predict the rate of heart disease (per 100,000 individuals) across the United States at the county-level from other socioeconomic indicators. Data was scraped from the USDA ERS website.

The target column is labeled `heart_disease_mortality_per_100k` which is in the 'Training_labels.csv' file.

For more reference, you can access the original kaggle dataset here: [Predicting heart disease rate](https://www.kaggle.com/nandvard/microsoft-data-science-capstone).

## Project Notebooks
This project consists of four major notebooks:

* [Compressed Notebook](https://github.com/samdomeier/Springboard-projects/blob/master/Predicting_Heart_Disease_Rate/PHDR_compressed_notebook.ipynb)
  > Recommended if you only have a couple of minutes to review this project.

  The compressed notebook contains a shortened version of the "Detailed Notebook". It will include partial EDA, full data wrangling/cleaning, and only the final model with results.
  
* [Detailed Notebook](https://github.com/samdomeier/Springboard-projects/blob/master/Predicting_Heart_Disease_Rate/PHDR_detailed_notebook.ipynb)
  > This is the most advanced notebook if you have the time to review it.

  This notebook contains everything in the "Data Wrangling and EDA" and "Creating the Model" notebooks. It includes every detail you will need to understand how this model was created. From EDA, to feature engineering, to fully detailing the modeling process.
  
* [Data Wrangling and EDA](https://github.com/samdomeier/Springboard-projects/blob/master/Predicting_Heart_Disease_Rate/PHDR_data_wrangling_and_EDA.ipynb)
  > If you are only interested in the data cleaning and feature engineering.

  This will have every step in the "Detailed Notebook" for the feature engineering.

* [Creating the Model](https://github.com/samdomeier/Springboard-projects/blob/master/Predicting_Heart_Disease_Rate/PHDR_creating_the_model.ipynb)
  > If you are only interested in the model creation.

  This will have every step in the "Detailed Notebook" for the model creation.

## Executive Summary
For the final step in my model creation, there were four methods that were considered for hyperparameter tuning. The results can be seen in the table below.

|  | Model Description	| Model Score	| Mean Fit Time (s)	| Std Fit Time |
| --- | --- | --- | --- | --- |
| BR_XGBR	| BaggingRegressor with XGBRegressor	| 0.777075	| 74.660406	| 0.786755 |
| ABR_RFR	| AdaBoostRegressor with RandomForestRegressor	| 0.762149	| 49.474793	| 1.124591 |
| XGBR	| XGBRegressor	| 0.761532	| 3.279330	| 0.118036 |
| GBR	| GradientBoostingRegressor	| 0.753177	| 2.304990	| 0.084161 |

---

The model that I decided to go with uses the `XGBRegressor`. It was the second most efficient model considered, and it had a score considerably close to the top two performing model scores.
