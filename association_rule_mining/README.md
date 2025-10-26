# Association Rule Mining

## Overview
This folder contains a minimal PyCaret workflow for **association rule mining** (market basket analysis) on grocery transaction data.

## Dataset
- **File:** `Groceries_dataset.csv`
- **Size:** 38,765 rows
- **Features:** Member_number, Date, itemDescription
- **Purpose:** Discover frequent itemsets and association rules to understand customer purchase patterns

## Task
Market basket analysis using the Apriori algorithm to find associations between grocery items purchased together.

## Notebook
- **File:** `association_rule_mining.ipynb`
- **Workflow:**
  1. Load the grocery transactions dataset
  2. Set up PyCaret `AssociationRulesExperiment` (requires Python 3.7-3.8 and PyCaret 2.x)
  3. Generate association rules using Apriori
  4. Display rules with support, confidence, and lift metrics
  5. Save rules to CSV

## How to Run

### Important: Environment Requirements
⚠️ **PyCaret's Association Rules module (`pycaret.arules`) is only available in PyCaret 2.x, which requires Python 3.7–3.8.**

If you are using Python 3.11, you have two options:

#### Option A: Use Python 3.8 environment (recommended for PyCaret)
1. Create a Python 3.8 virtual environment:
   ```bash
   python3.8 -m venv .venv-py38
   source .venv-py38/bin/activate
   pip install "pycaret==2.3.10" ipykernel
   ```

2. Add it as a Jupyter kernel:
   ```bash
   python -m ipykernel install --user --name pycaret2-38 --display-name "PyCaret 2 (Py3.8)"
   ```

3. Open the notebook and switch to the "PyCaret 2 (Py3.8)" kernel:
   ```bash
   jupyter notebook association_rule_mining.ipynb
   ```

#### Option B: Use mlxtend (alternative, works on Python 3.11)
If you prefer to stay on Python 3.11, use the `mlxtend` library instead of PyCaret for association rules:
```bash
pip install mlxtend pandas
```

## Model Output
- **File:** `association_rules_output.csv`
- Contains rules with columns: antecedents, consequents, support, confidence, lift

## Key Metrics
- **Support:** How frequently an itemset appears in transactions
- **Confidence:** Likelihood of purchasing item Y when item X is purchased
- **Lift:** How much more likely item Y is purchased when X is purchased (compared to baseline)

## References
- [PyCaret Association Rules Demo](https://github.com/pycaret/pycaret-demo-queens/blob/main/PyCaret%20Association%20Rule.ipynb)
- [Kaggle: Association Rule Mining with PyCaret](https://www.kaggle.com/code/ukveteran/association-rule-mining-pycaret-jma)
