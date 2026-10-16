# MTL-XF-023 — Required deliverables and metric contracts

**Decision:** Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?  
**Business acceptance:** Director of Finance / Section 151 Officer (simulated)  
**Core scope:** Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the annual medium-term financial planning challenge, with quarterly management follow-up, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. Financial year × local-authority code × authority type × service/account line × published measure/unit. Preserve hierarchy levels and gross/net accounting distinctions; do not sum parent totals with children.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'Incompatible authority responsibilities, accounting hierarchies and coverage-adjusted totals can change the interpretation of apparent financial pressure.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 8 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Produce authority/service spend bridges explaining at least 90% of material total cash change or explicitly account for the residual. Create like-for-like peer groups and show the effect of authority reorganisations on three-year growth.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of Finance / Section 151 Officer (simulated) (business acceptance)

Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the annual medium-term financial planning challenge, with quarterly management follow-up. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of Finance / Section 151 Officer (simulated): decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Comparable service outturn | Published expenditure for the selected service/account and unit; gross and net remain distinct. |
| Annual cash change | Current comparable outturn minus prior-year comparable outturn. |
| Annual percentage change | 100 × (current / previous − 1) only for a meaningful positive base; flag zero or negative bases. |
| Service expenditure share | 100 × comparable service net expenditure / compatible total net expenditure; exclude invalid or non-additive denominators. |
| Contribution to change | Service cash change / total cash change, with reconciliation and warning when the total is near zero. |
| Sustained growth | Growth in each of three consecutive comparable year transitions; incomplete histories are unclassified. |
| Peer deviation | Authority growth minus median growth of authorities with equivalent responsibilities. |
| Continuity coverage | Comparable authority-year records / expected authority-year records. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. Every peer group documents equivalent service responsibilities and excluded authority types.
2. Every headline spend movement has a £-unit, cash/real-terms label and accounting-item reference.
3. Every resilience concern is classified as supported expenditure pressure, additional evidence required, or comparison invalid.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
