# US-County-Level Economic Analysis: EDA and Predictive Modeling

## 📊 Project Overview

This repository contains two key components of a comprehensive county-level economic analysis project:

1. **Exploratory Data Analysis (EDA)** - `eda.ipynb` with `eda_final.csv`
2. **Predictive Modeling** - `Model1.ipynb` with `model1.csv`

The project analyzes economic indicators across US counties to understand relationships between GDP per capita, demographic factors, and economic outcomes.

## 📁 Files Included

### 📈 Exploratory Data Analysis
- **`eda.ipynb`** - Comprehensive exploratory data analysis notebook
- **`eda_final.csv`** - Processed dataset for EDA (4.6MB)

### 🤖 Predictive Modeling  
- **`Model1.ipynb`** - Machine learning models for GDP per capita prediction
- **`model1.csv`** - Model-ready dataset with log-transformed GDP per capita (4.0MB)

## 🔍 Dataset Overview

### eda_final.csv Features
- **Geographic**: County, State, Postal Code, GeoFIPS
- **Demographic**: Population estimates, birth/death rates, migration data
- **Economic**: GDP, GDP per capita, median household income, unemployment rate
- **Business**: Establishments, payroll data, establishments per capita
- **Social**: Poverty estimates and percentages
- **Temporal**: Year (2017-2022)

### model1.csv Features
- All features from `eda_final.csv` plus:
- **`Log_GDP_per_capita`** - Log-transformed GDP per capita (target variable)
- Preprocessed and cleaned for machine learning

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Running the Analysis

1. **Exploratory Data Analysis**:
   ```bash
   jupyter notebook eda.ipynb
   ```

2. **Predictive Modeling**:
   ```bash
   jupyter notebook Model1.ipynb
   ```

## 📊 EDA Key Features

### Data Exploration
- **Data Loading & Inspection**: Initial data exploration and structure analysis
- **Distribution Analysis**: Histograms and statistical summaries of key variables
- **Correlation Analysis**: 
  - Correlation matrix heatmaps
  - Scatter plots with regression lines
  - Focus on GDP per capita vs. median household income relationships

### Visualizations
- Distribution plots for all numerical variables
- Correlation heatmaps using seaborn
- Scatter plots with regression analysis
- Statistical summaries and descriptive statistics

## 🤖 Model1 Key Features

### Machine Learning Pipeline
- **Data Preprocessing**: StandardScaler for feature normalization
- **Train/Validation/Test Split**: 
  - Training: 2017-2020
  - Validation: 2021
  - Test: 2022

### Models Implemented
1. **Linear Regression**
   - Baseline model for GDP per capita prediction
   - Performance metrics: RMSE, R², MAE

2. **Partial Least Squares (PLS)**
   - Handles multicollinearity
   - 10 components used
   - Better performance than linear regression

3. **Gradient Boosting Regressor**
   - Default and hyperparameter-tuned versions
   - Feature importance analysis
   - Best performing model

4. **Support Vector Machines (SVM)**
   - RBF kernel implementation
   - Scaled features for optimal performance

5. **Random Forest**
   - Ensemble method for robust predictions
   - Feature importance ranking

### Model Evaluation
- **Metrics**: RMSE, R², MAE for validation and test sets
- **Visualizations**: 
  - Actual vs. Predicted scatter plots
  - Residual analysis with color-coded error magnitude
  - Feature importance plots
- **Hyperparameter Tuning**: RandomizedSearchCV for Gradient Boosting

## 📈 Key Findings

### EDA Insights
- Strong positive correlation between GDP per capita and median household income
- Significant variation in economic indicators across counties
- Clear relationships between demographic factors and economic outcomes

### Model Performance
- **Gradient Boosting** achieved the best performance
- **Validation R²**: ~0.73 (73% variance explained)
- **Test R²**: ~0.67 (67% variance explained)
- Key predictive features identified through importance analysis

## 🛠️ Technical Details

### Data Processing
- Log transformation of GDP per capita for better model performance
- Standard scaling of features for algorithms requiring normalization
- Temporal train/validation/test split for realistic evaluation

### Model Selection
- Multiple algorithms tested for robustness
- Hyperparameter optimization for best model
- Comprehensive evaluation on both validation and test sets

## 📋 Requirements

```
pandas>=1.5.0
numpy>=1.24.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.3.0
jupyter>=1.0.0
```

## 📝 Usage Notes

1. **Data Paths**: Update file paths in notebooks to match your local directory structure
2. **Memory Requirements**: Large datasets may require sufficient RAM (8GB+ recommended)
3. **Execution Time**: Model training, especially hyperparameter tuning, may take several minutes

## 🔗 Data Sources

- **US Census Bureau**: Population and poverty data
- **Bureau of Economic Analysis**: GDP and income data  
- **Bureau of Labor Statistics**: Employment data
- **County Business Patterns**: Business establishment data

## 📄 License

This project is for educational and research purposes. Please ensure compliance with data source terms of use.

---

**Note**: This analysis was conducted as part of a Data Science Capstone project focusing on county-level economic indicators and predictive modeling."
