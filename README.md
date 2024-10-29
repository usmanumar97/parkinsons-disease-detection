# Parkinson's Disease Prediction Project

## 📝 Overview
The goal of this project is to develop a classification model that predicts whether an individual has Parkinson's disease (label **1**) or is healthy (label **0**) based on vocal characteristics measured from voice recordings. 🎯 These features are indicative of the distinct vocal impairments commonly observed in Parkinson's patients, making this a **binary classification problem** where the model aims to accurately distinguish between healthy and Parkinson's cases.

## 🔄 Project Lifecycle

1. 🧼 Data Pre-Processing & Cleaning
2. 📊 Exploratory Data Analysis (EDA)
3. ⚙️ Feature Engineering
4. ✂️ Data Splitting
5. ⚖️ Balance Data with Sampling Techniques
6. 🤖 Training Machine Learning Model
7. 🔍 Feature Importance Analysis (Post-Modeling)

### 🎯 End Goal
An accurate and interpretable model for Parkinson's disease prediction.

## 📂 Dataset Overview
- **Name**: Contains an identifier for each subject and recording.
- **Vocal Attributes**:
  - **MDVP:Fo(Hz)**, **MDVP:Fhi(Hz)**, **MDVP:Flo(Hz)**: Measures of the fundamental vocal frequency, capturing average, maximum, and minimum frequency respectively.
  - **MDVP:Jitter(%)**, **MDVP:Jitter(Abs)**, **MDVP:RAP**, **MDVP:PPQ**, **Jitter:DDP**: Metrics capturing variations in fundamental frequency (jitter), which indicate stability in vocal pitch, often affected in Parkinson's disease.
  - **MDVP:Shimmer**, **MDVP:Shimmer(dB)**, **Shimmer:APQ3**, **Shimmer:APQ5**, **MDVP:APQ**, **Shimmer:DDA**: Measures of amplitude variation (shimmer), representing voice stability in terms of loudness.
  - **NHR**, **HNR**: Ratios capturing noise to tonal components in the voice, which may reflect vocal disorder severity.
- **Dynamical Complexity Measures**:
  - **RPDE**, **DFA**: Measures of vocal signal complexity and fractal scaling, linked to vocal stability.
  - **Spread1**, **Spread2**, **D2**, **PPE**: Nonlinear vocal metrics capturing deviations in pitch and energy, relevant for Parkinson's diagnosis.
- **Status**: Target variable indicating health status (**1** = Parkinson's, **0** = Healthy).

## 📈 Target Variable Analysis: `status`
The target variable **`status`** represents whether an individual has Parkinson's disease (**1**) or is healthy (**0**).

### 📊 Value Counts of `status`
The dataset has **147 positive cases** (Parkinson's) and **48 negative cases** (Healthy), indicating a class imbalance.

### ⚖️ Addressing Class Imbalance with SMOTE
We will use **SMOTE** to oversample the minority class (`0`), helping to create a balanced dataset and improve model performance.

## 📊 Analysis Findings
### 1. Jitter, Shimmer, and Fundamental Frequency Distribution
- Most of the **jitter**, **shimmer**, and **fundamental vocal frequency** metrics show **right-skewed** distributions.
- **Right-skewed distribution** suggests that the majority of subjects have **lower values**, while fewer individuals have much **higher values**, creating a long right tail.
- **Higher jitter and shimmer values** in the right tail indicate **vocal instability**, commonly seen in Parkinson's patients.
- The **fundamental frequency** metrics also show right skewness, implying that only a few individuals have unusually **high vocal frequencies**, which could indicate **reduced vocal control**.

### 2. Differentiating Healthy and Parkinson’s Patients
- The **right-skewed nature** of these distributions suggests that **higher values** for jitter, shimmer, and vocal frequency are more likely to be associated with Parkinson's disease.
- **Lower values** for these metrics typically indicate more stable vocal characteristics, often seen in **healthy** individuals.

## 🚀 Recent Progress
- We have applied **log transformation** to several features to address right skewness in the data. This is an ongoing process, and we are evaluating how effective these transformations have been in reducing skewness. Features transformed include **MDVP:Fo(Hz)**, **MDVP:Fhi(Hz)**, **MDVP:Jitter(%)**, and others related to **jitter**, **shimmer**, and **vocal frequency**.
- Comparative analysis has been performed using **box plots** and **bar charts** to understand the distribution of nonlinear complexity measures (**RPDE**, **DFA**, **PPE**) between healthy and Parkinson’s groups.

## 🔗 Dataset Link
[Parkinson Disease Detection Dataset on Kaggle](https://www.kaggle.com/datasets/debasisdotcom/parkinson-disease-detection)

## 📝 Note
This is an **ongoing project**, and I am actively working on improving and refining the model. More updates will be added as progress is made, including completing the log transformation and preparing the data for modeling.

