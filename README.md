# 🐝 RateBee
**Scan. Speak. Rate.** Smart feedback for local businesses: customers scan a QR/NFC stand, pick a rating, and get AI-drafted Google review suggestions they can edit and post in one tap.

![Next.js](https://img.shields.io/badge/Next.js-15-black) ![TypeScript](https://img.shields.io/badge/TypeScript-5-blue) ![Supabase](https://img.shields.io/badge/Supabase-Postgres-green) ![License](https://img.shields.io/badge/license-MIT-yellow)

<!-- screenshots: docs/feedback-flow.png, docs/dashboard.png -->

## Features
- Login-free mobile feedback flow (rating, tags, optional note)
- 3 natural AI drafts, editable, copy + open Google
- Multi-tenant shops, per-location QR codes with short links
- Owner dashboard: scans, completions, conversion, average rating, themes
- Branding: logo, colors, tags, thank-you message
- Swappable AI provider (Anthropic / OpenAI)

## Responsible use
RateBee **does not gate reviews** (every rating goes to Google), **does not offer incentives for Google reviews**, and drafts only reflect what the customer selected or wrote. This keeps shops within Google's review policies.

## Tech stack
Next.js 15 (App Router), TypeScript, Tailwind, shadcn/ui, Framer Motion, Supabase (Postgres/Auth/Storage), Zod, `qrcode`, Vercel.

## Setup
```bash
git clone https://github.com/<you>/ratebee && cd ratebee
npm install
cp .env.example .env.local     # fill in values
# run supabase/schema.sql in the Supabase SQL editor
npm run dev
```

## Environment variables
See `.env.example`. `SUPABASE_SERVICE_ROLE_KEY` is server-only.

## Roadmap
Voice input, Google Business Profile API, multi-language, NFC, staff stats, rewards, white-label.

## Contributing
Fork, branch (`feat/...`), run `npm run lint && npm test`, open a PR with a clear description.

## License
MIT
