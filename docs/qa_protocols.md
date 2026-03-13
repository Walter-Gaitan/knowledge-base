# LMS QA Protocols and Guidelines
(Source: https://lmsknowledgebase.miraheze.org/wiki/Main_Page)

## 🎓 Welcome
**Purpose**: Standardize QA processes and ensure consistent course quality across departments and modalities.

## 🔁 QA Protocols
### ✅ SQA – Standard QA
*   **When**: After TQA, before the live term
*   **Purpose**: Confirm consistency across sections/shells and validate applied changes
*   **Scope**: content accuracy; grading schema; assessments/rubrics; schedule validation; instructor-facing material
*   **Performed by**: QA Tester and/or Instructional Design

### 🔎 QA Reviewing Updates
*   **When**: After change requests are implemented
*   **Purpose**: Confirm requested updates were implemented correctly
*   **Scope**: requested items, formatting consistency, effects on course flow

## 📋 Course QA Checklist
### 🧭 Course Orientation
*   [ ] Syllabus present, accessible, up to date
*   [ ] Welcome/Getting Started page available
*   [ ] Course schedule/calendar accurate
*   [ ] Contact info and communication policy provided
*   [ ] Course policies align with institutional guidelines

### 🧱 Modules & Content
*   [ ] Clear, consistent module titles (naming conventions)
*   [ ] Learning objectives at top of each module or clearly accessible
*   [ ] Readable formatting (headings, bullets, spacing)
*   [ ] No placeholder/template text
*   [ ] Videos and links function correctly
*   [ ] Readings/media relevant to objectives

### 🧪 Assessments
*   [ ] Instructions are clear
*   [ ] Rubrics attached where applicable
*   [ ] Due dates correctly set and consistent with syllabus/schedule
*   [ ] Tests/quizzes published with correct settings
*   [ ] Submission methods functional and LMS-compatible

### ♿ Accessibility
*   [ ] Alt text for all images (or marked decorative)
*   [ ] Tables use headers and proper structure
*   [ ] Color contrast meets WCAG 2.1
*   [ ] Logical heading hierarchy (H1 > H2 > H3)
*   [ ] PDFs/docs readable by screen readers

### 🧭 Navigation & Course Structure
*   [ ] Clean, intuitive course menu; unused items removed
*   [ ] No placeholder links; all links work
*   [ ] Instructor-only/master-only materials removed from student view
*   [ ] No duplicated or over-nested content
*   [ ] Page titles match menu labels

### 🛠️ Technical Functionality
*   [ ] LTI tools (Turnitin, Cengage, Panopto, etc.) properly embedded
*   [ ] Interactive content loads correctly
*   [ ] Gradebook columns align with assignments
*   [ ] No broken HTML (iframes, embed tags, etc.)

## 📝 Assignment Review Criteria
1.  **Banner matches the activity type**: Ensure visual/banner accurately reflects assignment.
2.  **Directions are complete**: Full sentences, clear, grammatical.
3.  **All links work**: Open in new tabs, no raw URLs.
4.  **Due dates match syllabus**: Cross-check with official syllabus.
5.  **Rubrics are visible**: Match syllabus, ordered high-to-low.
6.  **Release conditions match syllabus**: Check availability rules.
7.  **Be concise**: Only report if change is required.

## 💬 Discussion Review Criteria
1.  **Banner matches activity type**.
2.  **Directions use complete sentences**.
3.  **All links work, open in separate tabs**.
4.  **Due dates match syllabus** (Exception: Medical Science).

5.  **Rubrics visible, match syllabus, descending order**.
6.  **Release conditions align with syllabus**.
7.  **Be concise**.

## 🧩 Correct Answer Alignment (Assessments)
*   Question text matches document exactly.
*   Answer options match content/order (unless randomized).
*   "EXCEPT"/"NOT" questions marked correctly.
*   Correct answer text matches document exactly (ignore letter labels if text matches).
*   Question type matches document.
*   Formatting preserved.

## ✍️ Grammar, Style, and Consistency QA Checklist
*   **Grammar**: Full sentences, agreement, tense.
*   **Tone**: Clear, instructional, professional.
*   **Clarity**: Specific, actionable steps.
*   **Objective phrasing**: "By the end of this module..."
*   **QA Tags**: #GrammarIssue, #InconsistentTone, #RedundantText, #TimeZoneConflict, #ClarityNeeded, #CapitalizationInconsistency

## 🧭 Content Issues Index
*   **Orientation**: Duplicate Syllabus Link, Placeholder Welcome Message
*   **Module Content**: Missing Learning Objectives, Inconsistent Heading Levels, Broken/Empty Links
*   **Assessment**: Vague Assignment Instructions, Missing Rubric, Quiz Not Published
*   **Accessibility**: Missing Alt Text, Low Color Contrast, Heading Skips
*   **Technical**: LMS Tool Not Loading, Incorrect Gradebook Setup

## 📅 Due Date Validation: Placeholder Dates
*   **Ignore**: Far-future placeholder dates (e.g., 1/2/2035) unless they conflict with syllabus or have incorrect time.
*   **Acceptable**: "Due date is 1/2/35; time is Sunday at 11:55 PM. Placeholder acceptable in unpublished shells."

## 🚫 Avoiding False Positives
*   **Placeholder Dates**: Ignore if aligned with iPlan/schedule.
*   **Rubric Availability**: Ignore if embedded in Gradebook/Overview.
*   **Missing/Unused Visuals**: Ignore if design doesn't call for them.
*   **Learning Objectives**: Ignore if listed in Course Overview/Syllabus.
