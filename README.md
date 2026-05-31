# 🏥 Immunocare Diet Planner — Deployment Guide

## What This Is
An AI-powered diet planning web app built for Immunocare patients.
Features: 10 rheumatology disease modes, English/Hindi, PDF download, Immunocare branding.

---

## Step 1 — Get Your Anthropic API Key (5 minutes)

1. Go to **https://console.anthropic.com/**
2. Sign up or log in
3. Click "API Keys" in the left menu
4. Click "Create Key" → name it "Immunocare Diet App"
5. Copy the key (starts with `sk-ant-...`) — save it somewhere safe

**Cost:** ~₹0.50–2 per patient plan generated (very low)

---

## Step 2 — Deploy on Vercel (10 minutes, FREE)

Vercel hosts the app for free. No credit card needed for basic use.

### Option A: One-Click (Easiest)

1. Go to **https://vercel.com** → Sign up with GitHub
2. Create a GitHub account if you don't have one: **https://github.com**
3. Upload this project folder to GitHub:
   - Go to github.com → New Repository → name it "immunocare-diet"
   - Upload all these files
4. In Vercel: "Import Project" → select your GitHub repo → Deploy

### Option B: Vercel CLI (Faster if comfortable with terminal)

```bash
npm install -g vercel
cd immunocare-diet
npm install
vercel
```

---

## Step 3 — Add Your API Key to Vercel (2 minutes)

This is the critical step — keeps your key secure.

1. In Vercel dashboard → Your project → "Settings"
2. Click "Environment Variables"
3. Add:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from Step 1
4. Click Save → Redeploy the project

---

## Step 4 — Get Your Live URL

After deployment, Vercel gives you a URL like:
`https://immunocare-diet.vercel.app`

You can also set a custom domain like `diet.immunocare.in` in Vercel settings.

---

## Sharing With Patients

- Share the URL via WhatsApp
- Add a QR code to your clinic
- Link from your Instagram bio (@immunocare.rheumatology)

---

## Running Locally (For Testing)

```bash
cd immunocare-diet
npm install
cp .env.local.example .env.local
# Edit .env.local and add your API key
npm run dev
# Open http://localhost:3000
```

---

## Files in This Project

```
immunocare-diet/
├── pages/
│   ├── index.jsx        ← The entire app UI
│   └── api/
│       └── chat.js      ← Secure API proxy (15 lines)
├── package.json
├── next.config.js
├── .env.local.example   ← Copy to .env.local and add API key
└── README.md            ← This file
```

---

## Need Help?

If you get stuck at any step, share this README with a developer or IT person.
The entire deployment should take under 30 minutes from scratch.

**The only technical step** is adding the API key in Vercel's settings panel — everything else is clicking buttons.

---

*Built for Immunocare Rheumatology & Clinical Immunology Centre, Nagpur*
*Dr. Tanmay Gandhi · @immunocare.rheumatology*
