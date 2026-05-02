# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This is a bilingual (English / German) research report on creatine supplementation and sleep, published as a GitHub README. There is no build system, no code, and no tests. All content lives in `README.md`.

## Content structure

`README.md` is the entire report. Each section uses a two-column markdown table (`| English | Deutsch |`) to present bilingual content in parallel. Section headings are bilingual too (e.g., `## 6. Benefits / Nutzen`).

`TODO.md` tracks outstanding peer-review revisions. Each item maps to a specific change in `README.md` and includes exact wording for replacements. Work through TODO items in order; check them off as each is applied.

## Editing conventions

- Preserve the two-column bilingual table structure for every content row.
- Section numbers in headings, the Table of Contents, and anchor links must stay in sync whenever sections are added or renumbered.
- TOC anchor links must use ASCII-only slugs (no umlauts). Use explicit `<a name="...">` tags above headings when the heading contains non-ASCII characters.
- The LICENSE file is GPL-3.0 (applies to any code). Report text (`README.md`) is CC BY 4.0.

## Verification after edits

The TODO.md verification checklist contains `grep` commands to confirm specific changes were applied or removed:

```bash
grep -c "Mechanism\|Wirkmechanismus" README.md
grep "eight human studies" README.md
grep "12%" README.md          # should be empty after Item 5
grep "Phosphokreatin-/ATP" README.md   # should be empty after Item 11a
```
