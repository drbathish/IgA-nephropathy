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

---

## Batch 2 — Full production run against research-question.md (2026-09-13)

Scope: research-question.md now exists (created 2026-09-13). This batch systematically covers, for both IgAN and IgAV: (1) mechanism/pathogenesis/biomarkers, (2) treatment/therapeutics (SGLT2i, sparsentan, iptacopan/avacopan/narsoplimab, TRF-budesonide, telitacicept/atacicept/blisibimod, rituximab), (3) diagnostics/clinical phenotypes. Priority: find tier-1/tier-2 IgAN-specific evidence (previously absent) and controlled/comparative evidence for newer targeted therapies. Consensus filters used throughout unless noted: year_min=2022, exclude_preprints=true, medical_mode=true (consistent with Batch 1 and with research-question.md's explicit Jan-2022-present date range).

## Run 6

- **Date:** 2026-09-13
- **Query:** "IgA nephropathy sparsentan randomized controlled trial"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 6 (2 PROTECT trial reports [interim + 2-year], 1 post-hoc complete-remission analysis, 1 gddY mouse mechanistic study, 1 systematic review [found via a parallel query, see Run 7], 1 unverified conference-abstract candidate logged)
- **Notes:** MAJOR FINDING — this query surfaced the PROTECT phase 3 RCT (Heerspink 2023 Lancet interim; Rovin 2023 Lancet 2-year results), which directly fills the previously identified gap of zero tier-1/tier-2 IgAN-specific evidence. All bibliographic details independently verified against PubMed (exact DOI/PMID/author-list match; see individual source records). Several hits were ASN/ERA-EDTA conference abstracts (baseline-characteristics posters, interim OLE data) with no associated full-text peer-reviewed publication identifiable in PubMed — excluded per research-question.md's exclusion criteria for conference-abstract-only findings (not recorded as source files, since their core bibliographic identity as a citable published work could not be established at all — distinct from the Wadhwani case below, which had enough detail to warrant a logged-but-unverified record). One candidate (Wadhwani et al., PRO analysis of PROTECT) had enough apparent detail to attempt verification but failed on two independent PubMed searches — logged as `unverified` per the escalation-avoidance rule (see sources/papers/unverified-wadhwani-2024-jasn-pro-protect.md) rather than silently dropped.

## Run 7

- **Date:** 2026-09-13
- **Query:** "IgA nephropathy systematic review meta-analysis treatment outcomes"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** rate-limited on first attempt; results obtained on retry within the same batch (see Run 6 raw results, query executed in parallel)
- **New candidates recorded:** 1 (Jeyabalan et al. 2025, PLOS One — systematic literature review and narrative synthesis of 76 RCTs in IgAN)
- **Notes:** TIER-1 EVIDENCE FOUND — directly fills the stated priority gap. Verified independently via PubMed (article type "Systematic Review" confirmed). Notable industry-adjacency (one co-author affiliated with Travere Therapeutics) flagged in the source record for evidence-reviewer's bias appraisal, not resolved here.

## Run 8

- **Date:** 2026-09-13
- **Query:** "SGLT2 inhibitor IgA nephropathy randomized controlled trial proteinuria eGFR"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 5 (ALIGN atrasentan final 2.5-year placebo-controlled RCT; atrasentan+SGLT2i placebo-controlled crossover RCT; ambrisentan+henagliflozin 3-arm randomized crossover RCT; already-counted PROTECT-adjacent items excluded as duplicates)
- **Notes:** MAJOR FINDING — surfaced the ALIGN trial (Heerspink 2026 Lancet), a placebo-controlled (not just active-comparator) phase 3 RCT of atrasentan, plus two further controlled/comparative trials combining endothelin receptor antagonists with SGLT2 inhibitors — directly addresses the stated priority for controlled/comparative evidence for newer targeted therapies (previously only single-arm evidence existed). All three independently verified via PubMed (exact metadata match, article type "Randomized Controlled Trial" confirmed for all three). Several additional hits were NDT/ASN conference abstracts reporting real-world SGLT2i case-control or single-arm cohort data (e.g., a 68-vs-68 matched case-control study, a dapagliflozin real-world cohort) — not recorded pending confirmation of an associated full-text publication (see Run 9 for follow-up attempt). One narrative review (Del Vecchio et al., SGLT2 inhibitors in glomerulonephritis, J Clin Med 2025) noted as background-context-only candidate, not yet recorded (queued for later batch verification alongside other narrative reviews collected this session).

## Run 9

- **Date:** 2026-09-13
- **Query:** "targeted-release budesonide NefIgArd IgA nephropathy randomized controlled trial"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 3 (NefIgArd Part A [Barratt 2022 Kidney Int]; NefIgArd 2-year results [Lafayette 2023 Lancet]; targeted-release budesonide in recurrent IgAN post-transplant [Gandolfini 2023 Kidney Int, flagged re: letter/commentary format for evidence-reviewer])
- **Notes:** MAJOR FINDING — surfaced the second placebo-controlled phase 3 IgAN RCT (NefIgArd/Nefecon), independently confirming and complementing the ALIGN and PROTECT trials already captured. All three independently verified via PubMed. Several additional hits were ASN/WCN/NDT conference abstracts (biomarker sub-analyses, network meta-analysis abstract, real-world case series n=11, Indian open-label single-arm trial) with no associated full-text peer-reviewed publication identifiable — not recorded per exclusion criteria for conference-abstract-only findings. Confirmed via a dedicated PubMed search that the SGLT2i real-world case-control abstract (#854, Obrișcă et al., flagged in Run 8) has no associated full-text publication in PubMed — logged as excluded (conference-abstract-only), not recorded as a source file since its bibliographic identity as a citable published work could not be established at all.

## Run 10

- **Date:** 2026-09-13
- **Query:** "iptacopan avacopan narsoplimab complement inhibitor IgA nephropathy clinical trial"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** rate-limited on first attempt; re-run pending
- **New candidates recorded:** pending re-run
- **Notes:** Consensus rate limit hit; re-queried in the next batch.
