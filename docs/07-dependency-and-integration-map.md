# Dependency and Integration Map

| System or area | Connects to | Data or event | Direction | Main failure mode | Monitoring and recovery |
|---|---|---|---|---|---|
| BookEasy | Aegis Security Cloud connector | Security events | BookEasy to AegisShield | Timeout or duplicate event | Delivery alert, retry, stable event ID, replay check |
| AegisShield application | PostgreSQL | Accounts, events, configuration | Read and write | Incompatible schema or failed migration | Migration rehearsal, backup, restore, reconciliation |
| AegisShield | Detection and alert service | Normalized events and findings | Internal flow | Event loss or delayed processing | Ingestion metrics and alert checks |
| AegisShield | Customer dashboard | Alerts and status | Internal flow | Missing or incorrect display | Regression tests and customer acceptance |
| Deployment pipeline | Runtime and services | Release package and configuration | Delivery flow | Failed deployment or bad version | Pre-release checks and rollback runbook |

## Dependency order

1. Confirm target versions and test environment.
2. Prepare representative data and complete restore rehearsal.
3. Implement connector retry, stable IDs, and duplicate protection.
4. Configure failure monitoring and alerts.
5. Run functional, security, recovery, and customer pilot tests.
6. Obtain sponsor approval before controlled release.
