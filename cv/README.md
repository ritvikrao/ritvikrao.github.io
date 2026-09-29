# CV and resume

LaTeX source for my CV and resume. The CV and the resume share the section
files in `sections/`, so each fact is written once. Jekyll ignores this folder
(it's listed under `exclude` in `_config.yml`), so none of it is published on
the website except the PDFs that `make public` copies to `files/cv.pdf` and
`files/resume.pdf`.

## Building

Run these from this folder (`cv/`):

| Command | Output | Address and phone? |
|---|---|---|
| `make` | `build/cv.pdf` and `build/resume.pdf` | Yes |
| `make public` | `build/cv-public.pdf` and `build/resume-public.pdf`, copied to `../files/cv.pdf` and `../files/resume.pdf` | No |
| `make clean` | Deletes `build/` | |

Use `make` for PDFs you send to people directly. Use `make public` for the
website.

Both commands fail if the resume is longer than 1 page. `make public` refuses to
copy either PDF to the website if any `[TODO: ...]` markers remain, or if the build
somehow read `personal.tex`.

Requires TeX Live (`latexmk`, `pdflatex`) and `pdfinfo`/`pdftotext` from poppler
(`brew install poppler`).

## Updating the website

1. Edit the files in `sections/`.
2. `make public`
3. Commit `files/cv.pdf` and `files/resume.pdf` (along with the source changes)
   and push.

The CV page (`_pages/cv.md`, at `/cv/`) embeds the CV and links to both PDFs,
so it updates on its own. `/resume` redirects to it.

## Personal info

My home address and phone number live in `personal.tex`, which git ignores, so
it never gets pushed. The public build never reads it. On a new machine, copy
`personal.example.tex` to `personal.tex` and fill it in. Without that file,
`make` still works but leaves the address and phone out.

## Editing

- `sections/*.tex`: one file per section. `cv.tex` and `resume.tex` list which
  sections each document includes and in what order.
- `\cvonly{...}` drops something from the resume. Use it on bullets or entries
  that don't fit on one page.
- Publications: `\pub*{...}` appears in both documents; `\pub{...}` appears in
  the CV only. `\venue{full name}{short name}` puts the short venue name on the
  resume.
- `\todo{...}` prints red placeholder text, and `make public` won't publish
  while any remain.
- Page layout, fonts, and the macros above are defined in `cvstyle.sty`.
