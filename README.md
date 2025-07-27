# 🧠 Customer Segmentation Analysis with K-means, Hierarchical, and Market Basket Analysis

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📋 Project Overview
This project implements a **customer segmentation analysis** pipeline using **K-means clustering**, **hierarchical clustering**, and **market basket analysis**. It leverages professional datasets from Kaggle to segment customers based on demographic and spending behavior and identify purchasing patterns. The pipeline includes data preprocessing, clustering, association rule mining, and visualizations, all implemented in Python for Google Colab.

---

## 🎯 Objectives
- Segment customers based on demographic and behavioral features
- Implement and compare K-means and hierarchical clustering
- Identify frequent itemsets and association rules via market basket analysis
- Evaluate clustering performance using elbow method and silhouette scores
- Visualize clusters, dendrograms, and association rules

---

## 📊 Dataset Information
**Datasets**:
1. **Mall Customer Segmentation Data** ([Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python))
   - **Size**: ~200 customers
   - **Files**:
     - `Mall_Customers.csv`: Customer data (CustomerID, Gender, Age, Annual_Income, Spending_Score)
   - **Target Output**: Customer segments based on Age, Annual_Income, and Spending_Score
   - **Techniques**: K-means and hierarchical clustering
2. **Online Retail Dataset** ([Kaggle](https://www.kaggle.com/datasets/carrie1/ecommercedata))
   - **Size**: ~500,000 transactions
   - **Files**:
     - `Online_Retail.csv`: Transaction data (InvoiceNo, Description, Quantity, etc.)
   - **Target Output**: Association rules for product purchases
   - **Technique**: Market basket analysis with Apriori algorithm

---

## 🔧 Technical Implementation

### 📌 Analysis Techniques
- **K-means Clustering**: Partitions customers into clusters based on standardized features
- **Hierarchical Clustering**: Builds a hierarchy of clusters using Ward’s linkage
- **Market Basket Analysis**: Identifies frequent itemsets and association rules using Apriori

### 🧹 Data Preprocessing
- **Mall Customer Data**:
  - Standardize `Age`, `Annual_Income`, and `Spending_Score`
  - Encode `Gender` (optional for clustering)
- **Online Retail Data**:
  - Filter out cancellations and missing values
  - Create binary basket matrix (invoices vs. items)

### ⚙️ Modeling
- **K-means**: Elbow method and silhouette scores to determine optimal clusters
- **Hierarchical**: Ward’s linkage with dendrogram visualization
- **Apriori**: Minimum support of 0.03 and lift threshold of 1.0 for association rules

### 📏 Evaluation Metrics
- **Clustering**:
  - Inertia (elbow method)
  - Silhouette score
- **Market Basket Analysis**:
  - Support, confidence, and lift for association rules

### 📊 Visualizations
- Elbow and silhouette plots for K-means
- Dendrogram for hierarchical clustering
- Scatter plot of clusters (Annual_Income vs. Spending_Score, sized by Age)
- Support vs. confidence scatter plot for association rules

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Google Colab or Jupyter Notebook

### Installation
Clone the repository:
```bash
git clone https://github.com/zubair-csc/005-Customer-Segmentation-Analysis-_K_means_hierarchical_markt_Basket.git
cd 005-Customer-Segmentation-Analysis-_K_means_hierarchical_markt_Basket
```

Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy mlxtend
```

### Dataset Setup
1. Download datasets:
   - [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
   - [Online Retail Dataset](https://www.kaggle.com/datasets/carrie1/ecommercedata)
2. Upload `Mall_Customers.csv` and `Online_Retail.csv` to Google Colab or place them in your project directory.
3. Update file paths in the script if necessary.

### Running the Script
1. Open `customer_segmentation_kaggle.py` in Google Colab or a Python environment.
2. Run the script to perform clustering and market basket analysis.
3. View outputs: cluster profiles, visualizations, and association rules.

---

## 📈 Results
- **K-means Clustering**: Segments customers into 5 clusters based on Age, Annual_Income, and Spending_Score
- **Hierarchical Clustering**: Similar segmentation with dendrogram visualization
- **Market Basket Analysis**: Identifies top product associations (e.g., items frequently purchased together)
- **Visualizations**: Clear plots for cluster analysis and association rule metrics

---

## 🙌 Acknowledgments
- Kaggle for providing the datasets
- Libraries: `pandas`, `numpy`, `scikit-learn`, `scipy`, `mlxtend`, `matplotlib`, `seaborn`
