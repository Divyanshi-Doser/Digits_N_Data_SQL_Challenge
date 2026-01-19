# 🛰️ Mission 6: Chaos and The Final Jump
## Six Weeks to Save Reality — SQL Investigation Project

---

## 📌 Project Overview
Mission 6 is a **SQL-based temporal analysis challenge** conducted as part of the  
**Six Weeks to Save Reality** series by **Digits n Data**.

In this mission, the timeline is fractured and multiple paradoxes appear.  
The objective is to determine the **earliest point in time on a Saturday** where a paradox occurs,  
and retrieve its **ParadoxScore**.  

This scenario simulates **time-travel analysis under high-stakes conditions**,  
requiring precise filtering, ordering, and selection of temporal events.

---

## 🎯 Mission Objective
The objective of this mission is to:

- Analyze the **Timeline_Paradox_Simulation** table  
- Identify the **earliest timestamp that falls on a Saturday**  
- Retrieve the **ParadoxScore** associated with that timestamp  

This value serves as the **mission password** and is crucial to “making the jump count” in the storyline.

---

## 🗂️ Data Source

### 📋 Timeline_Paradox_Simulation
| Column        | Description                               |
|---------------|-------------------------------------------|
| SimID         | Unique simulation identifier              |
| Timestamp     | Date and time of the simulated event     |
| DayOfWeek     | Day of the week corresponding to the timestamp |
| ParadoxScore  | Numerical score representing the paradox |

---

## 🧠 Investigation Approach

### 1️⃣ Filter by Day
First, filter the dataset to include only events where `DayOfWeek = 'Saturday'`.  
This isolates potential jump points in the timeline.

### 2️⃣ Order by Timestamp
Order the filtered rows in **ascending order by Timestamp** to identify the earliest event.

### 3️⃣ Select the ParadoxScore
Retrieve the **ParadoxScore** corresponding to the earliest Saturday timestamp.  
This avoids potential duplicates or ambiguities in case multiple events occur on the same day.

### 4️⃣ Handle Duplicates (if any)
If multiple rows have the same earliest timestamp, select one based on **SimID ascending** to maintain consistency.

---

## 🧾 SQL Techniques Used
- Filtering with `WHERE`  
- Ordering with `ORDER BY Timestamp ASC`  
- Limiting results with `LIMIT 1`  
- Handling duplicates with secondary ordering (SimID)  
- Temporal analysis on datetime columns  

This mission emphasizes **date filtering, ordering, and precise selection** in SQL.

---

## ✅ Final Outcome
The investigation identifies the **earliest Saturday timestamp** and its **ParadoxScore**:

**🕒 Timestamp:** 2024-12-28 09:00:00  
**🎯 ParadoxScore:** 30

This confirms the optimal point to make the “final jump” with **minimal timeline paradoxes**.

---

## 🧠 Key Learning
- Filtering by **day of the week** is crucial in temporal datasets  
- Ordering ensures the **earliest occurrence** is selected  
- SQL allows precise isolation of critical events even in chaotic datasets  

> *In time-travel analysis, the first move can determine the fate of reality.*

---

## 🎥 Presentation & Sharing
A cinematic **walkthrough** explaining the storyline, SQL logic, and timeline analysis has been shared on LinkedIn as part of the challenge.

🔗 **LinkedIn Post Link:**  
 [LinkedIn Post](https://www.linkedin.com/posts/divyanshi-doser_dnd-challenge-mission-6-activity-7418649834682859520-xTqC?utm_source=share&utm_medium=member_android&rcm=ACoAAFn4nbMBzA70MeO-p2EjHsa7DB-bJ35X5lE)

