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
WHERE Farmers.County = 'Uasin Gishu'
  AND Loans.Status = 'Disbursed';
