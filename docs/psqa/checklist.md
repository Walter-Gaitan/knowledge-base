---
title: PSQA Checklist
parent: PSQA — Post-Sync QA
nav_order: 1
---

# Post-Sync QA (PSQA) Checklist

**Goal**: Confirm that LTIs, Respondus, gradebook configuration, and due dates are correct after a course sync.

**Form URL**: [PSQA Form](https://forms.office.com/Pages/ResponsePage.aspx?id=V86IrTnQd0K3uMQU89Wa74eFLpALyTFDlgcvij0s5u1UNlQ2V0lJV1MyWUZHMkREVTQ5WUtMWFlNRi4u)

> **Related**: See the [PSQA Form Mapping](form-mapping.md) for the exact form questions and response options.

---

## Before You Start

- [ ] Tracking list for the program
- [ ] [Blackboard Course Development SharePoint](https://pacificcollege0.sharepoint.com/sites/BlackboardCourseDevelopment)
- [ ] Blackboard
- [ ] Schedule
- [ ] **Findings document** — Create a new Word document using the **SQA template** and change the title to **"Post-Sync QA Findings"**.
- [ ] **Start a timer** — Track how long the PSQA takes.

> [!WARNING]
> **Time Zones**: If your Blackboard account and the course are in different time zones, make the proper conversion when reviewing dates & times. Use your **personal account** to conduct this revision.

> [!IMPORTANT]
> **Sync Status**: Make sure the program is already synced in **Sync to BB** before starting the PSQA process.

---

## 1. Introduction

- [ ] **1. Course Code** — Enter the course code.
- [ ] **2. Status Change** — Change status to **"Under Post-Sync QA"**.

---

## 2. LTIs

**Reference**: [LTI Microsoft List](https://pacificcollege0.sharepoint.com/:l:/s/BlackboardCourseDevelopment/FF8TaTupFaxIplzaP1XLYw4BcjNVrIUOyZ9EmjJp3b7n_Q?e=87nx9m)

- [ ] **3. LTI Links** — Required LTIs present and all links work correctly.
  - Use **TeacherQA** account + **Student Preview** to test.

---

## 3. Respondus

- [ ] **4. Respondus Activation** — Respondus is activated (from **Books and Tools**).

---

## 4. TDAC Due Dates

> [!IMPORTANT]
> Only **TDAC** courses require due date updates in live shells. **AnS** uses placeholder **1/1/35**.

- [ ] **5. Due Dates** — Due dates adjusted for all assessments.

---

## 5. Gradebook

- [ ] **6. Grade Distribution** — Overall grade distribution matches syllabus.
- [ ] **7. Gradebook Sorting** — Sorted: Final Grade → Overall Grade → COA → module activities.
- [ ] **8. Grade Schema** — "Pacific College Letter" matches required parameters (A: 93.5–100%, A-: 89.5–93.5%, B+: 86.5–89.5%, B: 83.5–86.5%, B-: 79.5–83.5%, C+: 76.5–79.5%, C: 69.5–76.5%, F: 0–69.5%).

---

## 6. Wrap-Up

- [ ] **9. Time Log** — Add time as comment (format: `PS QA time: 1h 40m`).
- [ ] **10. Status Change** — Change to **"Post-Sync QA Findings"** + add findings link.
