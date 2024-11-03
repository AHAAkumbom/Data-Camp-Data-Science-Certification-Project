<img width="1128" alt="DS - LinkedIn" src="https://github.com/user-attachments/assets/baa1cbfd-01ca-473d-9299-57bf46e0e86f">

# DataCamp's Data Scientist Professional Certification
## Recipe Site Traffic
This project aims to predict high-traffic recipes and achieve an 80% accuracy rate in these predictions.

## Project Overview

1. **Dataset Description**:
   - **Observations**: 947
   - **Columns**: 8 (1 unique recipe ID, 4 numerical attributes - calories and three nutritional components, 2 categorical attributes - "category" and "servings," and 1 target variable indicating high traffic status)
   - After preprocessing, the dataset was refined to 895 observations.

2. **Data Preprocessing**:
   - **Steps Taken**: Removed duplicates, handled missing values, and converted data types as needed.
   - **Outcome**: A clean dataset prepared for further analysis.

3. **Exploratory Data Analysis (EDA)**:
   - **Pairplot**: Showed minimal correlation among numerical variables, preventing biases in model development.
   - **Histograms**: Indicated right-skewed distributions for calories and nutritional components, suggesting a preference for median as a statistical measure.
   - **Boxplots**: Highlighted right-skewed distributions and outliers, further supporting the use of median.

4. **Category Analysis**:
   - Median values for calories and nutritional components varied across categories, with the food category influencing these attributes.
   - Serving counts and certain categories were linked to higher traffic rates:
     - High-traffic categories: "Vegetable," "Potato," and "Pork."
     - Low-traffic category: "Beverages."

## Model Development

1. **Transformations**:
   - **Numerical Variables**: Yeo-Johnson transformation was used to address right-skewed distributions.
   - **Categorical Variables**: One-hot encoding applied to the "category" column.

2. **Model Selection**:
   - Given the binary target variable, binary classification models were chosen: Logistic Regression, Decision Tree, Random Forest, and Support Vector Machines.
   - **Baseline Model**: Logistic Regression, with other models serving as comparisons.

3. **Model Evaluation**:
   - Logistic Regression achieved 80.87% precision, meeting the 80% accuracy goal.
   - Decision Tree and Random Forest displayed overfitting, while Support Vector Machines showed underfitting.

## Key Insights and Recommendations

- **High Traffic Prediction Precision**: Emphasis on minimizing false negatives to avoid missing high-traffic recipes.
- **Key Performance Indicator (KPI)**: Introduced "High Traffic Conversion Rate" (True Positive / False Positive ratio) with a benchmark of >4.0 for model performance.
- **Business Insights**:
   - Recommended focus on "Vegetable," "Potato," and "Pork" categories for high traffic.
   - Consider deprioritizing the "Beverages" category due to lower traffic rates.

## Conclusion

Our project fulfilled its objectives by using the Logistic Regression model to predict high traffic recipes with 80% accuracy. The "High Traffic Conversion Rate" KPI and category insights offer valuable guidance for optimizing site content and predicting traffic effectively.
