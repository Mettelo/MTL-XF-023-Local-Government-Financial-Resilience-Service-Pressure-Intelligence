# MTL-XF-023 — Data workspace

## Required sources and cohort

MHCLG Revenue Outturn multi-year dataset, covering 2017/18–2025/26. The current CSV is 23.2 MB.

Freeze the agreed Revenue Outturn time-series v4 CSV and its actual metadata, with intended 2017/18–2025/26 coverage. Analyse outturn service expenditure only within compatible definitions and authority responsibilities. Budget-versus-outturn, funding gaps and reserves are conditional extensions requiring additional registered sources.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Financial year × local-authority code × authority type × service/account line × published measure/unit. Preserve hierarchy levels and gross/net accounting distinctions; do not sum parent totals with children.

## Required metric contract

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

## Mandatory quality risks

- Expenditure growth alone does not establish insolvency, a funding gap or statutory financial failure.
- Use nominal cash labels; real-terms claims require a registered deflator and disclosed base year.
- Do not invent budget, reserves or service-demand measures absent from the core file.

1. Reconcile five authority/service totals and one parent-child accounting bridge.
2. Demonstrate correct handling of zero and negative prior expenditure.
3. Show a reorganised authority is excluded or bridged with documented methodology.
4. Verify no budget variance or reserve-risk label is produced from outturn alone.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
