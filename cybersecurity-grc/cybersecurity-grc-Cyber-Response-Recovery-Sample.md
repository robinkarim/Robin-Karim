# Cyber Incident Response and Recovery Procedure
## Confirmed Unauthorized Access Event

**Audience:** Security Operations, IT Leadership, Incident Commander
**Purpose:** Provide a usable, step-by-step procedure for responding to and recovering from a confirmed unauthorized access event, written to be followed under time pressure rather than read for background only.

---

### 1. Activation Criteria

This procedure activates when the security operations queue confirms unauthorized access to a production system — not on unconfirmed alerts, which follow the standard triage procedure instead.

### 2. Roles

| Role | Responsibility |
|---|---|
| Incident Commander | Owns the response, makes containment decisions, approves communications |
| Security Analyst | Executes containment and evidence-preservation steps |
| System Owner | Confirms business impact, approves any service interruption |
| Communications Lead | Drafts and sends internal and, if required, external notifications |

### 3. Immediate Actions (First 30 Minutes)

1. Incident Commander confirms activation and opens the incident bridge.
2. Security Analyst isolates the affected system from the network while preserving system state (do not power off — this destroys volatile evidence).
3. Security Analyst begins the evidence log: timestamp of detection, systems involved, initial indicators observed.
4. System Owner is notified and asked to confirm what business function, if any, is currently impacted.

### 4. Containment (Hour 1–4)

5. Security Analyst reviews access logs to determine the entry point and scope of access (which accounts, which data, which systems).
6. Compromised credentials are disabled immediately; password reset is required before re-enablement.
7. If the entry point is a known vulnerability, Incident Commander approves emergency patching or a temporary compensating control (e.g., firewall rule) ahead of the standard change process.

### 5. Eradication and Recovery (Hour 4–24)

8. Once the entry point is closed and credentials rotated, System Owner and Security Analyst jointly verify the system is clean before restoring network connectivity.
9. If data integrity is in question, restore from the last verified clean backup rather than attempting to "clean" the live system.
10. System Owner signs off before the system returns to production.

### 6. Communication

Internal stakeholders are updated at defined checkpoints (activation, containment achieved, recovery complete) regardless of whether the incident becomes reportable. Communications Lead determines, with legal/compliance input, whether external notification thresholds have been met.

### 7. Post-Incident

A post-incident review is scheduled within 5 business days to document root cause, timeline, and at least one corrective action. This procedure itself is reviewed for gaps as part of that meeting.

---
*This sample has been generalized from production incident-response documentation. It reflects the structure and pacing used for real procedures; specific tooling references and timelines have been altered.*
