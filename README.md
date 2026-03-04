# Marine Plastic Pollution Estimator

## SDG Goal
SDG 14 – Life Below Water

## Project Objective
Estimate the metric tons of plastic waste entering the ocean based on:
- Coastal population density
- Mismanaged Waste Index

## Datasets Used
1. Jambeck et al. (2015) – Country level (2010)
2. Regional Plastic Leakage Dataset (2000–2019)

## Current Progress

Jambeck dataset cleaned  
Mismanaged Waste Index created  
Skewness analysis performed  
Log transformation tested (exploratory)  
Cleaned dataset saved in `data/processed/`

Regional Dataset
- Removed aggregated "World" row
- Cleaned and standardized column names
- Created normalized *Mismanaged Waste Index*
- Retained coastal population density as per project requirement


## Notes
- Cleaned datasets do not include transformation.
- Log transformations were tested but will depend on model selection.
- Log transformations calculated for jambeck dataset currently
- The regional dataset contains time-series data (2000–2019), which may allow panel or cross-sectional modeling depending on the chosen methodology


## Project Structure
 

└── 📁Marine Plastic Pollution Estimator
    └── 📁Data
        └── 📁processed
            ├── datafinal.csv
            ├── jambeck_cleaned.csv
        └── 📁raw
            ├── jambeck_2010.csv
            ├── mismanaged-plastic-waste.csv
            ├── plastic-leakage-to-aquatic-environments.csv
            ├── regional_plastic_leakage_2000_2019.xlsx
            ├── share-of-plastic-waste-that-is-mismanaged.csv
    └── 📁notebooks
        ├── 01_jambeck_preprocessing.ipynb
        ├── 02_regional_preprocessing.ipynb
    ├── .gitignore
    └── README.md
