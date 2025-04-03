# Dimensionality Reduction Exploration

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains a comprehensive Jupyter Notebook that demonstrates step-by-step applications of three popular dimensionality reduction techniques: **Principal Component Analysis (PCA)**, **t-SNE**, and **UMAP**.

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Technical Details](#technical-details)
  - [PCA](#pca)
  - [t-SNE](#t-sne)
  - [UMAP](#umap)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contact](#contact)

## Overview

Dimensionality reduction is a crucial step in data preprocessing, particularly when dealing with high-dimensional datasets. This repository explores three widely-used techniques:

- **PCA**: A linear method that transforms the data into a new coordinate system by finding the directions (principal components) that maximize the variance. The first principal component captures the greatest variance, while subsequent components capture the remaining variance under the constraint of orthogonality.
  
- **t-SNE**: A non-linear technique designed primarily for visualizing high-dimensional data. It works by converting similarities between data points to joint probabilities and then minimizing the Kullback-Leibler divergence between these probabilities in the high-dimensional and low-dimensional spaces. t-SNE is particularly adept at preserving local structure.
  
- **UMAP**: A more recent non-linear dimensionality reduction algorithm that balances the preservation of both local and global structure. UMAP leverages manifold learning techniques to create a fuzzy topological representation of the data, often resulting in clear cluster separation.

The notebook demonstrates these techniques in three parts:
1. **Part I**: Application of PCA on a synthetic 2D dataset.
2. **Part II**: PCA on the real-world Iris dataset.
3. **Part III**: A comparison of t-SNE, UMAP, and PCA on a synthetic 3D dataset.

Each section provides detailed explanations, code examples, and visualizations to help you understand the underlying mechanics and trade-offs of each algorithm.

## Repository Structure

```
Dimensionality-Reduction-Exploration/
├── Dimensionality_Reduction.ipynb  # Main Jupyter Notebook with all experiments
├── README.md                       # This file
└── LICENSE                         # MIT License
```

- **Dimensionality_Reduction.ipynb**: Contains the complete walkthrough of PCA, t-SNE, and UMAP including theory, code implementations, and visualizations.
- **LICENSE**: The project is licensed under the MIT License.

## Technical Details

### PCA

- **Theory**:  
  PCA identifies the directions of maximum variance in the data and projects the data onto a new subspace defined by these directions. The first principal component accounts for the highest variance, with each subsequent component capturing less variance while being orthogonal to the previous ones.
  
- **Implementation**:  
  - **Synthetic 2D Data**: A bivariate normal distribution is used to generate data, then PCA is applied to find and visualize the principal components.
  - **Iris Dataset**: PCA reduces the four-dimensional Iris data to two dimensions to visualize the separability of the species. Detailed code calculates explained variance ratios and demonstrates data projection.

### t-SNE

- **Theory**:  
  t-SNE is a non-linear technique focused on preserving local relationships. It converts pairwise similarities between data points into probabilities and minimizes the divergence between these probabilities in high- and low-dimensional spaces. Parameters like perplexity and maximum iterations can greatly influence the results.
  
- **Implementation**:  
  Applied on a standardized synthetic 3D dataset, the notebook shows how to adjust t-SNE parameters (e.g., perplexity = 30) and visualizes the resulting 2D embedding to highlight local cluster structures.

### UMAP

- **Theory**:  
  UMAP (Uniform Manifold Approximation and Projection) is based on manifold learning and topological data analysis. It seeks to preserve both local and global data structure by creating a fuzzy topological representation of the high-dimensional data.
  
- **Implementation**:  
  UMAP is applied to the same standardized synthetic 3D dataset. The notebook covers parameter tuning (e.g., `min_dist=0.5`, `spread=1`) and provides a detailed visualization of the 2D projection, comparing its performance with t-SNE and PCA.

## Installation

To run the notebook, ensure you have Python 3 installed along with the following libraries:
- numpy
- pandas
- matplotlib
- scikit-learn
- plotly
- umap-learn

You can install these dependencies using pip:

```bash
pip install numpy pandas matplotlib scikit-learn plotly umap-learn
```

## Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/runciter2078/Dimensionality-Reduction-Exploration.git
   ```

2. **Navigate to the Repository Directory:**

   ```bash
   cd Dimensionality-Reduction-Exploration
   ```

3. **Open the Jupyter Notebook:**

   ```bash
   jupyter notebook Dimensionality_Reduction.ipynb
   ```

4. **Run the Cells:**  
   Execute the cells sequentially in the notebook to explore the dimensionality reduction techniques and view the generated visualizations.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, please feel free to open an issue in the repository or contact the project maintainer.

**Repository URL:** [https://github.com/runciter2078/Dimensionality-Reduction-Exploration/tree/main](https://github.com/runciter2078/Dimensionality-Reduction-Exploration/tree/main)
```
