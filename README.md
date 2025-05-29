# Police Killings Analysis 2015

A comprehensive machine learning analysis of police killings in the United States using demographic, socioeconomic, and geographic data to predict armed status and identify disparities.

## Project Overview

This project analyzes **438 police killing incidents** from 2015 using advanced data science techniques to explore patterns in demographics, socioeconomic factors, and geographic distribution. We built and evaluated multiple machine learning models to predict whether victims were armed based on various features.

## Key Findings

- **Model Performance**: Achieved up to **77% accuracy** using Logistic Regression in predicting armed status
- **Racial Disparities**: Identified significant differences in armed vs. unarmed incidents across racial groups
- **Socioeconomic Impact**: Lower income and higher poverty levels correlate with increased likelihood of armed incidents
- **Geographic Patterns**: Urban areas show higher concentration of incidents, with distinct regional clustering

## Methodology

### Machine Learning Models
- **Logistic Regression**: 77.17% accuracy, 68.05% F1-score
- **Random Forest**: 72.83% accuracy, 66.04% F1-score  
- **Support Vector Machine**: 77.17% accuracy, 67.22% F1-score

### Feature Engineering
- Processed **10 key features** including age, gender, race/ethnicity, income, poverty rate, unemployment rate, and education levels
- Created binary target variable `is_armed` (armed vs. unarmed)
- Applied StandardScaler normalization and label encoding for categorical variables

### Evaluation Techniques
- **5-fold Stratified Cross-Validation** for robust performance assessment
- **Confusion Matrix Analysis** for detailed classification evaluation
- **Feature Importance Analysis** using Random Forest and linear model coefficients

## Visualizations

The analysis includes **10+ interactive visualizations**:
- Geographic heatmaps using **Folium** showing incident distribution
- Correlation matrices revealing feature relationships
- Feature importance plots from Random Forest models
- Demographic distribution charts by armed status
- Socioeconomic scatter plots (poverty vs. income)
- Confusion matrices for all three models

## Technologies Used

- **Python** - Primary programming language
- **Scikit-learn** - Machine learning models and evaluation
- **Pandas & NumPy** - Data manipulation and analysis
- **Matplotlib & Seaborn** - Statistical visualizations
- **Folium** - Interactive geographic mapping
- **Jupyter Notebook** - Development environment

## Repository Structure

```
police-killings-analysis/
├── PoliceKillings.ipynb          # Main analysis notebook
├── README.md                     # Project documentation
└── data/
    └── police_killing.csv        # Dataset (loaded from GitHub)
```

## Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn folium jupyter
```

### Running the Analysis
1. Clone this repository
2. Open `PoliceKillings.ipynb` in Jupyter Notebook
3. Run all cells to reproduce the analysis


## Dataset Details

- **Source**: [FiveThirtyEight Police Killings Dataset](https://github.com/fivethirtyeight/data/blob/master/police-killings/police_killings.csv)
- **Size**: 438 incidents (after cleaning)
- **Features**: 23 original columns including demographic, geographic, and socioeconomic data
- **Target Variable**: Binary armed status (armed/unarmed)
### Key Research Questions Addressed

1. **Predictive Modeling**: Can we predict armed status from demographic and socioeconomic features?
2. **Racial Analysis**: Are there significant racial differences in armed vs. unarmed incidents?
3. **Geographic Patterns**: How do regional and urban/rural factors correlate with armed status?
4. **Socioeconomic Impact**: Do income and poverty levels influence likelihood of armed incidents?
5. **Education Correlation**: Is there a relationship between community education levels and incident types?

## Key Results

### Most Important Features (Random Forest)
1. **Race/Ethnicity** - Strongest predictor of armed status
2. **Poverty Rate** - Higher poverty correlates with armed incidents  
3. **Personal Income** - Lower income associated with armed status

### Demographic Insights
- **Urban Concentration**: Most incidents occur in metropolitan areas
- **Income Threshold**: Incidents below $20,000 personal income show higher armed rates
- **Educational Impact**: Communities with higher college education rates have fewer armed incidents

## Ethical Considerations

This research aims to contribute to evidence-based policy discussions about police practices and community safety. All analysis is conducted with respect for the victims and their families, focusing on systemic patterns rather than individual cases.

*This project demonstrates the application of machine learning techniques to important social issues, providing data-driven insights for policy makers and researchers working on police reform and community safety.*
