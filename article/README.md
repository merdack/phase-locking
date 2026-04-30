# PRD-style physics article template

This directory contains a modular LaTeX scaffold for a physics article formatted with the American Physical Society `revtex4-2` class in Physical Review D (`prd`) style.

## Structure

```text
article/
  main.tex                  Main manuscript file
  Makefile                  Convenience build targets
  latexmkrc                 LaTeX build configuration
  sections/                 Article body sections
  appendices/               Supplementary derivations and numerical details
  bibliography/             BibTeX database
  figures/                  Figure source/export files
  tables/                   Reusable table fragments
  build/                    Generated build output
```

## Build

From this directory, run:

```sh
make
```

The default target uses `latexmk` and writes generated files to `build/`. The compiled PDF is `build/main.pdf`.
Install a TeX distribution with REVTeX, `latexmk`, BibTeX, and the APS bibliography style before building locally.

On GitHub, pull requests to `dev` or `main` build the PDF and upload it as a workflow artifact.
Pushes to `dev` or `main` also commit the generated `article/build/main.pdf` back to the branch.

To remove generated files:

```sh
make clean
```

## Notes

- Replace placeholder author, affiliation, title, and section text in `main.tex` and `sections/`.
- Add figures under `figures/` and reference them with paths relative to that directory.
- Add references to `bibliography/references.bib` and cite them with standard REVTeX commands.
