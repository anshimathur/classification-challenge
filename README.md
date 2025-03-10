# Spam Detection Model Comparison

## Goal

The goal of this project is to compare the performance of two machine learning models, **Logistic Regression** and **Random Forest Classifier**, in detecting spam messages using a dataset that includes various email-related features. The goal is to predict whether a given message is spam (labeled as 1) or not spam (labeled as 0), based on a collection of word frequencies and other characteristics.

## Problem

As spam emails become increasingly sophisticated, detecting spam messages requires effective models capable of recognizing patterns in the data. This project uses a **SpamBase** dataset, sourced from the UCI Machine Learning Repository, which contains features representing the frequency of specific words or characters in emails, along with labels that indicate whether the email is spam or not. The problem is to build models that can classify emails as spam or not, based on these features.

## Data

The dataset used in this project contains 4,601 instances, each representing an email, with 57 features corresponding to the frequency of various words and characters. The target variable (`spam`) indicates whether the email is spam (`1`) or not (`0`). The dataset includes features like:
- Word frequencies (e.g., `word_freq_make`, `word_freq_address`, etc.)
- Character frequencies (e.g., `char_freq_;`, `char_freq_(`, etc.)
- Capital letter usage metrics (e.g., `capital_run_length_average`, `capital_run_length_longest`)

### Source

The dataset is sourced from the **UCI Machine Learning Repository**:
- Dataset URL: [SpamBase Dataset](https://archive.ics.uci.edu/dataset/94/spambase)

## Approach

### 1. Data Preparation
- The dataset was imported using Pandas.
- The target variable `spam` was separated from the feature variables to create the labels (`y`) and features (`X`).
- The dataset was split into **training** and **testing** sets using `train_test_split` from Scikit-learn.
- The features were scaled using **StandardScaler** to normalize the data and improve the performance of the models.

### 2. Models
Two models were tested:
- **Logistic Regression:** A linear model used for binary classification.
- **Random Forest Classifier:** An ensemble method that builds multiple decision trees and aggregates their predictions.

Both models were trained on the training dataset, and their accuracy was evaluated on the testing set using the `accuracy_score` function from Scikit-learn.

### 3. Model Performance
- The **Random Forest Classifier** performed better, achieving an accuracy of **95.87%**, compared to the **Logistic Regression** model, which had an accuracy of **92.70%**.
- The Random Forest model showed higher accuracy due to its ability to capture non-linear relationships in the data and handle feature interactions better than the linear Logistic Regression model.

## Findings

- **Random Forests** was well-suited for this type of problem due to the complex and non-linear relationships between the features in the dataset.
- **Logistic Regression**, while still useful for simpler problems, did not perform as well on this data.
- This confirmed my initial prediction.

## Conclusion

Based on the analysis, **Random Forest Classifier** outperformed the **Logistic Regression** model by 3.17% in terms of accuracy and is the better-performing model for this spam detection task. This means that, on average, the Random Forest model was able to correctly classify 3.17% more instances than the Logistic Regression model, which can be considered a significant improvement, particularly in classification tasks with complex patterns and non-linear relationships.

## Resources

- **UCI Machine Learning Repository**
- **Scikit-learn Documentation**: 
- **Activity and Slides**
- **Google**
- **Tutoring**
- **OpenAI**


