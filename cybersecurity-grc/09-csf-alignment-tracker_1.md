# Cybersecurity Framework (CSF) Alignment Tracker: Quarterly Documentation Compliance Report

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-RPT-2026-Q4 |
| Document type | Compliance monitoring report |
| Reporting period | Q4 2026 (through October 31, 2026) |
| Prepared by | Robin Karim, Technical Writer, Governance, Risk, and Compliance (GRC) |
| Audience | Chief Information Security Officer (CISO); Director of Information Security; document owners |
| Data source | [Control Traceability Matrix](05-control-traceability-matrix.md), [Document Register](06-document-lifecycle-management.md#5-document-register) |

---

## 1. Summary

Documentation coverage of the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0 rose from **41% to 70%** since the engagement began in Q3 2026. The remediation phase is complete: all 11 governed documents are approved, owned, and on the review calendar.

The work now shifts to maintenance and closing the remaining gaps. Three items need leadership decisions this quarter (Section 5).

## 2. Coverage Trend by CSF Function

| CSF Function | Baseline (Q3 2026) | Q4 2026 | Change | Q2 2027 Target |
|--------------|-------------------:|--------:|-------:|---------------:|
| Govern (GV) | 25% | 58% | +33 | 83% |
| Identify (ID) | 50% | 67% | +17 | 83% |
| Protect (PR) | 60% | 80% | +20 | 90% |
| Detect (DE) | 25% | 50% | +25 | 75% |
| Respond (RS) | 50% | 88% | +38 | 100% |
| Recover (RC) | 25% | 75% | +50 | 100% |
| **Overall (22 categories)** | **41%** | **70%** | **+29** | **89%** |

*Scoring: each CSF category scores Full = 1, Partial = 0.5, Gap = 0. The percentage is the total score divided by the number of categories in the function.*

## 3. Portfolio Health Indicators

| Indicator | Baseline | Q4 2026 | Target | Status |
|-----------|---------:|--------:|-------:|--------|
| Governed documents with a named owner | 57% | 100% | 100% | ✅ Met |
| Documents formally reviewed in the last 24 months | 9% | 100% | 95% | ✅ Met |
| Requirements with a unique ID | 0% | 100% | 100% | ✅ Met |
| Requirements traced to CSF and NIST Special Publication (SP) 800-53 | 0% | 100% | 100% | ✅ Met |
| Team-maintained pages that set mandatory rules | 7 | 0 | 0 | ✅ Met |
| Open conflicting requirements | 6 | 0 | 0 | ✅ Met |
| Average days from draft to approval | Not tracked | 41 | 30 | ⚠️ Not met |
| Open documentation gaps (CSF categories) | 9 | 3 | 0 | ⚠️ In progress |

## 4. Remediation Backlog (Prioritized)

Priorities were set with document owners and security leadership on October 29, 2026. **Priority** combines audit exposure, risk, and effort.

| Rank | Item | Type | CSF / SP 800-53 | Owner | Effort | Target Date | Status |
|------|------|------|-----------------|-------|--------|-------------|--------|
| 1 | Add leadership program oversight requirement to ISP-001 | Gap (GAP-01) | GV.OV; PM-1, PM-9 | Director of Information Security | Low | 12/15/2026 | Drafting |
| 2 | Onboard two critical systems to central logging | Partial (GAP-04) | DE.CM; AU-6 | Manager, Security Operations | Medium | 01/31/2027 | Not started |
| 3 | Draft Network Security Standard | Gap (GAP-03) | PR.IR; SC-7 | Manager, Network Engineering | High | 03/31/2027 | Interviews scheduled |
| 4 | Contractor account end dates and weekly termination reconciliation | Partial | PR.AA-05; AC-2, PS-7 | Manager, Identity and Access Management (IAM) | Medium | 02/28/2027 | Backlog for STD-AC-001 v1.1 |
| 5 | Set recovery objectives for remaining 5 critical systems | Partial | RC.RP; CP-2 | System owners | Medium | 02/28/2027 | 2 of 5 in review |
| 6 | Add regulator and customer notification templates to PRO-IR-001 | Partial (GAP-05) | RS.CO; IR-6 | Legal Counsel | Low | 01/15/2027 | Drafting |
| 7 | Build compliance obligations register | Gap (GAP-02) | GV.OC; PM-9 | GRC Manager | Medium | 03/31/2027 | Not started |
| 8 | Add media handling rules to STD-PR-003 | Family gap | MP-6, MP-7 | Privacy Office Lead | Low | 02/15/2027 | Not started |

## 5. Decisions Needed from Leadership

| # | Decision | Options | Recommendation |
|---|----------|---------|----------------|
| 1 | Approve the risk committee as the body for twice-yearly program oversight (GAP-01) | (a) Risk committee; (b) a new security steering group | (a): it already meets quarterly and includes the right executives. |
| 2 | Shorten approval cycle time | (a) Keep current process; (b) allow minor revisions to be approved by the document owner only | (b): minor revisions made up 60% of approvals this quarter and do not change requirements. |
| 3 | Physical security documentation ownership | (a) Facilities; (b) Information Security | (a) owns the process, with Information Security as a required reviewer. |

## 6. Next Report

The Q1 2027 report will be delivered by April 15, 2027, and will add trend data for the Q2 2027 targets.
