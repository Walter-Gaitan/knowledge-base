---
layout: default
title: "🧠 Post-Sync QA Copilot Prompt"
date: 2024-06-10
---

This bot prompt automates Post-Sync QA tasks for LMS course shells. It generates:

- 🧾 Course info summary  
- 📅 Adjusted module schedule with time and skipped weeks  
- 📌 Automated due dates for assignments, discussions, and reflections  

---

## 📘 Required Inputs

To activate the logic, the user must provide:

- **Course Code**  
- **Course Title**  
- **Instructor Name**  
- **Class Day & Time (with Time Zone)**  
- **Start Date**  
- **End Date**  
- **Any Skipped Week(s)**  

---

## 🧾 Course Info Output Format

### 🧾 Course Info  
- **Course Code**: `COURSE.CODE.YYYYT`  
- **Course Title**: `Course Title Here`  
- **Instructor**: `Instructor Name`  
- **Class Time**: **Day(s), Start Time – End Time Time Zone**  
- **Start Date**: **MM/DD/YYYY**  
- **End Date**: **MM/DD/YYYY**  
- **Skip Week(s)**: `Optional – Week X – MM/DD/YYYY`


### 📅 Adjusted Module Schedule

| Module | Class Date  | Time (PT)              |
|--------|-------------|------------------------|
| 1      | 09/07/2025  | 6:00 AM – 9:00 AM      |
| 2      | 09/14/2025  | 6:00 AM – 9:00 AM      |
| 3      | 09/21/2025  | 6:00 AM – 9:00 AM      |
| 4      | 09/28/2025  | 6:00 AM – 9:00 AM      |
| 5      | 10/05/2025  | 6:00 AM – 9:00 AM      |
| 6      | 10/12/2025  | 6:00 AM – 9:00 AM      |
| 7      | 10/19/2025  | 6:00 AM – 9:00 AM      |
| 8      | 10/26/2025  | 6:00 AM – 9:00 AM      |
| *Skip* | 11/02/2025  | **No Class**           |
| 9      | 11/09/2025  | 6:00 AM – 9:00 AM      |
| 10     | 11/16/2025  | 6:00 AM – 9:00 AM      |

---

| Deliverable Type | Due Date Rule                                      |
| ---------------- | -------------------------------------------------- |
| Assignment       | 3 days after class (Wednesday), by 11:59 PM PT     |
| Discussion       | 1 day before next class (Saturday), by 11:59 PM PT |
| Reflection       | Same day as class (Sunday), by 6:00 PM PT          |


### 📌 Due Date Automation — WS810.52T

#### Module 1 (Class: 09/07/2025)
- Assignment Due: 09/10/2025 @ 11:59 PM PT
- Discussion Due: 09/13/2025 @ 11:59 PM PT
- Reflection Due: 09/07/2025 @ 6:00 PM PT

#### Module 2 (Class: 09/14/2025)
- Assignment Due: 09/17/2025 @ 11:59 PM PT
- Discussion Due: 09/20/2025 @ 11:59 PM PT
- Reflection Due: 09/14/2025 @ 6:00 PM PT

### 🔁 Skip Week Handling

- Skipped weeks are excluded from both the schedule and due date generation.

- All due dates should be offset accordingly, maintaining a weekly cadence.

### 🕒 Special Discussion Deadline Rule

> 💬 **All discussion participation must be completed by the final discussion deadline, as commonly required in syllabi:**

"Respond to comments made to your posts due by Module 10 at 11:55 PM PT."
