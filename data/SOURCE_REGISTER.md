# MTL-XF-023 — Source register and verification record

**Project:** Local Government Financial Resilience, Service Spend & Budget Pressure Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

Comparable English authority/service outturn analysis from the agreed multi-year CSV with the official metadata workbook as a required reference. Focus on net current service expenditure and declared service hierarchies. Preserve published England/class totals as source totals and distinguish them from sums of received LA returns.

**Outside core:** Funding adequacy, reserve sustainability, budget/outturn variance and real-terms growth are separate analyses requiring compatible verified items or registered additional sources. The resilience deliverable is an evidence-based challenge assessment, not a solvency score.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| Official multi-year publication | https://www.gov.uk/government/statistics/local-authority-revenue-expenditure-and-financing-england-revenue-outturn-multi-year-data-set |
| Official dataset guidance | https://www.gov.uk/government/statistics/local-authority-revenue-expenditure-and-financing-england-revenue-outturn-multi-year-data-set/revenue-outturn-multi-year-data-set-guidance |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The publication advertises 2017/18–2025/26 coverage, while the guidance's introductory text still names an earlier endpoint: reconcile this through the actual release log. Guidance describes wide authority/year rows, £ thousands in nominal cash, metadata item definitions and authority histories. Published England/class totals may include coverage adjustments, so they need not equal available-return sums.

**Field/reference mapping and acquisition instructions:** Required reference: https://assets.publishing.service.gov.uk/media/6ac3c069241ecad55a9793ae/Revenue_Outturn_metadata.ods . Use its dictionary to map selected items, including candidate RS_asc_net_exp, RS_csc_net_exp and RS_totsx_net_exp. Normalise selected wide columns into the documented analytical grain; confirm names in the frozen version.

**Remaining status:** Publication, guidance, metadata link and selected item descriptions verified; acquired CSV endpoint/columns and metadata version alignment pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed core input 1

```text
https://assets.publishing.service.gov.uk/media/6ab26ffffe72ed1e2b02ee74/Revenue_Outturn_time_series_data_v4.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### R1 — Required metadata workbook

```text
https://assets.publishing.service.gov.uk/media/6ac3c069241ecad55a9793ae/Revenue_Outturn_metadata.ods
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Reference metadata; match its version to the analytical input.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
