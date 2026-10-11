 Minimalist ATS-friendly CV template (LaTeX)
 
A simple, one-column CV template in pure LaTeX, designed to be parsed correctly by
Applicant Tracking Systems (ATS). Pure structure, no fluff.
 
Inspired by the layout of [Jake's Resume](https://github.com/jakegut/resume).
 
## Why this template
 
Many fancy LaTeX CV templates look great but parse badly in ATS. This one avoids the usual
problems:
 
- **One column**, so text is extracted in the correct reading order
- **No icons, no graphics, no layout tables** that can scramble or drop text
- **Standard section names** (Professional Summary, Technical Skills, Professional
  Experience, Education)
- **`T1` font encoding**, so characters copy out of the PDF correctly
- Plain bullet points and selectable text
## Usage
 
1. Edit `pure-cv.tex` and replace the placeholder content with your own.

2. Compile with:

```bash
   pdflatex pure-cv.tex
```
 
3. Check the result: open the PDF, select all (Ctrl+A), copy, and paste into a plain text
   editor. If the text appears in the right order and nothing is missing, ATS will most
   likely read it correctly too.

## Template commands
 
| Command | Purpose |
|---|---|
| `\rSection{Title}` | Section heading with a rule |
| `\rSubSectionListStart` / `\rSubSectionListEnd` | Wraps a group of entries |
| `\rSubSection{Company}{Dates}{Role}{Location}` | One entry header (two lines) |
| `\rItemizeBegin` / `\rItemizeEnd` | Wraps the bullet list under an entry |
| `\rItem{Text}` | A single bullet point |

## Customization
 
- **Language:** change `\usepackage[english]{babel}` (for example to `polish`) and translate
  the section titles. For non-English text, keep `T1` encoding enabled.
- **Page margins:** adjust `\usepackage[margin=1.6cm]{geometry}`.
- **Page footer:** add a `\vfill{ \footnotesize \emph{...} }` before `\end{document}`.

## Tips for ATS-friendly content
 
- Use a job title close to the one in the posting (for example "Python Developer").
- Put technologies in context inside bullet points, not only in the skills list.
- Prefer concrete results (scale, users, outcomes) over lists of duties.
- Keep the file to one or two pages, and export as a text-based PDF, not an image.
