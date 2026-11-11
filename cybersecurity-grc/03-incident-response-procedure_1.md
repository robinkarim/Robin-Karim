# Security Incident Response Procedure

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | PRO-IR-001 |
| Document type | Procedure |
| Version | 1.1 |
| Status | Approved |
| Parent documents | [ISP-001 Information Security Policy](01-information-security-policy.md), statements ISP-RS-01 through ISP-RS-03 and ISP-RC-01 through ISP-RC-03 |
| Document owner | Manager, Security Operations |
| Approver | Director of Information Security |
| Effective date | November 1, 2026 |
| Next scheduled review | November 1, 2027, or within 30 days after any Severity 1 (Sev 1) incident |
| Framework alignment | National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0: DE.AE, RS.MA, RS.AN, RS.CO, RS.MI, RC.RP, RC.CO; NIST Special Publication (SP) 800-53 Rev. 5: IR-4, IR-5, IR-6, IR-8, CP-10; NIST SP 800-61 Rev. 3 |

---

## 1. Purpose

This procedure tells the Security Operations team and supporting teams exactly what to do, and in what order, from the time a possible security incident is reported until the affected systems are restored and lessons learned are recorded.

## 2. Scope

This procedure covers all suspected and confirmed security incidents that affect Meridian Enterprise Services ("Meridian") systems, data, or workforce members. Physical safety events and routine information technology (IT) outages without a security cause follow the Business Continuity Plan instead.

## 3. Roles

| Role | Who Fills It | Responsibilities |
|------|--------------|------------------|
| Incident Commander (IC) | On-call Security Operations lead | Directs the response, makes containment decisions, and owns the incident record. |
| Security Analyst | Security Operations analyst on shift | Triages alerts, gathers evidence, and carries out containment steps. |
| Communications Lead | Corporate Communications delegate | Prepares internal and external messages approved by the IC and Legal. |
| Legal Counsel | Assigned attorney | Decides whether regulatory, customer, or law enforcement notification is required. |
| System Owner | Owner of the affected system | Approves service-affecting actions and leads recovery. |

## 4. Severity Levels

| Severity | Description | Examples | Initial Response Time | Leadership Notification |
|----------|-------------|----------|-----------------------|-------------------------|
| Sev 1 — Critical | Confirmed compromise of Restricted data or a critical system; business operations stopped | Ransomware on production servers; confirmed data exfiltration | 15 minutes | Chief Information Security Officer (CISO) within 30 minutes |
| Sev 2 — High | Likely compromise with limited spread | Compromised privileged account; malware on several endpoints | 1 hour | Director of Information Security within 2 hours |
| Sev 3 — Medium | Contained event with no confirmed data exposure | Phishing email clicked, credentials reset right away | 4 hours | Weekly summary |
| Sev 4 — Low | Policy violation or blocked attack attempt | Unauthorized software installed; blocked malware | 1 business day | Monthly metrics |

## 5. Procedure

### 5.1 Phase 1: Detect and Report

1. Receive the report from one of these sources:
   - An alert from the security monitoring platform.
   - A call or ticket to the Security Operations hotline.
   - A message to the security reporting mailbox.
2. Open an incident record in the IT Service Management (ITSM) tool using the **Security Incident** template.
3. Record the time the report was received. This time starts the response clock.

### 5.2 Phase 2: Analyze and Classify

4. Review the alert or report and collect initial evidence (logs, email headers, endpoint data).
5. Decide whether the event is a security incident.
   - **If no:** Document the reason, close the record as a false positive, and stop here.
   - **If yes:** Continue to step 6.
6. Assign a severity level using the table in Section 4.
7. For Sev 1 or Sev 2, page the Incident Commander and open a dedicated incident bridge.

> **Note:** When you are unsure between two severity levels, choose the higher one. You can lower the severity later; you cannot get back lost response time.

### 5.3 Phase 3: Contain

8. Carry out short-term containment based on the incident type:

   | Incident Type | Containment Action |
   |---------------|--------------------|
   | Compromised account | Disable the account and revoke active sessions and tokens. |
   | Infected endpoint | Isolate the device from the network using the endpoint detection and response (EDR) console. |
   | Malicious email | Remove the message from all mailboxes and block the sender. |
   | Compromised server | Get System Owner approval, then isolate the server or block its network traffic. |

9. Preserve evidence **before** you wipe or rebuild anything. Take a memory capture and disk image when the IC requests it, and record the chain of custody.

> **Warning:** Do not power off a compromised server unless the IC tells you to. Powering it off erases memory evidence.

### 5.4 Phase 4: Eradicate

10. Identify the root cause and every affected system.
11. Remove the threat: delete malware, close the exploited vulnerability, and reset affected credentials.
12. Confirm that no signs of the threat remain by running a fresh scan.

### 5.5 Phase 5: Recover

13. Restore systems from known-good backups or rebuild them to the approved secure baseline.
14. Get System Owner approval before returning a system to production.
15. Monitor restored systems closely for 14 days for signs that the threat has returned.
16. Send recovery status updates to leadership and affected stakeholders at the interval the IC sets (at least every 4 hours for Sev 1).

### 5.6 Phase 6: Notify

17. For any incident that may involve personal, customer, or regulated data, notify Legal Counsel within 1 hour of confirmation.
18. Legal Counsel decides whether external notification is required and approves all external messages.
19. The Communications Lead sends approved messages and records the time each was sent.

### 5.7 Phase 7: Close and Learn

20. Hold a lessons-learned review within 10 business days after a Sev 1 or Sev 2 incident is closed.
21. Record the root cause, timeline, what worked, what did not, and corrective actions with owners and due dates.
22. Send documentation updates to the Governance, Risk, and Compliance (GRC) team so affected policies, standards, and procedures can be revised.
23. Close the incident record.

## 6. Records

| Record | Location | Retention |
|--------|----------|-----------|
| Incident record | ITSM tool | 7 years |
| Evidence and chain-of-custody forms | Secure evidence storage | 7 years, or longer if under legal hold |
| Lessons-learned report | GRC document library | 7 years |

## 7. Revision History

| Version | Date | Author | Summary of Changes | Approved By |
|---------|------|--------|--------------------|-------------|
| 1.0 | 03/02/2025 | Security Operations | First release. | Director of Information Security |
| 1.1-draft | 09/30/2026 | R. Karim | Rewrote as numbered steps; added severity table and containment matrix; aligned with NIST SP 800-61 Rev. 3 and CSF 2.0; added Phase 7 feedback loop to the GRC team. | — |
| 1.1 | 10/28/2026 | R. Karim | Added Legal's 1-hour notification step after tabletop exercise feedback; approved. | Director of Information Security |
