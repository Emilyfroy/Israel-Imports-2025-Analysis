🇮🇱 Israel Imports Data Analysis – 2025
Exploring trends in Israel’s import market using real customs data

A comprehensive data analysis project built with Python, Pandas, Plotly, and Jupyter Notebook.

📌 Overview

This project analyzes Israel’s import activity for the year 2025 using official customs data.
The goal is to produce meaningful insights, high-quality visualizations, and a clear analytical workflow that demonstrates skills in:

Data cleaning & preparation

Feature engineering

Exploratory Data Analysis (EDA)

Visualization (Treemap, Donut Pie, Heatmap, Trendline…)

Business insights & interpretation

Working with real, messy data

This project is part of a Data Portfolio demonstrating creativity, curiosity, and analytical capabilities relevant to Industrial Engineering & Management.

📊 Dataset Description

The dataset contains detailed information on every import transaction to Israel in 2025:

Column	Description
Month	Month of import
Origin_Country	Country of origin
CustomsItem_8_Digits	HS classified product code
Quantity	Amount imported
Quantity_MeasurementUnitName	Unit (Litre/Kg/Tonne/Unit…)
NISCurrencyAmount	Import value in NIS
GoodsDescription	Short product category
FullGoodsDescription	Detailed product description

📁 The raw data is too large for GitHub, so only samples or processed files are included.

🧹 Data Cleaning Steps

Key preprocessing steps:

Converted HS codes to string format (leading zeros preserved)

Merged import data with the HS classification book

Removed rows with missing origin country

Handled inconsistent measurement units (kg vs tonne vs 1000 litres)

Converted tonne → kg

Separated datasets into volume-based and weight-based groups

Computed Price per Unit for each group

Detected outliers using IQR method and Winsorization

🔍 Exploratory Data Analysis (EDA)
✔ Top imported categories

We produced a Treemap showing the highest-value import categories and products.

(Insert image here)

✔ Crude Oil (Petroleum) Analysis

A deeper dive into one of Israel’s most important imports:

Identified top supplying countries

Examined monthly import trends

Compared volumetric vs weight-based pricing

Built Donut Pie chart (top 5 countries + other countries)

Built Heatmap of monthly import value per country

📈 Visualizations
🟦 Treemap – Imports by Goods Category & Product

Shows the structure of import value across categories.

![Treemap](graphs/treemap_products.png)

🟠 Donut Pie – Top 5 Oil Suppliers

Featuring custom colors + normalization to billions of NIS.

![Donut](graphs/oil_pie_donut.png)

🟩 Heatmap – Monthly Imports by Country

X = Month
Y = Top 20 countries
Color = Import value (Million NIS)

![Heatmap](graphs/oil_heatmap.png)

💡 Key Insights

Crude Oil is one of the top import categories in 2025.

Imports are highly concentrated among a small number of countries (top 5 > 80%).

Clear seasonality in monthly oil imports.

Large price variability due to differences in measurement units and product type.

Electronics (smartphones, chips) and diamonds are also major import sectors.

🗂 Project Structure
Imports2025/
│
├── notebooks/
│   ├── data_cleaning.ipynb
│   ├── oil_analysis.ipynb
│   └── visualization.ipynb
│
├── src/
│   ├── utils.py
│   ├── cleaning.py
│   └── plots.py
│
├── data/
│   ├── imports_sample.csv
│   └── data_info.txt
│
├── graphs/
│   ├── treemap_products.png
│   ├── oil_pie_donut.png
│   └── oil_heatmap.png
│
├── README.md
└── requirements.txt

🛠 Technologies & Tools

Python 3.10+

Pandas

NumPy

Plotly Express

Jupyter Notebook

Git + GitHub

VSCode / PyCharm

▶️ Running the Project

Install dependencies:

pip install -r requirements.txt


Run Jupyter:

jupyter notebook


Or run any script in src/.

🚀 Future Improvements

Build dashboard in Power BI or Plotly Dash

Include predictive modeling for monthly import forecasting

Add clustering of product categories

Automate ETL to clean and merge new years of data

👩‍💻 Author

Emily Froymovich
Industrial Engineering & Management
Israel, 2025

