# MTL-XF-023 — Acceptance criteria and domain tests

**Business decision owner:** Director of Finance / Section 151 Officer (simulated). **Decision:** Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Finance / Section 151 Officer (simulated) |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 8 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Finance / Section 151 Officer (simulated) |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Finance / Section 151 Officer (simulated) / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Every peer group documents equivalent service responsibilities and excluded authority types.
2. Every headline spend movement has a £-unit, cash/real-terms label and accounting-item reference.
3. Every resilience concern is classified as supported expenditure pressure, additional evidence required, or comparison invalid.

## Required prioritisation and sensitivity

Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reconcile five authority/service totals and one parent-child accounting bridge. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Demonstrate correct handling of zero and negative prior expenditure. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Show a reorganised authority is excluded or bridged with documented methodology. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Verify no budget variance or reserve-risk label is produced from outturn alone. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | Outturn rises from £10,000 thousand to £12,000 thousand | Change = £2 million and +20%; displayed unit is explicit. |
| DT6 | England source total differs from sum of available LA returns | Preserve both; explain grossing/coverage rather than force equality. |
| DT7 | A district and an upper-tier authority have different service remits | They do not enter the same unexplained peer ranking. |
| DT8 | Service components explain £9m of a £10m increase | Bridge coverage = 90%; £1m residual is visible. |
| DT9 | Parent total and its child line are both selected | No aggregate double count; hierarchy choice is explicit. |
| DT10 | Outturn grows but reserve/funding evidence is absent | No solvency judgement or funding gap is fabricated. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

**Optional extensions:** Funding adequacy, reserve sustainability, budget/outturn variance and real-terms growth are separate analyses requiring compatible verified items or registered additional sources. The resilience deliverable is an evidence-based challenge assessment, not a solvency score.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
