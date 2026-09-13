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
- **Query:** "iptacopan IgA nephropathy APPLAUSE randomized controlled trial complement factor B" and "narsoplimab MASP-2 inhibitor IgA nephropathy trial" and "telitacicept atacicept blisibimod BAFF APRIL inhibitor IgA nephropathy clinical trial" (3 parallel queries)
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10 each (30 total)
- **New candidates recorded:** 8 verified (APPLAUSE-IgAN interim [Perkovic 2024 NEJM]; APPLAUSE-IgAN final 24-month [Barratt 2026 NEJM]; iptacopan phase 2 [Zhang 2023 KI]; APPLAUSE-IgAN design/protocol [Rizk 2023 KI Reports, lower-weight protocol-only record]; sibeprenlimab phase 2 ENVISION [Mathur 2023 NEJM]; atacicept ORIGIN phase 2b [Lafayette 2024 KI]; cemdisiran phase 2 [Barratt 2024 CJASN]; IgAV narrative review of novel nephritis drug treatments [Williams et al. 2023 Clin Rheumatol, background-context only])
- **Notes:** MAJOR FINDING — this cluster surfaced a third and fourth placebo-controlled phase 3/pivotal-track IgAN RCT (iptacopan/APPLAUSE-IgAN interim + final), plus phase 2 RCTs for atacicept (a specifically named drug in research-question.md), sibeprenlimab (closely related APRIL-targeted mAb, flagged for evidence-reviewer to confirm in-scope status against the exact named-drug list), and cemdisiran (a complement C5 inhibitor, distinct mechanism from the three named complement drugs but within the general "complement pathway inhibitors" scope category). No narsoplimab RCT results were found — all narsoplimab hits were single-patient case reports/conference abstracts (see below) or a trial-design-only ERA-EDTA abstract (ARTEMIS-IgAN, POS-132); the pivotal narsoplimab phase 3 trial appears to have reported a non-significant primary endpoint per a citing commentary (Zhu et al. 2025 JASN letter, not independently verified as a primary source and not recorded) but no full-text primary publication of that result was found in this search — flagged as an evidence gap for narsoplimab specifically, not resolved by assumption. Several conference-abstract-only candidates excluded: iptacopan interim analysis abstracts (#456, WCN24-1506, WCN25-726 complement biomarkers, Rizk 2024 JASN low-eGFR subcohort), narsoplimab pediatric case report (Oni 2022 JASN abstract) and adult recurrent-IgAN case report (Storrar 2022 JASN abstract) — both potentially illustrative of a "genuinely novel/emerging intervention" per the tier-7 carve-out, but no full-text peer-reviewed publication was identified, so not recorded as source files per the conference-abstract exclusion criterion (noted here for audit-trail transparency). Also excluded: a systematic-review protocol (Ma et al. 2024 PLOS ONE, biologic agents in IgAN) with no results yet reported (not evidence-bearing), and a JASN letter/commentary on complement inhibition (Zhu et al. 2025) with no original data (background-only if used at all, not recorded as this session's focus was primary evidence). One off-topic false-positive (Wani et al., NELL1-associated membranous nephropathy — not IgAN/IgAV) excluded as out-of-scope.
- **Correction note:** A source record was initially filed for the Williams et al. 2023 Clin Rheumatol narrative review under an incorrectly-guessed DOI filename (10.1007-s10067-023-06764-9.md). The correct DOI (10.1007/s10067-023-06781-8) was confirmed via a follow-up PubMed metadata fetch in the same session; the original stub file was overwritten with a pointer to the corrected record (10.1007-s10067-023-06781-8.md) rather than deleted, per the project's audit-trail preservation rule.

## Runs 11-13 — avacopan sub-topic (SATURATED, evidence gap identified)

- **Date:** 2026-09-13
- **Queries:** "avacopan IgA nephropathy IgA vasculitis treatment"; "avacopan complement C5a receptor antagonist IgA nephropathy trial glomerular disease"; "avacopan IgA vasculitis nephritis case report compassionate use"
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10 each (30 total)
- **New candidates recorded:** 0
- **Notes:** SATURATION REACHED (3 consecutive reformulated queries, zero new in-scope candidates) per research-question.md's stopping rule. All 30 hits across three query reformulations were for ANCA-associated vasculitis (a distinct disease from IgAV) or C3 glomerulopathy (a distinct disease from IgAN) — none were IgAN- or IgAV-specific avacopan studies (aside from duplicate hits of already-recorded iptacopan/cemdisiran trials and the Williams review, which mentions avacopan only as a theoretical extrapolation candidate, not as tested). CONCLUSION: this appears to be a genuine, real evidence gap — avacopan (unlike iptacopan and narsoplimab) does not yet have a dedicated IgAN or IgAV clinical trial in the literature as of this search date. Flagging explicitly for research-writer/evidence-reviewer as an evidence gap rather than omitting silently.

## Run 14

- **Date:** 2026-09-13
- **Query:** "rituximab IgA nephropathy randomized controlled trial proteinuria" and "rituximab IgA vasculitis nephritis children treatment outcomes" (2 parallel queries; second rate-limited, not yet re-run)
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10 (first query only)
- **New candidates recorded:** 3 verified (telitacicept phase 2 RCT [Lv 2022 KI Reports]; atacicept JANUS phase II RCT [Barratt 2022 KI Reports]; ravulizumab phase 2 RCT [Lafayette 2024/2025 JASN])
- **Notes:** No rituximab-specific RCT for IgAN found (rituximab literature for IgAN/glomerular disease in this search was for relapsing nephrotic syndrome [Isaka 2025 JAMA — NOT IgAN-specific, excluded as off-topic] and a small uncontrolled case series [Sun et al., JASN conference abstract, n=8, IgAN with podocytopathy — excluded, no full-text publication identified]). One highly relevant conference-abstract-only finding — Trivioli et al., "Rituximab in adult-onset IgA vasculitis" (NDT abstract #3108, n=61 IgAV + n=15 crescentic IgAN, multicentre European cohort, 85% remission at 6 months) — could not be matched to any full-text peer-reviewed publication via a dedicated PubMed search (0 results); not recorded as a source file per the conference-abstract exclusion criterion, logged here for audit-trail transparency since it is the most substantial rituximab-in-IgAV dataset found this session. Second query (rituximab in pediatric IgAV nephritis) was rate-limited by Consensus and re-queried in Run 15.

## Run 15

- **Date:** 2026-09-13
- **Query:** "rituximab IgA vasculitis nephritis children treatment outcomes" (re-run)
- **Tool/database:** Consensus (primary)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 1 (Rohner et al. 2024 NDT — large multinational retrospective cohort, n=1148 children with biopsy-proven IgAVN, immunosuppression outcomes)
- **Notes:** MAJOR FINDING for the treatment/therapeutics and diagnostics/phenotype sub-topics — the largest pediatric IgAVN cohort found this session (41 centres, 25 countries), with a notable null finding (no second-line immunosuppressive regimen shown superior to others) that is itself an important evidence gap to represent in synthesis. Remaining hits were: 2 already-recorded background reviews (Castañeda 2024, Williams 2023); 1 single-case conference abstract (Kaiga et al., rituximab in refractory IgAV, JASN abstract — excluded, no full-text found); the same Trivioli rituximab abstract already logged as excluded in Run 14; and several off-topic rituximab studies in childhood nephrotic syndrome and ANCA-associated vasculitis (distinct diseases from IgAN/IgAV — excluded as out of scope).

## Run 16

- **Date:** 2026-09-13
- **Query:** "galactose-deficient IgA1 biomarker pathogenesis IgA nephropathy mucosal immunity gut-kidney axis" (with a follow-up on "IgA nephropathy gut microbiome TLR4 MyD88..." and "Lactobacillus casei cell wall extract..." to verify specific hits)
- **Tool/database:** Consensus (primary), PubMed (verification)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 3 verified (Zachova 2022 JASN — Gd-IgA1+ B cell lambda-light-chain/mucosal-homing study; Zhu 2024 NDT — gut microbiome/TLR4 mechanistic study with human+murine data; Li 2024/2025 JASN — novel humanized IGHA1 mouse model)
- **Notes:** Rich mechanism/pathogenesis/biomarker sub-topic yield for IgAN (mucosal immunity, gut-kidney axis, Gd-IgA1 origin). Several additional strong candidates identified but not yet recorded due to session scope/time: Wu et al. 2026 Kidney Int and Wu et al. 2025 JASN (two related C1GALT1-knockout mouse studies challenging the causal sufficiency of Gd-IgA1 for glomerular deposition — an important emerging counter-narrative to the "four-hit" model), Gentile et al. 2024 KI Reports (unconventional T cells/B cell subsets), and Seikrit et al. 2026 Kidney Int commentary on IgA2 as a co-pathogenic driver (commentary, would be background-only). These remain candidate leads not yet verified/recorded — flagged for a follow-up literature-scout batch if the orchestrator wants deeper mechanism-subtopic coverage; NOT dropped silently, logged here. Two already-recorded background reviews (Cheung 2024 Nat Rev Nephrol) resurfaced; a companion 2026 Kidney Int Supplements overview by the same author group was also seen but not recorded (redundant with the already-captured Cheung 2024 review for background purposes).

## Run 17

- **Date:** 2026-09-13
- **Query:** "IgA nephropathy diagnosis biopsy MEST-C Oxford classification prognostic score 2023 2024" and "IgA vasculitis pathogenesis mechanism complement lectin pathway biomarker" (2 parallel queries)
- **Tool/database:** Consensus (primary), PubMed (verification)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10 each (20 total)
- **New candidates recorded:** 3 verified (Jaugey 2023 NDT — deep learning MEST-C automation; Ștefan 2023 KI Reports — TIER-1 systematic review on MEST-C/complement linkage, 34 studies/10,082 patients; Barbour 2024 CJASN — major multiethnic IgAV-nephritis MEST-C validation study, n=361)
- **Notes:** MAJOR FINDING — the Barbour et al. study is the most rigorous IgAV-specific diagnostics/histology study found this session (centralized 3-pathologist re-scoring across 23 international centers) and nuances the direct IgAN-to-IgAV extrapolation of the Oxford MEST-C classification (only E1 and fibrous crescents were independently prognostic, not the full MEST-C panel). The Ștefan systematic review is a second tier-1 IgAN-specific study (alongside Jeyabalan et al.), further closing the previously identified tier-1 evidence gap. Additional strong candidates seen but not recorded due to session scope: Sahu et al. 2024 (JASN conference abstract on complement in childhood IgAN, n=52 — excluded, abstract-only), Genest et al. 2022 KI Reports (cross-disease complement pathway comparison including IgAN, n=112 — not IgAN/IgAV-specific enough as primary focus per exclusion criteria, background-adjacent), Barratt et al. 2023 KI lectin pathway review (already recorded as background), and a conference-abstract comparing complement biomarkers between IgAN and IgAVN (#887 Sanaei Nurmi, NDT, n=96 — excluded, abstract-only, logged for audit-trail transparency as a substantively relevant unresolved lead).

## Run 18

- **Date:** 2026-09-13
- **Query:** "IgA vasculitis clinical phenotype adult versus pediatric diagnosis outcomes" (with follow-up PubMed verification searches for Held et al., Levanon et al., Vivarelli et al., Maisons et al.)
- **Tool/database:** Consensus (primary), PubMed (verification)
- **Filters:** year_min=2022, exclude_preprints=true, medical_mode=true
- **Results returned:** 10
- **New candidates recorded:** 4 verified (Held et al. 2024 IJMS — IgAV-specific biomarker/pathogenesis study on Gd-IgA1/HMGB1/RAGE/PCDH1; Levanon et al. 2023 Medicine — comparative retrospective study of adult IgAV, pediatric IgAV, and IgAN; Vivarelli et al. 2024 Pediatric Nephrology — IPNA international clinical practice guideline for pediatric IgAN and IgAV nephritis, flagged as near-tier-1 evidence for evidence-reviewer's tier placement; Maisons et al. 2026 Eur J Intern Med — adult-onset IgAV clinical phenotype clustering study with independent validation cohort, note: has an associated corrigendum, flagged for evidence-reviewer)
- **Notes:** MAJOR FINDING — the Vivarelli IPNA guideline is a significant addition covering both IgAN and IgAV nephritis diagnosis/management for children, explicitly acknowledging the evidence gaps this project has independently identified (e.g., "little high-quality evidence" for pediatric IgAVN management, consistent with the Rohner et al. null finding on immunosuppressive regimen superiority already recorded). Several additional conference-abstract-only candidates found but excluded per the conference-abstract exclusion criterion (not recorded as source files): a POS0831 precursor abstract to the Levanon paper; a large adult IgAV cohort study (Hočevar et al., POS1167, n=362) with substantial short-term outcome data; and an outcomes study from a tertiary center (Salim et al., POS0500, n=72). A study protocol with no results yet (Jiang et al. 2025, BMJ Open, prospective pediatric IgAV cohort, n=478 planned) was noted but not recorded as it contains no extractable findings. A small case series (Marro et al. 2023, Pediatric Rheumatology, n=13 recurrent/persisting pediatric IgAV) was also seen but not recorded this session — flagged as a candidate for a future batch if deeper case-series-tier coverage of atypical IgAV courses is wanted. A narrative review (Stichert et al. 2026, J Am Acad Dermatol, adult IgAV) and another narrative review (Šestan et al. 2026, IJMS, vasculitis biomarkers) were also seen but not recorded — both would be background-tier (tier 8) only.

---

## Saturation summary across all sub-topics (end of this batch)

- **IgAN treatment/therapeutics:** NOT fully saturated but extensively covered — sparsentan, atrasentan, targeted-release budesonide, iptacopan, sibeprenlimab, atacicept, cemdisiran, ravulizumab, telitacicept, and SGLT2i-combination trials all have tier-1/tier-2 evidence now on file. Avacopan sub-topic specifically reached full 3-consecutive-query saturation with a confirmed evidence gap (no dedicated IgAN/IgAV avacopan trial exists in the literature as of this search). Narsoplimab: no positive trial result publication found (only case reports/trial-design abstracts); a citing commentary suggests the pivotal trial may have missed its primary endpoint, but this was not independently verified as a primary source — flagged as an evidence gap, not resolved by assumption.
- **IgAN mechanism/pathogenesis/biomarkers:** well covered but not saturated — gut-kidney axis, Gd-IgA1 origin, and novel mouse models represented; additional strong candidates (Wu et al. 2025/2026 C1GALT1 mouse studies, Gentile et al. 2024 unconventional T cells) were identified but not yet recorded, flagged for a follow-up batch.
- **IgAN diagnostics/clinical phenotypes:** well covered (MEST-C automation, systematic review of MEST-C/complement linkage, transplant-recurrence and prediction-tool validation studies referenced in Consensus results but not all individually recorded).
- **IgAV treatment/therapeutics:** covered via the large Rohner immunosuppression-outcomes cohort and background reviews, but primary controlled/comparative trial evidence remains sparse — the most substantial rituximab-in-IgAV dataset found (Trivioli et al., n=61) is conference-abstract-only and could not be recorded as a verified source. This is a genuine evidence gap distinct from IgAN, where controlled trial evidence is now comparatively rich.
- **IgAV mechanism/pathogenesis/biomarkers:** initial coverage established (Held et al. 2024) but not saturated — this sub-topic received comparatively less search depth than IgAN mechanism this session and would benefit from a dedicated follow-up batch.
- **IgAV diagnostics/clinical phenotypes:** well covered — the Barbour MEST-C validation study, Levanon comparative study, Maisons clustering study, and Vivarelli guideline collectively give this sub-topic good depth for a first production pass.

**Overall:** No sub-topic was searched to a full literal 3-consecutive-no-new-candidate saturation except avacopan (which did reach saturation with a confirmed gap). All other sub-topics were stopped at a bounded, well-populated sample per research-question.md's explicit non-exhaustive-retrieval guidance, given the very large size of this literature — not because new candidates stopped appearing.

---

## Run 19 — Targeted verification follow-up (not a new discovery search)

- **Date:** 2026-09-13
- **Purpose:** Orchestrator-requested follow-up on a specific verification gap flagged during evidence-reviewer's screening of sources/papers/10.1016-j.ejim.2026.106742.md (Maisons et al. 2026, EJIM, adult-onset IgAV clustering study). Goal: determine the substantive content of the associated corrigendum (PMID 42457434, DOI 10.1016/j.ejim.2026.107059) that could not be resolved at initial intake (abstract field empty). This is a bibliographic-verification follow-up on an already-recorded candidate, not a new literature search — no new candidate papers were sought or in scope.
- **Lookups/tools used, in order:**
  1. `mcp__PubMed__get_article_metadata` on PMIDs ["42457434","41644397"] — confirmed corrigendum's article type ("Published Erratum"), journal/volume/pages (Eur J Intern Med 151:107059), full author list match, pub date 2026-07-16; abstract field still empty.
  2. `mcp__PubMed__convert_article_ids` on PMID 42457434 (id_type=pmid) — no PMCID returned (no PMC full text exists for this item).
  3. `WebFetch` on `https://doi.org/10.1016/j.ejim.2026.107059` — 302 redirect to `https://linkinghub.elsevier.com/retrieve/pii/S095362052600364X`, redirect stub only, no article content.
  4. `WebFetch` on `https://linkinghub.elsevier.com/retrieve/pii/S095362052600364X` — same redirect-stub result, no content.
  5. `WebFetch` on `https://www.sciencedirect.com/science/article/pii/S095362052600364X` and on the `/pdf` variant of that URL — both HTTP 403 Forbidden.
  6. `WebFetch` on `https://api.crossref.org/works/10.1016/j.ejim.2026.107059` — confirmed Erratum/"update-to" relation to the original article's DOI, CC-BY license flag, zero references, no abstract field.
  7. `WebFetch` on `https://api.unpaywall.org/v2/10.1016/j.ejim.2026.107059` — reports is_oa=true/CC-BY but no direct PDF URL; best OA location is the same DOI landing page (which 403s on direct fetch).
  8. `WebFetch` on the EuropePMC REST API search for this DOI — metadata only, explicitly states "subscription required" for full text, no abstract.
  9. `WebSearch` with multiple reformulated queries combining the DOI/PMID/title with "corrigendum," "erratum," "we regret," "should read," "incorrectly," "correction" — no indexed snippet anywhere contains the corrigendum's actual corrected text.
  10. `WebFetch` on the EFIM (European Federation of Internal Medicine) reprint/summary page for the original article — makes no mention of any correction.
- **Filters applied:** none (targeted identifier/DOI lookups, not a filtered discovery search).
- **Results returned:** Corrigendum's *existence*, formal linkage to the original article, and bibliographic metadata were confirmed across all sources consulted. Its *substantive content* (what specific error/figure/number was corrected) was NOT obtainable through any tool available to literature-scout — every full-text access path was either paywalled (403), redirect-stub-only, or metadata-only with no abstract.
- **New candidates recorded:** 0 (this was a verification follow-up on an existing record, not a discovery search).
- **Outcome:** Updated the verification notes in `sources/papers/10.1016-j.ejim.2026.106742.md` with a dated addendum documenting this full attempt and its failure to access the corrigendum's content, per the anti-fabrication rule (state the access failure explicitly rather than guess). The existing caveat in `outputs/evidence-table.md` (row 40) and `outputs/research-report.md` that the cluster findings have not been checked against the corrigendum remains unresolved and is escalated back to the orchestrator/evidence-reviewer for a decision on how to treat this source going forward (e.g., retain with caveat, downgrade, or seek institutional access) — this is a recommendation, not a decision made here.
