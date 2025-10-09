# Storytelling Insights Dashboard (CEO-Level Report)

📅 **Project Date:** 2025  
🛠️ **Tool:** Power BI  

---

## 🎯 Objective
To create a **one-page executive storytelling dashboard** that delivers *actionable insights at a glance*.  
The goal is to communicate key business metrics and trends through minimal visuals, intuitive layout, and clean design — perfect for management reviews.

---

## 🧩 Key Highlights
- 🧠 **Storytelling Focus:** Structured flow from KPIs → Trends → Insights  
- 💼 **CEO-Friendly View:** Combines performance, contribution, and growth in one page  
- 📈 **Dynamic KPI Cards:** Sales, Profit, Growth %, and YoY trend indicators  
- 🧭 **Insight Sections:** Highlights key takeaways in plain language  
- 🎨 **Design:** Balanced light theme with clear hierarchy and visual breathing space  

---

## ⚙️ Power BI Concepts Used
- DAX measures for KPI and trend logic  
- Conditional formatting for highlight insights  
- Dynamic titles and explanations  
- Layout alignment and spacing for readability  
- Data storytelling with context and visual flow  

---

## 🧠 Sample DAX Used

Total Sales = SUM(Sales[Amount])

YoY Sales Growth % =
VAR CurrSales = [Total Sales]
VAR PrevSales =
    CALCULATE(
        [Total Sales],
        SAMEPERIODLASTYEAR('Calendar'[Date])
    )
RETURN
DIVIDE(CurrSales - PrevSales, PrevSales)

Top Region =
TOPN(
    1,
    SUMMARIZE(Sales, Sales[Region], "TotalSales", [Total Sales]),
    [TotalSales], DESC
)


## Preview

By Customer Level

![Customer](Customer.png)

By Finance Level

![Finance](Finance.png)
