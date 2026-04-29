# Post-Sync QA (PSQA) Checklist

**Goal**: Confirm that LTIs, Respondus, gradebook configuration, and due dates are correct after a course sync.

**Form URL**: [PSQA Form](https://forms.office.com/Pages/ResponsePage.aspx?id=V86IrTnQd0K3uMQU89Wa74eFLpALyTFDlgcvij0s5u1UNlQ2V0lJV1MyWUZHMkREVTQ5WUtMWFlNRi4u)

> **Related**: See the [PSQA Form Mapping](psqa_form_mapping.md) for the exact form questions and response options.

---

## Before You Start

Open the following documents and tools before beginning:

- [ ] Tracking list for the program
- [ ] [Blackboard Course Development SharePoint](https://pacificcollege0.sharepoint.com/sites/BlackboardCourseDevelopment)
- [ ] Blackboard
- [ ] Schedule
- [ ] **Findings document** — Create a new Word document using the **SQA template** and change the title to **"Post-Sync QA Findings"**.
- [ ] **Start a timer** — Track how long the PSQA takes. You will log this time in the wrap-up step.

> [!WARNING]
> **Time Zones**: If your Blackboard account and the course are in different time zones, make the proper conversion when reviewing dates & times. Use your **personal account** to conduct this revision.

> [!IMPORTANT]
> **Sync Status**: Make sure the program is already synced in **Sync to BB** before starting the PSQA process.

---

## 1. Introduction

- [ ] **1. Course Code** — Enter the course code.
- [ ] **2. Status Change** — In the Microsoft tracking list for the program, change the status to the **"Under Post-Sync QA"** tag.

---

## 2. LTIs

**Reference**: [LTI Microsoft List](https://pacificcollege0.sharepoint.com/:l:/s/BlackboardCourseDevelopment/FF8TaTupFaxIplzaP1XLYw4BcjNVrIUOyZ9EmjJp3b7n_Q?e=87nx9m) — Use this list to confirm the correct and required tools for each course.

- [ ] **3. LTI Links** — The course has the required LTIs and all links work correctly.
  - Use the **TeacherQA** account and activate **Student Preview** to test the links.
  - Options: *Correct* / *Incorrect. Documented* / *N/A*

---

## 3. Respondus

To activate Respondus, click on the Respondus tool from the **Books and Tools** section.

- [ ] **4. Respondus Activation** — Respondus is activated for the course.
  - Options: *Done* / *N/A*

---

## 4. TDAC Due Dates

> [!IMPORTANT]
> Only courses from the **TDAC program** require their due dates to be updated in the live shells.

> [!NOTE]
> **AnS Program**: If the course is from the **AnS** program, use the placeholder date **1/1/35** wherever a due date is needed.

**References**:
- [Program Schedules (SharePoint)](https://pacificcollege0.sharepoint.com/:u:/r/sites/BlackboardCourseDevelopment/SitePages/ProjectHome.aspx?csf=1&web=1&e=eaCoLO)
- [IPM800 Groups Tab — ClickUp](https://app.clickup.com/2386547/docs/28ukk-4857/28ukk-1837) — Check the **Groups tab** in Blackboard to update the due date for "sign-ups/choices/polls" in **IPM800**.

**Instructions**:
- Follow the course schedule to adjust due dates.
- For specific due-date info, refer to: the assessments' instructions in Blackboard, the course syllabus, and the program settings file.
- Some activities' settings (tests, assignments, discussions, journals) must be enabled when a due date is assigned. These options are identified by the text **"Must be set once due dates are set up"** next to the setting option.

- [ ] **5. Due Dates** — The due dates are adjusted for all assessments.
  - Options: *Done* / *N/A*

---

## 5. Gradebook

Match the grading distribution from the syllabus with the Overall grade in Blackboard and ensure the Blackboard layout is displayed correctly.

- [ ] **6. Grade Distribution** — The overall grade distribution matches the syllabus.
  - Options: *The overall grade distribution matches the syllabus* / *In at least one assessment, the value does not match syllabus. Documented.*

- [ ] **7. Gradebook Sorting** — All items in the Gradebook are sorted correctly.
  - **Expected order**: Final Grade → Overall Grade → Course Orientation Acknowledgement → module activities in consecutive order.
  - Options: *All items in the Gradebook are sorted correctly* / *At least one item in the Gradebook is not sorted correctly. Documented.*

- [ ] **8. Grade Schema** — The **"Pacific College Letter"** grading schema matches the following parameters:

| Grade | Range % |
|-------|---------|
| A     | 93.5% – 100% |
| A-    | 89.5% – < 93.5% |
| B+    | 86.5% – < 89.5% |
| B     | 83.5% – < 86.5% |
| B-    | 79.5% – < 83.5% |
| C+    | 76.5% – < 79.5% |
| C     | 69.5% – < 76.5% |
| F     | 0% – < 69.5% |

  - Options: *All the indications above are met* / *One or more indications above are not met. Documented.*

---

## 6. Wrap-Up

- [ ] **9. Time Log** — Stop the timer and add time spent on QA as a comment in the SharePoint list.
  - Format: `PS QA time: 1h 40m`

- [ ] **10. Status Change** — In the Microsoft list of the program, change the status from **"Under Post-Sync QA"** → **"Post-Sync QA Findings"** and add the findings document link.
