# Access Control Standard

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | STD-AC-001 |
| Document type | Standard |
| Version | 1.0 |
| Status | Approved |
| Parent policy | [ISP-001 Information Security Policy](01-information-security-policy.md), statements ISP-PR-01 and ISP-PR-02 |
| Document owner | Manager, Identity and Access Management (IAM) |
| Approver | Director of Information Security |
| Effective date | November 1, 2026 |
| Next scheduled review | May 1, 2027 (six-month review for new standards, then every 12 months) |
| Supersedes | IAM Team Wiki: "How We Do Access" (Confluence); Help Desk Runbook §4 "Account Requests"; Privileged Access Guidelines v0.9 (draft, never approved); Remote Access Policy v1.1; Password Policy v3.0 |
| Framework alignment | National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0: PR.AA-01, PR.AA-02, PR.AA-03, PR.AA-05; NIST Special Publication (SP) 800-53 Rev. 5: AC-2, AC-5, AC-6, AC-17, IA-2, IA-5 |

---

## 1. Purpose

This standard sets the minimum requirements for requesting, approving, granting, reviewing, and removing access to Meridian Enterprise Services ("Meridian") systems and data.

### 1.1 Why This Standard Was Created

Before this standard, access rules lived in three places: an IAM team wiki page, a section of the Help Desk runbook, and a privileged access draft that was never approved. The rules did not always agree. For example, the wiki said terminated users lost access "same day," while the Help Desk runbook said "within 3 business days." Auditors could not tell which rule Meridian actually followed.

This standard moves those operational requirements into one governed, version-controlled document with a named owner. The team wiki now links here and holds only how-to tips.

## 2. Scope

This standard applies to every account on Meridian systems, including employee, contractor, service, shared, and privileged accounts, in on-premises and cloud environments.

## 3. Requirements

### 3.1 Account Provisioning

| ID | Requirement | Source of Requirement |
|----|-------------|-----------------------|
| AC-STD-01 | Every access request **must** be submitted through the Information Technology Service Management (ITSM) portal. Email and chat requests **must not** be accepted. | Help Desk Runbook §4.1 |
| AC-STD-02 | Every access request **must** be approved by the user's manager and the system owner before access is granted. | IAM Wiki; confirmed in IAM interview, 09/03/2026 |
| AC-STD-03 | Each user **must** have a unique account. Shared accounts are prohibited unless the Chief Information Security Officer (CISO) approves an exception. | New requirement (gap closure, AC-2) |
| AC-STD-04 | Access **must** be granted through role-based groups. Direct permission grants to individual accounts **must** be documented with a reason. | IAM Wiki |

### 3.2 Authentication

| ID | Requirement | Source of Requirement |
|----|-------------|-----------------------|
| AC-STD-05 | Multifactor authentication (MFA) **must** be enforced for remote access, all privileged accounts, and every system that stores Confidential or Restricted data. | ISP-PR-02 |
| AC-STD-06 | Passwords **must** be at least 14 characters long. Passwords **must not** be required to expire on a schedule unless there is evidence of compromise. | Updated to align with NIST SP 800-63B |
| AC-STD-07 | Passwords **must** be checked against a list of known compromised passwords when they are created or changed. | New requirement (gap closure, IA-5) |
| AC-STD-08 | Accounts **must** lock after 10 failed login attempts within 15 minutes. | Help Desk Runbook §4.3 |

### 3.3 Privileged Access

| ID | Requirement | Source of Requirement |
|----|-------------|-----------------------|
| AC-STD-09 | Administrators **must** use a separate privileged account for administrative tasks. Privileged accounts **must not** be used for email or web browsing. | Privileged Access Guidelines v0.9 |
| AC-STD-10 | Privileged credentials **must** be stored in and checked out from the approved privileged access management (PAM) vault. | Privileged Access Guidelines v0.9 |
| AC-STD-11 | A person **must not** approve their own request for privileged access. | New requirement (gap closure, AC-5) |

### 3.4 Access Reviews

| ID | Requirement | Source of Requirement |
|----|-------------|-----------------------|
| AC-STD-12 | System owners **must** review user access to their systems every quarter and confirm or remove each account. | IAM Wiki (previously "twice a year"; changed to quarterly per CISO direction) |
| AC-STD-13 | Privileged access **must** be reviewed every month. | New requirement (gap closure, AC-6) |
| AC-STD-14 | Review results **must** be recorded in the ITSM portal and kept for three years as audit evidence. | Internal Audit finding IA-2025-07 |

### 3.5 Changes and Removal

| ID | Requirement | Source of Requirement |
|----|-------------|-----------------------|
| AC-STD-15 | Access for terminated users **must** be disabled within 4 hours of the termination time recorded by Human Resources (HR). For involuntary terminations, access **must** be disabled before or at the time the user is notified. | Resolved conflict between IAM Wiki and Help Desk Runbook; approved by CISO 09/12/2026 |
| AC-STD-16 | When a user changes roles, access that is no longer needed **must** be removed within 5 business days. | IAM Wiki |
| AC-STD-17 | Accounts with no login activity for 90 days **must** be disabled automatically. | New requirement (gap closure, AC-2(3)) |

## 4. Compliance Measurement

| Metric | Target | Data Source |
|--------|--------|-------------|
| Terminated-user accounts disabled within 4 hours | 100% | HR termination feed compared with directory logs |
| Quarterly access reviews completed on time | 95% or higher | ITSM review tickets |
| Privileged accounts enrolled in MFA | 100% | Identity provider report |

## 5. Exceptions

Exceptions follow Section 5 of [ISP-001](01-information-security-policy.md).

## 6. Revision History

| Version | Date | Author | Summary of Changes | Approved By |
|---------|------|--------|--------------------|-------------|
| 0.1 | 09/05/2026 | R. Karim | First draft built from IAM Wiki, Help Desk Runbook §4, and Privileged Access Guidelines v0.9. | — |
| 0.2 | 09/16/2026 | R. Karim | Resolved termination time-frame conflict (4 hours); added five gap-closure requirements; changed password rules to align with NIST SP 800-63B. | — |
| 0.3 | 10/07/2026 | R. Karim | IAM and Help Desk review: clarified role-change time frame; added the "Source of Requirement" column at the request of Internal Audit. | — |
| 1.0 | 10/21/2026 | R. Karim | Approved for publication. | Director of Information Security |
