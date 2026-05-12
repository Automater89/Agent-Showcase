# GitHub Copilot Prompts Used — Offboarding Process Redesign Project

**Project:** Employee Offboarding Process Redesign  
**Organization:** [Automotive Manufacturing Company]  
**Analyst:** [Your Name]  
**AI Tool:** GitHub Copilot (Claude Sonnet 4.6 via GitHub Copilot CLI)  

---

## A Note on Transparent AI Use

This file is intentionally included in the project repository to demonstrate responsible and transparent use of AI in professional process design work. Every artifact in this project was generated through a structured collaboration between a human analyst and GitHub Copilot: the analyst defined the problem context, specified the required format and content, reviewed all outputs for accuracy and relevance, and made deliberate decisions about what to include, refine, or discard. AI was used as a force multiplier for structured writing and analytical scaffolding — not as a replacement for domain judgment, stakeholder insight, or professional accountability. The prompts below are documented so that reviewers, hiring managers, and collaborators can see exactly how AI-generated content was guided and what human oversight looked like in practice.

---

## Artifact 1: `docs/problem-statement.md`

**Prompt used:**

> "Create a file called docs/problem-statement.md for a process redesign project focused on employee offboarding. Include sections for: Background, Problem Summary, Who Is Affected (stakeholders), Current Pain Points (5-7 bullet points), Scope, and Out of Scope. Write it as if prepared by an AI Process Innovation analyst presenting to a hiring manager at an automotive manufacturing company."

**Human review notes:**
- Verified that the stakeholder table reflected realistic cross-functional ownership at a manufacturing company (HR, IT, Payroll, Legal, Security, Operations).
- Confirmed that the Out of Scope section excluded items genuinely outside a process redesign boundary (e.g., HRIS platform selection, union negotiations).
- Adjusted tone to match a professional analyst audience, not a generic business audience.

---

## Artifact 2: `docs/sipoc.md`

**Prompt used:**

> "Create a file called docs/sipoc.md for an employee offboarding process at a large manufacturing company. Use a markdown table with columns: Supplier | Input | Process Step | Output | Customer. Include 6-8 process steps. After the table, add a 3-sentence 'SIPOC Summary' paragraph."

**Human review notes:**
- Verified that the 8 process steps were logically sequenced and complete end-to-end (intake through post-separation close).
- Confirmed that Supplier and Customer columns reflected realistic organizational actors, not generic labels.
- Reviewed the SIPOC Summary for accuracy and alignment with the problem statement framing.

---

## Artifact 3: `docs/process-maps.md`

**Prompt used:**

> "Create a file called docs/process-maps.md. First section: As-Is Process (describe the current offboarding swimlane in narrative form with steps labeled by actor: Manager, HR, IT, Security, Employee). Second section: Pain Point Analysis (5-7 specific pain points tied to actors). Third section: To-Be Process (same swimlane narrative with automation and AI touchpoints called out clearly). Note where Power Automate, Copilot, and AI classification could help."

**Human review notes:**
- Verified that As-Is pain points were specific and realistic for a large manufacturing environment, not generic HR complaints.
- Reviewed To-Be automation callouts to confirm they were technically plausible within the Microsoft 365 ecosystem.
- Confirmed that the AI classification use case (exit interview NLP) was appropriately scoped and flagged for governance review in the RAID log.
- Ensured the narrative format would be readable as a swimlane substitute for stakeholders who do not have access to Visio or Lucidchart.

---

## Artifact 4: `docs/user-stories.md`

**Prompt used:**

> "Create a file called docs/user-stories.md with 8 user stories and acceptance criteria for the future-state offboarding workflow. Format each as: User Story [number] | As a [actor] | I want [action] | So that [outcome]. Below each story, list 3-4 acceptance criteria as bullet points. Actors include: Manager, HR Coordinator, IT Admin, Security, and New Hire Manager."

**Human review notes:**
- Verified that all 5 actors were represented across the 8 stories and that no actor was over- or under-represented.
- Reviewed acceptance criteria for testability — each criterion was checked to confirm it could be validated in a UAT scenario.
- Confirmed that the New Hire Manager story (Story 8) reflected a realistic use case for backfill planning, not just a variation on the HR Coordinator perspective.

---

## Artifact 5: `docs/raid-log.md`

**Prompt used:**

> "Create a file called docs/raid-log.md with a markdown table RAID log for the offboarding redesign project. Include 4-5 Risks, 3-4 Assumptions, 3-4 Issues, and 3-4 Dependencies. Columns: Category | Item | Description | Owner | Mitigation or Note | Status."

**Human review notes:**
- Verified that risks were specific to the manufacturing context (union CBA, physical access control systems, API integration complexity) rather than generic project risks.
- Confirmed that the blocking issue (no single process owner) was appropriately flagged as a pre-condition for the redesign effort.
- Reviewed dependencies to ensure they were genuinely blocking or sequencing constraints, not just related work items.
- Added status emoji indicators for visual scannability in GitHub markdown rendering.

---

## Artifact 6: `docs/kpi-framework.md`

**Prompt used:**

> "Create a file called docs/kpi-framework.md with a KPI table for the redesigned offboarding process. Include 6-8 KPIs. Columns: KPI Name | What It Measures | Target | Data Source | Review Frequency | Owner. After the table, write a short paragraph on how AI and automation change the measurement story compared to the current state."

**Human review notes:**
- Verified that KPI targets were realistic and defensible — not aspirational vanity metrics.
- Confirmed that each KPI had a clearly defined, automatable data source in the To-Be state.
- Reviewed the closing paragraph to ensure it made a substantive analytical argument about the shift from invisible to measurable processes, not just a generic AI endorsement.

---

## Artifact 7: `prompts/copilot-prompts-used.md` (this file)

**Prompt used:**

> "Create a file called prompts/copilot-prompts-used.md that documents the GitHub Copilot prompts used to build this project. Organize by artifact. Include a short note at the top explaining that this file is intentionally included to demonstrate transparent AI use and show how AI-generated content was guided, reviewed, and refined by a human analyst."

**Human review notes:**
- This file was reviewed to ensure it accurately represents the prompts as submitted and that the human review notes reflect genuine analytical decisions made during the project.
- The transparency note was written to be clear and professional — appropriate for a portfolio or hiring context where the reviewer may be evaluating both AI fluency and professional judgment.

---

*All prompts were submitted through the GitHub Copilot CLI (Agent Showcase environment). Outputs were reviewed, accepted, and organized by the human analyst. No AI-generated content was published without human review.*
