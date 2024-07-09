# A Random Forest Classifier for ASD based on Resting-State Functional Connectivity
### *Final Project in Theory and Empirical Research I, supervisors: Dominik Pegler, Mengfan Zhang, Jozsef Arato* 
Jannis Breßgott, Sara Binder, Marla Pinkert

This is the repository for our final project :)

## Contents
- RF_for_ASD.ipynb.ipynb - Complete Notebook, includes download of data, calculation of functional connectivity measures, training and testing of random forest classifiers, discussion of results.
- Phenotypic_V1_0b_preprocessed1.csv - Contains phenotypical data such as diagnosis ("DX_GROUP", with 1 = Autism, 0 = Control)
- degree_df.csv - Contains dataframe with rows corresponding to individual subjects and columns corresponding to degree of respective ROIs
- graph_df.csv - Contains dataframe with rows corresponding to individual subjects and columns corresponding to betweenness centrality of respective ROIs


## Data
From Autism Brain Imaging Data Exchange (ABIDE)
- Downloaded using download_abide_preproc.py script (see /resources). https://github.com/preprocessed-connectomes-project/abide 
- Craddock 200, CC200 timeseries 
- CPAC → Worked best in classification for Yang et al. (2020) https://doi.org/10.14569/IJACSA.2020.0110401 
- Download dataframe: https://ucloud.univie.ac.at/index.php/s/W8qTeS8m6F33twT 

## Functional Connectivity
- Calculate correlations
- Create dataframes with 884 rows (subjects) and 19901 columns (19900 correlations between timeseries + 1 "FILE_ID")
- See download_and_correlation_df.ipynb

## Next possible steps:
- Cross validation - maybe OBB?
- Exclude features with importance = 0? -> 4300 would remain, 15600 are removed
- Hyperparameter testing: perhaps use sklearn.model_selection.RandomizedSearchCV

## Further things that might be interesting
- CC400 timeseries: Much more data, but finer parcellation might make for a better predictor
