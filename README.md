# project-management-dashboard
Power BI project management dashboard tracking tasks, employee performance, project progress, and resource allocation.
# 📊 Project Management Dashboard  

This repository contains a **Power BI dashboard** designed to monitor and analyze project performance. It provides insights into **tasks, employees, project progress, and overall resource allocation** to support effective project management.  

---

## 🔍 Project Overview  

The dashboard includes:  
- 📌 **Task Progress** – visual breakdown of tasks completed vs. pending.  
- 👥 **Employee Tracking** – number of employees and individual employee progress.  
- 📂 **Project Tracking** – number of projects, distribution across departments, and days required.  
- 📈 **Performance Metrics** – KPIs showing progress across teams.  

---

## 📂 Repository Contents  

- `project_data.csv` → dataset used (or placeholder/sample if dataset is private).  
- `images/dashboard_preview.png` → dashboard preview screenshot.

---  
-  **DAX calculations** 
-- Average Salary
Average Salary = AVERAGE('Survey Data'[Salary])

-- Count of Respondents
Respondent Count = COUNTROWS('Survey Data')

-- Percentage Using Python
Python Users % =
DIVIDE(
    CALCULATE(COUNTROWS('Survey Data'), 'Survey Data'[Language] = "Python"),
    [Respondent Count],
    0
)

-- Satisfaction Score (Weighted Average)
Satisfaction Score =
DIVIDE(
    SUMX('Survey Data', 'Survey Data'[Satisfaction] * 'Survey Data'[Weight]),
    SUM('Survey Data'[Weight]),
    0
)

-- Salary by Gender Gap
Gender Salary Gap =
CALCULATE(AVERAGE('Survey Data'[Salary]), 'Survey Data'[Gender] = "Male")
 - 
CALCULATE(AVERAGE('Survey Data'[Salary]), 'Survey Data'[Gender] = "Female")


---

## 🛠️ Tools & Technologies  

- **Power BI Desktop** – for dashboard development.  
- **Power Query** – for data cleaning and transformation.  
- **Data Visualization** – bar charts, pie charts, and KPIs to track project status.  

---

## 🚀 Key Insights  

- Dashboard tracks **42 employees** across **15 projects**.  
- Total **1218 days required** for project completion.  
- Provides visibility on **task-level completion rates** (e.g., Bug Fixes, Content Creation, Prototype).  
- Employee progress breakdown helps identify **top performers and resource gaps**.  
- Project distribution shows workload across departments like Engineering, Operations, Development, and Sales.  

---

## 📌 How to Use  

1. Clone this repository.  
2. Open `Project_Management_Dashboard.pbix` in **Power BI Desktop**.  
3. Load the dataset (if not already connected).  
4. Explore the interactive dashboard.  

---

## 🎯 Purpose  

This project demonstrates skills in:  
- Project tracking and reporting with **Power BI**.  
- Monitoring **employee performance and project timelines**.  
- Building **interactive dashboards** for project management use cases.  

---  

✨ If you like this project, feel free to **star ⭐ the repository** and connect with me!  
