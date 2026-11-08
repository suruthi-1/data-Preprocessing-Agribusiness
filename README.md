# Data Cleaning and Preprocessing Strategy for Agribusiness Datasets
  
**Language:** R  
**Environment:** RStudio

## 1. Project Overview

Agribusiness datasets often contain missing values, duplicate records, inconsistent formats, incorrect measurements, and outliers.

This project presents a structured strategy for cleaning and preprocessing a hypothetical agribusiness dataset named `farm_survey`.

The project demonstrates how R and RStudio can be used to improve data quality, prepare reliable datasets for analysis, and support reproducible data workflows.

## 2. Objectives

- Identify common data-quality issues in agribusiness datasets.
- Develop a structured ten-step data-cleaning workflow.
- Standardise column names, categories, dates, and measurement units.
- Detect and handle duplicate records and missing values.
- Identify impossible values and potential outliers.
- Check logical consistency across related variables.
- Apply preprocessing techniques for machine learning.
- Maintain reproducibility through documentation, testing, and version control.

## 3. Dataset Description

The project uses a hypothetical dataset called `farm_survey`, containing one record per farm per growing season.

The dataset includes:

| Variable | Description |
|---|---|
| Farm ID | Unique farm identifier |
| Region | State or district |
| Crop | Crop cultivated |
| Planting Date | Date of planting |
| Harvest Date | Date of harvesting |
| Area Value | Cultivated land area |
| Area Unit | Area measurement unit |
| Yield (t/ha) | Harvested yield per hectare |
| Fertilizer kg/ha | Fertilizer applied per hectare |
| Rainfall (mm) | Seasonal rainfall |
| Soil pH | Soil acidity or alkalinity |
| Price Raw | Farm-gate price per kg |
| Irrigation Type | Drip, Canal, or Rainfed |

**Note:** The dataset is hypothetical and uses simulated records for demonstration. No real farm survey data is included.

## 4. Data Cleaning Workflow

The project follows ten major cleaning steps:

1. Ingest and profile the raw data.
2. Standardise data structure, column names, and data types.
3. Remove duplicate records.
4. Standardise categorical labels.
5. Harmonise measurement units and formats.
6. Handle sentinel codes and impossible values.
7. Check logical consistency.
8. Detect and assess outliers.
9. Diagnose missing values.
10. Validate and export the cleaned dataset.

## 5. Data Preprocessing Framework

The preprocessing stage prepares cleaned data for statistical analysis and machine learning.

It includes:

- Training and testing data splitting.
- Missing-value imputation.
- Feature engineering.
- Data transformation.
- Feature scaling and normalisation.
- Categorical encoding.
- Feature selection.
- Saving the preprocessing recipe.

Preprocessing parameters are learned from training data and then applied to testing data to prevent data leakage.

## 6. Tools and Technologies

- **R** – Programming language for data analysis.
- **RStudio** – Development environment.
- **Tidyverse** – Data manipulation and visualisation.
- **Lubridate** – Date handling.
- **Janitor** – Data cleaning.
- **Naniar** – Missing-data analysis.
- **Tidymodels** – Data preprocessing and modelling.
- **Testthat** – Automated testing.
- **Targets** – Workflow automation.
- **Renv** – Package environment management.
- **Git and GitHub** – Version control and project management.

## 7. Repository Structure

```text
agribusiness-data-cleaning-preprocessing/
│
├── README.md
├── .gitignore
├── agribusiness-cleaning.Rproj
│
├── data/
│   ├── raw/
│   └── processed/
│
├── R/
│   ├── cleaning_functions.R
│   └── lookups.R
│
├── tests/
│   └── testthat/
│       └── test-cleaning.R
│
├── reports/
│   └── data_clean.Rmd
│
└── docs/
    ├── strategy_for_agribusiness_datasets.docx
    └── decision_log.md
```

## 8. How to Run the Project

1. Install R and RStudio.
2. Clone or download this repository.
3. Open `agribusiness-cleaning.Rproj` in RStudio.
4. Install the required packages:

```r
install.packages(c(
  "tidyverse",
  "lubridate",
  "janitor",
  "naniar",
  "tidymodels",
  "testthat",
  "targets",
  "renv"
))
```

5. Open `reports/data_clean.Rmd` in RStudio.
6. Review and execute the R code chunks.
7. Use the Knit option to generate the report in a supported output format.

## 9. Reproducibility

The project follows reproducible data-analysis practices:

- Preserve the original raw data.
- Document cleaning decisions.
- Use a fixed random seed (`set.seed(2026)`).
- Create reusable and testable R functions.
- Track package versions using `renv`.
- Automate workflows using `targets`.
- Record session information.
- Validate the cleaned data before exporting.

## 10. Expected Outcomes

- Improved data consistency and quality.
- Reliable and structured agribusiness datasets.
- Better handling of missing values and outliers.
- Reproducible cleaning and preprocessing workflows.
- Model-ready data for further analysis.

## 11. Quality Assurance


- Automated unit testing using testthat.
- Data validation and consistency checks.
- Outlier investigation using IQR.
- Raw data integrity checks using MD5 checksums.
- Reproducible execution using fixed random seeds.
- Workflow automation using targets.

## 12. Conclusion

This project demonstrates how a systematic data-cleaning and preprocessing strategy can improve the reliability and usability of agribusiness datasets.

By combining R programming, automated validation, and reproducible workflows, the project provides a foundation for trustworthy agricultural data analysis and future predictive modelling.

## 13. Limitations

This repository presents a strategy and starter implementation based on a hypothetical dataset. A separate real-world raw dataset and a complete executable end-to-end pipeline are not included.

## 14. Project Documentation

- **Word Document:** `docs/strategy_for_agribusiness_datasets.docx`
- **R Markdown Report:** `reports/data_clean.Rmd`
- **Cleaning Functions:** `R/cleaning_functions.R`
- **Lookup Tables:** `R/lookups.R`
- **Decision Log:** `docs/decision_log.md`

---

## 15.Grab

![data viewer.png]_(data viewer.png)_
Fig: RStudio Data Viewer showing test_prep, the preprocessed test set (92 rows, 16 columns). The numeric predictors are scaled and have no missing values (0% NA).
rstudio console.png
Fig: RStudio Environment and Files panels showing the objects created by the pipeline (train: 363 observations, test: 92 observations, rec_prep, test_prep) and the project files
rstudio environment.png
Fig: RStudio Console after running the cleaning and preprocessing pipeline, with View() used to inspect farm_raw, test, rec_prep and test_prep.

**Project:** Data Cleaning and Preprocessing Strategy for Agribusiness Datasets  
