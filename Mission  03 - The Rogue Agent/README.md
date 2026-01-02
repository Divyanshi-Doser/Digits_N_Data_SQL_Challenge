# 🛰️ Mission 3: The Rogue Agent  
## Six Weeks to Save Reality — SQL Investigation Project

## 📌 Project Overview
This project is a **SQL-based investigative analysis** designed as part of the  
**Six Weeks to Save Reality** challenge by **Digits n Data**.

The mission simulates a real-world security breach investigation where SQL is used
to identify an **internal threat** through structured data analysis, logical filtering,
and aggregation.

---

## 🎯 Mission Objective
The objective of this mission is to:

- Identify the **Security Officer** responsible for suspicious activity
- Detect who performed the **highest number of Security Sensor Overrides**
- Ensure all actions occurred **within 48 hours of Captain Marvel’s return**
- Reveal the **rogue agent** using data-driven evidence

---

## 🗂️ Data Sources

### 1️⃣ Compound_Personnel
| Column | Description |
|------|------------|
| PersonnelID | Unique identifier |
| Name | Officer’s full name |
| Role | Assigned role |
| Email | Contact email |

### 2️⃣ Security_Logs
| Column | Description |
|------|------------|
| LogID | Log identifier |
| PersonnelID | Officer reference |
| Action | Recorded activity |
| Timestamp | Date & time |

---

## 🧠 Investigation Approach

### 1️⃣ Identify the Anchor Event
The investigation begins by identifying the exact timestamp when  
**Captain Marvel returned to the compound**.  
This acts as the reference point for the entire analysis.

### 2️⃣ Apply the Time Window
A strict **48-hour window** is enforced starting from the return timestamp to ensure
only relevant post-event activity is considered.

### 3️⃣ Filter Suspicious Actions
Only log entries with the action  
**`Security Sensor Override`** are selected, as these indicate potential tampering.

### 4️⃣ Restrict to Internal Access
Logs are joined with personnel data and filtered to include only  
**Security Officers**, eliminating unrelated roles.

### 5️⃣ Aggregate Activity
Override actions are grouped by individual officers and counted to identify
unusual patterns.

### 6️⃣ Rank to Reveal the Threat
Results are sorted in descending order of override count to expose the
officer with the highest number of violations.

---

## 🧾 SQL Techniques Used
- Common Table Expressions (CTEs)
- INNER JOINs
- Datetime filtering
- Aggregation using COUNT
- Sorting and limiting results

This project focuses on **SQL logic and reasoning**, not just syntax.

---

## ✅ Final Outcome
The analysis successfully identifies a single **Security Officer** responsible for
the maximum number of unauthorized overrides, confirming the presence of an
internal security breach.

---

## 🎥 Video Presentation
A detailed **video presentation** explaining the storyline, SQL logic, and
step-by-step investigation has been shared on LinkedIn.

🔗 **LinkedIn Video Link:**  
( https://www.linkedin.com/posts/divyanshi-doser_sql-dataanalytics-learninginpublic-activity-7410278753949417472-IbrV?utm_source=share&utm_medium=member_android&rcm=ACoAAFn4nbMBzA70MeO-p2EjHsa7DB-bJ35X5lE )

---

## 🚀 Key Takeaway
> SQL is not about writing queries —  
> it’s about asking the right questions in the right order.

---

## 👤 Author
**Divyanshi Doser**  
SQL • Data Analytics • Story-Based Learning  
Digits n Data — Six Weeks to Save Reality

