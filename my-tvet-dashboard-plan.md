# MY TVET Dashboard — Plan

## Overview

Build a single-file `index.html` dashboard titled **MY TVET Dashboard** using plain HTML, CSS, and JavaScript (no frameworks). The layout uses a card-based design with a clean, professional light theme. All data is hardcoded sample data. The page is divided into four main sections:

1. **Students Registered** — stat card(s) showing enrolment numbers
2. **Tasks Remaining** — stat card showing outstanding task count
3. **Workshop Status** — a status table or card grid showing per-workshop progress
4. **Preparation Checklist** — an interactive checklist of preparation items

---

## Sub-Tasks

---

### Sub-Task 1 — Page Shell and Global Styles

**Intent**  
Establish the HTML skeleton, `<head>` metadata, Google Font import, and all shared CSS (variables, reset, layout grid, card base styles, colour palette, typography). This forms the foundation every other sub-task builds on.

**Expected Outcomes**  
- `index.html` exists with a valid HTML5 docstring, viewport meta, and page title "MY TVET Dashboard"
- A sticky top header bar displaying the dashboard title is visible
- A responsive CSS grid wrapper is ready to accept cards
- Light theme colour variables are defined (primary blue, white background, subtle grey borders, accent green)

**Todo List**  
- [ ] Create `index.html` with HTML5 boilerplate
- [ ] Add `<link>` for Google Font (Inter or Poppins)
- [ ] Define CSS custom properties: `--primary`, `--bg`, `--card-bg`, `--border`, `--text`, `--accent`
- [ ] Write global reset (`box-sizing`, `margin`, `padding`, `font-family`)
- [ ] Style the `<header>` bar (title, logo placeholder, background colour)
- [ ] Create `.dashboard-grid` CSS class (CSS Grid, auto-fill columns, gap)
- [ ] Style `.card` base (white background, border-radius, box-shadow, padding)

**Relevant Context**  
- No existing files — start from scratch
- Target: single `index.html` file; all styles go in a `<style>` block inside `<head>`

**Status** `[ ] pending`

---

### Sub-Task 2 — Students Registered Section

**Intent**  
Add a stat card displaying student enrolment figures using hardcoded sample data. Includes a breakdown by programme to make the card informative.

**Expected Outcomes**  
- A card titled "Students Registered" is visible on the dashboard
- Displays a large total count (e.g. 342) prominently
- Shows a mini breakdown table or pill badges: e.g. Electrical (120), Welding (98), ICT (74), Automotive (50)
- Card uses the primary colour accent for the headline number

**Todo List**  
- [ ] Add `<section id="students">` with `.card` wrapper inside `.dashboard-grid`
- [ ] Add card header: icon + "Students Registered" title
- [ ] Add large headline number `342`
- [ ] Add programme breakdown using a small `<ul>` or flex pill list with sample values
- [ ] Style the headline number (large font size, primary colour)
- [ ] Style the breakdown pills (small, rounded, grey background)

**Relevant Context**  
- Sample data: Total 342 — Electrical 120, Welding 98, ICT 74, Automotive 50
- Card lives inside `.dashboard-grid`

**Status** `[ ] pending`

---

### Sub-Task 3 — Tasks Remaining Section

**Intent**  
Add a stat card showing how many administrative or preparation tasks are still outstanding, with a visual progress indicator.

**Expected Outcomes**  
- A card titled "Tasks Remaining" is visible
- Displays the count of remaining tasks (e.g. 7 of 15)
- A simple CSS progress bar shows percentage complete (53%)
- A small list of the top 3 pending task names is shown below the bar

**Todo List**  
- [ ] Add `<section id="tasks">` with `.card` wrapper
- [ ] Add card header: icon + "Tasks Remaining" title
- [ ] Add headline "7 / 15 remaining"
- [ ] Add a `<div class="progress-bar">` with an inner fill div set to 53% width via inline style
- [ ] Add a short `<ul>` of 3 sample pending task names
- [ ] Style progress bar (rounded, grey track, green fill)
- [ ] Style pending task list (small font, muted colour, dash prefix)

**Relevant Context**  
- Sample pending tasks: "Submit training schedules", "Confirm venue bookings", "Upload learner consent forms"
- Progress bar fill colour uses `--accent` (green)

**Status** `[ ] pending`

---

### Sub-Task 4 — Workshop Status Section

**Intent**  
Add a section displaying the readiness status of each workshop (trade/programme area) in a compact status table or card grid.

**Expected Outcomes**  
- A card titled "Workshop Status" is visible
- A table (or grid of mini-cards) lists each workshop with its status badge
- Status values: Ready, In Progress, Pending — each with a distinct colour badge
- 5 sample workshops are displayed

**Todo List**  
- [ ] Add `<section id="workshops">` with `.card` wrapper
- [ ] Add card header: icon + "Workshop Status" title
- [ ] Add a `<table>` with columns: Workshop Name, Trainer, Capacity, Status
- [ ] Populate 5 sample rows (Electrical, Welding, ICT, Automotive, Plumbing)
- [ ] Add `.badge` CSS with variants: `.badge--ready` (green), `.badge--progress` (orange), `.badge--pending` (red/grey)
- [ ] Style table: clean lines, alternating row background, no outer border

**Relevant Context**  
- Sample data:
  - Electrical | Mr. Dlamini | 30 | Ready
  - Welding | Ms. Khumalo | 25 | In Progress
  - ICT | Mr. Nkosi | 40 | Ready
  - Automotive | Ms. Mokoena | 20 | Pending
  - Plumbing | Mr. Sithole | 15 | In Progress

**Status** `[ ] pending`

---

### Sub-Task 5 — Preparation Checklist Section

**Intent**  
Add an interactive checklist card where users can tick off preparation items. State is toggled via JavaScript — no persistence required.

**Expected Outcomes**  
- A card titled "Preparation Checklist" is visible
- Lists 8 sample checklist items, each with a checkbox
- Checking an item strikes through its text and dims it
- A counter below the list shows "X of 8 completed" and updates live as boxes are ticked

**Todo List**  
- [ ] Add `<section id="checklist">` with `.card` wrapper
- [ ] Add card header: icon + "Preparation Checklist" title
- [ ] Add a `<ul>` of 8 `<li>` items each containing a `<label>` + `<input type="checkbox">`
- [ ] Add a `<p id="checklist-count">` counter below the list
- [ ] Write JavaScript: listen for `change` events on checkboxes, update counter and toggle `.checked` class on `<li>`
- [ ] Style checked `<li>`: `text-decoration: line-through`, reduced opacity
- [ ] Style custom checkbox appearance for cleaner look

**Relevant Context**  
- Sample items: Register learners on TVET system, Print attendance registers, Prepare PPE for workshops, Set up projector in lecture hall, Brief workshop trainers, Confirm catering for orientation day, Test internet connectivity, Distribute learner handbooks
- All JS is inline `<script>` at bottom of `<body>`

**Status** `[ ] pending`

---

### Sub-Task 6 — Final Polish and Responsive Behaviour

**Intent**  
Ensure the dashboard looks polished at all screen sizes, add a footer, and do a final pass on spacing, alignment, and visual consistency.

**Expected Outcomes**  
- Dashboard is fully responsive: single column on mobile, multi-column on desktop
- Cards have consistent header icon + title styling across all sections
- Footer displays "MY TVET Dashboard © 2025"
- No horizontal scroll at 375px viewport width

**Todo List**  
- [ ] Add `<footer>` element with copyright text
- [ ] Add `@media (max-width: 768px)` rule to collapse grid to single column
- [ ] Audit and align card header icon sizes, font sizes, and padding across all cards
- [ ] Verify progress bar, badges, and checklist are readable at small sizes
- [ ] Style footer (centred, muted text, top border)

**Relevant Context**  
- `.dashboard-grid` should use `grid-template-columns: repeat(auto-fill, minmax(300px, 1fr))`
- Workshop status table may need horizontal scroll on mobile: wrap in `overflow-x: auto` div

**Status** `[ ] pending`
