# Bengaluru House Price Prediction

This project aims to predict house prices in Bengaluru, India, using machine learning techniques. The workflow follows a standard data science pipeline, including data loading, cleaning, feature engineering, dimensionality reduction, outlier handling, and visualization to prepare data for model training.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Project Steps](#project-steps)
  - [1. Data Loading and Initial Exploration](#1-data-loading-and-initial-exploration)
  - [2. Data Cleaning](#2-data-cleaning)
  - [3. Feature Engineering](#3-feature-engineering)
  - [4. Dimensionality Reduction](#4-dimensionality-reduction)
  - [5. Outlier Detection and Removal](#5-outlier-detection-and-removal)
  - [6. Data Visualization](#6-data-visualization)
- [Getting Started](#getting-started)
- [Future Work](#future-work)
- [License](#license)

---

## Project Overview

The goal is to build a robust model that predicts house prices based on property features. The process includes cleaning and preparing the data, engineering meaningful features, handling outliers, and visualizing patterns before applying machine learning algorithms.

---

## Dataset

**File:** `Bengaluru House Data.csv`

**Features include:**
- `area_type`: Type of area (e.g., Super built-up Area, Built-up Area)
- `availability`: Availability status
- `location`: Property location
- `size`: Number of BHKs or Bedrooms
- `society`: Society name
- `total_sqft`: Total square footage
- `bath`: Number of bathrooms
- `balcony`: Number of balconies
- `price`: Price (in Lakhs)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib

---

## Project Steps

### 1. Data Loading and Initial Exploration

- Load the dataset into a pandas DataFrame.
- Perform exploratory checks to understand structure, dimensions, and data types.

### 2. Data Cleaning

- Handle missing values by dropping rows with nulls (due to large dataset size).
- Clean the `size` column by extracting the numerical BHK count.
- Standardize `total_sqft` by converting ranges to averages and identifying non-standard entries.

### 3. Feature Engineering

- Create the `price_per_sqft` feature (price/total_sqft) to aid in outlier detection and analysis.

### 4. Dimensionality Reduction

- Reduce high cardinality in the `location` column by grouping infrequent locations into an "other" category.

### 5. Outlier Detection and Removal

- Remove outliers using:
  - Domain knowledge (e.g., minimum square feet per BHK)
  - Statistical methods (e.g., removing values outside standard deviation of `price_per_sqft` per location)

### 6. Data Visualization

- Visualize relationships (e.g., between total_sqft, price, BHK) using scatter plots and other charts to identify patterns and potential outliers.

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/JeswinJestin/BangloreHousePricePrediction.git
   cd BangloreHousePricePrediction
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib
   ```

3. **Run the Jupyter notebook:**
   - Open the `.ipynb` file in Jupyter Notebook or JupyterLab and follow the step-by-step data processing and analysis.

---

## Future Work

- Implement machine learning models (Linear Regression, Lasso, Decision Tree, etc.) for price prediction.
- Evaluate model performance using relevant metrics (e.g., RMSE, MAE).
- Perform hyperparameter tuning for optimal model selection.
- Explore advanced feature engineering techniques.

---

## License

---
