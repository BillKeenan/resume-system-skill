# Honesty Rules (set up in Bootstrap, enforced everywhere)

Senior leaders get probed: "Did you do that, or did your team?" Set the answers in advance.

## 1. Depth taxonomy

Define three tiers with the user, using examples from their own history, and store the result in `knowledge/profile/honesty-rules.md`. Default definitions:

| Tier | Meaning | Safe phrasing |
|---|---|---|
| **1. Led the team** | The deliverable was the team's work product. The user managed people and was accountable for outcomes but did not set the technical or design direction personally. | "Led the team that delivered…", "Accountable for…", "Managed teams responsible for…" |
| **2. Directed** | The user made architecture- or strategy-level calls and set direction. The team owned detailed design and implementation. | "Set direction for…", "Drove the architecture decision to…", "Directed…" |
| **3. Hands-on** | The user personally designed, built or authored it. Typical for founder-era or small-team roles. | "Built…", "Designed and implemented…" |

For every technical or "owned" claim, ask which tier applies. **Default to Tier 1 until the user confirms otherwise.** Overclaiming happens in both directions: from Tier 1 to 2 (drafting "led the technical design" when it was people management) and from 2 to 3. Each correction is worth recording with a date.

**Participated/coordinated (between tiers 1 and 2):** the user contributed to or coordinated others' design work without setting direction (for example, "party to the design", or a guild where staff decide and the user provides structure). Safe phrasing: "participated in", "coordinated teams to adopt", "established the forum where…". Never "designed", "architected" or "led the design".

**When honesty and register conflict, honesty wins.** If the only truthful verb is "contributed to" or "helped", use it, or restructure the bullet around the part the user did own.

Tool and technology names appear in role files labeled by tier. They appear in a resume's skills or competencies section **only** if the user has personal working knowledge (Tier 3), not because their team used them.

**Disciplines vs. tools:** a discipline (e.g. "event-driven systems") may appear in competencies only in leadership phrasing that matches the tier ("event-driven systems leadership", "cross-team technical coordination"). Tool names require Tier 3.

## 2. Pivot lines
For each technical story in interview prep, write a short, confident redirect for when a question moves from decision-level to implementation-level, for example: "I set the direction and made the call; the team owned the detailed design. Here's how I evaluated the tradeoffs…" It should read as honest scoping, never as a dodge.

## 3. "Never say" list
Ask during Bootstrap and store in the user's `honesty-rules.md`:
- Internal project codenames that must not appear externally
- Litigation, regulatory matters, or settlements
- NDA-covered clients, partners or unreleased products
- Confidential financials (use ranges or directional language instead)
- Sensitive personnel matters (terminations, performance cases)
- Anything the user simply prefers not to publish

**Scanning:** build the scan list from this file's never-say entries and scan every shareable output (resume, cover note, prep file, job-target notes). Exclude `honesty-rules.md` itself from the scan, and never quote it in other files.

When a "never say" item is relevant to a role, refer to it generically (or omit it) and **ask before including anything litigation- or NDA-adjacent**, even if the codename is avoided.

## 4. Fact verification
- Titles, dates and reporting lines: confirm each with the user once, and mark them confirmed.
- Never round up headcount, revenue or percentages. Use the user's stated figure or range.
- If a number came from an inference rather than the user, flag it and ask.
- **CV figures are drafts.** When a CV and the user disagree, record the user's figure, mark the CV's as superseded (with date), and flag any title or founder-status mismatch between sources. Resolve before use, or leave the claim out.
- **Confirmed is not the same as meaningful.** For each metric, confirm the unit, scale and baseline (an "NPS from 2.8 to 4.2" with no scale is unusable). Omit metrics that can't be defined.
- **Check status today.** Ask whether the outcome was later reversed or ended (product shut down, org dissolved, partnership lapsed) before using it as proof, and record the answer in the role file.

## 5. Before delivering any output
Scan every bullet for: tier overclaims, "never say" terms, unconfirmed numbers, and verbs like "owned/architected/designed" attached to Tier 1 work.
