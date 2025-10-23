Artificial Intelligence — Text Cleaning and Sentiment Analysis

This repository contains the AI coursework and NLP text cleaning tasks performed in Google Colab.
The focus is on data preprocessing, sentiment classification, and preparing datasets for natural language processing models.


Project Overview

This project demonstrates how sentiment-based text datasets were cleaned, analyzed, and visualized using Python.
The datasets include IMDB Movie Reviews and Twitter Airline Sentiment data, both used to study how people express opinions through text.


Files in this Repository

File Name:                 Description
--------------------------------------------------------------------
cleaned_imdb.csv           Cleaned IMDB dataset containing movie reviews labeled as positive or negative
cleaned_twitter_airline.csv Cleaned Twitter dataset with airline-related tweets labeled by sentiment
Links Google Collab         Reference links to Google Colab notebooks used for text cleaning and analysis
README.md                   Documentation describing datasets, steps, and results


Data Cleaning Workflow

All text preprocessing was done using Python (pandas, regex, tqdm) in Google Colab.

Steps Performed:
1. Removed HTML tags, URLs, mentions, emojis, and punctuation
2. Converted all text to lowercase and normalized extra spaces
3. Removed duplicate or empty rows
4. Added a word count column for each review or tweet
5. Saved final cleaned datasets in CSV format


Exploratory Data Analysis (EDA)

Each dataset was analyzed for:
- Word count distributions
- Sentiment distribution (positive, negative, neutral)
- Duplicate and missing values
- Random before/after samples to verify text cleaning results


Output Datasets

After cleaning, the following files were generated:

Dataset Name             Records   Columns   Output File
-------------------------------------------------------------------
IMDB Movie Reviews        50,000    3         cleaned_imdb.csv
Twitter Airline Sentiment 14,640    3         cleaned_twitter_airline.csv


Key Insights

- IMDB dataset contains long-form reviews, useful for sentiment and opinion mining.
- Twitter dataset includes short messages with mixed emotions, ideal for classification tasks.
- Cleaned data is balanced and ready for model training, visualization, or AI-based sentiment prediction.


Tools and Libraries Used

Python 3.10+
Pandas - data manipulation
Regex (re) - text normalization
Matplotlib - plotting graphs
tqdm - progress tracking
Google Colab - execution environment


Example Colab Snippet

import pandas as pd, re

df = pd.read_csv("/content/IMDB Dataset.csv")
df['clean_review'] = df['review'].str.lower()
df['clean_review'] = df['clean_review'].str.replace(r'http\S+|www\S+', '', regex=True)
df = df.drop_duplicates().dropna()
print("Shape after cleaning:", df.shape)
df.to_csv("/content/cleaned_imdb.csv", index=False)


Google Colab Links

All notebooks used in this project are listed in the file named: Links Google Collab


Author

Your Friend's Name
Artificial Intelligence Coursework
October 2025
Tools: Google Colab, Python, GitHub


License

This repository is for educational and research purposes only.
All datasets belong to their original creators (Kaggle, IMDB, and Twitter).
