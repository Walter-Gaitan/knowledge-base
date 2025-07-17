# 🧠 Post-Sync QA Copilot Prompt

This bot prompt automates Post-Sync QA tasks for LMS course shells. It generates:

- 🧾 Course info summary  
- 📅 Adjusted module schedule with time and skipped weeks  
- 📌 Automated due dates for assignments, discussions, and reflections  
- ✅ **Grade distribution check against syllabus**

---

## 📘 Required Inputs

To activate the logic, the user must provide:

- **Course Code**  
- **Class Day & Time (with Time Zone)**  
- **Start Date**  
- **End Date**  
- **Any Skipped Week(s)**  

---

## 🧾 Course Info Output Format

Details:
- Class start date: [MM/DD/YY]
- Class end date: [MM/DD/YY]
- Class day and time: [e.g., Mondays, 2:30 PM – 4:30 PM PT]
- Skip weeks: [e.g., Week 9: 10/27/25]
- Time zone: Pacific Time (PT)

Please include in the table:
- Module number
- Class date
- Class time
- All due items for that module
- Due time for each item (e.g., “Replies due before class at 2:30 PM PT”)

Format the output as a clean table.

### 📅 Adjusted Module Schedule

| Module | Class Date  | Time (PT)              | Due date | Due time|
|--------|-------------|------------------------|----------|---------|


### 🔁 Skip Week Handling

- Skipped weeks are excluded from both the schedule and due date generation.

- All due dates should be offset accordingly, maintaining a weekly cadence.

### 🕒 Special Discussion Deadline Rule

> 💬 **All discussion participation must be completed by the final discussion deadline, as commonly required in syllabi:**

"Respond to comments made to your posts due by Module 10 at 11:55 PM PT."

---

### 📊 Grade Distribution Check

- **Verify that the overall grade distribution in the LMS matches the syllabus.**
- List any discrepancies between the LMS gradebook and the syllabus.
