# Security Documentation Style Guide

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-STY-001 |
| Document type | Style guide |
| Version | 1.0 |
| Document owner | Governance, Risk, and Compliance (GRC) Manager |
| Maintained by | Robin Karim, Technical Writer, GRC |
| Effective date | November 1, 2026 |
| Next scheduled review | July 2027 |

---

## 1. Purpose

This guide keeps every Meridian Enterprise Services ("Meridian") security policy, standard, and procedure consistent, so readers know what is required, who must do it, and by when. It applies to all governed security documents and to any team page that links to them.

For general grammar and punctuation not covered here, follow the *Microsoft Writing Style Guide*.

## 2. Document Types

| Type | Answers | Mandatory? | Typical Approver | Requirement Words |
|------|---------|------------|------------------|-------------------|
| Policy | What we require and why | Yes | Chief Information Security Officer (CISO) | shall, shall not |
| Standard | The specific rule that meets the policy | Yes | Director of Information Security | must, must not |
| Procedure | The exact steps to follow | Yes, when the standard calls for it | Director of Information Security | Numbered imperative steps |
| Guideline | A recommended way to do something | No | Document owner | should, may |

## 3. Requirement Language

Use these words exactly. Do not swap in other words that sound similar.

| Word | Meaning | Use In |
|------|---------|--------|
| shall / shall not | A leadership-level requirement | Policies |
| must / must not | A mandatory, testable requirement | Standards and procedures |
| should / should not | A recommendation; exceptions do not need approval | Guidelines |
| may | Permitted but optional | Any document |

**Avoid:** "will," "is required to," "needs to," "is expected to," "it is important that." These are vague or hide who is responsible.

### 3.1 Write Testable Requirements

Every requirement must make clear **who or what it applies to**, **what must happen**, and **when or how often**, so an auditor can test it. Name the responsible role whenever one person or team is accountable.

| Weak | Strong |
|------|--------|
| Access should be reviewed regularly. | System owners **must** review user access to their systems every quarter. |
| Patches will be applied in a timely manner. | Information Technology (IT) Operations **must** apply critical security patches within 14 days of release. |
| Incidents are to be reported. | Workforce members **must** report suspected security incidents to the Security Operations hotline right away. |

### 3.2 One Requirement per Statement

Split statements that contain "and" between two separate obligations. Each requirement gets its own ID so it can be traced in the [Control Traceability Matrix](05-control-traceability-matrix.md).

## 4. Approved Terminology

| Use | Do Not Use | Note |
|-----|------------|------|
| cybersecurity | cyber security, cyber-security | One word, as used by the National Institute of Standards and Technology (NIST) and the Cybersecurity and Infrastructure Security Agency (CISA). |
| multifactor authentication (MFA) | two-factor, 2FA, multi-factor | MFA covers two or more factors. |
| workforce member | user, staff, associate (in policy scope statements) | Covers employees, contractors, and temporary staff. Use "user" only when referring to an account. |
| security incident | breach (unless Legal has confirmed one), event (when an incident is confirmed) | "Breach" has legal meaning. Only Legal declares a breach. |
| system owner | business owner, app owner | The person accountable for a system's risk. |
| document owner | author, maintainer | The person accountable for a document's accuracy. |
| Restricted, Confidential, Internal, Public | secret, sensitive, private | Use only the four approved classification levels, capitalized. |
| Security Operations | SOC team, security desk | Use "Security Operations Center (SOC)" only when referring to the 24/7 monitoring function itself. |
| privileged account | admin account, super user | |
| right away | immediately, ASAP | Give a time frame whenever one exists. |

## 5. Acronyms

- Spell out every acronym the first time it appears in a document, followed by the acronym in parentheses, for example: Governance, Risk, and Compliance (GRC).
- After the first use, use the acronym alone. Do not spell it out again later in the same document.
- The metadata table at the top of a document counts as the first use.
- Framework identifiers (for example, PR.AA-05 or AC-2) are not spelled out; link to the framework instead.

## 6. Formatting Rules

| Element | Rule |
|---------|------|
| Headings | Title case for all headings. Number level-2 headings (1., 2., 3.) and their subsections (3.1, 3.2). |
| Requirement IDs | Policy statements: `[DOC]-[FUNCTION]-[NN]`, for example ISP-PR-02. Standard requirements: `[TOPIC]-STD-[NN]`, for example AC-STD-15. IDs are never reused after a requirement is removed. |
| Dates | "November 1, 2026" in metadata tables and running text; MM/DD/YYYY in data tables, logs, and revision history. |
| Times and time frames | Use numerals: 4 hours, 30 days, 5 business days. |
| Lists | Use numbered lists for steps in order and bulleted lists for everything else. |
| Tables | Use tables for requirements, roles, and anything compared across more than two attributes. |
| Notes and warnings | **Note:** for helpful context. **Warning:** for actions that could cause data loss, outages, or lost evidence. |
| Emphasis | Bold the requirement word (**must**, **shall**). Do not use italics for emphasis. |
| Links | Link to the governed document, never to a copy. |

## 7. Voice and Tone

- Write in plain language at about an 8th–10th grade reading level.
- Prefer active voice. Write "System owners must review access," not "Access must be reviewed." Passive voice is acceptable in policy statements that apply to the whole organization, because the Roles and Responsibilities section assigns accountability.
- Address procedure readers directly: "Open an incident record."
- Keep sentences under 25 words where possible.
- Explain the reason for a requirement when it is not obvious. Readers follow rules they understand.

## 8. Required Sections

| Section | Policy | Standard | Procedure |
|---------|:------:|:--------:|:---------:|
| Metadata table | ✓ | ✓ | ✓ |
| Purpose | ✓ | ✓ | ✓ |
| Scope | ✓ | ✓ | ✓ |
| Roles and responsibilities | ✓ | Optional | ✓ |
| Requirements or policy statements | ✓ | ✓ | — |
| Procedure steps | — | — | ✓ |
| Compliance measurement | Optional | ✓ | Optional |
| Exceptions | ✓ | ✓ (reference policy) | — |
| Enforcement | ✓ | — | — |
| Related documents | ✓ | ✓ | ✓ |
| Revision history | ✓ | ✓ | ✓ |

Templates for each type: [policy](policy-template.md), [standard](standard-template.md), and [procedure](procedure-template.md).

## 9. Pre-Submission Checklist

Before sending a draft for review, confirm that:

- [ ] The correct template was used, and every required section is present.
- [ ] Every requirement uses the approved requirement word and makes clear who or what, what, and when.
- [ ] Every requirement has a unique ID.
- [ ] Each acronym is spelled out once, on first use.
- [ ] Terminology matches Section 4.
- [ ] All links point to governed documents in the GRC document library.
- [ ] Spelling and grammar have been checked.
- [ ] The revision history is updated.
