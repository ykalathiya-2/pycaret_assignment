# Anomaly Detection

## Overview
This folder contains a minimal PyCaret workflow for **anomaly detection** on bank transaction data.

## Dataset
- **File:** `bank_transactions_data_2.csv`
- **Size:** 2,512 samples
- **Features:** Transaction details including TransactionID, AccountID, TransactionAmount, TransactionDate, TransactionType, Location, DeviceID, IP Address, MerchantID, AccountBalance, PreviousTransactionDate, Channel, CustomerAge, CustomerOccupation, TransactionDuration, and LoginAttempts
- **Purpose:** Detect fraudulent or anomalous transactions based on transactional behavior patterns

## Task
Unsupervised anomaly detection using PyCaret to identify outliers and suspicious transactions.

## Notebook
- **File:** `Anomaly_detection.ipynb`
- **Workflow:**
  1. Load and explore the dataset
  2. Set up PyCaret `AnomalyExperiment`
  3. Create an Isolation Forest model
  4. Evaluate and assign anomaly labels
  5. Save the trained model

## How to Run
1. Ensure PyCaret is installed:
   ```bash
   pip install pycaret[analysis]
   ```

2. Open and run `Anomaly_detection.ipynb` in Jupyter:
   ```bash
   jupyter notebook Anomaly_detection.ipynb
   ```

3. Run all cells in order. The notebook will:
   - Load `bank_transactions_data_2.csv`
   - Train an Isolation Forest anomaly detector
   - Assign anomaly labels (0 = normal, 1 = anomaly)
   - Display sample results

## Model Output
- Trained models are saved as `.pkl` files (excluded from Git via `.gitignore`)
- Anomaly labels are added to the dataset as a new column

## References
- [PyCaret Anomaly Detection Tutorial](https://nbviewer.org/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Anomaly%20Detection.ipynb)
