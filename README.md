# 👥 HR Analytics Dashboard (Power BI Project)

An interactive **Power BI Dashboard** designed to analyze **employee attrition**, **demographics**, and **HR trends** across multiple departments.  
This project helps HR managers and leadership teams identify retention challenges, monitor workforce dynamics, and support data-driven decision-making.

---

## 📊 Dashboard Preview

### Page 1 – HR Overview
![HR Analytics Dashboard Page 1](../Documentation/HR_Analytics_Project.jpg)

### Page 2 – Attrition Insights
![HR Analytics Dashboard Page 2](../Documentation/HR_Analytics_Project2.jpg)

---

## 🎯 Project Objectives
- Analyze overall workforce metrics (Total Employees, Attrition Rate, Average Age).  
- Understand employee attrition by **department**, **education**, **age**, and **job role**.  
- Evaluate the influence of **salary hike**, **job satisfaction**, and **work-life balance** on attrition.  
- Provide management a clear, data-driven view of workforce trends.

---

## ⚙️ Tools & Skills Used

| Category | Details |
|-----------|----------|
| **Data Source** | CSV / Excel (HR Employee Data) |
| **Tools** | Microsoft Power BI Desktop |
| **Techniques** | Power Query for ETL, DAX Calculations, Data Modeling |
| **Visualization Types** | KPI Cards, Bar Chart, Donut Chart, TreeMap, Table, Line Chart |

---

## 🧩 Data Model
**Tables:**
- `EmployeeData` — Employee demographics and metrics  
- `Department` — Department-wise data  
- `Education` — Education categories  
- `JobRole` — Role and satisfaction-related data  

Relationships created on:
- `EmployeeData[Department]` → `Department[Department]`  
- `EmployeeData[Education]` → `Education[Education]`

---

## 🧮 DAX Measures (Key Metrics)

```DAX
Total Employees = COUNT(EmployeeData[EmployeeID])

Attrition Count = 
CALCULATE(
    COUNT(EmployeeData[EmployeeID]),
    EmployeeData[Attrition] = "Yes"
)

Active Employees = 
[Total Employees] - [Attrition Count]

Attrition Rate % =
DIVIDE([Attrition Count], [Total Employees]) * 100

Average Age = AVERAGE(EmployeeData[A]()

🧑‍💻 Author

Dinakar Shetty
Business & Data Analyst | Power BI | SQL | Excel | Python
📧 Email: dinakar.shetty2@gmail.com
