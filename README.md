# Power BI Sales Dashboard – Skill Nexis - Week 1

## 📊 Project Overview

This project is a **Power BI sales dashboard** created as part of **Week 1: Introduction to Power BI & Data Modelling**.

The dashboard was developed using a **700-record Excel sales dataset** and demonstrates the basic Power BI workflow of importing data, cleaning and transforming it using **Power Query**, creating calculations and **DAX measures**, and presenting the results through interactive visualisations.

The Week 1 project specifically requires a simple sales dashboard showing:

* Total Revenue
* Sales by Region
* Top 5 Products by Profit

## The practice exercises additionally cover Excel data import, replacing null values, creating a calculated column, and renaming and formatting data fields.

## 🎯 Project Objectives

The main objectives of this project were to:

* Understand the Power BI Desktop interface and basic workflow.
* Import sales data from an Excel workbook.
* Clean and transform data using Power Query.
* Handle missing/null values.
* Rename and format data fields appropriately.
* Create a calculated column using DAX.
* Create measures for revenue and profit analysis.
* Build visualisations to analyse sales performance.
* Use slicers to interactively filter the dashboard.
* Apply basic data modelling concepts.

---

## 📁 Dataset

**Source:** `Sample_data.xlsx`

The dataset contains **700 records** covering the years **2013 and 2014**.

### Main fields used in the analysis

* Segment
* Country
* Product
* Discount Band
* Units Sold
* Manufacturing Price
* Sale Price
* Gross Sales
* Discounts
* Sales
* COGS
* Profit
* Date
* Month Number
* Month Name
* Year

### Data Cleaning

The following Power Query cleaning steps were performed:

* Replaced blank values in the **Discount Band** field with `"Not Available"`.
* Renamed the `Sales` field to remove the unwanted leading space in the original column name.
* Checked and applied appropriate data types.
* Renamed and formatted fields where required.

The practice set specifically requires replacing null values with **“Not Available”** and renaming and formatting the data fields.

---

## 🔄 Power Query Transformation

Power Query was used before creating the dashboard to prepare the dataset for analysis.

The main transformation performed was:

```text
Blank Discount Band
        ↓
"Not Available"
```

Additional preparation included checking field names and data types so that the data could be used correctly in calculations and visualisations.

Power BI's Power Query environment is intended for data transformation and manipulation before analysis. The reference material also covers cleaning, filtering and combining data using Power Query.

---

## 🧮 Calculated Column

A calculated column was created to demonstrate the Week 1 calculation exercise:

```DAX
Total = Sales_Data[Units Sold] * Sales_Data[Sale Price]
```

This represents the total value calculated from units sold and sale price.

The practice exercise specifies the calculation concept as:

```text
Total = Qty × Price
```

which was implemented using the corresponding fields available in the supplied dataset.

---

## 📐 DAX Measures

The dashboard uses DAX measures to calculate key business metrics.

### Total Revenue

```DAX
Total Revenue = SUM(Sales_Data[Sales])
```

### Total Profit

```DAX
Total Profit = SUM(Sales_Data[Profit])
```

### Total Units Sold

```DAX
Total Units = SUM(Sales_Data[Units Sold])
```

An optional profit margin calculation can also be represented as:

```DAX
Profit Margin % = DIVIDE([Total Profit], [Total Revenue])
```

---

## 📈 Dashboard Visualisations

The completed dashboard contains the three main outputs required for the Week 1 project.

### 1. Total Revenue

A **Card visual** is used to display total revenue.

**Metric:**

```text
Total Revenue
```

The dashboard displays approximately:

```text
₹118.7M
```

Revenue is based on the **Sales** column, representing net sales after discounts.

---

### 2. Sales by Region

The dataset does not contain a separate `Region` field, so **Country** is used to represent the requested regional sales analysis.

A bar chart displays revenue by country.

| Country                  | Revenue |
| ------------------------ | ------: |
| United States of America |  ₹25.0M |
| Canada                   |  ₹24.9M |
| France                   |  ₹24.4M |
| Germany                  |  ₹23.5M |
| Mexico                   |  ₹20.9M |

The dashboard therefore uses **Country as the geographical grouping for the Region analysis**.

---

### 3. Top 5 Products by Profit

A bar chart displays the **top five products based on total profit**.

| Rank | Product  | Profit |
| ---- | -------- | -----: |
| 1    | Paseo    |  ₹4.8M |
| 2    | VTT      |  ₹3.0M |
| 3    | Amarilla |  ₹2.8M |
| 4    | Velo     |  ₹2.3M |
| 5    | Montana  |  ₹2.1M |

The dataset contains six products. Therefore, **Carretera** is excluded from the Top 5 visual.

---

## 🎛️ Interactive Filters

The dashboard includes filters for:

* **Year**
* **Segment**

These slicers allow users to filter the dashboard and examine sales performance for different years and business segments.

Slicers are visual filters in Power BI and can be used to filter data interactively.

---

## 🗂️ Data Modelling

The Week 1 material introduces relationships and data models as an important part of Power BI.

For this project, the supplied dataset is contained in a single Excel table, so the dashboard does not require multiple-table relationships.

The project therefore focuses primarily on:

```text
Excel Dataset
      ↓
Power Query
      ↓
Cleaned Data
      ↓
Calculated Column + DAX Measures
      ↓
Power BI Visualisations
      ↓
Interactive Dashboard
```

The reference material explains the role of fact and dimension tables and the importance of data modelling when working with multiple related datasets.

---

## 🔍 Key Dashboard Insights

The completed dashboard provides a quick overview of sales performance:

* Total revenue is approximately **₹118.7 million**.
* The **United States of America** contributes the highest revenue among the countries shown.
* **Paseo** is the highest-profit product.
* The Top 5 product analysis excludes **Carretera**, which has the lowest profit among the six products.
* The dashboard can be filtered by **Year** and **Segment**.

---

## 🛠️ Tools & Skills Used

### Tools

* Microsoft Power BI Desktop
* Power Query
* DAX
* Microsoft Excel

### Skills Demonstrated

* Data importing
* Data cleaning
* Data transformation
* Null-value handling
* Data type management
* Calculated columns
* DAX measures
* Data visualisation
* Interactive filtering
* Basic data modelling
* Dashboard design

## The reference lab material covers Power BI visualisations including bar charts, column charts, tables and slicers, which are relevant to the dashboard developed in this project.

## 📂 Repository Files

```text
PowerBI-Sales-Dashboard/
│
├── README.md
├── week1_sales_dashboard.pbix
├── week1_sales_dashboard.pdf
├── dashboard_preview.png
└── Sample_data.xlsx
```

### File Descriptions

**`week1_sales_dashboard.pbix`**
The original Power BI Desktop project file containing the data model, Power Query transformations, DAX calculations and dashboard.

**`week1_sales_dashboard.pdf`**
PDF export of the completed dashboard.

**`dashboard_preview.png`**
Preview image of the dashboard for viewing directly on GitHub.

**`Sample_data.xlsx`**
Original Excel dataset used as the source for the project.

---

## ▶️ How to Open the Project

To explore the project:

1. Download `week1_sales_dashboard.pbix`.
2. Open the file using **Microsoft Power BI Desktop**.
3. Review the Report view to explore the dashboard.
4. Use the **Year** and **Segment** slicers to interact with the report.
5. Open the data and model views to examine the calculations and structure.

Power BI Desktop is used to create data models, reports and visualisations and can also publish reports to the Power BI service.

---

## 📌 Project Context

**Course/Module:** Week 1 – Introduction to Power BI & Data Modelling
**Project Type:** Sales Dashboard
**Dataset:** Sample_data.xlsx
**Records:** 700
**Years Covered:** 2013–2014
**Platform:** Microsoft Power BI Desktop

---

## 👤 Author

**Shruti Gupta**

This project was created as a practical exercise to develop foundational skills in **Power BI, Power Query, DAX, data analysis and dashboard development**.

