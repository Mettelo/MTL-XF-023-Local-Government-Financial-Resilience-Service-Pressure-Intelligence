# MTL-XF-023 — Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Local Government Finance & Service Planning Directorate  
**Accountable simulated executive:** Director of Finance / Section 151 Officer (simulated)  
**Sector:** Local Government / Public Finance  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** annual medium-term financial planning challenge, with quarterly management follow-up

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business problem

The finance directorate must challenge expenditure assumptions across services without treating every spending increase as financial deterioration. Comparing an upper-tier council's social-care responsibilities with a district's narrower service remit can create misleading peer rankings. Parent totals, net expenditure and income items can also be counted inconsistently unless the analytical model follows the accounting structure.

## Commissioned decision

> Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

## Practical use

During the financial-plan review, the Director opens an authority's change bridge and sees whether adult social care, children's services or another service explains the movement in comparable net expenditure. The finance lead compares equivalent authority types and requests funding, reserve and demand evidence before deciding whether the signal indicates a resilience concern or an expected service change.

The full [business context](project/BUSINESS_CONTEXT.md) names operational stakeholders, decisions, risks and proposed benefit measures.

## What must be delivered

1. Produce authority/service spend bridges explaining at least 90% of material total cash change or explicitly account for the residual.
2. Create like-for-like peer groups and show the effect of authority reorganisations on three-year growth.
3. Shortlist up to ten authority/service cases for financial-plan challenge; compare absolute and percentage pressure and record evidence still required.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

**Extensions:** Funding adequacy, reserve sustainability, budget/outturn variance and real-terms growth are separate analyses requiring compatible verified items or registered additional sources. The resilience deliverable is an evidence-based challenge assessment, not a solvency score.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Every peer group documents equivalent service responsibilities and excluded authority types.
2. Every headline spend movement has a £-unit, cash/real-terms label and accounting-item reference.
3. Every resilience concern is classified as supported expenditure pressure, additional evidence required, or comparison invalid.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement.

- Expenditure growth alone does not establish insolvency, a funding gap or statutory financial failure.
- Use nominal cash labels; real-terms claims require a registered deflator and disclosed base year.
- Do not invent budget, reserves or service-demand measures absent from the core file.

## Team and stakeholder ownership

Director of Finance / Section 151 Officer (simulated) approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-023-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
