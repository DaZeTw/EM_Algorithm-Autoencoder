# Clustering and Dimensionality Reduction using EM Algorithm and Autoencoders

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Conclusion](#conclusion)

## Overview

This project investigates scenarios where the relationship between features is non-linear or data contains multiple clusters, each exhibiting different feature relationships. We develop methods for combining multiple Principal Component Analyses (PCAs) using the Expectation-Maximization (EM) algorithm and introduce constraints to an Autoencoder neural network to mimic PCA. The project involves the use of Python and PyTorch with simulated data, specifically the Vehicle Silhouettes dataset.

### Dataset Overview

The dataset used in this project is the **Vehicle Silhouettes dataset**, which contains various geometric features of different vehicles. These features are used to distinguish between different classes of vehicles.

**Features:**

- COMPACTNESS
- CIRCULARITY
- DISTANCE CIRCULARITY
- RADIUS RATIO
- PR.AXIS ASPECT RATIO
- MAX.LENGTH ASPECT RATIO
- SCATTER RATIO
- ELONGATEDNESS
- PR.AXIS RECTANGULARITY
- MAX.LENGTH RECTANGULARITY
- SCALED VARIANCE_MAJOR
- SCALED VARIANCE_MINOR
- SCALED RADIUS OF GYRATION
- SKEWNESS ABOUT_MAJOR
- SKEWNESS ABOUT_MINOR
- KURTOSIS ABOUT_MAJOR
- KURTOSIS ABOUT_MINOR
- HOLLOWS RATIO

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/DaZeTw/EM_Algorithm-Autoencoder.git
   cd your-repo-name
   ```

2. **Create a virtual environment** (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

### Google Colab Notebook

For an interactive version of this project, you can view and run the code in Google Colab: [Google Colab Notebook](https://colab.research.google.com/drive/1W4hDpCZWxVnid2cdDIJsBIYyGe4r_sYE?usp=sharing)

## Usage

1. **Data Preprocessing**: Load and preprocess the dataset.
2. **Dimensionality Reduction**: Apply PCA and Kernel PCA.
3. **Clustering**: Perform clustering using K-Means, EM algorithm, and Gaussian Mixture Models.
4. **Autoencoders**: Train and evaluate autoencoders for dimensionality reduction.

### Running the Script

To run the main script, use:

```bash
python Clustering_and_Dimensionality_Reductio.py
```

## Results

#### Clustering Metrics

- Adjusted Rand Index (ARI): Measures the similarity between true labels and predicted labels.
- Normalized Mutual Information (NMI): Measures the mutual dependence between true labels and predicted labels.
- Silhouette Score: Measures how similar an object is to its own cluster compared to other clusters.
- Davies-Bouldin Index (DB): Measures the average similarity ratio of each cluster with its most similar cluster.

#### Evaluation Results

- K-Means: Achieves the best silhouette score and DB index.
- K-Means Initialization: Shows the best ARI.
- Random Initialization: Provides high ARI and NMI.
- Hierarchical Initialization: Performs worse across most metrics.
- Gaussian Mixture Model: Exhibits high NMI and a good silhouette score.

#### Dimensionality Reduction

- PCA: Effective for linear patterns with high explained variance.
- Simple Autoencoder: Capable of capturing complex, non-linear patterns but requires careful tuning.
- PCA Autoencoder: Balances capturing variance and maintaining linear interpretability.

#### Key Observations

- The choice of initialization method significantly impacts clustering performance.
- PCA remains a robust baseline for linear patterns, while advanced methods like autoencoders offer significant advantages for non-linear relationships.

## Conclusion

The project demonstrates the importance of selecting appropriate methods and initialization strategies for effective clustering and dimensionality reduction. Future work could explore further optimization and application to different datasets.
