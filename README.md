# 📊 Call Center Performance Dashboard (Power BI)

### 🎯 Project Objective

To analyze the performance and efficiency of a customer support team by evaluating ticket volume, resolution speed, SLA compliance, and customer satisfaction. The goal is to identify operational bottlenecks and trends affecting the customer experience.

---

### 👁️ Dashboard Preview

#### Page 1: Trends
This page gives a high-level overview of the key performance indicators (KPIs) and general trends.

![Trends Dashboard](Call%20centre%20data%20analysis/Trends_dashboard.png)

#### Page 2: Diagnostic Analysis
This page drills down into agent-specific performance and correlates different metrics to find insights.

![Diagnostic Analysis Dashboard](Call%20centre%20data%20analysis/Diagnostic_questions.png)

---

### 🗃️ Data Source

The dataset for this project is a Microsoft Excel file (`01 Call-Center-Dataset.xlsx`), originally sourced from Kaggle.

---

### ⚙️ Process

1.  **Data Cleaning & Transformation (Power Query):**
    * Connected to the raw Excel file and performed data cleaning operations.
    * Handled missing values, corrected data types, and created new conditional columns for analysis (e.g., "SLA Breaches").

2.  **Data Modeling:**
    * Built a relational model within Power BI to connect data tables.
    * Established relationships to enable cross-filtering and complex analysis between agents, tickets, and time.

3.  **DAX Calculations:**
    * Wrote DAX measures to calculate key performance indicators (KPIs) not present in the original data, including:
        * Total Contacts & Unresolved Contacts
        * Average Call Handling Time (CHT) in minutes
        * Average Response Time in seconds
        * Average Customer Satisfaction Rating (max 5)
        * Missed Call Rate (%)

4.  **Dashboard Design:**
    * Designed the multi-page interactive dashboard shown in the preview above.

---

### 💡 Key Questions & Insights

#### 1. Descriptive Analysis (Trends)

* **What is the overall performance?**
    * **Total Contacts:** 5K
    * **Avg. CHT:** 2.93 minutes
    * **Avg. Response Time:** 54.75 seconds
    * **Avg. Satisfaction:** 2.76 / 5
    * **Unresolved Contacts:** 1K (20%)
    * **Missed Call Rate:** 18.92%

* **Who is handling the workload?**
    * Workload is fairly evenly distributed among all agents (Jim, Martha, Dan, Diane, Becky, Greg, Joe, Stewart).

* **What are the main issues?**
    * The top concerns are **"Streaming," "Technical Support,"** and **"Payment Related."**

* **When are we busiest?**
    * The vast majority of contacts occurred in **January**, with a sharp drop-off in February and March.

#### 2. Diagnostic Analysis (Insights)

* **Is there a connection between call handling time (CHT) and customer satisfaction?**
    * Yes, there is a slight **negative correlation**. As CHT increases, average satisfaction tends to decrease.

* **When do most missed calls occur?**
    * Missed calls spike significantly between **1:30 PM (13:30) and 3:00 PM (15:00)**.

* **How does agent performance vary?**
    * **Dan** has the highest average satisfaction rating (approx. 2.85).
    * **Joe** has the lowest average satisfaction rating (approx. 2.7). This suggests performance is agent-dependent, not just a factor of time.

* **What is the relationship between resolved tickets and satisfaction?**
    * For all agents, satisfaction ratings of 3, 4, and 5 are almost **100% "Resolved contacts."**
    * This indicates a strong, direct link: **resolving a customer's issue is the single most important factor in achieving a high satisfaction score.**
