# CryptoClustering

In this project, we apply Python and unsupervised learning techniques to explore if cryptocurrency prices are affected by 24-hour or 7-day changes.

## Project Setup

1. **Create a New Repository**: Set up a new repository called `CryptoClustering`.
2. **Clone & Push**: Clone the repo to your local machine and push all changes to GitHub.

## Instructions

### Step 1: Data Preparation
- Load `crypto_market_data.csv` into a DataFrame.
- Examine the data with summary statistics and plots.

### Step 2: Data Scaling
- Use `StandardScaler` from `scikit-learn` to normalize the data.
- Create a DataFrame with scaled data, setting `coin_id` as the index.

### Step 3: Finding Optimal Clusters
1. **Using the Scaled Data**:
   - Use the Elbow method to determine the best `k` by calculating inertia for `k` values from 1 to 11.
   - Plot the Elbow curve and determine the optimal `k`.

2. **Clustering**:
   - Apply K-means clustering with the optimal `k` and visualize the clusters using `hvPlot`.
   - Set `price_change_percentage_24h` and `price_change_percentage_7d` on the axes, color points by clusters, and display `coin_id` on hover.

### Step 4: Principal Component Analysis (PCA)
- Perform PCA to reduce the scaled data to three principal components.
- Calculate and interpret the explained variance for the components.

### Step 5: Clustering with PCA Data
1. **Finding Optimal k with PCA**:
   - Repeat the Elbow method on the PCA data.
   - Compare the optimal `k` with the original scaled data.

2. **Clustering**:
   - Use K-means with the optimal `k` on PCA data, then plot clusters with `PC1` and `PC2` as axes.

### Analysis
- Discuss the impact of using PCA versus full feature data in clustering.

## Technologies Used
- **Python Libraries**: `Pandas`, `scikit-learn`, `hvPlot`
- **Clustering Algorithm**: K-means
- **Dimensionality Reduction**: PCA

## License
MIT License
