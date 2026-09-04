# Sparkle & Co — Cleaning Company Website (Demo)

A React + Vite marketing/lead-gen site for a Tampa, FL residential and
commercial cleaning company. Built as a polished demo you can deploy and
later customize for a real client.

## Tech stack
- React 18
- Vite 5
- Plain CSS (no framework) — all styles in `src/index.css`

## Getting started

```bash
npm install
npm run dev
```

Open the local URL Vite prints (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
npm run preview
```

The production build is output to `dist/`.

## Deploying

**Vercel**
1. Push this folder to a GitHub repo (or drag the folder into vercel.com's import screen).
2. Vercel auto-detects Vite. Build command: `npm run build`, output directory: `dist`.
3. Deploy.

**Netlify**
1. Build command: `npm run build`
2. Publish directory: `dist`

## Project structure

```
sparkle-cleaning/
├── package.json
├── vite.config.js
├── index.html              ← Vite entry HTML (loads /src/main.jsx)
├── public/                 ← static assets served as-is (robots.txt, favicons, etc.)
├── src/
│   ├── main.jsx             ← React root
│   ├── App.jsx               ← assembles all page sections
│   ├── index.css             ← all site styles
│   ├── data/
│   │   └── businessConfig.js ← EDIT THIS to re-skin the site for a new client
│   └── components/
│       ├── Navbar.jsx
│       ├── Hero.jsx
│       ├── TrustBar.jsx
│       ├── ProblemBenefit.jsx
│       ├── ServicesGrid.jsx
│       ├── WhatsIncluded.jsx
│       ├── BeforeAfter.jsx
│       ├── WhyChooseUs.jsx
│       ├── HowItWorks.jsx
│       ├── Reviews.jsx
│       ├── RecurringPlans.jsx
│       ├── ServiceAreas.jsx
│       ├── FAQ.jsx
│       ├── FinalCTA.jsx
│       ├── QuoteForm.jsx     ← 7-step lead form with validation + mock submit
│       ├── Contact.jsx
│       ├── Footer.jsx
│       └── MobileCTABar.jsx
└── README.md
```

## Re-skinning for a new cleaning company

Almost everything client-specific (name, phone, email, hours, service
areas, services, testimonials, FAQ, social links, Google review link) lives
in **`src/data/businessConfig.js`**. Edit that one file first.

## Connecting the quote form to a real backend

`src/components/QuoteForm.jsx` contains a `sendQuoteRequest()` function that
currently only logs the submitted data to the console. Replace its body
with a real API call — the comment inside shows the shape for a `fetch`
call to your own `/api/quote-request` endpoint, which you can then wire to
email, Google Sheets, a CRM, n8n, Zapier, Make, HubSpot, or GoHighLevel.

## Demo content notice

Testimonials, ratings, before/after photos, and trust badges in this
project are clearly-labeled placeholders. Replace them with real,
verified information before using this as a live client website.
