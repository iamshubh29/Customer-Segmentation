# Customer Segmentation with Clustering

This project focuses on clustering customer data from a mall to analyze patterns in spending and income behavior using different clustering techniques. The dataset consists of customer IDs, gender, age, annual income, and spending scores. Below is a detailed breakdown of the workflow, techniques used, and results.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Data Preprocessing](#data-preprocessing)
4. [Clustering Techniques](#clustering-techniques)
5. [Results](#results)
6. [Steps to Reproduce](#steps-to-reproduce)
7. [Future Work](#future-work)

---

## Project Overview

The goal of this project is to segment customers into different clusters based on their **Annual Income** and **Spending Score**. By applying clustering algorithms such as K-Means, Gaussian Mixture Models (GMM), DBSCAN, and HDBSCAN, we aim to discover meaningful groups within the data.

---

## Technologies Used

- **Python Libraries:**
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `hdbscan`
  - `PCA`

---

## Data Preprocessing

1. Loaded the dataset from `Mall_Customers.csv`.
2. Checked and handled missing values.
3. Selected relevant features (**Annual Income** and **Spending Score**).
4. Standardized the data using `StandardScaler` to ensure uniform scaling.

---

## Clustering Techniques

### 1. K-Means Clustering

- Used the **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters.
- Final number of clusters: **5**.
- Best Silhouette Score: **0.554**.

### 2. Gaussian Mixture Models (GMM)

- Used to handle overlapping clusters probabilistically.
- Optimal number of components: **5**.
- Best Silhouette Score: **0.557**.

### 3. DBSCAN

- A density-based clustering algorithm.
- Determined `eps` parameter using the k-distance graph.
- Best Silhouette Score: **0.388**.

### 4. HDBSCAN

- A hierarchical density-based clustering algorithm.
- Automatically determined clusters.
- Best Silhouette Score: **0.602**.

---

## Results

| Algorithm | Best Silhouette Score | Number of Clusters |
| --------- | --------------------- | ------------------ |
| K-Means   | 0.554                 | 5                  |
| GMM       | 0.557                 | 5                  |
| DBSCAN    | 0.388                 | Varies             |
| HDBSCAN   | 0.602                 | Automatic          |

### Visualization of Clusters

1. **K-Means Clustering:** Distinct 5 clusters visualized with centroids.
2. **Gaussian Mixture Models:** Smooth transitions between clusters.
3. **DBSCAN:** Detected noise and dense regions.
4. **HDBSCAN:** Best performance with the least noise.

---

## Steps to Reproduce

1. Install the required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn hdbscan
   ```
2. Place the `Mall_Customers.csv` file in the project directory.
3. Run the Python script provided above.
4. Visualize and analyze the clusters using the plotted graphs.

---

## Future Work

- Extend the analysis by incorporating additional features such as **Age** or **Gender**.
- Experiment with advanced clustering methods like **Spectral Clustering**.
- Implement clustering in real-time using interactive dashboards.

---


