# Automated Essay Scoring System

## Introduction
This project develops an Automated Essay Scoring (AES) system using a dataset of over 10,000 expert-graded essays. The goal is to build a machine learning model capable of assigning scores to essays with a degree of accuracy comparable to human expert graders.

## Data Preprocessing
The dataset was first loaded and then thoroughly cleaned. The cleaning steps included:
- Removal of entries with missing scores (`domain1_score`).
- Cleaning of essays

## Exploratory Data Analysis (EDA)
A comprehensive EDA was performed, with steps including:
- Heatmaps of missing data to identify  null values.
- Distribution analysis of essay scores.
- Examination of the average scores by essay set, highlighting the variation in grading across different topics.

## Feature Engineering
To enrich the model's input data, several feature engineering steps were conducted:
- Tokenization and removal of punctuation and stop words.
- Calculation of various text-based metrics such as average sentence length, readability scores (Flesch Reading Ease and Gunning Fog Index), and sentiment polarity.

## Model Selection and Training
For the modeling phase:
- A RandomForestRegressor was chosen for its robustness and effectiveness in handling diverse features.
- The model was trained on TF-IDF vectorized essay texts combined with the engineered features.
- Learning curves were plotted to visualize the model's performance over different sizes of training data.

## Evaluation Metrics
- The QWK (Quadratic Weighted Kappa) was the primary metric used for model evaluation, as it is specifically designed to measure agreement between two ratings, which is ideal for this grading task.
- Cross-validation scores were calculated to ensure the robustness and reliability of the model's performance.

## Conclusion
The AES system developed shows promising results in automating the essay grading process.
