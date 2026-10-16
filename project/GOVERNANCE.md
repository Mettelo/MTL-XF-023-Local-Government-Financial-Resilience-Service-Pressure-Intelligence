# MTL-XF-023 — Governance and decision controls

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Authority and accountability

**Director of Finance / Section 151 Officer (simulated)** owns business scope, prioritisation assumptions, accepted analytical limitations and investigation recommendations. The Mettelo review panel owns programme acceptance. Operational responsibilities are in [business context](BUSINESS_CONTEXT.md); delivery-role artefacts are in [the project brief](PROJECT_BRIEF.md).

The Data Governance Analyst approves source identity, metadata, licence evidence and field support. The Data Engineer owns transformations and reruns. Domain specialists approve interpretation; a distinct reviewer checks critical calculations and executes or reviews DT1–DT10. Combining delivery roles does not remove review accountability.

## Stage gates

| Gate | Accountability | Required review |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Publication, guidance, metadata link and selected item descriptions verified; acquired CSV endpoint/columns and metadata version alignment pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Finance / Section 151 Officer (simulated) + operational stakeholders | Within like-for-like authority responsibilities, compare three-transition sustained-growth cases ordered by absolute service-spend increase and by percentage increase on positive bases. Explain at least 90% of material total change through an accounting bridge or quantify why the hierarchy is non-additive. Attach funding/reserve/demand evidence requests before any resilience judgement. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

## Data/source control

Use the [source register](../data/SOURCE_REGISTER.md) as the authoritative evidence record. Preserve agreed URLs and explicitly label new required references, supplements and fallbacks. Record each actual file's resolved URL, retrieval UTC, release, scope, bytes, checksum and licence notices. Public access alone is not proof of unrestricted redistribution. No raw-data upload is part of this update.

Freeze input files only after the source-to-deliverable matrix passes; retain original bytes in an approved location and never overwrite a snapshot. A fallback must have a documented activation reason, compatible coverage and version-selection rule. Do not stack overlapping combined and fallback inputs.

## Domain interpretation

- Expenditure growth alone does not establish insolvency, a funding gap or statutory financial failure.
- Use nominal cash labels; real-terms claims require a registered deflator and disclosed base year.
- Do not invent budget, reserves or service-demand measures absent from the core file.

**Primary risk:** Incompatible authority responsibilities, accounting hierarchies and coverage-adjusted totals can change the interpretation of apparent financial pressure.

The [metric contract](DELIVERABLES.md) and [domain tests](ACCEPTANCE_CRITERIA.md) govern calculations. Thresholds/weights that are project choices must be labelled as such, with baseline and alternative scenarios; they are not official service standards. No automatic allocation or regulatory/professional certification is implied.

## Core and extension change control

Funding adequacy, reserve sustainability, budget/outturn variance and real-terms growth are separate analyses requiring compatible verified items or registered additional sources. The resilience deliverable is an evidence-based challenge assessment, not a solvency score.

Every source/scope change records requester, date, reason, old/new requirement, coverage/schema impact, affected KPIs/artefacts/tests, owner, reviewer and decision. Missing mandatory evidence blocks the dependent release; it is not resolved by relabelling a promised deliverable unavailable. Optional models need a naive baseline, appropriate holdout, leakage checks, uncertainty and a named reviewer.

## Reuse, information and repository controls

Never commit secrets, private correspondence or unnecessary personal details. Preserve suppression and publication notices. Check screenshots and exports for permitted publication. The team repository must be under Mettelo with individual member accounts, evidence-linked contributions and reviews. Record environment, manifest and final commit/tag so reviewers can reproduce results without paid-only access. Accurately describe verified participation; do not claim real-client employment, endorsement, operational adoption or achieved savings.
