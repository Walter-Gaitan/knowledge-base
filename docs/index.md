# Blackboard QA Automation

Welcome to the **Blackboard QA Automation** documentation site.

## Getting Started

If you are new to the team, start with the **[QA Onboarding Guide](QA_Onboarding_Guide.md)**.

---

## QA Processes

Our quality assurance workflow follows three phases in order:

### 🔍 TQA — Teacher QA
The first pass. Instructional Designers and Faculty verify the course is structurally sound before it reaches the QA team.

*   **[TQA Checklist](tqa_checklist.md)** — Full 48-step verification checklist
*   **[TQA Advice](tqa_advice.md)** — Pro-tips and common pitfalls
*   **[TQA Form Mapping](tqa_form_mapping.md)** — Form field reference

### ✅ SQA — Student QA
The student-perspective review. QA Analysts verify the course is student-ready by checking navigation, content, and link validity.

*   **[SQA Checklist](student_qa_checklist.md)** — Full 43-step verification checklist
*   **[SQA Advice](sqa_advice.md)** — Pro-tips and common pitfalls
*   **[SQA Form Mapping](form_mapping.md)** — Form field reference

### 🔁 PSQA — Post-Sync QA
The final check after course sync. Confirms LTIs, Respondus, gradebook, and due dates are correct.

*   **[PSQA Checklist](psqa_checklist.md)** — 10-step post-sync verification checklist
*   **[PSQA Form Mapping](psqa_form_mapping.md)** — Form field reference

---

## 🤖 Automation

Our Playwright test suite automates login and course verification checks.

*   **[Automation Setup](automation_setup.md)** — Install, configure, and run the test suite
*   **[Test Reference](test_reference.md)** — What each test does, architecture, and npm scripts

---

## Reference

*   **[QA Protocols](qa_protocols.md)** — Standards, review criteria, and guidelines for all QA processes
*   **[Edge Cases](edge_cases.md)** — 35 things that can go wrong when auditing a course
*   **[Program Quirks](program_quirks.md)** — Program-specific exceptions (TDAC, Med CAN, MSN, ATI)
