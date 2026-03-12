# Course QA Edge Cases

Things that can be wrong or misleading when auditing a Blackboard course. Use this as a companion to the [SQA Checklist](student_qa_checklist.md) and [TQA Checklist](tqa_checklist.md).

---

## Start Here

| # | Edge Case | What to Look For |
|---|-----------|------------------|
| 1 | Module exists but is **hidden from students** | Visible to instructor but students see nothing |
| 2 | Named differently — "Welcome", "Getting Started", "Orientation" | Not recognized by standard name match |
| 3 | Module is **empty** — title exists but no content inside | Appears on outline but has zero items |
| 4 | Content is **outdated** — references a previous term/year | Dates, instructor name, or term info are stale |
| 5 | Links inside are **broken** — point to old/deleted pages | External URLs or internal Blackboard links 404 |
| 6 | Module is present but **collapsed by default** — students might miss it | Not expanded or pinned at the top |

---

## Student Resources

| # | Edge Case | What to Look For |
|---|-----------|------------------|
| 7 | Named "Program Resources" instead of "Student Resources" | Valid alternate naming but may confuse checklist |
| 8 | Present but **contains no actual resources** — placeholder text only | Title shown, but body is "TBD" or lorem ipsum |
| 9 | Resources link to **external sites** that are now **down or moved** | Library links, tutoring portals, etc. returning errors |
| 10 | **Duplicate** Student Resources sections in different modules | Confusing for students; which one is current? |
| 11 | Resources are from a **previous term** — outdated office hours, contacts | Advisor names, phone numbers, or hours are wrong |

---

## Start Course Orientation

| # | Edge Case | What to Look For |
|---|-----------|------------------|
| 12 | Orientation is **merged into Start Here** instead of separate | Content exists but not as its own module |
| 13 | **Video** in orientation is **broken or private** — doesn't play | YouTube/Kaltura embed is unavailable |
| 14 | Orientation references a **syllabus** that isn't uploaded yet | "See syllabus" but no syllabus available |
| 15 | Orientation has **no completion tracking** — students can skip it | Module should have forced completion before moving on |
| 16 | Orientation is **available but date-restricted** — opens after term starts | Students can't access it during the first week when they need it most |

---

## Modules 1–15

| # | Edge Case | What to Look For |
|---|-----------|------------------|
| 17 | **Module numbering gap** — e.g., Module 5 missing, jumps from 4 to 6 | Could be intentional (short course) or an oversight |
| 18 | Modules exist but are **all hidden/unavailable** | Instructor hasn't published them for the current term |
| 19 | Module names are **inconsistent** — "Module 1" vs "Week 1" vs "Unit 1" | Course uses different naming convention than checklist expects |
| 20 | Module has **title only, no content** inside | Appears on outline but clicking it shows empty page |
| 21 | **Wrong module order** — Module 3 appears before Module 2 | Drag-and-drop error in course setup |
| 22 | Module content is **copy-pasted from another course** — wrong references | Mentions wrong course code, instructor, or assignment names |
| 23 | **Assignments inside modules** have no due dates set | Content exists but grading deadlines are missing |
| 24 | Discussion boards or assignments link to **deleted or archived items** | "This item is no longer available" errors |
| 25 | Module has **date availability** set wrong — locked until future date | Students can't access current week's content |
| 26 | **Duplicate modules** — two "Module 7" entries | Copy error; one may be blank or outdated |
| 27 | Course has **more than 15 modules** — extras not checked | Checklist only goes to 15; Module 16+ would be skipped |
| 28 | Course has **fewer than 15 modules** — flagged as "missing" but correct | Short-term course only has 8 weeks; not an error |

---

## Cross-Cutting Concerns

| # | Edge Case | What to Look For |
|---|-----------|------------------|
| 29 | **Entire course is a copy** that wasn't updated for new term | All dates, announcements, and instructor info are from last term |
| 30 | Course is set to **"unavailable" at the course level** | Modules exist but students can't access the course at all |
| 31 | **Syllabus** not uploaded or linked anywhere in the course | Often required but not explicitly in the module list |
| 32 | **Instructor contact info** missing from Start Here or Orientation | Students have no way to reach the instructor |
| 33 | **Accessibility issues** — images without alt text, videos without captions | Content present but not ADA-compliant |
| 34 | **Gradebook columns** don't match assignments in modules | Assignments exist but have no corresponding grade column |
| 35 | **Announcements area** is empty — no welcome or start-of-term post | Students receive no initial communication |
