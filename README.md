 🧳 Gezinomi Data Analysis Project

This project is a **data analysis study** on a travel booking dataset.  
The goal is to **explore customer behavior, pricing trends, and booking patterns** to create customer personas and revenue-based segments.

---

## 🎯 Objectives
- Clean and preprocess travel booking data
- Perform exploratory data analysis (EDA) with visualizations
- Calculate average earnings based on cities, hotel concepts, and seasons
- Create **level-based personas** by combining multiple features
- Segment customers into groups based on their spending potential
- Estimate revenue for new customers based on their profiles

---
```
## 📂 Project Structure
gezinomi_data_project/
├── gezinomi_data_project.ipynb   Jupyter Notebook with full analysis
└── README.md                     Project description

```

---


## 🛠️ Tools & Libraries
- **Python 3.9+**
- **Pandas** – data cleaning and aggregation
- **NumPy** – numerical operations
- **Matplotlib & Seaborn** – visualizations
- **Jupyter Notebook** – interactive development

---

## 🔍 Analysis Steps

### 1. Data Loading & Cleaning
- Loaded the dataset (`miuul_gezinomi.csv`)
- Converted `Price` from string to float
- Inspected unique values for **cities** and **hotel concepts**

### 2. Exploratory Data Analysis
- Calculated total and average price by **city** and **concept**
- Visualized:
  - Number of sales by city (bar chart)
  - Distribution of sales by hotel concept (pie chart)
  - Price variations across cities and concepts (bar plots)
  - Stacked bar chart for city-concept sales comparison

### 3. Booking Category Feature
- Created `BookingCategory` based on how early the booking was made:
  - **Last Minuters** (0-7 days before)
  - **Potential Planners** (7-30 days)
  - **Planners** (30-90 days)
  - **Early Bookers** (90+ days)

### 4. Revenue Breakdown
- Calculated mean price and sales count by:
  - **City, Concept, and Booking Category**
  - **City, Concept, and Season**

### 5. Persona Creation
- Created a new variable `sales_level_based` combining:
  - `SaleCityName`, `ConceptName`, and `Seasons`

Example:
```
ANTALYA_HERŞEY DAHIL_HIGH
GIRNE_YARIM PANSIYON_LOW
```
### 6. Customer Segmentation
- Divided personas into 4 segments (`A`, `B`, `C`, `D`) using **quartiles of Price**  
- Calculated mean, max, and total revenue for each segment

### 7. Revenue Prediction for New Customers
- Estimated expected revenue and segment for new customers.  
Example:
- **ANTALYA_HERŞEY DAHIL_HIGH** → Expected revenue: X, Segment: A  
- **GIRNE_YARIM PANSIYON_LOW** → Expected revenue: Y, Segment: C  
