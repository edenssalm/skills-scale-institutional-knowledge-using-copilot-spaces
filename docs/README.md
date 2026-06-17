# OctoAcme Project Management Docs

This README consolidates links to the project management process documents and provides an overview of OctoAcme's approach to running projects.

## OctoAcme Project Management Overview

OctoAcme operates on a structured, iterative lifecycle that emphasizes customer value, clear ownership, and data-driven decisions. The project lifecycle spans five key phases: **Initiation** (problem validation and stakeholder alignment via a concise one-pager), **Planning** (breaking work into prioritized backlog items with acceptance criteria and estimates), **Execution** (delivering in small increments with CI/CD rigor), **Release** (deploying with pre-flight checklists and rollback plans), and **Close & Retrospective** (capturing learnings and converting them into actionable improvements). This approach ensures that projects move through gating criteria at each phase—success metrics must be clear, stakeholders must be aligned, and team capacity must be confirmed before proceeding.

**Core roles and responsibilities** are clearly defined to maintain accountability and streamline decision-making. The **Project Manager (PM)** coordinates delivery schedules, manages risks, and maintains stakeholder communications. The **Product Manager (PdM)** defines outcomes, prioritizes the backlog, and measures success against business and customer metrics. **Developers** implement features, collaborate on design, write tests, and help identify technical risks. **QA/Testing** validates acceptance criteria and quality standards. This clear role definition eliminates ambiguity and ensures that each function—product strategy, delivery coordination, technical implementation, and quality assurance—receives focused ownership.

Communication is structured through multiple cadences to keep teams synchronized and risks visible. Daily standups (15 minutes) focus on progress and blockers; weekly syncs between PM and PdM align strategy and prioritization; twice-weekly delivery team standups maintain execution momentum; and monthly stakeholder updates ensure transparency. Risk escalation follows a three-level path: team-level triage in standups, PM escalation to Product Lead and dependent teams, and sponsor-level escalation for business-impacting issues. A risk register is maintained throughout the project with ID, description, impact, likelihood, owner, and mitigation status, reviewed at weekly syncs to ensure early intervention.

Quality and testing are woven throughout execution rather than left to the end. The team uses small pull requests (≤400 lines when possible), requires automated CI checks (tests, linting, security scanning) before review, and mandates at least one approval before merging. Unit tests cover new logic, integration tests validate cross-component flows, and end-to-end smoke tests verify critical paths before release. A Definition of Done is established during planning and applied consistently to all backlog items. Post-release, retrospectives (45–75 minutes) capture what went well, what could improve, and generate 2–3 prioritized action items to avoid overload. This continuous improvement mindset, combined with structured reporting of velocity, burndown, and key success metrics, creates a culture of learning and iterative enhancement.

## Process Documents

- [Project Management Overview](./octoacme-project-management-overview.md) — High-level introduction to OctoAcme's project management approach, core roles, key artifacts, and communication cadence.
- [Project Initiation Guide](./octoacme-project-initiation.md) — Steps to validate business need, align stakeholders, and decide go/no-go for planning.
- [Project Planning](./octoacme-project-planning.md) — Breaking work into shippable increments, identifying dependencies, and creating release plans.
- [Execution & Tracking](./octoacme-execution-and-tracking.md) — Day-to-day execution, sprint workflows, PR practices, quality gates, and progress reporting.
- [Risks & Communication](./octoacme-risks-and-communication.md) — Risk identification and management, stakeholder communication templates, and escalation paths.
- [Release & Deployment](./octoacme-release-and-deployment.md) — Release types, pre-release requirements, deployment checklists, and rollback playbooks.
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md) — Running effective retrospectives and converting learnings into action items.
- [Roles & Personas](./octoacme-roles-and-personas.md) — Detailed descriptions of Developers, Product Managers, and Project Managers in the OctoAcme organization.

## How to Contribute

Use the repository's **"Add Content to Project Management Process Docs"** issue template to propose additions or updates to existing process documents. When submitting:

- Select the process document you want to update (or `<new document>` for new content)
- Provide a clear summary of the new content
- Explain the rationale for the addition
- Include suggested content (optional but helpful)
- Verify that your contribution aligns with existing docs and closes a documented gap

This collaborative approach ensures that OctoAcme's processes remain current, accessible, and reflective of team best practices.
