# ADHD Brain Activity Pattern Modeling – Notes

## Challenge Overview

The core objective is to analyze brain activity patterns associated with ADHD and investigate how these patterns may differ between males and females. The focus is on functional MRI (fMRI) connectome matrices, which represent structured brain activity data.

While socio-demographic and behavioral data are available, the primary research emphasis remains on neuroimaging.

---

## Data Considerations

### Functional MRI Data
- High-dimensional data (~19,900 features).
- Key to identifying neurobiological patterns.

### Additional Features
- Socio-demographic (age, sex, race, education).
- Behavioral assessments:  
  - SDQ (Strengths and Difficulties Questionnaire)  
  - APQ (Alabama Parenting Questionnaire)

These provide useful context but are not diagnostic tools and should be used carefully to avoid data leakage.

---

## Dimensionality Reduction with PCA

Principal Component Analysis (PCA) was applied to:
- Reduce dimensionality while preserving variance.
- Minimize noise and redundancy.
- Improve model training efficiency.

**Trade-offs:**
- Principal components are harder to interpret.
- Potential loss of ADHD-relevant signals if too many components are discarded.

---

## Data Preprocessing

- Outliers and anomalous records were removed based on distribution analysis.
- Normalization and standardization applied to prepare data for modeling.

---

## Modeling Approaches

### Logistic Regression (Multi-Output)
- Predicts both ADHD outcome and sex.
- Regularization (L1/L2) used to handle high dimensionality.

### Random Forest
- Robust to non-linear patterns and high-dimensional features.
- Class weights used to handle imbalance.
- Provides feature importance for interpretability.

### XGBoost
- Handles imbalance via scale_pos_weight or custom objective.
- High performance in classification tasks.
- Captures complex relationships.

### Neural Networks
- Multi-output architecture with shared layers.
- Captures deep interactions between MRI and metadata.
- Imbalance addressed via:
  - Class weighting
  - Focal loss
  - Mini-batch sampling strategies

### Support Vector Machines (SVM)
- Effective for classification, especially with high-dimensional data.
- Tuned using class weights to manage imbalance.
- Finds optimal decision boundaries in complex feature spaces.

---

## Class Imbalance Strategy

- ADHD and sex labels are imbalanced.
- Addressed using:
  - Class weighting in models
  - Stratified cross-validation
  - Evaluation with F1-score

---

## Evaluation Metrics

- Accuracy not used as primary metric.
- Focused on:
  - F1-Score
  - Precision and Recall

---

## Analytical Strategy

### MRI-Centric Analysis
- Focuses solely on fMRI data.
- Ideal for extracting neuroscience insights.

### Prediction-Oriented Analysis
- Uses all available features (MRI and metadata).
- Requires careful handling to avoid data leakage.
- Separate analyses performed to distinguish between:
  - Scientific understanding
  - Predictive performance

---

## Summary

- fMRI data is central to addressing the core research question.
- Additional metadata can enhance model performance but must be used cautiously.
- A combination of PCA, data cleaning, and multiple model types (including ensemble, kernel-based, and deep learning approaches) ensures a robust exploration of the problem space.
