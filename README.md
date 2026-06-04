# 🌾 AI Kisan Mitra — Multilingual AI Assistant for Indian Farmers

> A voice-first, multimodal AI agent helping Indian farmers with crop disease diagnosis, live mandi prices, government scheme discovery, and regional agri-alerts — all in their native language.

🔗 **Live Demo:** [ai-kisan-mitra-new.vercel.app](https://ai-kisan-mitra-new.vercel.app)
📦 **Repo:** [github.com/DeepakLakeshar/AI-Kisan-Mitra-NEW](https://github.com/DeepakLakeshar/AI-Kisan-Mitra-NEW)

---

## 💡 Problem We're Solving

| Problem | Our Solution |
|---|---|
| Raw mandi data isn't actionable | AI-summarized trends with charts |
| Language barriers for farmers | Voice-first multilingual interface |
| Scattered information sources | Unified agri-intelligence dashboard |
| Disease identification without experts | Image + voice based Gemini diagnosis |

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🎙️ Voice Chat | Gemini-powered live chat in native Indian languages |
| 🌿 Crop Disease Diagnosis | Upload a crop photo or describe symptoms via voice |
| 📈 Mandi Prices | Real-time and historical trends via data.gov.in APIs |
| 📍 Market Comparisons | Cross-district and cross-state price analysis |
| 🧾 Scheme Discovery | Government subsidy finder with AI summaries |
| 🗓️ Crop Calendar | Contextual sowing and harvesting suggestions |
| 📰 Region Alerts | Soil, weather, and agri-news updates |
| 🔐 Authentication | Secure login via Clerk |
| 🧪 Soil Quality *(Planned)* | pH and nutrient analysis assistant |

---

## 🔁 User Flow

```
📤 Upload crop image OR describe symptoms by voice in native language
        ↓
🧠 Google Gemini processes audio + image
        ↓
🌿 Diagnoses disease        📊 Shows mandi price trends        💰 Summarizes govt schemes
        ↓
🗣️ Returns voice + text output with interactive Recharts visualizations
```

---

## 🧱 Tech Stack

| Technology | Purpose |
|---|---|
| **Next.js 15** (Turbopack) | App framework with App Router |
| **TypeScript** | Type-safe codebase |
| **Tailwind CSS v4** | Utility-first styling |
| **@google/genai** | Google Gemini API (multimodal AI) |
| **Clerk** | Authentication and user management |
| **Recharts** | Interactive mandi price charts |
| **Framer Motion** | UI animations |
| **react-markdown + remark-gfm** | Rendered AI markdown responses |
| **data.gov.in APIs** | Real-time and historical mandi price data |
| **Vercel** | Deployment and edge functions |

---

## 🧩 Folder Structure

```
/public          # Static assets
/src
  /app           # Next.js App Router pages and layouts
  /components    # Reusable UI components
  /lib           # Helper utilities (API calls, chart helpers, TTS)
.env.example     # Environment variable template
vercel.json      # Vercel deployment config
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/DeepakLakeshar/AI-Kisan-Mitra-NEW.git
cd AI-Kisan-Mitra-NEW
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

Requires **Node.js 20.x**.

### 3. Set Up Environment Variables

```bash
cp .env.example .env.local
```

Fill in your keys in `.env.local`:

```env
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_your_key_here
CLERK_SECRET_KEY=sk_test_your_key_here

# Google Gemini (server-side only — never expose to browser)
GEMINI_API_KEY=your_gemini_api_key_here

# Mandi Price APIs — data.gov.in
MANDI_API_KEY=your_data_gov_in_api_key_here
HISTORICAL_MANDI_API_URL=https://api.data.gov.in/resource/9ef84268-d588-465a-a308-a864a43d0070
TODAY_MANDI_API_URL=https://api.data.gov.in/resource/35985678-0d79-46b4-9ed6-6f13308a1d24

# Public variants (for client-side mandi fetch if needed)
NEXT_PUBLIC_MANDI_API_KEY=your_data_gov_in_api_key_here
NEXT_PUBLIC_HISTORICAL_MANDI_API_URL=https://api.data.gov.in/resource/9ef84268-d588-465a-a308-a864a43d0070
NEXT_PUBLIC_TODAY_MANDI_API_URL=https://api.data.gov.in/resource/35985678-0d79-46b4-9ed6-6f13308a1d24
```

> ⚠️ `GEMINI_API_KEY` is intentionally server-only (no `NEXT_PUBLIC_` prefix) to keep it secure.

### 4. Run the Dev Server

```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000)

---

## 🔑 API Keys You'll Need

| Key | Where to Get |
|---|---|
| `GEMINI_API_KEY` | [aistudio.google.com](https://aistudio.google.com) |
| `MANDI_API_KEY` | [data.gov.in](https://data.gov.in) — register and request API access |
| Clerk Keys | [clerk.com](https://clerk.com) — create a new application |

For detailed Clerk setup, see [CLERK_SETUP.md](./CLERK_SETUP.md).

---

## 🚢 Deployment

The project is configured for **Vercel** deployment out of the box via `vercel.json`.

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

Add all environment variables from `.env.local` to your Vercel project's Environment Variables settings before deploying.

---

## 🧪 Planned Enhancements

- Soil quality analysis from sensor or API data
- Location context for hyper-local mandi prices
- Weather context integration
- Offline voice support for low-connectivity areas

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE).

---

## 📬 Contact

**Project Lead:** Deepak Lakeshar
**GitHub:** [github.com/DeepakLakeshar](https://github.com/DeepakLakeshar)
**Live App:** [ai-kisan-mitra-new.vercel.app](https://ai-kisan-mitra-new.vercel.app)

---

> Built with ❤️ by **Aura Grow Team** — empowering Indian farmers with AI.
