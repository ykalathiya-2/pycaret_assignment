# Clustering (Customer Segmentation)

## Overview
This folder contains a minimal PyCaret workflow for **customer segmentation** using clustering algorithms.

## Dataset
- **File:** `segmentation data.csv`
- **Size:** 2,000+ samples
- **Features:** ID, Sex, Marital status, Age, Education, Income, Occupation, Settlement size
- **Purpose:** Segment customers based on demographic and economic characteristics

## Task
Unsupervised clustering to identify distinct customer segments for targeted marketing strategies.

## Notebook
- **File:** `clustering.ipynb`
- **Workflow:**
  1. Load and explore the customer dataset
  2. Set up PyCaret `ClusteringExperiment` with normalization
  3. Create a K-Means clustering model (4 clusters)
  4. Evaluate with elbow plot and silhouette analysis
  5. Assign cluster labels to customers
  6. Save the trained model

## How to Run
1. Ensure PyCaret is installed:
   ```bash
   pip install pycaret[analysis]
   ```

2. Open and run `clustering.ipynb` in Jupyter:
   ```bash
   jupyter notebook clustering.ipynb
   ```

3. Run all cells in order. The notebook will:
   - Load `segmentation data.csv`
   - Train a K-Means clustering model
   - Generate elbow and silhouette plots
   - Assign cluster labels to each customer
   - Save the pipeline

## Model Output
- **Model file:** `kmeans_segmentation_model.pkl` (excluded from Git)
- Dataset with added `Cluster` column indicating segment membership

## Visualizations
- **Elbow plot:** Helps determine optimal number of clusters
- **Silhouette plot:** Evaluates cluster quality and separation
- **PCA cluster plot:** 2D visualization of clusters

## Use Case
Customer segmentation enables:
- Targeted marketing campaigns
- Personalized product recommendations
- Resource allocation optimization
- Customer lifetime value analysis

## References
- [PyCaret Clustering Tutorial](https://nbviewer.org/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Clustering.ipynb)
