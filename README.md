# 575-Final-project Workflow 

## Table of Contents

- [Installation](#installation)
- [Data](#data)
- [Code](#code)
- [Image](#image)

## Installation

1. Clone this repository using the following command:
    ```bash
    git clone https://github.com/renawuq/575-Final-project-Group7.git
    ```

2. This project relies on data that cannot be shared publicly due to confidentiality agreements. However, you are welcome to use your own dataset. To do so:
    - Download or prepare your own **MEX data** (or any relevant dataset) that you would like to analyze.
    - Change the file paths in the code to point to your own dataset files.

3. Before running the code, make sure you have all the required libraries installed. You can install the necessary R packages by running the following commands in your R console:

```r
install.packages(c("cowplot", "dplyr", "ggplot2", "readr", "patchwork", "tidyverse", "tidyr", "metap", "multtest"))
install.packages("glmGamPoi")
install.packages("presto")
install.packages("Seurat")
install.packages("sctransform")


4. Adjust the code if needed

## Data

Due to privacy and confidentiality agreements, the dataset used in this project cannot be shared publicly. However, you can substitute the data with your own dataset.

## Code
This part contains all the code we used for the project, including data preprocessing and data analysis:

You could run the code in the following order: 

- `data_preprocessing_clustering.Rmd`: The first script you should run for data preprocessing and clustering.
- `DGE_cbb575.Rmd`: The script for DGE analysis and identifying markers.
- `filtering20termsizes.ipynb`: Helper code for the Enrichment analysis.
- `cytokinehelper2graph.ipynb`: Another helper code for the Enrichment analysis.
- `cluster0-20termsize.cys`: Enrichment analysis performed with gProfiler and visualized with Cytoscape.

## Image
This folder contain some of the image generated from our code


