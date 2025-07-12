
# TrueCarbon x YieldMap Platform

A fullstack AI-powered platform for responsible property development and carbon reduction.

## 🧭 Purpose

- **YieldMap**: Identify sites with planning uplift and development potential.
- **TrueCarbon**: Score and reduce carbon in UK homes with AI-guided retrofit insights.
- This repo combines both into one shared codebase.

---

## 🧰 Stack Overview

| Layer     | Tech                  |
|-----------|------------------------|
| Frontend  | React (Vite + Tailwind) |
| Backend   | Flask (Python)          |
| Database  | Airtable                |
| AI Models | GPT + rule-based logic  |
| Deployment | Netlify (Frontend), Render (Backend - paused for now) |

---

## 🔧 Local Setup

### 1. Clone this Repo

```bash
git clone https://github.com/YieldMap/truecarbon-yieldmap-platform.git
cd truecarbon-yieldmap-platform
```

### 2. Setup Backend (Flask)

```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env  # Add your Airtable key, base/table IDs
python main.py
```

By default, runs at: `http://localhost:5000`

### 3. Setup Frontend (React)

```bash
cd ../frontend
npm install
cp .env.example .env
npm run dev
```

Runs at: `http://localhost:5173`

---

## 🌐 Deployment

### Frontend (Netlify - Free)

1. Push `/frontend` folder to GitHub
2. Go to [Netlify](https://netlify.com), link repo, set:
   - Build command: `npm run build`
   - Publish directory: `dist`

### Backend (Render - Hold until needed)

Configured via `render.yaml`, runs Flask API on demand.

---

## 📂 Folder Structure

```
true-platform/
├── backend/        # Flask API
├── frontend/       # React Admin UI
├── data/           # Planning, EPC, and ROI helpers
├── notebooks/      # AI model training (valuation, retrofit)
```

---

## 📋 Next Steps

- Set up your Airtable Base and connect via `.env`
- Start adding AI prompts + logic to `routes/`
- Deploy React UI to Netlify
- Expand `/retrofit` and `/uplift` pages
- Collect logs and improve AI accuracy over time

---

## 🛠 Maintainers

Built by William Tyler-Street and team. For pilots, contributions, or developer onboarding, reach out via Notion or GitHub Issues.
