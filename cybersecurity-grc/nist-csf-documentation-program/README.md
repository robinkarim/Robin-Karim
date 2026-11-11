# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) Security Documentation Program — Writing Samples

**Author:** Robin Karim, Senior Technical Writer and Information Technology (IT) Business Systems Analyst
**Portfolio:** [github.com/robinkarim/Robin-Karim](https://github.com/robinkarim/Robin-Karim) | [LinkedIn](https://www.linkedin.com/in/robinkarim)

## About This Folder

This folder holds a complete set of writing samples that show how I remediate, consolidate, and maintain an information security documentation portfolio aligned with NIST CSF 2.0 and NIST Special Publication (SP) 800-53 Rev. 5.

The samples are written for **Meridian Enterprise Services**, a fictional mid-sized company whose Information Security team inherited a scattered set of policies, wiki pages, and team runbooks. The scenario follows a six-month engagement: the first half focuses on remediation and consolidation, and the second half sets up the routines that keep the portfolio current.

> **Note:** Meridian Enterprise Services, its staff names, systems, and metrics are fictional. The frameworks, control identifiers, and documentation practices are real and reflect how I approach this work on the job.

## What Is in This Folder

| # | File | Document Type | What It Shows |
|---|------|---------------|---------------|
| 1 | [01-information-security-policy.md](01-information-security-policy.md) | Policy | A governing policy organized around the six CSF functions |
| 2 | [02-access-control-standard.md](02-access-control-standard.md) | Standard | Operational requirements moved out of team-maintained guidance into a governed standard |
| 3 | [03-incident-response-procedure.md](03-incident-response-procedure.md) | Procedure | A step-by-step procedure covering the Respond and Recover functions |
| 4 | [04-policy-consolidation-map.md](04-policy-consolidation-map.md) | Consolidation crosswalk | How 23 legacy documents became 11 governed documents |
| 5 | [05-control-traceability-matrix.md](05-control-traceability-matrix.md) | Traceability matrix | Requirements traced to CSF categories and SP 800-53 control families, with gaps flagged |
| 6 | [06-document-lifecycle-management.md](06-document-lifecycle-management.md) | Lifecycle plan and register | Version control, ownership records, review and approval workflow, and review calendar |
| 7 | [07-security-documentation-style-guide.md](07-security-documentation-style-guide.md) | Style guide | Approved terminology, requirement language, and house style |
| 8 | [08-stakeholder-interview-guide.md](08-stakeholder-interview-guide.md) | Interview guide | How I interview control operators and turn their answers into written requirements |
| 9 | [09-csf-alignment-tracker.md](09-csf-alignment-tracker.md) | Compliance monitoring report | Quarterly CSF coverage tracking and a prioritized remediation backlog |
| — | [traceability-matrix.csv](traceability-matrix.csv) | Data file | Sortable copy of the traceability matrix for spreadsheet or governance, risk, and compliance (GRC) tool import |
| — | [policy-template.md](policy-template.md) | Template | Reusable policy template (used for File 1) |
| — | [standard-template.md](standard-template.md) | Template | Reusable standard template (used for File 2) |
| — | [procedure-template.md](procedure-template.md) | Template | Reusable procedure template (used for File 3) |

## How the Samples Map to the Work

| Responsibility | Where It Is Demonstrated |
|----------------|--------------------------|
| Draft and revise policies, standards, and procedures using CSF-aligned templates | Files 1–3 and the three template files |
| Consolidate documents into a structure organized around Govern, Identify, Protect, Detect, Respond, and Recover | Files 1 and 4 |
| Move operational requirements from team-maintained guidance into governed documentation | Files 2 and 4 |
| Apply approved terminology, templates, and house style | File 7, applied across every file |
| Incorporate stakeholder and leadership feedback through review and final approval | File 6 (approval workflow) and the revision history in Files 1–3 |
| Trace requirements to CSF functions and SP 800-53 control families to expose gaps | File 5 |
| Manage version control, ownership, review and approval cycles, and the review calendar | File 6 |
| Maintain templates, style guidance, and documentation as the program evolves | Files 6 and 7 |
| Support compliance monitoring by tracking CSF alignment over time | File 9 |
| Interview security, IT, and business stakeholders and translate practices into requirements | File 8 |
| Partner with document owners and security leadership to prioritize remediation | Files 6 and 9 |

## Document Hierarchy Used in These Samples

```
Policy      → What the organization requires and why (approved by leadership)
  Standard  → The specific, measurable rules that satisfy the policy
    Procedure → The step-by-step instructions a team follows to meet the standard
      Guideline → Recommended practices (not mandatory)
```

## Frameworks Referenced

- NIST Cybersecurity Framework (CSF) 2.0 (February 2024)
- NIST SP 800-53 Rev. 5, *Security and Privacy Controls for Information Systems and Organizations*
- NIST SP 800-61 Rev. 3, *Incident Response Recommendations and Considerations for Cybersecurity Risk Management*

## Why Markdown

These samples are written in Markdown and stored in Git on purpose. A docs-as-code approach gives every document a full change history, makes reviews visible through pull requests, and keeps the portfolio easy to search and maintain.
