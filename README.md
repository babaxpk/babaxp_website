# BABAXPK Website

Official website for **BABAXPK (OPC) Private Limited** — an Indian aerospace and unmanned-systems enterprise.

## Tech Stack
- **Next.js 16** (App Router)
- **TypeScript** (strict mode)
- **Tailwind CSS v4**
- **Zod** for form validation

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Production build (runs opportunity validation first) |
| `npm run start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | TypeScript type check |
| `npm run validate:opportunities` | Validate all 480 opportunity records |
| `npm run validate:content` | Validate all content files |

## Project Structure

```
babaxpk-website/
├── app/                    # Next.js App Router pages
│   ├── company/            # Company pages
│   ├── products/           # Product pages (KAVALE-ISR, MARUTYA)
│   ├── capabilities/       # Capability pages
│   ├── opportunities/      # 480 opportunity catalogue
│   ├── industries/         # Industry pages
│   ├── investors/          # Investor section
│   ├── partners/           # Partner section
│   ├── research/           # Research pages
│   ├── insights/           # Blog/insights
│   ├── contact/            # Contact forms
│   ├── legal/              # Legal pages
│   └── api/                # API routes
├── components/
│   ├── layout/             # Navigation, Footer
│   └── ui/                 # Reusable components
├── content/
│   └── opportunities/      # business-opportunities.json (480 entries)
├── lib/                    # Utility functions and data
├── types/                  # TypeScript type definitions
└── scripts/                # Build validation scripts
```

## Adding Content

### Adding an Opportunity
Edit `content/opportunities/business-opportunities.json`. The build validates exactly 480 records with unique IDs and slugs.

### Adding a Product
Create a new page in `app/products/[product-name]/page.tsx`.

### Adding an Insight Article
Create `app/insights/[slug]/page.tsx`.

## Deployment

Deploy to Vercel (recommended):
```bash
npx vercel
```

Or build for any Node.js host:
```bash
npm run build
npm run start
```

## Contact & Legal
- **Email:** babaxpk.com@gmail.com
- **Phone:** +91 91870 27143
- **CIN:** U26515KA2025OPC212557
- **Location:** Bengaluru, Karnataka, India

## Claim Status System
All products and opportunities use a mandatory claim-status system:
- **Verified Capability** — confirmed active capability
- **In Development** — active development
- **Concept / R&D** — research/engineering evaluation (current product status)
- **Future Opportunity** — default for all 480 catalogue entries
- **Partnership Opportunity** — entry through collaboration
- **Supply or Trading Opportunity** — sourcing/distribution activities
- **Regulatory Review Required** — needs regulatory approval

## Important Disclaimers
Both current products (KAVALE-ISR and MARUTYA) are in **Concept / R&D** stage.
No products are commercially available. All specifications are development targets.
