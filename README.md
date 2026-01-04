# NLP Disaster Tweets (Kaggle Mini-Project)

This project is based on the Kaggle competition **"Natural Language Processing with Disaster Tweets"**.
The goal is to classify tweets as describing a real disaster (1) or not (0).

## Dataset
The Kaggle dataset contains three files:
- `train.csv`: labeled tweets (includes the `target` column)
- `test.csv`: unlabeled tweets for Kaggle submission
- `sample_submission.csv`: required submission format

Main columns:
- `text`: tweet content
- `keyword`, `location`: optional metadata (may be blank)
- `target`: label in training data (1 = disaster, 0 = not disaster)

## Approach
1. **Exploratory Data Analysis (EDA)**:
   - Inspected dataset structure and missing values
   - Checked class distribution
   - Cleaned missing values in `keyword` and `location`

2. **Baseline model (best performing)**:
   - TF-IDF vectorization (max 5,000 features)
   - Logistic Regression classifier
   - Produced the strongest performance and was used for Kaggle submission

3. **Sequential neural network experiments**:
   - Tokenization + padding
   - Embedding + LSTM models
   - Performed troubleshooting (class weights, longer sequences, cleaner input)
   - In this notebook environment, the LSTM models collapsed to predicting the majority class

## Kaggle Submission
A submission file `submission.csv` was generated and uploaded to Kaggle.

## Repository Contents
- `disaster_tweets_project.ipynb`: full notebook with EDA, modeling, and results

## Reference
Kaggle competition: Natural Language Processing with Disaster Tweets
