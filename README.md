# PNI Gene Expression Classifier 

## Objective - Assess effectiveness of Random Forest and XGBoost for predicting PNI 


## Model Exploration
Model exploration was done using the Dataiku AutoML platform with the cleaned input data generated from the preprocessing notebooks. The best model (Random Forest) is evaluated with the notebooks in this repository. 

## Datasets 

1. **PNI_001_cleaned.csv** - preprocessed dataset which is the input for model

2. **PNI_001_features_raw.csv** - raw gene data (no labels)

3. **PNI_001_labels.csv** - raw PNI binary labels 

4. **unannotated_scored_pni001.csv** - unannotated dataset for model scoring


## Notebooks 

1. **pni_data_preprocessing** - converts raw features and labels into cleaned data for modeling (row = patients, columns = genes)

2. **pni_randomforest_xgboost_crossvalidation.ipynb** - initial cross validation study to confirm autoML results

3. **pni_randomforest_sfs.ipynb** - sequential feature selector study for random forest

4. **pni_randomforest_cross_validation.ipynb** - cross validation for random forest model (chosen model). deep dive into metrics

5. **pni_randomforest_predict_unscored.ipynb** - scoring the unannotated dataset for model evaluation by external subject matter experts


## Python Dependencies 

Python version > 3.4
* scikit-learn
* xgboost
* pandas
* numpy
* matplotlib
* seaborn 
* mlxtend