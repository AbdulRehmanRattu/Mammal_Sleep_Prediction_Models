
# Mammal Sleep Prediction Models

This project aims to predict total sleep and dreaming duration in mammals using regression models. We explored both linear regression and XGBoost techniques to create robust predictive models. The project involves data analysis, feature engineering, model training, and evaluation.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Analysis and Exploration](#data-analysis-and-exploration)
3. [Addressing Data Issues and Feature Engineering](#addressing-data-issues-and-feature-engineering)
4. [Feature Selection and Preprocessing](#feature-selection-and-preprocessing)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Visualizing Predictions](#visualizing-predictions)
7. [Conclusion and Future Directions](#conclusion-and-future-directions)
8. [Installation](#installation)
9. [Usage](#usage)
10. [Contact](#contact)

## Introduction
The goal of this project is to develop regression models to predict two distinct variables: "TotalSleep" and "Dreaming" duration in mammals, using the sleep dataset. The project ensures reproducibility and adheres to the outlined requirements.

## Data Analysis and Exploration
1. **Data Processing:**
   - Loaded the data using pandas (`pd.read_excel`).

2. **Data Cleaning:**
   - Obtained basic information, data types, and identified missing values using `df.info()`.

3. **Exploratory Analysis:**
   - **Histograms:** Used `plt.hist` to visualize numerical attribute distributions.
   - **Boxplots:** Used `sns.boxplot` to identify outliers.
   - **Correlation Heatmap:** Used `sns.heatmap` to assess relationships between numerical attributes.

## Addressing Data Issues and Feature Engineering
1. **Missing Values:**
   - Applied median imputation for the "NonDreaming" column using `SimpleImputer`.

2. **New Feature Creation:**
   - Created "BrainBodyRatio" by calculating the ratio between "BrainWt" and "BodyWt".

3. **Outlier Management:**
   - Applied winsorization to reduce the impact of outliers using `scipy.stats.mstats.winsorize`.

## Feature Selection and Preprocessing
1. **Feature and Target Separation:**
   - Divided dataset into features and target variables.

2. **Pipelines for Transformations:**
   - **Numerical Features:**
     - Created a pipeline with median imputation and standardization.
   - **Categorical Features:**
     - Created a pipeline with imputation and one-hot encoding.

## Model Training and Evaluation
1. **Data Split:**
   - Split dataset into training (80%) and testing (20%) sets using `train_test_split`.

2. **Initial Linear Regression Models:**
   - Implemented linear regression for "TotalSleep" and "Dreaming".
   - Performance:
     - **TotalSleep Model MSE:** 0.6685
     - **Dreaming Model MSE:** 0.2537

3. **Exploring XGBoost:**
   - Implemented XGBoost (`XGBRegressor`) for both predictions.
   - Performance:
     - **XGBoost TotalSleep Model MSE:** 0.1338
     - **XGBoost Dreaming Model MSE:** 0.4003

## Visualizing Predictions
- Created line plots for actual vs. predicted values to compare model performance.

## Conclusion and Future Directions
The project successfully established regression models for predicting "TotalSleep" and "Dreaming" duration. Future improvements could include hyperparameter tuning and feature selection to enhance model performance.

## Installation
To install the required packages, run the following command:
```bash
pip install -r requirements.txt
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/AbdulRehmanRattu/TicTacToe_AI.git
   ```
2. Navigate to the project directory:
   ```bash
   cd TicTacToe_AI
   ```
3. Ensure you have the required dataset `sleep_dataset.xlsx` in the project directory.

4. Run the script:
   ```bash
   python script_name.py
   ```

## Contact
For any inquiries or issues, please contact me at:

- **Email:** rattu786.ar@gmail.com
- **LinkedIn:** [Abdul Rehman Rattu](https://www.linkedin.com/in/abdul-rehman-rattu-395bba237)

---

Thank you for exploring this project!
