# PISA PERFORMANCE SCORES ANALYSIS📊

## Overview

This project involves analyzing and modeling the **PISA Performance Scores by Country** dataset. The goal is to identify clusters of countries based on educational performance using KMeans clustering and then build classification models to predict cluster membership. The project includes a comparison of Logistic Regression and Random Forest models to evaluate their performance.

## Project Structure

- **[Clustering].ipynb**: Jupyter Notebook for clustering analysis.  
- **[Classification].ipynb**: Jupyter Notebook for classification tasks.  
- **dataset_clustering.csv**: Dataset of PISA performance scores by country, used for clustering.  
- **dataset_classification.csv**: Dataset generated from clustering, used for classification.  
- **requirements_clustering.txt**: File containing required Python libraries for clustering.  
- **requirements_classification.txt**: File containing required Python libraries for classification.  

## Project Workflow

### Step 1: Clustering with KMeans
Performed KMeans clustering on the PISA Performance Scores dataset to group countries based on educational performance. Two clusters were identified with the following characteristics:

#### **Cluster 1**  
- **PISA Score**: 502.72 (high performance)  
- **Location Index**: 22.55 (distributed across regions)  
- **Analysis**: Represents countries with high educational performance, often found in regions such as Western Europe, East Asia, and other OECD countries.

#### **Cluster 2**  
- **PISA Score**: 421.22 (low performance)  
- **Location Index**: 20.90 (more concentrated geographically)  
- **Analysis**: Represents countries with lower educational performance, likely from regions with limited educational resources, such as Sub-Saharan Africa, South Asia, or parts of Latin America.

### Step 2: Classification and Model Comparison
Used the dataset generated from clustering to predict cluster membership. Two machine learning models, Logistic Regression and Random Forest, were built and compared.

#### Results:
1. **Random Forest**  
   - **Performance**: Perfect accuracy, F1-Score, Precision, and Recall (100%) before and after tuning.  
   - **Conclusion**: Consistently reliable and highly effective for this dataset.  

2. **Logistic Regression**  
   - **Performance**: Initially very high accuracy (~99.76%) but experienced a slight drop after tuning (~95.9%).  
   - **Conclusion**: Effective but slightly less robust compared to Random Forest.  

## Setup Instructions

### Prerequisites
- Python 3.10 or higher
- Jupyter Notebook

### Environment Setup
#### For Clustering
```bash
conda create --name pisa_clustering_env python=3.10
conda activate pisa_clustering_env
pip install -r req_clustering.txt
```

#### For Classification
```bash
conda create --name pisa_classification_env python=3.10
conda activate pisa_classification_env
pip install -r req_classification.txt
```

## How to Run

### Step 1: Clustering
1. Clone the repository:  
   ```bash
   git clone https://github.com/ngaeninurul/pisa_performance_scores.git
   cd pisa_performance_scores
   ```
2. Open and run the `[Clustering]` notebook:  
   ```bash
   jupyter notebook
   ```

### Step 2: Classification
1. Navigate to the `[Classification]` notebook.  
2. Execute the notebook to compare Logistic Regression and Random Forest models.
