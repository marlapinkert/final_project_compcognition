# GitHub respository for our final project :)

## Contents
- download_and_correlation_df.ipynb - calculate connectivity and download data
- random_forrest_with_data.ipynb - random forrest classifier (work in progress)

## Data
From Autism Brain Imaging Data Exchange (ABIDE)
- Downloaded from https://github.com/preprocessed-connectomes-project/abide using their download_abide_preproc.py script (see /resources)
- Craddock 200, CC200 timeseries 
- CPAC → Worked best in classification for Chen et al. 2018
- See download_and_correlation_df.ipynb
- Download dataframe: https://ucloud.univie.ac.at/index.php/s/W8qTeS8m6F33twT 

## Functional Connectivity
- Calculate partial correlations
- Create dataframe with 884 rows (subjects) and 19901 columns (correlations between timeseries)
- See download_and_correlation_df.ipynb

## Random Forrest
- random_forrest_with_data.ipynb: Simple rf classifier, some attempts at plotting
