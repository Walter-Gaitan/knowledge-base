# SQA Advice & Preparation Guide

> **📋 Looking for the full checklist?** See the [SQA Checklist](student_qa_checklist.md) for the complete 43-step verification process.

**SQA (Student Quality Assurance)** is the phase where QA Analysts verify the course from the **student's perspective** — ensuring everything a student sees, clicks, and reads works correctly.

The goal of SQA is to catch anything the TQA phase missed and confirm the course is truly "student-ready".

## 🎯 The "Big 5" SQA Issues

These are the most common reasons for findings. Checking these first saves time.

### 1. Student View ≠ Instructor View
*   **Always use Student Preview.** Content that looks fine in Edit mode may be hidden, broken, or mis-ordered from the student side.
*   Hidden parent folders will hide all items inside — even if individual items say "Visible".

### 2. Banner Mismatches
*   Every activity type (Assignment, Discussion, Test, Journal) should have a banner that matches its type.
*   Watch for banners left over from a course copy (e.g., an Assignment with a Discussion banner).

### 3. Rubric Visibility
*   Rubrics must be **visible to students** — not just attached.
*   Open each rubric link as a student to confirm it loads and matches the SharePoint file.
*   Watch for rubrics that link to an old or wrong version.

### 4. Link Verification
*   Click **every link**. External links break silently after course copies.
*   All links must open in a **new tab** — no in-page navigation.
*   Check LTI links (Cengage, Panopto, Zoom) especially; these are the most fragile.

### 5. Tab Ordering
*   **Discussions tab**: Topics should follow sequential order (Introductions → Module 1 → Module 2 → …).
*   **Gradebook tab**: Columns should be chronological or sequential.
*   **Groups tab**: Self-enrollment groups should be set up if the course requires them.

---

## 💡 Pro-Tips for a Smooth SQA

### 1. Work Module by Module
Don't jump around. Start at "Start Here" and work through each module in order. This mirrors the student experience and helps you catch flow issues.

### 2. Check the Syllabus Early
The Syllabus is your "source of truth". Open it first, note the key dates and assignment names, then verify they match what's in Blackboard. Mismatches between the Syllabus and the LMS are the most common findings.

### 3. Watch for Copy Artifacts
Course copies leave behind duplicate modules ("Syllabus (1)"), old instructor names, previous-term dates, and stale announcements. Scan for "(1)" and "(copy)" in titles.

### 4. Raw Links Are Easy to Miss
A raw link (`https://www.example.com/...`) in the middle of a paragraph is easy to overlook. Slow down when reading instructions and descriptions — if you see a URL instead of descriptive text, flag it *(ATI resources excepted)*.

### 5. Don't Forget the Orientation Acknowledgement
The "Course Orientation Acknowledgement" test must gate access to subsequent modules. Complete it in Student Preview to confirm the release conditions actually work.

---

## 🚀 SQA Wrap-Up

When you finish your review:
1.  Add your findings to the **Microsoft tracking list**.
2.  Record your time as a comment *(e.g., "QA time: 15 mins")*.
3.  Set the course status to **"SQA findings"**.
