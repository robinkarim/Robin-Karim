# KB0142 — Patient Portal Login Fails After Password Reset

**Category:** Patient Portal / Authentication
**Audience:** Support Tier 1
**Last Reviewed:** Current cycle

---

### Symptom

Patient successfully completes a password reset (receives the "password updated" confirmation) but the new password is rejected when attempting to log in immediately afterward.

### Cause

The portal's authentication cache can take up to 5 minutes to recognize a newly reset password. Attempting to log in immediately after reset, before the cache clears, returns an "invalid credentials" error even though the new password is correct.

### Resolution

1. Confirm with the patient that they received the password reset confirmation (email or on-screen message). If not, the reset itself did not complete — do not proceed with this article; escalate to KB0098 (Password Reset Not Completing).
2. Ask the patient to wait 5 minutes and attempt login again without requesting another reset.
3. If login still fails after 5 minutes, confirm the patient is entering the password exactly as set (check for autofill from a password manager using an old saved value).
4. If login continues to fail after step 3, escalate to Tier 2 with the patient's account identifier and the exact error message displayed.

### Do Not

Do not have the patient request a second password reset while troubleshooting this issue — overlapping reset requests can leave the account in an inconsistent state that requires manual Tier 2 intervention to resolve.

### Related Articles

- KB0098 — Password Reset Not Completing
- KB0156 — Patient Portal Account Locked After Failed Attempts

---
*This article has been generalized from production knowledge base content. Ticket volume patterns and specific system names have been altered.*
