# 🧠 Post-Sync QA Copilot Prompt

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

```markdown
### 🧾 Course Info  
- **Course Code**: WS810.52T.2025F  
- **Course Title**: Advanced Integrative Diagnosis  
- **Instructor**: David Hashemipour  
- **Class Time**: **Sundays, 6:00 AM – 9:00 AM PT**  
- **Start Date**: **09/07/2025**  
- **End Date**: **11/16/2025**  
- **Skip Week(s)**: Week 9 – 11/02/2025

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

...
