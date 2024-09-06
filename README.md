# EEG Emotion Analysis

This project involves the analysis of EEG data to classify emotions into categories such as POSITIVE, NEUTRAL, and NEGATIVE. The data undergoes preprocessing and feature encoding to prepare it for machine learning models.

## Table of Contents
- [Overview](#overview)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Feature Encoding](#feature-encoding)
- [Model Interpretation](#model-interpretation)
  - [LIME](#lime)
  - [SHAP](#shap)
- [Usage](#usage)
- [Results](#results)
- [Requirements](#requirements)
- [Acknowledgements](#acknowledgements)

## Overview
The goal of this project is to analyze EEG signals to predict emotional states. The data is processed to clean and encode the features for use in machine learning algorithms.

## Data
The dataset (`emotions_new.csv`) contains multiple columns representing various EEG signal features:
- `mean_0_a`, `mean_1_a`, ..., `mean_d_4_a`: Mean values of different EEG channels.
- `fft_741_b`, `fft_742_b`, ..., `fft_749_b`: Frequency domain features extracted using FFT (Fast Fourier Transform).
- `label`: The target variable indicating the emotional state (POSITIVE, NEUTRAL, NEGATIVE).

## Preprocessing
The data preprocessing steps include:
- Loading the dataset into a Pandas DataFrame.
- Rounding off decimal values and converting them to integers.
- Applying feature encoding based on predefined thresholds.

## Feature Encoding
Numerical columns are encoded into discrete values using the following rules:
- Values greater than 0.5 are encoded as `1`.
- Values between -0.5 and 0.5 are encoded as `0`.
- Values less than -0.5 are encoded as `-1`.

## Model Interpretation
To understand the model's predictions, we used LIME and SHAP:

### LIME
LIME was used to generate local explanations for individual predictions:

**Key Insights**: LIME helps in understanding which features contributed most to the prediction for specific instances.


### SHAP
SHAP provides a global understanding of feature importance across all predictions:

**Key Insights**: SHAP values indicate the impact of each feature on the model's output.


## Usage
To use this project:
1. Clone the repository.
2. Ensure all dependencies are installed (see [Requirements](#requirements)).
3. Run the Jupyter notebook to preprocess the data, train models, and generate explanations using LIME and SHAP.

## Results
- The trained model achieved [accuracy/other metrics] on the test set.
- LIME and SHAP analyses revealed that features like [example features] were most influential in predicting the emotional states.

## Requirements
- Python 3
- Jupyter Notebook
- Pandas
- NumPy
- LIME
- SHAP
- Scikit-learn

## Acknowledgements
This project utilizes EEG data and basic data processing techniques to explore the classification of emotions using machine learning models.
