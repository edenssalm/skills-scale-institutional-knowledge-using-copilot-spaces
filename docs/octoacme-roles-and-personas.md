# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Core Roles

### Developers

#### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

#### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

#### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

#### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

### Product Managers

#### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

#### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

#### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

#### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

### Project Managers

#### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

#### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

#### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

#### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Extended Roles & Cross-Functional Personas

These personas represent operational and cross-functional roles that frequently influence delivery, release, quality, and stakeholder communication. They clarify decision rights, handoffs, and accountability across the project lifecycle.

### Delivery Manager

#### Role Summary
Delivery Manager oversees delivery timelines and cross-team coordination, removes blockers, and tracks milestones and delivery risks. Acts as the day-to-day execution partner to the Project Manager.

#### Responsibilities
- Monitor and enforce delivery timelines and sprint velocity
- Identify and escalate blockers and dependencies
- Facilitate daily standups and remove impediments
- Track milestones and alert stakeholders to risks early
- Coordinate handoffs between teams and workstreams

#### Goals
- Maintain predictable, on-time delivery
- Reduce blocked time and unplanned delays
- Keep teams aligned and responsive to priority changes

#### Interactions with Other Roles
- **Works closely with**: Project Manager (joint ownership of timeline), Engineering Lead (blockers), Product Manager (priority conflicts), Release Manager (handoff to release phase)
- **Reports to**: Project Manager or Program Lead

#### Typical Communication
- Daily standups and blocker triage
- Weekly delivery sync with all workstreams
- Escalations to Project Manager for policy or resource issues

---

### Product Operations Lead

#### Role Summary
Product Operations Lead manages product rollout processes, feature flagging coordination, release analytics, and post-launch monitoring readiness. Ensures smooth transitions from development to production.

#### Responsibilities
- Coordinate feature flag rollout strategy and phased deployments
- Track release analytics and monitor early adoption signals
- Prepare monitoring dashboards and runbooks for launch
- Manage customer communication and rollout sequencing
- Coordinate with support and customer success on known issues and workarounds

#### Goals
- Enable fast, low-risk feature rollouts
- Reduce time-to-value and customer impact from issues
- Provide data-driven insights on feature adoption and usage

#### Interactions with Other Roles
- **Works closely with**: Product Manager (rollout sequencing), Release Manager (gating decisions), Data/Analytics Lead (telemetry setup), DevOps Engineer (deployment infrastructure)
- **Reports to**: Product Manager or VP Product

#### Typical Communication
- Pre-release planning with Product and Release teams
- Analytics briefings and adoption reports
- Post-launch retrospectives

---

### Release Manager

#### Role Summary
Release Manager owns the end-to-end release process, including planning, cutover checklists, rollback procedures, and release communications. Ensures releases are safe, documented, and communicated clearly.

#### Responsibilities
- Create and maintain release checklists and runbooks
- Plan cutover activities, timing, and rollback procedures
- Coordinate release communications to stakeholders and customers
- Gate releases with sign-offs from QA, Security, and Operations
- Execute or oversee release day activities and post-release verification

#### Goals
- Execute predictable, low-risk releases
- Minimize customer-facing incidents and rollbacks
- Maintain clear audit trail of release decisions and approvals

#### Interactions with Other Roles
- **Works closely with**: Engineering Lead (release readiness), QA Lead (test sign-off), DevOps Engineer (deployment execution), Stakeholder Liaison (customer communication), Security Reviewer (security approval)
- **Reports to**: VP Engineering or Release Engineering Lead

#### Typical Communication
- Release planning meetings and kick-off
- Daily release coordination calls during cutover window
- Post-release verification and incident response

---

### QA Lead / Test Coordinator

#### Role Summary
QA Lead defines testing strategy, acceptance criteria, and test execution schedules. Validates release readiness and gates the release to production.

#### Responsibilities
- Define testing strategy (unit, integration, end-to-end, smoke tests)
- Create and maintain acceptance criteria checklists
- Coordinate manual and automated test execution
- Sign off on release readiness and identify blockers
- Track and triage bug reports and quality regressions

#### Goals
- Ensure high-quality releases that meet acceptance criteria
- Reduce production defects and customer escalations
- Enable fast feedback cycles to development

#### Interactions with Other Roles
- **Works closely with**: Developers (test feedback), Product Manager (acceptance criteria), Release Manager (release gating), Engineering Lead (test infrastructure)
- **Reports to**: QA Manager or VP Quality Assurance

#### Typical Communication
- Test planning sessions with Product and Engineering
- Daily test status updates during execution
- Release gate sign-offs and defect reviews

---

### Stakeholder Liaison

#### Role Summary
Stakeholder Liaison serves as the single point of contact for external stakeholders, sponsors, and customers. Translates stakeholder requirements into acceptance criteria and manages expectations through clear, timely communications.

#### Responsibilities
- Gather and prioritize stakeholder feedback and requirements
- Translate stakeholder needs into acceptance criteria and user stories
- Provide regular stakeholder updates on progress and timeline
- Manage expectations through transparent risk and issue communication
- Facilitate steering committee and sponsor alignment meetings

#### Goals
- Maintain strong stakeholder alignment and satisfaction
- Reduce scope creep and miscommunication-driven delays
- Ensure project outcomes meet stakeholder expectations

#### Interactions with Other Roles
- **Works closely with**: Project Manager (project status and risks), Product Manager (roadmap and roadmap changes), Release Manager (launch readiness and communications)
- **Reports to**: Project Manager or Sponsor

#### Typical Communication
- Weekly/bi-weekly stakeholder updates
- Monthly steering committee meetings
- Ad-hoc escalation communications

---

### Implementation Engineer / Integration Specialist

#### Role Summary
Implementation Engineer owns integration tasks, deployment scripts, and environment setup for complex integrations. Ensures systems and services are correctly wired and operational.

#### Responsibilities
- Develop and test integration scripts and connectors
- Set up staging and production environments
- Document deployment procedures and runbooks
- Coordinate integration testing with QA and Developers
- Troubleshoot integration issues during and after deployment

#### Goals
- Deliver reliable, well-documented integrations
- Reduce integration-related deployment delays and incidents
- Enable fast, repeatable deployments across environments

#### Interactions with Other Roles
- **Works closely with**: DevOps Engineer (infrastructure and deployment), Developers (API contracts and testing), Release Manager (deployment execution)
- **Reports to**: Engineering Lead or Infrastructure Lead

#### Typical Communication
- Integration planning and design reviews
- Runbook reviews with Release and DevOps teams
- Deployment day coordination

---

### Process Steward

#### Role Summary
Process Steward maintains process documentation, facilitates retrospectives focused on process improvements, and enforces process hygiene. Ensures the team continuously improves how work gets done.

#### Responsibilities
- Maintain and update process documentation and playbooks
- Facilitate retrospectives and process improvement discussions
- Track and follow up on process improvement action items
- Identify and remove process bottlenecks
- Ensure compliance with defined processes (e.g., review gates, sign-offs)

#### Goals
- Reduce friction and improve consistency in project execution
- Enable the team to continuously improve their ways of working
- Build a learning culture focused on sustainable delivery

#### Interactions with Other Roles
- **Works closely with**: Project Manager (process issues), Scrum Master (if applicable), all team leads (process feedback and implementation)
- **Reports to**: Project Manager or PMO

#### Typical Communication
- Retrospective facilitation and synthesis
- Process documentation updates shared with team
- Quarterly process effectiveness reviews

---

### DevOps Engineer / SRE (Site Reliability Engineer)

#### Role Summary
DevOps Engineer owns CI/CD pipelines, production monitoring, observability, and runbooks. Ensures systems are reliable, observable, and can be rapidly and safely deployed.

#### Responsibilities
- Build and maintain CI/CD pipelines and infrastructure-as-code
- Configure production monitoring, alerting, and observability
- Develop and maintain runbooks for common operational tasks
- Perform capacity planning and performance tuning
- Respond to and resolve production incidents

#### Goals
- Enable fast, safe deployments with high confidence
- Maintain high system reliability and uptime
- Reduce mean-time-to-recovery for incidents

#### Interactions with Other Roles
- **Works closely with**: Release Manager (deployment execution and gating), Implementation Engineer (integration and deployment), Developers (observability and performance feedback)
- **Reports to**: VP Engineering or Infrastructure Lead

#### Typical Communication
- Deployment day coordination
- Incident response and retrospectives
- Infrastructure planning and capacity reviews

---

### Documentation Owner

#### Role Summary
Documentation Owner ensures user-facing and operational documentation (runbooks, user guides, FAQs) are updated as part of the release definition of done. Maintains a single source of truth for product and operational guidance.

#### Responsibilities
- Maintain user-facing documentation and help articles
- Create and update runbooks for operational tasks
- Coordinate documentation reviews with Subject Matter Experts (SMEs)
- Version and archive documentation for previous releases
- Gather user feedback on documentation clarity and completeness

#### Goals
- Reduce support volume through clear, discoverable documentation
- Enable self-service for users and operators
- Accelerate onboarding of new users and support staff

#### Interactions with Other Roles
- **Works closely with**: Product Manager (user guides and FAQs), Engineering and Operations teams (runbooks and technical docs), Release Manager (documentation gating for releases)
- **Reports to**: Product Manager, Engineering Lead, or Documentation Lead

#### Typical Communication
- Documentation planning during feature definition
- Content reviews with SMEs
- Post-release documentation verification

---

### Security Reviewer / Threat Assessor

#### Role Summary
Security Reviewer performs security reviews, threat modeling, and ensures security sign-off before release. Protects the organization and customers from security risks.

#### Responsibilities
- Conduct threat modeling and security design reviews
- Perform code and architecture security reviews
- Review security test results and penetration test findings
- Gate releases with security sign-off
- Ensure compliance with security policies and standards

#### Goals
- Identify and mitigate security risks before release
- Maintain customer trust and regulatory compliance
- Build a security-aware engineering culture

#### Interactions with Other Roles
- **Works closely with**: Engineering Lead (security architecture), Developers (code review feedback), Release Manager (release gating), Product Manager (security-driven feature decisions)
- **Reports to**: Chief Security Officer or VP Security

#### Typical Communication
- Security design reviews during planning
- Code review feedback and security briefings
- Release gate sign-offs and security retrospectives

---

## Role Interaction Map: Key Handoffs and Gates

This matrix shows critical interactions and gates where roles must coordinate:

| Phase | From → To | Gate / Coordination |
|-------|-----------|-------------------|
| Planning | Product Manager → Project Manager | Scope and resource sign-off |
| Planning | Product Manager → Engineering Lead | Acceptance criteria and design |
| Execution | Developers → QA Lead | Testing is ready; acceptance criteria clear |
| Execution | Engineering Lead → Release Manager | Feature is complete and tested |
| Release | QA Lead → Release Manager | Test sign-off (all criteria met) |
| Release | Security Reviewer → Release Manager | Security sign-off |
| Release | Release Manager → DevOps Engineer | Deployment approval |
| Release | DevOps Engineer → Release Manager | Production verification complete |
| Stakeholders | Release Manager → Stakeholder Liaison | Launch communication approval |
| Post-Release | All Leads → Process Steward | Retrospective input for continuous improvement |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Refer to the Role Interaction Map when designing release coordination or planning workshops.
- When identifying process gaps, map them to specific personas to clarify accountability.
