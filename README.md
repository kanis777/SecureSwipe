# SecureSwipe
UI:Streamlit\
Platform:Google Colab\
# SecureSwipe Fraud Detection Project

## Overview
This project aims to detect fraudulent transactions in the SecureSwipe dataset. The dataset contains both fraudulent and successful transactions, and the goal is to build a model that can accurately classify transactions as fraudulent or successful.

## Project Structure
- `data/`: Contains the dataset used for training and testing.
- `src/`: Contains the source code for data preprocessing, model training, and evaluation.
- `models/`: Contains saved trained models.
- `results/`: Contains evaluation results and visualizations.

## Steps

### 1. Data Preprocessing
- Removed null, missing, and duplicate values.
- Scaled 'amt' and 'time' columns using RobustScaler to handle outliers.
- Detected and handled outliers using the Interquartile Range (IQR) method.
- Oversampled the data using Synthetic Minority Over-sampling Technique (SMOTE) due to class imbalance.

### 2. Model Training
- Utilized Logistic Regression as the classification model.
- Checked for multicollinearity using Variance Inflation Factor (VIF).
- Addressed multicollinearity by applying Ridge regularization.

### 3. Evaluation Metrics
- Evaluated the model using the following metrics:
  - Accuracy
  - Precision
  - Recall
  - Confusion Matrix

### 4. Privacy-Preserving Techniques
- Implemented Privacy-Preserving Aggregated Training with Exponential Mechanism (PATE) using Laplacian noise for security.

## Usage
1. Clone the repository:

```bash
git clone https://github.com/your-username/SecureSwipe-Fraud-Detection.git
```
Navigate to the project directory:
```bash
cd SecureSwipe-Fraud-Detection
```
Install dependencies:
```bash
pip install -r requirements.txt
```
