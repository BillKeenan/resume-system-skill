# Role File Schema

A role file is the source of truth for one position. Include **more** detail than will ever appear on a resume. Use `assets/role-template.md` as the starting point.

## Required sections

1. **Header** — title, company, dates (month + year), location, reporting line.
2. **Scope (org-scale facts)** — the facts senior-level validation depends on:
   - Total headcount in scope, and how it changed from start to end
   - Direct reports, and leaders-of-leaders vs. ICs
   - Geographies and time zones
   - Budget, P&L or revenue responsibility (ranges are fine)
   - Number of products, business units or platforms owned
   - Key cross-functional partners (product, business, finance, security, legal)
3. **Context** — what state the org/product was in when the user arrived and why they were hired. Turnaround, growth, merger, new market? This is what makes accomplishments meaningful.
4. **Accomplishments** — one block each, structured as:
   - **What** (the action, in plain words)
   - **Why it mattered** (business or organizational problem)
   - **Result** (metric, direction of change, or scale signal)
   - **Depth tier** (see `honesty-rules.md`) and a confidence note
   - **Cross-functional footprint** (who had to be influenced or coordinated)
   - **Status today** (ongoing / ended / reversed). A product that was later shut down is a risk to feature as proof.
5. **Org-building and people** — hiring (volume, time-to-hire, roles closed), career ladders, attrition, promotions, leaders developed, org-model changes.
6. **Tech and domain** — stack and domain terms, labeled by depth tier. Keep separate from accomplishments so it never reads as a personal-skills claim by accident.
7. **Challenges overcome** — hard calls, conflicts, failures and recoveries. These feed interview stories.
8. **Not for external use** — items under confidentiality, litigation, NDAs, or sensitive personnel matters. Reference the "never say" list.

## Conventions
- Mark unknowns inline: `[Detail to fill in: what specifically is missing]`.
- Date provenance: `(confirmed 2026-03-02)` after any fact the user verified or corrected.
- Prefer ranges and approximations over fabricated precision: "~150 staff (130–180)".
- Record "don't remember" explicitly so bullets use softer language.
- Never include a metric the user hasn't stated or approved.
