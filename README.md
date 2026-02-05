# 📊 Amazon Sales Analysis Dashboard (Power BI)

## 📌 Project Overview
This project is a **Power BI dashboard** built to analyze Amazon sales data and extract meaningful business insights. The dashboard focuses on **Month-by-Month (MoM) sales performance**, product trends, and regional distribution using **DAX and proper data modeling techniques**.

The project also includes **data cleaning and preprocessing using Python**, showcasing an end-to-end analytics workflow from raw data to insights.

---

## 🎯 Objectives
- Clean and prepare raw sales data using Python  
- Analyze total sales performance across product categories and sizes  
- Track **Month-over-Month (MoM) sales trends**  
- Understand sales distribution across shipping states  
- Build an interactive and business-ready dashboard  

---

## 🗂️ Dataset
The dataset contains Amazon sales transaction data with the following key fields:
- Order Date  
- Sales Amount  
- Product Category  
- Product Size  
- Shipping State  
- Sales Channel  

Before loading into Power BI, the raw data was **cleaned and transformed using Python**.

---

## 🧹 Data Cleaning (Python)
Python was used for data preprocessing to ensure clean and analysis-ready data.

### Key steps included:
- Handling missing and null values  
- Standardizing date formats  
- Cleaning categorical values (category, size, state names)  
- Removing duplicates and inconsistent records  
- Exporting cleaned data for Power BI consumption  

**Tools used:**
- Python
- Pandas
- NumPy

---

## 🧠 Key Features
- 📅 Month-by-Month sales trend analysis  
- 🧮 DAX measures for current and previous month sales  
- 📊 Category-wise and size-wise sales distribution  
- 🌍 State-wise shipping and sales analysis  
- 🎛️ Interactive slicers and drill-down visuals  

---

## 🛠️ Tools & Technologies
- **Python (Pandas, NumPy)** – Data Cleaning & Preparation  
- **Power BI Desktop** – Data Visualization  
- **DAX (Data Analysis Expressions)**  
- Data Modeling (Star Schema)  
- Microsoft Excel (initial data exploration)

---

## 📐 Data Modeling
- Created a **dedicated Date table**
- Established a **one-to-many relationship** between Date and Sales tables
- Used Date table columns for all time-based visuals
- Avoided auto date hierarchy for accurate time intelligence

---

## 📊 DAX Measures Used

### 📅 Date Table
```DAX
Date =
ADDCOLUMNS (
    CALENDAR (
        MIN ( 'Amazon Sale Report'[Date] ),
        MAX ( 'Amazon Sale Report'[Date] )
    )
)
