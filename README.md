# Role-Based LMS Dashboard with In-Chat Charting Chatbot

A modular, responsive LMS frontend demonstrating **RBAC**, **role-tailored dashboards**, and a **chatbot that renders charts inside the conversation**. Built with React (Vite) and reputable charting/data-grid libraries.

 **Assignment fit:**  
 - Role selection & mock login   
 - RBAC-driven dashboard (Admin & Student) 
 - Chatbot modal with static Q&A & in-chat charts 
 - Mock data files for users, RBAC, dashboard metrics, chatbot Q&A, charts  

---

## Demo
- **Live**:https://lms-rbac.vercel.app/  


---

## Tech Stack
- **Framework:** React (Vite)  
- **Charts:** Chart.js 
- **UI Library:** Tailwind,  
- **State/Context:** React Context API (`ThemeContext`) + local storage for session role  


---

## Project Structure
```plaintext
.
├── node_modules/
├── public/
│   └── (static assets, logos, etc.)
├── index.html                 # Root HTML (Vite entry)
├── src/
│   ├── components/
│   │   ├── ChartMessageBubble.jsx   # Renders charts inside chatbot messages
│   │   ├── ChatBotModal.jsx         # Chatbot modal with Q&A + chart integration
│   │   ├── DashBoard.jsx            # Main dashboard container (role-based rendering)
│   │   └── RoleSelector.jsx         # Mock login / role switcher
│   │
│   ├── pages/
│   │   ├── Achievements.jsx
│   │   ├── Analytics.jsx
│   │   ├── CourseManagement.jsx
│   │   ├── MyCourses.jsx
│   │   ├── Progress.jsx
│   │   ├── Settings.jsx
│   │   └── UserManagement.jsx
│   │
│   ├── widgets/
│   │   ├── AdminWidgets.jsx         # Admin-specific dashboard widgets
│   │   └── StudentWidgets.jsx       # Student-specific dashboard widgets
│   │
│   ├── contexts/
│   │   └── ThemeContext.jsx         # Theme provider (light/dark)
│   │
│   ├── mock/
│   │   ├── charts.js                # Predefined chart configs + datasets
│   │   ├── chatbotQA.js             # Role-specific Q&A pairs and chart triggers
│   │   ├── dashboardData.js         # Mock dashboard data for tables/charts
│   │   └── user.js                  # Roles and RBAC mapping
│   │
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
│
├── .gitignore
└── package.json
```
---

## Features
### 1) Authentication & Role Selection
- Simple mock role switcher via `RoleSelector.jsx` (no backend).  
- Role persisted in `localStorage` for session continuity.  

### 2) RBAC Enforcement
- Role → allowed modules defined in `mock/user.js`.  
- `DashBoard.jsx` only renders widgets allowed for current role.  

### 3) Role-Tailored Dashboards
- **Admin**: org usage stats, active users, completion rates, user/course management.  
- **Student**: my courses, progress, achievements, upcoming deadlines, quiz history.  
- At least **1 chart** and **1 table** per role.  

### 4) Chatbot Modal
- Opens from any page.  
- **Static Q&A** from `mock/chatbotQA.js`.  
- **In-Chat Charts**: triggers render `ChartMessageBubble.jsx` with configs from `mock/charts.js`.  

### 5) Responsiveness & Accessibility
- Mobile / Tablet / Desktop breakpoints.  
- Modal focus trap, `aria-live` for messages, keyboard accessible navigation.  

---

## Getting Started


**Follow these steps to set up and run the project locally:**

### 1. Navigate to project directory
```bash

cd directory
```
### 2. Install dependencies
```bash
npm install
npm audit fix --force   # optional, resolves vulnerabilities if any
```
### 3. Start the development server
```bash

npm run dev
```
### 4. Open in browser



