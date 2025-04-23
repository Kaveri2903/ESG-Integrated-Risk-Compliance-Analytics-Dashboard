# ESG-Integrated-Risk-Compliance-Analytics-Dashboard For Financial Institutions

![ESG main Dashboard](https://github.com/user-attachments/assets/4767391e-0ae6-4d6e-ad88-3470e260dde2)

This project is a comprehensive **Power BI dashboard** designed to analyze and visualize **risk metrics**, **ESG compliance**, and **regulatory status** across multiple financial institutions. It is inspired by real-world consulting scenarios in the **banking sector**, particularly aligned with roles in Risk, Governance, and Regulatory Advisory.

---

## 📊 Project Overview

The dashboard enables:
- Insightful tracking of **compliance status** and **Value at Risk**
- ESG score analysis per bank
- Time-based trends for risk categories
- Visual flagging of **High vs. Normal risk levels**
- Interactive exploration using slicers for CompanyID, Risk Category, Compliance Status, and Date

---

## 🛠 Tools & Technologies
- **Power BI Desktop**
- **DAX** for measures and calculated columns
- **CSV data transformation** and cleansing
- Optional use of **Power Query** for advanced shaping

---

## 🧠 Key Features

| Feature | Description |
|--------|-------------|
| 🔍 **Compliance Insights** | Track number of days banks are under review |
| 📈 **Rolling Averages** | 30-day rolling averages for key risk indicators |
| ⚠️ **High Risk Flag** | Automatically classify banks with high Value_at_Risk |
| 🗓 **Time Aggregation** | Aggregate by month, quarter, and year |
| 🔄 **Interactive Slicers** | Filter by CompanyID, Risk Category, Compliance Status, and Date |
| 📊 **Custom Visuals** | Pie charts, bar graphs, line charts, and KPI cards |

---

## 📐 DAX Formulas Used

### ✅ Under Review Days (Measure)
```dax
Under_Review_Days = 
CALCULATE(
    COUNTROWS(complete_bank_risk_data_1),
    complete_bank_risk_data_1[Compliance_Status] = "Under Review"
)

High_Risk_Flag = 
IF(complete_bank_risk_data_1[Value_at_Risk] > 1000000, "High", "Normal")


Rolling_Avg_30D = 
AVERAGEX(
    DATESINPERIOD('Date'[Date], MAX('Date'[Date]), -30, DAY),
    CALCULATE(SUM(complete_bank_risk_data_1[Value_at_Risk]))
)


Avg_ESG_Score = 
AVERAGEX(
    VALUES(complete_bank_risk_data_1[CompanyID]),
    CALCULATE(AVERAGE(complete_bank_risk_data_1[ESG_Score]))
)
```

📁 PowerBI_Bank_Risk_Project
│
├── 📊 Dashboard.pbix         
├── 📄 complete_bank_risk_data_1.csv
├── 📝 README.md
└── 📚 Screenshots/   

![ESG main Dashboard](https://github.com/user-attachments/assets/df27bf07-bdaf-4503-9750-f391dcc21942)

![ESG 1](https://github.com/user-attachments/assets/0c9dd364-154a-4ac5-93a7-208664b2aaf1)

![ESG 2](https://github.com/user-attachments/assets/30f0d92f-103f-4b25-8a5e-705ed7ea3e8f)

![image](https://github.com/user-attachments/assets/ad77e20f-c4a3-4e4c-a5b3-7aded65738bd)




---

## 🔍 Example Use Cases

- Regulatory reporting and audits
- ESG integration analysis in risk frameworks
- Client portfolio compliance tracking
- Presentation to stakeholders on institutional risk levels

---

## 🚀 Getting Started

1. Download and open the `Dashboard.pbix` file in Power BI Desktop
2. Load the provided CSV file if not already embedded
3. Refresh data, and interact using slicers and filters
4. Customize measures or thresholds as needed

---

## ✨ Outcome

This dashboard showcases my ability to:
- Build **business-ready analytical tools**
- Translate complex regulatory concepts into actionable insights
- Use **DAX**, **data modeling**, and **Power BI** visuals effectively

---

## 📬 Contact

Created by Kaveri Gadhe
📧 kaverigadhe43@gmail.com  

---



