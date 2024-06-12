# GitHub respository for our final project :)

## Contents
- download_and_correlation_df.ipynb - calculate connectivity and download data
- random_forrest_with_data.ipynb - random forrest classifier (work in progress)

## Data
From Autism Brain Imaging Data Exchange (ABIDE)
- Downloaded using download_abide_preproc.py script (see /resources). Source: https://github.com/preprocessed-connectomes-project/abide 
- Craddock 200, CC200 timeseries 
- CPAC → Worked best in classification for Chen et al. 2018
- See download_and_correlation_df.ipynb
- Download dataframe: https://ucloud.univie.ac.at/index.php/s/W8qTeS8m6F33twT 

## Functional Connectivity
- Calculate correlations and partial correlations
- Create dataframes with 884 rows (subjects) and 19901 columns (19900 correlations between timeseries + 1 Identifier)
- See download_and_correlation_df.ipynb

## Random Forrest
- random_forrest_with_data.ipynb: Simple rf classifier, some attempts at plotting

## Next possible steps:
- Cross validation - maybe OBB?
- Exclude features with importance = 0? -> 4300 would remain, 15600 are removed
- Hyperparameter testing: perhaps use sklearn.model_selection.RandomizedSearchCV

## Further things that might be interesting
- Classify different autism diagnoses?
- CC400 timeseries: Much more data, but finer parcellation might make for a better predictor
- Compare RF Model with other models?
