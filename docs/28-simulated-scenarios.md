# Simulated validation scenarios - AegisShield SIEM Core Modernization

> Fictional portfolio evidence. These scenarios use simulated or approved masked data in a non-production environment. They demonstrate how the Project Manager would coordinate validation; they do not claim a real customer deployment.

The scenarios connect the project requirements, GitHub execution records, and the BookEasy pilot decision. Each scenario has an expected result and an evidence owner.

| ID | Scenario | Expected result | Requirement | GitHub record |
|---|---|---|---|---|
| SC-01 | Supported runtime and dependencies | Login, API, regression, and security checks pass on the selected supported versions. | REQ-01 | [Issue #1](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/1) |
| SC-02 | Database migration and restore | Representative records reconcile and the database can be restored in staging. | REQ-02 / REQ-06 | [Issue #2](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/2) |
| SC-03 | Normal BookEasy event delivery | An agreed event reaches the API, database, detection flow, alert path, and analyst dashboard. | REQ-04 | [Issue #3](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/3) |
| SC-04 | Timeout and retry without duplication | A timeout and retry preserve the event ID and produce one processed event. | REQ-03 | [ISS-01 / Issue #9](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/9) |
| SC-05 | Delivery failure monitoring | A simulated connector failure produces an actionable operational alert. | REQ-05 | [Issue #4](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/4) |
| SC-06 | Regression and recovery checks | Login, ingestion, alerts, dashboard behavior, security controls, migration, monitoring, and rollback checks pass. | REQ-04 / REQ-06 / REQ-07 | [Issue #5](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/5) |
| SC-07 | BookEasy pilot acceptance | BookEasy accepts the agreed pilot scenarios and results before production authorization. | REQ-04 | [Issue #6](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/6) |
| SC-08 | Controlled release and handover | The sponsor decision, post-release checks, runbook, monitoring, recovery ownership, and closure evidence are recorded. | REQ-08 | [Issues #7 and #8](https://github.com/evamarquez/aegisshield-bookeasy-pilot/issues/7) |

## Execution checkpoints

- [Week 2 planning board](https://github.com/users/evamarquez/projects/3) - scope, owners, dependencies, and acceptance evidence ready.
- [Week 8 issue board](https://github.com/users/evamarquez/projects/4) - duplicate-event defect found; pilot blocked while the fix is investigated.
- [Week 13 close-out board](https://github.com/users/evamarquez/projects/5) - the correction is accepted, release stabilized, and operations handover completed.

The scenarios are intentionally bounded. Passing them supports the fictional BookEasy pilot and controlled release decision; it does not prove that every possible connector failure, security condition, or customer rollout would succeed.
