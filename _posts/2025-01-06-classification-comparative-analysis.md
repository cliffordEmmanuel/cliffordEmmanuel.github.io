---
layout: post
title: Predicting House Prices; SVC vs Random Forest
subtitle : I set out to explore whether machine learning could help us predict house prices more accurately.
tags: [ml, regression ]
author: Clifford
comments : True
---


# ❤️ Predicting Heart Disease: SVC vs Random Forest

Heart disease remains one of the leading causes of death worldwide. With the right data, machine learning can help us spot early signs of risk — but which algorithms work best?

In this project, I compared **Support Vector Classifier (SVC)** and **Random Forest Classifier (RFC)** to predict heart disease.

## The Dataset

I used the **Heart Disease dataset**, which contains **303 patient records** with features like:

* Age
* Blood pressure
* Cholesterol levels
* ECG results
* Exercise-induced angina
* Maximum heart rate achieved

The goal: classify patients as **at risk of heart disease** or **not at risk**.

## The Approach

Two models were tested:

1. **Support Vector Classifier (SVC, RBF kernel)** – finds the best boundary between classes.
2. **Random Forest Classifier (RFC)** – combines multiple decision trees to improve predictions.

Performance was measured using **accuracy, precision, recall, and F1-score**.


## Results

* **SVC outperformed RFC** across all metrics:

  * Accuracy: 87% (vs 80% for RFC)
  * Precision & Recall: balanced around 0.86–0.88
* RFC showed slightly better recall for positive cases (heart disease present) but weaker precision.
* SVC was more **consistent across both classes**, making it more reliable for medical screening.


## Insights

* **SVC provided balanced predictions**, which is critical for healthcare applications where false negatives can be dangerous.
* **Random Forest offered feature importance** (useful for interpretability) but showed more bias toward one class.
* Both models are acceptable, but SVC showed more robustness in this dataset.


## Next Steps

If I extended this project, I would:

* Apply **robust feature scaling** (e.g., StandardScaler, RobustScaler).
* Perform **feature engineering** using domain knowledge (e.g., cholesterol ratios, blood pressure categories).
* Explore **polynomial features** and **interaction terms** for improved prediction power.


## Conclusion

This study shows how ML models can support **early diagnosis of heart disease**. While Random Forest is useful, the **Support Vector Classifier gave more reliable results** for this dataset.

📄 You can [view the full report here](https://github.com/cliffordEmmanuel/classification-comparison).
