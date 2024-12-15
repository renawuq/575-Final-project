# 575-Final-project Workflow

## Table of Contents

- [Installation](#installation)
- [Data](#data)
- [Code](#code)
- [File Descriptions](#file-descriptions)

## Installation

1. **Clone this repository** using the following command:
    ```bash
    git clone https://github.com/renawuq/575-Final-project-Group7.git
    ```

2. **Prepare Your Own Data**  
    This project relies on data that cannot be shared publicly due to confidentiality agreements. However, you are welcome to use your own dataset. To use your own data:
    - Download or prepare your own **MEX data** (or any relevant dataset) that you would like to analyze.
    - Update the file paths in the code to point to your dataset files.

3. **Install Required Dependencies**  
    Before running the code, make sure you have all the necessary libraries installed.

    - **R Libraries**:  
      You can install the necessary R packages by running the following commands in your R console:

      ```r
      install.packages(c("cowplot", "dplyr", "ggplot2", "readr", "patchwork", "tidyverse", "tidyr", "metap", "multtest"))
      install.packages("glmGamPoi")
      install.packages("presto")
      install.packages("Seurat")
      install.packages("sctransform")
      ```

    - **Python Libraries**:  
      You will also need Python libraries such as `pandas`, `numpy`, `matplotlib`, and `seaborn`. You can install them using:

      ```bash
      pip install pandas numpy matplotlib seaborn
      ```

    - **Cytoscape Software**:  
      You will need **Cytoscape** for visualizing the `*.cys` files. Download it from [Cytoscape's official website](https://cytoscape.org/).

4. **Adjust the Code**  
    - Ensure that the file paths in the scripts point to your dataset.
    - Modify the gene lists or other parameters based on your research focus.

## Data

Due to privacy and confidentiality agreements, the dataset used in this project cannot be shared publicly. However, you can substitute the data with your own dataset by updating the file paths in the provided scripts.

## Code

This section contains all the code used for the project, including data preprocessing and analysis. You should run the scripts in the following order:

1. **`data_preprocessing_clustering.Rmd`**  
   This is the first script you should run. It handles data preprocessing, including loading, cleaning, scaling, and performing PCA. It also includes the clustering process using the Seurat library to identify cell subpopulations.

2. **`Annotations.Rmd`**  
   After running `data_preprocessing_clustering.Rmd`, run this script to annotate the clusters based on marker gene expression. It identifies markers for each cluster, visualizes key transcription factors defining T cell subpopulations, and generates dot plots for a detailed analysis of gene expression.

3. **`DGE_cbb575.Rmd`**  
   This script is used for Differential Gene Expression (DGE) analysis and for identifying marker genes. It leverages Seurat's `FindMarkers()` function to identify genes differentially expressed between clusters. The results are filtered based on log fold change and statistical significance.

4. **`filtering20termsizes.ipynb`**  
   This Jupyter notebook is a helper for filtering enrichment terms during the Enrichment Analysis. It processes and filters the output to ensure that relevant terms are selected for further analysis.

5. **`cytokinehelper2graph.ipynb`**  
   Another Jupyter notebook that helps prepare data for the Enrichment Analysis. It processes cytokine-related gene sets and prepares them for visualization in Cytoscape.

6. **`cluster0-20termsize.cys`**  
   This Cytoscape file contains the visualized results of the Enrichment analysis for **cluster 0**. The analysis is performed using **gProfiler** and visualized in **Cytoscape** for better understanding of gene set enrichment.

7. **`cluster1-20termsize.cys`**  
   Similar to the previous file, this Cytoscape file visualizes the Enrichment analysis results, but for **cluster 1**. It also uses **gProfiler** and visualizes the results in **Cytoscape** for further insight into the gene set enrichments.

## File Descriptions

- **`data_preprocessing_clustering.Rmd`**:  
  Script for the initial data preprocessing steps, including loading the data, performing scaling, and clustering the dataset using Seurat. It also includes PCA for identifying cell subpopulations.

- **`Annotations.Rmd`**:  
  This script annotates the clusters identified in the previous step using marker genes. It visualizes important transcription factors that define T cell subsets and includes dot plots to assess expression across clusters.

- **`DGE_cbb575.Rmd`**:  
  A script for performing Differential Gene Expression (DGE) analysis using Seurat's `FindMarkers()` function. It identifies significantly differentially expressed genes between the clusters based on statistical thresholds such as p-value and log fold change.

- **`filtering20termsizes.ipynb`**:  
  A helper Jupyter notebook used to filter the results of the Enrichment analysis by removing irrelevant or non-significant terms. It prepares the data for further analysis.

- **`cytokinehelper2graph.ipynb`**:  
  Another Jupyter notebook used to process cytokine-related gene sets and prepare them for visualization in Cytoscape, contributing to the Enrichment analysis.

- **`cluster0-20termsize.cys`**:  
  Cytoscape visualization of Enrichment analysis results for **cluster 0**, based on analysis performed with gProfiler.

- **`cluster1-20termsize.cys`**:  
  Similar to `cluster0-20termsize.cys`, this file contains the visualization of Enrichment analysis results for **cluster 1**, also produced using gProfiler and visualized in Cytoscape.

