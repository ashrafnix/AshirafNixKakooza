<div align="center">

<img src="./app/logo.svg" alt="RepurposeAI Logo" width="180"/>

# RepurposeAI

**The world's most sophisticated AI-powered content repurposing engine.**  
Turn one piece of content into a complete suite of high-performing, platform-native assets across every major social channel — in seconds.

[![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.x-38BDF8?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Firebase](https://img.shields.io/badge/Firebase-12-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-1.17-8B5CF6?logo=google&logoColor=white)](https://ai.google.dev)
[![PayPal](https://img.shields.io/badge/PayPal-Live-003087?logo=paypal&logoColor=white)](https://developer.paypal.com)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-black?logo=vercel&logoColor=white)](https://vercel.com)
[![License](https://img.shields.io/badge/License-Proprietary-red)](./LICENSE)

**[🚀 Live App →](https://repurposeai.nexusintelligencexystems.com)**  
**[💰 Pricing →](https://repurposeai.nexusintelligencexystems.com/pricing)**  
**[🔒 Privacy Policy →](https://repurposeai.nexusintelligencexystems.com/privacy)**

</div>

---

## 📌 Table of Contents

1. [Overview](#-overview)
2. [Core Features](#-core-features)
3. [Tech Stack](#-tech-stack)
4. [Architecture Overview](#-architecture-overview)
5. [Project Structure](#-project-structure)
6. [Supported Input Sources](#-supported-input-sources)
7. [Output Formats](#-output-formats)
8. [AI Engine: Gemini Rotator](#-ai-engine-gemini-rotator)
9. [Standalone AI Tools](#-standalone-ai-tools)
10. [Automation Workflows](#-automation-workflows)
11. [Image Generation & Canvas](#-image-generation--canvas)
12. [Pricing & Plans](#-pricing--plans)
13. [Payment Integration](#-payment-integration)
14. [Authentication & Security](#-authentication--security)
15. [Database Schema (Firestore)](#-database-schema-firestore)
16. [Firestore Security Rules](#-firestore-security-rules)
17. [Admin Dashboard](#-admin-dashboard)
18. [API Reference](#-api-reference)
19. [Environment Variables](#-environment-variables)
20. [Getting Started (Local Dev)](#-getting-started-local-dev)
21. [Deployment](#-deployment)
22. [Roadmap](#-roadmap)
23. [License](#-license)

---

## 🧠 Overview

RepurposeAI is a **production-grade, full-stack SaaS application** built with Next.js 15 and Google Gemini AI. It transforms any long-form content (YouTube videos, blog posts, podcasts, PDFs, or plain text) into a complete, publish-ready suite of platform-specific social media assets — simultaneously, in a single generation job.

### The Problem

Content creators, influencers, and marketers produce long-form content (1-hour podcast, 5,000-word blog post, 30-minute video tutorial) and must then manually rewrite it into 5–7 different tones and formats for Twitter, LinkedIn, Instagram, email newsletters, and blogs. This process is:

- ⏱️ **Time-consuming** — hours of reformatting per piece of content
- 💸 **Expensive** — hiring a social media team costs $500–$2,000+/week
- 📉 **Inconsistent** — different editors produce varying quality and voice

### The Solution

RepurposeAI ingests content via multiple input methods, passes it through a finely-tuned Gemini AI engine with deep platform-specific formatting intelligence, and returns six perfectly structured, publish-ready content assets — all in one generation.

> **"You're not buying AI writing. You're buying a content multiplier. One piece of content → 10+ high-performing assets."**

### Business Model

RepurposeAI operates as a **SaaS (Software as a Service)** business with:
- 📦 **Tiered Subscription Plans** — Free through Enterprise, billed monthly via PayPal
- 🪙 **Pay-As-You-Go Credits** — No-commitment credit packs for occasional users
- 🔁 **Recurring MRR** — Passive monthly revenue that grows with the user base

---

## ✨ Core Features

| Feature | Description |
|---|---|
| 🤖 **AI Content Generation** | Powered by Gemini AI with a custom system-instruction architecture that enforces per-platform tone, structure, hooks, and CTAs |
| 🎯 **Multi-Platform Output** | Generates Twitter threads, LinkedIn posts, email newsletters, blog articles, Instagram captions, and executive summaries in one shot |
| 🔗 **YouTube Ingestion** | Fetches full video transcripts via `youtube-transcript` and feeds them directly into the AI pipeline |
| 🌐 **Web Scraping** | Scrapes any public article or web page using `cheerio` and extracts clean, semantic text for repurposing |
| 📄 **Document Upload** | Accepts PDF, DOCX, and TXT files (up to 5MB). Extracts 100% of the text using `pdf-parse` and `mammoth` |
| 📡 **RSS Feed Ingestion** | Ingests any RSS feed URL and extracts article content from the latest feed items |
| ✍️ **Rich Text Editor** | Full Tiptap-powered editor for composing, reviewing, and editing generated content before publishing |
| 🔄 **AI Content Refinement** | Dedicated `/api/refine` endpoint to re-process specific outputs with custom instructions |
| 🖼️ **AI Image Generation** | Integrated image generation pipeline (Hugging Face SDXL / Stable Horde) for social media visuals |
| 🖼️ **Image Gallery & Canvas** | Dashboard section for managing generated images and building visual compositions |
| 🛠️ **Standalone AI Tools** | A curated suite of single-purpose AI writing tools (bio writer, hashtag generator, hook writer, etc.) |
| ⚙️ **Automation Workflows** | Build automated content generation pipelines triggered on a schedule or by events |
| 📊 **Generation History** | Every generation job is saved to Firestore and accessible in the History dashboard with full output review |
| 📦 **Export as ZIP** | Download all generated content formats as a `.zip` archive in one click |
| 💳 **Subscription Billing** | Live PayPal subscription API integration with automated plan activation and webhook lifecycle management |
| 💰 **Pay-As-You-Go Credits** | One-time PayPal orders for credit packs — no commitment required, credits never expire |
| 🔐 **Firebase Auth** | Google OAuth and Email/Password sign-in via Firebase Authentication |
| 👤 **User Profile & Avatar** | Custom profile page with Cloudinary-powered avatar upload |
| 📧 **Transactional Email** | Auto-sends confirmation and welcome emails via Resend on plan activation |
| 👑 **Admin Dashboard** | Password-protected admin panel with platform telemetry, user MRR tracking, and plan analytics |
| 🔁 **API Key Rotation** | A custom Gemini key rotator that round-robins across up to N API keys with transparent failover on rate limits |
| ⚡ **Vercel Analytics** | First-class integration with `@vercel/analytics` and `@vercel/speed-insights` |
| 📱 **PWA Ready** | Web app manifest configured for progressive web app installation |
| 🗺️ **SEO Optimized** | Auto-generated sitemap, robots.txt, and full OpenGraph metadata |
| 📱 **MTN MoMo (Upcoming)** | Mobile money payment integration for African markets (Ghana 🇬🇭, Uganda 🇺🇬, Rwanda 🇷🇼, Zambia 🇿🇲, Côte d'Ivoire 🇨🇮) |

---

## 🛠 Tech Stack

### Frontend
| Library | Version | Purpose |
|---|---|---|
| `next` | 15.x | Full-stack React framework (App Router, Server Components, API Routes) |
| `react` | 19.x | UI rendering with concurrent features |
| `typescript` | 5.9.x | End-to-end type safety |
| `tailwindcss` | 4.x | Utility-first CSS with JIT compiler |
| `motion` | 12.x | Declarative animations & page transitions (Framer Motion) |
| `lucide-react` | 0.553.x | Consistent, lightweight icon system |
| `@tiptap/react` | 3.x | Headless, extensible rich text editor |
| `@tiptap/starter-kit` | 3.x | Tiptap core extensions bundle |
| `react-dropzone` | 15.x | Drag-and-drop file upload UX |
| `react-markdown` | 10.x | Safe, extensible Markdown rendering |
| `sonner` | 2.x | Accessible, beautiful toast notifications |
| `date-fns` | 4.x | Lightweight date formatting & parsing |
| `clsx` + `tailwind-merge` | latest | Conditional class name management |
| `class-variance-authority` | 0.7.x | Typed UI variant system |

### Backend / API
| Library | Version | Purpose |
|---|---|---|
| `@google/genai` | 1.17.x | Google Gemini AI SDK |
| `firebase-admin` | 13.x | Server-side Firestore reads/writes & token verification |
| `firebase` | 12.x | Client-side Auth & Firestore real-time listeners |
| `@paypal/react-paypal-js` | 7.8.x | PayPal Smart Buttons & Subscriptions UI |
| `resend` | 6.x | Transactional email delivery |
| `cheerio` | 1.x | Fast server-side HTML scraping (jQuery-like API) |
| `youtube-transcript` | 1.x | YouTube video transcript extraction |
| `pdf-parse` | 2.x | Full-text PDF extraction |
| `mammoth` | 1.x | DOCX → plain text conversion |
| `rss-parser` | 3.x | RSS & Atom feed ingestion |
| `cloudinary` | 2.x | Cloud image CDN — uploads, transforms, delivery |
| `adm-zip` | 0.5.x | Server-side ZIP archive creation for content export |

### Infrastructure
| Service | Purpose |
|---|---|
| **Vercel** | Hosting, serverless functions, edge network, CI/CD |
| **Firebase Firestore** | Primary NoSQL database (users, outputs, history) |
| **Firebase Authentication** | Identity & session management |
| **PayPal Live API** | Subscription billing and one-time payment orders |
| **Cloudinary** | User avatar and generated image CDN |
| **Google Gemini** | Core AI generation model (`gemini-2.5-flash-lite-preview`) |
| **Hugging Face / Stable Horde** | AI image generation pipeline |
| **Resend** | Transactional email (plan upgrades, welcome emails) |

### Dev Tools
| Tool | Purpose |
|---|---|
| `eslint` + `eslint-config-next` | Code linting |
| `typescript` | Compile-time type checking |
| `firebase-tools` | Firestore rules deployment |
| `puppeteer` | Browser automation (screenshots) |
| `@tailwindcss/typography` | Prose content styling |
| `tw-animate-css` | CSS animation utilities for Tailwind |

---

## 🏗 Architecture Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                          CLIENT (Browser)                           │
│   Next.js App Router · React 19 · TailwindCSS 4 · Framer Motion    │
│                                                                     │
│  Landing Page → Auth Modal → Dashboard → Repurpose / Tools / Admin │
├─────────────────────────────────────────────────────────────────────┤
│                       NEXT.JS API ROUTES                            │
│                       (Serverless Functions)                        │
│                                                                     │
│  /api/generate              ← Core AI repurposing endpoint ⚡       │
│  /api/refine                ← AI-powered content refinement         │
│  /api/tools                 ← Standalone AI tools engine            │
│  /api/automations           ← Automated content workflow engine     │
│  /api/extract-youtube       ← YouTube transcript pipeline           │
│  /api/extract-web           ← Web scraper (cheerio)                 │
│  /api/extract-document      ← PDF / DOCX / TXT parser              │
│  /api/generate-image        ← Hugging Face / Stable Horde SDXL     │
│  /api/paypal/create-order          ← PAYG one-time payment order   │
│  /api/paypal/create-subscription   ← Subscription creation         │
│  /api/paypal/activate-subscription ← Post-approval activation      │
│  /api/webhooks/paypal       ← PayPal IPN lifecycle handler         │
│  /api/admin/me              ← Admin identity verification           │
│  /api/admin/telemetry       ← Platform MRR & user analytics        │
│  /api/upload-avatar         ← Cloudinary avatar upload             │
│  /api/upload-image          ← Cloudinary image asset upload        │
│  /api/download              ← Export outputs as .zip archive       │
├─────────────────────────────────────────────────────────────────────┤
│                            SERVICES (lib/)                          │
│                                                                     │
│  gemini-rotator.ts    ← Multi-key AI request manager + failover    │
│  firebase-admin.ts    ← Server-side Firebase Admin SDK singleton   │
│  paypal.ts            ← PayPal REST API client wrapper             │
│  plans.ts             ← Plan limits, tier definitions & pricing     │
│  email.ts             ← Resend transactional email helpers          │
│  firestore-error.ts   ← Firestore error classifier & logger        │
│  clipboard.ts         ← Clipboard interaction utility              │
│  utils.ts             ← Shared utility functions                   │
├─────────────────────────────────────────────────────────────────────┤
│                        EXTERNAL SERVICES                            │
│                                                                     │
│  Google Gemini API  ·  Firebase/Firestore  ·  PayPal Live          │
│  Cloudinary CDN  ·  HuggingFace / Stable Horde  ·  Resend Email   │
└─────────────────────────────────────────────────────────────────────┘
```

### Request Lifecycle (Core Generation)

```
User submits content
        │
        ▼
/api/generate (POST)
        │
        ├── 1. Verify Firebase ID Token (firebase-admin)
        ├── 2. Load user document from Firestore
        ├── 3. Enforce usage limits (PAYG credits → plan limit)
        ├── 4. Route to correct input extractor:
        │        ├── text    → use raw content directly
        │        ├── youtube → /api/extract-youtube (transcript)
        │        ├── web     → /api/extract-web (cheerio)
        │        └── doc     → /api/extract-document (pdf/docx/txt)
        ├── 5. Build prompt with system instructions + schema
        ├── 6. Call Gemini API via key rotator (failover enabled)
        ├── 7. Parse structured JSON response
        ├── 8. Save output document to Firestore (/outputs/{id})
        ├── 9. Decrement PAYG credit or increment monthly usage count
        └── 10. Return output to client
```

---

## 📁 Project Structure

```
repurposeAI/
├── app/
│   ├── api/
│   │   ├── admin/
│   │   │   ├── me/                  ← Admin identity & access check
│   │   │   └── telemetry/           ← MRR, user count & plan analytics
│   │   ├── automations/             ← Automated repurposing workflow engine
│   │   ├── download/                ← Export generated content as .zip
│   │   ├── extract-document/        ← PDF / DOCX / TXT text extraction
│   │   ├── extract-web/             ← Cheerio web article scraper
│   │   ├── extract-youtube/         ← YouTube transcript fetcher
│   │   ├── generate/                ← ⚡ Core AI generation endpoint
│   │   ├── generate-image/          ← AI image generation (SDXL)
│   │   ├── paypal/
│   │   │   ├── create-order/        ← PAYG one-time PayPal order
│   │   │   ├── create-subscription/ ← Subscription plan creation
│   │   │   └── activate-subscription/ ← Post-approval activation
│   │   ├── refine/                  ← AI content refinement endpoint
│   │   ├── tools/                   ← Standalone AI tools engine
│   │   ├── upload-avatar/           ← Cloudinary avatar upload
│   │   ├── upload-image/            ← Cloudinary image upload
│   │   └── webhooks/
│   │       └── paypal/              ← PayPal IPN webhook handler
│   │
│   ├── dashboard/
│   │   ├── admin/                   ← Admin panel (telemetry, users, MRR)
│   │   ├── automations/             ← Automation builder UI
│   │   ├── canvas/                  ← Visual image canvas tool
│   │   ├── gallery/                 ← Generated image gallery
│   │   ├── history/                 ← Full generation history viewer
│   │   ├── images/                  ← Image management hub
│   │   ├── profile/                 ← User profile & avatar editor
│   │   ├── repurpose/               ← 🎯 Main repurposing interface
│   │   ├── settings/                ← Account & subscription settings
│   │   └── tools/                   ← Standalone AI tools hub
│   │
│   ├── pricing/                     ← Public pricing page with plan toggle
│   ├── cookie-policy/               ← Cookie policy page
│   ├── privacy/                     ← Privacy policy page
│   ├── terms/                       ← Terms of service page
│   ├── globals.css                  ← Global styles & design tokens
│   ├── layout.tsx                   ← Root layout with providers & analytics
│   ├── manifest.ts                  ← PWA web app manifest
│   ├── page.tsx                     ← Public landing page
│   ├── robots.ts                    ← SEO robots.txt config
│   └── sitemap.ts                   ← Auto-generated XML sitemap
│
├── components/
│   ├── auth-modal.tsx               ← Auth modal (login / signup / reset)
│   ├── auth-provider.tsx            ← Firebase Auth React context provider
│   ├── canvas/                      ← Image canvas editor components
│   ├── error-boundary.tsx           ← React error boundary wrapper
│   ├── feedback-widget.tsx          ← In-app user feedback widget
│   ├── image-generation-loader.tsx  ← AI image gen progress UI
│   ├── logo.tsx                     ← SVG logo component
│   ├── paypal-checkout.tsx          ← PayPal Smart Buttons wrapper
│   ├── rich-text-editor.tsx         ← Tiptap editor wrapper component
│   └── ui/                          ← Reusable UI primitive components
│
├── lib/
│   ├── clipboard.ts                 ← Browser clipboard interaction utility
│   ├── email.ts                     ← Resend email client & templates
│   ├── firebase-admin.ts            ← Firebase Admin SDK singleton (server)
│   ├── firestore-error.ts           ← Firestore error classification & logging
│   ├── gemini-rotator.ts            ← ⚡ Multi-key AI request manager
│   ├── paypal.ts                    ← PayPal REST API client wrapper
│   ├── plans.ts                     ← Plan limits, tier config & pricing data
│   └── utils.ts                     ← Shared utility functions
│
├── hooks/                           ← Custom React hooks
├── scripts/
│   ├── setup-paypal.mjs             ← PayPal subscription plan provisioning
│   └── setup-paypal.ps1             ← PowerShell variant of setup script
│
├── public/                          ← Static assets (icons, images, OG images)
├── .env.local                       ← Local environment variables (DO NOT COMMIT)
├── .gitignore
├── firebase.json                    ← Firebase hosting & Firestore config
├── firebase.ts                      ← Firebase client-side SDK initialization
├── firestore.rules                  ← Firestore row-level security rules
├── next.config.ts                   ← Next.js configuration
├── package.json
├── postcss.config.mjs
└── tsconfig.json
```

---

## 📥 Supported Input Sources

| Input Type | Method | Details |
|---|---|---|
| **Plain Text** | Paste | Direct input — up to 500,000 characters |
| **YouTube Video** | URL | Full transcript extracted via `youtube-transcript` package |
| **Web Article** | URL | Full-page text scraped via `cheerio` HTML parser |
| **PDF File** | Upload | 100% text extraction via `pdf-parse` (up to 5MB) |
| **Word Document** | Upload | Full DOCX parsing via `mammoth` library (up to 5MB) |
| **TXT File** | Upload | Raw text file direct read (up to 5MB) |
| **RSS Feed** | URL | Feed item content extracted via `rss-parser` |

---

## 📤 Output Formats

Each generation job produces **6 distinct, platform-native content assets** simultaneously:

| Format | Platform | Target Length | Key Rules Enforced |
|---|---|---|---|
| **Twitter/X Thread** | Twitter/X | 3 posts | Hook → Insight → CTA. One idea per tweet. Max 240 chars on post 1 |
| **LinkedIn Post** | LinkedIn | 150–250 words | First 2 lines must hook before the "see more" fold. Ends with engagement question + 3–5 hashtags |
| **Email Newsletter** | Email | 300–450 words | Starts with compelling subject line. Warm opener, value body, CTA sign-off |
| **Blog Article** | Blog / SEO | 500–700 words | Keyword-rich H1, hook intro, 2+ H2 sections, scannable body, CTA conclusion |
| **Instagram Caption** | Instagram | 80–150 words + hashtags | Scroll-stopping first line. Personal voice. Micro-CTA embedded. 10–15 hashtags in separate block |
| **Executive Summary** | Universal | 2–3 sentences | Core insight + why it matters + implied action, distilled for a busy decision-maker |

All formats are generated **simultaneously in a single API call** using a structured JSON schema enforced by Gemini's `responseMimeType: 'application/json'` + `responseSchema` feature.

### User-Configurable Parameters

Before generating, users can customize:

| Parameter | Options |
|---|---|
| **Tone** | Professional, Casual, Humorous, Inspirational, Educational, Authoritative, Conversational |
| **Target Audience** | (Free text — e.g., "startup founders", "fitness enthusiasts") |
| **Length** | Short · Standard · Long |

---

## ⚡ AI Engine: Gemini Rotator

The core of RepurposeAI's scalability on free/low-cost API tiers is the **Gemini API Key Rotator** (`lib/gemini-rotator.ts`).

### How It Works

1. **Multiple API Keys:** Configure up to N Gemini API keys as a comma-separated value in `GEMINI_API_KEYS`.
2. **Fisher-Yates Shuffle:** On each request, the key list is randomly shuffled to distribute load evenly across Vercel's stateless serverless functions.
3. **Automatic Failover:** If a key returns a `429 (Rate Limited)` or `503 (Server Error)`, the rotator silently moves to the next key and retries.
4. **Fast Failure:** If the error is not a rate limit (e.g., bad schema, authentication error), the rotator throws immediately without wasting retries.
5. **Exhaustion Handling:** If all keys are simultaneously rate-limited, a user-friendly error is returned.

```typescript
// Example: 5 API keys provides ~5x the free-tier throughput
GEMINI_API_KEYS="key1,key2,key3,key4,key5"
```

### Model Configuration

| Setting | Value |
|---|---|
| **Model** | `gemini-2.5-flash-lite-preview` |
| **Temperature** | `0.8` (creative but consistent) |
| **Response Mode** | Structured JSON via `responseMimeType: 'application/json'` + `responseSchema` |
| **Thinking Budget** | `0` (disabled for maximum speed on flash model) |
| **System Instructions** | Deep per-platform content formatting knowledge injected as system-level prompt |

### Why This Architecture?

This design solves a critical limitation: Gemini's free tier has strict per-minute rate limits. By rotating across multiple free-tier keys, the effective throughput multiplies linearly. When deployed on Vercel's serverless platform (which creates ephemeral, stateless function instances), the random shuffle ensures that no single key is consistently hit first across concurrent requests.

---

## 🛠️ Standalone AI Tools

The `/dashboard/tools` section provides a curated set of single-purpose AI writing tools powered by the same Gemini engine. These are quick, focused tasks that don't require a full content repurposing job.

Examples include:
- **Bio Writer** — Generate professional or casual bios from a short description
- **Hook Generator** — Create scroll-stopping opening lines for any platform
- **Hashtag Research Tool** — Generate researched, trending hashtag sets
- **Caption Rewriter** — Transform a draft caption into a platform-optimized version
- **CTA Generator** — Produce high-converting calls-to-action
- **Headline Analyzer** — Score and improve blog or newsletter headlines
- **Content Idea Generator** — Brainstorm content ideas from a keyword or niche

All tool outputs are rendered through the rich text editor and can be copied or exported.

---

## ⚙️ Automation Workflows

The `/dashboard/automations` section (currently in active development) allows users to build automated content pipelines:

- **Triggers:** Schedule-based (daily/weekly), RSS feed updates, or manual
- **Actions:** Automatically repurpose new content from a connected source
- **Output:** Post directly to connected accounts or save to history
- **Status:** 🔨 In Progress — targeted for Q2 2026

---

## 🖼️ Image Generation & Canvas

### AI Image Generation
Users can generate social media-ready images from text prompts using:
- **Hugging Face SDXL** — High-quality diffusion model via HF Inference API
- **Stable Horde** — Distributed generation network (free tier with API key; anonymous mode available with slower results)

Generated images are uploaded and stored via **Cloudinary** for persistent access.

### Image Canvas
The `/dashboard/canvas` tool provides a drag-and-drop visual editor for combining generated images, adding text overlays, and building social media graphics — similar to a lightweight Canva-style editor.

### Image Gallery
All generated images are accessible in the `/dashboard/gallery` section, organized chronologically with full image download support.

---

## 💳 Pricing & Plans

RepurposeAI uses a **tiered subscription model** plus a **pay-as-you-go** credit option.

### Subscription Plans

| Plan | Launch Price | MSRP | Monthly Repurposes | Best For |
|---|---|---|---|---|
| **Free** | $0/mo | $0/mo | 5 | Trying it out |
| **Starter** | $5/mo | $7/mo | 10 | Hobbyists & beginners |
| **Creator** ⭐ | $15/mo | $24/mo | 60 | Active content creators |
| **Pro** | $39/mo | $59/mo | 180 | Full-time creators & agencies |
| **Enterprise** | $99/mo | $129/mo | 500 | Teams & high-volume publishers |

> **🔒 Early Bird Guarantee:** The first 50–100 subscribers lock in the launch price **forever** — no future price increases, guaranteed.

### Pay-As-You-Go Credit Packs

| Pack | Price | Credits | Per-Credit Cost |
|---|---|---|---|
| Starter Pack | $5 | 10 repurposes | $0.50/repurpose |
| Value Pack ⭐ | $12 | 30 repurposes | $0.40/repurpose |

Credits **never expire** and require no subscription commitment.

### Usage Enforcement (Server-Side)

Usage limits are strictly enforced inside `/api/generate`:

1. **PAYG Credits First:** If `user.paygoCredits > 0`, one credit is consumed before checking the monthly plan limit.
2. **Plan Monthly Limit:** If no PAYG credits remain, the system queries Firestore for all outputs generated since the 1st of the current month and compares against the plan ceiling (defined in `lib/plans.ts`).
3. **Limit Exceeded:** Returns HTTP `403` with a descriptive message prompting the user to upgrade or purchase credits.

This means limits cannot be bypassed by manipulating the client—all checks run server-side after Firebase token verification.

---

## 💰 Payment Integration

### PayPal Live API

RepurposeAI is fully integrated with the **PayPal REST API in live (production) mode**.

#### Subscription Flow

```
1. User selects a plan on the Pricing page
        │
        ▼
2. POST /api/paypal/create-subscription
   └── Creates a PayPal Billing Agreement for the selected plan ID
   └── Returns PayPal approval URL
        │
        ▼
3. User completes PayPal checkout (redirect or popup)
        │
        ▼
4. PayPal sends webhook → POST /api/webhooks/paypal
   └── Event: BILLING.SUBSCRIPTION.ACTIVATED
   └── Signature verified via PAYPAL_WEBHOOK_ID
   └── Updates user.plan in Firestore
   └── Sends confirmation email via Resend
        │
        ▼
5. User's dashboard reflects the new plan tier immediately
```

#### Pay-As-You-Go Flow

```
1. User selects a credit pack
        │
        ▼
2. POST /api/paypal/create-order
   └── Creates a PayPal one-time order
        │
        ▼
3. User approves the PayPal order
        │
        ▼
4. POST /api/paypal/activate-subscription (order capture)
   └── Captures payment via PayPal Orders v2 API
   └── Increments user.paygoCredits in Firestore
        │
        ▼
5. Credits are available immediately for use
```

#### PayPal Plan IDs (Live Environment)

| Plan | Regular Billing ID | Launch Price ID |
|---|---|---|
| Starter | `P-6DV22536A4197813HNHMVNMI` | `P-2DB497816U1301831NHMVNMQ` |
| Creator | `P-59247853WU7826034NHMVNMI` | `P-74E681394J482850WNHMVNMY` |
| Pro | `P-5CB18145F2359271YNHMVNMQ` | `P-15V31003AX295605WNHMVNMY` |
| Enterprise | `P-8NX05025259924427NHMVNMQ` | `P-5LA39148Y08238503NHMVNMY` |

> Plan IDs are provisioned using `scripts/setup-paypal.mjs` via the PayPal REST API. The `LAUNCH` variants are grandfathered pricing plans with a permanent discount.

### MTN Mobile Money (Q3 2026)

Integration with the **MTN MoMo API** is planned for Q3 2026. This will allow users in supported African markets to pay for credits and subscriptions via mobile USSD — **without needing a bank card or PayPal account.**

Supported countries: Ghana 🇬🇭, Uganda 🇺🇬, Rwanda 🇷🇼, Zambia 🇿🇲, Côte d'Ivoire 🇨🇮

---

## 🔐 Authentication & Security

| Layer | Technology | Details |
|---|---|---|
| **Client Auth** | Firebase Authentication | Google OAuth 2.0 + Email/Password |
| **Session Token** | Firebase ID Token (JWT) | Sent as `Authorization: Bearer <token>` on every protected API call |
| **Server Verification** | `firebase-admin.auth().verifyIdToken()` | All protected routes verify the JWT before processing anything |
| **Admin Access** | `ADMIN_EMAILS` env var | Only whitelisted emails can call `/api/admin/*` routes |
| **PayPal Webhooks** | `PAYPAL_WEBHOOK_ID` signature verification | All incoming PayPal events are cryptographically verified before state changes |
| **Firestore Rules** | `firestore.rules` | Row-level security — users can only read/write their own data |
| **Secrets** | `.env.local` / Vercel Env | All API keys and secrets stored in environment variables, never in source code |

### Auth Flow

```
User visits app
     │
     ▼
AuthProvider (components/auth-provider.tsx)
     │
     ├── onAuthStateChanged listener (Firebase)
     ├── Loads user Firestore document on login
     ├── Stores user + idToken in React context
     └── Refreshes token before every API call
```

---

## 🗃 Database Schema (Firestore)

### `users/{uid}`
```json
{
  "uid": "string",
  "email": "string",
  "displayName": "string",
  "photoURL": "string (Cloudinary URL)",
  "plan": "'free' | 'starter' | 'creator' | 'pro' | 'agency'",
  "paygoCredits": "number (0+)",
  "paypalSubscriptionId": "string (optional)",
  "createdAt": "Firestore Timestamp",
  "updatedAt": "Firestore Timestamp"
}
```

### `outputs/{outputId}`
```json
{
  "userId": "string",
  "inputType": "'text' | 'youtube' | 'web' | 'document'",
  "originalUrl": "string (optional, for YouTube / web inputs)",
  "content": "string (source content preview, truncated)",
  "tone": "string",
  "targetAudience": "string",
  "length": "'Short' | 'Standard' | 'Long'",
  "result": {
    "tweets": ["string", "string", "string"],
    "linkedin": "string",
    "newsletter": "string",
    "blog": "string",
    "instagram": "string",
    "summary": "string"
  },
  "createdAt": "Firestore Timestamp"
}
```

### `images/{imageId}` *(Generated Images)*
```json
{
  "userId": "string",
  "prompt": "string",
  "cloudinaryUrl": "string",
  "cloudinaryPublicId": "string",
  "createdAt": "Firestore Timestamp"
}
```

---

## 🛡 Firestore Security Rules

Security rules (`firestore.rules`) enforce that:

- Users can **only read and write their own** `users/{uid}` document.
- Users can **only read and write their own** `outputs/{outputId}` documents (filtered by `userId`).
- All admin-level reads are performed server-side via the **Firebase Admin SDK**, which bypasses client-facing security rules entirely.
- No unauthenticated client can read or write any document.

Deploy updated rules using:
```bash
firebase deploy --only firestore:rules
```

---

## 👑 Admin Dashboard

The admin panel is accessible at `/dashboard/admin` and is restricted to email addresses listed in the `ADMIN_EMAILS` environment variable. The admin check runs server-side on every request to `/api/admin/*`.

### Available Telemetry

| Metric | Description |
|---|---|
| **Total Users** | All registered platform users |
| **Total Outputs** | Cumulative AI generation jobs completed across all users |
| **MRR** | Monthly Recurring Revenue calculated from active subscription plan distribution |
| **Plan Breakdown** | Distribution of users across Free, Starter, Creator, Pro, and Enterprise tiers |
| **Recent Signups** | Latest user registrations with timestamps and plan info |

### MRR Calculation

MRR is calculated server-side by:
1. Querying all `users` with `plan != 'free'`
2. Mapping each plan to its **launch price** (to reflect actual revenue from grandfathered subscribers)
3. Summing the total

---

## 📡 API Reference

All API routes are Next.js **App Router route handlers**. Protected routes require a valid Firebase ID token in the `Authorization: Bearer <token>` header.

| Method | Route | Auth | Description |
|---|---|---|---|
| `POST` | `/api/generate` | ✅ Required | Core AI repurposing — accepts content + config, returns 6 platform outputs |
| `POST` | `/api/refine` | ✅ Required | Re-process a specific output with custom instructions |
| `POST` | `/api/tools` | ✅ Required | Run a standalone AI tool (bio, hooks, hashtags, etc.) |
| `POST` | `/api/automations` | ✅ Required | Trigger or configure an automation workflow |
| `POST` | `/api/extract-youtube` | ✅ Required | Extract transcript from a YouTube URL |
| `POST` | `/api/extract-web` | ✅ Required | Scrape and extract text from a web URL |
| `POST` | `/api/extract-document` | ✅ Required | Parse and extract text from PDF/DOCX/TXT upload |
| `POST` | `/api/generate-image` | ✅ Required | Generate an AI image from a text prompt |
| `POST` | `/api/paypal/create-order` | ✅ Required | Create a PayPal one-time order for PAYG credits |
| `POST` | `/api/paypal/create-subscription` | ✅ Required | Create a PayPal billing subscription |
| `POST` | `/api/paypal/activate-subscription` | ✅ Required | Capture payment and activate plan / credits |
| `POST` | `/api/webhooks/paypal` | 🔒 Signature | PayPal IPN event handler (no user token, PayPal signature required) |
| `GET` | `/api/admin/me` | ✅ Admin | Verify admin identity |
| `GET` | `/api/admin/telemetry` | ✅ Admin | Fetch platform metrics |
| `POST` | `/api/upload-avatar` | ✅ Required | Upload user avatar to Cloudinary |
| `POST` | `/api/upload-image` | ✅ Required | Upload generated image asset to Cloudinary |
| `GET` | `/api/download` | ✅ Required | Generate and stream a ZIP of output content |

---

## 🔧 Environment Variables

Create a `.env.local` file in the project root with the following keys:

```bash
# ─── GEMINI AI ───────────────────────────────────────────────────────────────
# Comma-separated list of Gemini API keys (more keys = higher throughput)
GEMINI_API_KEYS="key1,key2,key3"

# ─── FIREBASE ────────────────────────────────────────────────────────────────
# Full Firebase Admin SDK service account JSON (single line, no newlines)
FIREBASE_SERVICE_ACCOUNT='{"type":"service_account","project_id":"..."}'

# Client-side Firebase config (safe to expose — rules enforced in Firestore)
NEXT_PUBLIC_FIREBASE_API_KEY="your_api_key"
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN="your-project.firebaseapp.com"
NEXT_PUBLIC_FIREBASE_PROJECT_ID="your-project-id"
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET="your-project.appspot.com"
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID="000000000000"
NEXT_PUBLIC_FIREBASE_APP_ID="1:000000000000:web:xxxxxxxxxxxx"

# ─── PAYPAL ──────────────────────────────────────────────────────────────────
NEXT_PUBLIC_PAYPAL_CLIENT_ID="your_paypal_client_id"
PAYPAL_CLIENT_SECRET="your_paypal_client_secret"
PAYPAL_MODE="live"                          # "sandbox" for testing
NEXT_PUBLIC_PAYPAL_MODE="live"
PAYPAL_WEBHOOK_ID="your_webhook_id"         # From PayPal Developer Dashboard

# PayPal Subscription Plan IDs (created via scripts/setup-paypal.mjs)
PAYPAL_PLAN_STARTER="P-xxx"
PAYPAL_PLAN_CREATOR="P-xxx"
PAYPAL_PLAN_PRO="P-xxx"
PAYPAL_PLAN_AGENCY="P-xxx"
PAYPAL_PLAN_LAUNCH_STARTER="P-xxx"
PAYPAL_PLAN_LAUNCH_CREATOR="P-xxx"
PAYPAL_PLAN_LAUNCH_PRO="P-xxx"
PAYPAL_PLAN_LAUNCH_AGENCY="P-xxx"

# ─── CLOUDINARY ──────────────────────────────────────────────────────────────
CLOUDINARY_CLOUD_NAME="your_cloud_name"
CLOUDINARY_API_KEY="your_api_key"
CLOUDINARY_API_SECRET="your_api_secret"

# ─── IMAGE GENERATION ────────────────────────────────────────────────────────
HUGGINGFACE_API_TOKEN="your_hf_token"
STABLE_HORDE_API_KEY="your_horde_key"      # Leave empty for anonymous (slower)

# ─── RESEND (Email) ──────────────────────────────────────────────────────────
RESEND_API_KEY="re_xxxxxxxxxxxx"
RESEND_FROM_EMAIL="hello@yourdomain.com"

# ─── APP ─────────────────────────────────────────────────────────────────────
NEXT_PUBLIC_APP_URL="https://your-domain.com"
ADMIN_EMAILS="admin@yourdomain.com,admin2@yourdomain.com"
```

> ⚠️ **Never commit `.env.local` to version control.** It is listed in `.gitignore` by default.

---

## 🚀 Getting Started (Local Dev)

### Prerequisites

- **Node.js** 20.x or later
- **npm** 10.x or later
- A Firebase project with **Firestore** and **Authentication** enabled
- A PayPal Developer account (sandbox for testing, live for production)
- At least one **Google Gemini API key** (get one free at [ai.google.dev](https://ai.google.dev))
- A **Cloudinary** account (free tier is sufficient for development)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/repurposeAI.git
cd repurposeAI

# 2. Install all dependencies
npm install

# 3. Set up environment variables
copy .env.local.example .env.local
# Open .env.local and fill in your credentials

# 4. (First time) Provision PayPal subscription plans
node scripts/setup-paypal.mjs

# 5. Deploy Firestore security rules
npx firebase deploy --only firestore:rules

# 6. Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Useful Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the Next.js development server with hot reload |
| `npm run build` | Compile and build the production bundle |
| `npm run start` | Start the production server (requires `build` first) |
| `npm run lint` | Run ESLint across the codebase |
| `npm run clean` | Clear the Next.js `.next` build cache |
| `node scripts/setup-paypal.mjs` | Create PayPal billing subscription plans via REST API |
| `firebase deploy --only firestore:rules` | Deploy updated Firestore security rules |

### Testing Payments Locally

For PayPal testing during local development, switch to sandbox mode:

```bash
PAYPAL_MODE="sandbox"
NEXT_PUBLIC_PAYPAL_MODE="sandbox"
NEXT_PUBLIC_PAYPAL_CLIENT_ID="your_sandbox_client_id"
PAYPAL_CLIENT_SECRET="your_sandbox_secret"
```

Use a [PayPal sandbox buyer account](https://developer.paypal.com/tools/sandbox/accounts/) to simulate payments. Webhook events can be tested using [PayPal's webhook simulator](https://developer.paypal.com/dashboard/webhooksSimulator).

---

## 🌐 Deployment

RepurposeAI is purpose-built for **Vercel** with zero additional server configuration required.

### Vercel Deployment Steps

1. Push your code to a GitHub repository.
2. Connect the repository to a new **Vercel project**.
3. Add all environment variables from `.env.local` to Vercel's **Environment Variables** panel (Settings → Environment Variables).
4. Set the **Framework Preset** to `Next.js` (auto-detected).
5. Click **Deploy**. Vercel handles builds and deploys automatically on every `git push` to `main`.

### Post-Deployment Checklist

- [ ] Set `NEXT_PUBLIC_APP_URL` to your production domain in Vercel env vars.
- [ ] Configure the PayPal **webhook URL** in the PayPal Developer Dashboard:
  ```
  https://your-domain.com/api/webhooks/paypal
  ```
- [ ] Copy the generated **Webhook ID** from PayPal and set it as `PAYPAL_WEBHOOK_ID` in Vercel.
- [ ] Deploy Firestore security rules:
  ```bash
  firebase deploy --only firestore:rules
  ```
- [ ] Verify admin dashboard is accessible at `/dashboard/admin` with an admin-listed email.
- [ ] Run a test generation job end-to-end to verify Gemini key rotation is working.
- [ ] Confirm Cloudinary image uploads are functional on `/dashboard/profile`.

### Custom Domain

Point your domain's DNS to Vercel (via A record or CNAME), then add it in **Vercel → Settings → Domains**. Vercel handles SSL provisioning automatically.

---

## 🗺 Roadmap

| Feature | Status | ETA |
|---|---|---|
| Core generation engine (6 formats) | ✅ Live | — |
| YouTube & web ingestion | ✅ Live | — |
| PDF / DOCX / TXT upload | ✅ Live | — |
| RSS feed ingestion | ✅ Live | — |
| PayPal subscriptions & PAYG | ✅ Live | — |
| Content history & ZIP export | ✅ Live | — |
| AI image generation (SDXL) | ✅ Live | — |
| Image canvas / editor | ✅ Live | — |
| Admin analytics dashboard | ✅ Live | — |
| User profile & avatar upload | ✅ Live | — |
| Standalone AI tools hub | ✅ Live | — |
| Transactional email (Resend) | ✅ Live | — |
| Automation workflows | 🔨 In Progress | Q2 2026 |
| MTN MoMo mobile payments | 🔨 In Progress | Q3 2026 |
| Zapier / Make.com integration | 📋 Planned | Q3 2026 |
| Bulk repurposing (batch mode) | 📋 Planned | Q3 2026 |
| Developer API (public REST) | 📋 Planned | Q4 2026 |
| Direct social publishing (Buffer/Hootsuite) | 📋 Planned | Q4 2026 |
| Team workspaces & collaboration | 📋 Planned | Q1 2027 |
| Mobile app (React Native) | 📋 Planned | 2027 |

---

## 📄 License

This is a **proprietary software project**. All rights reserved.  
Unauthorized copying, distribution, or modification of any part of this codebase is strictly prohibited without explicit written permission from the author.

---

<div align="center">

Built with ❤️ by **Nexus Intelligence Systems**  
© 2026 RepurposeAI. All rights reserved.

[🚀 Live App](https://repurposeai.nexusintelligencexystems.com) · [💰 Pricing](https://repurposeai.nexusintelligencexystems.com/pricing) · [🔒 Privacy Policy](https://repurposeai.nexusintelligencexystems.com/privacy) · [📋 Terms](https://repurposeai.nexusintelligencexystems.com/terms)

</div>
