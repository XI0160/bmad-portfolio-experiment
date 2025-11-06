# Cornell Student Center — Heuristic Evaluation

## **Goal**
Evaluate the current Cornell Student Center interface for usability, clarity, and task efficiency during common student actions such as viewing schedules, checking finances, and managing enrollment.

## **Method**
Inspection-based evaluation using **Nielsen’s 10 Usability Heuristics**.  
Screens evaluated:
- Dashboard (Student Center Home)
- Academics > My Academics
- Academics > Weekly Schedule
- Enrollment > Add / Drop Classes
- Enrollment > Class Search
- Finances and Personal Information

---

## **Findings**

| No | Heuristic | Violation (Observed in Screenshots) | Severity | Recommendation |
|----|------------|------------------------------------|-----------|----------------|
| 1 | **Visibility of System Status** | After clicking “Add Class,” “Continue,” or “Search,” no visible loading indicator or confirmation appears. The user must infer completion by page reload or layout change. | **High** | Add loading animation and success/error banners. Maintain visible progress indicator (Step 1–2–3) during class enrollment. |
| 2 | **Match between System and Real World** | Terminology such as “Term,” “Career,” “Enrollment Appointment,” and “Permission Nbr” reflects administrative database language. Students must decode what these mean. | **High** | Replace with human-readable equivalents: “Semester,” “Degree Level,” “Registration Time,” “Instructor Approval Code.” |
| 3 | **User Control and Freedom** | The “Go To” dropdown lacks context, and the system provides no quick navigation back to the Dashboard. Clicking “Back” in the browser may trigger session errors. | **Medium** | Introduce a persistent global navigation header and breadcrumb trail. Support browser-back safely via client-side routing. |
| 4 | **Consistency and Standards** | Inconsistent page templates: “My Academics” uses text links, “Enrollment” uses form fields, “Finances” collapses accordion panels. Buttons differ in style and hierarchy. | **Medium** | Standardize button colors, font sizes, spacing, and page grid across modules. |
| 5 | **Error Prevention** | In “Add Class” and “Drop Class” workflows, users can proceed without valid enrollment periods or incomplete course numbers. System errors only appear after full submission. | **High** | Add inline field validation and inactive button states before prerequisites are satisfied. |
| 6 | **Recognition rather than Recall** | The “Add Class” and “Search for Classes” pages require remembering exact course numbers and abbreviations. No autocomplete or pre-fill from prior searches. | **High** | Implement autocomplete, search suggestions, and recent searches. Offer course filters (instructor, time, credit). |
| 7 | **Flexibility and Efficiency of Use** | Tasks like “Search → Add → Confirm → Return to Schedule” require multiple reloads. No “Recent Tasks” or shortcuts for frequent users. | **Medium** | Introduce personalized dashboard cards (My Schedule, Add Class, Drop Class) and keyboard shortcuts. |
| 8 | **Aesthetic and Minimalist Design** | Layout heavily text-based, low visual hierarchy, poor white space. “Search for Classes” and “Drop Classes” pages appear empty and unbalanced when no data present. | **Medium** | Simplify layout using visual grouping and adaptive empty states (“You have no classes yet—Search for new courses”). |
| 9 | **Help Users Recognize, Diagnose and Recover from Errors** | Error boxes contain generic text (“You do not have a valid enrollment appointment”) without next steps. | **Medium** | Add actionable guidance (“Check your enrollment date under ‘Milestones’ or contact Registrar”). |
| 10 | **Help and Documentation** | No contextual help for advanced functions such as “Wait List” or “Permission Nbr.” Users must refer to external Registrar PDFs. | **Low** | Embed inline help popovers (“What is a Waitlist?”) and short definitions. |

---

## **Additional Observations (from New Screenshots)**

- **My Academics Page:** Hierarchy tree on the right (Institution → Career → Program → Major) adds unnecessary complexity; could be visualized as a summary card.  
- **Weekly Schedule:** Table visualization lacks differentiation; empty slots dominate view. No color-coding for course types or day highlights.  
- **Drop Classes Page:** Overly minimal, with empty state message that gives no next action.  
- **Class Search Page:** Form layout is rigid and uninviting; “Additional Search Criteria” hidden behind a small dropdown, causing user uncertainty.

---

## **Overall Assessment**

| Severity Level | Issue Count | Representative Examples |
|----------------|--------------|---------------------------|
| **High** | 4 | Feedback absence, jargon-heavy terminology, error prevention, recall overload |
| **Medium** | 4 | UI inconsistency, layout density, workflow friction, vague error text |
| **Low** | 1 | Missing contextual help |

The Student Center is functionally complete but **visually and cognitively outdated**.  
Users spend effort understanding administrative logic rather than managing their academic workflow.

---

## **Redesign Opportunities**

1. **Unified Dashboard Experience**  
   Merge Academics, Finances, and Personal Information into a single homepage with visual cards and status summaries.

2. **Smart Enrollment Flow**  
   Convert Add/Drop workflow into a modern 3-step wizard:  
   _Search → Select → Confirm_, with real-time validation and feedback.

3. **Improved Visual Hierarchy**  
   Apply Cornell branding with higher contrast, grid spacing, and accessible font sizes. Add empty-state illustrations for clarity.

4. **Contextual Guidance System**  
   Inline definitions, “?” icons, and tooltips for academic jargon and error causes.

5. **Adaptive Search & Filters**  
   Enable natural-language queries (“Find design classes next semester”) and save favorite filters or instructors.

---

## **Next Steps**

- Map existing Information Architecture and identify redundant categories.  
- Prototype redesigned dashboard and enrollment flow in Figma.  
- Conduct 5–8 usability tests measuring time-to-enroll and error recovery success.  
- Prioritize redesign backlog using frequency × severity scoring.


