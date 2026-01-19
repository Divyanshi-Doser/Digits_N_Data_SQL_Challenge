# 🛰️ Mission 4: Trace the Black Market Flow  
## Six Weeks to Save Reality — SQL Investigation Project

## 📌 Project Overview
This project is a **SQL-based investigative analysis** created as part of the  
**Six Weeks to Save Reality** challenge by **Digits n Data**.

Mission 4 simulates a high-stakes financial intelligence operation where SQL is used
to uncover **hidden transaction patterns** behind legitimate-looking accounts.
The focus is on **data-driven reasoning, temporal filtering, and aggregation logic**.

---

## 🎯 Mission Objective
The objective of this mission is to:

- Trace suspicious transfers originating from **Stark QUANTUM_FLOW accounts**
- Analyze transaction activity within the **last 7 days**
- Identify the **account holder who received the largest total transfer**
- Reveal potential involvement in an underground black market operation

---

## 🗂️ Data Sources

### 1️⃣ Account_Holders
| Column | Description |
|------|------------|
| AccountID | Unique account identifier |
| HolderName | Name of the account holder |
| ContactEmail | Registered email address |

### 2️⃣ Stark_Transactions
| Column | Description |
|------|------------|
| TransactionID | Unique transaction identifier |
| SenderAccount | Sending account ID |
| ReceiverAccount | Receiving account ID |
| Amount | Transfer amount |
| TransactionType | Type of transaction |
| TransactionDate | Date of transaction |

---

## 🧠 Investigation Approach

### 1️⃣ Identify the Source Accounts
The investigation begins by isolating all accounts associated with  
**`QUANTUM_FLOW`**, which act as the suspected source of illicit transfers.

### 2️⃣ Determine the Anchor Date
Instead of using hard-coded dates, the **maximum transaction date** is identified.
This ensures the analysis dynamically adapts to the most recent data available.

### 3️⃣ Apply the 7-Day Time Window
A rolling **7-day window** is constructed backward from the maximum transaction date,
capturing only recent and relevant activity.

### 4️⃣ Filter Relevant Transactions
Only transactions:
- Sent from QUANTUM_FLOW accounts  
- Occurring within the defined 7-day window  

are included in the analysis.

### 5️⃣ Aggregate Transfer Amounts
Transactions are grouped by **receiver account**, and total amounts received are
calculated to detect abnormal inflows.

### 6️⃣ Rank to Reveal the Target
Results are ordered in descending order of total received amount to identify the
top recipient and potential black market endpoint.

---

## 🧾 SQL Techniques Used
- Common Table Expressions (CTEs)
- INNER JOINs
- Subqueries
- Date arithmetic (SQLite)
- Aggregation using SUM
- Sorting and limiting results

This mission emphasizes **logical sequencing and temporal accuracy** in SQL analysis.

---

## ✅ Final Outcome
The investigation successfully identifies **Vision AI Research** as the account
holder who received the **largest total transfer** from QUANTUM_FLOW accounts
within the last 7 days.

This confirms a significant concentration of funds and raises further questions
about the true nature of these transfers.

---

## 🎥 Video Presentation
A cinematic **video walkthrough** explaining the storyline, SQL logic, and
investigation flow has been shared on LinkedIn.

🔗 **LinkedIn Video Link:**  
 [LinkedIn Post]( https://www.linkedin.com/posts/divyanshi-doser_sql-dataanalytics-learninginpublic-activity-7412785747218563072-oox8?utm_source=share&utm_medium=member_android&rcm=ACoAAFn4nbMBzA70MeO-p2EjHsa7DB-bJ35X5lE )

---

## 🚀 Key Takeaway
> In SQL investigations,  
> **how you define time** can change **what the data reveals**.

---

## 👤 Author
**Divyanshi Doser**  
SQL • Data Analytics • Story-Based Learning  
Digits n Data — Six Weeks to Save Reality

