# Process Maps: Employee Offboarding

**Process Name:** Employee Offboarding — As-Is / To-Be Analysis  
**Organization:** [Automotive Manufacturing Company]  
**Prepared by:** AI Process Innovation Analyst  
**Date:** May 2026  

---

## Section 1: As-Is Process (Current State Swimlane — Narrative Form)

The following describes the current offboarding process as observed across facilities, mapped by actor in swimlane sequence. Steps are labeled with the responsible actor in brackets.

---

**[Manager]** — A team member submits a resignation or the manager initiates a termination decision. The manager verbally notifies HR and sends an email — often to a personal HR contact rather than a shared inbox or system — with basic details: employee name, last day, and reason for departure. No standard form or system entry is required at this stage. The timing of this notification varies widely, sometimes occurring days after the decision is made.

**[HR]** — Upon receiving the manager's notification, an HR Business Partner manually creates a separation record in the HRIS (e.g., SAP HCM or Workday). HR then drafts a departure checklist — typically a Word document or spreadsheet maintained locally — and manually emails individual departments (IT, Payroll, Security, Benefits) with relevant details. There is no centralized ticketing system or automated routing. HR tracks completion by following up via email threads.

**[Employee]** — The departing employee may or may not receive formal offboarding communications at this stage. In many cases, the employee is handed a generic checklist or verbally told what to expect. There is no self-service portal or structured guide. The employee continues working, often unaware of what documentation, assets, or knowledge transfer is expected of them before their final day.

**[Manager]** — The manager is expected to coordinate a knowledge transfer but receives no structured framework or timeline to do so. Conversations about handoffs happen informally, if at all. Open projects, supplier contacts, equipment ownership, and process documentation are rarely captured in a formal transition plan.

**[HR]** — HR separately schedules an exit interview, often within the final week or on the last day itself. The format varies by HR partner — some use a structured form, others conduct an informal conversation. Responses are recorded in personal notes, a shared drive folder, or not at all. There is no standard repository or analysis workflow for exit data.

**[IT]** — IT receives the offboarding notification via email from HR and manually queues account deprovisioning. Depending on workload and notification timing, this may happen before or after the employee's last day — or in some cases, days afterward. Active Directory, email, VPN, ERP system access, and application licenses are revoked individually and manually. There is no automated trigger or deprovisioning workflow.

**[Security]** — Physical security (badge access) is managed by a separate team that also relies on HR email notification. Badge deactivation and access card return are tracked via a paper log or spreadsheet. There is no integration between the physical security system and the HRIS or IT deprovisioning workflow.

**[Payroll]** — Payroll receives a manual notification from HR and processes the final paycheck, PTO payout, and benefits termination separately. Errors frequently arise from late or incomplete information — particularly around final timesheet approval, shift differentials, or union pay rules. COBRA and 401(k) continuation packets are mailed or emailed without tracking or confirmation of receipt.

**[Employee]** — On their final day, the departing employee turns in physical assets (laptop, badge, tools) through a loosely coordinated process. They may or may not have completed a formal exit interview. They leave without confirmation that all steps are closed, and no alumni or post-separation follow-up is initiated.

**[HR]** — After the employee's departure, HR manually marks the HRIS record as terminated. Any outstanding checklist items are chased individually. Exit interview data — if collected — sits dormant. There is no post-mortem, offboarding scorecard, or feedback loop to leadership.

---

## Section 2: Pain Point Analysis

The following pain points are directly tied to specific actors and process steps observed in the As-Is state.

---

- **[Manager] Unstructured and delayed separation notification.** There is no required form, system trigger, or SLA for notifying HR when a separation occurs. Managers use informal email to personal contacts, causing downstream delays across IT, Payroll, and Security. In some cases, departments are not notified until the employee's final week — or after they have already left.

- **[HR] Manual, email-driven task coordination with no audit trail.** HR relies on individual emails to each department to initiate offboarding tasks. There is no centralized tracker, no automated escalation, and no real-time visibility into completion status. When something is missed, root cause is difficult to determine and accountability is unclear.

- **[IT] Delayed and inconsistent access deprovisioning.** IT receives late notifications and performs manual, system-by-system account revocation with no automated workflow. This creates a window of days — sometimes weeks — during which former employees retain access to sensitive manufacturing systems, ERP data, and shared drives, representing a significant cybersecurity and intellectual property risk.

- **[Security] Physical and digital security managed in silos.** Badge deactivation is disconnected from IT deprovisioning. A former employee's digital accounts may be revoked while building access remains active (or vice versa), creating inconsistent and incomplete offboarding closure. Neither system communicates with the other or with the HRIS.

- **[Manager / Employee] No structured knowledge transfer process.** There is no template, timeline, or accountability mechanism for capturing institutional knowledge before a departure. Critical information — supplier relationships, machine settings, custom workflows, undocumented tribal knowledge — is routinely lost, impacting operational continuity and increasing ramp-up time for replacements.

- **[Payroll] Final pay errors due to late or incomplete data.** Payroll depends on accurate, timely inputs from HR, managers (final timesheet approval), and Benefits. When these arrive late or inconsistently, final paychecks contain errors — wrong PTO balances, missing shift differentials, or late benefits terminations — that generate employee disputes, corrections, and in some cases, regulatory exposure.

- **[HR] Exit interview data collected but never utilized.** Exit interviews are conducted inconsistently, stored in unstructured formats, and rarely reviewed by leadership. The organization is sitting on a valuable, untapped signal about turnover drivers, management issues, compensation gaps, and process failures — but has no mechanism to surface or act on it at scale.

---

## Section 3: To-Be Process (Future State Swimlane — Narrative Form)

The following describes the redesigned offboarding process, incorporating automation, AI-assisted decision-making, and structured workflows. Automation and AI touchpoints are called out explicitly.

---

**[Manager]** — When a separation decision is made, the manager completes a structured **Separation Intake Form** embedded in Microsoft Teams or the HRIS self-service portal. Upon submission, a **Power Automate flow** is triggered automatically — routing the separation record to HR, creating departmental tasks in the offboarding system, and sending the employee a personalized offboarding welcome message. The manager receives an auto-generated **Knowledge Transfer Checklist** tailored to the employee's role, department, and tenure, pre-populated using role data from the HRIS.

> 🤖 **Power Automate:** Triggers multi-department offboarding workflow from a single form submission, eliminating manual email routing and ensuring no department is missed.

**[HR]** — HR receives a pre-built offboarding case in the HRIS or a connected service management tool (e.g., ServiceNow, Power Apps). All tasks — IT deprovisioning, Payroll notification, Benefits termination, exit interview scheduling — are automatically assigned with due dates and SLA timers. HR's role shifts from coordinator to exception manager: they are only alerted when tasks fall behind or require human judgment.

> 🤖 **Power Automate + Microsoft Copilot:** Copilot in Outlook or Teams summarizes the offboarding case status on demand, surfaces overdue tasks, and drafts follow-up communications to department owners without HR manually composing emails.

**[Employee]** — The departing employee receives a personalized **Offboarding Hub** — a self-service page (built in SharePoint or a Power Apps portal) that outlines their timeline, required actions, asset return instructions, and knowledge transfer expectations. They can complete and submit their knowledge transfer documentation directly through the portal. Progress is tracked automatically.

> 🤖 **Microsoft Copilot:** The employee can interact with a Copilot-powered FAQ assistant embedded in the Offboarding Hub to get answers about final pay, benefits continuation, 401(k) options, and asset return — reducing inbound HR inquiries.

**[Manager]** — The manager reviews and approves the employee's knowledge transfer submissions through the portal. If critical documentation is missing or incomplete, the system flags gaps and sends automated reminders with escalation to the manager's own manager if not resolved within the SLA window.

> 🤖 **AI Classification (Azure AI / Copilot Studio):** An AI model reviews submitted knowledge transfer documents and classifies them by completeness, topic coverage, and risk level — alerting HR when high-risk gaps (e.g., single-point-of-failure roles) are identified before the employee's last day.

**[IT]** — When the offboarding case is created, IT receives an automatically generated deprovisioning ticket with a target completion date tied to the employee's last day. An **automated deprovisioning workflow** — integrated with Active Directory, Microsoft Entra ID, and the ERP system — begins revoking access in a defined, auditable sequence. IT is notified of exceptions (e.g., shared accounts, delegated permissions) that require manual review.

> 🤖 **Power Automate:** Orchestrates account disablement, license reclamation, email delegation, and VPN revocation across systems in a defined order — triggered automatically at a scheduled time relative to the employee's last day, with a full audit log generated on completion.

**[Security]** — Badge deactivation is triggered through the same Power Automate flow — integrated with the physical access control system via API — at the same time as IT deprovisioning. The Security team receives a confirmation notification and is only required to intervene for exceptions (e.g., extended access requests, active investigations).

> 🤖 **Power Automate:** Unified trigger ensures IT and Physical Security deprovisioning happen in lockstep, eliminating the siloed, manual handoffs that create access gaps.

**[Payroll]** — Payroll receives a structured, system-generated notification containing all required data: final day, PTO balance (auto-calculated from HRIS), applicable pay rules (including union differentials), and benefits termination date. Final timesheet approval is routed automatically to the manager with a hard deadline enforced by the system. COBRA and benefits continuation packets are sent digitally with delivery confirmation tracked.

> 🤖 **Power Automate:** Automates final pay data assembly and routes for approval, reducing manual data entry errors and ensuring Payroll receives complete, accurate information on time.

**[HR]** — Exit interviews are scheduled automatically as part of the offboarding workflow, with a standardized digital survey sent to the employee in advance. Responses are stored in a centralized data repository. After submission, an **AI classification model** analyzes free-text responses — categorizing themes such as compensation concerns, management issues, career development, workload, or culture — and routes insights to a live analytics dashboard accessible to HR leadership and hiring managers.

> 🤖 **AI Classification (Azure AI Language / Copilot Studio):** Natural language processing categorizes and scores exit interview responses at scale, enabling HR leadership to identify turnover patterns, departmental risk signals, and systemic issues without manual review of individual responses.

**[HR / Manager]** — At case closure, an automated **Offboarding Scorecard** is generated — capturing cycle time, task completion rate, deprovisioning timeliness, and employee experience score — and shared with the HR Business Partner and hiring manager. Outstanding items are flagged for resolution. The departing employee is automatically added to an alumni outreach list for future re-engagement, referral programs, or boomerang hiring pipelines.

> 🤖 **Power Automate + Copilot:** Copilot generates a natural-language summary of the offboarding case for the hiring manager — highlighting what went well, what was delayed, and recommended actions for the next departure in the same team or role family.

---

*This document is a living artifact and will be updated as process workshops, stakeholder interviews, and tooling assessments are completed. The To-Be design assumes integration capability with the existing HRIS, Microsoft 365 ecosystem, and physical access control systems.*
