# Design Export

Markdown is the master copy of every resume. A designed PDF is a view of it. The skill ships one built-in design, `assets/design/resume.html`: a one-column, two-page print layout with a dated left rail, so the career arc can be scanned down the page. `assets/design/preview.png` shows what it looks like.

## Offer flow
When a resume passes Phase 4, say something like:

> "Your resume is ready in markdown. Want a designed PDF too? I can put it into the built-in layout, or into a template of your own if you have one."

Wait for the user's answer. Don't export unasked.

## Using the built-in design
1. Copy `assets/design/resume.html` to `resumes/[company]-[role-slug]-[YYYY-MM-DD].html` (same base name as the markdown).
2. Replace the sample content with the finished resume, keeping every class name and the tag structure. Edit only the content, not the CSS. If the user wants a different look (accent colour, fonts), change the `:root` tokens only.
3. Mapping:

   | Resume part | Where it goes |
   |---|---|
   | Name | `h1` in the masthead |
   | Target-role title line | `.tagline` |
   | Contact details | `.contact` list items |
   | Summary | `.summary` paragraph |
   | Core competencies | `.competencies` list (delete the section if not used) |
   | A full role | one `.role` article: dates and city in `.when`, title in `h3`, company in `.company`, one-line context in `.context`, bullets in the `ul` |
   | Earlier, condensed roles | `.entry.compact`, one line each |
   | Patents, education | `.entry` rows |

4. Delete any section the resume doesn't use, and any sample text left over.
5. Produce the PDF (see below), then check it.

## Producing the PDF
- **Headless tool available** (Chrome/Chromium `--print-to-pdf`, WeasyPrint, wkhtmltopdf): render to `resumes/[same base name].pdf`.
- **No tool available:** tell the user to open the HTML in Chrome or Edge, choose Print, set Destination to "Save as PDF", Paper size to Letter (or A4), Margins to Default, turn **off** Headers and footers, and turn **on** Background graphics.
- The design loads Newsreader and Public Sans from Google Fonts and falls back to Georgia and the system sans-serif if the fonts can't load. A PDF made offline will look slightly different but is still correct.

## Checks before reporting it done
- Page count is two or fewer. If over, apply the page-fit cut order from `templates/resume-template.md`, regenerate the markdown, then re-export. Never shrink the type to fit; the template sets a 9.5pt floor.
- Look at every page as an image (convert the PDF to PNG) for clipped text, orphaned headings or a section split from its rows.
- Re-run the never-say scan on the HTML, including the `<title>` and any comments.
- Remove the how-to comment block at the top of the HTML before sharing it.

## Using a different template
If the user has a template they prefer (a Word `.docx`, a Google Doc export, or their own HTML), use that instead:
1. Ask for the file and save a copy to `templates/design/` in their own knowledge base. It stays out of the skill repo, and third-party templates should never be redistributed.
2. If it needs particular fonts, tell the user to install them (and restart Word) before exporting.
3. Map the resume parts to the template's slots using the table above as a guide.
4. Reuse the template's existing styles instead of overriding fonts, sizes or spacing. Edit the text in its paragraphs and list styles.
5. Remove unused placeholder sections, and export to PDF.
6. Run the same checks as above, including headers, footers and the document's author and title properties.

To make the user's choice permanent, record it in `templates/resume-template.md` ("Design export: use `templates/design/[file]`") so later sessions use it automatically.
