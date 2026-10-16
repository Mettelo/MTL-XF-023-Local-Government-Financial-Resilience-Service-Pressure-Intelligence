# MTL-XF-023 — Required deliverables

**Commissioned decision:** Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

All locations below refer to the team's delivery repository. The master repository defines the requirements and contains no completed analysis. Owners are assigned from [the project roles](PROJECT_BRIEF.md).

## D1 — Discovery & decision requirements

**Due:** Week 1  
**Team artefact location:** `docs/01-discovery/`

Decision statement; stakeholder map; as-is reporting to investigation-review process; at least eight prioritised requirements. Answer these questions: Which service lines account for most of the change in comparable net expenditure? Which authorities show expenditure growth across at least three comparable years? Do rankings change when comparing absolute change, percentage change and like-for-like authority peers? Which reorganisations or accounting changes make trends unreliable? What funding, reserves, inflation and demand data are required before a resilience judgement?

**Acceptance evidence:** All requirements have an owner, priority, deliverable and test ID; domain analyst approves scope.

## D2 — Governed sources & cohort

**Due:** Week 2  
**Team artefact location:** `docs/02-data-governance/; data/`

Freeze the agreed Revenue Outturn time-series v4 CSV and its actual metadata, with intended 2017/18–2025/26 coverage. Analyse outturn service expenditure only within compatible definitions and authority responsibilities. Budget-versus-outturn, funding gaps and reserves are conditional extensions requiring additional registered sources. Register exact files, metadata, licences, checksums, coverage and critical fields; record rejection of unavailable dimensions.

**Acceptance evidence:** 100% of inputs registered; no claimed freeze until acquisition evidence exists.

## D3 — Reproducible analytical model

**Due:** Week 3  
**Team artefact location:** `src/; sql/; docs/03-data-model/`

Financial year × local-authority code × authority type × service/account line × published measure/unit. Preserve hierarchy levels and gross/net accounting distinctions; do not sum parent totals with children. Deliver load, type checks, hierarchy handling, lineage, exclusions and environment instructions.

**Acceptance evidence:** A second member regenerates equivalent curated outputs from identical inputs; no unexplained duplicate analytical keys.

## D4 — Quality & reconciliation

**Due:** Week 3  
**Team artefact location:** `docs/04-data-quality/; tests/`

Profile missingness, suppression, valid values, keys and join coverage. Reconcile five authority/service totals and one parent-child accounting bridge. Demonstrate correct handling of zero and negative prior expenditure. Show a reorganised authority is excluded or bridged with documented methodology. Verify no budget variance or reserve-risk label is produced from outturn alone.

**Acceptance evidence:** Every input row is accounted for as retained, excluded or quarantined; five published cells reconcile within declared rounding.

## D5 — KPI catalogue

**Due:** Week 4  
**Team artefact location:** `docs/05-kpi-catalogue/`

Define all 8 measures listed below with formula, grain, denominator, unit, source fields, exclusions, owner, refresh and limitations.

**Acceptance evidence:** 100% headline metrics trace to source fields and tested transformations; conditional unavailable measures are explicitly marked.

## D6 — Domain analytical assessment

**Due:** Week 5  
**Team artefact location:** `analysis/; docs/06-analysis/`

Produce authority/service spend bridges explaining at least 90% of material total cash change or explicitly account for the residual. Create like-for-like peer groups and show the effect of authority reorganisations on three-year growth.

**Acceptance evidence:** At least five evidence-backed findings state period, population, comparison, magnitude, uncertainty and limitation; negative findings count.

## D7 — Investigation decision framework

**Due:** Week 6  
**Team artefact location:** `docs/07-decision-framework/`

Shortlist up to ten authority/service cases for financial-plan challenge; compare absolute and percentage pressure and record evidence still required. Record eligibility, thresholds, weights if used, reason codes and manual review triggers.

**Acceptance evidence:** Every shortlisted case has metrics, rationale, owner and evidence gaps; at least two scenarios compared; fewer than ten is valid where evidence is insufficient.

## D8 — BI decision-support product

**Due:** Draft Week 6; final Week 7  
**Team artefact location:** `dashboard/`

Executive overview answering 'Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?' plus diagnostic and data-quality views; visible periods, units, denominator notes, resettable filters and accessible labels.

**Acceptance evidence:** Five headline measures reconcile; every filter tested; export screenshots/PDF plus reproducible build or free access instructions.

## D9 — Independent assurance & UAT

**Due:** Week 7  
**Team artefact location:** `docs/08-assurance-uat/`

At least ten scenarios including the four project-specific tests below; requirement-to-test matrix, expected/actual evidence, defect log and simulated stakeholder feedback.

**Acceptance evidence:** No unresolved critical/high defect; accepted lower-severity limitations have a named reviewer and explicit impact.

## D10 — Technical & operational handover

**Due:** Week 8  
**Team artefact location:** `docs/09-technical-handover/`

Clean setup, architecture, frozen input manifest, run/refresh steps, output checks, troubleshooting and change-control process for Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence.

**Acceptance evidence:** Another member reproduces the core outputs without undocumented edits and records environment, duration and discrepancies.

## D11 — Executive recommendation

**Due:** Week 8  
**Team artefact location:** `deliverables/`

Maximum two-page briefing and 15–20 minute presentation: commissioned decision, five findings, investigation shortlist, sensitivity, missing evidence, responsibilities and next review.

**Acceptance evidence:** Every quantitative claim links to an artefact/metric; no unsupported causal, policy or operational guarantee.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8  
**Team artefact location:** `CONTRIBUTIONS.md; delivery issues/PRs`

Record who delivered and reviewed each MTL-XF-023 work package, including domain, governance, engineering, BI and assurance contributions.

**Acceptance evidence:** Every member links to substantive artefacts and review/presentation evidence; commit count alone is insufficient.

## Required KPI definitions

| Metric | Required definition / calculation |
| --- | --- |
| Comparable service outturn | Published expenditure for the selected service/account and unit; gross and net remain distinct. |
| Annual cash change | Current comparable outturn minus prior-year comparable outturn. |
| Annual percentage change | 100 × (current / previous − 1) only for a meaningful positive base; flag zero or negative bases. |
| Service expenditure share | 100 × comparable service net expenditure / compatible total net expenditure; exclude invalid or non-additive denominators. |
| Contribution to change | Service cash change / total cash change, with reconciliation and warning when the total is near zero. |
| Sustained growth | Growth in each of three consecutive comparable year transitions; incomplete histories are unclassified. |
| Peer deviation | Authority growth minus median growth of authorities with equivalent responsibilities. |
| Continuity coverage | Comparable authority-year records / expected authority-year records. |

For every metric record business purpose, formula, source fields, grain, unit, numerator/denominator, exclusions, suppression, zero-base behaviour, owner, refresh and test evidence. Do not populate conditional metrics from invented fields.

## Mandatory domain scenarios

1. Reconcile five authority/service totals and one parent-child accounting bridge.
2. Demonstrate correct handling of zero and negative prior expenditure.
3. Show a reorganised authority is excluded or bridged with documented methodology.
4. Verify no budget variance or reserve-risk label is produced from outturn alone.

## Review gates

Week 2: cohort and source approval. Week 4: model, DQ and metrics approval. Week 6: analytical and decision-framework review. Week 8: UAT, independent rerun and final panel review. Record reviewer, date, artefact version and decision at every gate.
