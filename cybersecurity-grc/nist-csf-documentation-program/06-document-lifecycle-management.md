# Security Documentation Lifecycle Management

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-PRO-001 |
| Document type | Procedure and controlled register |
| Version | 1.0 |
| Document owner | Governance, Risk, and Compliance (GRC) Manager |
| Maintained by | Robin Karim, Technical Writer, GRC |
| Approver | Director of Information Security |
| Effective date | November 1, 2026 |
| Framework alignment | National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0: GV.PO-01, GV.PO-02; NIST Special Publication (SP) 800-53 Rev. 5: PM-1, PL-1, and the first control in each family (for example, AC-1), which covers policy and procedures |

---

## 1. Purpose

This procedure explains how Meridian Enterprise Services ("Meridian") security documents are created, reviewed, approved, published, maintained, and retired. It also holds the document register and the review calendar.

## 2. Lifecycle Stages

```
 Request → Draft → Stakeholder Review → Revise → Leadership Review → Approve → Publish → Maintain → Retire
              ↑                                                                             |
              └────────────────────── scheduled or triggered review ────────────────────────┘
```

| Stage | What Happens | Who | Exit Criteria |
|-------|--------------|-----|---------------|
| 1. Request | A new document or change is requested through the GRC intake form. | Anyone | Request logged with a reason and a proposed owner |
| 2. Draft | The technical writer drafts the document from the approved template, using interviews and source material. | Technical Writer, document owner | Draft follows the template and the style guide |
| 3. Stakeholder review | Subject matter experts and affected teams comment on the draft. Review window: 10 business days. | Reviewers listed in the review plan | All comments logged in the comment tracker |
| 4. Revise | The writer resolves every comment: accepted, changed, or declined with a reason. | Technical Writer | Comment tracker shows zero open items |
| 5. Leadership review | Security leadership reviews the revised draft. Legal and Human Resources (HR) review when the document affects workforce conduct. | Director of Information Security; Legal; HR | Leadership comments resolved |
| 6. Approve | The approver signs off in the document management system. | Approver named in the document header | Approval recorded with date |
| 7. Publish | The document is published to the GRC document library, and affected teams are notified. | Technical Writer | Published; notification sent; old version archived |
| 8. Maintain | The document is reviewed on schedule or when a trigger occurs. | Document owner | Review completed and logged |
| 9. Retire | The document is withdrawn, and links to it are removed or redirected. | Document owner, GRC | Retirement logged in the register |

### 2.1 Review Triggers Outside the Calendar

A document must be reviewed before its scheduled date when any of these occur:

- A Severity 1 (Sev 1) security incident related to the document's topic.
- An audit finding, assessment result, or regulatory change that affects the document.
- A major system, organization, or process change.
- A new revision of CSF or SP 800-53.

## 3. Version Control Rules

| Rule | Detail |
|------|--------|
| Version numbering | **Major.Minor**. A major change (new or removed requirement) raises the first number and needs full approval. A minor change (clarification, formatting, broken link) raises the second number and needs owner approval only. |
| Drafts | Drafts are labeled with a suffix, for example `2.0-draft1`. Draft versions are never published. |
| Single source of truth | Only the version in the GRC document library is official. Printed or downloaded copies are uncontrolled. |
| Archive | Every superseded version is kept for 7 years in the archive folder. |
| Revision history | Every version is recorded in the document's revision history table with date, author, summary, and approver. |

## 4. Comment Resolution Log (Example: ISP-001 v2.0)

This is how stakeholder and leadership feedback is tracked through review.

| # | Reviewer | Section | Comment | Resolution | Status |
|---|----------|---------|---------|------------|--------|
| 1 | Information Technology (IT) Operations | 4.3, ISP-PR-02 | Multifactor authentication (MFA) for "all systems" is not possible for legacy manufacturing systems. | Accepted. Scope narrowed to remote, privileged, and Confidential or Restricted data access. Legacy systems handled through exceptions. | Closed |
| 2 | Legal | 6 | Enforcement language should mention contractors. | Accepted. Added "or contract." | Closed |
| 3 | HR | 4.3, ISP-PR-03 | New-hire training deadline of 7 days conflicts with onboarding schedule. | Changed to 30 days after HR confirmed the onboarding timeline. | Closed |
| 4 | Security Operations | 4.4, ISP-DE-03 | Requests 24-month log retention. | Declined for this version. Legal confirmed 12 months meets current obligations; cost impact sent to the Director for fiscal year 2028 planning. | Closed (declined with reason) |
| 5 | Director of Information Security | 4.1 | Add a requirement for supplier reassessment. | Accepted. Added ISP-GV-05. | Closed |

## 5. Document Register

| Document ID | Title | Type | Version | Owner | Approver | Last Approved | Review Cycle | Next Review | Status |
|-------------|-------|------|---------|-------|----------|---------------|--------------|-------------|--------|
| ISP-001 | Information Security Policy | Policy | 2.0 | Director of Information Security | Chief Information Security Officer (CISO) | 10/24/2026 | 12 months | 11/01/2027 | Current |
| STD-GV-001 | Third-Party Risk Management Standard | Standard | 1.0 | Vendor Risk Lead | Director of Information Security | 10/30/2026 | 12 months | 11/01/2027 | Current |
| STD-ID-001 | Asset Management and Data Classification Standard | Standard | 1.0 | Manager, IT Operations | Director of Information Security | 10/30/2026 | 12 months | 11/01/2027 | Current |
| STD-ID-002 | Risk Assessment Standard | Standard | 1.0 | GRC Manager | Director of Information Security | 10/16/2026 | 12 months | 11/01/2027 | Current |
| STD-AC-001 | Access Control Standard | Standard | 1.0 | Manager, Identity and Access Management | Director of Information Security | 10/21/2026 | 6 months, then 12 | 05/01/2027 | Current |
| STD-PR-002 | Secure Configuration and Vulnerability Management Standard | Standard | 1.0 | Manager, Infrastructure | Director of Information Security | 10/30/2026 | 12 months | 11/01/2027 | Current |
| STD-PR-003 | Data Protection and Encryption Standard | Standard | 1.0 | Privacy Office Lead | Director of Information Security | 10/30/2026 | 12 months | 11/01/2027 | Current — revision planned to add media handling rules (see Traceability Matrix §4.2) |
| STD-PR-004 | Security Awareness and Training Standard | Standard | 1.0 | Security Awareness Lead | Director of Information Security | 10/09/2026 | 12 months | 11/01/2027 | Current |
| STD-DE-001 | Security Monitoring and Logging Standard | Standard | 1.0 | Manager, Security Operations | Director of Information Security | 10/23/2026 | 12 months | 11/01/2027 | Current |
| PRO-IR-001 | Security Incident Response Procedure | Procedure | 1.1 | Manager, Security Operations | Director of Information Security | 10/28/2026 | 12 months, or after a Sev 1 incident | 11/01/2027 | Current |
| PRO-RC-001 | Backup and Recovery Procedure | Procedure | 1.0 | Manager, Infrastructure | Director of Information Security | 10/30/2026 | 12 months | 11/01/2027 | Current |

## 6. Review Calendar (2027)

Reviews are staggered so owners and approvers are not asked to review every document in the same month.

| Month | Activity | Documents |
|-------|----------|-----------|
| January | Quarterly documentation sweep: broken links, team pages setting rules, owner changes | All |
| February | Scheduled review | STD-PR-004 |
| March | Scheduled review | STD-ID-002 |
| April | Quarterly sweep; CSF alignment report to leadership | All |
| May | Six-month review of new standard | STD-AC-001 |
| June | Scheduled review | STD-DE-001, PRO-RC-001 |
| July | Quarterly sweep; template and style guide review | Templates, Style Guide |
| August | Scheduled review | STD-GV-001, STD-ID-001 |
| September | Scheduled review | STD-PR-002, STD-PR-003 |
| October | Quarterly sweep; annual incident response tabletop feeds PRO-IR-001 updates | All; PRO-IR-001 |
| November | Annual review | ISP-001, PRO-IR-001 |
| December | Annual program report; set next year's calendar | Register |

> **Note:** In the first year, review dates in the register show November 1, 2027, as the latest allowed date. The calendar spreads the actual reviews across the year, so most documents will be reviewed earlier than their latest date.

## 7. Overdue Reviews

| Days Past Due | Action |
|---------------|--------|
| 1–30 | Reminder sent to the document owner. |
| 31–60 | Escalation to the owner's manager and the GRC Manager. |
| 61 or more | Reported to the Director of Information Security as a program risk in the monthly status report. |
