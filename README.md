# Financial Dashboard Project Report 📊
A dynamic Power BI financial dashboard providing real-time insights on income, expenses, savings, and growth trends, empowering users to make data-driven financial decisions.
#### [Click here](https://app.powerbi.com/view?r=eyJrIjoiMTFiM2ViMTMtNzNmZi00YzNjLWFlNDgtMWQ2OGUxMjBjMjU2IiwidCI6IjcyZjJhZDk4LWM0OWMtNDBjOC1hYmFmLWQ5ZWMwZmVmMmJjMSIsImMiOjF9) for live demo of the Dashboard.

## Overview of Dashboard
![thumbnail ](https://github.com/user-attachments/assets/d367e6d7-56d7-4625-a63e-6cb183af02e5)


## Introduction 🌟  
The *Financial Dashboard* project is a robust and dynamic solution for analyzing key financial metrics such as income, savings, expenses, and financial growth trends over time. Built using *Power BI*, the dashboard is designed to offer real-time insights, interactive visualizations, and intuitive controls, enabling users to make well-informed financial decisions. This project addresses the common challenges of managing finances using static methods like spreadsheets and demonstrates the power of visual analytics in simplifying complex data.

---

## Problem Statement ⚠  
Traditional methods of tracking finances, such as spreadsheets, often lack interactivity, real-time insights, and advanced analytical capabilities. Users struggle to analyze trends, evaluate financial health, or gain actionable insights efficiently. This project aims to overcome these challenges by creating a highly interactive financial dashboard in *Power BI*.

---

## Project Objectives 🎯  
- Develop an interactive and dynamic financial dashboard to track income, expenses, savings, and targets over time.  
- Provide advanced visualizations and filtering options for granular analysis.  
- Enable financial trend analysis with monthly growth metrics.  
- Offer actionable insights to improve financial decision-making and efficiency.

---

## Key Features 🌟  
1. *Dynamic Visualizations*:  
   - Line charts, donut charts, matrices, and KPI cards present financial data clearly and interactively.  
2. *Monthly Growth Analysis*:  
   - Tracks the growth of income, savings, and expenses on a monthly basis.  
3. *Expense-to-Savings Ratio*:  
   - Provides a key metric for evaluating financial efficiency.  
4. *Interactive Filtering*:  
   - Allows slicing and dicing data by year, month, or category for focused analysis.  
5. *Dynamic Titles*:  
   - Line chart titles change based on slicer selections, improving user engagement.

---

## How the Dashboard Was Created 🛠  

### Data Collection 📅  
The dataset comprised income, expenses, savings, and targets recorded over different dates. Initially, dates were represented as columns, making it difficult to analyze trends.

#### Data Transformation Steps:  
1. *Unpivoted Columns*:  
   - Converted date columns into rows using *Power BI’s unpivot feature* for better row-wise analysis.  
2. *Created Calculated Columns*:  
   - *Year*:
     ```DAX
     Year = FORMAT('Dataset'[Date],"yyyy")
       
   - *Month-Year*:  
     ```DAX
     Month-Yr = FORMAT('Dataset'[Date],"mmm-yy")  
     
---

### Visualizations 📈  
1. *Line Chart*:  
   - Tracks trends in expense percentages, savings percentages, and targets over time.  
2. *Donut Charts*:  
   - Displays proportions of savings and expenses for quick insights.  
3. *Matrix Table*:  
   - Categorizes data by year and type, providing detailed breakdowns.  
4. *KPI Cards*:  
   - Summarizes metrics such as total income, total expenses, total savings, and expense-to-savings ratio.  
5. *Dynamic Slicers*:  
   - Users can filter data by year or specific categories, enhancing interactivity.
  
#### Dashboard Visualization Progress
  ##### Before Visual Enhancements
  This screenshot shows the initial version of the dashboard before any visual edits or optimizations.
  ![Screenshot 2024-11-12 113313](https://github.com/user-attachments/assets/84e158bb-f467-4600-b6be-c5ac5b628b40)

  

 ##### After Visual Enhancements
 This screenshot demonstrates the final version of the dashboard, reflecting the visual improvements and design changes.
  ![Screenshot 2024-11-17 225912](https://github.com/user-attachments/assets/20f436e4-71f9-42cc-96ce-ebd0d1edbf98)

  


---

### Insights Derived 💡  
1. *Savings Trends*:  
   - Identified months with higher savings, enabling better financial planning.  
2. *Expense Monitoring*:  
   - Highlighted months with expense spikes, helping users address potential overspending.  
3. *Income Growth*:  
   - Revealed trends in income growth over time, aiding long-term planning.  
4. *Efficiency Insights*:  
   - Provided actionable insights into financial efficiency through the expense-to-savings ratio.

---

### Importance of Insights 🔑  
1. *Informed Decision-Making*:  
   - Empowers users to make data-driven financial choices.  
2. *Resource Optimization*:  
   - Helps identify areas for budget adjustments.  
3. *Goal Setting*:  
   - Facilitates realistic goal-setting and long-term financial planning.  
4. *Efficiency Improvement*:  
   - Encourages better savings habits while managing expenses effectively.

---

## Key Metrics 📊  
1. *Total Income*:  
   ```DAX
   Total_Income = CALCULATE(SUM('Dataset'[Amount]), 'Dataset'[Type] = "Income")  
2. *Total Expenses*:  
   ```DAX
   Total_Expenses = CALCULATE(SUM('Dataset'[Amount]), 'Dataset'[Type] = "Expense")  
3. *Total Savings*:  
   ```DAX
   Total_Savings = [Total_Income] - [Total_Expenses]  
4. *Savings Percentage*:  
   ```DAX
   Savings% = DIVIDE([Total_Savings], [Total_Income])  
5. *Monthly Growth*:  
   ```DAX
   CY_Monthly_Sale = CALCULATE([Total_Income], 'Dataset'[Month-Yr] = MAX('Dataset'[Month-Yr]))
   PY_Monthly_Sale = 
   VAR PY_Month = PREVIOUSMONTH('Dataset'[Date])
   RETURN CALCULATE([Total_Income], 'Dataset'[Date] = PY_Month)

   Monthly_Growth = DIVIDE([CY_Monthly_Sale] - [PY_Monthly_Sale], [PY_Monthly_Sale])  
6. *Expense-to-Savings Ratio*:  
   ```DAX
   Exp_vs_Sav = DIVIDE([Total_Expenses], [Total_Savings])
   
---

## Project Outcomes 🎉  
- Created a comprehensive and interactive financial dashboard using *Power BI*.  
- Simplified complex datasets for better financial insights and trend analysis.  
- Empowered users to make data-driven decisions through dynamic filtering and visualizations.  
- Provided actionable insights for improving financial efficiency and achieving long-term goals.

---
