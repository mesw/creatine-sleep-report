# TODO — Peer Review Revisions to Creatine & Sleep Report

All changes are confined to `README.md`. Branch: `claude/revise-peer-review-feedback-Pzurf`.

---

## Structural Additions

- [ ] **Item 15 — New Section 2 "Mechanism / Wirkmechanismus"**
  Insert between Introduction and Methodology. Cover phosphocreatine/ATP buffering hypothesis, brain energetics, cite Dworak 2017 as mechanistic context. Bilingual table format, ~2 rows.

- [ ] **Renumber all sections** after inserting new Section 2:
  Methodology → 3, Well-Rested Humans → 4, Sleep Deprivation → 5, Population-Level → 6, Benefits → 7, Risks → 8, Conclusions → 9.

- [ ] **Item 3 — Expand Methodology (new Section 3)**
  Replace single vague paragraph with: databases searched (PubMed, Google Scholar, Scopus), date range (through April 2026), keyword strings, inclusion criteria (human, peer-reviewed, English or German), exclusion criteria (non-peer-reviewed, animal-only except mechanistic context), records-screened/included count.

- [ ] **Item 13 — New "Summary of Included Studies" table**
  Place immediately after Methodology. Columns: Study | Year | Design | N | Population | Dose | Duration | Primary Sleep Finding | Effect direction. ASCII-only; English headers with short German caption above.

- [ ] **Item 8 — New "License & Attribution / Lizenz & Zuordnung" section**
  Place before Disclaimer. Document content: CC BY 4.0. Contributors line (placeholder: "Repository maintainer: mesw. Contributions welcome via pull request."). Note that GPL-3.0 applies to any code; README text is dual-covered under CC BY 4.0.

---

## Content Fixes

- [ ] **Item 1 — Fix abstract study count**
  Change "nine human studies" → "eight human studies" (EN) and "neun Humanstudien" → "acht Humanstudien" (DE).

- [ ] **Item 2 — Split McMorris 2006 / 2007**
  Replace single combined bullet in Section 5 (Sleep Deprivation) with two separate bullets:
  - McMorris et al. (2006, *Psychopharmacology*): 7 d × 20 g/d; 24 h sleep deprivation; cognitive + mood + catecholamine focus; creatine attenuated declines in random movement generation, choice reaction, balance, mood.
  - McMorris et al. (2007, *Physiology & Behavior*): 7 d × 20 g/d; 24 h sleep deprivation with intermittent exercise; cognitive + mood + hormonal (melatonin, cortisol, growth hormone); creatine preserved performance on prefrontal-sensitive tasks.
  Update both EN and DE.

- [ ] **Item 7 — Rebalance Ben Maaoui null results**
  Rewrite Section 4.1 Findings row so objective-null results lead. Add one sentence explicitly flagging that objective metrics were unchanged as the study's most important negative finding. Add short "Null-result note" in Interpretation row.

- [ ] **Item 4 — COI disclosure for Aguiar Bonfim Cruz**
  Add new row in Section 4.2 table titled "Conflict of interest / Interessenkonflikt" noting co-author D.G. Candow's declared industry ties (Alzchem scientific advisory board; paid expert witness in creatine-related litigation); advise readers to weigh positive findings accordingly.

- [ ] **Item 5 — Remove unverified 12% claim**
  In Section 5, Gordji-Nejad row, delete "improved cognitive performance by approximately 12%". Replace with: "preserved brain phosphocreatine/ATP levels and mitigated cognitive decline during 21 hours of sleep deprivation (magnitude of cognitive effect not precisely quantified in the primary paper)." Update EN + DE.

- [ ] **Item 12 — Bold the dietary-creatine caveat**
  In Section 6 (Population-Level), surround "This was dietary creatine — not supplementation." with bold (`**...**`). Do the same for the German equivalent "Hierbei handelt es sich um Nahrungskreatin — nicht um eine Supplementierung."

- [ ] **Item 10 — Clarify "n = 14–29 in direct RCTs"**
  In Section 8 Research gaps row, change wording to: "Small sample sizes in the direct RCTs reviewed (n = 14–29; the only large-n study, Baltic 2025, is cross-sectional and not an RCT)." Update EN + DE.

---

## Reference List Fixes

- [ ] **Item 9 — Add missing DOIs**
  - Ref 3 (McMorris 2006): `https://doi.org/10.1007/s00213-005-0269-z`
  - Ref 4 (McMorris 2007): `https://doi.org/10.1016/j.physbeh.2006.08.024`
  - Ref 9 (Dworak 2017): `https://doi.org/10.1111/jsr.12523`
  - Ref 13 (Antonio 2025): `https://doi.org/10.1080/15502783.2024.2441760`

---

## German Stylistic Fixes

- [ ] **Item 11a — Fix compound term**
  Replace all occurrences of `Phosphokreatin-/ATP-Spiegel` → `Phosphokreatin- und ATP-Spiegel` (appears in Section 1 Einleitung, Section 5 Gordji-Nejad row, new Mechanism section). Also covers `Phosphokreatin-/ATP-System` → `Phosphokreatin- und ATP-System`.

- [ ] **Item 11b — Fix section 4.2 heading and body**
  Replace heading `Natürlich menstruierende Frauen` → `Frauen mit natürlichem Menstruationszyklus`. Also update opening sentence `21 natürlich menstruierende Frauen` → `21 Frauen mit natürlichem Menstruationszyklus`.

---

## Anchor Link Safety

- [ ] **Item 14 — Replace umlaut-containing TOC anchors**
  Add explicit `<a name="...">` tags above affected headings and update TOC links to ASCII-only anchor names:
  - `<a name="mechanism"></a>` → TOC: `#mechanism`
  - `<a name="population-level-evidence"></a>` → TOC: `#population-level-evidence`
  - `<a name="risks-and-limitations"></a>` → TOC: `#risks-and-limitations`
  - `<a name="license-attribution"></a>` → TOC: `#license-attribution`
  Regenerate all TOC entries to reflect new section numbering.

---

## Verification Checklist

After writing the file, run these checks:

```bash
grep -c "Mechanism\|Wirkmechanismus" README.md          # > 0
grep -c "McMorris.*2006" README.md                      # own line
grep -c "McMorris.*2007" README.md                      # own line
grep "eight human studies" README.md                    # present
grep "acht Humanstudien" README.md                      # present
grep "12%" README.md                                    # empty
grep "Natürlich menstruierende" README.md               # empty
grep "Phosphokreatin-/ATP" README.md                    # empty
grep "10.1007/s00213" README.md                         # present
grep "10.1016/j.physbeh" README.md                      # present
grep "10.1111/jsr.12523" README.md                      # present
grep "10.1080/15502783" README.md                       # present
```

---

## Git

- [ ] Commit with message: `Revise report per peer review feedback`
- [ ] Push: `git push -u origin claude/revise-peer-review-feedback-Pzurf` (retry up to 4× on network failure)
