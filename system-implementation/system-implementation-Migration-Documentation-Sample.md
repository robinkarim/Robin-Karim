# Migration Documentation
## Legacy Student Information System → Enterprise Platform: Enrollment Data Mapping

**Audience:** Migration team, downstream data consumers (state reporting, transportation, food services)

---

### 1. Purpose

Maps enrollment data fields from the legacy system to the new enterprise platform, documenting where field structures differ and how those differences are resolved for the cutover.

### 2. Field Mapping Summary

| Legacy Field | New Platform Field | Notes |
|---|---|---|
| `STU_STATUS` (single code, 6 values) | `enrollment_status` (structured: status + sub-status) | Legacy code 4 ("Inactive-Other") splits into 3 new sub-statuses; migration team manually reviewed each Code 4 record to assign the correct sub-status rather than defaulting all of them to one value |
| `GRADE_LVL` (numeric, includes -1 for pre-K) | `grade_level` (enumerated, includes "PK") | Direct mapping with value translation |
| `HOME_LANG` (free text) | `home_language` (controlled list, ISO 639 codes) | Free-text values were reviewed and matched to the closest controlled-list code; approximately 3% could not be confidently matched and were flagged for school-level follow-up rather than guessed |
| `SPED_FLAG` (Y/N) | `iep_status` (structured, multiple values) | Legacy Y/N does not capture IEP status detail; migration team cross-referenced with the special education system of record to populate the new structured field accurately rather than defaulting all "Y" records to a single generic status |

### 3. Records Requiring Manual Review

Approximately 3% of home-language records and all Code 4 enrollment-status records required manual review rather than automated mapping, due to ambiguity that could not be resolved with confidence through a translation table alone. These were tracked in a dedicated review log and signed off by the enrollment data owner before cutover, rather than migrated with a best-guess default.

### 4. Downstream Impact

Transportation and food services reporting, both of which consume enrollment status and grade level fields, were validated against the new field structure in the staging environment two weeks before cutover to confirm their existing reports would continue to function without a rebuild.

### 5. Cutover Data Freeze

Enrollment data is frozen for new entries 24 hours before cutover to allow the final migration pass and validation to run against a stable dataset. Any enrollment change needed during the freeze window is logged manually and applied to the new system directly after cutover, rather than being entered into the legacy system and re-migrated.

---
*This document has been generalized from production migration documentation for a multi-year student information system migration. Field names and percentages have been altered.*
