# Student Records Management System (SRMS)

A web-based student records management platform built with **real SQL running in the browser** — no backend, no setup, no hosting costs.

**[View live demo →](#)** *(replace with your GitHub Pages URL after deployment)*

---

## What it does

SRMS is a complete records system for a small academic department:

- **Dashboard** — live statistics, students-by-department, top courses, recent activity
- **Students** — full CRUD with search, department filter, and status tracking
- **Courses** — course catalogue with credit hours and semester tracking
- **Enrollments** — many-to-many student↔course relationships with grade entry
- **Attendance** — per-course daily attendance marking (present / absent / late / excused)
- **Reports** — student transcripts with GPA calculation, course gradebooks, and a live SQL console
- **Role-based access** — admin, teacher, and viewer roles with distinct permissions

---

## Why SQL.js?

Most student "database projects" use `localStorage` with JSON objects — which doesn't demonstrate any actual database skill.

This project uses **[SQL.js](https://sql.js.org/)** — SQLite compiled to WebAssembly — which means **the exact same SQL you'd write against MySQL or PostgreSQL runs here**, in the browser:

- Real `CREATE TABLE` with foreign keys, `CHECK` constraints, and `UNIQUE` indexes
- Real `JOIN`s across four tables
- Real aggregate queries (`SUM`, `AVG`, `COUNT`, `GROUP BY`)
- Real `CASE` expressions for GPA calculation
- Real `ON DELETE CASCADE` behaviour

The entire database persists to `localStorage` as a SQLite binary file, so data survives page reloads.

---

## Tech stack

| Layer | Technology |
|---|---|
| Markup + Styling | HTML5, Tailwind CSS |
| Logic | Vanilla JavaScript (ES6+) |
| Database | SQLite via SQL.js (WebAssembly) |
| Auth | SHA-256 hashing via Web Crypto API |
| Persistence | Browser localStorage (SQLite binary) |

No build step. No npm. No framework. Open `index.html` and it works.

---

## Database schema
