# Smart Factory Product Quality Classification
[\[LG Aimers\] Smart factory product quality status classification AI Hackathon](https://dacon.io/en/competitions/official/236080/) – **2nd Place**

## Overview
This project develops a machine learning model to classify product quality status in a smart factory environment.
The goal is to determine whether manufactured products meet quality standards so that production systems can maintain stability and efficiency.

The solution achieved **2nd place** in the **LG AI Research Smart Factory AI Hackathon**.

## Approach
Industrial manufacturing data contained **high-dimensional features, missing values, and outliers**, which increased the risk of overfitting.
To address this, the pipeline focused on **robust preprocessing and feature reduction** before model training.

Key steps:
* Removed constant and low-informative features
* Handled missing values and replaced outliers using **Z-score detection**
* Performed **two-stage feature selection**
  * Pearson correlation filtering
  * RandomForest feature importance
* Trained a **K-fold stacking ensemble** with tree-based models

Base models:

`RandomForest` `Gradient Boosting` `XGBoost` `LightGBM` `CatBoost`

Meta model:

`XGBoost`

<img width="630" height="155" alt="Image" src="https://github.com/user-attachments/assets/912deb80-8c20-416d-bfe9-3687064bcf41" />

## Results
| Metric        | Score       |
| ------------- | ----------- |
| Validation F1 | **0.6972**  |
| Private Score | **0.6974**  |

The close match between validation and private scores indicates **stable generalization performance**.

## Key Insight
For real-world industrial datasets, **careful preprocessing and feature reduction were more impactful than increasing model complexity**.
