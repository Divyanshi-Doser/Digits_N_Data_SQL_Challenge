# 🛰️ Mission 5: The Assassin’s Sequence
## Six Weeks to Save Reality — SQL Investigation Project

---

## 📌 Project Overview
This project is a **SQL-based movement sequence analysis** conducted as part of the  
**Six Weeks to Save Reality** challenge by **Digits n Data**.

Mission 5 simulates a **high-risk intelligence operation** where ordered movement logs
must be analyzed to predict an imminent attack.  
The focus of this mission is on **sequence-based reasoning, window functions, and
pattern detection in time-ordered data**.

---

## 🎯 Mission Objective
The objective of this mission is to:

- Analyze **Steve’s ordered movement logs**
- Use **SequenceID** as the authoritative ordering column
- Detect the movement that occurs **immediately after `VIBRANIUM_SAFE`**
- Identify the **exact timestamp** marking the start of the attack

This timestamp serves as the **mission password** and the critical turning point
in the storyline.

---

## 🗂️ Data Source

### 📋 Movement_Logs
| Column       | Description                     |
|-------------|---------------------------------|
| LogID       | Unique log identifier            |
| SequenceID  | Definitive ordering of movements|
| TimeStamp   | Date and time of movement        |
| LocationCode| Location identifier              |
| TargetID    | Target being tracked             |

---

## 🧠 Investigation Approach

### 1️⃣ Establish the Correct Order
The investigation begins by recognizing that **SequenceID**, not timestamps,
defines the true chronological flow of events.

### 2️⃣ Detect the Repeating Anomaly
During analysis, the location code **`VIBRANIUM_SAFE`** appears multiple times.
This indicates a recurring checkpoint rather than a single event.

### 3️⃣ Look Ahead in the Sequence
To determine when escalation begins, it is necessary to identify
**what occurs immediately after `VIBRANIUM_SAFE`** in sequence order.

This requires looking into the **next row** without disrupting the dataset
or performing expensive self-joins.

### 4️⃣ Apply a Window Function
A **window function (`LEAD`)** is used to access the timestamp of the
next movement while preserving row context and order.

### 5️⃣ Isolate the Final Trigger Point
Since multiple occurrences of `VIBRANIUM_SAFE` exist, the **final occurrence**
is selected — the one that directly leads to attack initiation.

---

## 🧾 SQL Techniques Used
- Window Functions (`LEAD`)  
- `OVER (ORDER BY SequenceID)`  
- Subqueries  
- Filtering with `WHERE`  
- Ordering and limiting results  
- Sequence-based analysis without self-joins  

This mission highlights the importance of **analytical precision over query complexity**.

---

## ✅ Final Outcome
The investigation successfully identifies the timestamp:

**🕒 2025-07-15 09:01:25**

This moment marks the transition into **ATTACK_INITIATED**, confirming the exact point
at which the threat becomes active.

---

## 🧠 Key Learning
- Sequence-based logic is often more reliable than raw timestamps  
- Window functions enable elegant, scalable solutions  
- Correct interpretation of data order can completely change conclusions  

> *In intelligence — and in data — the next step matters most.*

---

## 🎥 Presentation & Sharing
A cinematic **presentation walkthrough** explaining the storyline, SQL logic,
and investigative reasoning has been shared on LinkedIn as part of the challenge.

🔗 **LinkedIn Post Link:**  
( [ Tap Here ](https://www.linkedin.com/posts/divyanshi-doser_six-weeks-to-save-reality-mission-5-activity-7415760656584429568-ciol?utm_source=share&utm_medium=member_android&rcm=ACoAAFn4nbMBzA70MeO-p2EjHsa7DB-bJ35X5lE) )
