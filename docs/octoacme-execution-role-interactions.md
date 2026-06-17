# OctoAcme — Execution Phase: Role Interactions & Handoffs

## Purpose
Provide a detailed reference for how roles coordinate and hand off work during the execution phase, reducing ambiguity and accelerating issue resolution.

## Overview
Execution is the longest phase of the project lifecycle. Success depends on clear role responsibilities, well-defined handoffs, and proactive communication. This document maps typical interactions and gates.

---

## Daily Execution Flow

### Morning: Daily Standup (15 min)

**Participants**: Developers, QA Lead, Delivery Manager, Project Manager (as needed)

**Flow**:
1. Each developer shares: (1) What I completed yesterday, (2) What I'm working on today, (3) Blockers or risks
2. QA Lead updates on test execution status and any blockers
3. Delivery Manager flags dependencies, escalations, and asks clarifying questions
4. Blockers are immediately triaged and assigned to an owner for same-day resolution

**Owner**: Delivery Manager (facilitates) + Project Manager (escalates if needed)

**Output**: Updated project board, blocker list, and escalation flag if needed

---

### Mid-Week: Development Sync (30 min)

**Participants**: Developers, Engineering Lead, Product Manager, QA Lead

**Topics**:
- Code review status and PR backlog
- Any acceptance criteria clarifications needed
- Technical design decisions or blockers
- Test readiness and coverage

**Owner**: Engineering Lead (facilitates)

**Output**: Cleared acceptance criteria questions, updated test plan, design decisions documented

---

### Weekly: Delivery Sync (1 hr)

**Participants**: Project Manager, Product Manager, Delivery Manager, Engineering Lead, QA Lead, Release Manager (if feature near completion)

**Topics**:
- Overall progress toward milestone (% complete)
- Velocity vs. planned pace
- Risks and mitigation plans
- Dependency status
- Upcoming work readiness

**Owner**: Project Manager (facilitates) + Product Manager (provides priority decisions)

**Output**: Status update for stakeholders, escalations logged in risk register, priority decisions documented

---

## Work Transition Points (Gates)

### Gate 1: "Ready" → "In Progress"

**When**: Developer picks up a story from the backlog

**Criteria**:
- ✅ Story has been refined (acceptance criteria clear)
- ✅ Dependencies identified and clear path forward
- ✅ Design review completed (if applicable)
- ✅ Developer has asked clarification questions

**Owner**: Developer (confirms readiness) + Product Manager (clarifies acceptance criteria)

**If blocked**: Flag in standup immediately; Delivery Manager escalates

---

### Gate 2: "In Progress" → "In Review" (Pull Request)

**When**: Developer opens a PR

**Criteria**:
- ✅ All automated tests passing
- ✅ Code linting passes
- ✅ PR description includes: (1) Issue link, (2) Acceptance criteria summary, (3) Test results, (4) Any breaking changes
- ✅ Self-review completed; developer notes any concerns

**Owner**: Developer

**Review Process**:
1. Code review from peer (24-hour SLA for first comment)
2. Address feedback; iterate until approved
3. Merge only after approval + passing CI

**If blocked**: Unclear feedback or missing context → Deliver Manager flags; Engineering Lead clarifies

---

### Gate 3: "In Review" → "QA" (Ready for Testing)

**When**: PR merged to main branch; code deployed to QA environment

**Criteria**:
- ✅ PR merged and tests passing in CI
- ✅ Feature deployed to QA environment
- ✅ QA Lead has reproduction steps or user story
- ✅ Acceptance criteria clearly linked in QA task

**Owner**: Developer (merge) + DevOps Engineer (deploy to QA)

**QA Lead Actions**:
1. Verify acceptance criteria against feature
2. Test on agreed-upon browsers/devices
3. Log any defects or gaps
4. Communicate status daily to team

**If issues found**: Developer is notified same day; fixes prioritized based on severity

---

### Gate 4: "QA" → "Release Ready" (Release Gating)

**When**: QA Lead confirms all acceptance criteria met

**Criteria**:
- ✅ All acceptance criteria verified and signed off by QA Lead
- ✅ Security Reviewer has approved (security scan + review)
- ✅ No open critical or high-severity defects
- ✅ Known issues are documented with workarounds
- ✅ Documentation Owner confirms user guides and runbooks are updated

**Approvals Required**:
1. QA Lead (functional acceptance)
2. Security Reviewer (security sign-off)
3. Engineering Lead (technical sign-off)
4. Release Manager (release readiness)

**If issues**: Defect severity assessed; critical issues block release; non-critical issues tracked for next release

---

## Role Responsibilities During Execution

### Developers

**Daily Activities**:
- Pick up work from "Ready" column
- Write code and tests
- Request peer review via PR
- Address code review feedback
- Investigate QA defects and provide fixes

**Weekly Sync Input**:
- Report progress percentage
- Surface technical blockers or risks
- Identify dependency conflicts early

**Release Readiness**:
- Ensure test coverage meets team standard (e.g., 80%+)
- Validate fixes for QA-found defects
- Participate in release day support if needed

---

### QA Lead

**Daily Activities**:
- Monitor QA environment for new deployments
- Execute test cases against acceptance criteria
- Log defects in issue tracking system
- Communicate test status to team in standup

**Mid-Phase**:
- Plan test strategy for current sprint/milestone
- Coordinate with Developers on testability
- Prepare test data and environments

**Pre-Release**:
- Complete acceptance criteria verification
- Perform smoke tests on release candidate
- Sign off on release readiness

---

### Delivery Manager

**Daily Activities**:
- Facilitate standup and triage blockers
- Monitor project board for progress
- Remove administrative or coordination blockers
- Escalate resource or dependency issues

**Weekly**:
- Prepare delivery metrics (velocity, % complete)
- Provide Stakeholder Liaison with status update
- Identify risks to timeline and escalate

**Pre-Release**:
- Confirm all teams are ready
- Create release day coordination schedule

---

### Engineering Lead

**Daily Activities**:
- Available for design questions and technical decisions
- Review complex code changes or architecture questions
- Triage technical blockers

**Mid-Week**:
- Facilitate development sync
- Ensure design quality and consistency
- Sign off on complex PRs

**Pre-Release**:
- Ensure code quality standards are met
- Approve technical readiness for release

---

### Product Manager

**Daily Activities**:
- Be available for acceptance criteria clarifications
- Respond to priority conflict questions
- Engage in discussions about feature trade-offs

**Weekly**:
- Participate in delivery sync
- Update roadmap if priorities change
- Share stakeholder feedback with team

**Pre-Release**:
- Approve release messaging and communication
- Be available during release for customer questions

---

### Release Manager

**Entering Execution Phase**:
- Understand feature scope and release plan
- Identify dependencies with other projects

**Mid-Phase**:
- Track feature status and readiness
- Begin release planning when features enter "QA"

**Pre-Release**:
- Coordinate final readiness review
- Prepare release checklist and runbooks
- Schedule release day activities
- Gate release with approval from QA, Security, Eng Lead

---

### Security Reviewer

**Early Phase**:
- Participate in design review (if sensitive features)
- Advise on security test cases

**Mid-Phase**:
- Review security scanning results from CI
- Audit code changes for security issues

**Pre-Release**:
- Provide security sign-off before release
- Document any security-related release notes

---

## Escalation Playbook

### Blocker lasting > 1 day

**Level 1**: Delivery Manager triages in standup and assigns owner

**Level 2** (if unresolved after 1 day): Escalate to Project Manager
- Project Manager convenes cross-functional sync
- Brings in SME or Engineering Lead
- Makes priority/resource decisions

**Level 3** (if timeline at risk): Escalate to Sponsor or VP Engineering
- Scope or timeline trade-off decisions
- Resource reallocation
- Stakeholder communication

---

### Quality Issue

**Critical defect** (blocks release):
- QA Lead immediately notifies Developer and Engineering Lead
- Developer prioritizes fix; escalated to next standup
- Re-testing done same day or next day

**High-severity defect** (degrades feature):
- Assessed in daily standup
- Developer and QA prioritize fix
- May delay release by 1-2 days

**Medium/low-severity defect** (workaround available):
- Documented and tracked
- Fixed in next release or maintenance window
- Does not block current release

---

### Resource Conflict

**Example**: Shared resource needed by two features

**Resolution**:
1. Identify conflict in standup
2. Delivery Manager escalates to Project Manager + Product Manager
3. Product Manager makes priority call (which feature is higher priority)
4. Resource reallocated; other feature timeline adjusted
5. Stakeholder Liaison notified of change

---

## Communication Standards

### Status Updates
- **Daily**: Standup (verbal, async note in Slack/Teams if remote)
- **Weekly**: Delivery Sync (30-60 min, recorded)
- **Weekly**: Stakeholder update (written summary via email or dashboard)
- **Ad-hoc**: Escalation notifications (Slack/Teams + email)

### Decision Logging
- All priority decisions logged in a decision log (linked from project board)
- Rationale and alternatives captured
- Owner and date recorded

### Risk Communication
- Risk register reviewed weekly
- New risks added with mitigation plan
- Escalated risks notified to stakeholders within 24 hours

---

## Tools & Artifacts

- **Project Board**: GitHub Projects with columns (Backlog, Ready, In Progress, In Review, QA, Done)
- **Issue Tracking**: GitHub Issues for bugs and tasks
- **PR Workflow**: GitHub PRs with CI checks and review policy
- **Communication**: Slack/Teams for daily coordination, email for formal updates
- **Documentation**: Linked in issues or GitHub wiki

---

## Success Metrics

- **On-Time Delivery**: % of milestones delivered on schedule
- **Blocker Resolution Time**: Avg hours to resolution
- **Cycle Time**: Avg days from Ready → Done
- **Test Coverage**: % of code with automated tests
- **Defect Escape Rate**: Defects found in production vs. during QA
- **Team Velocity**: Story points completed per sprint
