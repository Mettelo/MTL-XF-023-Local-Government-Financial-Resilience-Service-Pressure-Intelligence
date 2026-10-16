# MTL-XF-023 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Required reference: https://assets.publishing.service.gov.uk/media/6ac3c069241ecad55a9793ae/Revenue_Outturn_metadata.ods . Use its dictionary to map selected items, including candidate RS_asc_net_exp, RS_csc_net_exp and RS_totsx_net_exp. Normalise selected wide columns into the documented analytical grain; confirm names in the frozen version.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
