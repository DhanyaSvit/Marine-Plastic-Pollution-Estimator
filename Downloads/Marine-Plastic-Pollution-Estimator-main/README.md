# Marine Plastic Pollution Estimator

## SDG Goal
SDG 14 – Life Below Water

## Project Objective
Estimate the metric tons of plastic waste entering the ocean based on:
- Coastal population density
- Mismanaged Waste Index

## Datasets Used
1. Jambeck et al. (2015) – Country level (2010)
2. Regional Plastic Leakage Dataset (2000–2019)-used for model training

## Data Preprocessing

Jambeck dataset 
- Dataset cleaned and standardized  
- Mismanaged Waste Index created  
- Skewness analysis performed  
- Log transformation tested (exploratory)  
- Cleaned dataset saved in `Data/processed/`

Regional Dataset
- Removed aggregated "World" row
- Cleaned and standardized column names
- Created normalized *Mismanaged Waste Index*
- Retained coastal population density as per project requirement

## Machine Learning Model

A Random Forest Regression model was trained to estimate plastic leakage.

## Model Used

Random Forest Regressor

## Model Training Notebook

Model_training_Random_forest.ipynb

## Documentation

The complete project documentation is available in:

cohort12 (marine-plastic-pollution-estimator).docx

## Project Structure

Marine-Plastic-Pollution-Estimator
│
├── Data
│   ├── processed
│   │   ├── datafinal.csv
│   │   ├── jambeck_cleaned.csv
│   │
│   └── raw
│       ├── jambeck_2010.csv
│       ├── mismanaged-plastic-waste.csv
│       ├── plastic-leakage-to-aquatic-environments.csv
│       ├── regional_plastic_leakage_2000_2019.xlsx
│       ├── share-of-plastic-waste-that-is-mismanaged.csv
│
├── notebooks
│   ├── 01_jambeck_preprocessing.ipynb
│   ├── 02_regional_preprocessing.ipynb
│
├── RandomSWRwithGridSearchCVmodel.ipynb
├── Plastic Waste - Jambeck et al. (2015).csv
├── datafinal.xlsx
├── cohort12(marine-plastic-pollution-estimator).docx
│
├── .gitignore
└── README.md

## Notes
- Cleaned datasets do not include transformation.
- Log transformations were tested but will depend on model selection.
- Log transformations calculated for jambeck dataset currently
- The regional dataset contains time-series data (2000–2019), which may allow panel or cross-sectional modeling depending on the chosen methodology


