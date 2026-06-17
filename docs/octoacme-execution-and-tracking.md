# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Role-Specific Execution Responsibilities

### Developers
- Provide accurate estimates and flag risks early
- Complete work to "Definition of Done" before marking ready for QA
- Participate in code review and respond to feedback promptly
- Maintain test coverage above team-defined thresholds

### QA Lead
- Coordinate test execution and validate against acceptance criteria
- Flag any gaps between feature and acceptance criteria
- Provide daily test status during execution phase
- Gate progress to release phase with formal sign-off

### Delivery Manager
- Monitor daily progress and identify at-risk work
- Surface blockers in standup for immediate triage
- Escalate resource or dependency issues to Project Manager
- Provide visibility into remaining work to Stakeholder Liaison

### Product Manager
- Be available for question clarification and scope decisions
- Provide priority guidance when conflicts arise
- Participate in demos and validate feature delivery
- Update stakeholders on progress and changes

### Release Manager
- Ensure release planning begins when feature enters "In Review" phase
- Prepare cutover checklist and rollback procedures
- Coordinate final readiness review with all teams

## Execution Checklist

### Pre-Execution (Sprint/Milestone Planning)
- [ ] Acceptance criteria defined and shared with team
- [ ] Estimates reviewed and velocity baselined
- [ ] Blockers and dependencies identified
- [ ] Definition of Done documented and team-aligned

### During Execution (Daily/Weekly)
- [ ] Daily standups held; blockers surfaced and triaged
- [ ] PR review SLA maintained (24 hours or team-defined)
- [ ] Test execution on schedule; no quality regressions
- [ ] Risk register updated weekly
- [ ] Stakeholder updates shared (weekly or as needed)

### Pre-Release Gate (Ready to Release)
- [ ] All acceptance criteria met and verified by QA
- [ ] Developers sign off on code quality and test coverage
- [ ] Release Manager confirms release checklist preparation
- [ ] Security Reviewer provides security sign-off
- [ ] Documentation Owner confirms runbooks and user guides are ready
- [ ] DevOps Engineer confirms deployment infrastructure is ready
- [ ] Stakeholder Liaison confirms customer communication is prepared

## Dependency & Handoff Coordination

### Developer → QA Lead Handoff
**When**: Feature enters "In Review" column on project board
**Handoff Criteria**:
- Code reviewed and approved
- All automated tests passing
- PR description includes acceptance criteria link
- Clear reproduction steps for manual testing

**QA Responsibilities**:
- Verify feature meets all acceptance criteria
- Test on multiple browsers/devices if applicable
- Identify any edge cases or gaps
- Provide feedback loop to developers for fixes

### QA Lead → Release Manager Handoff
**When**: Feature enters "QA" column and passes all acceptance criteria
**Handoff Criteria**:
- Test report with results linked in release checklist
- All acceptance criteria checkboxes completed
- Any known issues or workarounds documented
- Performance and security scan results reviewed

**Release Manager Responsibilities**:
- Finalize cutover plan and rollback procedures
- Coordinate with DevOps on deployment sequence
- Prepare customer communication
- Schedule release verification activities

### Release Manager → DevOps Engineer Handoff
**When**: Release day or pre-approved deployment window
**Handoff Criteria**:
- Release checklist completed and signed off
- Runbooks reviewed and tested
- Rollback procedures validated
- Monitoring and alerts configured

**DevOps Responsibilities**:
- Execute deployment per approved runbook
- Monitor system health during and post-deployment
- Execute smoke tests and verification checklist
- Be ready to execute rollback if critical issues detected

## Communication Cadence During Execution

| Frequency | Participants | Topics |
|-----------|--------------|--------|
| Daily | Developers, QA, Delivery Manager | Progress, blockers, dependencies, test status |
| Weekly | PM, Project Manager, Delivery Manager, Leads | Progress, risks, metrics, scope changes |
| Weekly | Release Manager, Product Manager, Security Reviewer | Release readiness and planning |
| As-needed | All teams | Escalations, blocker triage, priority conflicts |

## Metrics to Track

- **Velocity**: Completed story points per sprint
- **Cycle Time**: Days from "Ready" to "Done"
- **Blocker Duration**: Days to resolution
- **Test Coverage**: % of code covered by automated tests
- **PR Review Time**: Hours from submission to first review
- **Release Success Rate**: % of deployments without rollback

## When to Escalate

### To Project Manager
- Blockers lasting > 1 day
- Resource conflicts
- Scope changes or trade-off decisions needed
- Milestone or timeline at risk

### To Product Manager
- Acceptance criteria ambiguity
- Trade-off decisions between features
- Customer impact or priority conflicts

### To VP Engineering / Sponsor
- Project at risk of missing major milestone
- Critical quality or security issues
- Significant resource constraints
