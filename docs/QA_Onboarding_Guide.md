# Manual QA Onboarding Guide

Welcome to the team! This guide is designed to help you get started as a Manual Quality Assurance (QA) Analyst. Your role is critical in ensuring our Blackboard Ultra courses are error-free, consistent, and user-friendly for students.

## 1. What is Software Quality Assurance (SQA)?

**Software Quality Assurance (SQA)** is the process of verifying that a product meets all requirements and quality standards. As a Manual QA Analyst, you are the last line of defense before a course goes live to students or faculty.

### Core Principles for Manual QA
1.  **Think Like a User**: Always navigate the course as a student would. If it's confusing to you, it will be confusing to them.
2.  **Attention to Detail**: Small errors (broken links, typos, wrong dates) can majorly impact the user experience.
3.  **Consistency**: Courses should feel familiar. Use the protocols to ensure every course follows the same structure.

### Your Responsibilities
-   **Verification**: Manually checking course pages against our checklists.
-   **Validation**: Ensuring features work as intended (e.g., clicking links, checking start dates).
-   **Reporting**: Clearly documenting any issues you find so they can be fixed.

---

## 2. Project Overview: Blackboard Course Verification

Our goal is to ensure every Blackboard Ultra course shell is "Student Ready" and "Instructor Ready". We check for structural integrity, content accuracy, and compliance with our standards.

### Key Documents You Will Use
*   **[QA Protocols](qa_protocols.md)**: The "Rule Book". This document explains *what* makes a course correct (e.g., naming conventions, required modules, accessibility rules).
*   **[Student QA Checklist](student_qa_checklist.md)**: The "Scorecard". This is the specific list of items you must check for every course (e.g., "Is the Syllabus link working?", "Is Module 1 visible?").

---

## 3. The QA Process

Your daily workflow will typically involve the following steps:

### Step 1: Access the Course
Log in to Blackboard and navigate to the course shell you are assigned to review.

### Step 2: "Student View" Review
Most of your testing should be done using the **Student Preview** mode in Blackboard. This ensures you see exactly what a student sees (hiding instructor-only files, grade center columns, etc.).

### Step 3: Run the Checklist
Open the **[Student QA Checklist](student_qa_checklist.md)** and methodically go through each section:
1.  **Course Info & Orientation**: Check the Banner, Syllabus link, and Start Here module.
2.  **Modules & Navigation**: Ensure all modules are visible and logical.
3.  **Content Checks**: Open assignments and discussions. Check for broken links, clear instructions, and attached rubrics.

### Step 4: Verify "release" conditions
Ensure that content meant to be hidden until a certain date is actually hidden, and content meant to be visible is visible.

### Step 5: Accessibility Spot Check
*   Do images have descriptions (Alt text)?
*   Are headers used correctly in text (H1, H2)?
*   Is the contrast readable?

### Step 6: Reporting Issues
When you find a bug (e.g., a broken link, a missing rubric, a typo):
1.  **Document it**: Note the Course ID, the specific location (e.g., "Module 1 > Assignment 2"), and the issue.
2.  **Tag it**: User standard tags if you are logging into a system (e.g., `#BrokenLink`, `#GrammarIssue`).
3.  **Be Clear**: Write the issue so that anyone reading it knows exactly how to find and fix it.
    *   *Bad*: "Link broken."
    *   *Good*: "In 'Module 1 Overview', the link to 'Article 1' leads to a 404 error page."

---

## 4. Common Issues to Watch For
*   **Placeholder Text**: Look for text like "Insert content here" or generic dates like "1/1/2035".
*   **Raw URLs**: We want descriptive links (e.g., "Click here for the article"), not raw web addresses (e.g., `https://www.google.com...`).
*   **Permissions**: Ensure files attached from Google Drive or SharePoint are actually shareable with students.
*   **Gradebook**: Check that grade columns match the assignments listed in the syllabus.

---

## 5. Tools & Resources

While your work is primarily manual, we have automated tools to help catch errors early.

### Automation Suite (Playwright)
We have a Playwright test suite that can automatically log in to Blackboard and verify course module visibility. This is useful for quickly checking that all 18 required modules are present.

*   **[Automation Setup](automation_setup.md)** — How to install and run the tests
*   **[Test Reference](test_reference.md)** — What each test does and when to use it

### Other Tools
*   **LanguageTool Reports**: Highlight potential grammar and spelling mistakes.
*   **Link Checkers**: Automated lists of broken links.

Use these reports to guide your manual review, but always verify the findings yourself.

**Questions?** Reach out to the Lead QA or refer to the `qa_protocols.md` for deep dives into specific rules.
