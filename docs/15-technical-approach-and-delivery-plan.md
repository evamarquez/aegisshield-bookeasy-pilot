# Technical Approach and Delivery Plan

## Service flow

BookEasy systems -> connector -> AegisShield event API -> PostgreSQL -> existing detection rules -> analyst dashboard.

No separate queue is assumed in this case. Monitoring tracks request, retry, duplicate, and delivery-failure status directly.

## Methodology used

This project uses a hybrid approach. The team uses a planned approach for scope, risks, approvals, dates, and release decisions. The technical work is delivered in small steps so the team can build, test, find issues, and correct them before moving forward.

## Proposed changes

| Area | Approach | Owner |
|---|---|---|
| Runtime and libraries | Propose Node.js 24 LTS and compatible Express, Passport, and Axios versions; validate compatibility before approval. | Engineering lead |
| Database | Propose PostgreSQL 17; rehearse migration, protect incoming events, and verify restore and integrity. | Database engineer |
| Connector | Use a stable event ID, check processed-event records before writing, make retries safe, and expose delivery failures. | Backend engineer |
| Operations | Monitor request, retry, duplicate, and delivery-failure status. | DevOps / SRE |

## Delivery plan and dependencies

1. Confirm compatibility and target versions.
2. Implement in a non-production environment after targets and test data are ready.
3. Rehearse migration and recovery, including how incoming events are protected and reconciled.
4. Run functional, security, integration, duplicate, monitoring, and rollback tests.
5. Validate agreed scenarios with BookEasy and record acceptance.
6. Present evidence, readiness, rollback, and change-window details to the sponsor for go/no-go approval.

## Technical safeguards

The stable event ID is checked against processed-event records before an event is written, so a retry is accepted only once. Database restore and application rollback are separate procedures: restore recovers data, while rollback returns the application to the prior version. Node.js 24 and PostgreSQL 17 are proposed targets pending compatibility validation and technical-owner approval.
