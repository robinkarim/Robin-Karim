# Operations Runbook
## Cloud Infrastructure: Nightly Batch Job Failure — Enrollment Sync

**Audience:** Operations team (on-call rotation)
**Severity Guidance:** This runbook covers a Priority 2 event (delayed data, not a full outage). For full platform outage, see the separate Platform Outage Runbook.

---

### 1. Trigger

Automated alert fires when the nightly enrollment sync job (Kubernetes CronJob `enrollment-sync-nightly`) fails or does not complete within its expected 45-minute window.

### 2. Initial Triage (First 10 Minutes)

1. Check the job's pod logs in the cluster dashboard for the most recent failed run.
2. Identify the failure category from the log output:
   - **Connection timeout** to the source database → go to Section 3.
   - **Data validation error** (malformed record) → go to Section 4.
   - **Resource limit exceeded** (pod OOMKilled) → go to Section 5.

### 3. Connection Timeout

1. Confirm the source database is reachable from the cluster using the standard connectivity check script.
2. If the database is reachable but the job still timed out, check for an active long-running query on the source database that may be blocking the sync's read.
3. Manually re-trigger the job once connectivity is confirmed stable. Do not re-trigger repeatedly without confirming the underlying cause — repeated triggers against an unstable connection can compound the delay.

### 4. Data Validation Error

1. Locate the specific record(s) causing the validation failure from the job's error output.
2. Determine whether the record is a genuine data-quality issue (escalate to the data owner) or a new, valid data pattern the validation rule doesn't yet account for (escalate to the platform engineering team for a rule update — do not bypass validation to force the job through).
3. Once the underlying record or rule issue is resolved, manually re-trigger the job.

### 5. Resource Limit Exceeded

1. Check whether this run's data volume is unusually high (e.g., a bulk enrollment event) compared to the typical nightly volume.
2. If volume is the cause, manually re-trigger with the temporary elevated resource profile (documented in the cluster resource-profile reference) rather than permanently raising the default limit for a one-time event.
3. If volume is normal and the job still exceeded its resource limit, escalate to platform engineering — this indicates a regression, not a one-time event.

### 6. Downstream Notification

If the sync will be delayed beyond 2 hours from its normal completion time, notify the downstream consumer teams (reporting, transportation) proactively rather than waiting for them to notice stale data.

### 7. Post-Resolution

Log the failure category, root cause, and resolution in the on-call handoff notes so recurring patterns are visible to the next on-call engineer.

---
*This runbook has been generalized from production operations documentation. Job names, timing thresholds, and specific tooling references have been altered.*
