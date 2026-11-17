# Directory Layout

Create this in the user's chosen folder (ask where; default `./resume/`).

```
CLAUDE.md                  # optional: short project guide so future sessions follow the system
knowledge/
  profile/
    summary.md             # identity, contact, leadership philosophy, core competencies, career arc, differentiators
    honesty-rules.md       # the user's depth taxonomy + "never say" list (user-specific, see references/honesty-rules.md)
    open-questions.md      # running list of gaps to fill, with space for answers
  roles/
    [company]-[title-slug].md   # one file per job, newest first in your head, any order on disk
  job-targets/
    [company]-[role-slug].md        # the posting + Phase 1 analysis
    [company]-[role-slug]-prep.md   # interview prep
  resumes/
    [company]-[role-slug]-[YYYY-MM-DD].md   # generated, dated, never edited into the source
  templates/
    resume-template.md     # the user's formatting rules
```

## Rules
- One file per role. Never merge roles in the source.
- Resumes are write-once outputs; regenerate rather than hand-edit across versions.
- `CLAUDE.md` (if created) should state: purpose, structure, "tailor at generation time", key facts, and a pointer to `honesty-rules.md`. Keep it under ~60 lines.
- Regenerating the same resume on the same day: append `-v2`, `-v3` to the filename. Keep earlier versions.
- Job-target files: if the posting file already contains analysis, append a dated section instead of overwriting.
- Binary exports (docx/pdf) live next to the markdown they came from, same base name.
