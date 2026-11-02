# Modernization Decision Matrix and Decision Log

## Decision matrix

| Area | Option | Reason | Decision |
|---|---|---|---|
| Runtime | Upgrade | Reduces support and security risk while preserving the service | Upgrade selected components |
| Database | Upgrade with rehearsal | Improves supportability but needs recovery evidence | Proceed with controlled migration |
| BookEasy connector | Improve | The current flow works but needs retry and duplicate protection | Improve in this increment |
| Dashboard and detections | Monitor | Existing behavior must be preserved; redesign is out of scope | Do not redesign now |
| Other customer connectors | Investigate later | No evidence supports expanding the pilot now | Keep outside scope |

## Decision log

| ID | Decision | Owner | Timing | Rationale |
|---|---|---|---|---|
| DEC-01 | Move the pilot by one week | Sponsor | Week 9 | Protect acceptance criteria after the duplicate-event defect |
| DEC-02 | Keep BookEasy as the only pilot | Sponsor and Product | Week 2 | Limit customer and delivery risk |
| DEC-03 | Require restore evidence before release | Database and Sponsor | Week 4 | Protect data recovery and release confidence |
| DEC-04 | Use GitHub board snapshots as execution evidence | PM | Portfolio preparation | Keep one source of truth instead of duplicating Jira and Monday |
