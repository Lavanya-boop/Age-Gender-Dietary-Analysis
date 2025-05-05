# Age-Gender-Dietary-Analysis

## Analysis of Dietary Data: Exploring the Impact of Age and Gender on Calorie Consumption

A research project by **Mahitha Vontimitta**, **Veronica Angelina Itta**, and **Lavanya Ranganatham**

## Overview

This repository contains our analysis exploring how age and gender influence calorie consumption patterns in a demographically diverse population. Using data from the USDA FoodData Central, we investigated the relationships between demographic factors and dietary habits, focusing on calorie intake and various nutritional components.

## Research Question

What is the extent to which age and gender influence the variability in calorie consumption among individuals in a demographically diverse population, and how do potential interactions between age and gender contribute to these differences?

## Hypothesis

**Null Hypothesis (H0)**: There is no significant association between age and calorie intake among individuals in the population. Similarly, there is no significant difference in calorie intake between genders.

**Alternative Hypothesis (H1)**: There is a significant association between age and calorie intake among individuals in the population. Additionally, there is a significant difference in calorie intake between genders.

## Data Source

- **Source**: [USDA FoodData Central (FDC)](https://fdc.nal.usda.gov/)
- **Datasets Used**:
  - `DEMO.CSV`: Contains demographic information
  - `DSQTOT.CSV`: Contains dietary data

## Variables

The study analyzed the following variables:
- Age
- Gender
- Calorie Intake
- Protein
- Carbohydrates
- Fat
- Fiber
- Sugar
- Sodium

## Methodology

### Data Processing
- Data loading using the `read.csv()` function in R
- Data cleaning and merging based on the "SEQN" column (unique identifier)
- Replacement of missing values and preprocessing

### Analysis Techniques
1. **Data Visualization**
   - Box plots of calorie intake by age group
   - Density plots of calorie intake by gender
   - Histograms of calorie consumption
   - Scatter plots for correlation visualization

2. **Correlation Analysis**
   - Correlation matrix using Spearman method
   - Analysis of relationships between calories, age, and nutritional factors

3. **Statistical Testing**
   - **Kruskal-Wallis test**: Non-parametric test to determine differences across age groups
   - **Dunn's Test**: Post-hoc analysis for pairwise differences between age groups

4. **Regression Analysis**
   - **Linear Regression**: To evaluate the impact of age and gender on calorie consumption
   - **Logistic Regression**: To predict likelihood of high calorie intake based on demographics

## Key Findings

1. **Correlation Analysis Results**:
   - Calories strongly positively correlated with total fat (0.80), carbs (0.67), and protein (0.54)
   - Age shows weak negative correlations with most nutritional factors
   - Sugar intake moderately positively correlated with carbs (0.55) and calories (0.47)
   - Fiber intake has modest positive correlations with carbs (0.38), protein (0.29), and calories (0.28)
   - Moderately strong positive inter-correlations among protein, carbs, and total fat (0.42 to 0.55)

2. **Statistical Analysis Results**:
   - Significant differences in calorie consumption across different age groups (Kruskal-Wallis test)
   - Specific pairwise differences between age groups identified (Dunn's test)
   - Linear regression confirmed significant influence of age and gender on calorie intake
   - Interaction effects between age and gender were observed

3. **Key Conclusions**:
   - Younger age groups tend to have higher calorie needs
   - Males generally consume more calories than females
   - The relationship between age, gender, and calorie intake is multifaceted

## Applications and Future Directions

- Health authorities can develop personalized dietary guidelines based on age and gender demographics
- Nutritional programs can be designed to address specific dietary needs of diverse population segments
- Future research could investigate other factors influencing dietary behavior, such as socioeconomic status or cultural practices
- Longitudinal studies could explore changes in dietary habits over time and their impact on health outcomes

## Repository Structure

```
.
├── data/
│   ├── DEMO.CSV                # Demographic data
│   └── DSQTOT.CSV              # Dietary data
├── R/
│   ├── data_loading.R          # Data loading and preprocessing
│   ├── visualization.R         # Data visualization scripts
│   ├── correlation_analysis.R  # Correlation analysis
│   └── statistical_tests.R     # Statistical testing and regression models
├── results/
│   ├── figures/                # Generated visualizations
│   └── tables/                 # Statistical output tables
├── docs/
│   ├── presentation.pdf        # Project presentation slides
│   └── report.pdf              # Full research report
├── README.md
└── LICENSE
```

## Requirements

- R (version 4.0.0 or higher)
- Required R packages:
  - dplyr
  - ggplot2
  - tidyr
  - dunn.test

## Contributors

- Mahitha Vontimitta
- Veronica Angelina Itta
- Lavanya Ranganatham

## References

- FoodData Central. (n.d.). https://fdc.nal.usda.gov/
- Mikkelsen, B. E., Beck, A. M., & Lassen, A. D. (2006). Do recommendations for institutional food service result in better food service? A study of compliance in Danish hospitals and nursing homes from 1995 to 2002–2003. European Journal of Clinical Nutrition, 61(1), 129–134.
- Vaughan, L. E. (2006). Embedding Education into Diabetes Practice. Journal of Human Nutrition and Dietetics, 19(3), 240–241.
