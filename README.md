# MTL-XF-023 — Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Local Government Finance & Service Planning Directorate  
**Sector:** Local Government / Public Finance  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-023-Local-Government-Financial-Resilience-Service-Pressure-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence.** A council finance directorate needs to identify which services are driving expenditure pressure, which authorities are seeing persistent growth, and where medium-term financial plans need deeper challenge.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Which comparable authorities and service lines show sustained expenditure pressure requiring medium-term financial-plan challenge, and what further funding or reserve evidence is needed?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- Which service lines account for most of the change in comparable net expenditure?
- Which authorities show expenditure growth across at least three comparable years?
- Do rankings change when comparing absolute change, percentage change and like-for-like authority peers?
- Which reorganisations or accounting changes make trends unreliable?
- What funding, reserves, inflation and demand data are required before a resilience judgement?

## Approved data and cohort

MHCLG Revenue Outturn multi-year dataset, covering 2017/18–2025/26. The current CSV is 23.2 MB.

Freeze the agreed Revenue Outturn time-series v4 CSV and its actual metadata, with intended 2017/18–2025/26 coverage. Analyse outturn service expenditure only within compatible definitions and authority responsibilities. Budget-versus-outturn, funding gaps and reserves are conditional extensions requiring additional registered sources.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Produce authority/service spend bridges explaining at least 90% of material total cash change or explicitly account for the residual.
2. Create like-for-like peer groups and show the effect of authority reorganisations on three-year growth.
3. Shortlist up to ten authority/service cases for financial-plan challenge; compare absolute and percentage pressure and record evidence still required.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

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

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Local Government Finance & Service Planning Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 023 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 023 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 023 dashboard measures and test every visible filter. |
| Local Government Finance Analyst | Approve gross/net mappings, service hierarchies and the change bridge; sign off five source reconciliations. |
| Service Planning Analyst | Translate up to ten authority/service signals into financial-plan challenge questions and missing evidence. |
| Financial Assurance Analyst | Test reorganisations, negative bases and additive totals; review all eight metric definitions. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Expenditure growth alone does not establish insolvency, a funding gap or statutory financial failure.
- Use nominal cash labels; real-terms claims require a registered deflator and disclosed base year.
- Do not invent budget, reserves or service-demand measures absent from the core file.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-023-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
