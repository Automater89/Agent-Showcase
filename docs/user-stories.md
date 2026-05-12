# User Stories: Future-State Employee Offboarding Workflow

**Process Name:** Employee Offboarding — Future State  
**Organization:** [Automotive Manufacturing Company]  
**Prepared by:** AI Process Innovation Analyst  
**Date:** May 2026  

---

## User Story 1

**As a** Manager,  
**I want** to submit a separation notification through a structured digital form in Microsoft Teams or the HRIS portal,  
**So that** all downstream departments (HR, IT, Payroll, Security) are automatically notified and their tasks are initiated simultaneously without me sending individual emails.

**Acceptance Criteria:**
- A separation intake form is accessible directly from Microsoft Teams or the HRIS self-service portal and requires no more than 5 minutes to complete.
- Upon form submission, a Power Automate flow triggers offboarding tasks for HR, IT, Payroll, and Security within 5 minutes, with no manual routing required.
- The manager receives a confirmation notification with a summary of what has been initiated and expected next steps.
- The form enforces required fields (employee name, last day, separation type) and prevents submission with missing critical data.

---

## User Story 2

**As a** Manager,  
**I want** to receive a structured, role-specific knowledge transfer checklist automatically when a team member's offboarding begins,  
**So that** I can ensure critical institutional knowledge, project handoffs, and supplier relationships are documented before the employee's last day.

**Acceptance Criteria:**
- A knowledge transfer checklist is auto-generated and delivered to the manager within one business day of separation intake submission.
- The checklist is pre-populated with role-relevant categories (e.g., active projects, key contacts, documented SOPs, system credentials to transfer) based on the departing employee's HRIS role data.
- The manager can assign checklist items to the departing employee or other team members and track completion status in the portal.
- An automated escalation reminder is sent to the manager if the checklist is less than 80% complete 3 business days before the employee's last day.

---

## User Story 3

**As an** HR Coordinator,  
**I want** a centralized offboarding case dashboard that shows real-time completion status of all tasks across departments,  
**So that** I can manage exceptions proactively without relying on email threads or manual follow-up to determine what has or hasn't been done.

**Acceptance Criteria:**
- A dashboard view displays all active offboarding cases with task status per department (IT, Payroll, Security, Benefits) in real time.
- Overdue tasks are visually flagged and an automated escalation notification is sent to the task owner and their manager when an SLA is breached.
- HR Coordinators can filter cases by department, facility, separation type, or last day date.
- The dashboard includes a case audit trail showing when each task was assigned, updated, and completed — accessible for compliance review.

---

## User Story 4

**As an** HR Coordinator,  
**I want** exit interview responses to be automatically analyzed and categorized by theme using AI,  
**So that** I can surface actionable turnover insights to leadership without manually reviewing and coding individual responses.

**Acceptance Criteria:**
- Exit interview responses are collected through a standardized digital form sent automatically to the departing employee at least 5 business days before their last day.
- AI classification (via Azure AI Language or Copilot Studio) categorizes free-text responses into predefined themes: compensation, management, career growth, workload, culture, or other.
- A monthly exit interview insights report is auto-generated and distributed to HR leadership and hiring managers, summarizing top themes by department and role family.
- Individual responses remain confidential and are not attributed to specific employees in any distributed report.

---

## User Story 5

**As an** IT Admin,  
**I want** account deprovisioning to be triggered automatically when an offboarding case is created and executed in a defined, auditable sequence,  
**So that** former employees' system access is revoked on time and I am not dependent on receiving a manual email notification from HR.

**Acceptance Criteria:**
- A deprovisioning ticket is automatically created in the IT service management system within 1 hour of offboarding case creation, with a target completion date set to the employee's last day.
- The automated workflow revokes access across Active Directory, Microsoft Entra ID, ERP systems, VPN, and shared drives in a defined sequence without requiring manual intervention for standard cases.
- IT receives automated exception alerts for non-standard scenarios (e.g., shared accounts, delegated inboxes, admin-level permissions) that require human review before revocation.
- A full deprovisioning audit log — listing each system, action taken, timestamp, and completed-by (user or automated process) — is generated and attached to the offboarding case on completion.

---

## User Story 6

**As a** Security (Physical Access) Administrator,  
**I want** badge deactivation to be triggered automatically through the same offboarding workflow that initiates IT deprovisioning,  
**So that** physical and digital access revocation happen in lockstep and I am not dependent on a separate manual notification from HR.

**Acceptance Criteria:**
- Badge deactivation is triggered by the same Power Automate flow that initiates IT deprovisioning, using an API integration with the physical access control system.
- Badge access is deactivated no later than end-of-business on the employee's last day, or immediately upon termination for involuntary separations.
- Security receives a confirmation notification when deactivation is complete and is alerted to any exceptions (e.g., extended access requests approved by HR or Legal).
- Asset return (access card, keys, PPE) is tracked through a digital checklist within the offboarding case, replacing the current paper log.

---

## User Story 7

**As an** HR Coordinator,  
**I want** final pay data to be automatically assembled from HRIS records and routed to Payroll with manager approval required before processing,  
**So that** final paychecks are accurate, compliant, and issued on time without errors caused by late or incomplete manual data entry.

**Acceptance Criteria:**
- When an offboarding case is created, the system auto-pulls the employee's PTO balance, pay rate, shift classification, and benefits termination date from the HRIS and populates a final pay summary.
- The final timesheet is routed automatically to the manager for approval, with a hard deadline of 2 business days before the last day enforced by the system.
- Payroll receives the completed final pay data package (including manager-approved timesheet) automatically upon manager sign-off, with no manual data re-entry required.
- COBRA and benefits continuation documents are sent digitally to the departing employee with delivery confirmation tracked within the offboarding case.

---

## User Story 8

**As a** New Hire Manager (hiring manager for the backfill role),  
**I want** to receive an auto-generated offboarding summary when a case is closed — including knowledge transfer completion status and exit interview themes — so that I can make informed decisions about backfill requirements, role redesign, and onboarding priorities for the replacement hire.

**Acceptance Criteria:**
- An offboarding close-out summary is automatically generated and sent to the hiring manager within 2 business days of case closure.
- The summary includes: knowledge transfer completion percentage, any documented gaps, anonymized exit interview theme categories, and offboarding cycle time.
- The summary is generated in plain language by Microsoft Copilot, formatted for a non-technical audience, and requires no manual authoring by HR.
- The hiring manager can access the full offboarding case record (excluding confidential exit interview content) through the HRIS or Power Apps portal for reference during backfill planning.

---

*User stories will be refined and prioritized in collaboration with stakeholders during Sprint 0 planning. Acceptance criteria are intended as a starting point for QA and UAT design.*
