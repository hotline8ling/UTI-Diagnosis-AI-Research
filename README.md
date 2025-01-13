# Predictive System for Early UTI Detection

## Overview

This repository contains the implementation and research behind a **Predictive System for Early Urinary Tract Infection (UTI) Detection**. By leveraging **reduced models**, **ensemble learning through soft voting**, and advanced machine learning techniques, this project demonstrates AI's transformative potential in healthcare diagnostics.

The system was developed by a research team led by **Roj Gian D. Gorospe**, showcasing a practical application of AI in healthcare to enhance diagnostic accuracy, reduce biases, and optimize resource utilization.

---

## Features

1. **Machine Learning Models**:
   - TabNet, XGBoost, SVM, LightGBM, and Logistic Regression.
   - Optimized using **Optuna** for hyperparameter tuning.
   - Shapley Additive Explanation (**SHAP**) for feature importance analysis.

2. **Reduced Models**:
   - Feature reduction based on SHAP analysis.
   - Retain high accuracy with fewer input parameters.

3. **Ensemble Learning**:
   - **Soft Voting** combines predictions from the top-performing models.
   - Reduces biases and improves robustness.

4. **Evaluation Metrics**:
   - AUC, Precision, Recall, Specificity, Accuracy, and F1 Score.
   - Ensemble models achieved:
     - **AUC**: 95.2%
     - **Recall**: 94.4% (Overall) and 93.7% (Reduced)

5. **Data Handling**:
   - Focused on urinalysis test results with 10-parameter dipsticks.
   - Extensive preprocessing to ensure data quality and reliability.

---

## System Architecture

![System Architecture](D:/SENIOR UST/UTI-Diagnosis-AI-Research/sysarch.png)

---

## Dataset

- Data sourced from clinical diagnostics centers in the Philippines (2020-2024).
- Preprocessed for:
  - **Cleaning**: Removing duplicates, nulls, and inconsistencies.
  - **Normalization**: Scaling features for model compatibility.
  - **Validation**: Reviewed by a certified internal medicine doctor.

- **Stratified Data**:
  - Age groups: 0-6, 7-18, 19-40, 41-60 years.
  - Total observations: 412 samples.

---

## Methodology

### Data Preprocessing
1. Data cleaning and normalization.
2. Feature engineering based on SHAP analysis.
3. Splitting: Training (70%), Validation (20%), Test (30%).

### Modeling
- Models trained on both full and reduced datasets.
- Ensemble models designed to aggregate predictions through soft voting.

### Statistical Analysis
- Approximate z-test used to assess statistical significance of results.
- Ensured no significant difference between full and reduced models, validating the efficiency of reduced models.

---

## Results

| Model                  | AUC    | Precision | Recall  | Accuracy | Specificity |
|------------------------|--------|-----------|---------|----------|-------------|
| Logistic Regression    | 94.29% | 91.18%    | 98.41%  | 94.35%   | 90.16%      |
| XGBoost                | 95.95% | 95.31%    | 96.83%  | 95.97%   | 95.08%      |
| Reduced XGBoost        | 96.77% | 96.83%    | 96.83%  | 96.77%   | 96.72%      |
| Ensemble (Overall)     | 95.16% | 95.24%    | 95.24%  | 95.16%   | 95.08%      |
| Ensemble (Reduced)     | 94.37% | 95.16%    | 93.65%  | 94.35%   | 95.08%      |

---

## Conclusion

- The study demonstrates that **reduced models** and **ensemble methods** can achieve diagnostic performance comparable to full models while being computationally efficient.
- Ensemble models effectively reduce bias and handle noise in medical data, paving the way for scalable and accurate healthcare solutions.

---

## Recommendations

1. **Integrate Urine Culture**:
   - Future datasets should include urine culture results for gold-standard validation.

2. **Broader Data Collection**:
   - Include diverse sources to handle variations in urinalysis methods.

3. **Privacy-Preserving Machine Learning**:
   - Explore techniques like differential privacy and homomorphic encryption.

---

## Citation

If you use this project in your research, please cite:

Nathaniel Ken A. Aquino
Department of Computer Science
College of Information and Computing Sciences
University of Santo Tomas
Manila, Philippines
nathanielken.aquino.cics@ust.edu.ph

Neal Carlos B. Gayapa
Department of Computer Science
College of Information and Computing Sciences
University of Santo Tomas
Manila, Philippines
nealcarlos.gayapa.cics@ust.edu.ph

Roj Gian D. Gorospe
Department of Computer Science
College of Information and Computing Sciences
University of Santo Tomas
Manila, Philippines
rojgian.gorospe.cics@ust.edu.ph

Luke Terrel M. Santibañez
Department of Computer Science
College of Information and Computing Sciences
University of Santo Tomas
Manila, Philippines
luketerrel.santibanez.cics@ust.edu.ph

