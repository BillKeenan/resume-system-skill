# Build Process: Job Posting → Finished Resume

Five phases. Each produces an artifact that feeds the next. Do not skip Phase 1.

## Phase 1 — Posting analysis
Save the posting to `job-targets/[company]-[role-slug].md` (if the file already has analysis, append a dated section rather than overwriting), then write a short brief:
1. **Role classification:** Director, VP, SVP or C-level (or ambiguous). Sets bullet depth and register (`seniority-registers.md`).
2. **Primary emphasis axis — pick ONE:**
   - Scale & organizational complexity
   - Transformation & turnaround
   - Commercial & product partnership (revenue, P&L, cross-functional influence)
   - Technical credibility (platform, architecture, a specific domain)
3. **Key phrases to mirror:** exact language from the posting: title register, domain terms, cultural signals.
4. **Gaps/risks:** what the posting asks for that the history covers thinly. Decide per gap: reframe with adjacent experience, or de-emphasize. Never fabricate.

## Phase 2 — Map the knowledge base
Read `profile/summary.md`, `profile/honesty-rules.md` and relevant role files.
- **Lead role:** usually the most recent and largest. Exception: when the posting is domain-specific and an earlier role is the better match.
- **Tier-rank accomplishments:** Tier 1 mirrors a stated requirement (lead with it); Tier 2 supports the primary axis (include if space); Tier 3 is generic (omit or condense).
- **Role depth:** set a bullet budget per role, decreasing with age and relevance. A typical starting point: current role 4–6, previous 4–6, then 3–4, then 2–3, then 1–2, with early-career roles omitted or one line. Store the user's own table in `templates/resume-template.md`.
- **Page fit:** project length now. Plan consolidation (e.g. merge early founder roles into one line) before drafting.

## Phase 3 — Assemble
Read `templates/resume-template.md` first.
- **Summary (3–4 lines):** line 1 mirrors the posting's title language; line 2 is ONE differentiator matching the primary axis; lines 3–4 give the value proposition in the company's vocabulary.
- **Core competencies:** only for larger companies likely to use ATS screening. 6–10 terms mirroring posting language, restricted to skills the user personally holds (honesty-rules §1).
- **Bullets:** formula `[Action verb] + [what] + [resulting in] + [quantified outcome]`. Three tests: strong specific verb; quantified outcome or scale signal; answers "so what" in business terms.
- Apply the depth tier to every verb.

## Phase 4 — Validate
1. **Signal mirror:** every key phrase from Phase 1 appears, or exclusion is a conscious decision.
2. **Metric density:** each senior role has ≥2 bullets with hard numbers or directional scale.
3. **Register check:** does each bullet sound like the target level? Flag tool-centric bullets and "helped/assisted/contributed to".
4. **Page fit:** over two pages? Cut in order: consolidate early roles, trim middle-role bullets by one, remove core competencies.
5. **Honesty check:** tier overclaims, never-say terms (scan every shareable output, see `honesty-rules.md` §3), unconfirmed or undefined numbers, and outcomes since reversed (§4).
6. **User style rules:** apply every style or voice rule recorded in `templates/resume-template.md` (e.g. "no unproved adjectives"), including ones added by Learn mode.

Output a list of failing bullets with proposed fixes.

## Phase 5 — Finalize
Apply fixes, then do a final pass:
- Does the summary read as written for *this* job?
- Is the career arc legible and building toward this role?
- Any redundant bullets across roles?

Save as `resumes/[company]-[role-slug]-[YYYY-MM-DD].md`. Offer a cover note and interview prep (`job-prep.md`).

## Iteration loop
After feedback, re-enter at:
- **Phase 2** if the issue is content selection (wrong emphasis, missing signal)
- **Phase 3** if it is specific bullets or the summary
- **Phase 4** if it is tone or register

Always write any new metric, accomplishment or reframe back into the role files.
