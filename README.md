# Pima Indians Diabetes Prediction Project

## Project Goal
This project is about predicting if a person has diabetes or not using health data from Pima Indian women. I tried different machine learning models to see which one works best.

---

## Dataset
The data comes from the National Institute of Diabetes and Digestive and Kidney Diseases.  
It has several health-related features and one target column `Outcome` which tells if a person has diabetes.

### Features (Input)
- `Pregnancies`: Number of times pregnant  
- `Glucose`: Blood sugar level after 2 hours  
- `BloodPressure`: Blood pressure measurement  
- `SkinThickness`: Skin thickness measurement  
- `Insulin`: Insulin level in blood  
- `BMI`: Body Mass Index  
- `DiabetesPedigreeFunction`: Family history score  
- `Age`: Person's age  

### Target (Output)
- `Outcome`: 0 = No diabetes, 1 = Has diabetes

---

## Data Preparation
1. **Fix missing values** – Replaced `0` in features like Glucose, BloodPressure, etc. with the mean.  
2. **Remove duplicates** – Checked and no duplicates found.  
3. **Check data types** – Ensured all features are numbers.  
4. **Handle categories** – Not needed for this dataset, but could encode text categories in other datasets.  

---

## Feature Scaling
- **StandardScaler** – Makes features have mean 0 and std 1 (good for Logistic Regression, KNN).  
- **MinMaxScaler** – Scales features between 0 and 1.  

---

## Train-Test Split
- 80% for training, 20% for testing  
- `random_state=42` to get same split every time  

---

## Models Used and Accuracy
| Model | Accuracy | Short Description |
|-------|---------|-----------------|
| Logistic Regression | 0.75 | Basic yes/no prediction, works with straight decision boundaries |
| K-Nearest Neighbors | 0.74 | Predicts based on closest neighbors |
| Decision Tree | 0.72 | Makes predictions like a flowchart |
| Random Forest | 0.75 | Uses many trees and takes majority vote |
| Naive Bayes | 0.75 | Uses probabilities assuming features are independent |

---

## How I Checked Model Performance
- **Accuracy** – % of correct predictions  
- **Classification Report** – Shows precision, recall, F1-score  
- **Confusion Matrix** – Shows correct vs wrong predictions  
- **ROC Curve & AUC** – Shows how well the model separates classes  

---

## Visualizations
- **Histograms** – Show how feature values are spread  
- **Correlation Heatmap** – Shows relationship between features and outcome  


