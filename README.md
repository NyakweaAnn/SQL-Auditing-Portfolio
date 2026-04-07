# 🌾 AFC Loan Portfolio: My SQL Learning Journey

[![SQL](https://img.shields.io/badge/Skill-SQL-blue.svg)]()
[![Database](https://img.shields.io/badge/Database-MySQL-orange.svg)]()
[![Project-Status](https://img.shields.io/badge/Status-Learning_In_Progress-green.svg)]()

## 📌 Project Overview
I am currently bridging the gap between my finance background and data analytics. This project is a practical simulation of an internal audit at the **Agricultural Finance Corporation (AFC)**. 

I built a relational database from scratch to practice how a real institution manages farmer data and loan disbursements.

---

## 🛠️ What I Built (Step-by-Step)

### **1. The Database Foundation**
I designed two tables to keep the data organized. This is called **Data Normalization**—making sure every piece of info has its own home.
* **Farmers Table:** Contains personal details and location (County).
* **Loans Table:** Tracks the financial side (Amount and Status).

### **2. The "Bridge" (SQL JOIN)**
My biggest milestone was learning how to link these tables together. I wrote a query to find exactly who in **Uasin Gishu** had already received their funds.

```sql
SELECT Farmers.Full_Name, Farmers.County, Loans.Approved_Amount, Loans.Status
FROM Farmers
JOIN Loans 
  ON Farmers.Farmer_ID = Loans.Farmer_ID
### **3. The Financial Summary (Aggregations)**
I practiced acting like an auditor by calculating the **Total Cash Flow** per region. I used:
* **SUM**: To add up the loan values and assess total financial exposure.
* **GROUP BY**: To segment the totals for each individual County, allowing for regional comparisons.

---

## 📖 Key Takeaways & Lessons
* ✅ **Primary Keys are Essential:** I learned that without unique IDs, data relationships break and the system gets messy fast.
* ✅ **Filtering for Accuracy:** The `WHERE` clause is my best friend for isolating "Pending" vs "Disbursed" accounts during an audit.
* ✅ **Logical Thinking:** SQL is like a puzzle—you have to tell the computer exactly where to look, what to join, and how to filter.

---

## 🚀 Future Goals
* [ ] Connect this MySQL database to **Power BI** for live dashboarding and charts.
* [ ] Practice **"Data Cleaning"** queries to handle missing values or duplicate entries.

---

## 📊 Final Audit Results
Below is the successful output of my audit query showing the active disbursements in **Uasin Gishu**:

![Audit Results](audit_results_screenshot.png)
WHERE Farmers.County = 'Uasin Gishu'
  AND Loans.Status = 'Disbursed';
