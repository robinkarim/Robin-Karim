# Infrastructure Build Document
## Azure Resource Group Provisioning — Regional Reporting Environment

**Platform Owner:** Cloud Infrastructure Team
**Review Cycle:** Reviewed at each quarterly platform review, or upon material change

---

### 1. Purpose

Documents the standard build for provisioning a regional reporting environment resource group in Azure, including networking, access control, and monitoring configuration. Intended for infrastructure engineers performing the build and for platform owners validating it during review cycles.

### 2. Prerequisites

- Subscription-level Contributor access scoped to the target resource group
- Approved network address space allocation from the networking team
- Naming convention reference (Appendix A, maintained in the platform wiki)

### 3. Build Steps

1. Create the resource group using the approved naming convention: `rg-report-[region]-[env]`.
2. Deploy the virtual network using the allocated address space, with subnets separated for application tier and data tier.
3. Apply the standard network security group rule set, restricting inbound access to the application tier from the corporate VPN range only.
4. Deploy the reporting database instance with private endpoint connectivity (no public endpoint permitted in any environment, including non-production).
5. Configure diagnostic settings to route logs to the centralized Log Analytics workspace.
6. Apply resource tags per the tagging standard: cost center, environment, owner, data classification.
7. Validate the build against the platform owner's pre-handoff checklist before marking the environment ready for application deployment.

### 4. Access Control

Access to the resource group is granted through role-based access control groups only — no individual user role assignments are permitted, to keep access reviewable through the standard quarterly group membership audit.

### 5. Monitoring and Alerting

Standard alert rules are applied automatically through the platform's policy assignment: CPU threshold, storage threshold, and failed-connection-attempt alerting. Environment-specific alert rules beyond the standard set must be requested through the platform owner and documented in Appendix B.

### 6. Review Cycle Notes

This document is reviewed each quarter against the live environment to catch configuration drift — for example, a security group rule added manually outside the standard build process. Any drift identified during review is either brought back into alignment or the build document is updated to reflect an approved, intentional change.

---
*This document has been generalized from production infrastructure build documentation. Specific naming conventions, address ranges, and policy names have been altered.*
