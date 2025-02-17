# Crypto Clustering Project

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/downloads/release/python-380/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](https://opensource.org/license/mit)

This project utilizes clustering techniques to analyze and classify cryptocurrency market data. Using advanced data analysis and visualization methods, the project aims to uncover patterns and trends in the cryptocurrency market.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Files in the Repository](#files-in-the-repository)
- [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Results](#results)
- [Visuals](#visuals)
- [FAQs](#faqs)
- [License](#license)

## Overview
The primary goal of this project is to perform clustering analysis on cryptocurrency market data to group assets with similar behaviors and characteristics. The project includes data preprocessing, dimensionality reduction, clustering, and visualization.

## Dataset
The dataset used for this analysis contains cryptocurrency market data, including various metrics such as trading volume, market cap, and price changes over time.

- **Source**: Uploaded CSV file (`crypto_market_data.csv`)
- **Key Features**:
  - Cryptocurrency symbols
  - Market capitalization
  - Volume traded
  - Percent changes over different time frames

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/YourRepoName.git
   cd YourRepoName
   ```
2. Install required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Crypto_Clustering.ipynb
   ```
2. Run the notebook cells sequentially to preprocess the data, apply clustering algorithms, and visualize the results.
3. Analyze the clustering outputs to draw insights about cryptocurrency groupings.

## Files in the Repository
- **Crypto_Clustering.ipynb**: Main Jupyter Notebook for clustering analysis.
- **crypto_market_data.csv**: Dataset containing cryptocurrency market information.
- **requirements.txt**: File containing the required Python libraries.

## Technologies Used
- **Python**:
  - Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- **Jupyter Notebook** for interactive development and visualization

## Project Workflow
1. **Data Preprocessing**:
   - Load and inspect the dataset.
   - Handle missing values and clean the data.
   - Scale the features to normalize the data.

2. **Dimensionality Reduction**:
   - Apply PCA (Principal Component Analysis) to reduce the feature space.

3. **Clustering Analysis**:
   - Implement clustering algorithms such as K-Means and Hierarchical Clustering.
   - Optimize the number of clusters using metrics like the elbow method.

4. **Visualization**:
   - Visualize clusters in two or three dimensions.
   - Generate plots to analyze the clustering results.

## Results
- Clustering analysis provided insights into groups of cryptocurrencies with similar market behavior.
- Key visualizations helped identify patterns and relationships in the data.

## Visuals
This section showcases the visuals generated during the analysis.

### **Elbow Method**
![image](https://github.com/user-attachments/assets/88a8bee9-686b-4e34-b501-7a716632ac30)


*Figure 1: Elbow Method graph showing inertia for different cluster counts in the original data vs. Elbow Method graph showing inertia for different cluster counts in the PCA-transformed data.*

### **Cluster Visualizations**
![image](https://github.com/user-attachments/assets/33248f79-01a8-451c-9191-020d8263a60e)


*Figure 2: Clusters visualized in the original data space vs. Clusters visualized in the PCA-transformed data space.*

## FAQs

### **What is the best value for `k`?**
The best value for `k` appears to be 4, as there is a noticeable drop in inertia before the curve starts to flatten significantly. This indicates an optimal balance between reducing inertia and maintaining simplicity. However, `k=6` and `k=7` also show decent potential as they lie in the flatter part of the curve, suggesting diminishing returns in inertia reduction with higher cluster numbers.

### **What is the total explained variance of the three principal components?**
The total explained variance of the three principal components is calculated by summing their individual explained variance values:

0.37269822 + 0.32489961 + 0.18917649 = 0.88677432

Therefore, the total explained variance is 0.8868 (rounded to 4 decimal places) or 88.68%.

### **What is the best value for `k` when using the PCA data?**
The best value for `k` when using the PCA data remains `k=4` (inertia = 43.586). This suggests that four clusters provide an optimal balance of simplicity and effectiveness after dimensionality reduction.

### **Does it differ from the best `k` value found using the original data?**
No, the best `k` value is consistent between the original data and the PCA-transformed data (both are `k=4`). However, the PCA-transformed data achieves a lower inertia (43.586 vs. 79.022 in the original data), indicating better-defined and more compact clusters due to reduced dimensional noise.

### **After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?**
The "k Clusters" based on the original data are more scattered and dispersed, which can make it harder to distinguish clear patterns between clusters. In contrast, the "k Clusters in PCA" are more compact and better separated, making the differences between clusters more noticeable.

One key observation is the difference in cluster assignments for "coin_id: ethlend," which is assigned to cluster 1 in "k Clusters" but cluster 2 in "k Clusters in PCA." This indicates that dimensionality reduction can affect cluster assignments and potentially improve the interpretability of the results.

After experimenting with different cluster counts, the 4-cluster solution seems to be the optimal choice for both the original and PCA-transformed data, as it balances clarity and compactness effectively.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

---

Feel free to contribute to the project by submitting issues or pull requests!
