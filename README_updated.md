
# User Behaviour Class Analysis in Mobile Device Data

## Project Overview

This project investigates the nature of **User Behaviour Classes** within a mobile device dataset. The primary objective is to identify and understand key factors influencing user engagement by analyzing demographic and behavioral metrics. The analysis progresses from initial descriptive statistics and visual exploration in Power BI to predictive modeling using logistic regression with dimension reduction techniques. 

## Tech Stack

- **Python**: Core programming language used for data analysis, modeling, and statistical calculations.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations and data handling.
- **scikit-learn**: For building predictive models, PCA, logistic regression, and validation techniques.
- **Power BI**: For creating descriptive visualizations and initial data exploration.
- **Matplotlib & Seaborn**: For data visualization and plotting of analysis results.
- **SciPy**: Used for hierarchical clustering and dendrogram visualization.

## Project Structure

### 1. Descriptive Statistics and Data Exploration
   - Using **Power BI**, we conducted an initial exploratory analysis, providing visual insights into user demographics, device types, and operating systems. The descriptive statistics also highlighted distinct characteristics of User Behaviour Classes across device models.
   - These insights established a foundation for further analysis, focusing on understanding how different attributes relate to User Behaviour Classes.

### 2. Correlation Analysis
   - A **correlation matrix** was used to assess relationships among attributes, revealing significant multicollinearity among quantitative variables.
   - To quantify this, we calculated the **Variance Inflation Factor (VIF)**, confirming the need for dimensionality reduction to avoid redundancy and improve model interpretability.

### 3. Dimensionality Reduction with PCA
   - **Principal Component Analysis (PCA)** was applied to manage multicollinearity. The **Scree Plot** indicated that the first component explained over 90% of the variance, while the second accounted for around 1.5%.
   - **Interpretation of PCA Components**:
      - **First Component**: Nearly evenly composed of all quantitative variables, suggesting it captures overall device usage trends.
      - **Second Component**: Heavily weighted on **Data Usage** (80%) and less correlated with User Behaviour Class and other quantitative variables, highlighting variability in usage patterns within each class.

### 4. Predictive Modeling with Logistic Regression
   - Based on the PCA results, the first two components were selected to train a **logistic regression model** for predicting User Behaviour Classes.
   - **Model Performance**: The model achieved over 90% accuracy, validated through cross-validation, indicating a reliable prediction of user class based on device usage patterns.

### 5. Visualization and Insights
   - A **scatter plot** of the PCA components reveals clear clusters for different User Behaviour Classes.
   - The **First Component** reflects a unified trend in total device usage time, while the **Second Component** (Data Usage) shows more variability within classes, suggesting it captures nuanced behavioral differences.
   - These findings support the hypothesis that User Behaviour Classes are primarily defined by total device usage time.

## Conclusion

The analysis demonstrates that User Behaviour Classes can be effectively distinguished based on device usage time, validated by PCA and logistic regression. This hypothesis is further supported by analyzing the average values of each quantitative variable across classes.

## Future Work

- **Clustering Analysis**: Applying clustering techniques, such as **k-means** or **hierarchical clustering**, on quantitative attributes could further validate the identified User Behaviour Classes.
- **Model Comparison**: Exploring alternative classification models (e.g., decision trees, SVM) could offer additional perspectives on model performance and robustness.

## Repository Structure

- `Data/`: Contains the original and preprocessed datasets.
- `Notebooks/`: Includes Jupyter notebooks with code for data analysis, visualization, and modeling.
- `Reports/`: Power BI reports summarizing descriptive statistics and initial visual exploration.
- `Models/`: Contains the logistic regression model and PCA results.

## Results

Through dimensionality reduction and logistic regression, the project achieved a highly accurate predictive model for User Behaviour Classes. Cross-validation confirms its robustness, making it a valuable tool for segmenting user behavior in mobile device contexts.

