The following is required to run this project.  All packages can be installed via Anaconda and pip.
xgboost and keras are not included with Anaconda.  These can be easily installed via the following commands:
- pip install xgboost
- pip install keras

The 'input' directory should be populated with the following files.  These can be
downloaded from https://www.kaggle.com/c/talkingdata-mobile-user-demographics/data
- app_events.csv
- events.csv
- sample_submission.csv
- app_labels.csv
- phone_brand_device_model.csv
- gender_age_train.csv
- gender_age_test.csv
- label_categories.csv

Project directory:
- Notebook1.ipynb contains the bulk of my work, it includes:
- Data exploration and preprocessing
- First level model training (xgboost, neural nets, and logistic regression)
- Time/location feature engineering
- Second level (stacked) model training (incorporating output from first models, and engineered features)
- Feature blending (arithmetic, geometric, and harmonic means)
- Notebook2.ipynb contains the code supporting my highest scoring submissions.  I found that my first model(s) (from Notebook1) was overly complex, Notebook2 simplifies applying lessons learned.
- ‘Leak_exploit_incomplete.py’ provides incomplete code I wrote in an attempt to take advantage of a data leak that was disclosed in the final days of the competition.  I did not have enough time to complete my implementation, unfortunately.  
- Readme.md provides info on the utilized packages
- The ‘input’ directory contains all of the files provided to competition participants, unaltered
- The ‘output’ directory (left empty to save space in my submission) is where my prediction/submissions are written
- The ‘preprocessed’ directory contains CSVs of features I engineered.  They took a long time to process, so the notebooks I submitted load the features from CSVs instead of processing them fresh (the feature processing code is provided, but is commented-out)