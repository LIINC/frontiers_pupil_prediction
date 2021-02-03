# Pupil Diameter Prediction with LSTM Architecture

Working version on Google Cloud

## Data Processing
1. Uses raw data from the eyelink eye tracker, with classifications (blinks, saccades, fixations, etc.),
1. Designs areas of interest (AOIs) to map fixation data
**Script file:** scripts/process_raw_data.ipynb

## BiLSTM network setup with areas of interest (AOIs) 
1. Uses all classified data in a sequence model,
1. Generates embedding from AOI sequences per trial (learned on training data, fixed for test),
1. Splits and logs test performance,
1. Aggregates performance from BiLSTM in addition to some off-the-shelf models.


## Analysis
1. Compares BiLSTM performance, with and without AOI, with off-the shelf models,
1. Correlates performance data from participant demographic surveys with model accuracy and residuals,
1. t-SNE plots of embeddings for similarity analysis.
