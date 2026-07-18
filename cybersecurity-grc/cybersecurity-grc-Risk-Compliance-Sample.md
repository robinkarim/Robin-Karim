# Risk and Compliance Narrative
## Access Review Control — Mapping to ISO/IEC 27001 Annex A.9

**Purpose:** Connect an implemented control to the standard it satisfies, in language a non-specialist reviewer (auditor, business sponsor) can follow without needing prior framework expertise.

---

### The Control in Plain Terms

Every quarter, managers review the list of people who have access to systems containing customer data and confirm that each person still needs that access for their current role. Access that is no longer needed is removed within 5 business days of the review.

### Why This Control Exists

People change roles, leave teams, or leave the organization more often than access lists get updated on their own. Without a recurring review, access tends to accumulate — someone moves to a new team but keeps their old system access "just in case." That accumulated access is exactly what an attacker benefits from if an account is ever compromised: more access means more potential damage from a single compromised credential.

### Standard Alignment

This control satisfies **ISO/IEC 27001 Annex A.9 (Access Control)**, specifically the requirement that user access rights be reviewed at planned intervals and adjusted following any change in role or employment status. It also supports the **NIST Cybersecurity Framework's Protect function**, under identity management and access control.

### How Compliance Is Evidenced

- Quarterly review sign-off from each manager, retained for audit
- System-generated report showing access removed within the 5-day window, or an documented exception with business justification
- Any exception beyond 10 business days requires information security officer approval, logged in the exception register

### Common Audit Question and Response

**"How do you know a manager actually reviewed the list, rather than just approving it without checking?"**
The review interface requires an explicit action per user (Confirm / Remove) rather than a single blanket sign-off, and the system logs which option was selected for each entry. A blanket approval with no individual actions taken is flagged for follow-up rather than accepted as a completed review.

### Residual Risk Note

Contractors provisioned through a separate onboarding path are reviewed on the same quarterly cycle but by a different manager population (procurement-approved leads rather than direct people managers). This is documented as a known variance rather than a gap, since the control intent — periodic review, timely removal — is still met.

---
*This sample has been generalized and does not describe the specific control environment of any organization. Prepared as the documentation lead working with compliance SMEs; not a certified compliance determination.*
