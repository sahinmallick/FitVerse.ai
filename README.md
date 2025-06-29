

# 🧠 FitVerse AI – Your Voice-Powered Fitness Companion

Welcome to **FitVerse AI**, an intelligent, voice-first fitness assistant that adapts to your lifestyle. Just speak — and let AI take care of your personalized workout and meal plans. FitVerse AI helps you stay consistent, motivated, and in control of your fitness journey with a real-time, AI-powered backend built on [Convex](https://docs.convex.dev/).

---

## 🚀 Live Demo

👉 [fit-verse-ai.vercel.app](https://fit-verse-ai.vercel.app)

---

## 🌟 Highlights

* 🎙️ Voice-based onboarding & daily interaction powered by Vapi
* 🏋️‍♂️ Personalized workout and meal plans, updated weekly
* 📊 Daily chart tracking with Convex backend
* 📈 Dashboard with activity logs, plan history, and insights
* 🧠 Editable goals/preferences and AI plan regeneration
* ⚡ Responsive UI optimized for mobile and desktop

---

## 💡 Vision

Many fitness apps offer generalized routines that lack personalization and motivation. **FitVerse AI** solves this by combining **AI-driven personalization**, **voice interaction**, and **daily progress tracking** into one cohesive experience — empowering users to build healthier habits, consistently.

---

## 🧱 Tech Stack

| Component           | Technology                                  |
| ------------------- | ------------------------------------------- |
| Frontend            | Next.js (App Router), Tailwind CSS          |
| Authentication      | Clerk                                       |
| Backend & DB        | Convex                                      |
| AI & Voice Engine   | GPT / Gemini 2.0, Whisper, ElevenLabs, Vapi |
| Workflow Automation | Vapi AI, custom actions                     |
| Hosting             | Vercel                                      |

---

## 🔧 Setup & Installation Guide

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/fitverse-ai.git
cd fitverse-ai
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Setup Environment Variables

Create a `.env.local` file at the root:

```env
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_1234567890
CLERK_SECRET_KEY=sk_test_abcdefghij

# Convex Backend
NEXT_PUBLIC_CONVEX_URL=https://your-team.convex.cloud
CONVEX_DEPLOY_KEY=convex-deploy-key-here

# AI & Voice APIs
OPENAI_API_KEY=your_openai_or_gemini_key
NEXT_PUBLIC_ELEVENLABS_API_KEY=elevenlabs-api-key
VAPI_API_KEY=vapi-ai-api-key
```

---

### 4. Configure Convex Backend

```bash
npx convex init
npx convex dev
```

Make sure your project is linked to your Convex team.

---

### 5. Setup Clerk Authentication

Go to [Clerk.dev](https://clerk.dev):

* Create a new project
* Add web origin: `http://localhost:3000`
* Copy your Publishable & Secret keys to `.env.local`

---

### 6. Run Locally

```bash
npm run dev
```

Then open: [http://localhost:3000](http://localhost:3000)

---

### 7. Deploy to Vercel

1. Push your code to GitHub
2. Import the repo to [Vercel](https://vercel.com)
3. Add the same `.env.local` variables in Vercel’s dashboard
4. Deploy 🚀

---

## 📁 Project Structure

```
fitverse-ai/
├── app/                    # Next.js App Router pages
├── components/             # Reusable UI components
├── lib/                    # Convex, Clerk, AI logic
├── convex/                 # Convex backend
│   ├── _generated/         # Auto-generated server utils
│   └── functions/          # Core fitness logic
├── public/                 # Static files
├── styles/                 # Tailwind config
├── .env.local              # Environment variables
└── README.md
```

---

## 🛠️ Convex Backend Overview

### 🔹 Features

* 📊 Public Queries to fetch user fitness progress
* 🧠 Mutations to update daily stats, logs, and goals
* 🔐 Internal APIs for secure operations
* ⚡ HTTP Actions for webhooks or third-party integrations
* 📅 Supports both deterministic and non-deterministic logic

### 🔹 Convex File Structure

```
convex/
├── _generated/
│   └── server.js       # Auto-generated server utilities
├── functions/
│   ├── daily.ts        # Core logic for tracking workouts & meals
│   └── utils.ts        # Formatting and validation helpers
├── http.js             # Optional: HTTP endpoint router
├── convex.json         # Convex config
```

---

## 🔒 Security Guidelines

* Use `internalQuery`, `internalMutation`, and `internalAction` for server-only logic
* Sanitize all client inputs and validate schemas
* Never expose sensitive business logic to the frontend

---

## ✅ Key Features Delivered

* Voice-powered onboarding & goal setting
* AI-personalized fitness and meal plans
* Daily progress tracking & charting
* Plan history and dashboard insights
* Full profile customization
* Secure auth & scalable backend infrastructure

---

## 💬 Troubleshooting

* **Hydration error (Next.js):** Use `useEffect` for client-side only components
* **Vapi node error:** Ensure all nodes include valid `type`, `name`, and `metadata`
* **Convex access error:** Verify `CONVEX_DEPLOY_KEY` and project linking

---


## 💡 Pro Tip

To regenerate Convex types & bindings anytime, run:

```bash
npx convex dev
```

