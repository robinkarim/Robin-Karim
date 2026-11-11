# Policy Consolidation Map

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-PLN-001 |
| Document type | Consolidation crosswalk (working document) |
| Version | 1.2 |
| Prepared by | Robin Karim, Technical Writer, Governance, Risk, and Compliance (GRC) |
| Reviewed by | Director of Information Security |
| Date | October 30, 2026 |

---

## 1. Summary

At the start of the engagement, Meridian Enterprise Services ("Meridian") had **23 security documents** spread across SharePoint, Confluence, and shared drives. Ten had no named owner, only two had a formal review in the last 24 months, and six requirements contradicted each other across documents.

This map shows how those 23 documents were consolidated into **11 governed documents** organized around the six National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0 functions.

| Measure | Before | After |
|---------|--------|-------|
| Total security documents | 23 | 11 |
| Documents with a named owner | 13 (57%) | 11 (100%) |
| Documents formally reviewed in the last 24 months | 2 (9%) | 11 (100%) |
| Storage locations | 4 | 1 (GRC document library) |
| Known conflicting requirements | 6 | 0 |
| Team-maintained pages holding mandatory rules | 7 | 0 |

## 2. Target Structure

| CSF Function | Governed Document | Document ID |
|--------------|-------------------|-------------|
| Govern (GV) | Information Security Policy | ISP-001 |
| Govern (GV) | Third-Party Risk Management Standard | STD-GV-001 |
| Identify (ID) | Asset Management and Data Classification Standard | STD-ID-001 |
| Identify (ID) | Risk Assessment Standard | STD-ID-002 |
| Protect (PR) | Access Control Standard | STD-AC-001 |
| Protect (PR) | Secure Configuration and Vulnerability Management Standard | STD-PR-002 |
| Protect (PR) | Data Protection and Encryption Standard | STD-PR-003 |
| Protect (PR) | Security Awareness and Training Standard | STD-PR-004 |
| Detect (DE) | Security Monitoring and Logging Standard | STD-DE-001 |
| Respond (RS) | Security Incident Response Procedure | PRO-IR-001 |
| Recover (RC) | Backup and Recovery Procedure | PRO-RC-001 |

## 3. Legacy-to-Target Crosswalk

**Disposition key:**
- **Merged:** Content moved into the target document; the legacy document was retired.
- **Promoted:** Mandatory rules moved from team-maintained guidance into a governed document; the team page stays as a how-to reference that links to the governed document.
- **Retired:** Content was outdated or duplicated and was not carried forward.

| # | Legacy Document | Location | Last Reviewed | Owner | Target Document | Disposition | Notes |
|---|-----------------|----------|---------------|-------|-----------------|-------------|-------|
| 1 | Information Security Policy v1.3 | SharePoint | 03/2024 | J. Alvarez | ISP-001 | Merged | Restructured by CSF function. |
| 2 | Acceptable Use Policy v2.1 | SharePoint | 06/2023 | Human Resources (HR) | ISP-001 | Merged | Became statement ISP-PR-06. |
| 3 | Security Awareness Policy v1.0 | SharePoint | 01/2022 | None | ISP-001 / STD-PR-004 | Merged | Policy statement in ISP-001; details in standard. |
| 4 | Data Handling Policy v1.4 | SharePoint | 11/2023 | Privacy Office | ISP-001 / STD-PR-003 | Merged | Classification levels moved to STD-ID-001. |
| 5 | Vendor Security Questionnaire Guide | Shared drive | 2021 | None | STD-GV-001 | Merged | Questionnaire kept as an appendix. |
| 6 | Procurement Security Checklist | Confluence (Procurement) | 08/2024 | Procurement | STD-GV-001 | Promoted | Mandatory review triggers moved to the standard. |
| 7 | Asset Inventory Guidelines | Confluence (Operations) | 2022 | Information Technology (IT) Operations | STD-ID-001 | Promoted | Inventory requirements made mandatory. |
| 8 | Data Classification Quick Reference | SharePoint | 05/2024 | Privacy Office | STD-ID-001 | Merged | Four classification levels adopted. |
| 9 | Risk Assessment Methodology v2 | Shared drive | 2020 | None | STD-ID-002 | Merged | Updated scoring scale. |
| 10 | Identity and Access Management (IAM) Team Wiki: "How We Do Access" | Confluence (IAM) | Ongoing | IAM team | STD-AC-001 | Promoted | Resolved termination time-frame conflict. |
| 11 | Help Desk Runbook §4 "Account Requests" | Confluence (Help Desk) | 07/2025 | Help Desk | STD-AC-001 | Promoted | Steps stay in runbook; rules moved to standard. |
| 12 | Privileged Access Guidelines v0.9 | Shared drive | Never approved | None | STD-AC-001 | Merged | Draft content approved through standard review. |
| 13 | Remote Access Policy v1.1 | SharePoint | 2021 | None | STD-AC-001 | Merged | Virtual private network (VPN) rules updated for multifactor authentication (MFA). |
| 14 | Password Policy v3.0 | SharePoint | 2019 | None | STD-AC-001 | Retired | 90-day expiration rule replaced by current NIST guidance. |
| 15 | Server Hardening Checklist | Confluence (Infrastructure) | 2023 | Infrastructure | STD-PR-002 | Promoted | Baselines referenced by version. |
| 16 | Patch Management Procedure v1.2 | SharePoint | 10/2024 | IT Operations | STD-PR-002 | Merged | Patch time frames set by severity. |
| 17 | Encryption Guidelines | Shared drive | 2020 | None | STD-PR-003 | Merged | Approved algorithms updated. |
| 18 | Removable Media Policy | SharePoint | 2018 | None | STD-PR-003 | Retired | Duplicated Data Handling Policy; outdated. |
| 19 | Security Training Calendar | Confluence (Security) | Ongoing | Security Awareness | STD-PR-004 | Promoted | Completion deadlines made mandatory. |
| 20 | Security Operations Center (SOC) Alert Triage Playbook | Confluence (SecOps) | Ongoing | SecOps | STD-DE-001 | Promoted | Triage time frames moved to standard; playbook kept. |
| 21 | Log Retention Memo | Email (2022) | 2022 | None | STD-DE-001 | Merged | 12-month retention confirmed with Legal. |
| 22 | Incident Response Plan v1.0 | SharePoint | 03/2025 | SecOps | PRO-IR-001 | Merged | Renumbered as PRO-IR-001 and rewritten as numbered steps. |
| 23 | Disaster Recovery Notes | Shared drive | 2021 | None | PRO-RC-001 | Merged | Recovery objectives confirmed with system owners. |

## 4. Conflicts Resolved

| # | Topic | Conflicting Sources | Resolution | Decided By | Date |
|---|-------|---------------------|------------|------------|------|
| 1 | Terminated-user access removal | IAM Wiki ("same day") vs. Help Desk Runbook ("3 business days") | Within 4 hours of HR termination time | Chief Information Security Officer (CISO) | 09/12/2026 |
| 2 | Password expiration | Password Policy (90 days) vs. Remote Access Policy (60 days) | No forced expiration; screen against compromised-password lists | CISO | 09/12/2026 |
| 3 | Access review frequency | IAM Wiki (twice a year) vs. Internal Audit request (quarterly) | Quarterly; monthly for privileged accounts | CISO | 09/12/2026 |
| 4 | Log retention | Log Retention Memo (6 months) vs. Incident Response Plan (1 year) | 12 months | Legal and CISO | 09/26/2026 |
| 5 | Data classification levels | Data Handling Policy (3 levels) vs. Quick Reference (4 levels) | 4 levels: Public, Internal, Confidential, Restricted | Privacy Office | 09/26/2026 |
| 6 | Vendor reassessment cycle | Questionnaire Guide (annual) vs. Procurement Checklist (at renewal) | Every 2 years, or at renewal for high-risk vendors | Director of Information Security | 10/03/2026 |

## 5. Rule for Team-Maintained Pages Going Forward

Team wikis and runbooks may keep how-to steps, tips, and screenshots. They may **not** set mandatory requirements. Any page that uses "must," "shall," or a required time frame must link to the governed document that sets that rule. The GRC team checks for this during the quarterly documentation sweep.
