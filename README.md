# Marine Plastic Pollution Estimator

## SDG Goal
SDG 14 – Life Below Water

## Project Objective
Estimate the metric tons of plastic waste entering the ocean based on:
- Coastal population
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


## Notes
- Cleaned datasets do not include transformation.
- Log transformations were tested but will depend on model selection.


## Project Structure

current_project_structure : 

└── 📁Marine Plastic Pollution Estimator
    └── 📁Data
        └── 📁processed
            ├── jambeck_cleaned.csv
        └── 📁raw
            ├── jambeck_2010.csv
            ├── regional_plastic_leakage_2000_2019.xlsx
    └── 📁notebooks
        ├── 01_jambeck_preprocessing.ipynb
    ├── .gitignore
    └── README.md
