# Risk Register and RAID Log

**Baseline:** Week 2 planning baseline  
**Review cadence:** Weekly with risk owners  
**Last reviewed:** January 14, 2026 (simulated)

## Scoring criteria

- **Low probability:** The event is not expected under the current plan.
- **Medium probability:** There is a credible chance it may occur.
- **High probability:** It is likely without additional action.
- **Low impact:** Limited rework or local delay.
- **Medium impact:** Material delay or contained customer effect.
- **High impact:** Release blocker, data-integrity concern, service disruption, or major schedule impact.

## Risk register

| ID | Cause and consequence | Probability / impact | Prevention | Trigger | Contingency | Owner | Status | Last review | Preventive action due |
|---|---|---|---|---|---|---|---|---|---|
| R01 | Version differences may cause library incompatibility, break service behavior, and delay deployment. | Medium / High | Compatibility review and regression testing. | Required library fails on the target runtime. | Keep current version, revise target, and escalate schedule impact. | Engineering lead | Open | Jan 14 | Jan 20 |
| R02 | Incomplete migration preparation may cause missing or inconsistent data and force rollback. | Medium / High | Backup, restore rehearsal, record counts, checksums or agreed integrity checks, and reconciliation. | Counts or integrity checks do not match the agreed data set. | Stop release, restore the prior database, reconcile incoming events, and investigate. | Database engineer | Mitigating | Jan 14 | Jan 21 |
| R03 | Retry timeouts may create duplicate or missing events and block the pilot. | Medium / High | Stable event IDs, duplicate checks, timeout tests, and processing-log review. | A repeated event is processed more than once or is not processed. | Pause pilot approval, correct the connector, replay or reconcile affected events, and retest. | Engineering lead | Open | Jan 14 | Jan 22 |
| R04 | Part-time capacity and competing work may delay testing or decisions. | Medium / Medium | Confirm weekly availability and review conflicts with functional leads. | A planned owner cannot meet a task date. | Re-sequence work, assign backup support, or request a sponsor schedule decision. | PM | Open | Jan 14 | Jan 16 |
| R05 | Inadequate data protection during testing or release may expose customer information. | Low / High | Masked or approved test data, access review, encryption checks, and clean-log review. | Unauthorized access, sensitive data in logs, or failed control check. | Stop the activity, restrict access, notify Security, and follow the incident process. | Security lead | Open | Jan 14 | Jan 23 |

## RAID notes

- **Assumption:** The cross-functional team can provide the planning capacity listed in the schedule.
- **Dependency:** Target compatibility and migration rehearsal must be ready before integrated testing.
- **Action:** QA records the final acceptance checks after leads confirm the pending thresholds and scenarios.
- **Decision:** The sponsor approves any change to baseline scope, schedule, or release conditions.

## Key terms

**Risk:** An uncertain event that could affect the project.  
**Issue:** A risk that has happened or a current problem.  
**Risk owner:** The role accountable for monitoring and responding.  
**Trigger:** A sign that the risk may be occurring.  
**Mitigation:** Action taken to reduce probability or impact.  
**Contingency:** Action taken if the risk occurs.
