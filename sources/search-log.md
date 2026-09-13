# Search Log

> Append-only record of every search run performed by `literature-scout`. Each run is logged even if it produced zero new candidates.

**Note on scope for this batch:** `research-question.md` does not yet exist in this repository. Per the literature-scout stopping conditions, an underspecified `research-question.md` would normally trigger escalation before searching. This batch was run as a bounded ad hoc test against the user's direct query below rather than against a formal scope file — treat all records below as provisional pending a real `research-question.md`.

---

## Run 1

- **Date:** 2026-09-13
- **Query:** "IgA nephropathy recent clinical and mechanistic advances"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 5
- **Notes:** Dominated by major reviews (Nature Reviews Nephrology, Nature Reviews Disease Primers, Kidney International, NDT, JASN) reflecting a very high-activity therapeutic area (multiple newly approved/emerging targeted therapies: SGLT2 inhibitors, sparsentan, iptacopan, targeted-release budesonide, BAFF/APRIL inhibitors). Several 2026-dated review hits reflect Consensus's forward-dated online-first indexing. Recency and relevance prioritized; journal impact treated as secondary (all top hits are in high-impact nephrology journals, consistent with a mature, well-studied field rather than a deliberate filter).

## Run 2

- **Date:** 2026-09-13
- **Query:** "IgA vasculitis Henoch-Schönlein purpura recent studies"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 3
- **Notes:** Rate-limited on first attempt; re-run succeeded. Mix of narrative reviews, a Cochrane systematic review (highest methodological quality in the set), pediatric cohort/case-series studies, and a mechanistic/immunology study. Several small case series and abstract-only conference results appeared (e.g., a 0-citation conference abstract) — excluded from source records as too preliminary for evidence intake without full-text verification.

## Run 3

- **Date:** 2026-09-13
- **Query:** "IgA nephropathy"
- **Tool/database:** PubMed (secondary/cross-verification)
- **Filters:** date_from=2022, date_to=2026, sort=pub_date
- **Results returned:** 3,303 total (10 shown, sorted by publication date)
- **New candidates recorded:** 2 (of 6 metadata-checked)
- **Notes:** Query alone is far too broad for a bounded scope (3,303 hits) — this is expected without a real `research-question.md` narrowing by study type, population, or sub-topic. Used here only to sample the most recent items and cross-verify Consensus hits. Most of the newest-dated items were narrow mechanistic/case studies; selected a real-world retrospective cohort (finerenone) and a biomarker association study (homocysteine) as illustrative recent primary-research examples.

## Run 4

- **Date:** 2026-09-13
- **Query:** "IgA vasculitis"
- **Tool/database:** PubMed (secondary/cross-verification)
- **Filters:** date_from=2022, date_to=2026, sort=pub_date
- **Results returned:** 1,159 total (10 shown, sorted by publication date)
- **New candidates recorded:** 3 (of 6 metadata-checked)
- **Notes:** Same over-breadth issue as Run 3. Selected a multicenter case series with systematic literature review (necrotizing arteritis phenotype), a case series/case report on telitacicept (novel BAFF/APRIL-targeted therapy also emerging in IgAN), and a mechanistic animal study (Rehmannia glutinosa extract) representing basic-research evidence. Excluded several letters/editorials with no abstract and a single-patient case report series without further corroboration pending fuller review.

## Run 5

- **Date:** 2026-09-13
- **Query:** Targeted PubMed title/author lookups to cross-verify 4 Consensus-discovered reviews (Cheung 2024 NRN; Stamellou 2023 NRDP; Barratt 2023 Kidney Int; Castañeda 2024 JCM; Hahn 2023 Cochrane)
- **Tool/database:** PubMed (verification)
- **Filters:** none (exact-title / title+author search)
- **Results returned:** 1 unambiguous match each for 4 of 5 targets on the first attempt; Stamellou 2023 required a follow-up journal+year-qualified search after two false-positive matches (different Stamellou papers)
- **New candidates recorded:** 0 (verification-only run against already-recorded candidates)
- **Notes:** All 5 titles, author lists, journals, years, and DOIs independently confirmed against PubMed metadata, matching the Consensus-supplied bibliographic details exactly. No discrepancies found. This satisfies the two-independent-source verification requirement for these 5 records.

**Saturation:** Not fully reached for either topic — both remain very large, active literatures (thousands of PubMed hits). This batch stopped at a bounded, illustrative sample per the test scope rather than continuing to full saturation; a real research run would need `research-question.md` to define sub-scope (e.g., a specific intervention, population, or study-design filter) before saturation is a meaningful stopping criterion.
