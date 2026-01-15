# Customer Segmentation using Hierarchical Clustering

A strategic marketing analytics project that employs unsupervised machine learning to group customers into distinct segments. By using Hierarchical Clustering, the system identifies natural groupings in consumer behavior without requiring a pre-defined number of clusters.

## Overview

Hierarchical Clustering is a powerful unsupervised learning method that builds a tree of clusters. This project focuses on the **Agglomerative (Bottom-Up)** approach, where each data point starts as its own cluster and pairs are merged iteratively based on similarity. This is particularly useful for market segmentation where the relationship between different groups is as important as the groups themselves.

## Dataset

- **Source:** Customer Marketing Dataset (`31_hierarchical_clustering_data.csv`).
- **Key Features:**
  - `CustomerID`: Unique identifier.
  - `Annual_Income`: Yearly earnings of the customer.
  - `Spending_Score`: A score assigned by the system based on customer behavior and purchasing nature.
  - `Age` & `Region`: Demographic and geographic metadata.

## Objectives

- Understand the difference between **Agglomerative** (Bottom-up) and **Divisive** (Top-down) clustering.
- Utilize **Dendrograms** to visualize the merging process and identify the "optimal" number of clusters.
- Apply **Feature Selection** to focus on the most impactful variables (Income vs. Spending).
- Implement the model using the **Ward Linkage** method to minimize within-cluster variance.

## Methods and Analysis

The project follows a structured unsupervised learning pipeline:

- **Dendrogram Analysis**
  - The "DNA" of the hierarchical model. By observing the longest vertical distance not crossed by any horizontal line, we determine the natural number of segments in the customer base.



- **Agglomerative Clustering Implementation**
  - Using the `AgglomerativeClustering` algorithm to group data points.
  - Experimenting with different linkage criteria to see how cluster boundaries shift.



- **Segment Visualization**
  - Plotting the resulting clusters on a 2D scatter plot (Annual Income vs. Spending Score).
  - Defining the personas: e.g., "High Earners/Low Spenders" (Careful), "High Earners/High Spenders" (Target), etc.

- **Business Insights**
  - Evaluating how a marketing team can use these clusters to tailor email campaigns, loyalty rewards, or regional promotions.

## Tech Stack

- **Language:** Python 3
- **Libraries:**
  - `pandas` and `numpy`: Data processing.
  - `scipy.cluster.hierarchy`: Specific tools for building and plotting dendrograms.
  - `scikit-learn`: Implementation of the Agglomerative model.
  - `matplotlib` and `seaborn`: Visualization of segments.
- **Environment:** Jupyter / Google Colab

## How to Run

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/customer-segmentation-hierarchical.git
   cd customer-segmentation-hierarchical

2. *Create and activate a virtual environment (optional but recommended):*
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate

3. *Install dependencies:*
   pip install pandas numpy matplotlib seaborn scikit-learn scipy

4. *Open the notebook:*
   jupyter notebook 31_Hierarchical_clustering_customer_segmentation_formarketing_good.ipynb

5. Ensure the dataset is present: Place 31_hierarchical_clustering_data.csv in the root folder.
