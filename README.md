# Sea-Level-Pressure

## Problem Statement

Weather forecasting and climate monitoring depend heavily on understanding the factors that influence atmospheric conditions. Sea level pressure is one of the most important meteorological measurements because it affects weather patterns, storm development, and climate behavior.

However, meteorological datasets often contain numerous interrelated variables, making it difficult to determine which factors significantly influence sea level pressure and how those relationships interact.

The objectives of this project were to:

* Identify meteorological variables that significantly influence sea level pressure.
* Determine which predictors have the strongest relationships with atmospheric pressure.
* Build reliable multiple linear regression models for predicting sea level pressure.
* Improve predictive performance through interaction modeling and model selection techniques.
* Validate model accuracy using cross-validation and bootstrapping methods.

Using 365 days of weather observations from Denver, Colorado, this study examines the predictive effects of temperature, visibility, dew point, wind speed, and maximum wind gust on sea level pressure.

---

## Methodology

### Dataset

The dataset was obtained from the USAF Climatology Center and contains 365 daily weather observations recorded in Denver, Colorado during 2018.

### Variables Used

**Response Variable**

* Sea Level Pressure (SLP)

**Predictor Variables**

* Mean Temperature (TEMP)
* Mean Visibility (VISIB)
* Mean Dew Point (DEWP)
* Mean Wind Speed (WDSP)
* Maximum Wind Gust (GUST)

An additional seasonal feature was created to support exploratory analysis and visualization.

### Research Workflow

1. Data Cleaning and Preparation

   * Selected relevant variables
   * Converted season into a categorical factor
   * Checked for missing and unusual values

2. Exploratory Data Analysis (EDA)

   * Histograms
   * Scatterplot matrices
   * Correlation analysis
   * Seasonal comparisons
   * Distribution assessments

3. Regression Modeling

   * Built a first-order multiple linear regression model
   * Developed a full two-way interaction model
   * Evaluated statistical significance of predictors

4. Model Selection

   * Forward Selection
   * Backward Elimination
   * Stepwise Selection
   * AIC and BIC comparison

5. Model Validation

   * Residual diagnostics
   * Variance Inflation Factor (VIF) analysis
   * 10-Fold Cross Validation
   * Leave-One-Out Cross Validation (LOOCV)
   * Bootstrap resampling (5,000 iterations)

---

## Tools & Technologies

* R
* RStudio
* Tidyverse
* Caret
* MASS
* GGally
* RMS
* Statistical Modeling
* Data Visualization
* Multiple Linear Regression
* Cross Validation
* Bootstrap Analysis

---

## Explanation

Multiple linear regression was used to investigate the relationships between sea level pressure and several meteorological predictors while accounting for the influence of multiple variables simultaneously.

The analysis focused on:

* Measuring the significance of individual weather variables.
* Evaluating interactions between predictors.
* Assessing model assumptions and validity.
* Improving predictive accuracy through model selection and validation techniques.

The project emphasized:

* Statistical reliability
* Model interpretability
* Predictive performance
* Scientific validity

A key finding was that the interaction between temperature and dew point contributed meaningful explanatory power beyond the effects of the individual variables alone.

---

## Results

### Significant Predictors

The analysis found statistically significant evidence that:

* Temperature predicts sea level pressure (**p < 0.0001**)
* Visibility predicts sea level pressure (**p = 0.0056**)
* Dew Point predicts sea level pressure (**p < 0.0001**)
* Wind Speed predicts sea level pressure (**p < 0.0001**)
* Maximum Wind Gust predicts sea level pressure (**p = 0.0007**)

### Key Findings

* Temperature exhibited the strongest relationship with sea level pressure.
* Visibility showed the weakest correlation.
* All regression assumptions were satisfied.
* Multicollinearity remained within acceptable limits.
* Interaction effects improved overall model performance.
* The Temperature × Dew Point interaction emerged as the most influential interaction term.

### Model Performance Improvements

The interaction model:

* Increased explanatory power
* Reduced prediction error
* Improved cross-validation performance
* Produced lower RMSE and MAE values
* Achieved higher R² and Adjusted R² values

These results demonstrate the value of incorporating interaction effects when modeling complex atmospheric systems.

---

## Accuracy Metrics

### Primary Model Metrics

| Metric      | First-Order Model | Interaction Model |
| ----------- | ----------------- | ----------------- |
| R²          | 0.3836            | 0.4524            |
| Adjusted R² | 0.3750            | 0.4289            |
| RMSE        | 5.5788            | 5.2579            |
| MAE         | 4.3161            | 4.0582            |
| AIC         | 2304.68           | 2281.43           |
| BIC         | 2331.98           | 2347.72           |

### Cross-Validation Results

#### 10-Fold Cross Validation

| Model       | RMSE   | R²     | MAE    |
| ----------- | ------ | ------ | ------ |
| First-Order | 5.6244 | 0.3794 | 4.3823 |
| Interaction | 5.4347 | 0.4247 | 4.2199 |

#### Leave-One-Out Cross Validation

| Model       | RMSE   | R²     | MAE    |
| ----------- | ------ | ------ | ------ |
| First-Order | 5.6720 | 0.3631 | 4.3885 |
| Interaction | 5.4807 | 0.4066 | 4.2408 |

### Evaluation Highlights

* Adjusted R² improved significantly after incorporating interaction terms.
* Feature selection improved predictive reliability.
* Statistical significance testing strengthened model interpretability.
* Residual diagnostics confirmed model validity.
* Bootstrap confidence intervals demonstrated model stability.
* Visualization techniques improved communication of results.

---

## Lessons Learned

This project strengthened my understanding of statistical modeling and predictive analytics in environmental science.

### Key Takeaways

* Data cleaning and preprocessing are critical for building reliable models.
* Exploratory data analysis helps uncover meaningful relationships before modeling.
* Multicollinearity can impact coefficient interpretation and must be evaluated carefully.
* Statistical significance testing is essential for identifying meaningful predictors.
* Interaction effects can reveal important relationships hidden in simpler models.
* Cross-validation provides a more realistic assessment of model performance.
* Bootstrapping is a valuable technique for evaluating model stability and uncertainty.
* Model interpretability is just as important as predictive accuracy.

### Skills Developed

* Multiple Linear Regression
* Predictive Analytics
* Statistical Analysis
* Model Selection
* Cross Validation
* Bootstrap Resampling
* Data Visualization
* Data Interpretation
* Research Communication
* Scientific Reporting

---

## Conclusion

This project successfully developed and validated multiple linear regression models to predict sea level pressure using meteorological data from Denver, Colorado.

The final interaction model outperformed the baseline model, explaining approximately **45% of the variability in sea level pressure** while achieving lower prediction error and stronger validation results. Temperature emerged as the strongest predictor, and the interaction between temperature and dew point significantly improved model performance.

These findings demonstrate how statistical modeling techniques can be used to better understand atmospheric behavior, improve predictive accuracy, and support data-driven decision-making in climatology and environmental research.
