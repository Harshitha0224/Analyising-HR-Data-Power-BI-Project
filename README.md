# Analyising-HR-Data-Power-BI-Project
This Power BI project focuses on analysing **employee attrition** and overall **HR performance metrics** to help organisations understand the key drivers behind employee turnover.

The dashboard provides insights into:
- Attrition rate trends
- Workforce age demographics
- Department-wise attrition
- Gender and job satisfaction breakdowns


## 🧠 Skills & Tools Used
- **Power BI** – Data visualization and dashboard creation  
- **Power Query Editor** – Data cleaning and transformation  
- **DAX (Data Analysis Expressions)** – Calculated measures  
- **Excel** – Raw dataset  
- **Data Modelling** – Relationships and data structure setup  


## 🧹 Data Preparation

1. **Data Cleaning:**
   - Promoted headers (first row as column names)
   - Removed unnecessary columns and null values  
   - Standardized data types for numerical and categorical columns  

2. **Conditional Column for Attrition Count:**
   ```DAX
   Attrition Count =
   IF('HR data'[Attrition] = "Yes", 1, 0)

Calculated Measures:

1.  **Attrition Rate**
 ```DAX
 Attrition Rate =
SUM('HR data'[Attrition Count]) / SUM('HR data'[Employee Count])
```
2. **Active Employees**
```DAX
Active Employees =
SUM('HR data'[Employee Count]) - SUM('HR data'[Attrition Count])

```
Sorting by Age Band:
Created a new conditional column for sorting:

```nginx
Under 25  → 1  
25–34     → 2  
35–44     → 3  
45–54     → 4  
55+       → 5
```
**Dashboard Insights**

![HR Analytics Dashboard](images/HR%20Analytics%20Dashboard.png)

🧾 1. **Overall HR Summary**

![KPI Cards](images/KPI%20Cards.png)

Includes key metrics such as total employees, active employees, attrition rate, and average age.

📉 2. **Attrition Rate by Department**

![Department-wise Attrition](images/department-wise%20attrition.png)

Shows which departments have the highest attrition percentages to help HR identify problem areas.

👩‍💼 3. **Employee Count by Gender**

![Gender-wise Employee Distribution](images/gender-wise%20employee%20distribution.png)

Visualizes workforce diversity and gender balance.

🧓 4. **Employee Count by Age Group**

![Age-group-wise Employee Count](images/age-group-wise%20employee%20count.png)

Highlights which age ranges have the most employees and where attrition is highest.

💬 5. **Job Satisfaction and Attrition Correlation**

![Job Satisfaction vs Attrition](images/job%20satisfaction%20vs%20attrition.png)

Analyses whether satisfaction ratings influence employee turnover.

📅 6. **Education Field and Attrition**

![Education-wise Attrition](images/education-wise%20attrition.png)

Shows which educational backgrounds have higher or lower attrition rates.

# 🚀 Key Insights

- The highest attrition was found in the 25–34 age group.
- Sales and HR departments showed higher turnover compared to other teams.
- Job satisfaction has a visible impact on attrition trends.
Younger employees are more likely to leave within their first few years.

# Project Learnings
- Data transformation and modelling using Power Query
- Writing DAX measures for key KPIs
- Creating visually appealing Power BI dashboards
- Deriving actionable HR insights for decision-making

# Conclusion

This HR Analytics dashboard provides a comprehensive view of employee attrition and workforce composition.
It empowers HR teams to make data-driven decisions to improve retention, enhance job satisfaction, and optimise recruitment strategies.
