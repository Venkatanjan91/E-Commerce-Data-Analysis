# 📊 E-Commerce Data Analysis  

## 📌 Project Overview  
This project analyzes sales and shipping performance using the **Sample Superstore dataset**.  
The goal is to explore patterns in orders, shipments, and profitability, and to visualize insights with interactive dashboards.  

### Objectives:  
- Clean and preprocess raw data  
- Perform exploratory data analysis (EDA)  
- Convert date columns for time-based insights  
- Build interactive visualizations with Plotly  
- Derive actionable business insights  

---

## 📂 Dataset  
- **File:** `Sample - Superstore.csv`  
- **Features include:**  
  - Order & Ship Dates  
  - Category & Sub-Category  
  - Region  
  - Sales, Quantity, Discount, Profit  

---

## ⚙️ Tech Stack  
- **Python** – Core programming  
- **Pandas** – Data cleaning & analysis  
- **Plotly (Express & Graph Objects)** – Interactive charts  
- **Jupyter Notebook** – Development & exploration  

---

## 📑 Project Workflow  

1. **Import Libraries**  
   ```python
   import pandas as pd
   import plotly.express as px
   import plotly.graph_objects as go
   import plotly.io as pio
Load Dataset
```python
data = pd.read_csv('Sample - Superstore.csv', encoding='latin-1')
```

Explore Data
```python
data.head()       # Preview first rows  
data.info()       # Check column types & nulls  
data.describe()   # Summary statistics  

```
Preprocess Data
```python
data['Order Date'] = pd.to_datetime(data['Order Date'], format='mixed')
data['Ship Date'] = pd.to_datetime(data['Ship Date'], format='mixed')

data['Order Year'] = data['Order Date'].dt.year
data['Order Month'] = data['Order Date'].dt.month
data['Order Day of Week'] = data['Order Date'].dt.dayofweek

```
Analysis & Visualizations

Sales & profit trends over time

Regional and category performance

Shipping delays vs order dates

Profitability by sub-category

## 📊 Example Insights

Certain categories drive high sales but low profit due to discounts.

Monthly sales trends reveal seasonal peaks.

Shipping delays differ significantly across regions.

## 🚀 How to Run

You can run this project directly in Google Colab without installing anything:

Open the Colab Notebook using this link:

👉[** Open in Colab**] (https://colab.research.google.com/drive/1IkC9NmmiRSiQZPRWR3qR5YFerOSwYQMH?usp=sharing)

Go to File → Save a copy in Drive to make your own editable copy.

Run each cell step by step to reproduce the analysis.

📜 License

This project is licensed under the MIT License.
