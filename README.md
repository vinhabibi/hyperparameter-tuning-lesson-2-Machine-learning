# Hyperparameter Tuning Lesson 2 (Machine Learning)

This repository contains a Jupyter notebook that compares multiple hyperparameter tuning strategies for an SVM classifier on the Ionosphere dataset.

## Notebook

- Hyper_parameter_tunning__lesson_2.ipynb

## Project Goal

Evaluate and compare the performance of these tuning approaches:

- Manual Search
- Grid Search (GridSearchCV)
- Random Search (RandomizedSearchCV)
- Optuna-based optimization

## Dataset

The notebook loads data from:

- /content/ionosphere.csv

This is a Google Colab-style path. If you run locally, update the path to where ionosphere.csv exists on your machine.

## Libraries Used

- pandas
- numpy
- scikit-learn
- scipy
- optuna
- matplotlib

## Workflow Summary

1. Load and preprocess the Ionosphere dataset.
2. Encode labels using LabelEncoder.
3. Split data into train/test with train_test_split.
4. Scale features using StandardScaler.
5. Train and evaluate SVM models with different tuning methods.
6. Compare best parameters and test accuracy.

## Key Results (from notebook output)

- Manual Search best accuracy: 0.9717
- Grid Search best CV accuracy: 0.9469
- Grid Search test accuracy: 0.9623
- Random Search best CV accuracy: 0.9510
- Random Search test accuracy: 0.9340
- Optuna best CV accuracy: 0.9551
- Optuna test accuracy: 0.9623

## Example Best Parameters

- Grid Search: {'C': 10, 'gamma': 'scale', 'kernel': 'rbf'}
- Random Search (approx): {'C': 9.7178, 'gamma': 0.0086, 'kernel': 'rbf'}
- Optuna (approx): {'C': 6.9359, 'gamma': 0.0474, 'kernel': 'rbf'}

## How to Run

1. Open the notebook in Jupyter or Google Colab.
2. Install required packages (for example, optuna).
3. Make sure ionosphere.csv is available and update the dataset path if necessary.
4. Run cells from top to bottom.

## Notes

- The notebook includes interpretation sections discussing observations and conclusions.
- Results can vary slightly between runs due to randomized search behavior.
