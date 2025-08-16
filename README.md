# A Clustering of Residuals for Efficient Data Selection Method for Sparse Gaussian Process Models

This repository presents a comprehensive evaluation of various data selection methods for machine learning, with a focus on addressing the computational challenges of **Gaussian Processes (GPs)** on large datasets. It introduces a novel approach called **CORE (Clustering of Residuals for Efficient data selection)** and compares its performance against several established baselines.

The project's analysis, code, and results are all contained within a single Jupyter Notebook for ease of viewing and reproducibility.

## Research Overview

The primary objective of this research is to find an efficient way to select a representative subset of data points to train a GP model, thereby mitigating its cubic computational complexity ($O(n^3)$). The proposed CORE method works by first filtering data points based on their residuals from a preliminary linear model and then applying a density-based clustering algorithm to select a concise, informative subset.

The study evaluates the performance of CORE and other methods, including **K-Means**, **Random Sampling**, **DBSCAN**, **OIPS**, and **Farthest Point Sampling (FPS)**, on the challenging **Egyptian Used Car Pricing dataset**. The results show that while the dataset itself is difficult for these models, the density-based approaches (CORE and DBSCAN) consistently achieve better predictive accuracy than fixed-budget methods, demonstrating their effectiveness at capturing the intrinsic structure of the data.

## How to View and Run the Project

To replicate the results and explore the analysis yourself, follow these steps:

1. **Clone the repository**:

```

git clone [https://github.com/MohamedEbrahem1/SDSS-2025](https://github.com/MohamedEbrahem1/SDSS-2025)
cd SDSS-2025

```

2. **Create and activate a virtual environment**:

```

python -m venv venv
source venv/bin/activate \# On Windows, use `venv\Scripts\activate`

```

3. **Install the required libraries**:

```

pip install -r requirements.txt

```
4. **Run the Jupyter Notebook**:

```

jupyter notebook research\_evaluation.ipynb

```

Open the notebook in your browser and run the cells in order to see the full analysis, including the data preprocessing, model training, and performance plots.