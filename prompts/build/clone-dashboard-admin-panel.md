---
title: "Clone Dashboard & Admin Panel"
slug: clone-dashboard-admin-panel
stage: Build
category: "Website Cloning"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-dashboard-admin-panel
---
# Clone Dashboard & Admin Panel

Replicate a target admin panel into a fully functional React and Supabase dashboard featuring real-time CRUD operations and data visualizations.

Variables: target_url

## Prompt

You are a product engineer. Reproduce the dashboard/admin panel from the target website with full CRUD functionality.

Target URL: {{target_url}}

## Layout
1. **Shell**: Sidebar navigation (collapsible), top bar (search, notifications, user menu), main content area.
2. **Responsive**: Sidebar becomes bottom nav or hamburger on mobile.
3. **Navigation**: Active states, nested sections, icon + label pattern.

## Dashboard Components
1. **Stat Cards**: KPI cards with value, trend indicator (up/down %), sparkline or mini chart.
2. **Charts**: Reproduce exact chart types (line, bar, area, pie, donut) with the same data visualization library (Recharts, Chart.js, or D3).
3. **Data Tables**: Sortable columns, search/filter, pagination, row actions (edit, delete), bulk selection.
4. **Activity Feed**: Recent actions with timestamps, user avatars, action descriptions.

## CRUD Operations
For each data entity:
1. **List View**: Table with search, filter, sort, paginate.
2. **Create**: Form with validation, file upload if needed.
3. **Read**: Detail view with all fields.
4. **Update**: Edit form pre-populated with current values.
5. **Delete**: Confirmation dialog, soft delete vs hard delete.

## Real-Time
- Live updates when data changes (Supabase Realtime)
- Optimistic UI updates
- Conflict resolution for concurrent edits

Build with:
- React + TypeScript + Tailwind
- TanStack Table for data tables
- Recharts for charts
- React Hook Form + Zod for forms
- Supabase for backend

Output complete dashboard shell, all page components, and backend integration.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Reproduces complex dashboards with charts, data tables, CRUD operations, and real-time updates.
