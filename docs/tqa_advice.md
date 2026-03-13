# TQA Advice & Preparation Guide

> **📋 Looking for the full checklist?** See the [TQA Checklist](tqa_checklist.md) for the complete 48-step verification process.

**TQA (Teacher Quality Assurance)** is the phase where Instructional Designers and Faculty prepare the course *before* it reaches the Student QA (SQA) team.

The goal of TQA is to ensure the course is "structurally sound" so SQA can focus on fine-tuning the student experience rather than fixing broken foundations.

## 🎯 The "Pre-SQA" Checklist

Before you mark a course as ready for SQA, please verify these "Big 5" items. These are the most common reasons for SQA kickbacks.

### 1. Dates, Dates, Dates
*   **System Dates**: Ensure the Course Start/End dates in the LMS settings are correct for the upcoming term.
*   **Due Dates**: Run a bulk edit or quick scan. Are there any dates from 2023 or 2024 lingering?
*   **Release Conditions**: Check that "Start Here" and "Module 1" are actually visible on the start date.

### 2. The Gradebook Schema
*   **Total Points**: Does the total match the syllabus? (e.g., if Syallbus says 1000 points, does Gradebook show 1005?)
*   **Weighted Columns**: If using weights, do they add up to 100%?
*   **Zeros**: Are "Treat ungraded items as 0" settings consistent?

### 3. Broken Links (The "Click Test")
*   **External Tools**: Click every LTI link (Cengage, Zoom, Panopto). These often break during course copy.
*   **Files**: unexpected permission errors on Google Drive/SharePoint links are common.

### 4. Duplicate Content
*   Course Copy often creates duplicates (e.g., "Syllabus (1)", "Copy of Final Exam").
*   **Action**: Delete the old versions. Do not just hide them.

### 5. Placeholder Removal
*   Scan for "[INSERT DATE HERE]" or "Instructor Name".
*   Update the "Welcome" announcement.

---

## 💡 Pro-Tips for a Smooth TQA

### 1. Use the "Student View"
Don't just look at the course in Edit mode. Enter **Student Preview** and try to submit the first assignment. If you can't, the students can't.

### 2. Check the "Hidden" folders
Sometimes content is inside a folder that is hidden. Even if the item says "Visible", if the parent folder is "Hidden", students won't see it.

### 3. Update the Syllabus First
The Syllabus is the "source of truth" for SQA. If you change a due date or an assignment name in Blackboard, **update the Syllabus document immediately**. SQA will flag a defect if they don't match.

---

## 🚀 Ready for SQA?
Once you have checked these items:
1.  Set the course status to **"Ready for SQA"** (or equivalent).
2.  Notify the SQA team.
3.  Relax! You've caught the big bugs.
