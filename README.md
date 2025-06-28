# 🏋️‍♂️ Fitness App - Daily Chart Backend (Convex)

This is the backend implementation for a **Fitness App Daily Chart Provider**, built using [Convex](https://docs.convex.dev/). It powers features like workout tracking, daily progress charts, and nutrition logs.

> ⚙️ Includes auto-generated utility file: `convex/_generated/server.js`.

---

## 📌 Features

- 🌐 Public Queries to fetch user fitness data.
- 🧠 Mutations to update logs, goals, and stats.
- 🔐 Internal APIs for secure server-only logic.
- ⚡ HTTP Actions for webhooks, reminders, or 3rd-party integrations.
- 🛠️ Supports both deterministic and non-deterministic logic with actions.

---

## 📁 Project Structure

```md

convex/
├── \_generated/
│   └── server.js     # Convex utility exports
├── functions/
│   ├── daily.ts      # Core logic for tracking daily workouts
│   └── utils.ts      # Helper functions for formatting, validation, etc.
├── http.js           # Optional: HTTP endpoint router
├── convex.json       # Convex config

````

---

## 🚀 Getting Started

### 1. Install dependencies

```bash
npm install convex
````

### 2. Initialize Convex

```bash
npx convex init
```

### 3. Start Dev Server

```bash
npx convex dev
```

---

## 🧩 Auto-Generated Server Utility

File: `convex/_generated/server.js`

```ts
/* eslint-disable */
/**
 * Generated utilities for implementing server-side Convex query and mutation functions.
 *
 * THIS CODE IS AUTOMATICALLY GENERATED.
 * To regenerate, run `npx convex dev`.
 * @module
 */

import {
  actionGeneric,
  httpActionGeneric,
  queryGeneric,
  mutationGeneric,
  internalActionGeneric,
  internalMutationGeneric,
  internalQueryGeneric,
} from "convex/server";

export const query = queryGeneric;
export const internalQuery = internalQueryGeneric;
export const mutation = mutationGeneric;
export const internalMutation = internalMutationGeneric;
export const action = actionGeneric;
export const internalAction = internalActionGeneric;
export const httpAction = httpActionGeneric;
```

---

## 🔒 Security Guidelines

* Only expose what's necessary to the client.
* Use `internalQuery`, `internalMutation`, and `internalAction` for sensitive logic.
* Sanitize all client inputs and validate schemas.

---

## 👨‍💻 Author

**Monish Mondal**
Convex Enthusiast | Full-stack Developer
📫 Let's connect!

---

## 📄 License

MIT License. Free to use, fork, and modify.

---

## 💡 Pro Tip

Regenerate all types and bindings anytime using:

```bash
npx convex dev
```
