
# CryptoClustering

## Overview
CryptoClustering is a data science project that applies K-means clustering and Principal Component Analysis (PCA) to classify cryptocurrencies based on their price fluctuations over various timeframes. The goal is to explore patterns in the cryptocurrency market using clustering techniques and dimensionality reduction for a better understanding of market trends.

## Project Structure
- `Resources/crypto_market_data.csv`: Contains the cryptocurrency market data, including price change percentages over different time periods.
- `Crypto_Clustering.ipynb`: Jupyter notebook that contains the full code for loading, preparing, and analyzing the data.

## Workflow
1. **Data Preparation**: Load the data, normalize it using `StandardScaler` from `scikit-learn`, and inspect the summary statistics.
2. **Finding the Optimal k**: Use the elbow method to determine the best number of clusters (`k`) for the K-means algorithm using both the original scaled data and PCA-reduced data.
3. **K-means Clustering**:
   - Cluster cryptocurrencies using the best `k` value found from the original scaled data.
   - Cluster the PCA-reduced data using the optimal `k` value.
4. **Principal Component Analysis (PCA)**: Reduce the data to three principal components and analyze the total explained variance.
5. **Visualizations**: Create scatter plots to visualize the clustered data and analyze the impact of clustering with and without dimensionality reduction.
6. **Feature Weights Analysis**: Determine which features have the strongest positive or negative influence on each principal component.

## Requirements
- Python 3.8+
- Libraries: `pandas`, `scikit-learn`, `matplotlib`, `hvplot`, `numpy`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/CryptoClustering.git
   ```
2. Change directory:
   ```bash
   cd CryptoClustering
   ```
3. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
- Run the `Crypto_Clustering.ipynb` notebook to see the analysis and visualizations.
- Use the provided dataset to explore different clustering methods and visualize the results.

## Results
- The elbow method identified `k = 4` as the optimal number of clusters using both the original scaled data and PCA data.
- PCA reduced the dimensionality while retaining approximately 89.5% of the original variance, simplifying the clustering process.
- Clustering results were visualized using scatter plots, allowing for better understanding of how cryptocurrencies are grouped based on their price change percentages.

## Key Insights
- **K-means Clustering** is an effective method for grouping cryptocurrencies based on historical price fluctuations.
- **PCA** allows for dimensionality reduction while preserving most of the variance, making it easier to visualize and interpret clusters.
- **Feature Weights** analysis highlights which time intervals have the most influence on the clustering process.

## Contributing
Contributions are welcome! If you have suggestions for improvement or new features, please create an issue or submit a pull request.
