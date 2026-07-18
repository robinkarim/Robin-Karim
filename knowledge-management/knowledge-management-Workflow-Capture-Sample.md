# Workflow Capture: Manual Insurance Eligibility Verification Override

**Captured from:** Interview with senior enrollment specialist
**Purpose:** Document a process currently held informally by one team member, so it does not depend on that person's availability.

---

### Context

The automated eligibility verification system correctly handles most enrollment cases, but fails silently for a specific scenario: a dependent added mid-year under a qualifying life event, where the insurance carrier's file feed has not yet been updated to reflect the new dependent. In this scenario, the automated check returns "ineligible" even though the enrollment is valid. Currently, only one specialist reliably recognizes this pattern and knows how to override it correctly.

### Captured Workflow

1. **Recognize the pattern.** The eligibility system returns "ineligible" for a dependent added under a qualifying life event within the last 10 business days. This timing window is the key signal — an "ineligible" result outside that window is more likely a genuine eligibility issue and should not be overridden using this workflow.
2. **Confirm the qualifying event.** Check the enrollment record for the qualifying life event type and date. Marriage, birth, and adoption events all qualify; a general "family status change" entry without a specific sub-type does not — escalate those instead of overriding.
3. **Check the carrier feed status.** Open the carrier feed dashboard and confirm the dependent does not yet appear in the carrier's system. If the dependent already appears, the "ineligible" result is likely a genuine issue, not a feed-timing gap — do not override.
4. **Apply the manual override.** In the enrollment system, apply the "Pending Carrier Sync" override code, which allows the enrollment to proceed while flagging it for automatic re-verification once the carrier feed updates.
5. **Set a follow-up check.** The system automatically re-checks overridden records after 15 business days. If the carrier feed still hasn't updated by then, the case is escalated to the carrier relations team rather than re-overridden again.

### Why This Matters

Without this override, a valid new dependent could be denied coverage processing for weeks while waiting on the carrier's own feed timing — a delay that has nothing to do with actual eligibility. Capturing this as a documented workflow, rather than leaving it as one specialist's judgment call, means any enrollment specialist can apply it consistently and correctly.

### Open Question for Process Owner

Should the 10-business-day recognition window in Step 1 be configurable, since carrier feed timing varies by carrier? Flagged for the process owner to confirm before this workflow is finalized as a formal SOP.

---
*This capture has been generalized from a production knowledge-management engagement. Specific system names and carrier details have been altered.*
