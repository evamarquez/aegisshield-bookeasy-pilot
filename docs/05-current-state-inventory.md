# Current-State Inventory

## Purpose

This inventory gives the team a shared view of what exists before any modernization work starts. It is a planning baseline, not a claim about a real production system.

## Platform components

| Area | Current state | Main concern | Owner |
|---|---|---|---|
| Application runtime | Older supported version is nearing end of support | Security fixes and library compatibility | Engineering |
| Event ingestion | Receives security events from customer systems | Delivery can be retried and create duplicates | Backend engineering |
| Database | PostgreSQL instance with older version and recovery steps | Migration and restore evidence is incomplete | Database engineering |
| Detection and alerts | Existing rules and alert flow are in use | Must keep working during the pilot | Security and Product |
| Customer dashboard | Existing dashboard used by analysts | No redesign in this increment; regression risk still matters | Product and QA |
| Monitoring | Basic service and connector monitoring exists | Delivery failures are not always visible early | DevOps / SRE |
| Release process | Team has deployment and rollback steps | Steps need to be tested and documented for this change | DevOps / SRE |

## Key dependencies

1. Runtime and dependency updates must be tested before the BookEasy pilot.
2. The connector needs agreed event scenarios before retry and duplicate handling can be tested.
3. Database migration depends on a representative test copy and a successful restore rehearsal.
4. Monitoring and alerts must be ready before integration testing.
5. QA evidence, security review, customer acceptance, and sponsor approval are required before production release.

## Baseline questions

- Which runtime and database versions are the approved targets?
- What event types and volumes should BookEasy use for pilot validation?
- What is the recovery time target if rollback is needed?
- Which existing alerts and dashboards are release-blocking if they fail?
- Who can approve a schedule change or stop the release?

## Planning conclusion

The first increment should focus on supportability, data recovery, connector reliability, and failure visibility. A full platform rebuild or a redesign of the customer experience would create too much scope for this pilot.
