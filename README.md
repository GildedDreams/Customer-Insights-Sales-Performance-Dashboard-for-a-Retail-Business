# Customer Insights & Sales Performance Dashboard for a Retail Business

An end-to-end retail analytics project combining interactive data visualisation, exploratory data analysis, sales forecasting, product demand prediction, and customer churn classification using Python and machine learning.

## Overview

This project analyses retail sales and customer data to uncover sales trends, evaluate product performance, estimate profitability, and explore customer churn risk. It combines an interactive dashboard with machine learning models to demonstrate how data analytics can support business and inventory decisions.

## Key Features

- **Sales Analytics Dashboard:** Interactive visualisations of revenue, estimated profit, monthly sales trends, top-performing products, customer segments, and regional sales.
- **Exploratory Data Analysis:** Analysis of sales patterns, product performance, order quantities, and estimated profit margins.
- **Sales Forecasting:** Random Forest regression and moving-average forecasting to estimate future monthly sales.
- **Product Demand Prediction:** Machine learning pipeline to predict order quantities using product, customer, regional, pricing, and order-related features.
- **Customer Churn Classification:** Random Forest classifier using customer behaviour and satisfaction features, with synthetically generated churn labels.
- **Inventory Insights:** Product sales-velocity analysis to identify potentially slow-moving products and dead-stock candidates.
- **Model Evaluation:** Evaluation using appropriate regression and classification metrics, including MAE, RMSE, R², precision, recall, F1-score, and confusion matrices.

## Technologies Used

- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** Scikit-learn
- **Visualisation:** Plotly, Matplotlib
- **Interactive Dashboard:** Plotly, ipywidgets
- **Development Environment:** Jupyter Notebook

## Project Structure

```text
retail-analytics-dashboard/
├── customers.csv
├── customers_with_churn_label.csv
├── merged_rows.csv
├── powerbi_sales_dataset.csv
├── dashboard.py / dashboard.ipynb
├── sales_forecasting.py
├── product_demand_prediction.py
├── customer_churn_prediction.py
├── category_analysis.py
└── README.md
```

## Machine Learning Approach

### 1. Sales Forecasting

Monthly sales are aggregated from transaction data. Depending on the amount of historical data available, the project uses a moving-average baseline or a Random Forest regression model with date-based features, lagged sales, and rolling averages.

### 2. Product Demand Prediction

A preprocessing pipeline handles numerical and categorical features, including customer segment, region, city, product, category, price, and order status. A Random Forest regressor predicts order quantities and is evaluated using regression metrics.

### 3. Customer Churn Classification

Customer behaviour indicators, including time since the last purchase, repeat purchase rate, satisfaction score, and newsletter subscription, are used to construct a synthetic churn-risk score. A Random Forest classifier is trained to classify customers into churn-risk groups.

**Important limitation:** The churn labels are artificially generated from a rule based on customer features rather than actual observed churn outcomes. Consequently, the model demonstrates a classification workflow but does not establish real-world churn prediction accuracy.

## Dashboard Insights

The dashboard supports exploration of:

- Total revenue and estimated profit
- Monthly revenue trends and growth
- Top products by revenue
- Revenue distribution across customer segments
- Regional sales patterns
- Sales performance by date range, region, and category

## Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace the URL with your actual GitHub repository URL.

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib scikit-learn plotly ipywidgets jupyter
```

### 3. Prepare the datasets

Place the required CSV files in the appropriate directory and ensure the column names match those expected by each script.

### 4. Run the project

Run the relevant Python scripts or open the Jupyter Notebook files to execute the analysis, train the models, and generate visualisations.

For the interactive dashboard, launch Jupyter Notebook and run the dashboard notebook if the implementation uses `ipywidgets`.

## Limitations

- Forecasting and classification performance depends on the quality, size, and representativeness of the available datasets.
- Synthetic churn labels are not a substitute for verified historical churn data.
- Estimated profit and inventory classifications are analytical estimates and may not reflect actual business outcomes.
- Model performance should be interpreted using the evaluation results obtained from the datasets rather than assumed in advance.

## Future Improvements

- Validate churn predictions using real historical customer-retention data.
- Improve forecasting through time-series validation and comparison with baseline models.
- Add automated reporting and more advanced dashboard filtering.
- Incorporate verified inventory and customer-retention outcomes.
- Deploy the dashboard as a web application.

## Disclaimer

This project is intended for educational and analytical purposes. Its outputs illustrate data analysis and machine learning techniques and should not be treated as verified business forecasts without further validation.

## Author(s)
**Aditya Naveen Sharma**
**Sushant Suhas Bhase**
GitHub: [GildedDreams]((https://github.com/GildedDreams/))
