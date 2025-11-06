# Cornell Student Center — Information Architecture Redesign

## **Objective**
Simplify and modernize the Student Center’s information architecture to reduce cognitive load, unify navigation, and support faster completion of academic tasks (view, plan, enroll, verify).

---

## **1. Old vs New Information Architecture**

### **Old Architecture (Current System)**
```plaintext
Student Center
├── Academics
│   ├── Search
│   ├── Plan
│   ├── Enroll
│   ├── My Academics
│   │   ├── Transfer Credit
│   │   ├── Course History
│   │   ├── Transcript
│   │   └── Enrollment Verification
├── Finances
│   ├── My Account
│   ├── Financial Aid
│   └── Other Finance Information
├── Personal Information
│   ├── Addresses
│   ├── Emergency Contact
│   └── Preferences
└── Right-Side Panels
    ├── Holds
    ├── To-Do List
    ├── Milestones
    ├── Enrollment Dates
    └── Student Resources
```

**Problems:**
- Functionally fragmented (Academic, Finance, Personal tabs siloed).  
- Hidden dependencies between pages (e.g., enrollment requires data from Academics but lives elsewhere).  
- Overloaded terminology (Career, Term, Program).  
- Repetitive navigation (each action returns to the main dashboard).  
- No central overview of student status.

---

### **New Architecture (Proposed System)**
```plaintext
Cornell Student Hub
├── Dashboard
│ ├── This Week’s Schedule
│ ├── Enrollment Status & Holds
│ ├── Financial Balance
│ ├── Upcoming Deadlines
│ └── Quick Actions (Add Class / Drop Class / Transcript)
│
├── Courses
│ ├── Search Classes
│ ├── My Plan (wishlist / planned classes)
│ ├── Enroll / Drop
│ └── Weekly Schedule
│
├── Records
│ ├── Transcript
│ ├── Grades
│ └── Enrollment Verification
│
├── Finances
│ ├── Billing Summary
│ ├── Financial Aid
│ └── Payment History
│
├── Profile
│ ├── Personal Info
│ ├── Emergency Contact
│ └── Preferences
│
└── Support
├── Advisor Contact
├── Registrar Office
└── Help & FAQ
```

**Design Logic:**
- Group by **user intent** instead of administrative domain.  
- Each top-level tab represents an actionable workflow, not a data silo.  
- “Dashboard” acts as the dynamic overview of the student’s academic and financial state.

---

## **2. Task-Flow Comparison**

| Task | Current Flow (Steps) | New Flow (Steps) |
|------|----------------------|------------------|
| **Add Class** | Home → Enroll → Add → Choose Term → Enter Class Nbr → Review | Dashboard → Add Class → Search by Keyword → Confirm → Done |
| **Drop Class** | Home → Enroll → Drop → Change Term → Confirm | Dashboard → Manage Classes → Toggle “Drop” on current class |
| **View Schedule** | Home → My Academics → Weekly Calendar | Dashboard → Schedule Card (inline preview + expand) |
| **Check Financial Aid** | Home → Finances → View Financial Aid | Dashboard → Finances → Aid Summary (card view) |
| **Transcript Request** | My Academics → Transcript → External Page | Records → Transcript → Request / View (in-page modal) |

**Outcome:**  
Average click-depth reduced from 4–5 to 2–3.  
Redundant reloads eliminated.  
Core workflows consolidated into unified navigation logic.

---

## **3. Redesign Principles**

1. **Action-Oriented IA**  
   Replace static data categories (“Academics,” “Finances”) with verbs and goals (“Courses,” “Records,” “Support”).

2. **Progressive Disclosure**  
   Simplify top-level view; show detail only when needed (e.g., expand course info inline instead of new page).

3. **Semantic Consistency**  
   Replace institutional jargon with human-readable labels:  
   “Enrollment Appointment” → “Registration Opens On,”  
   “Permission Nbr” → “Instructor Approval Code.”

4. **Task Continuity**  
   Keep users in context: transitions between search → add → confirm happen in a single-page flow.

5. **Unified Feedback System**  
   Toasts, banners, and inline status messages use consistent color logic (green = success, red = error, yellow = warning).

---

## **4. Visual & Interaction Redesign (Prototype Direction)**

| Section | Interaction Change | Visual Change |
|----------|--------------------|---------------|
| **Dashboard** | Card-based layout; dynamic modules for schedule, holds, and finances | Responsive grid (2–3 columns); Cornell Red accent; consistent button hierarchy |
| **Class Search** | Smart search (type “INFO 3450” or “data visualization”) | Simplified form; result cards with professor photo and schedule badges |
| **Enrollment Flow** | 3-step wizard (Search → Select → Confirm) | Progress tracker and contextual hints |
| **Weekly Schedule** | Integrated calendar with color-coded class types | Hover for class info; “Add from calendar” shortcut |
| **Finances** | Real-time balance with payment CTA | Clear card hierarchy, alert badges for unpaid items |
| **Profile** | Editable inline fields with autosave | Simplified typography, grouped inputs |

---

## **5. Next Steps**

1. **Wireframe** — Create low-fidelity sketches showing new Dashboard, Search, and Enrollment flow.  
2. **Prototype** — Build Figma interactive prototype for usability testing.  
3. **User Testing** — Conduct tests with 5 Cornell students focusing on:  
   - Enrollment completion time  
   - Error clarity  
   - Perceived satisfaction (SUS score)  
4. **Iteration** — Incorporate test results; refine IA labels and navigation hierarchy.  
5. **Implementation Plan** — Export components to design system for handoff.

---

## **Appendix: Old vs New Visual Metaphor**

| Before | After |
|--------|-------|
| Administrative interface designed for staff | Student-centered design prioritizing tasks |
| Fragmented tabs with reload-heavy flow | Unified hub with contextual navigation |
| Form-based inputs requiring codes | Searchable, discoverable interactions |
| Jargon and unclear status | Human language and transparent progress |

---

