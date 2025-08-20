---
layout: post
title: Can Machine Learning Help Predict Heart Disease? A Data Science Exploration
subtitle :  
tags: [ml, regression, classification ]
author: Clifford
comments : True
---

# Can Machine Learning Help Predict Heart Disease?

Heart disease remains one of the leading causes of death worldwide. Early diagnosis can save lives, but traditional methods of risk assessment often depend on limited clinical tests or subjective interpretation. With the growing availability of health data, I wanted to explore whether **machine learning (ML) techniques** could assist in predicting heart disease risk more accurately.

This post summarizes my project: applying different ML algorithms to a clinical dataset to see how well they could predict the presence of heart disease.


## The Dataset

I used a publicly available dataset from Kaggle containing **1,025 anonymized patient records**. Each record included **13 clinical features** (like age, chest pain type, blood pressure, cholesterol levels, ECG results, maximum heart rate, etc.) and a target label indicating whether the patient had heart disease.

Why this dataset?

* It’s a standard benchmark for healthcare ML experiments.
* The size (1k+ records) is manageable yet complex enough to apply multiple techniques.
* It includes both categorical and numerical features, which means meaningful preprocessing steps are required.


## Approach

I followed a typical **data science workflow**:

1. **Exploratory Data Analysis (EDA):**

   * Visualized feature distributions and checked correlations.
   * Found that some features (e.g., chest pain type, thalassemia, maximum heart rate) strongly correlated with heart disease.

2. **Preprocessing:**

   * Handled categorical features through encoding.
   * Scaled numerical features to a common range to help algorithms like SVM and KNN.

3. **Modeling:**
   I compared four algorithms:

   * Logistic Regression (baseline)
   * Random Forest (ensemble method)
   * K-Nearest Neighbours (KNN)
   * Support Vector Machine (SVM with RBF kernel)

4. **Evaluation:**

   * Used accuracy, precision, recall, F1-score, and ROC-AUC.
   * Applied **5-fold cross-validation** and **GridSearchCV** for hyperparameter tuning.


## Results

* **Random Forest** was the clear winner, achieving **\~99.7% accuracy** and perfect scores on precision, recall, and F1.
* **SVM** also performed strongly with \~91.7% accuracy and high ROC-AUC.
* Logistic Regression and KNN gave reasonable baselines but underperformed compared to ensemble methods.

Interestingly, the most predictive features included:

* **Chest pain type** (certain types highly associated with disease).
* **Maximum heart rate achieved** (higher stress response linked to risk).
* **Number of major vessels** and **thalassemia type** (clear clinical indicators).


## Insights

* **Ensemble models like Random Forest excelled** because they can capture complex feature interactions without heavy assumptions.
* **Cross-validation was critical** — early models showed near-perfect scores that looked like overfitting, but validation confirmed generalizability.
* Some findings challenged medical intuition, such as younger patients showing more heart disease in this dataset. This highlights the need for broader, more representative datasets.


## Future Directions

To extend this project, I would:

* Consider hybrid techniques.
* Compare the results with the published articles on the same dataset.
* Increase the training set size.
* Integrate **Explainable AI tools** (like SHAP or LIME) so clinicians can understand *why* the model makes predictions.
* Expand the dataset with multi-institutional records for stronger generalization.
* Explore **deep learning models** for non-linear relationships and time-series clinical data.


## Conclusion

This project shows the potential of machine learning in assisting with early heart disease detection. While the results are promising, clinical deployment would require larger datasets, rigorous testing, and interpretability.

For me, the key takeaway was how much value comes from following a **research mindset**: clearly defining the problem, testing multiple approaches, validating results, and critically reflecting on their implications.

📄 You can [view the full research report here](https://github.com/cliffordEmmanuel/heart-disease-prediction/blob/main/Heart-disesase-prediction-report.pdf).



