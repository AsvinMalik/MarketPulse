# MarketPulse — FB Marketplace Intelligence Platform

> **AI-powered real-time marketplace analytics** built by [Asvin](https://github.com/AsvinMalik) · IIIT Naya Raipur

A production-grade Next.js 14 dashboard featuring real-time data analysis, K-Means clustering, pricing intelligence, and an AI market advisor powered by Claude (Anthropic).

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router) |
| Frontend | React 18 + TypeScript |
| Charts | Chart.js + react-chartjs-2 |
| Animation | Framer Motion |
| AI Backend | Anthropic Claude (claude-sonnet-4-20250514) |
| API | Next.js API Routes (serverless) |
| Styling | CSS Modules |
| Hosting | Vercel (recommended) |

---

## Features

- **Real-time data simulation** — 600 listings, refreshable
- **Live ticker** — category prices with % change
- **Smart filters** — category, condition, max price
- **4 analysis tabs** — Overview, Pricing, ML Clusters, Opportunities
- **K-Means clustering** — 3 buyer segments (Budget / Mid-market / Premium)
- **Correlation matrix** — Pearson r across price, views, days
- **AI Advisor** — Claude-powered chat with SSE streaming
- **Opportunity detection** — demand/supply gap analysis
- **Fully responsive** — works on all devices

---

## Getting Started (Local)

### 1. Clone and install

```bash
git clone https://github.com/AsvinMalik/marketpulse
cd marketpulse
npm install
```

### 2. Add your API key

```bash
cp .env.local.example .env.local
```

Edit `.env.local`:
```
ANTHROPIC_API_KEY=sk-ant-your-key-here
```

Get your key at: https://console.anthropic.com

### 3. Run locally

```bash
npm run dev
```

Visit http://localhost:3000

---

## Deploy to Vercel (Share on Resume)

This gives you a **live public URL** that anyone can visit.

### Step 1 — Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit: MarketPulse"
git remote add origin https://github.com/AsvinMalik/marketpulse.git
git push -u origin main
```

### Step 2 — Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) → Sign in with GitHub
2. Click **"Add New Project"** → Select your `marketpulse` repo
3. Click **"Deploy"** (Vercel auto-detects Next.js)

### Step 3 — Add API Key (Critical)

In Vercel dashboard:
1. Go to your project → **Settings** → **Environment Variables**
2. Add:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-ant-your-key-here`
   - **Environment:** Production + Preview + Development
3. Click **Save** → Go to **Deployments** → **Redeploy**

### Step 4 — Get your URL

Your site is now live at:
```
https://marketpulse-asvin.vercel.app
```

Put this on your resume! ✅

---

## API Cost

The AI Advisor uses Claude claude-sonnet-4-20250514. Approximate costs:
- Input: ~$3 / million tokens
- Output: ~$15 / million tokens
- Each chat message ≈ 500–1000 tokens → **~$0.002 per message**
- Set spending limits at: https://console.anthropic.com/settings/limits

---

## Project Structure

```
marketpulse/
├── src/
│   ├── app/
│   │   ├── api/chat/route.ts      ← Secure Claude API route
│   │   ├── components/
│   │   │   ├── Navbar.tsx
│   │   │   ├── Ticker.tsx
│   │   │   ├── Sidebar.tsx
│   │   │   ├── KpiRow.tsx
│   │   │   ├── Charts.tsx
│   │   │   ├── ChartCard.tsx
│   │   │   ├── AIAdvisor.tsx      ← Streaming AI chat
│   │   │   └── OpportunityCards.tsx
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   └── lib/
│       └── dataEngine.ts          ← Data generation + ML algorithms
├── .env.local.example
├── next.config.js
├── package.json
└── README.md
```

---

## Resume Description

> **MarketPulse** — Full-stack AI analytics platform built with Next.js 14, React, TypeScript, and Chart.js. Features real-time K-Means clustering, Pearson correlation analysis, price decay regression, and an AI market advisor powered by Anthropic's Claude API with SSE streaming. Deployed on Vercel.
> [Live Demo](https://marketpulse-asvin.vercel.app) · [GitHub](https://github.com/AsvinMalik/marketpulse)

---

Built with ❤️ by Asvin · IIIT Naya Raipur · asvin24102@iiitnr.edu.in
