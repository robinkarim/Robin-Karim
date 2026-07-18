# Migration and Implementation Notes
## ServiceNow / Azure Cutover — Reporting Module

**Structured in:** DITA XML, managed through Confluence and Jira
**Audience:** Migration team, platform owners, downstream reporting consumers

---

### 1. Scope of This Cutover

Migrates the incident and request reporting module from the legacy on-premise instance to the ServiceNow cloud platform, hosted on Azure infrastructure. Does not cover the change management module, which follows in a later phase.

### 2. Pre-Cutover Checklist

- Historical data validated in the staging environment against source-system record counts (target: 100% match within tolerance for known duplicate-record cleanup)
- Dashboard parity confirmed against the current-state monthly reporting package
- Access groups provisioned and tested in staging with a pilot group of 5 reporting consumers
- Rollback plan documented and reviewed with the platform owner

### 3. Cutover Sequence

1. Freeze write access to the legacy reporting module (read-only mode) at the scheduled cutover start time.
2. Run the final incremental data sync to capture any records created since the last staging sync.
3. Validate record counts between legacy and new environment match the freeze-point baseline.
4. Redirect reporting consumers to the new environment via updated bookmarks/links distributed in advance.
5. Monitor the new environment for the first business day at elevated attention, with the platform team on standby.
6. Decommission legacy reporting module write access entirely once the new environment is confirmed stable (typically 5 business days post-cutover).

### 4. Known Issues Carried Into Cutover

**Issue: Duplicate records from a historical data-entry error.** Approximately 40 records in the legacy system share duplicate ticket numbers due to a data-entry issue from several years prior. These are flagged in the migration mapping rather than silently deduplicated, since deduplication logic could not be validated with full confidence against the original source records.

**Issue: Timezone display difference.** The new platform displays timestamps in the viewer's local timezone by default, while the legacy system displayed a fixed corporate timezone regardless of viewer location. This is a known, intentional behavior difference — not a defect — and is called out explicitly in cutover communications to avoid confusion during the first reporting cycle.

### 5. Rollback Plan

If a cutover-blocking issue is identified within the first 4 hours, write access reverts to the legacy module and the new environment is held in read-only mode for troubleshooting. A rollback beyond 4 hours requires platform owner and change advisory board approval due to the data-freshness gap that would need to be reconciled.

---
*This document has been generalized from production migration documentation. Record counts, timelines, and specific data issues have been altered.*
