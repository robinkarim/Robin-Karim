# AI Governance & Acceptable Use Policy

*A Model Policy for Generative AI Use in a FINRA/SEC-Regulated Environment*

**Writing sample prepared by Robin Karim** — Senior Technical Writer & IT Business Systems Analyst
[robinrkarim@yahoo.com](mailto:robinrkarim@yahoo.com) | [github.com/robinkarim/Robin-Karim/tree/writing-samples](https://github.com/robinkarim/Robin-Karim/tree/writing-samples)

> **Sample scope note:** This document is a demonstrative policy artifact written for portfolio purposes. It is modeled on real regulatory frameworks (FINRA, SEC, model risk management practice) but is not an actual policy of any current or former employer and contains no proprietary or confidential content.

---

## 1. Purpose and Scope

This policy establishes the requirements, controls, and governance structure for the responsible use of artificial intelligence (AI), including generative AI and large language models (LLMs), across the firm. It applies to all employees, contractors, and third-party vendors who use AI tools in connection with firm business, including client communications, research, marketing, operations, and internal productivity.

This policy supports the firm's obligations as a member of the Financial Industry Regulatory Authority (FINRA) and an entity subject to oversight by the U.S. Securities and Exchange Commission (SEC). It is intended to be read alongside the firm's existing Written Supervisory Procedures (WSPs), Information Security Policy, and Vendor Risk Management Policy, not to replace them.

## 2. Regulatory Framework

AI use is not exempt from existing securities regulation. The following authorities directly inform this policy:

- **FINRA Regulatory Notice 24-09** (June 27, 2024) — reminds member firms that FINRA rules and federal securities laws apply to the use of generative AI and LLMs on a technology-neutral basis, and that AI use implicates supervision, model risk management, data privacy, and accuracy obligations.
- **FINRA Rule 3110 (Supervision)** — requires a reasonably designed supervisory system for any AI tool used in the course of firm business, including tools that draft, summarize, or surface client-facing content.
- **FINRA Rule 2210 (Communications with the Public)** — content standards apply to AI-generated or AI-assisted communications exactly as they apply to human-drafted communications; AI authorship does not change the review and approval requirement.
- **SEC proposed Rule 211(h)(2)-4** under the Investment Advisers Act and related Exchange Act **Rule 15l-2** (Conflicts of Interest Associated with the Use of Predictive Data Analytics) — while not yet finalized as of this writing, the proposal signals the SEC's expectation that firms identify and neutralize conflicts of interest arising from AI-driven investor interactions; this policy adopts its conflict-review approach as a forward-looking control.
- **Regulation S-P** — governs the privacy and safeguarding of client nonpublic personal information (NPI); no NPI may be entered into an AI tool that is not on the Approved AI Tools List in Section 5.
- **Model risk management principles** consistent with interagency guidance (e.g., SR 11-7-style practice) — applied here to AI/LLM outputs used in any analytical, forecasting, or decision-support capacity.

## 3. Governance Structure and Roles

### 3.1 AI Governance Committee

A cross-functional AI Governance Committee (Compliance, Legal, Information Security, Information Technology (IT) Audit, and business-line representatives) owns this policy, approves new AI use cases, and meets quarterly or upon material change in AI tooling or regulatory guidance.

### 3.2 Roles and Responsibilities

| Role | Responsibility |
|---|---|
| AI Governance Committee | Approves/denies AI use case intake requests; reviews risk tiering; escalation point for AI-related incidents. |
| Compliance | Confirms alignment with FINRA Rules 3110/2210 and SEC guidance; reviews AI-assisted client communications prior to release. |
| IT Audit | Performs independent, periodic control testing of AI tools per Section 7; validates logging, access controls, and vendor attestations. |
| Information Security | Vets AI tools for data handling, encryption, and NPI exposure risk before addition to the Approved AI Tools List. |
| Business Owners | Complete use-case intake forms; ensure human-in-the-loop review; maintain prompt/output logs for their function. |

## 4. AI Use Case Risk Classification

Every AI use case is classified at intake and re-assessed annually or upon material change:

| Tier | Definition | Example |
|---|---|---|
| Low | Internal productivity use; no client data, no external communication, no decision impact. | Drafting internal meeting notes or a Standard Operating Procedure (SOP) outline. |
| Medium | Client-facing output or internal analysis with human review before use. | AI-drafted client email reviewed and released by a registered representative. |
| High | Client data processed, or output materially influences an investment, supervisory, or compliance decision. | AI-assisted surveillance summary used to flag potential Rule 3110 exceptions. |

## 5. Acceptable Use Standards

### 5.1 Approved Tools and Data Handling

- Only AI tools on the current Approved AI Tools List (maintained by Information Security) may be used for firm business; personal or unauthorized AI accounts are prohibited for any work-related task.
- Client NPI, account numbers, and material non-public information (MNPI) must never be entered into an AI tool unless that tool has an executed data processing agreement and has been rated for NPI/MNPI handling.
- Every prompt and corresponding output for Medium- and High-tier use cases must be logged, time-stamped, and retained per the firm's books-and-records schedule.

### 5.2 Prohibited Uses

- Using AI output as a final, unreviewed client communication or public-facing marketing material.
- Using AI to generate performance projections, guarantees, or forward-looking statements without Compliance pre-clearance.
- Using AI to circumvent or auto-approve required supervisory review steps.

## 6. Human-in-the-Loop Review and Supervision

Consistent with FINRA Rule 3110, every Medium- or High-tier AI output requires documented human review before use. The reviewer attests, at minimum, to factual accuracy against a verified source, absence of fabricated ("hallucinated") content, and compliance with Rule 2210 content standards. Reviewer identity, date, and disposition are recorded in the use-case log referenced in Section 5.1.

## 7. IT Audit and Controls Review

IT Audit performs an independent review of AI tooling on the following cadence and scope:

| Control Area | Test Performed | Frequency |
|---|---|---|
| Access management | Confirm AI tool access is provisioned/de-provisioned per Human Resources (HR) events and least-privilege role mapping. | Quarterly |
| Logging integrity | Sample prompt/output logs for completeness against the use-case register. | Quarterly |
| Vendor due diligence | Re-validate Service Organization Control 2 (SOC 2) reports (or equivalent) and data processing terms for each Approved AI Tool. | Annually |
| Model risk review | Re-assess High-tier use cases for drift, accuracy, and continued fitness for purpose. | Semi-annually |
| Incident review | Root-cause review of any reported AI-related error, complaint, or near-miss. | As triggered |

Findings are reported to the AI Governance Committee with a remediation owner and target date; unresolved High-tier findings are escalated to Compliance leadership within five business days.

## 8. Data Privacy and Security

All AI tool onboarding follows Information Security's standard vendor risk assessment, with specific attention to Regulation S-P safeguards for client NPI: data residency, encryption in transit and at rest, retention/deletion terms, and whether prompts or outputs are used to train the vendor's underlying model (which is prohibited unless explicitly disclosed to and approved by the firm).

## 9. Training and Attestation

- All personnel with AI tool access complete role-based AI use training at onboarding and annually thereafter.
- Annual attestation confirms understanding of the Approved AI Tools List, prohibited uses, and the human-in-the-loop requirement.

## 10. Policy Review and Ownership

This policy is owned by Compliance in partnership with Information Security and is reviewed at least annually, and upon any material FINRA or SEC guidance update, by the AI Governance Committee.

## Appendix A: AI Use Case Intake Form (Abridged)

| Field | Description |
|---|---|
| Use case name / owner | Business function and named accountable owner. |
| AI tool | Must be selected from the Approved AI Tools List. |
| Data inputs | Confirmation of whether client NPI or MNPI is involved. |
| Risk tier | Low / Medium / High per Section 4. |
| Review workflow | Named human reviewer and approval step prior to use/release. |
| Logging plan | Where prompt/output logs are stored and for how long. |

