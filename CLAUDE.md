# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A Quarto website with the teaching material for **10888 - Delineamento, Análise e Interpretação de Dados**, an elective in the BICT Mar undergraduate program at Unifesp (2nd semester of 2026). It is not a software project: the "code" is R embedded in `.qmd` documents that produce the course site published at https://fcopf.github.io/daid-2026/.

All prose, headings, callout titles, and code comments are in **Brazilian Portuguese** (`lang: pt-BR`). Match this in any content you write.

## Commands

```bash
quarto preview                                  # live preview with auto-reload
quarto render                                   # full site build into _site/
quarto render content/computer-lab/lab-anova-um-fator.qmd   # render a single document
```

R dependencies are managed by renv (`.Rprofile` auto-activates it):

```bash
Rscript -e 'renv::status()'    # check lockfile vs installed library
Rscript -e 'renv::restore()'   # install what renv.lock specifies
Rscript -e 'renv::snapshot()'  # after adding a library() call to any .qmd
```

There are no tests or linters. The verification step for any content change is that `quarto render` completes without R errors and the resulting page reads correctly.

## Build behavior that matters

- `execute: freeze: auto` — rendered R output is cached in `_freeze/`, which is **gitignored**. CI therefore re-executes every chunk from scratch on each push; a chunk that works locally only because of a stale freeze will fail there.
- `execute-dir: project` — chunks run with the working directory at the repo root, not next to the `.qmd`.
- `.github/workflows/publish.yml` renders on every push to `main` and deploys to the `gh-pages` branch (R 4.3 + renv restore + Quarto). Nothing else publishes the site.
- `_quarto.yml` renders `index.qmd`, `content/*/*.qmd`, and `course-info/*.qmd`. A new document only appears in the build if it lands in one of those globs.
- `.renvignore` excludes local copies of other course repos (`prob-est-2026-main/`, `mead-main-EXAMPLE/`) so their `library()` calls do not leak into `renv.lock`.

## Structure and the three-way pairing

Content lives in three parallel directories, one document per week of the course:

- `content/pre-reading/pread-*.qmd` — conceptual reading, done **before** the meeting (15, one per week)
- `content/computer-lab/lab-*.qmd` — hands-on R session, for the 10 weeks with a class meeting
- `content/assignment/assig-*.qmd` — take-home activity, for the 5 weeks without one

Each week has exactly one pre-reading plus either a lab or an assignment, never both. That pairing is asserted in **four** places, and adding, removing, or renaming a document means updating all of them:

1. `index.qmd` — the schedule table (week, date, theme, and 📖/💻/📝 links)
2. `content/pre-reading/index.qmd`, `content/computer-lab/index.qmd`, `content/assignment/index.qmd` — the per-directory catalog tables, each cross-referencing the week number
3. the prose in `course-info/syllabus.qmd` ("Como a UC funciona", which states the 10 + 5 split and the count of 15 deliverables)
4. the sibling documents' intro paragraphs, which reference each other by title

## Document conventions

Every content `.qmd` repeats the same YAML front matter — title, `subtitle` naming the slot ("Leitura prévia", "Prática em R 02", "Atividade extraclasse 01"), the two-line author block, `date: today`, and a `format: html` block. Labs and assignments add `code-tools: true`; pre-readings do not. Copy the front matter from a sibling document rather than writing it fresh.

- **Self-contained documents.** Every document loads its own packages, imports its own data, and runs top to bottom in a fresh R session. Nothing is shared across documents. The only package used anywhere is `tidyverse`, and the standard opening chunk is `library(tidyverse)` followed by `theme_set(theme_bw(base_size = 12))`. Pre-readings hide it with `#| include: false`; labs and assignments show it, because the R itself is the lesson there.
- **Data by URL.** Datasets are read over HTTP from `https://raw.githubusercontent.com/FCopf/datasets/` (mostly the Zuur 2009 sets: RIKZ, Biodiversity, Clams, Squid). No data files live in this repo, and none should be added — put new datasets in the `FCopf/datasets` repo and link to them.
- **`title: "Entregue"`** — every lab and assignment ends with a `.callout-important` with this exact title, stating what the student submits. There are 15 of them and the grade is their mean; do not create a lab or assignment without one.
- **Callouts** use `appearance="minimal"` with an explicit `title=`. `callout-tip` is the workhorse ("Observe", conceptual asides), `callout-warning` flags a common mistake, `callout-important` marks the deliverable.
- **No R teaching prerequisite.** Functions are explained in prose the first time they appear (`replicate()`, `sample()`, `read_tsv()`), and the analytical progression is fixed by the syllabus: variation → population/sample → sampling distribution → replication → null model → t test → ANOVA → blocks/factorial → regression → ANCOVA. A document should not use a concept the schedule introduces in a later week.
- **Citations** come from `references.bib` (`@gotelli2015`, `@quinn2002`, `@hurlbert1984`, `@zuur2009`, …); add an entry there before citing. Links to the companion MEAD site (`https://fcopf.github.io/mead/`) are the standard "read more" pointer.

## Styling

`styles/theme.scss` and `styles/theme-dark.scss` are near-duplicates (Cosmo + Atkinson Hyperlegible from `fonts/`) and must be edited **in tandem** — a rule added to one without the other breaks in that colour scheme. They define the three project-specific classes: `.cronograma-bme` (the schedule table, with `.aula-celula` modifiers `.is-extraclasse` and `.is-pausa`), `.catalogo-materiais` (the per-directory catalog tables), and `.uc-id-card` / `.uc-id-grid` (`course-info/uc-id.qmd`).

## Note

`CLAUDE.md` is listed in `.gitignore`, so this file stays local and untracked by design.
