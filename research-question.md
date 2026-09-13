# Research Question

> Single source of truth for scope, screening criteria, and constraints. `literature-scout`, `evidence-reviewer`, and `research-writer` must all treat this file as authoritative and must not narrow, broaden, or reinterpret it on their own judgment. Changes to this file require re-running affected downstream steps (see Change Log at the bottom) — it is not append-only in the way `search-log.md` is, but every substantive change must be logged there.

- **Status:** active
- **Scope type:** clinical, with a basic/mechanistic-research component
- **Owner:** drbathish@gmail.com

## Research question

What are the recent (2022–present) advances in the diagnosis, pathogenesis, and treatment of IgA nephropathy (IgAN) and IgA vasculitis (IgAV, including IgA vasculitis nephritis), across both clinical and basic/mechanistic research?

## Scope framework

**Population / disease / model:**
Human patients — pediatric and adult — with biopsy-confirmed or clinically diagnosed IgA nephropathy (IgAN), and/or IgA vasculitis (IgAV; formerly Henoch–Schönlein purpura), including IgA vasculitis nephritis (IgAVN). For basic/mechanistic studies, also includes human kidney tissue/biopsy specimens, human cell lines or primary cells, and animal models specifically used to model IgAN or IgAV pathogenesis (e.g., Gd-IgA1 immune complex models, HSP mouse models).

**Intervention / exposure / biomarker / mechanism:**
Any of the following, when specific to IgAN or IgAV:
- Pharmacologic or biologic therapies (e.g., SGLT2 inhibitors, endothelin receptor antagonists, targeted-release budesonide, complement pathway inhibitors such as iptacopan/avacopan/narsoplimab, BAFF/APRIL inhibitors such as telitacicept/atacicept/blisibimod, B-cell-depleting agents such as rituximab, RAAS blockade, mineralocorticoid receptor antagonists, immunosuppressants)
- Diagnostic or prognostic biomarkers (e.g., galactose-deficient IgA1 [Gd-IgA1], anti-glycan autoantibodies, urinary/serum multi-omics markers)
- Pathogenic mechanisms or pathways (e.g., mucosal immunity and the gut–kidney axis, complement activation including the lectin pathway, genetic/genomic risk loci, immune complex formation and mesangial deposition)

**Comparator (where applicable):**
Placebo, standard/supportive care, or an active comparator, for interventional and comparative observational studies. Not required for single-arm observational, descriptive, or mechanistic/preclinical studies.

**Outcomes / endpoints:**
- Clinical: proteinuria/albuminuria change, eGFR trajectory or decline, remission/relapse rates, progression to kidney failure or end-stage kidney disease, adverse events/safety, extra-renal disease activity (for IgAV)
- Mechanistic: pathway activation or inhibition, biomarker levels, histological/immunofluorescence findings, gene expression or other omics endpoints

**Study types (evidentiary priority, highest to lowest):**
1. Systematic reviews and meta-analyses (including Cochrane reviews)
2. Randomized controlled trials (RCTs)
3. Prospective cohort studies
4. Retrospective cohort / real-world studies with a defined comparator or control period
5. Case series (n ≥ 10), cross-sectional studies
6. Mechanistic / preclinical studies (animal models, in vitro, ex vivo, multi-omics, network pharmacology) relevant to pathogenesis or a novel therapeutic target
7. Case reports and case series with n < 10 — include only when illustrating a genuinely novel or emerging intervention/mechanism, or a clinically significant diagnostic pitfall; always flagged as low evidentiary weight
8. Narrative reviews — usable for background/context only, never as a primary evidence source in the evidence table

**Date range:** January 2022 – present

**Language:** English. Non-English studies are excluded unless a full text or authoritative English abstract is available and independently verifiable; if excluded solely for language, log this explicitly rather than omitting silently.

## Inclusion criteria

- Peer-reviewed journal publication (or a Cochrane systematic review)
- Directly addresses IgA nephropathy and/or IgA vasculitis (including IgAV nephritis)
- Published January 2022 or later
- English language (or independently verifiable English translation)
- Reports on human subjects, human-derived samples, or an animal/cell model explicitly used to study IgAN or IgAV pathogenesis
- Falls into one of the study types listed above

## Exclusion criteria

- Preprints not yet peer-reviewed (log separately if found; do not include in the evidence table)
- Conference abstracts without an associated full-text peer-reviewed publication
- Editorials, letters, or commentaries with no original data (background-context use only, never as an evidence-table entry)
- Studies where IgAN/IgAV is incidental rather than a primary focus (e.g., broad CKD cohorts that only mention IgAN as one of many etiologies without IgAN/IgAV-specific analysis)
- Duplicate publications of the same patient cohort/dataset (keep the most complete/most recent; note the duplicate in the source record)
- Studies whose bibliographic details cannot be independently verified (per the anti-fabrication rules in the root `CLAUDE.md`)
- Single-patient case reports that do not illustrate a novel/emerging intervention or diagnostic pitfall (per study-type priority above)

## Topic-specific constraints

- Where IgAN and IgAV findings are both reported (they share overlapping pathogenesis and are frequently studied together, e.g., shared BAFF/APRIL-targeted therapies), record and report them separately in the evidence table — do not merge findings across the two diseases even when a single study covers both.
- Treat therapies newly approved or in late-stage trials for IgAN (e.g., sparsentan, iptacopan, targeted-release budesonide) as high-relevance even in IgAV-focused searches, since IgAV literature explicitly discusses extrapolating from IgAN trial data — but flag any such extrapolation as indirect evidence, not IgAV-specific evidence.
- Journal impact (e.g., journal quartile/SJR via Consensus, or venue reputation) is a secondary ranking signal only — never a substitute for methodological quality when prioritizing which studies to fully screen first.
- Given the size of this literature (thousands of PubMed hits per topic as of the initial scoping search), `literature-scout` should not attempt exhaustive retrieval. A search run is adequately bounded once it has covered: (a) the highest-quality systematic reviews/RCTs/Cochrane reviews available in the date range, and (b) a representative, saturation-tested sample of lower-tiers relevant to the specific sub-topic the user is asking about at the time. If the user's request implies a narrower sub-topic (a specific drug, mechanism, or population), treat that request as a temporary narrowing of this file's scope for that run only, and note the narrowing in `search-log.md` rather than editing this file.

## Change log

| Date | Change | Reason |
|------|--------|--------|
| 2026-09-13 | Initial version created | Establish scope for IgAN/IgAV literature review following architecture review and literature-scout test run |
