# ReturnsBough

**Understand why products come back.**

AI product returns analytics software that analyzes customer-reported return reasons to identify recurring product, sizing and fulfilment issues.

Marketing website and interactive product demonstration for ReturnsBough.

- Industry: Ecommerce, Retail, Machine Learning
- Founder: Chukwuebuka Eze (Founder & CEO)
- Co-founder: Halimat Yusuf (Co-founder & CTO)
- Contact: chukwuebuka@returnsbough.top
- Business model: Transaction-volume subscriptions

## Stack

Vite · React 19 · TypeScript · Tailwind CSS v4 · React Router · Lucide React · Recharts.

No API keys or backend are needed. The workspace demo runs on seeded mock data kept in the browser (localStorage), and `npm test` runs the Vitest unit tests.

## Getting started

```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # type-check and build into dist/
npm run preview    # serve the production build
npm test           # unit tests
```

Requires Node 20 or later.

## Routes

| Route | Page |
| --- | --- |
| `/` | Home — problem, solution, features, workflow, AWS, safeguards, customers, MVP, pricing, team, roadmap, FAQ |
| `/product` | Core features in detail |
| `/how-it-works` | Step-by-step workflow |
| `/use-cases` | Online retailers, Apparel brands, Fulfilment companies |
| `/technology` | How ReturnsBough uses AWS (Bedrock, SageMaker AI, S3, DynamoDB, Lambda) |
| `/security` | Safeguards and data handling |
| `/pricing` | Transaction-volume subscriptions (illustrative) |
| `/about` | Story, principles and team |
| `/contact` | Contact and demo request (`?type=demo`) |
| `/privacy`, `/terms` | Legal drafts |
| `/workspace/*` | Interactive demo: Returns workspace |

## Editing content

Everything — copy, founders, pricing, AWS services, theme colours and fonts, and the workspace data model — lives in `src/config/business.ts`. After changing the theme there, regenerate `src/theme.css` with the values shown in that file (or edit `src/theme.css` directly).

## Deploying

`npm run build` produces a static site in `dist/`. `vercel.json` (Vercel) and `public/_redirects` + `public/_headers` (Netlify / Cloudflare Pages) set the SPA fallback, security headers and caching.

The proposed AWS architecture is described in `docs/architecture.md`.

### Before launch

- Pricing, roadmap, FAQ, privacy notice and terms are drafts.
- The workspace uses fictional demo data; the organisation and people in it are not real.
