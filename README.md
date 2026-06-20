# QuickDraw10: Dimensionality Reduction & Image Clustering

This repository contains an unsupervised machine learning pipeline for clustering images from **QuickDraw10**, a curated subset of the Google QuickDraw dataset (a modern alternative to MNIST). 

Developed as part of a Computer Science academic project at Amirkabir University of Technology, this project explores how different dimensionality reduction techniques and centroid initialization strategies affect the performance of K-Means clustering on image data.

## Key Concepts Explored
* **Dimensionality Reduction:** Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA).
* **Clustering:** K-Means algorithm implementation and tuning.
* **Centroid Initialization:** Comparing random initialization against deterministic class-mean initialization.
* **Variance Analysis:** Reconstructing images using PCA components that capture 95% of the data variance.
* **Cluster Evaluation:** Visualizing class distributions within clusters using 2D/3D scatter plots and bar graphs.

## Repository Structure
```text
quickdraw-clustering/
│
├── data/                  # (Ignored in Git) Store the QuickDraw10 dataset here
├── notebooks/             # Jupyter notebooks with full ML pipelines
│   └── quickdraw_analysis.ipynb
├── .gitignore             # Strict ignore rules for massive dataset files
└── README.md              # Project documentation
```

## Project Workflow

This project is broken down into the following analytical steps:
PCA & LDA Projections: Reducing the dataset dimensions and projecting the samples onto their first 2 and 3 principal components, followed by an LDA projection for comparison.  
K-Means with Random Initialization: Clustering the data using the first two principal components with $K=3, 7, 10$ and plotting the final centroids.
K-Means with Mean Initialization: Re-running the clusters by manually setting the initial centroids to the exact mathematical means of specific class groupings to observe convergence differences.
95% Variance Reconstruction: Finding the optimal number of principal components to capture 0.95 variance, and visually comparing the reconstructed images to the original hand-drawn samples.  
Full 10-Cluster Analysis: Executing K-Means with $K=10$ on the optimal feature space, visualizing 100 random samples, and generating bar graphs to evaluate the actual class distribution within each discovered cluster.