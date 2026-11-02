# Risk Register and RAID Log

| ID | Risk or issue | Probability | Impact | Owner | Response | Status |
|---|---|---:|---:|---|---|---|
| R01 | Runtime update causes regression in core functions | Medium | High | Engineering | Test login, ingestion, alerts, and dashboard before pilot | Open |
| R02 | Database migration cannot be restored in the change window | Low | Critical | Database Engineering | Rehearse restore and reconcile records before release | Mitigating |
| R03 | Connector timeout creates duplicate events | Medium | High | Backend Engineering | Use stable event IDs, deduplication, and timeout tests | Occurred; controlled |
| R04 | Pilot scenarios or customer reviewers are not ready | Medium | Medium | Customer Success | Agree scenarios and review date early | Open |
| R05 | Release failure affects customer service | Low | Critical | DevOps / SRE | Approved window, monitoring, rollback, and escalation path | Mitigating |

## Issue record

**ISS-01:** During week 8 integration testing, a connector timeout created duplicate events. The PM paused pilot approval, coordinated root-cause review, tracked the fix and retest, and escalated the schedule impact. The sponsor approved a one-week shift.

## RAID actions

- **Assumption:** Team capacity is available for the fictional 13-week plan.
- **Dependency:** BookEasy test scenarios must be agreed before acceptance testing.
- **Action:** Complete stable-ID and timeout tests before pilot approval.
- **Decision needed:** Sponsor go/no-go after evidence review.
