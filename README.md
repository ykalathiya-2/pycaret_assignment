# PyCaret Assignment - Low-Code Machine Learning Workflows

This repository demonstrates minimal, reproducible machine learning workflows using **PyCaret** - a low-code ML library in Python. Each folder contains a complete end-to-end example for different ML tasks, from data loading to model deployment.

## 📁 Repository Structure

```
pycaret_assignment/
├── anomaly_detection/          # Fraud detection on bank transactions
├── association_rule_mining/    # Market basket analysis on grocery data
├── clustering/                 # Customer segmentation
├── multiclass/                 # Student performance classification
├── regression/                 # Car price prediction
├── time_series/                # Weather forecasting (univariate)
└── README.md                   # This file
```

Each folder contains:
- 📓 Jupyter Notebook (`.ipynb`) with complete workflow
- 📊 Dataset (`.csv`)
- 📝 Detailed README with task description and instructions
- 🔧 Saved models (`.pkl` - excluded from Git)

---

## 🎯 Machine Learning Tasks

### 1. [Anomaly Detection](anomaly_detection/)
**Task:** Identify fraudulent or anomalous bank transactions  
**Dataset:** `bank_transactions_data_2.csv` (2,512 samples)  
**Algorithm:** Isolation Forest  
**Use Case:** Fraud detection, security monitoring

**Key Features:**
- Unsupervised anomaly detection
- Transaction behavior pattern analysis
- Binary anomaly labels (0 = normal, 1 = anomaly)

---

### 2. [Association Rule Mining](association_rule_mining/)
**Task:** Market basket analysis to find item purchase associations  
**Dataset:** `Groceries_dataset.csv` (38,765 transactions)  
**Algorithm:** Apriori  
**Use Case:** Product recommendations, cross-selling strategies

**Key Features:**
- Frequent itemset mining
- Association rules with support, confidence, and lift
- Customer purchase pattern insights

**⚠️ Note:** Requires Python 3.7–3.8 and PyCaret 2.x for `pycaret.arules` module

---

### 3. [Clustering](clustering/)
**Task:** Customer segmentation for targeted marketing  
**Dataset:** `segmentation data.csv` (2,000+ customers)  
**Algorithm:** K-Means Clustering  
**Use Case:** Market segmentation, personalized marketing

**Key Features:**
- Unsupervised customer grouping
- Elbow method and silhouette analysis
- 4 distinct customer segments
- PCA visualization

---

### 4. [Multiclass Classification](multiclass/)
**Task:** Predict student grade categories  
**Dataset:** `Student_performance_data _.csv`  
**Algorithm:** Auto-selected (compare 15+ models)  
**Use Case:** Educational analytics, early intervention

**Key Features:**
- Automated model comparison
- Multi-class grade prediction
- Interactive evaluation plots
- Confusion matrix and classification report

---

### 5. [Regression](regression/)
**Task:** Car price prediction for market entry strategy  
**Dataset:** `CarPrice_Assignment.csv`  
**Algorithm:** Auto-selected (compare 20+ models)  
**Use Case:** Pricing strategy, market analysis

**Key Features:**
- Feature importance analysis
- Price prediction with confidence intervals
- Business insights for automotive market
- Residual analysis

**Problem Context:** Geely Auto (Chinese company) entering US market

---

### 6. [Time Series Forecasting](time_series/)
**Task:** Weather forecasting with and without exogenous variables  
**Dataset:** `DailyDelhiClimateTrain.csv` (2013–2017)  
**Algorithms:** Auto-selected (ARIMA, ETS, Prophet, etc.)  
**Use Case:** Weather prediction, agricultural planning

**Key Features:**
- Two forecasting approaches:
  - Univariate (meantemp only)
  - Univariate with exogenous variables (humidity, wind, pressure)
- 14-day ahead forecasts
- Automated model selection

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+ (3.7–3.8 required for association rules)
- Jupyter Notebook or JupyterLab
- Git

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ykalathiya-2/pycaret_assignment.git
   cd pycaret_assignment
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install PyCaret:**
   ```bash
   # For most tasks (clustering, classification, regression, anomaly, time series)
   pip install "pycaret[analysis]"
   
   # For time series extras (Prophet, TBATS, etc.)
   pip install "pycaret[time_series]"
   
   # For association rules (requires Python 3.7-3.8)
   pip install "pycaret==2.3.10"  # Only in Python 3.8 environment
   ```

4. **Install Jupyter:**
   ```bash
   pip install jupyter
   ```

### Running Notebooks

Navigate to any task folder and launch the notebook:

```bash
cd anomaly_detection
jupyter notebook Anomaly_detection.ipynb
```

Or open the entire repository in JupyterLab:

```bash
jupyter lab
```

---

## 📊 Datasets Overview

| Task | Dataset | Samples | Target | Type |
|------|---------|---------|--------|------|
| Anomaly Detection | Bank Transactions | 2,512 | Anomaly Label | Unsupervised |
| Association Rules | Groceries | 38,765 | Item Associations | Unsupervised |
| Clustering | Customer Segmentation | 2,000+ | Cluster ID | Unsupervised |
| Multiclass | Student Performance | Varies | GradeClass | Supervised |
| Regression | Car Prices | Varies | Price | Supervised |
| Time Series | Delhi Climate | 1,462+ | meantemp | Forecasting |

---

## 🛠️ PyCaret Features Demonstrated

### AutoML Capabilities
- ✅ Automated model comparison
- ✅ Hyperparameter tuning
- ✅ Feature engineering and preprocessing
- ✅ Cross-validation
- ✅ Model evaluation and interpretation

### Workflows Covered
- **Setup:** Data preprocessing pipeline configuration
- **Compare Models:** Automatic model benchmarking
- **Create Model:** Train specific algorithms
- **Tune Model:** Hyperparameter optimization
- **Evaluate Model:** Interactive plots and metrics
- **Predict Model:** Generate predictions
- **Save/Load Model:** Model persistence
- **Finalize Model:** Train on full dataset

---

## 📝 Best Practices

### Model Files
- All `.pkl` model files are excluded from Git (see `.gitignore`)
- Models can be regenerated by running the notebooks
- For production use, store models in:
  - GitHub Releases
  - Cloud storage (S3, GCP, Azure)
  - Model registry (MLflow, DVC)

### Virtual Environments
- Use separate environments for different Python versions
- Association rules require Python 3.8 with PyCaret 2.x
- Other tasks work with Python 3.8–3.11 and PyCaret 3.x

### Reproducibility
- All notebooks use `session_id` for reproducible results
- Dataset files are version-controlled
- Preprocessing steps are documented

---

## 📚 References and Resources

### Official PyCaret Resources
- [PyCaret Documentation](https://pycaret.gitbook.io/docs/)
- [PyCaret GitHub](https://github.com/pycaret/pycaret)
- [PyCaret Tutorials](https://pycaret.gitbook.io/docs/get-started/tutorials)

### Tutorials Used
- [Clustering Tutorial](https://nbviewer.org/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Clustering.ipynb)
- [Anomaly Detection Tutorial](https://nbviewer.org/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Anomaly%20Detection.ipynb)
- [Time Series Tutorial](https://colab.research.google.com/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Time%20Series%20Forecasting.ipynb)
- [Association Rules Demo](https://github.com/pycaret/pycaret-demo-queens/blob/main/PyCaret%20Association%20Rule.ipynb)

---

## 🎓 Learning Outcomes

By completing these notebooks, you will learn:
- ✅ Low-code ML with PyCaret
- ✅ End-to-end ML workflows (data → model → deployment)
- ✅ Model comparison and selection
- ✅ Evaluation metrics for different task types
- ✅ Best practices for reproducible ML
- ✅ Handling different data types (tabular, time series, transactional)

---

## ⚠️ Important Notes

### Python Version Compatibility
- **PyCaret 3.x** (latest): Python 3.8–3.11
  - Clustering, Classification, Regression, Anomaly Detection, Time Series
- **PyCaret 2.x** (legacy): Python 3.7–3.8
  - Association Rules (only available in 2.x)

### Environment-Specific Issues
If you encounter `ModuleNotFoundError: No module named 'pycaret.arules'`:
- You are using PyCaret 3.x (Python 3.11)
- Create a Python 3.8 environment with PyCaret 2.3.10 for association rules
- See `association_rule_mining/README.md` for detailed instructions

### Git LFS / Large Files
- Model files (`.pkl`) are excluded via `.gitignore`
- If you need to share models, use GitHub Releases or cloud storage
- The repository was cleaned using `git-filter-repo` to remove large files from history

---

## 🤝 Contributing

This repository is for educational purposes. If you find issues or have suggestions:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

## 📄 License

This project is for educational use. Datasets and code are used for learning purposes only.

### Dataset Attributions
- **Bank Transactions:** Synthetically generated for fraud detection analysis
- **Groceries:** Market basket analysis dataset
- **Customer Segmentation:** Demographic and economic survey data
- **Student Performance:** Educational analytics dataset
- **Car Prices:** Automotive market data (Geely Auto case study)
- **Delhi Climate:** Weather Underground API (PES University assignment)

---

## 👨‍💻 Author

**Yash Kalathiya**  
GitHub: [@ykalathiya-2](https://github.com/ykalathiya-2)

---
