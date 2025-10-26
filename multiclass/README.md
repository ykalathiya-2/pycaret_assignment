# Multiclass Classification (Student Performance)

## Overview
This folder contains a minimal PyCaret workflow for **multiclass classification** to predict student grade categories.

## Dataset
- **File:** `Student_performance_data _.csv`
- **Features:** Various student attributes and academic metrics
- **Target:** `GradeClass` - Categorical student performance levels
- **Purpose:** Predict student grade categories based on their characteristics

## Task
Supervised multiclass classification using PyCaret's AutoML to identify the best model for predicting student grades.

## Notebook
- **File:** `multiclass.ipynb`
- **Workflow:**
  1. Load and explore the student performance dataset
  2. Set up PyCaret `ClassificationExperiment` with normalization and transformation
  3. Compare multiple classification models automatically
  4. Evaluate the best model interactively
  5. Generate predictions
  6. Save the trained model

## How to Run
1. Ensure PyCaret is installed:
   ```bash
   pip install pycaret[analysis]
   ```

2. Open and run `multiclass.ipynb` in Jupyter:
   ```bash
   jupyter notebook multiclass.ipynb
   ```

3. Run all cells in order. The notebook will:
   - Load `Student_performance_data _.csv`
   - Automatically compare 15+ classification algorithms
   - Select the best model based on accuracy
   - Display interactive evaluation plots
   - Generate predictions with probability scores

## Model Output
- **Model file:** `best_student_performance_model.pkl` (excluded from Git)
- Predictions with grade class labels and confidence scores

## Evaluation Metrics
- Accuracy
- Precision, Recall, F1-Score (per class)
- Confusion Matrix
- ROC-AUC (multiclass)
- Classification Report

## Use Case
Student performance prediction enables:
- Early intervention for at-risk students
- Personalized learning path recommendations
- Resource allocation for academic support
- Data-driven educational policy decisions

## References
- [PyCaret Classification Tutorial](https://pycaret.gitbook.io/docs/get-started/tutorials)
