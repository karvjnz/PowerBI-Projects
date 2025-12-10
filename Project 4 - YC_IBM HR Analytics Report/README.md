
<h1>📊 Power BI Dashboard – IBM HR Analytics Employee Attrition & Performance</h1>

A comprehensive HR analytics solution built in Power BI, designed to uncover insights on employee attrition, performance trends, satisfaction levels, and workforce demographics.
This project transforms raw HR data into a powerful decision-support tool for HR teams and business leaders.

<h2>📁 Table of Contents</h2>

1. 📌 Project Overview
2. 📊 Key Features
3. 🧩 Power BI Components Used
4. 🔢 DAX Measures
5. 📈 Insights & Outcomes
6. 🎯 Conclusion

**🔍 Project Overview**

This Power BI report analyzes workforce data from the IBM HR Analytics Employee Attrition & Performance dataset.
The dashboard provides clear visibility into attrition drivers, employee satisfaction levels, performance patterns, and demographic insights—helping organizations make data-driven HR decisions.

**📊 Key Features**

1️⃣ Employee Attrition Analysis

1. Attrition by Age Group, Department, Job Role, Education, and Marital Status
2. KPI-based attrition rate measurement
3. Trend analysis on Work-Life Balance, Years at Company, and attrition

**2️⃣ Performance & Satisfaction Insights**

1. In-depth analysis of Job Satisfaction, Environment Satisfaction, and Performance Ratings
2. Comparison of high performers vs employees at risk of attrition
3. Scatterplots highlighting correlation between Monthly Income and Performance

**3️⃣ Workforce Demographics**

1. Gender, age bands, education fields, and department distributions
2. Key metrics including Average Monthly Income, Average Tenure, and Promotion Gap

**4️⃣ HR KPIs & Metrics**

1. Attrition Rate
2. Average Salary
3. Tenure & Years with Current Manager
4. Overtime impact on attrition
5. Travel frequency vs job satisfaction

🧩 Power BI Components Used

✔ Slicers  
✔ Visuals  
✔ Data Modeling  

Designed using a clean star schema with a FactEmployee table and supporting dimensions
Managed relationships between demographic, satisfaction, and performance data

**Data cleaning via Power Query:**
1. Duplicate removal
2. Standardized text formatting
3. Data type corrections
4. Custom calculated columns (age bands, tenure groups, etc.)

**🔢 DAX Measures**

Below are key DAX calculations used in the dashboard:

Attrition Rate =
DIVIDE(
    CALCULATE(COUNTROWS(Employees), Employees[Attrition] = "Yes"),
    COUNTROWS(Employees)
)

Average Monthly Income =
AVERAGE(Employees[MonthlyIncome])

Tenure Band =
SWITCH(
    TRUE(),
    Employees[YearsAtCompany] <= 2, "New (0-2 Years)",
    Employees[YearsAtCompany] <= 5, "Mid (3-5 Years)",
    Employees[YearsAtCompany] <= 10, "Senior (6-10 Years)",
    "Veteran (10+ Years)"
)

Overtime Attrition =
CALCULATE(
    [Attrition Rate],
    Employees[OverTime] = "Yes"
)

High Performer Flag =
IF(
    Employees[PerformanceRating] >= 4,
    "High Performer",
    "Standard"
)

**📈 Insights & Outcomes**
1. Young employees (25–35) show the highest attrition rate, especially in Sales and R&D.
2. Employees doing overtime are nearly 2× more likely to leave than others.
3. Highest attrition roles include Sales Executives, Laboratory Technicians, and HR.
4. Lower Environment Satisfaction strongly correlates with higher attrition.
5. Higher Monthly Income is associated with higher job satisfaction and lower attrition risk.

**🎯 Conclusion**

🔹 This Power BI HR Analytics Dashboard transforms raw employee data into actionable, strategic insights, empowering HR teams to:
🔹 Identify attrition risks proactively
🔹 Improve employee satisfaction
🔹 Shape effective retention strategies
🔹 Strengthen workforce planning and decision-making


**📬 Contact:**
If you would like to discuss this project, collaborate, or explore more dashboards:

👤 Name: Karthik Manoharan  
📧 Email: karvjnz@gmail.com  
🔗 LinkedIn: www.linkedin.com/in/karvj
