# Improvement Plan for Case 01

## Purpose

This plan improves the technical project management case one document at a time. The goal is to make the case easy to follow, realistic, and strong enough to show how a Technical Project Manager thinks and works.

The case should show a clear chain:

> Sponsor handoff -> project framing -> authorization -> current-state analysis -> prioritization -> delivery plan -> first increment -> release readiness -> portfolio summary

## Important decision before editing

Choose one official case name and use it everywhere.

The current repository uses:

**Aegis Security Cloud Modernization - BookEasy Pilot**

Earlier drafts used different labels for the project. Those names should not stay mixed together.

Recommended choice for this repository:

- Company: AegisShield
- Product: Aegis Security Cloud
- Project: Aegis Security Cloud Modernization - BookEasy Pilot
- BookEasy is the first controlled pilot and stays in the case throughout.

If the project will use a named customer pilot, define it once in the scenario and repeat it consistently in every document.

## Source of truth by tool

Keep each tool focused on one job:

- **GitHub:** the only tool used for this case. It holds the final documents, decisions, diagrams, version history, and three board snapshots.
- **Board snapshot 1:** before the problem, showing the baseline plan.
- **Board snapshot 2:** during the problem, showing the duplicate-event defect, impact, and recovery work.
- **Board snapshot 3:** after the problem, showing the accepted fix, pilot, handover, and closure.

Jira and Monday are not used as separate systems in this portfolio case. Their intended views are represented as GitHub board snapshots so the story stays in one source of truth.

## Tool decision for the portfolio

GitHub Projects is the selected tool for the execution view because it can show the backlog as a table, board, and schedule. The case uses GitHub-style snapshots to show the baseline, the week-8 issue, and the recovery outcome. The snapshots are labeled as simulated portfolio evidence; they are not presented as records from a real client project.

GitLab remains an optional learning alternative. No GitHub or GitLab account, project, or permission is assumed in this case.

## Work sequence

Do not edit every file at once. Complete each step, review it, and then move to the next one.

### Step 0 — Clean the case frame

Update:

- `README.md`
- `00-scenario.md`

Changes:

- Confirm the official company, product, project, and role names.
- Add a short note that the case is fictional and simulated.
- Make the project start with a sponsor handoff rather than an already-approved detailed plan.
- Separate facts received from the sponsor, assumptions, and questions the project manager must validate.
- Keep the initial timeline as a planning assumption, not a promise.

Done when:

- A new reader can explain what the company does, what is wrong, why the project starts now, and what the sponsor is asking for.
- No competing project names remain.

### Step 1 — Improve the Sponsor Handoff

File:

- `00-scenario.md`

Keep these sections:

1. Business context.
2. Current problem.
3. Findings supplied by the sponsor.
4. Sponsor request.
5. Constraints and non-negotiables.
6. Open questions for the project manager.

Improve the sponsor request so it says exactly what the first phase must produce. For example:

> Establish a trustworthy current-state baseline, recommend a risk-based modernization sequence, and coordinate a safe first implementation increment without disrupting customer service.

Do not put the full plan, full backlog, or final acceptance criteria in this document. Those belong later.

Done when:

- The handoff gives enough context to start.
- It does not pretend that unknown facts have already been decided.
- The sponsor, project manager, and technical owners have different responsibilities.

### Step 2 — Improve the Project Brief

File:

- `01-project-brief.md`

Strengthen the objective so it describes the target state, not just the work. Use this structure:

> Modernize the platform by moving critical components toward supported versions, improving integration reliability, and creating a controlled path to release. The result must preserve current customer functions, make risks visible, and include evidence from testing before production approval.

Add or refine:

- Business need.
- Target outcome.
- Main deliverables.
- In scope.
- Out of scope.
- Success measures.
- Assumptions.
- Open questions.

Keep the success measures clearly labeled as fictional targets. Do not present them as real results.

Done when:

- Someone can understand the project in two minutes.
- The objective explains how the service should work after the first increment.
- Scope, outcomes, and deliverables do not contradict each other.

### Step 3 — Add the Project Charter

New file:

- `05-project-charter.md`

The charter is the authorization document. It should include:

- Project purpose.
- Objective.
- High-level scope.
- Main deliverables.
- Initial milestones.
- Success criteria.
- Main risks.
- Assumptions and constraints.
- Sponsor and project manager authority.
- Decision and approval path.
- Simulated approval status and date.

Use a simple authority rule:

- The sponsor approves scope, funding direction, major changes, and production release.
- Technical owners approve technical design and implementation choices.
- Product approves customer and product priorities.
- The Technical Project Manager coordinates the work, tracks decisions, escalates blockers, and maintains the plan.

Done when:

- It is clear who can approve what.
- The project manager has enough authority to coordinate the work.
- The document does not claim the project is complete.

### Step 4 — Improve Stakeholder and Communication Planning

New file:

- `06-stakeholder-register-and-communication-plan.md`

It is fine to keep these together. Use two clear sections.

Stakeholder Register fields:

- Stakeholder or group.
- Role.
- Interest.
- Influence.
- Main concern.
- Decision or input needed.
- Engagement approach.

Communication Plan fields:

- Audience.
- Information needed.
- Owner.
- Channel.
- Frequency.
- Format or artifact.
- Escalation path.

At minimum, include the sponsor, Product, Engineering, Security, DevOps or SRE, QA, Support, Customer Success, Compliance or Legal, and pilot customer representatives if a pilot is used.

Done when:

- Every major stakeholder has a reason to be involved.
- Every recurring communication has an owner and purpose.
- The plan explains how bad news and blockers are escalated.

### Step 5 — Define the current state before proposing solutions

New files:

- `07-current-state-inventory.md`
- `08-dependency-and-integration-map.md`

The inventory should include:

- Component or service.
- Purpose.
- Owner.
- Runtime or version.
- Data handled.
- Customer impact.
- Current support status.
- Known issue.
- Evidence source.
- Confidence level.

The dependency and integration map should show:

- System A.
- System B.
- Data or event exchanged.
- Direction.
- Auth method.
- Failure mode.
- Monitoring.
- Rollback or recovery option.

Do not invent detailed technology facts. If the case does not define a fact, label it as an assumption or open question.

Done when:

- Every critical component has an owner.
- Every customer-facing integration has a risk or confidence note.
- The modernization priorities can be traced to evidence.

### Step 6 — Prioritize risk and decisions

New files:

- `09-risk-register-and-raid-log.md`
- `10-modernization-decision-matrix.md`
- `11-decision-log.md`

Risk Register fields:

- Risk ID.
- Description.
- Cause.
- Impact.
- Probability.
- Severity.
- Score.
- Owner.
- Mitigation.
- Trigger.
- Due date.
- Status.

Decision Matrix options:

- Upgrade.
- Replace.
- Retire.
- Monitor.
- Investigate.

Decision criteria should include security risk, customer impact, support status, effort, dependency risk, rollback difficulty, and business value.

Decision Log fields:

- Decision ID.
- Date.
- Decision.
- Options considered.
- Reason.
- Owner.
- Approver.
- Impact on scope, time, cost, or risk.

Done when:

- The first increment is chosen because of evidence.
- The case shows what was not chosen and why.
- Risks have owners and actions, not just descriptions.

### Step 7 — Build the delivery plan

New files:

- `12-work-breakdown-and-roadmap.md`
- `13-milestone-and-dependency-plan.md`

Recommended work breakdown:

1. Baseline and inventory.
2. Risk and dependency assessment.
3. First increment design.
4. Environment and test preparation.
5. Implementation.
6. Integration validation.
7. User or customer validation.
8. Release readiness.
9. Controlled rollout.
10. Handoff and lessons learned.

For each work package, define:

- Owner.
- Start and finish assumption.
- Inputs.
- Deliverable.
- Dependency.
- Acceptance condition.
- Risk.

Done when:

- The plan shows how work moves from discovery to release.
- Dependencies are visible.
- The timeline is connected to deliverables, not just dates.

### Step 8 — Define testing and release readiness

New files:

- `14-test-and-acceptance-plan.md`
- `15-release-readiness-and-rollback-plan.md`

Testing should cover:

- Existing core functions.
- Authentication and authorization.
- Event ingestion.
- Customer-facing integrations.
- Duplicate or retry behavior.
- Dashboards and alerts.
- Data integrity.
- Monitoring and audit evidence.

Acceptance criteria should be testable. Each one needs:

- Given condition.
- Action.
- Expected result.
- Evidence.
- Approver.

Release readiness should include:

- Test results.
- Known issues.
- Monitoring in place.
- Backup confirmed.
- Rollback steps tested or reviewed.
- Support and customer communication ready.
- Approval recorded.

Done when:

- The case shows how the team knows the release is safe.
- Rollback is treated as part of the release, not an afterthought.

### Step 9 — Create a leadership status update

New file:

- `16-leadership-status-update.md`

Use a one-page format:

- Overall status.
- Completed this period.
- Next period.
- Top risks.
- Blockers.
- Decisions needed.
- Timeline or scope change.
- Help requested from leadership.

Done when:

- An executive can understand the state of the project without reading every artifact.

### Step 10 — Prepare the portfolio version

Update:

- `README.md`
- Website case study page.

The portfolio summary should show:

- Problem.
- Role.
- Approach.
- Key artifacts.
- Simulated outcome.
- What the case demonstrates.

Keep the full documents in GitHub and show only the most useful artifacts on the website.

## GitHub setup step by step

Use GitHub as the document and evidence hub.

1. Create a repository with a clear name such as `aegisshield-platform-modernization-case`.
2. Create these folders:
   - `docs/01-initiation`
   - `docs/02-current-state`
   - `docs/03-planning`
   - `docs/04-delivery`
   - `docs/05-release`
   - `diagrams/`
3. Move the current Markdown files into the matching folders, or keep the current flat structure until the case is stable. Do not reorganize and rewrite at the same time.
4. Add a root `README.md` with the case summary, document map, fictional-project note, and current status.
5. Add a `CHANGELOG.md` that records major updates to the case.
6. Add labels such as `initiation`, `scope`, `risk`, `decision`, `release`, `documentation`, and `portfolio`.
7. Create one GitHub Issue for each planned artifact. Use the issue title format: `[Case 01] Improve Project Charter`.
8. Add acceptance criteria to each issue. Example: `The charter names the sponsor, authority, milestones, risks, and approval status.`
9. Create a branch for each meaningful document batch, such as `case01/charter-and-stakeholders`.
10. Commit in small groups with clear messages, such as `docs(case01): add project charter draft`.
11. Open a pull request for each completed batch. In the description, include what changed, what remains open, and how the document was checked.
12. Use GitHub Issues for questions and decisions that need a written record.
13. Tag the stable version when the case is ready for the portfolio, for example `case-01-v1`.
14. Link the public case website back to the stable README and selected documents.

## GitHub board snapshots

Jira and Monday are not used in this case. To show the same project-control thinking without creating duplicate tools, use three GitHub-style board snapshots:

1. `github-board-before.md` - baseline plan before the integration problem.
2. `github-board-during.md` - the duplicate-event defect, impact, owner, and recovery work.
3. `github-board-after.md` - accepted fix, pilot, release, handover, and closure.

Each snapshot should show the columns `To do`, `In progress`, and `Done`, plus the point in time, status, issue or decision, and the next action. These are portfolio evidence views, not claims that a live customer board existed.

## Review checkpoints

After each phase, check:

- Is the purpose of the document clear?
- Does it use the official project name?
- Does it separate facts, assumptions, decisions, and open questions?
- Does every action have an owner?
- Can a reader trace the plan back to a business or technical problem?
- Is the result labeled as simulated rather than real client work?

## Definition of done for the full case

The case is ready for the portfolio when:

- The documents follow one consistent story.
- The sponsor handoff leads logically to the charter and plan.
- The current-state evidence supports the risks and priorities.
- The first increment has scope, owner, milestones, acceptance criteria, tests, rollback, and approval steps.
- The GitHub repository is easy to navigate.
- The three GitHub board snapshots show how status changed before, during, and after the issue.
- The README clearly explains what the case demonstrates and what is fictional.
