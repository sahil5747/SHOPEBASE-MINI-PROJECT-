# ShopBase — E-commerce Admin Mini App

A fully functional multi-module e-commerce admin panel built with plain HTML, CSS, and JavaScript. No frameworks or build tools required.

---

## 📁 Project Structure

```
shopbase/
├── index.html          ← Main entry point
├── css/
│   └── style.css       ← All styles
├── js/
│   ├── data.js         ← Shared mock data (products, orders, users)
│   ├── auth.js         ← Login & Auth module
│   ├── catalogue.js    ← Product Catalogue module
│   ├── reporting.js    ← Reporting & Dashboard module
│   ├── users.js        ← User Management module
│   └── app.js          ← Main app controller (navigation, toasts, modals)
└── README.md
```

---

## 🚀 How to Run

### Option 1 — Open directly in browser
Just double-click `index.html`. It works without a server.

### Option 2 — VS Code Live Server (recommended)
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html` → **Open with Live Server**
3. App opens at `http://127.0.0.1:5500`

---

## 🔐 Login Credentials

| Role    | Email                      | Password    | Permissions            |
|---------|---------------------------|-------------|------------------------|
| Admin   | admin@shopbase.com        | password123 | Full access            |
| Manager | manager@shopbase.com      | password123 | Edit & view only       |
| Viewer  | viewer@shopbase.com       | password123 | View only              |

---

## 📦 Modules

### 1. Login & Auth (`js/auth.js`)
- Role-based login (Admin / Manager / Viewer)
- Session persistence via `sessionStorage`
- Permission-gated UI (buttons hidden for lower roles)

### 2. Product Catalogue (`js/catalogue.js`)
- Product grid with emoji thumbnails
- Search & category filter
- Stock status badges (In stock / Low stock / Out of stock)
- Add / Edit / Delete products (Admin & Manager only)
- Product detail modal

### 3. Reporting Dashboard (`js/reporting.js`)
- KPI metric cards (Revenue, Orders, AOV, Return Rate)
- Weekly revenue bar chart
- Category breakdown donut chart
- Recent orders table with status badges
- Export & date range filter buttons

### 4. User Management (`js/users.js`)
- User table with avatar, role, status, last active
- Search & role filter
- Invite new users (Admin only)
- Edit user role & status (Admin & Manager)
- Delete users (Admin only)

---

## 🎨 Tech Stack
- Vanilla HTML5, CSS3, JavaScript (ES6+)
- [Tabler Icons](https://tabler.io/icons) via CDN — no install needed
- No frameworks, no build step, no npm

---

## 💡 Extending the App

To connect a real backend, replace the `DB` object in `js/data.js` with API calls:

```js
// Example: Replace DB.products with a fetch call
const response = await fetch('https://your-api.com/products');
DB.products = await response.json();
renderCatalogue();
```
