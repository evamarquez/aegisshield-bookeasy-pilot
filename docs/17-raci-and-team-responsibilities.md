# RACI and Team Responsibilities

## How to read the matrix

The matrix uses R, A, C, and I to show responsibility, accountability, consultation, and updates.

| Deliverable or decision | R | A | C | I |
|---|---|---|---|---|
| Project baseline approval | PM | CTO / sponsor | Engineering lead, Product | Delivery team |
| Project reporting | PM | PM | CTO / sponsor | Delivery team |
| Runtime and connector changes | Backend engineer | Engineering lead | Security, QA, DevOps | PM |
| Database migration and restore | Database engineer | Database engineer | DevOps, Engineering, QA | PM, Security |
| Security and data protection validation | Security engineer | Security lead | Database, DevOps, QA | PM, CTO |
| Test evidence and defect validation | QA engineer | QA engineer | Engineering, Security, Database | PM |
| BookEasy pilot acceptance | Customer Success | BookEasy representative | QA, Engineering, PM | CTO |
| Production go/no-go authorization | PM coordinates evidence | CTO | Engineering, QA, Security, DevOps, BookEasy | Delivery team |
| Production deployment execution | DevOps / SRE | Engineering lead | Database, QA, Security, PM | CTO, Customer Success |
| Operational handover acceptance | DevOps / SRE | Support lead | Engineering, Database, QA, PM | Customer Success |

The person who executes a task can also be accountable for its result. Authorization and execution are separate responsibilities.

## Key terms

**Responsible:** The role that performs the work.  
**Accountable:** The role that answers for the result or makes the final decision. Each row has one accountable role.  
**Consulted:** People whose input is needed before completing the work or making a decision.  
**Informed:** People who receive updates but do not need to approve the work.  
**Baseline:** An approved version of the project plan used to track progress and assess changes.  
**Go/no-go:** A formal decision to proceed with or postpone a release.  
**Handover:** The transfer of the service, documentation, and support responsibilities to the operations team.
