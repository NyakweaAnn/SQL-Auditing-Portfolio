📊 🌾 AFC Loan Portfolio Audit: Relational Database & SQL Analytics
🌟 About This Project
I am currently learning SQL to combine my interest in finance with data skills. Since I've worked at the Agricultural Finance Corporation (AFC), I decided to use a "Farmer & Loan" scenario to practice my first database queries.

✍️ What I Did (Step-by-Step)
1. Creating the Tables
I started by building two tables from scratch.

A Farmers table for names and locations.

A Loans table to track money and status.

2. My First "Join" Query
The biggest thing I learned was how to connect two different tables using a shared ID. This query looks for farmers in Uasin Gishu who have already received their money (Disbursed).

SQL
SELECT Farmers.Full_Name, Farmers.County, Loans.Approved_Amount, Loans.Status
FROM Farmers
JOIN Loans 
  ON Farmers.Farmer_ID = Loans.Farmer_ID
WHERE Farmers.County = 'Uasin Gishu'
  AND Loans.Status = 'Disbursed';
3. Learning "Math" in SQL
I also practiced how to calculate totals. Instead of looking at every person, I wanted to see the Total Sum of all loans for each county.

I used SUM to add up the money.

I used GROUP BY to organize it by County.

📖 Key Takeaways
Primary Keys: I learned that every farmer needs a unique ID number so the computer doesn't get confused.

Filtering: Using WHERE helps me find exactly what I need without looking at thousands of rows.

Accuracy: I realized that one tiny typo in a command (like a missing comma) can stop the whole thing from working!
