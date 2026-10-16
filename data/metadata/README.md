# MTL-XF-023 — Metadata, lineage and freeze evidence

Metadata makes local government financial resilience, service spend & budget pressure intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Financial year × local-authority code × authority type × service/account line × published measure/unit. Preserve hierarchy levels and gross/net accounting distinctions; do not sum parent totals with children.

## Metric definition coverage

- Comparable service outturn: Published expenditure for the selected service/account and unit; gross and net remain distinct.
- Annual cash change: Current comparable outturn minus prior-year comparable outturn.
- Annual percentage change: 100 × (current / previous − 1) only for a meaningful positive base; flag zero or negative bases.
- Service expenditure share: 100 × comparable service net expenditure / compatible total net expenditure; exclude invalid or non-additive denominators.
- Contribution to change: Service cash change / total cash change, with reconciliation and warning when the total is near zero.
- Sustained growth: Growth in each of three consecutive comparable year transitions; incomplete histories are unclassified.
- Peer deviation: Authority growth minus median growth of authorities with equivalent responsibilities.
- Continuity coverage: Comparable authority-year records / expected authority-year records.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
