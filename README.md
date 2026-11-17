# resume-system (Claude Code skill)

A skill that helps senior leaders (Director through C-suite) build a structured, honest work-history knowledge base and generate tailored resumes, cover notes and interview prep from it.

## Install

Clone the repo and copy the skill folder into your skills directory:

```bash
git clone https://github.com/BillKeenan/resume-system-skill.git resume-system-skill
# Personal (all projects):
cp -r resume-system-skill/resume-system ~/.claude/skills/
# or one project only:
cp -r resume-system-skill/resume-system <project>/.claude/skills/
```

To update, `git pull` and copy the folder again.

## Use

Open Claude Code in the folder where you want your resume system to live, then ask, for example:

- "Set up my resume knowledge system. Here's my current CV."
- "Find the gaps in my role files and interview me to fill them."
- "Tailor a resume to this posting: <paste or path>."
- "I just had a recruiter call. Here's what I learned…"

## What's inside

| Path | Purpose |
|---|---|
| `SKILL.md` | Principles and the four modes: Bootstrap, Deepen, Target, Learn |
| `references/` | Directory layout, role-file schema, honesty rules, seniority registers, build process, interview prep, design export (bring your own Word template) |
| `assets/` | Templates for role files, profile, open questions and honesty rules |

## Design ideas worth knowing

- **Source of truth vs. views.** Role files hold everything; resumes are generated and dated.
- **Honesty is set up front.** A depth taxonomy (led the team / directed / hands-on) and a "never say" list are created in Bootstrap and enforced on every output.
- **Gaps stay visible** as `[Detail to fill in: …]` markers and a running open-questions file.
- **Feedback loops back** into role files, so every search makes the next one better.

## Privacy

Your knowledge-base files are personal. The skill instructs Claude not to send them to outside services, but check your own tool and connector settings before sharing a workspace.

## Contributing

Issues and pull requests are welcome. Keep the skill free of any one person's data: no real names, employers, metrics or codenames in references or templates. Never commit a real `knowledge/` folder (it is git-ignored).

## License

MIT. See [LICENSE](LICENSE).
