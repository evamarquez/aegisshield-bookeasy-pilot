# GitHub Board Snapshot 2 - During the Problem

**Project:** Aegis Security Cloud Modernization - BookEasy Pilot  
**Point in time:** End of week 8  
**Board purpose:** Show how the team handled a pilot-blocking defect.

| Pending | In progress | In review | In testing | Blocked | Done |
|---|---|---|---|---|---|
| Confirm revised pilot date | Fix duplicate-event handling | Root-cause review | Validate retry and deduplication | BookEasy pilot approval | Runtime update tested |
| Update customer communication |  | Review integration evidence | Re-run timeout scenarios | Production approval | Database restore rehearsal passed |
| Prepare go/no-go decision |  |  |  |  | Security review completed |
|  |  |  |  |  | Failure alert test passed |

**Issue:** A timeout in the connector created duplicate events during integration testing.  
**Decision:** Pause pilot approval, protect the scope, fix the issue, and move the forecast pilot by one week.  
**Status:** Amber. The risk is visible, owned, and being managed with evidence.

## Week 8 milestone view

| Milestone | Original | Forecast | Status |
|---|---|---|---|
| BookEasy pilot | Week 10 | Week 11 | Pending sponsor approval |
| Production release | Week 11 | Week 12 | Depends on pilot acceptance |
| Handover and closure | Week 12 | Week 13 | Depends on stabilization |

**ISS-01 card:** Owner: Engineering lead. It blocks the pilot until the original event ID is preserved across timeout retries, duplicate processing is prevented, and QA records passing evidence.
