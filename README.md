# YieldSense AI

# Crop Yield Prediction & Agricultural Productivity Forecasting System

YieldSense AI is a machine learning project focused on predicting crop yield using soil, weather, crop management, regional, and seasonal parameters.

## Project Objective

The objective of this project is to develop a machine learning model to predict crop yield (tons per hectare) using agricultural and environmental features.

Since the target variable (`yield_tpha`) is a continuous numerical value, this problem is treated as a regression problem.

## Data Source

The dataset used for this project was obtained from the Kaggle Crop Yield Prediction Challenge.

### Dataset Details

- Total records: 4800
- Total columns: 18
- Categorical features: `crop_type`, `region`, `season`
- Numerical features: `soil_ph`, `soil_moisture`, `avg_temperature`, `total_rainfall`, `fertilizer_amount`, `pesticide_usage`, `sunlight_hours`, `nitrogen_content`, `phosphorus_content`, `potassium_content`, `irrigation_frequency`
- Date feature: `harvest_date`
- Target variable: `yield_tpha`
- Target unit: tons per hectare

## Milestone 1 – Requirements & Dataset Preparation

### Environment Setup

- Created a project-specific virtual environment.
- Installed required Python libraries: Pandas, NumPy, Matplotlib, Seaborn and Scikit-learn.
- Used Jupyter Notebook in VS Code for implementation.

### Data Exploration

- Loaded and inspected the crop yield dataset.
- Examined the first few records using `df.head()`.
- Examined the dataset structure using `df.info()`.
- Calculated descriptive statistics using `df.describe()`.

### Data Cleaning

- Checked for missing values.
- Checked for duplicate records.
- Converted `harvest_date` into datetime format.
- Derived `harvest_month` from the harvest date.
- Removed identifier fields from the modeling features.

### Data Analysis

Two important visualizations were generated:

1. Distribution of Crop Yield
2. Correlation Heatmap

The analysis helped understand the distribution of the target variable and relationships between numerical features.

### Feature Engineering

Categorical features were converted into numerical form using One-Hot Encoding.

Numerical features were standardized using StandardScaler.

The dataset was divided into training and testing sets using an 80:20 split.

### Preprocessing Results

- Training samples: 3840
- Testing samples: 960
- Encoded categorical features: 13
- Scaled numerical features: 12
- Final processed training features: 25
- Final processed testing features: 25

## Project Structure

```text
YieldSense-AI/
│
├── dataset/
│   ├── crop_yield_train.csv
│   └── processed/
│       ├── X_train.npy
│       ├── X_test.npy
│       ├── y_train.npy
│       └── y_test.npy
│
├── notebooks/
│   └── EDA.ipynb
│
├── .gitignore
└── README.md
