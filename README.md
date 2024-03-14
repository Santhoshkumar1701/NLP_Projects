# AWS Review Software Analysis

This repository contains Python code for analyzing and modeling the AWS review software dataset. The dataset is loaded using pandas, preprocessed, and then used to train Decision Tree Classifier models with both TF-IDF and Count Vectorization.

## Dataset

The dataset used in this analysis is named `aws_review_sofware_dataset.csv`. It contains the following columns:

- `Unnamed: 0`: Index column
- `overall`: Overall rating
- `verified`: Verification status of the review
- `reviewTime`: Time of the review
- `reviewerID`: ID of the reviewer
- `asin`: Amazon Standard Identification Number
- `style`: Style of the review
- `reviewerName`: Name of the reviewer
- `reviewText`: Text of the review
- `summary`: Summary of the review
- `unixReviewTime`: Unix timestamp of the review time
- `vote`: Number of votes the review received
- `image`: Image associated with the review (if any)

## Preprocessing

The following preprocessing steps are performed on the dataset:

1. Sampling: Randomly select 10,000 samples from the dataset.
2. Handling Missing Values: Check for and handle any missing values in the dataset.
3. Tokenization: Tokenize the review text into sentences and words using NLTK.
4. Lemmatization: Lemmatize the words in the reviews using the PyWSD library.
5. Vectorization: Vectorize the words using TF-IDF Vectorizer and Count Vectorizer from scikit-learn.

## Model Training

Two models are trained using different vectorization techniques:

1. **TF-IDF Vectorization:**
   - A Decision Tree Classifier model is trained using the TF-IDF matrix and the target variable `verified`. The accuracy of the trained model on the training data is approximately 99.69%.

2. **Count Vectorization:**
   - A Decision Tree Classifier model is trained using the Count Vectorizer matrix and the target variable `verified`. The accuracy of the trained model on the training data is approximately 99.46%.
