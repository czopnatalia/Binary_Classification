# Occupancy Detection System – Smart Building Analysis

## Project Overview
The goal of this project is to build a robust binary classification model to predict room occupancy based on environmental factors like temperature, humidity, light, and CO2 levels. 

This solution is designed for **Smart Building** applications to optimize energy consumption (e.g., HVAC and lighting control) and improve space management.

The project follows the **CRISP-DM** methodology, covering everything from data preprocessing and exploratory analysis to model evaluation and final predictions.

## Key Features
* **Advanced Preprocessing**: Merging multiple datasets and handling time-series data.
* **Feature Engineering**: Creating cyclical time features to capture patterns in human activity.
* **Exploratory Data Analysis (EDA)**: Identifying key predictors through correlation matrices and boxplot visualizations, highlighting Light and CO2 as crucial variables.
* **Machine Learning Models**: Implementation and comparison of **C&RT Decision Trees** and **Random Forest**.
* **High Performance**: The final Random Forest model achieved a remarkable **99.4% accuracy** (OOB error: 0.61%).


## Tech Stack
* **Language**: R 
* **Libraries**: `tidyverse` (dplyr, ggplot2), `caret`, `randomForest`, `rpart`, `corrplot`.

## Evaluation Results (Validation Set)
The models were evaluated using multiple metrics to account for class imbalance (approx. 23% occupancy):

| Metric | Decision Tree (C&RT) | Random Forest |
| :--- | :--- | :--- |
| **Accuracy** | 99.09%  | 99.40%  |
| **Sensitivity** | 99.44%  | 98.67%  |
| **Specificity** | 98.99%  | 99.62%  |
| **Kappa** | 0.9747  | 0.9831  |
| **AUC-ROC** | 0.9921  | 0.9992  |

## Project Structure
* `occupancy_data/` - Training and test datasets (txt files).
* `CS_projekt.Rmd` - Main R script containing the full pipeline.
* `CS_projekt.pdf` - Detailed diagnostic and descriptive report.

---

## How to Run This Project

To run this project locally, follow these steps:

### 1. Prerequisites
Ensure you have the following installed:
* **R** (version 4.0 or newer)
* **RStudio** (recommended)

### 2. Install Required Libraries
Open RStudio and install the necessary packages using the following command:
```r
install.packages(c("tidyverse", "caret", "randomForest", "rpart", "rpart.plot", "corrplot", "pROC"))
