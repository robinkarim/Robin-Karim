# Business Requirements Document
## ITSM Ticketing Platform Migration — Requirements for Incident and Request Management

**Document status:** Final — approved for release
**Prepared by:** Business Systems Analyst
**Distribution:** Project Sponsor, Engineering Lead, QA Lead, Change Advisory Board

---

### 1. Purpose

This document defines the business requirements for migrating incident and service request management from a legacy, on-premise ticketing tool to a cloud-based ITSM platform. It reflects requirements gathered through stakeholder interviews, current-state process walkthroughs, and review of existing ticket volume and escalation data. It is intended to give both business sponsors and the engineering team a single point of sign-off before development begins.

### 2. Background

The current ticketing tool no longer receives vendor support and cannot integrate with the organization's identity provider, forcing manual account provisioning for every new agent. Average time-to-resolution has climbed over the past two years as ticket volume has grown faster than the tool's reporting capability can track. Leadership has approved migration to a supported ITSM platform as part of the broader infrastructure modernization program.

### 3. Stakeholders

| Role | Interest |
|---|---|
| Service Desk Manager | Agent workflow continuity, minimal retraining burden |
| IT Security | SSO integration, access logging, audit trail |
| Reporting/Analytics Team | Historical data migration, dashboard parity |
| End Users (all departments) | Uninterrupted ability to submit and track requests |

### 4. Business Requirements

**BR-01 — Ticket Submission**
Users must be able to submit incidents and service requests through a self-service portal, with category selection driving routing to the correct queue.

**BR-02 — Identity Integration**
The platform must authenticate against the existing identity provider via SSO, eliminating manual account creation for new agents and users.

**BR-03 — SLA Tracking**
The platform must track and report against existing SLA tiers (Priority 1 through 4) with automated escalation notifications at defined thresholds.

**BR-04 — Historical Data Migration**
A minimum of 24 months of closed-ticket history must be migrated and remain searchable, preserving original timestamps and resolution notes.

**BR-05 — Reporting Parity**
Reporting must reproduce the current monthly volume-by-category and average-resolution-time dashboards without manual reconciliation.

### 5. Out of Scope

- Migration of the change management module (planned for Phase 2)
- Retirement of the legacy tool's read-only archive instance

### 6. Traceability

Each requirement above traces back to a stakeholder interview or ticket-data finding logged in the discovery workbook (Appendix A, maintained separately). Requirements BR-02 and BR-03 were escalated directly from IT Security and the Service Desk Manager, respectively, during Discovery Week 2.

### 7. Sign-Off

| Name | Role | Date |
|---|---|---|
| | Project Sponsor | |
| | Engineering Lead | |
| | QA Lead | |

---
*Client and system names have been generalized. This sample reflects the structure and level of detail used in production BRDs; specific figures and terminology have been altered.*
