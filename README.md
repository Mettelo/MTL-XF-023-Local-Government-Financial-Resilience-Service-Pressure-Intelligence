# MTL-XF-023 — Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Local Government Finance & Service Planning Directorate  
**Accountable simulated executive:** Director of Finance / Section 151 Officer (simulated)  
**Sector:** Local Government / Public Finance  
**Team:** 3–5 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** annual medium-term financial planning challenge, with quarterly management follow-up

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated finance directorate is preparing its annual medium-term financial-plan challenge. Service finance leads must explain expenditure assumptions, while the Director of Finance needs an evidence-led agenda for the services and comparable authorities requiring deeper scrutiny.

## Business problem

The finance team must decide which service expenditure assumptions deserve challenge before the next medium-term plan is finalised. Current comparisons show headline authority growth but do not consistently explain which services contributed to it, whether the peer councils have equivalent responsibilities, or whether a boundary change breaks the trend.

This leaves two competing risks: accepting a material pressure without an adequate explanation, or challenging an apparent outlier created by an invalid comparison. The commission is to produce a comparable service-spend change bridge and a documented challenge agenda. The core outturn data supports questions about expenditure pressure; funding adequacy, reserves and budget variance need their own compatible evidence.

## Commissioned decision

> Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

## Practical use

During the annual challenge meeting, the Head of Financial Planning opens an authority's net-current-service-expenditure bridge and identifies which declared service lines explain the cash movement. The relevant adult or children's services finance lead compares the movement with councils carrying equivalent responsibilities and checks whether reorganisation or incomplete returns change the interpretation.

The Director records the case as supported expenditure pressure, further evidence required or comparison invalid. A supported pressure becomes a focused question for the service plan, with a request for demand, funding and reserve evidence as relevant. The team does not propose a service cut or declare an authority financially unsustainable from outturn growth alone.

**Management handover:** A financial-plan challenge pack containing reconciled service-change bridges, a documented peer map, absolute/percentage pressure scenarios and a challenge log. Each challenge must identify the service finance owner, accounting item, comparison basis and missing evidence needed for the next planning decision.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

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
