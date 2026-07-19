# Gap and Impact Analysis
## Legacy Ticketing Tool → Cloud ITSM Platform

**Prepared for:** Change Advisory Board
**Purpose:** Identify functional and process gaps between current and future state, and assess downstream impact before cutover.

---

### 1. Current State Summary

The legacy tool handles incident and request management through a single on-premise instance, with manual account provisioning, no native SSO, and reporting built on a static monthly export rather than live dashboards.

### 2. Future State Summary

The target platform provides SSO-based authentication, live reporting dashboards, and a configurable workflow engine that supports both incident and request management natively.

### 3. Gap Analysis

| Area | Current State | Future State | Gap |
|---|---|---|---|
| Authentication | Manual local accounts | SSO via identity provider | New provisioning workflow must be designed and tested before cutover |
| Reporting | Static monthly export, manually reconciled | Live dashboard, real-time | Historical data must be reshaped to match new schema; some legacy fields have no direct equivalent |
| Escalation Rules | Configured per-agent, undocumented in places | Centrally configured, rule-based | Existing informal escalation practices must be documented and rebuilt as explicit rules, or they will be lost |
| Mobile Access | Not supported | Native mobile app | No gap to close, but introduces a new support surface (device management, app-level access policy) |
| Attachment Size Limit | 10 MB | 25 MB | Future state removes an existing user pain point; no negative impact identified |

### 4. Impact Assessment

**Process Impact:** Service desk agents will need to adjust to a different queue-assignment interface. Training time is estimated at half a day per agent based on platform vendor documentation and a pilot group walkthrough.

**Data Impact:** Approximately 8% of legacy tickets contain free-text fields that do not map cleanly to the new categorized schema. These will be migrated as-is into a notes field rather than forced into a category, to avoid introducing inaccurate historical data.

**People Impact:** The informal escalation practices currently held by two senior agents represent a single point of knowledge risk. This analysis recommends those practices be documented as formal rules during Discovery, rather than migrated informally, so the knowledge does not depend on those two individuals going forward.

**Risk if Gaps Are Not Addressed:** Without a formal escalation rule-build, Priority 1 tickets could default to standard SLA timers post-migration, effectively lengthening response time for the most urgent issues. This is flagged as a go/no-go item for cutover.

### 5. Recommendation

Proceed to build phase with the escalation-rule gap treated as a blocking item for cutover sign-off. All other gaps are manageable within the existing project timeline.

---
*This sample has been generalized from production gap/impact analysis documentation. Figures, field names, and specific platform details have been altered.*
