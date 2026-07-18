# High-Order Technical Specification (HOTS)
## ServiceNow Incident-to-Change Automated Linkage

**Maintained by:** ServiceNow Platform Team
**Review Cycle:** Reviewed at each release cycle

---

### 1. Objective

Specify the automated linkage between an incident record and any change record created to resolve it, so that incident resolution time and change success rate can be reported against each other without manual reconciliation.

### 2. Current Behavior (Baseline)

Incidents and changes exist as related records only when an agent manually links them. Reporting on "incidents resolved via change" currently requires a manual cross-reference and is not reliable at scale.

### 3. Specified Behavior

**3.1 Automatic Link Creation**
When a change record is created from within an open incident record (using the "Create Change" action), the system automatically populates the change's "Related Incident" field and the incident's "Related Change" field — bidirectionally, without requiring a second manual step.

**3.2 Status Propagation**
When the linked change record moves to "Implemented," the incident record receives an automated comment noting the change was implemented and prompting the agent to verify resolution. This does not automatically close the incident — agent confirmation is still required.

**3.3 Reporting Field**
A new reporting field, "Resolved via Change" (boolean), is set to true automatically whenever an incident is closed with a non-empty "Related Change" field, supporting the change-success and incident-resolution reporting requirement without manual tagging.

### 4. Out of Scope

- Automatic linkage for changes created independently of an incident record (these remain manually linkable but not automated)
- Retroactive linkage of historical records prior to this specification's implementation date

### 5. Dependencies

This specification depends on the existing "Create Change" action already being available from the incident form — no new UI action is being introduced, only the automated field population behind it.

### 6. Acceptance Criteria

- Creating a change from an incident populates both related-record fields without manual entry.
- Moving a linked change to "Implemented" generates the automated incident comment within 1 minute.
- The "Resolved via Change" field correctly reflects true/false state on 100% of a 50-record validation sample prior to release.

### 7. Review Notes

This specification is reviewed at each release cycle rather than filed once, since platform updates have previously changed default field behavior on the incident and change tables without an explicit announcement — catching that kind of drift early is the main reason this document is kept current rather than archived after initial build.

---
*This specification has been generalized from production HOTS documentation. Field names and specific automation logic have been altered.*
