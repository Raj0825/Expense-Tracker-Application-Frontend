# 💸 SpendSmart — Frontend

> Modern dark-themed frontend for SpendSmart Expense Tracker. Built with pure HTML, CSS, and Vanilla JavaScript — no frameworks needed!

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Deployed](https://img.shields.io/badge/Deployed-GitHub%20Pages-222?style=flat-square&logo=github)

---

## 🌐 Live Demo

👉 **[https://raj0825.github.io/Expense-Tracker-Application-Frontend/login.html](https://raj0825.github.io/Expense-Tracker-Application-Frontend/login.html)**

> ⚠️ Note: Backend is on Render free tier — first request may take 30-60 seconds to wake up.

---

## 🔗 Related Repositories

| Repo | Description |
|---|---|
| [Expense-Tracker-Application](https://github.com/Raj0825/Expense-Tracker-Application) | Spring Boot Backend |
| [Expense-Tracker-Application-Frontend](https://github.com/Raj0825/Expense-Tracker-Application-Frontend) | This repo — Frontend |

---

## ✨ Features

- 🔐 **Login & Register** — JWT token auth, stored in localStorage
- 📊 **Dashboard** — Stat cards, last 7 days bar chart, by category donut chart
- 💳 **Expenses List** — Search, filter by category/date, pagination
- ➕ **Add/Edit Expense** — Category hero banner, payment method selector
- 📈 **Monthly Reports** — Month-by-month spending breakdown
- 💡 **Smart Suggestions** — Financial insights based on spending
- 👤 **Profile Settings** — Update name, currency, monthly budget
- 📱 **Responsive** — Works on desktop, tablet, mobile
- 🌙 **Dark Theme** — Modern dark UI with purple accents

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 + CSS Variables | Styling and theming |
| Vanilla JavaScript | Logic and API calls |
| Google Fonts (Syne + DM Sans) | Typography |
| SVG | Interactive donut/pie charts |
| Fetch API | REST API communication |
| localStorage | JWT token storage |

---

## 📁 Project Structure

```
Expense-Tracker-Application-Frontend/
├── docs/
│   ├── index.html          # Redirects to login
│   ├── login.html          # Login & Register page
│   ├── dashboard.html      # Main dashboard with charts
│   ├── expenses.html       # Expenses list with filters
│   ├── add-expense.html    # Add/Edit expense form
│   ├── reports.html        # Monthly reports
│   ├── suggestions.html    # Smart suggestions
│   ├── profile.html        # User profile/settings
│   ├── shared.css          # Global styles & design system
│   └── shared.js           # Shared utilities, API helper, sidebar
└── README.md
```

---

## 🎨 Design System

### Colors
```css
--bg:      #07071a    /* Page background */
--sidebar: #0b0b1f    /* Sidebar background */
--card:    #0f0f26    /* Card background */
--accent:  #7c5cfc    /* Primary purple */
--accent2: #22d3a5    /* Green accent */
--text:    #eeeeff    /* Primary text */
--muted:   #5a5a7a    /* Muted text */
```

### Typography
- **Headings** — Syne (800 weight)
- **Body** — DM Sans (300-600 weight)

---

## 📄 Pages Overview

### 🔐 login.html
- Toggle between Sign In and Create Account
- JWT token saved to localStorage on success
- Auto redirect to dashboard if already logged in

### 📊 dashboard.html
- 4 stat cards (This Month, Last Month, Total Spent, Budget Remaining)
- Last 7 Days bar chart (pure SVG)
- By Category donut/pie chart (pure SVG, interactive)
- Recent expenses list
- Smart insights panel

### 💳 expenses.html
- Paginated expense list (15 per page)
- Search by title
- Filter by category and date range
- Edit and delete actions
- Total expense count display

### ➕ add-expense.html
- Category hero banner (updates on selection)
- 11 category buttons in grid layout
- Payment method selector (Cash, Card, UPI, Net Banking, Other)
- Optional description, tags, recurring toggle
- Edit mode (loads existing expense data)

### 📈 reports.html
- Month selector
- Spending breakdown by category
- Progress bars per category

### 💡 suggestions.html
- Smart financial tips based on spending patterns
- Warning/success/alert type cards

### 👤 profile.html
- Update name, currency preference
- Set monthly budget
- Change password

---

## 🔌 API Integration

All API calls go through `shared.js`:

```javascript
const API = 'https://spendsmart-api-ooqh.onrender.com/api';

async function apiFetch(path, opts={}) {
  const headers = { 'Content-Type': 'application/json' };
  const token = getToken();
  if(token) headers['Authorization'] = `Bearer ${token}`;
  const res = await fetch(`${API}${path}`, { ...opts, headers });
  return await res.json();
}
```

---

## 🚀 Local Development

### Option 1: Open directly in browser
Just open any HTML file in your browser — but API calls won't work since backend is on Render.

### Option 2: Run with Spring Boot backend locally
1. Clone the backend repo
2. Run Spring Boot on `localhost:8080`
3. Change `shared.js` API URL to:
```javascript
const API = 'http://localhost:8080/api';
```
4. Open `http://localhost:8080/login.html`

---

## 🌍 Deployment

Frontend is deployed on **GitHub Pages** from the `/docs` folder.

```
Branch: main
Folder: /docs
URL: https://raj0825.github.io/Expense-Tracker-Application-Frontend/
```

Any push to `main` branch automatically updates the live site.

---

## 🐛 Common Issues

| Issue | Fix |
|---|---|
| Blank page on load | Check if GitHub Pages is enabled in repo Settings |
| Failed to fetch | Backend is sleeping — wait 60 seconds and retry |
| Login redirects wrong | Check `shared.js` nav paths include repo name |
| Charts not loading | Backend API `/dashboard/stats` may be slow — wait |

---

## 👨‍💻 Developer

**Raj Shah** — TY B.Tech CSE
Walchand Institute of Technology, Solapur | GPA: 8.9/10

[![GitHub](https://img.shields.io/badge/GitHub-Raj0825-black?style=flat-square&logo=github)](https://github.com/Raj0825)
[![LeetCode](https://img.shields.io/badge/LeetCode-RajShah2508-orange?style=flat-square)](https://leetcode.com/RajShah2508)
[![Backend Repo](https://img.shields.io/badge/Backend-Spring%20Boot-green?style=flat-square&logo=springboot)](https://github.com/Raj0825/Expense-Tracker-Application)

---

> Built with ❤️ using pure HTML + CSS + JavaScript | Hosted on GitHub Pages
