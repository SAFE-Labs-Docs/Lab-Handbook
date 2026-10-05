# CLAUDE.md

A markdown-only handbook of 33 lab-culture commitments, plus community examples of each. There is no build step: the markdown is the product, and a GitHub Action pushes it to a WordPress site.

## Layout

| Path | Holds | Edit here when |
| --- | --- | --- |
| `README.md` | The full handbook: intro, section/terminology explainers, then all 33 commitments as collapsible `<details>` blocks under `## SAFE Policies` (line ~74), `## SAFE Teams` (~307), `## SAFE Careers` (~692) | Changing a commitment's Details, Suggestions or Template text |
| `1-POLICIES/NN-Name/README.md` | Community examples for Policies commitments 01 to 11 | Adding or fixing a lab's example for a Policies commitment |
| `2-TEAMS/NN-Name/README.md` | Same for Teams commitments 01 to 11 | Same, Teams |
| `3-CAREERS/NN-Name/README.md` | Same for Careers commitments 01 to 11 | Same, Careers |
| `1-POLICIES/README.md`, `2-TEAMS/README.md`, `3-CAREERS/README.md` | Three-line stub headings | Rarely |
| `.github/workflows/sync-to-wordpress.yml` | The only CI: markdown to HTML, POSTed to the website | Changing how pages are published |
| `.github/workflows/README.md` | One-line stub | Rarely |

Folder names are the commitment order within a category (`01-` to `11-`), for example `1-POLICIES/03-AI-Use`, `2-TEAMS/05-Onboarding`, `3-CAREERS/11-Interview-Process`.

## Build, run, test

There is no package.json, Makefile, test suite or local preview script. Preview by reading the markdown. The only automation is `.github/workflows/sync-to-wordpress.yml`, which runs on push to `main`, `development` or `integrate-website`, and on manual `workflow_dispatch`. It embeds a Python 3.9 script (`pip install requests markdown`) written to `sync.py` at run time; to test the conversion locally, copy the script out of the YAML heredoc.

## Conventions

- Each commitment exists in two places that must stay in sync in spirit: its `<details>` block in the root `README.md` (Details, Suggestions, Template) and its folder `README.md` (`## Details`, `## Suggestions`, `## Examples`). Editing a commitment's wording usually means touching both.
- Folder READMEs open with `# I commit to ...` as the title, then a short contribution invitation, then `## Details`, `## Suggestions` (bullet list), `## Examples`.
- Examples are grouped under `### <Country>` headings, each as a blockquote (`>`) starting with an italic linked lab name such as `_[LabName_2026](url)_:`. New examples go under the matching country; add a new country heading if needed.
- The root README uses raw HTML inside `<details>`/`<summary>` (`<b>`, `<br/>`, `<i>`), not markdown, for each commitment. Match the existing block when adding or editing one.
- Each root-README block ends with a link to `https://github.com/SAFE-Labs-Docs/Lab-Handbook/tree/main/<folder>`; keep it pointing at the right folder if you rename one.
- Verbs are defined in the root README `## Key terminology` (document, publicly document, establish); use them consistently in commitment headings (`**I commit to _publicly document_ ...**`).

## Traps

- Every `.md` file outside dot-directories is synced to the website by path, so renaming or moving a folder or file changes the published page identity. Do not rename `NN-Name` folders casually.
- The sync script strips any line containing both "most readable version" and "safe labs website" (case-insensitive). That is the root README's second line; do not reword it expecting it to publish.
- The script rewrites the LaTeX colour wrapper `${\color{green}` ... `}$` into bold. Other LaTeX will not render on the website.
- Markdown is converted with the `extra`, `tables`, `codehilite` and `toc` extensions only, so GitHub-only syntax may not render identically on the site.
- A failed connectivity test to the website API aborts the whole run (`exit(1)`); individual file failures are only logged and counted.
- `.DS_Store` is gitignored; do not add it.
- The root README is about 950 lines and 73 KB; read it by line range, not whole.

## Deeper docs

The root `README.md` has the terminology (`## Key terminology`), the per-commitment section meanings (`## Sections for each commitment`), and the rationale. Do not duplicate those here.
