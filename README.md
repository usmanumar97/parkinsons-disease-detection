# Parkinson's Disease Prediction Project

## 📝 Project Overview
The objective of this project is to create a machine learning model that predicts Parkinson’s disease from vocal characteristics recorded from patients. This classification task aims to distinguish between individuals with Parkinson's disease (labeled as **1**) and healthy individuals (labeled as **0**). These features capture distinct vocal impairments that are prevalent in Parkinson’s patients, making this a **binary classification problem**.

## 🔄 Project Lifecycle

1. **Data Pre-Processing & Cleaning**
2. **Exploratory Data Analysis (EDA)**
3. **Feature Engineering**
4. **Data Splitting**
5. **Balance Data with Sampling Techniques**
6. **Training the Machine Learning Model**
7. **Feature Importance Analysis (Post-Modeling)**

## 📂 Dataset Overview Summary
This dataset includes various vocal attributes measured from individuals, relevant for assessing vocal instability—a key symptom of Parkinson's. Below is an outline of the key variables used:

- **Name**: Contains an identifier for each subject and recording.

- **Vocal Attributes**:
  - **Fundamental Frequency Metrics**: Average, high, and low frequencies (**MDVP:Fo(Hz)**, **MDVP:Fhi(Hz)**, **MDVP:Flo(Hz)**).
  - **Frequency Variation Metrics**: Measures of pitch stability, such as jitter (**MDVP:Jitter(%)**, **MDVP:Jitter(Abs)**, **MDVP:RAP**, **MDVP:PPQ**, **Jitter:DDP**).
  - **Amplitude Variation Metrics**: Shimmer metrics indicating loudness variability, such as **MDVP:Shimmer**, **Shimmer:APQ5**, **MDVP:APQ**, **Shimmer:DDA**.
  - **Noise Ratios**: **NHR** and **HNR** metrics, indicating noise levels in the voice.

- **Dynamical Complexity Measures**:
  - **Signal Complexity Metrics**: **RPDE**, **DFA** for capturing dynamic complexity in voice signals.
  - **Pitch Variation Metrics**: Nonlinear pitch metrics (**Spread1**, **Spread2**, **D2**, **PPE**) indicative of voice irregularities.

- **Status**: Target variable indicating health status (**1 = Parkinson's, 0 = Healthy**).

## ⚖️ Addressing Class Imbalance
Given that the dataset has **147 Parkinson’s cases** and **48 healthy cases**, class imbalance handling is essential. **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to generate a balanced dataset.

## 📊 EDA Findings
### 1. Feature Distributions
  - **Right-Skewed Features**: Jitter, Shimmer, and vocal frequency metrics show a right-skewed distribution, where the majority have lower values, with a few individuals exhibiting higher values, suggesting vocal instability in Parkinson’s cases.
  - **Skew Correction**: Log transformation was applied to adjust the skewness in jitter, shimmer, and frequency metrics for more normal-like distributions.

### 2. Distinguishing Parkinson’s and Healthy Cases
  - **Higher Jitter and Shimmer Values**: Tend to correlate with Parkinson’s, aligning with the expectation that Parkinson’s affects vocal stability.
  - **Lower Values**: Typically align with more stable vocal characteristics in healthy individuals.

## 🚀 Recent Progress
1. **Feature Transformation**: Applied log transformations on several features to address skewness, with ongoing evaluations on their effectiveness.
2. **Visualization Analysis**: Box plots and bar charts were used to visualize nonlinear complexity measures (RPDE, DFA, PPE) and their distributions across healthy and Parkinson’s cases.

## 🎯 Project Goal
To develop a robust, interpretable model for predicting Parkinson's disease based on vocal characteristics.


## 🔗 Dataset Source
The dataset is available on [Kaggle - Parkinson Disease Detection Dataset](https://www.kaggle.com/datasets/debasisdotcom/parkinson-disease-detection).

---

This is an ongoing project with continuous improvements being made for greater accuracy and interpretability.

---

