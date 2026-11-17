# Design Export (bring your own template)

Markdown is the canonical deliverable. To produce a designed `.docx` or `.pdf`, export the finished markdown into a template the **user supplies**. This skill does not bundle any design template.

## Where to get a template
Any one-column Word resume template works. One example the skill was developed with is the free **Connery** template from Resume Genius, available in several colors: <https://resumegenius.com/resume-templates/basic>. Check the source's terms before reuse, and do not redistribute third-party templates in this repo or in the user's shared files.

## Before exporting
1. Ask the user for the template file and where it lives. Save a copy under `templates/design/` in their own knowledge base (not in the skill repo).
2. Check the fonts. Many templates need specific fonts installed (e.g. Poppins and Roboto Slab for Connery); without them the layout breaks. Tell the user to install them and restart Word.
3. Finish and validate the markdown resume first. Never export a draft that hasn't passed Phase 4.

## Mapping markdown to template slots
Identify the template's placeholders and map each:

| Resume part | Template slot |
|---|---|
| Name, contact line, LinkedIn | Header block |
| Summary (3–4 lines) | Profile / summary section |
| Core competencies | Skills section (one line, if the template has room) |
| Role heading: title, company, dates | Job header line |
| Company context sentence | Subheading under the job header |
| Bullets | List style in the template (reuse it; don't add new bullet formatting) |
| Patents, education | Closing sections |

## Export rules
- **Reuse the template's own styles.** Edit text inside existing paragraphs and list styles; don't override fonts, sizes or spacing.
- **Two pages max.** Render to PDF and check page count. If over, apply the page-fit cut order from `templates/resume-template.md`, regenerate the markdown, then re-export. Don't shrink fonts to fit.
- **Remove unused placeholder sections** (empty skills boxes, sample text) instead of leaving them.
- **Name outputs** to match the markdown: `resumes/[company]-[role-slug]-[YYYY-MM-DD]-[template].docx` and `.pdf`.
- **Re-run the never-say scan** on the exported file's text, including headers, footers and document properties (author, title, comments).
- **Check the result visually** (convert to PDF and look at the pages) before reporting it done.

## Tooling
Use whatever Word/PDF tooling the environment offers (for example a docx skill, python-docx, or LibreOffice for PDF conversion). Prefer editing the template's XML or document model over generating a new file, so the design is preserved.
