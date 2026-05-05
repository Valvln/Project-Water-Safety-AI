# Project-Water-Safety-AI

## Water Potability Classification: A Safety-First ML Approach
This repository contains a rigorous Machine Learning analysis designed to predict water potability using physical and chemical parameters. In water management, the cost of a False Positive (classifying contaminated water as safe) is critical; therefore, this project emphasizes risk mitigation, calibration, and model reliability.

## Project Objective
The goal of this project is to develop a robust classification pipeline that balances predictive power with operational efficiency. By leveraging advanced imputation techniques and non-linear models, we aim to provide a trustworthy decision-support tool for public health safety.

## Dataset Overview
The analysis is performed on the *Water Potability Dataset*, which includes:

**Samples**: 3,276 water bodies.

**Features**: 9 metrics including pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, and Turbidity.

**Target**: Binary classification (1: Potable, 0: Not Potable).

## Technical Workflow
The project follows a comprehensive and specialized Data Science pipeline:

**Environment Setup & Initial Loading**: Setting up the analytical framework and preliminary data inspection.

**Data Splitting**: Ensuring a clean separation between training and test environments from the start.

**Exploratory Data Analysis (EDA)**:

* **Target Distribution**: Assessing class balance.

* **Missing Data**: Applying Little's Test followed by Iterative Imputer for statistically sound data recovery.

* **Outlier Detection**: Implementing Isolation Forest to handle anomalous environmental readings.

* **Multivariate Analysis**: Using Spearman Correlation to detect non-linear relationships.

**Baseline Modeling**: Establishing a benchmark using Random Forest.

**Feature Engineering**: Comparing Feature Importance vs. T-tests to identify the most significant predictors.

**Dimensionality Reduction**: Creating a Reduced Dataset to optimize sensor costs.

**Spot-check Modeling**: Comparing Logistic Regression, SVC, and XGBoost.

**Optimization**: Hyperparameter tuning for SVC and XGBoost using Validation Curves and C-Gamma Heatmaps.

**Advanced Evaluation**: Comparing models via ROC-AUC, Accuracy, and Precision-Recall curves.

**Validation**: Final performance assessment on the Test Set with detailed Confusion Matrices and Classification Reports.

**Probability Calibration**: Analyzing Calibration Curves and Brier Scores to ensure honest probability estimates.

**Error Forensics**: Identifying Shared Failures and analyzing the intrinsic ambiguity of the chemical data.

## Key Results
**Champion Model**: The Optimized SVC on the Reduced Dataset proved to be the winner, offering the best balance between discriminative power and calibration.

**Generalization**: High consistency between training and test phases, effectively mitigating overfitting.

**Operational Efficiency**: Successfully identified that *pH* and *Sulfate* are the primary drivers, allowing for high-accuracy monitoring even with a reduced sensor array (3 fewer variables).

**Reliability**: The Brier Score analysis confirms that the model provides dependable confidence intervals for real-world deployment.

## Future Improvements & Governance
Implementation of Threshold Moving to further minimize False Positives.

Deployment of a "Grey Zone" Alerting system for samples with low-confidence probabilities.

Integration of a Soft Voting Ensemble (SVC + XGBoost) for maximum robustness.
