# MTL-XF-023 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Local Government Finance & Service Planning Directorate. **Decision owner:** Director of Finance / Section 151 Officer (simulated). **Team:** 6–8. **Duration:** 8 weeks. **Review:** annual medium-term financial planning challenge, with quarterly management follow-up.

## Business problem and commission

The finance directorate must challenge expenditure assumptions across services without treating every spending increase as financial deterioration. Comparing an upper-tier council's social-care responsibilities with a district's narrower service remit can create misleading peer rankings. Parent totals, net expenditure and income items can also be counted inconsistently unless the analytical model follows the accounting structure.

> Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

## Core deliverable boundary

Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

**Optional / out of core:** Funding adequacy, reserve sustainability, budget/outturn variance and real-terms growth are separate analyses requiring compatible verified items or registered additional sources. The resilience deliverable is an evidence-based challenge assessment, not a solvency score.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Financial year × local-authority code × authority type × service/account line × published measure/unit. Preserve hierarchy levels and gross/net accounting distinctions; do not sum parent totals with children.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Every peer group documents equivalent service responsibilities and excluded authority types.
2. Every headline spend movement has a £-unit, cash/real-terms label and accounting-item reference.
3. Every resilience concern is classified as supported expenditure pressure, additional evidence required, or comparison invalid.

## Business questions

1. Which service lines account for most of the change in comparable net expenditure?
2. Which authorities show expenditure growth across at least three comparable years?
3. Do rankings change when comparing absolute change, percentage change and like-for-like authority peers?
4. Which reorganisations or accounting changes make trends unreliable?
5. What funding, reserves, inflation and demand data are required before a resilience judgement?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the annual medium-term financial planning challenge, with quarterly management follow-up, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Finance / Section 151 Officer (simulated) owns business approval. |
| Data Governance Analyst | Own the MTL-XF-023 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Incompatible authority responsibilities, accounting hierarchies and coverage-adjusted totals can change the interpretation of apparent financial pressure. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-023 scope. |
| BI Developer | Implement the annual medium-term financial planning challenge, with quarterly management follow-up overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Local Government Finance Analyst | Approve gross/net mappings, service hierarchies and the change bridge; sign off five source reconciliations. |
| Service Planning Analyst | Translate up to ten authority/service signals into financial-plan challenge questions and missing evidence. |
| Financial Assurance Analyst | Test reorganisations, negative bases and additive totals; review all eight metric definitions. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Publication, guidance, metadata link and selected item descriptions verified; acquired CSV endpoint/columns and metadata version alignment pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Finance / Section 151 Officer (simulated) + operational stakeholders | Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
