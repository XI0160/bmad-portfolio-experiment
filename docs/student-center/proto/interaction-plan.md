# Cornell Student Center — Prototype Interaction Plan

## Objective
Translate the redesigned information architecture into tangible interaction flows and interface components for Figma prototyping.

---

## 1. Core User Tasks
Each prototype flow corresponds to one essential student goal.  
These define what interactions must be represented in Figma.

| Flow ID | User Goal | Start Point | End State | Expected Outcome |
|----------|------------|--------------|------------|------------------|
| F1 | Add a Class | Dashboard → Quick Action | Confirmation Modal | Class successfully added with inline feedback |
| F2 | Drop a Class | Dashboard → Manage Classes | Updated Schedule | Class removed; undo option visible for 10s |
| F3 | View Weekly Schedule | Dashboard → Schedule Card | Expanded Schedule View | Interactive calendar with course hover states |
| F4 | Check Financial Balance | Dashboard → Finances Card | Billing Page | Clear summary with “Pay Now” button |
| F5 | View Transcript | Dashboard → Quick Action → Records | Transcript Modal | Transcript displayed inline; export option enabled |

---

## 2. Page Wireframe Layouts

### A. Dashboard
**Purpose:** Central hub summarizing academic, financial, and enrollment information.

**Wireframe Zones**
[Header/Nav] — fixed global navigation (Cornell logo, Help, Profile)
[Left Column] — Schedule Card (This Week) + Enrollment Status
[Right Column] — Financial Balance + Quick Actions (Add / Drop / Transcript)
[Footer] — Last updated timestamp + accessibility shortcuts


**Interaction Highlights**
- Cards update dynamically after each action (e.g., adding or dropping a class).  
- Success feedback uses toast banners with distinct colors (green=success, red=error).  
- Hovering over a course reveals details (location, credits, instructor).  

---

### B. Add / Drop Classes (Modal Workflow)
**Purpose:** Simplify enrollment management.

**Steps**
1. Search field supports natural input (“INFO 2040” or “Data Science”).  
2. Autocomplete + filter (department, instructor, credit).  
3. Preview panel shows schedule conflicts in red.  
4. Confirm → Toast “Class Added Successfully.”  
5. Undo → Restores prior state.

**Components**
- Search input (typeahead)
- Filter dropdowns
- Conflict alert tag
- Confirmation modal
- Undo banner

---

### C. Weekly Schedule (Expanded View)
**Purpose:** Provide visual representation of timetable.

**Layout**
[Header] — Term selector + Export to Calendar button
[Grid] — Monday → Friday (columns); time slots (rows)
[Cells] — Course cards color-coded by category
[Sidebar] — Legend + “Add New Course” shortcut


**Interactions**
- Hover course → Show full detail popover.  
- Drag course card → Opens “Add / Drop” modal prefilled.  
- Empty slot → “+ Add Class” quick shortcut.  

---

### D. Financial Summary Page
**Purpose:** Visualize outstanding balances and payment options.

**Layout**
[Header] — “My Finances” title + last updated date
[Summary Card] — Current Balance + Alerts
[Chart Area] — Payment breakdown (tuition, fees, aid)
[CTA] — “Pay Now” button


**Feedback**
- Payment confirmation triggers animated success banner.  
- Balance auto-refreshes post-payment.

---

### E. Transcript Modal
**Purpose:** Allow quick access without leaving current context.

**Layout**
Modal overlay
├── Header: Student name, term selector
├── Body: Course list + grades
├── Footer: Buttons [Export PDF] [Close]

**Interactions**
- “Export PDF” triggers native download dialogue.  
- Modal is keyboard accessible (ESC = close).

---

## 3. Component Inventory
| Component | Description | Reuse Location |
|------------|--------------|----------------|
| Header Bar | Global navigation with logo + profile | All pages |
| Card Container | Base for dashboard modules | Dashboard, Finances |
| Search Field | Smart autocomplete input | Add / Drop |
| Modal Window | Reusable overlay | Transcript, Add Class |
| Toast Banner | Temporary feedback message | Success/Error states |
| Calendar Grid | 7xTime grid layout | Weekly Schedule |
| CTA Button | Primary red action button | Enrollment, Finances |

---

## 4. Interaction Principles
1. **Consistency** — Same interaction patterns across modules (modals, toasts, hover).  
2. **Visibility of Status** — Always display active state or confirmation banner.  
3. **Error Prevention** — Inline validation before submission.  
4. **Undo Availability** — Every critical action reversible for 10 seconds.  
5. **Keyboard Accessibility** — Tab traversal + ESC to close modals.

---

## 5. Prototype Implementation Plan (Figma)
1. Create frame templates for:  
   - Dashboard  
   - Add / Drop Modal  
   - Schedule View  
   - Financial Summary  
   - Transcript Modal  
2. Define component variants (cards, buttons, toasts, modals).  
3. Connect frames with smart animate for smooth transitions.  
4. Tag interactive hotspots for testing (Quick Actions, Search Field, Pay Now).  
5. Share prototype link for usability testing and feedback.

---

## 6. Testing Metrics
| Metric | Description | Target |
|---------|--------------|--------|
| Task Completion Rate | % of users who finish enrollment without errors | ≥ 90% |
| Time on Task | Seconds to add/drop one class | ≤ 60s |
| Error Rate | Wrong clicks or invalid submissions | ≤ 5% |
| Satisfaction (SUS) | Post-test usability score | ≥ 80/100 |

---

## 7. Next Steps
- Prepare prototype assets and style tokens in Figma.  
- Conduct remote usability sessions (5 participants).  
- Document insights in `docs/student-center/evaluation/usability-results.md`.  
- Begin visual design refinement phase after testing feedback.

---

**Interactions**
- “Export PDF” triggers native download dialogue.  
- Modal is keyboard accessible (ESC = close).

---

## 3. Component Inventory
| Component | Description | Reuse Location |
|------------|--------------|----------------|
| Header Bar | Global navigation with logo + profile | All pages |
| Card Container | Base for dashboard modules | Dashboard, Finances |
| Search Field | Smart autocomplete input | Add / Drop |
| Modal Window | Reusable overlay | Transcript, Add Class |
| Toast Banner | Temporary feedback message | Success/Error states |
| Calendar Grid | 7xTime grid layout | Weekly Schedule |
| CTA Button | Primary red action button | Enrollment, Finances |

---

## 4. Interaction Principles
1. **Consistency** — Same interaction patterns across modules (modals, toasts, hover).  
2. **Visibility of Status** — Always display active state or confirmation banner.  
3. **Error Prevention** — Inline validation before submission.  
4. **Undo Availability** — Every critical action reversible for 10 seconds.  
5. **Keyboard Accessibility** — Tab traversal + ESC to close modals.

---

## 5. Prototype Implementation Plan (Figma)
1. Create frame templates for:  
   - Dashboard  
   - Add / Drop Modal  
   - Schedule View  
   - Financial Summary  
   - Transcript Modal  
2. Define component variants (cards, buttons, toasts, modals).  
3. Connect frames with smart animate for smooth transitions.  
4. Tag interactive hotspots for testing (Quick Actions, Search Field, Pay Now).  
5. Share prototype link for usability testing and feedback.

---

## 6. Testing Metrics
| Metric | Description | Target |
|---------|--------------|--------|
| Task Completion Rate | % of users who finish enrollment without errors | ≥ 90% |
| Time on Task | Seconds to add/drop one class | ≤ 60s |
| Error Rate | Wrong clicks or invalid submissions | ≤ 5% |
| Satisfaction (SUS) | Post-test usability score | ≥ 80/100 |

---

## 7. Next Steps
- Prepare prototype assets and style tokens in Figma.  
- Conduct remote usability sessions (5 participants).  
- Document insights in `docs/student-center/evaluation/usability-results.md`.  
- Begin visual design refinement phase after testing feedback.

---
