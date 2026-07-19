# Use Case: Submit and Track a Service Request

**Use Case ID:** UC-014
**Actor:** End User (any authenticated employee)
**Related Requirement:** BR-01, BR-03

---

### Description

An end user submits a service request through the self-service portal and tracks it through to resolution, receiving status updates without needing to contact the service desk directly.

### Preconditions

- User is authenticated via single sign-on.
- The self-service portal is available and the user's department is mapped to a valid request category.

### Main Flow

1. User navigates to the self-service portal and selects **New Request**.
2. User selects a request category (e.g., Hardware, Access, Software Install).
3. System displays a category-specific form with required fields.
4. User completes the form and attaches supporting files if needed, then submits.
5. System generates a ticket number, assigns a priority based on category rules, and routes the ticket to the correct fulfillment queue.
6. User receives an email confirmation containing the ticket number and expected SLA window.
7. Fulfillment team updates the ticket status as work progresses; user receives a notification at each status change.
8. Fulfillment team marks the ticket **Resolved** and adds resolution notes.
9. User receives a resolution notification and has 5 business days to reopen the ticket before it is automatically closed.

### Alternate Flows

**3a. Required field left blank**
System blocks submission and highlights the missing field(s) with inline validation messaging. User corrects and resubmits.

**5a. Category cannot be auto-routed**
If category rules do not resolve to a single queue (e.g., a request spanning both Access and Hardware), the ticket routes to a triage queue for manual assignment by a service desk agent within 1 business hour.

**9a. User reopens ticket**
User selects **Reopen** within the 5-day window and adds a comment describing why the resolution was incomplete. Ticket reverts to **In Progress** and reassigns to the original fulfillment agent.

### Exception Flow

**E1. Portal outage during submission**
If the portal is unavailable, the user is directed to a fallback phone line; ticket is logged manually by a service desk agent using the same category rules, and the user receives the same confirmation email once the ticket is entered.

### Postconditions

- Ticket exists in the system with a full audit trail of status changes and timestamps.
- SLA clock starts at ticket creation and stops at first "Resolved" status.

---
*This sample has been generalized from production use-case documentation. Category names, SLA windows, and routing logic have been altered.*
