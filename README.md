# -Fake-News-prediction

This repository contains a machine learning model that predicts whether a news article is real or fake. The model uses Natural Language Processing (NLP) techniques and logistic regression to classify news articles based on their content.

# # Overview # #
The project is built using Python and several libraries, including scikit-learn, pandas, and nltk. The dataset used consists of news articles, including their titles, authors, and text content, labeled as real or fake. The model is trained to distinguish fake news from real news by analyzing the content of these articles.

## Dataset
The dataset consists of 20,800 news articles with the following features:

id: Unique identifier for each article.
title: The title of the article.
author: The author of the article.
text: The content of the article.
label: Indicates whether the news is real (0) or fake (1).

 ## Preprocessing
The following preprocessing steps are applied to the dataset:

Handling Missing Values: Missing values in the title, author, or text columns are filled with empty strings.
Combining Features: The author and title columns are combined to form a new feature named content.
Text Cleaning and Stemming:
Removing non-alphabetic characters.
Converting all text to lowercase.
Removing stopwords (common words that do not contribute much to meaning).
Applying stemming to reduce words to their root form.

 ## Model Training
The model uses the following steps for training:

Vectorization: The TfidfVectorizer is used to convert the processed text data into numerical features.
Splitting the Dataset: The data is split into training and testing sets with an 80/20 ratio.
Training the Model: A logistic regression model is trained on the training set.


## Evaluation
The model is evaluated using the accuracy score on both the training and testing datasets:

Training Accuracy: ~98.6%
Testing Accuracy: ~97.9%

## Prediction
The model can predict whether a new piece of text is real or fake news.

To use the prediction function:
Pass the input text through the text preprocessing steps.
Transform the processed text using the trained TfidfVectorizer.
Use the trained logistic regression model to make a prediction
