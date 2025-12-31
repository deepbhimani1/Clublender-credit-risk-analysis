# Credit-risk-analysis

This repository contains the code and analysis for a data mining project focusing on clustering, outlier detection, and classification.

## Repository Map

```
├── CREDIT_RISK_ANALYSIS.ipynb                    # Main Jupyter Notebook containing all analysis
├── EDA_Preprocessing.ipynb                       # Initial EDA and preprocessing workflow
├── final_report.pdf                              # Final 2-page project report
├── LoanData_sample.csv                           # Reduced sample of the original loan dataset used for EDA
├── X_scaled_pca.csv                              # Preprocessed PCA features (Required for Clustering/LOF)
├── X_unscaled.csv                                # Raw features (Required for XGBoost Classification)
├── y.csv                                         # Target labels (0 = Fully Paid, 1 = Charged Off)
├── README.md                                     # Project documentation
```

## Environment & Dependencies

This project requires **Python 3.9 up to max 3.10**.

**Critical Note:** To ensure scikit-learn-extra (used for K-Medoids) functions associated with numpy correctly, you must install a Numpy version lower than 2.0.0.

### Required Libraries

- **Core:** numpy (< 2.0.0), pandas
- **Visualization:** matplotlib, seaborn
- **Machine Learning:** scikit-learn, scikit-learn-extra (for KMedoids), xgboost
- **Dimensionality Reduction:** TSNE (from sklearn.manifold), PCA
- **Environment:** jupyter

## Setup Instructions

You can set up the environment directly using the command line.

1. Clone or Download this repository.

2. Open your terminal (Command Prompt, PowerShell, or Terminal).

3. Install dependencies by running the following command:

   ```bash
   pip install "numpy<2.0.0" pandas scikit-learn scikit-learn-extra matplotlib seaborn xgboost jupyter
   ```

   **Note:** The quotes around `"numpy<2.0.0"` are often required in ZSH (Mac/Linux) to prevent syntax errors, but they work in Windows as well.

## Data Access
The notebook loads the following project-generated CSVs:
- X_unscaled.csv
- X_scaled_pca.csv
- y.csv

No additional raw dataset download is required.
The notebook is configured to load data relative to the project root.

## How to Run

1. Navigate to the project folder in your terminal:
   ```bash
   cd path/to/repo
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Open `CREDIT_RISK_ANALYSIS.ipynb` from the dashboard.

4. Run all cells sequentially (**Cell > Run All**) to perform the data cleaning, clustering, and model evaluation.

## Analysis Overview

The notebook covers the following workflow:

- **Preprocessing:** Data cleaning and RFE, SelectKBest, fisher score, Mutual Information.
- **Clustering:** Implementation of K-Means, K-Medoids, and Agglomerative Hierarchical Clustering.
- **Outlier Detection:** Implementation of Local Outlier Factor (LOF), Clustering-Based, and Distance-Based
- **Classification:** Implementation of Random Forest Classifier, XGBoost, and Logistic Regression. All with hyperparameter tuning and feature selection.
- **Visualization:** PCA, t-SNE, ROC curves, and correlation matrix.
