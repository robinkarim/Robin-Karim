# Stakeholder Interview Guide: Turning Control Practices into Written Requirements

*Writing sample by Robin Karim. Meridian Enterprise Services is a fictional organization; the frameworks and control identifiers are real.*

| Field | Value |
|-------|-------|
| Document ID | GRC-GDE-001 |
| Document type | Working guide |
| Version | 1.0 |
| Prepared by | Robin Karim, Technical Writer, Governance, Risk, and Compliance (GRC) |
| Date | September 2026 |

---

## 1. Purpose

Most security controls already exist in some form before anyone writes them down. People patch servers, approve access, and review alerts every day. The goal of these interviews is to learn how a control **actually** works, compare that with what the documents say, and turn the real, approved practice into clear, testable requirements.

## 2. Who to Interview

| Stakeholder Group | Why Interview Them | Example Roles |
|-------------------|--------------------|---------------|
| Security | They own the control objectives and know where the risk is | Security Operations lead, Identity and Access Management (IAM) manager, vulnerability analyst |
| Information Technology (IT) | They operate most technical controls day to day | Help Desk lead, systems administrator, network engineer |
| Business | They own systems and data and approve access | Application owner, department manager, Human Resources (HR) partner |
| Oversight | They test the controls and know past findings | Internal Audit, Legal, Privacy Office |

## 3. Before the Interview

1. Read the current documents for the control area, including team wikis and runbooks.
2. Pull the relevant National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) 2.0 subcategories and NIST Special Publication (SP) 800-53 controls so you know what "complete" looks like.
3. Note any conflicts or gaps between documents.
4. Send the interviewee a short agenda and three or four of the questions ahead of time.
5. Book 45 minutes. Ask whether they can show you the process on screen.

## 4. Question Bank

Start broad, then get specific. Ask the interviewee to **show** rather than **tell** whenever possible.

### 4.1 How the Control Works Today

- Walk me through the last time you did this. What started it?
- What tool or system do you use? Can you show me?
- Who else is involved, and where does the work get handed off?
- How long does it usually take? What is the longest it has taken?

### 4.2 Rules and Decisions

- What has to be true before you can approve or complete this?
- Is there a time limit? Where did that number come from?
- What do you do when something does not fit the normal process?
- Who can make an exception, and how is it recorded?

### 4.3 Evidence

- If an auditor asked you to prove this happened last quarter, what would you show them?
- Where are those records kept, and for how long?

### 4.4 Gaps and Pain Points

- What part of this process breaks most often?
- Is there anything the current documentation says that you do not actually do? Why?
- If you could change one rule, what would it be?

## 5. After the Interview

1. Send a summary to the interviewee within 2 business days and ask them to correct anything wrong.
2. Sort what you learned into four groups:
   - **Already documented and accurate**: no change.
   - **Practiced but not documented**: candidate for a new requirement.
   - **Documented but not practiced**: flag for leadership; either the practice or the document must change.
   - **Neither documented nor practiced, but required by the framework**: a gap; add it to the gap list.
3. Draft requirements using the [Security Documentation Style Guide](07-security-documentation-style-guide.md).
4. Bring any conflicts to the document owner and security leadership for a decision. The writer documents decisions; the writer does not make them.

## 6. Worked Example: From Interview Notes to Requirements

**Interview:** Help Desk Lead and IAM Manager, September 3, 2026, 45 minutes
**Control area:** Account termination

### 6.1 Raw Notes (Summarized)

> "HR sends a ticket when someone leaves. Usually it comes in the same day, but sometimes it's a few days late. We try to disable the account as soon as we see the ticket. For firings, the manager usually pings us on chat and we do it while they're in the meeting. The runbook says three days, but nobody waits that long. Contractors are the problem — their managers forget to tell anyone. We don't really check afterward whether it got done."

### 6.2 Analysis

| Observation | Category | Framework Link |
|-------------|----------|----------------|
| Accounts are disabled when the HR ticket arrives; no defined time limit in practice | Practiced but not documented (and conflicts with the 3-day runbook rule) | PR.AA-05; AC-2, PS-4 |
| Involuntary terminations are handled through informal chat requests | Practiced but not documented; no audit trail | PS-4 |
| Contractor departures are often missed | Gap | PR.AA-05; PS-7 |
| No check that removal was completed | Gap | AC-2(j) |

### 6.3 Resulting Draft Requirements

These went to the Chief Information Security Officer (CISO) for a decision on the time frame, then into the [Access Control Standard](02-access-control-standard.md):

| Draft Requirement | Final Requirement ID |
|-------------------|----------------------|
| Access for terminated users **must** be disabled within 4 hours of the termination time recorded by HR. For involuntary terminations, access **must** be disabled before or at the time the user is notified. | AC-STD-15 |
| Contractor accounts **must** have an end date set at creation and **must** be disabled automatically on that date unless the sponsoring manager extends it. | Added to STD-AC-001 v1.1 backlog |
| The IAM team **must** compare the HR termination feed with active directory accounts every week and disable any account that was missed. | Added to STD-AC-001 v1.1 backlog |

### 6.4 Follow-Up Sent to Interviewees

> Thank you both for walking me through the termination process on Thursday. Here is what I captured. Please let me know by Friday if anything is wrong or missing.
>
> 1. Accounts are disabled when the HR ticket arrives, usually the same day.
> 2. Involuntary terminations come in through chat, and the account is disabled during the meeting.
> 3. Contractor departures are sometimes missed because no one notifies IAM.
> 4. There is no follow-up check that the account was disabled.
>
> I'll be drafting a time frame for leadership to approve and will share the draft standard with you for review before it goes further.
