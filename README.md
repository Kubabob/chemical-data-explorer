![Python](https://img.shields.io/badge/Python-3.10-blue)
![RDKit](https://img.shields.io/badge/RDKit-2023.09.5-green)
![SciPy](https://img.shields.io/badge/SciPy-1.12.0-orange)
![Pandas](https://img.shields.io/badge/Pandas-2.1.3-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8.2-red)

This repository contains implementations of advanced data exploration techniques applied to a dataset of chemical compounds and their molecular descriptors. The project demonstrates the application of multivariate statistical methods to analyze and visualize complex chemical data.

## Project Overview

This project applies two key data exploration techniques to analyze relationships between various chemical compounds:

1. **Hierarchical Cluster Analysis (HCA)** - Used to identify natural groupings of chemical compounds based on their molecular descriptors
2. **Principal Component Analysis (PCA)** - Applied to reduce dimensionality and identify the most important variables that explain variation in the dataset

## Dataset

The dataset consists of chemical compounds (pesticides/insecticides) including:
- Organophosphate compounds
- Neonicotinoids
- DDT and its analogs
- Pyridine carboxylic acids

For each compound, SMILES (Simplified Molecular Input Line Entry System) codes were used to generate molecular descriptors using the RDKit library. These descriptors provide a numerical representation of chemical properties and structural features.

## Analysis Process

### Data Preparation
- Conversion of SMILES codes to molecular structures using RDKit
- Generation of chemical descriptors (~147 features per compound)
- Data standardization/autoscaling to handle different measurement scales

### Hierarchical Cluster Analysis
- Calculation of distance matrices using Euclidean and Manhattan metrics
- Application of different linkage methods (single, complete)
- Generation of dendrograms to visualize hierarchical relationships
- Cluster identification and interpretation

### Principal Component Analysis
- Correlation matrix analysis
- Eigenvalue decomposition
- Scree plot analysis for dimension determination
- Component interpretation

## Key Findings

- Successfully identified chemical groups based on structural similarity
- Discovered meaningful patterns in complex high-dimensional chemical data
- Reduced the dimensionality while preserving essential information
- Visualized relationships between compounds in a more interpretable form

## Folder Structure

```
├── HCA/               # Hierarchical Cluster Analysis
│   ├── hca.ipynb     # Main analysis notebook
│   ├── smiles.ipynb  # SMILES processing
│   └── sprawozdanie/ # Report and documentation
│
├── PCA/               # Principal Component Analysis
│   ├── pca.ipynb     # Analysis notebook
│   └── sprawko/      # Report and documentation
│
├── figures/           # Generated visualizations
└── sprawozdanie/      # Overall project documentation
```

## Technologies Used

- **Python** - Primary programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **SciPy** - Scientific computing, hierarchical clustering
- **Matplotlib** - Data visualization
- **RDKit** - Cheminformatics and molecular processing
- **Jupyter Notebooks** - Interactive development and analysis

## Visualizations

The project includes various visualizations:
- Dendrograms showing hierarchical relationships between compounds
- Distance matrices represented as heatmaps
- Principal component plots
- Molecular structure visualizations

## How to Run

1. Clone this repository
2. Install required dependencies: `uv sync`
3. Run Jupyter notebooks: `jupyter notebook`

## License

This project is available under the MIT License.

## Acknowledgments

This project was completed as part of a data exploration techniques course at university.