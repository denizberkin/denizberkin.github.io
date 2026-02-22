# Resume TeX Source

This folder contains the LaTeX source files used to generate the website resume PDF.

## Main file

- `resume.tex` is the entry point compiled by GitHub Actions.

## Supporting files

- Keep custom style/class files (`.sty`, `.cls`) and section files under this folder (for example, `sections/`).
- Use relative paths from `resume.tex` (e.g., `\usepackage{sections/TLCresume}`).

## Automatic build

The workflow at `.github/workflows/compile-resume-tex.yml` runs on pushes that modify:

- `assets/resume-src/**/*.tex`
- `assets/resume-src/**/*.sty`
- `assets/resume-src/**/*.cls`

It compiles `assets/resume-src/resume.tex` and updates:

- `assets/pdf/resume.pdf`

## Notes

- The website link to the resume should remain `/assets/pdf/resume.pdf`.
