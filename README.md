# PayPr

# 💸 PayPr — Modern Expense Tracker for Gen Z

> _Track smarter. Spend better. No logins. No clutter. Just vibes._  

PaypR is a beautifully animated, mobile-first expense tracker built for Gen Z users (and anyone who wants something cooler than spreadsheets). It helps you manage expenses with AI insights, heatmaps, and subtle gamification — all wrapped in a smooth, black & pastel blue UI.

!

---

## ✨ Features

### 🛬 Landing Page
- Gorgeous **animated hero** with pastel vibes
- Lottie animations for an engaging intro
- “Start Exploring” button that fades into the dashboard — no login needed

### 📊 Dashboard
- Add expenses with emoji-rich category tags
- See expenses broken down by category (food, transport, etc.)
- **Live currency selector** (₹, $, €, etc.)
- Monthly **Spending Goal bar** auto-resets every month
- **Heatmaps & Pie charts** show where your money’s going
- Swipe to edit/delete (mobile) or hover actions (desktop)

### 🤖 AI Magic (via OpenAI or Genkit)
- NLP-based **auto-categorization** of expenses
- Smart **spending insights** like “You’re spending 30% more on food this month”
- Chill advice in a friendly tone (_“Maybe skip one subscription this month? 🤔”_)

### 🎯 Smart Alerts
- Monitors average spending by category
- Alerts you if a spend looks unusual (e.g., a 3× spike in ride shares)
- Option to “Ignore” or “Review” with a chart comparison

### 🏆 Gamification
- Budget streaks (days without overspending)
- Fun achievements like:
  - “No Swiggy for 3 days!” 🍱  
  - “You skipped 2 subscriptions this week!” 🎉
- Light leaderboard support (can be added via Redis or PlanetScale)

### 📁 Reports
- Detailed monthly summaries
- Export to PDF or CSV
- AI-generated suggestions to improve savings
- Heatmaps and bar/pie charts (via Recharts or Chart.js)

### 💬 About Us & Contact
- LinkedIn & GitHub icons linking to creator's profiles
- “Contact Us” form:
  - Name, email, role (user/contributor), message
  - Sends submissions to `heypaypr@gmail.com`

---

## 🧱 Tech Stack

| Frontend            | Backend / Infra          | AI & Extras              |
|---------------------|--------------------------|--------------------------|
| **Next.js 14+**     | Vercel Edge Functions     | OpenAI / Genkit AI       |
| Tailwind CSS        | PlanetScale (MySQL)      | Chart.js or Recharts     |
| React Server Comps  | Vercel Blob / UploadThing| Lottie Web Animations    |
| React + App Router  | LocalStorage (fallback)  | Vercel Analytics         |

---

## 📦 Install & Run

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/paypr.git
cd paypr

# 2. Install dependencies
pnpm install

# 3. Set up environment variables
cp .env.example .env.local
# Add your OpenAI key, PlanetScale DB credentials, Vercel Blob keys, etc.

# 4. Run locally
pnpm dev

Env Variables:
OPENAI_API_KEY=your-openai-key
DATABASE_URL=mysql://user:pass@host/db
VERCEL_BLOB_TOKEN=your-blob-token
EMAIL_TO=heypaypr@gmail.com

Folder Structure:
/app
  /landing        → Landing Page
  /home           → Dashboard
  /reports        → Analytics + Charts
  /about          → About + Contact Form
  /api            → Serverless functions (save expense, contact form, etc.)
/components       → UI elements (charts, cards, modals)
/lib              → AI utils, helpers, expense categorization
/public           → Lottie animations, icons
/styles           → Tailwind config, global styles

Made with by Shreyas Chowdhury

GitHub: @MaverickScripts

Have feedback, want to contribute, or just want to say hi?

Submit your message on the About Us page, or email us at heypaypr@gmail.com

Copyright (c) 2025 Shreyas Chowdhury

All rights reserved.

This software and its source code are the property of Shreyas Chowdhury ("the Author").

Unauthorized copying of this file, via any medium, is strictly prohibited. No part of this repository may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the Author.
