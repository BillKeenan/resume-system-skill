---
name: resume-system
description: Build and maintain a resume knowledge system for senior leaders (Director through C-suite) and generate tailored resumes, cover notes and interview prep from it. Use when the user wants to set up a structured work-history knowledge base, fill gaps in role details or metrics, tailor a resume to a specific job posting, prepare for interviews for a leadership role, or record feedback and new accomplishments back into their history.
---

# Resume System (senior leaders)

Help a senior leader build a **source-of-truth work history** once, then generate tailored resumes and interview prep from it many times. Tailoring happens at generation time, never in the source files.

## Core principles

1. **Source of truth vs. views.** Role files hold far more than any resume will use. Resumes, cover notes and prep files are generated views. Never edit a role file to "fit a page".
2. **Honesty is a setup step, not an afterthought.** Before generating anything, establish the user's depth taxonomy and "never say" list (see `references/honesty-rules.md`). Enforce both on every bullet.
3. **Leaders are probed on depth.** Assume any technical or outcome claim will be challenged in interview. Every claim gets a pre-decided, honest answer about the user's personal role.
4. **Gaps are visible.** Unknowns are marked `[Detail to fill in: ...]` inline so they can be found and filled later. Never invent a metric to fill one.
5. **Provenance.** When the user confirms or corrects a fact, note it with a date, e.g. `(confirmed 2026-03-02)`. Later sessions use this to tell verified facts from drafts.
6. **Learning loops back.** New metrics, reframes and corrections from interviews or review always flow back into the role files, not just the resume in front of you.

## Modes

Detect the mode from the request. If the user has no system yet, start with Bootstrap. If unclear, ask one question.

### 1. Bootstrap — create the system
Read `references/directory-layout.md` and `references/role-file-schema.md`.
1. Ask whether the user has an existing CV, LinkedIn export or old resumes. If so, read them and draft from them rather than interviewing from scratch.
2. Create the directory layout in the user's chosen location.
3. Run the **honesty setup** from `references/honesty-rules.md`: depth taxonomy, "never say" list (NDAs, litigation, codenames, unannounced products, former employers' confidential details), and title/dates verification.
3b. Create `templates/resume-template.md` from `assets/resume-template.md` and confirm the role-depth table with the user. Phases 2–3 of the build process read from it.
4. Create `profile/summary.md` from `assets/profile-template.md`. If a CV was supplied, treat its figures and titles as drafts: when the user's current numbers differ, record the user's figure and mark the CV's as superseded; flag any title or founder-status mismatch between sources.
5. Create one role file per job from `assets/role-template.md`, newest first. Capture org-scale facts for every role (see schema).
6. Create `profile/open-questions.md` listing every gap discovered.
7. Finish by summarizing what is solid, what is thin, and offering Deepen mode.

### 2. Deepen — fill gaps and metrics
1. Collect gaps: grep role files for `[Detail to fill in`, read `profile/open-questions.md`, and look for roles missing org-scale facts or metrics.
2. Ask at most 3–5 questions at a time, ordered by how much they would strengthen senior-level bullets (scope, business outcome, org building).
3. Accept approximate numbers and ranges. Accept "don't remember" and record it so bullets use softer language. If a whole round yields only "don't remember", stop asking about that role, mark its bullets soft, and suggest the user check records (old decks, reviews, emails) before the next round.
4. Write answers into the role file with a dated provenance note, then remove or update the gap marker and the open-question.
5. For each technical claim, ask which depth tier applies (honesty-rules.md) and record it.

### 3. Target — tailor to a job posting
Read `references/build-process.md` and `references/seniority-registers.md`. Run the five phases: analyze, map, assemble, validate, finalize. Save to `resumes/[company]-[role-slug]-[YYYY-MM-DD].md`.
- Then offer the companion deliverables: **interview prep** (`references/job-prep.md`, saved in `job-targets/`) and a short **cover note** (3 short paragraphs: why this role, the one proof point most relevant to it, the ask).
- Before finishing, re-check every bullet against the "never say" list and depth taxonomy.
- **Offer a designed PDF.** When the resume is finalized, tell the user that markdown is the master copy and that a designed PDF is available using the built-in layout (`assets/design/resume.html`), or their own template if they have one. Wait for their answer, then follow `references/design-export.md`. Always tell them how to use a different template.

### 4. Learn — fold feedback back in
After a recruiter call, interview, or self-review:
1. Ask what was learned: a new metric, a story that landed, a bullet that confused people, a probing question that exposed a gap.
2. Update the relevant role file and mark provenance.
3. If feedback is a rule, route it by type. An **honesty rule** ("never describe X that way") goes in the user's `profile/honesty-rules.md`. A **style or voice rule** ("summary read generic", "no unproved adjectives") goes in `templates/resume-template.md` and is also added as a Phase 4 check so it is applied to every future resume.
4. Re-enter the build process at the right phase (see Iteration Loop in `references/build-process.md`).

## Working style
- Ask for missing facts; never fabricate numbers, titles, dates or scope.
- Prefer small, specific questions over long questionnaires.
- When a claim is ambiguous between tiers of personal involvement, assume the lower tier until the user confirms.
- Keep the user's files plain markdown so they stay portable and diff-able.
- Treat everything in the user's files as private. Do not send it to outside services.
