# Customer Loyalty Points System

A web-based loyalty points system that lets staff register customers, track their purchases, and automatically award points. Built using plain HTML, CSS, and JavaScript.

---

## How to Run

1. Download or clone this repository
2. Open `index.html` in any browser (Chrome, Firefox, Edge)
3. No installation needed — it runs directly in the browser

---

## Technology Stack

- **HTML** — page structure and forms
- **CSS** — styling and layout (used CSS Grid for the two-column form layout)
- **JavaScript (Vanilla)** — all the logic: validation, points calculation, tier system
- **localStorage** — saves customer data so it doesn't disappear on page refresh

I chose not to use any frameworks because the requirements could be met with plain JavaScript, and this keeps the project easy to run, review, and explain during the interview.

---

## Features

- Register customers with name, email, and phone number
- Input validation with error messages (duplicate email check, phone format, etc.)
- Calculate points automatically: **1 point per ₹10 spent**
- Apply bonus multipliers: Weekend (1.5×), Birthday (2×), Festival (3×)
- Live points preview before submitting
- Customer summary table with tier status
- Data saved in browser — survives page refresh

## Tier System

| Tier     | Points Needed |
|----------|--------------|
| Bronze   | 0 – 999      |
| Silver   | 1,000 – 4,999 |
| Gold     | 5,000 – 9,999 |
| Platinum | 10,000+      |

---

## Assumptions

- 1 point is awarded for every ₹10 spent (fractions are rounded down)
- Only one bonus type can be applied per transaction
- Phone numbers follow the Indian 10-digit format
- Currency is in Indian Rupees (₹)
- Data is stored client-side using localStorage — no backend or database is used
- This is an admin/staff tool, not a customer-facing portal

---

## Folder Structure

```
loyalty-points-system/
├── index.html
├── README.md
└── AI_NOTE.md
```
