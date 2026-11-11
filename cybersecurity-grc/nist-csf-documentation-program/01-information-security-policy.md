# Information Security Policy

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | ISP-001 |
| Document type | Policy |
| Version | 2.0 |
| Status | Approved |
| Document owner | Director of Information Security |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | November 1, 2026 |
| Next scheduled review | November 1, 2027 |
| Supersedes | ISP-001 v1.3; Acceptable Use Policy v2.1; Security Awareness Policy v1.0; Data Handling Policy v1.4 |
| Framework alignment | National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0: all functions; NIST Special Publication (SP) 800-53 Rev. 5: PM, PL, RA, AT, AC, IA, SC, SI, AU, IR, CP |

---

## 1. Purpose

This policy sets the requirements Meridian Enterprise Services ("Meridian") follows to protect the confidentiality, integrity, and availability of its information and information systems. It establishes leadership's direction for the security program and serves as the parent document for every security standard and procedure.

The policy is organized around the six CSF 2.0 functions: Govern, Identify, Protect, Detect, Respond, and Recover.

## 2. Scope

This policy applies to:

- All Meridian employees, contractors, consultants, and temporary staff.
- All third parties who access Meridian information or systems.
- All information systems that Meridian owns, leases, or operates, whether on premises or in the cloud.
- All information Meridian creates, receives, stores, or transmits, in any format.

## 3. Roles and Responsibilities

| Role | Responsibility |
|------|----------------|
| CISO | Owns the security program, approves this policy, and accepts or escalates residual risk. |
| Director of Information Security | Owns this document, sponsors standards and procedures, and reports program status to leadership. |
| Governance, Risk, and Compliance (GRC) team | Maintains the documentation portfolio, review calendar, and framework traceability. |
| System owners | Ensure their systems meet the applicable standards and fund remediation. |
| Document owners | Keep assigned standards and procedures accurate and complete scheduled reviews on time. |
| People managers | Make sure their staff complete required training and follow this policy. |
| All workforce members | Follow this policy and report suspected security events right away. |

## 4. Policy Statements

Each statement has a unique requirement ID so it can be traced to standards, procedures, and framework controls. See the [Control Traceability Matrix](05-control-traceability-matrix.md).

### 4.1 Govern (GV)

| ID | Requirement |
|----|-------------|
| ISP-GV-01 | Meridian **shall** maintain a documented security program that is approved by the CISO and reviewed at least once a year. |
| ISP-GV-02 | Security roles, responsibilities, and authorities **shall** be documented and assigned to named individuals. |
| ISP-GV-03 | Meridian **shall** set a cybersecurity risk appetite and use it to guide risk decisions. |
| ISP-GV-04 | Every security policy, standard, and procedure **shall** have a named owner, a version number, and a scheduled review date. |
| ISP-GV-05 | Suppliers that access Meridian data or systems **shall** be assessed for security risk before onboarding and at least once every two years. |

### 4.2 Identify (ID)

| ID | Requirement |
|----|-------------|
| ISP-ID-01 | Meridian **shall** maintain a current inventory of hardware, software, data, and cloud services. |
| ISP-ID-02 | Information **shall** be classified as Public, Internal, Confidential, or Restricted. |
| ISP-ID-03 | Risk assessments **shall** be completed for new systems before production use and for existing systems at least once a year. |
| ISP-ID-04 | Lessons learned from incidents, audits, and assessments **shall** be used to improve the program. |

### 4.3 Protect (PR)

| ID | Requirement |
|----|-------------|
| ISP-PR-01 | Access to systems and data **shall** be granted based on least privilege and approved business need. See [STD-AC-001](02-access-control-standard.md). |
| ISP-PR-02 | Multifactor authentication (MFA) **shall** be required for remote access, privileged access, and access to Confidential or Restricted data. |
| ISP-PR-03 | All workforce members **shall** complete security awareness training within 30 days of hire and once a year after that. |
| ISP-PR-04 | Confidential and Restricted data **shall** be encrypted in transit and at rest. |
| ISP-PR-05 | Systems **shall** be configured to approved secure baselines, and security patches **shall** be applied within the time frames set in the Secure Configuration and Vulnerability Management Standard (STD-PR-002). |
| ISP-PR-06 | Workforce members **shall** use Meridian systems only for authorized business purposes. |

### 4.4 Detect (DE)

| ID | Requirement |
|----|-------------|
| ISP-DE-01 | Security-relevant events from critical systems **shall** be logged and sent to the central security monitoring platform. |
| ISP-DE-02 | The Security Operations team **shall** monitor alerts and triage them within the time frames set in the Security Monitoring and Logging Standard (STD-DE-001). |
| ISP-DE-03 | Log data **shall** be kept for at least 12 months. |

### 4.5 Respond (RS)

| ID | Requirement |
|----|-------------|
| ISP-RS-01 | Meridian **shall** maintain and test an incident response plan at least once a year. See [PRO-IR-001](03-incident-response-procedure.md). |
| ISP-RS-02 | Workforce members **shall** report suspected security incidents to the Security Operations team right away. |
| ISP-RS-03 | Incidents **shall** be classified by severity, and notifications **shall** follow legal, regulatory, and contract requirements. |

### 4.6 Recover (RC)

| ID | Requirement |
|----|-------------|
| ISP-RC-01 | Critical systems **shall** have documented recovery plans with defined recovery time and recovery point objectives. |
| ISP-RC-02 | Backups of critical data **shall** be tested at least once every quarter. |
| ISP-RC-03 | Recovery status **shall** be communicated to leadership and affected stakeholders during and after an incident. |

## 5. Exceptions

Exceptions to this policy must be requested through the Security Exception Request form. Each request must include the business reason, compensating controls, and an end date. Exceptions are approved by the CISO for no longer than 12 months and are logged in the risk register.

## 6. Enforcement

Violations of this policy may lead to loss of system access and disciplinary action, up to and including termination of employment or contract. Violations that involve illegal activity may be referred to law enforcement.

## 7. Related Documents

- [STD-AC-001 Access Control Standard](02-access-control-standard.md)
- [PRO-IR-001 Security Incident Response Procedure](03-incident-response-procedure.md)
- STD-PR-002 Secure Configuration and Vulnerability Management Standard
- STD-DE-001 Security Monitoring and Logging Standard
- [Security Documentation Style Guide](07-security-documentation-style-guide.md)

## 8. Definitions

| Term | Definition |
|------|------------|
| Policy | A leadership-approved statement of what the organization requires and why. |
| Standard | A mandatory, measurable rule that supports a policy. |
| Procedure | Step-by-step instructions for carrying out a standard. |
| Least privilege | Giving users only the access they need to do their jobs, and nothing more. |

## 9. Revision History

| Version | Date | Author | Summary of Changes | Approved By |
|---------|------|--------|--------------------|-------------|
| 1.3 | 03/15/2024 | J. Alvarez | Annual review; no material changes. | CISO |
| 2.0-draft1 | 08/22/2026 | R. Karim | Restructured around CSF 2.0 functions; merged four legacy policies; added requirement IDs. | — |
| 2.0-draft2 | 09/19/2026 | R. Karim | Incorporated Legal, Human Resources (HR), and Information Technology (IT) Operations comments; changed MFA scope per IT Operations feedback. | — |
| 2.0 | 10/24/2026 | R. Karim | Final edits from the Security Leadership review; approved for publication. | CISO |
