# Personalised Landing Pages

One landing page per prospect, built for that person and their company, not a generic sales page.

I built this during GrowthX Cohort 4. The brief: five warm prospects had asked for a demo of Clay. Make each one a page that feels like it was written just for them, so they book the call.

## How it works

Claude reads three inputs: the prospect list, Clay's ideal customer profile, and Clay's value proposition. For each prospect it works out their role, what their company is likely struggling with, and which part of Clay matters most to them. Then it writes and builds a page around that. Each page is deployed on its own link on Vercel (a hosting service for websites).

## What's in here

* `landing-page-prospects.csv`: the five prospects. The names are fictional and the emails and LinkedIn links are placeholders.
* `clay_icp.txt` and `clay_value_prop.txt`: the context Claude used.
* `*.html`: the five finished pages, one per prospect.
* `CLAUDE.md`: the brief Claude worked from.

Built by [Vandana Agarwal Nik](https://vandanaagarwal.in), with Claude.
