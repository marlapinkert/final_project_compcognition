# A Random Forest Classifier for ASD based on Resting-State Functional Connectivity
### *Final Project in Theory and Empirical Research I, supervisors: Dominik Pegler, Mengfan Zhang, Jozsef Arato* 
Jannis Breßgott, Sara Binder, Marla Pinkert

This is the repository for our final project :)

## Contents
- RF_for_ASD.ipynb.ipynb - Complete Notebook, includes download of data, calculation of functional connectivity measures, training and testing of random forest classifiers, discussion of results.
- Phenotypic_V1_0b_preprocessed1.csv - Contains phenotypical data such as diagnosis ("DX_GROUP", with 1 = Autism, 0 = Control)
- degree_df.csv - Contains dataframe with rows corresponding to individual subjects and columns corresponding to degree of respective ROIs
- graph_df.csv - Contains dataframe with rows corresponding to individual subjects and columns corresponding to betweenness centrality of respective ROIs

The .csv file which contains the individual correlations between regions is too big to upload, therefore it can be downloaded here: https://ucloud.univie.ac.at/index.php/s/jKogT2Npszs35RT 

## Data
From Autism Brain Imaging Data Exchange (ABIDE), downloaded using download_abide_preproc.py script (see /resources). https://github.com/preprocessed-connectomes-project/abide 
Preprocessed data chosen:
- Atlas: Craddock 200, CC200 timeseries 
- Pipeline: CPAC → Worked best in classification for Yang et al. (2020) https://doi.org/10.14569/IJACSA.2020.0110401 

## Functional Connectivity
- Calculate correlations between different ROIs
- Create dataframes with 884 rows (subjects) and 19901 columns (19900 correlations between timeseries + 1 "FILE_ID")

## Graph Theoretical Measures
- Calculate betweenness centrality based on proportional thresholds (70% - 90% in steps of 2)
- Calculate degree based on non-binarized connections, including negative correlations
