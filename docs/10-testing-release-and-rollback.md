# Testing, Release, and Rollback Plan

## Test gates

| Gate | Evidence required | Owner |
|---|---|---|
| Functional | Login, ingestion, alerts, dashboard, retry, and duplicate tests pass | QA |
| Security | Access and security control checks pass | Security |
| Recovery | Backup, restore, reconciliation, and rollback rehearsal pass | Database / DevOps |
| Customer pilot | BookEasy accepts agreed scenarios and results | Customer Success / BookEasy |
| Release readiness | No critical blocker, owners ready, monitoring active, sponsor decision recorded | PM / Sponsor |

## Test environment and data

Testing uses a non-production environment that matches the proposed runtime, application dependencies, and database path. The team uses synthetic or approved masked BookEasy events. Test data must include normal events, retries, simulated timeouts, duplicate attempts, alerts, dashboard results, migration records, and recovery records.

## Approval scenarios and evidence

QA records the test case, expected result, actual result, owner, date, and evidence link. A gate passes only when all agreed scenarios pass or an accepted exception is documented. Security owns security and data-protection evidence; Database owns migration and restore evidence; DevOps owns monitoring and rollback evidence; BookEasy confirms pilot scenarios.

## Release checklist

- Approved change window and named owners.
- Backup completed and restore evidence available.
- Monitoring and failure alerts active.
- Customer communication sent.
- Rollback steps reviewed and time-boxed.
- Go/no-go decision recorded.

## Rollback plan

### Migration sequence

1. Confirm the approved change window, backup, owners, monitoring, and customer communication.
2. Capture a final backup and verify that it can be restored.
3. Control incoming events through the agreed path and record events received during the change for replay or reconciliation.
4. Run the database migration and validate schema, record counts, integrity checks, and application connectivity.
5. Resume normal flow, verify event processing, alerts, dashboard behavior, and monitoring.
6. Record the migration evidence before requesting production approval.

### Rollback triggers and authority

Rollback is triggered by a critical service failure, failed integrity or reconciliation check, lost or duplicated events outside the agreed tolerance, failed login or event-flow validation, or an unrecoverable monitoring or security control failure. The CTO / sponsor decides whether to authorize rollback; the PM coordinates the decision and evidence, DevOps executes the application rollback, and Database executes the data restore or reconciliation procedure.

Restoring a database backup and reverting the application version are separate actions. Data received after migration is protected through the recorded event path, replay, or reconciliation procedure. The team validates service health and data integrity after recovery and keeps the issue open until the sponsor and technical owners accept the result.

The PM records the decision, timeline, impact, evidence, and follow-up actions.

## Key terms

**Test gate:** A checkpoint that must pass before work advances.  
**Migration rehearsal:** A practice database change using representative data.  
**Rollback:** Returning the application or data path to an approved prior state.  
**Reconciliation:** Comparing records and events to find and resolve differences.
