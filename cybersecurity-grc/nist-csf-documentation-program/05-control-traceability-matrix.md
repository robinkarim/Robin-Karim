# Control Traceability Matrix

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-TRC-001 |
| Document type | Traceability matrix (controlled record) |
| Version | 1.0 |
| Prepared by | Robin Karim, Technical Writer, Governance, Risk, and Compliance (GRC) |
| Data as of | October 31, 2026 |
| Frameworks | National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0; NIST Special Publication (SP) 800-53 Rev. 5 |
| Sortable version | [traceability-matrix.csv](traceability-matrix.csv) |

---

## 1. How to Read This Matrix

Each row traces one documented requirement to the CSF 2.0 subcategory it supports and the SP 800-53 control it helps implement. The matrix answers three questions:

1. **Where is each requirement written down?** (Requirement ID and Source Document)
2. **What framework outcome does it support?** (CSF Subcategory and SP 800-53 Control)
3. **Where are the gaps?** (Section 4 lists CSF categories and SP 800-53 families with weak or no coverage.)

**Coverage status key:**
- **Full:** The requirement fully addresses the subcategory outcome, and evidence is produced.
- **Partial:** The requirement addresses part of the outcome, or evidence is not yet produced.
- **Gap:** No documented requirement exists.

## 2. Requirement-to-Control Trace

| Requirement ID | Requirement (Summary) | Source Document | CSF Function | CSF Subcategory | SP 800-53 Control | Coverage | Evidence |
|----------------|-----------------------|-----------------|--------------|-----------------|-------------------|----------|----------|
| ISP-GV-01 | Documented security program, approved and reviewed yearly | ISP-001 | Govern | GV.PO-01, GV.PO-02 | PM-1, PL-1 | Full | Signed approval; review calendar |
| ISP-GV-02 | Security roles assigned to named individuals | ISP-001 | Govern | GV.RR-02 | PM-2, PS-9 | Full | Roles table; organization chart |
| ISP-GV-03 | Cybersecurity risk appetite set | ISP-001 | Govern | GV.RM-02 | PM-9 | Partial | Risk appetite statement in draft |
| ISP-GV-04 | Every document has owner, version, and review date | ISP-001 | Govern | GV.PO-02 | PM-1, PL-1 | Full | Document register |
| ISP-GV-05 | Supplier security assessment before onboarding | ISP-001 | Govern | GV.SC-06, GV.SC-07 | SR-6, SA-9 | Full | Vendor assessment records |
| ISP-ID-01 | Inventory of hardware, software, data, and cloud services | ISP-001 | Identify | ID.AM-01, ID.AM-02, ID.AM-07 | CM-8, PM-5 | Partial | Cloud services not in inventory |
| ISP-ID-02 | Four-level data classification | ISP-001 | Identify | ID.AM-05 | RA-2 | Full | Classification standard |
| ISP-ID-03 | Risk assessments for new and existing systems | ISP-001 | Identify | ID.RA-04, ID.RA-05 | RA-3 | Full | Risk assessment reports |
| ISP-ID-04 | Lessons learned used to improve program | ISP-001 | Identify | ID.IM-01, ID.IM-03 | CA-5, PM-4 | Partial | No tracking of corrective actions |
| ISP-PR-01 | Least-privilege access | ISP-001 | Protect | PR.AA-05 | AC-6 | Full | See STD-AC-001 |
| ISP-PR-02 | Multifactor authentication (MFA) for remote access, privileged access, and Confidential or Restricted data | ISP-001 | Protect | PR.AA-03 | IA-2(1), IA-2(2) | Full | Identity provider report |
| ISP-PR-03 | Security awareness training at hire and yearly | ISP-001 | Protect | PR.AT-01 | AT-2 | Full | Learning Management System (LMS) completion report |
| ISP-PR-04 | Encryption in transit and at rest | ISP-001 | Protect | PR.DS-01, PR.DS-02 | SC-8, SC-28 | Full | Configuration scans |
| ISP-PR-05 | Secure baselines and timely patching | ISP-001 | Protect | PR.PS-01, PR.PS-02 | CM-2, CM-6, SI-2 | Full | Vulnerability scan reports |
| ISP-PR-06 | Acceptable use of systems | ISP-001 | Protect | PR.AT-01 | PL-4 | Full | Signed acknowledgments |
| ISP-DE-01 | Security event logging to central platform | ISP-001 | Detect | PR.PS-04, DE.CM-09 | AU-2, AU-6, AU-12 | Partial | Two critical systems not yet onboarded |
| ISP-DE-02 | Alert triage within set time frames | ISP-001 | Detect | DE.AE-02 | SI-4, IR-4 | Full | Security Operations metrics |
| ISP-DE-03 | 12-month log retention | ISP-001 | Detect | PR.PS-04 | AU-11 | Full | Storage configuration |
| ISP-RS-01 | Incident response plan maintained and tested | ISP-001 | Respond | ID.IM-04, RS.MA-01 | IR-8, IR-3 | Full | Tabletop exercise report |
| ISP-RS-02 | Workforce reports suspected incidents | ISP-001 | Respond | RS.MA-02 | IR-6 | Full | Hotline and mailbox records |
| ISP-RS-03 | Severity classification and required notifications | ISP-001 | Respond | RS.MA-03, RS.CO-02 | IR-6, IR-4 | Full | Incident records |
| ISP-RC-01 | Recovery plans with recovery time and recovery point objectives | ISP-001 | Recover | RC.RP-01 | CP-2, CP-10 | Partial | Objectives set for 9 of 14 critical systems |
| ISP-RC-02 | Quarterly backup testing | ISP-001 | Recover | PR.DS-11, RC.RP-03 | CP-4, CP-9 | Full | Restore test logs |
| ISP-RC-03 | Recovery status communicated | ISP-001 | Recover | RC.CO-03 | CP-2, IR-4 | Full | Status updates in incident record |
| AC-STD-02 | Manager and system owner approval for access | STD-AC-001 | Protect | PR.AA-05 | AC-2 | Full | Information Technology Service Management (ITSM) approvals |
| AC-STD-03 | Unique accounts; no shared accounts | STD-AC-001 | Protect | PR.AA-01 | AC-2, IA-2 | Full | Directory report |
| AC-STD-06 | 14-character passwords, no forced expiration | STD-AC-001 | Protect | PR.AA-01 | IA-5(1) | Full | Directory policy settings |
| AC-STD-11 | No self-approval of privileged access | STD-AC-001 | Protect | PR.AA-05 | AC-5 | Partial | Workflow change in progress |
| AC-STD-12 | Quarterly user access reviews | STD-AC-001 | Protect | PR.AA-05 | AC-2(j) | Full | Review tickets |
| AC-STD-15 | Terminated-user access disabled within 4 hours | STD-AC-001 | Protect | PR.AA-05 | AC-2, PS-4 | Full | Human Resources (HR) feed and directory logs |
| AC-STD-17 | Inactive accounts disabled at 90 days | STD-AC-001 | Protect | PR.AA-05 | AC-2(3) | Partial | Automation scheduled for Q1 2027 |
| PRO-IR-001 §5.3 | Containment actions by incident type | PRO-IR-001 | Respond | RS.MI-01 | IR-4 | Full | Incident records |
| PRO-IR-001 §5.3 | Evidence preservation and chain of custody | PRO-IR-001 | Respond | RS.AN-07 | IR-4, AU-9 | Full | Chain-of-custody forms |
| PRO-IR-001 §5.7 | Lessons-learned review after Sev 1 and Sev 2 incidents | PRO-IR-001 | Respond | ID.IM-04 | IR-4 | Full | Lessons-learned reports |

## 3. Coverage Summary by CSF Function

| CSF Function | Categories in CSF 2.0 | Categories With Full Coverage | Partial | Gap | Coverage |
|--------------|----------------------|-------------------------------|---------|-----|----------|
| Govern (GV) | 6 | 3 (GV.RR, GV.PO, GV.SC) | 1 (GV.RM) | 2 (GV.OC, GV.OV) | 58% |
| Identify (ID) | 3 | 1 (ID.RA) | 2 (ID.AM, ID.IM) | 0 | 67% |
| Protect (PR) | 5 | 4 (PR.AA, PR.AT, PR.DS, PR.PS) | 0 | 1 (PR.IR) | 80% |
| Detect (DE) | 2 | 0 | 2 (DE.CM, DE.AE) | 0 | 50% |
| Respond (RS) | 4 | 3 (RS.MA, RS.AN, RS.MI) | 1 (RS.CO) | 0 | 88% |
| Recover (RC) | 2 | 1 (RC.CO) | 1 (RC.RP) | 0 | 75% |
| **Total** | **22** | **12** | **7** | **3** | **70%** |

*Coverage score: Full = 1 point, Partial = 0.5 point, Gap = 0 points, divided by the number of categories.*

*Category ratings look at every subcategory in the category. A category can be Partial even when the requirements mapped to it in Section 2 are rated Full, because other subcategories in that category are not yet covered (for example, DE.AE and RS.CO).*

## 4. Gaps and Recommended Actions

### 4.1 CSF Categories With Gaps or Partial Coverage

| Gap ID | CSF Category | Current Coverage | What Is Missing | Recommended Action | Proposed Owner | Priority |
|--------|--------------|------------------|-----------------|--------------------|----------------|----------|
| GAP-01 | GV.OV: Oversight | Gap | No requirement for leadership to review security program results and adjust strategy | Add a policy statement requiring a twice-yearly program review by the risk committee | Director of Information Security | High |
| GAP-02 | GV.OC: Organizational Context | Gap | Legal, regulatory, and contract requirements are not documented in one place | Create a compliance obligations register and reference it in ISP-001 | GRC Manager | Medium |
| GAP-03 | PR.IR: Technology Infrastructure Resilience | Gap | No requirement for network segmentation or capacity planning | Draft a Network Security Standard | Manager, Network Engineering | High |
| GAP-04 | DE.CM: Continuous Monitoring | Partial | Two critical systems are not sending logs to the central platform | Add both systems to the logging onboarding plan | Manager, Security Operations | High |
| GAP-05 | RS.CO: Incident Reporting and Communication | Partial | No templates for regulator and customer notifications | Add notification templates as an appendix to PRO-IR-001 | Legal Counsel | Medium |

### 4.2 SP 800-53 Control Families With No Documented Requirements

| Family | Name | Observation | Recommended Action |
|--------|------|-------------|--------------------|
| PE | Physical and Environmental Protection | Facilities team follows an undocumented badge process | Interview Facilities; draft a Physical Security Standard |
| MP | Media Protection | Removable Media Policy was retired as outdated, with nothing replacing it | Add media handling rules to STD-PR-003 |
| PT | Personally Identifiable Information Processing and Transparency | Privacy Office owns privacy notices outside the security portfolio | Confirm ownership boundary with the Privacy Office and cross-reference |
| MA | Maintenance | Vendor remote maintenance is handled case by case | Add remote maintenance rules to STD-AC-001 at next review |

## 5. Maintenance

The GRC team updates this matrix when:

- A governed document is published, revised, or retired.
- A gap is closed or a new gap is found during an audit or assessment.
- NIST publishes a revision to CSF or SP 800-53.

Coverage scores from this matrix feed the quarterly [CSF Alignment Tracker](09-csf-alignment-tracker.md).
