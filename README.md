# Supermarket Sales Analysis & Prediction

Overview:
This project demonstrates an end-to-end data analytics and machine learning workflow on supermarket sales data. It focuses on:
- Exploratory Data Analysis (EDA) to uncover sales patterns, transaction distributions, and customer behavior.
- Data Visualization including line plots, histograms, boxplots, and sales segment distributions.
- Machine Learning Modeling to predict gross income per transaction using Random Forest and Gradient Boosting Regressors.
The goal is to showcase the ability to transform raw data into actionable insights to support business decisions in retail.

Dataset:
- Source: https://github.com/sushantag9/Supermarket-Sales-Data-Analysis
- Features: Branch, City, Customer Type, Gender, Product Line, Unit Price, Quantity, Tax, Total, Date, Time, Payment, Rating, Gross Income, and more.
- Contains transactional records over three months.

Exploratory Data Analysis (EDA):
- Total sales fluctuate significantly; spikes may correspond to promotions or paydays.
- Most transactions are low-to-mid value, while high-value purchases, though rare, contribute disproportionately to revenue.
- Gross income distribution is right-skewed; most profits come from small-to-medium transactions.
- Customer ratings indicate Branch B shows slightly lower median and more variation compared to Branch A and C.
- Visualizations include total sales over time, histogram of total sales and gross income, sales segmentation countplots, and boxplots/stripplots for customer ratings.

Machine Learning: Gross Income Prediction
Objective: Predict gross income per transaction using ensemble regression models.

Models:
Random Forest Regressor    - MAE: 7.01, RMSE: 10.57, R²: 0.99827
Gradient Boosting Regressor - MAE: 6.46, RMSE: 8.78, R²: 0.99882
- Gradient Boosting slightly outperforms Random Forest.
- Extremely high R² is due to the deterministic relationship: gross income = Unit Price × Quantity.

Feature Importance:
- Unit Price and Quantity dominate predictions.
- Secondary features (Branch, Payment, Product Line, Hour, Week, Rating) show subtle, data-driven patterns:
  - Certain branches consistently bring slightly higher revenue.
  - Peak hours moderately affect gross income.

Predicted vs Actual & Residual Analysis:
- Predictions closely match actual values.
- Residuals are centered around zero, indicating stable performance.
- Highlights nuanced deviations and potential outliers.

Key Takeaways:
- Implemented an end-to-end ML workflow: preprocessing, encoding, ensemble modeling, evaluation, and visualization.
- Gradient Boosting Regressor is recommended for gross income prediction.
- Demonstrates the ability to extract actionable insights even when primary predictors dominate.
- Reinforces understanding of sales patterns, customer behavior, and operational metrics in retail.

Files & Outputs:
- *.png → visualizations of trends, distributions, residuals, and feature importance
- supermarket-sales-analysis.ipynb → original Jupyter notebook
- supermarket-sales-analysis.py → exported Python script

Tech Stack:
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (Random Forest & Gradient Boosting Regressors)

License:
Please star this project adn follow my GitHub. This project is released under The Unlicense. You are free to use, modify, and distribute it for any purpose without restriction.
© 2025 RsydMathTech
