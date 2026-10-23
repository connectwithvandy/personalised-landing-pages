# Clay Personalized Landing Pages — Project Brief

## What This Project Is
We are building **personalized landing pages for 5 warm prospects** who have requested a demo of Clay (clay.com). The goal is to maximize conversion by making each page feel like it was built specifically for that person and their company — not a generic sales page.

**Primary objective:** Get each prospect to book a demo call.

---

## Source Files
| File | Purpose |
|---|---|
| `landing-page-prospects.csv` | The 5 prospects — names, titles, companies, emails, LinkedIn URLs |
| `clay_icp.txt` | Clay's Ideal Customer Profile — buyer personas, pain points, fit signals |
| `clay_value_prop.txt` | Clay's value proposition — what it does, how it's different, stats, use cases |

---

## The 5 Prospects

| # | Name | Title | Company | Website |
|---|---|---|---|---|
| 1 | Sarah Mitchell | VP of Revenue Operations | Retool | retool.com |
| 2 | Marcus Chen | Head of Growth | Linear | linear.app |
| 3 | Emily Rodriguez | Director of Sales Development | Loom | loom.com |
| 4 | James Okonkwo | GTM Engineer | Webflow | webflow.com |
| 5 | Rachel Goldstein | VP of Sales | Airtable | airtable.com |

---

## Build Decisions (Locked In)

| Decision | Choice | Notes |
|---|---|---|
| **Format** | Static HTML/CSS files | One `.html` file per prospect. Self-contained, no dependencies, easy to host or share. |
| **Personalization depth** | Role-based messaging | Headlines, pain points, and value props tailored to their specific title — not just name/company swaps. Also incorporate company-specific context where possible. |
| **CTA** | Book a demo | Primary CTA button throughout. Link placeholder: `[YOUR_CALENDLY_LINK]` — swap this out when ready. |
| **Design style** | Clay brand + prospect company accent | Dark background, Clay's purple/teal gradient as primary. Prospect's company brand color used as a secondary accent. Elegant, modern SaaS aesthetic. |
| **Assets** | Placeholders for now | `[YOUR_CALENDLY_LINK]` used throughout. No video embed currently. |

---

## Design System (Use Consistently Across All Pages)

```css
--bg:           #08080E;       /* Page background */
--surface:      #0F0F1A;       /* Card/section background */
--border:       rgba(255,255,255,0.07);
--text:         #EEEEFF;       /* Primary text */
--text-muted:   #7878A0;       /* Secondary text */
--clay-purple:  #7B5FFF;       /* Clay brand purple */
--clay-teal:    #2EC4B6;       /* Clay brand teal */
--gradient:     linear-gradient(135deg, #7B5FFF 0%, #2EC4B6 100%);

/* Prospect accent colors (one per page): */
--retool-red:   #E8432D;       /* Retool */
--linear-purple: #5E6AD2;      /* Linear */
--loom-purple:  #625DF5;       /* Loom */
--webflow-blue: #4353FF;       /* Webflow */
--airtable-teal: #18BFFF;      /* Airtable */
```

**Font:** Inter (Google Fonts), weights 400/500/600/700/800/900

---

## Page Structure (Template for All 5 Pages)

Every page follows this section order:

1. **Nav** — Clay logo | "[Company]" badge with pulsing dot | "Book Demo →" CTA
2. **Hero** — Personalized headline with prospect's first name + company name. Role-specific subheadline. Two CTAs: "Book Your Demo →" and "See how Clay helps [Company] ↓"
3. **Logo bar** — "Trusted by…" strip with Clay's known customers (OpenAI, Anthropic, Ramp, Canva, Rippling, Notion, Vanta, Intercom)
4. **Problem section** — 4 cards. Pain points written specifically for their role + their company's buyer profile. Use the `clay_icp.txt` pain points as a base but make them specific.
5. **Solution section** — 4 Clay features mapped to their role's needs. Accompanied by a mock enrichment UI / visual on the right side.
6. **Stats band** — 3×, 80%, 150+, 4.9★ (Clay's real published numbers)
7. **Use cases** — 3 concrete workflows relevant to their role (numbered 01, 02, 03)
8. **Final CTA section** — Gradient-bordered card. "Book [First Name]'s Demo →" personalized button.
9. **Footer** — Clay logo | copyright + stats | "Made for [First Name] @ [Company]"

---

## Progress Tracker

| # | Prospect | Company | Status | File |
|---|---|---|---|---|
| 1 | Sarah Mitchell | Retool | ✅ **APPROVED & LOCKED** | `sarah-mitchell-retool.html` |
| 2 | Marcus Chen | Linear | ⏳ Not started | — |
| 3 | Emily Rodriguez | Loom | ⏳ Not started | — |
| 4 | James Okonkwo | Webflow | ⏳ Not started | — |
| 5 | Rachel Goldstein | Airtable | ⏳ Not started | — |

---

## Persona Messaging Guide

### 1. Sarah Mitchell — VP of Revenue Operations @ Retool
- **Angle:** Retool sells to technical buyers (engineers, devops, CTOs) who are nearly invisible in standard enrichment tools. RevOps pain is stale CRM data + fragmented stack + SDRs wasting time on research.
- **Key Clay value props for this persona:** Waterfall enrichment for hard-to-find technical personas, Claygent AI research, automated CRM hygiene, stack consolidation.
- **Company accent color:** `#E8432D` (Retool red)

### 2. Marcus Chen — Head of Growth @ Linear
- **Angle:** Linear is a developer tool with a fast-moving, PLG-leaning audience. Head of Growth cares about scalable outbound, intent signals, and personalization at scale without hiring more people.
- **Key Clay value props:** Intent-based outreach triggers, enrichment for developer ICPs, AI personalization at scale, speed-to-lead on inbound.
- **Company accent color:** `#5E6AD2` (Linear purple)

### 3. Emily Rodriguez — Director of Sales Development @ Loom
- **Angle:** SDR leader focused on rep productivity, pipeline coverage, and personalization quality. Pain is SDRs spending half their time on research instead of selling, low reply rates from generic outreach.
- **Key Clay value props:** Claygent AI briefings per prospect, 80% reduction in research time, personalized outreach at scale, waterfall email coverage.
- **Company accent color:** `#625DF5` (Loom purple)

### 4. James Okonkwo — GTM Engineer @ Webflow
- **Angle:** Highly technical persona. GTM Engineers want to build workflows, not click through UIs. They care about API access, waterfall logic, automation power, and integrations. Clay is literally a GTM development environment.
- **Key Clay value props:** No-code/code-friendly platform, 150+ integrations, workflow automation, waterfall enrichment logic, push to any CRM/sequencer.
- **Company accent color:** `#4353FF` (Webflow blue)

### 5. Rachel Goldstein — VP of Sales @ Airtable
- **Angle:** Owns pipeline targets and revenue. Cares about speed-to-lead, rep efficiency, forecast accuracy, and winning more deals faster. Pain is missing pipeline and reps not having the right context to close.
- **Key Clay value props:** Faster inbound routing, enriched prospect data for better conversations, CRM hygiene that reps actually trust, outbound scale.
- **Company accent color:** `#18BFFF` (Airtable teal/blue)

---

## Process for Remaining Pages

1. **Iterate on Sarah's page first** — get explicit approval from user before moving on
2. Build pages 2–5 using the locked design system and persona messaging guide above
3. Name files consistently: `[firstname]-[lastname]-[company].html`
4. Each page should feel completely bespoke — reference the company, the role, and the specific challenges that persona faces
5. Replace `[YOUR_CALENDLY_LINK]` across all pages once the user provides the link

---

## Key Constraints & Preferences
- **Do not build all at once** — user wants to see, iterate, and approve each page
- The design must feel **very elegant** — "modern SaaS vibes" was the explicit brief
- Personalization should maximize the chance of winning the account — think about what would make *that specific person* feel seen
- All files are standalone `.html` — no build step, no framework, no dependencies (except Google Fonts CDN)
