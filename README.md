# Spotify Explicit Song Classifier

This project is a machine learning pipeline that predicts whether a song is marked as explicit based on its audio features. The model is trained on a labeled dataset provided by Magshimim and leverages various supervised learning algorithms to optimize predictive accuracy.

## Project Goals

- Automatically classify songs as explicit or not explicit.
- Identify the audio features most correlated with explicit content.
- Compare different classification algorithms in terms of accuracy, precision, recall, and F1 score.

## Data Source

The dataset used in this project was provided by the Magshimim Cyber Program. It includes audio features extracted from Spotify tracks, such as:

- Danceability  
- Energy  
- Loudness  
- Speechiness  
- Acousticness  
- Instrumentalness  
- Liveness  
- Tempo  
- Valence  
- Duration  

The dataset includes both the audio features and the `explicit` label (binary: 0 for non-explicit, 1 for explicit).

## Methodology

The following steps were performed:

### 1. Data Cleaning and Preprocessing

- Removed duplicates and unnecessary columns.
- Verified data balance and distribution.
- Scaled features using MinMaxScaler.
- Converted categorical labels to numerical format.

### 2. Exploratory Data Analysis

- Used histograms, heatmaps, and pairplots to analyze feature distributions and correlations.
- Noted that explicit songs tend to have higher energy, loudness, and tempo.

### 3. Model Training and Evaluation

Multiple classification algorithms were trained and compared:

- Decision Tree  
- K-Nearest Neighbors (KNN)  
- Random Forest  
- Bagging Classifier  

GridSearchCV was used for hyperparameter tuning. Evaluation was done using:

- Accuracy  
- Precision  
- Recall 
- Confusion Matrix  

The best performing models were the ensemble methods (Bagging and XGBoost), both achieving high recall and precision.

## Results Summary

| Model          | Recall   |
|----------------|----------|
| NCC            | ~0.72    | 
| Decision Tree  | ~0.92    | 
| KNN            | ~0.99    |
| Random Forest  | ~0.93    |
| Bagging        | ~0.99+   |


## Full Report

A detailed written analysis of this project can be found in the accompanying report:  
[Project Documentation (Google Docs)](https://docs.google.com/document/d/1E9uMAeaPfuz1Cnkbpl18PHM7TmwUeTob)
