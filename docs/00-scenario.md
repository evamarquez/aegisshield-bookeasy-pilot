# Sponsor Handoff and Scenario - Aegis Security Cloud Modernization

> Simulated portfolio case study. AegisShield, BookEasy, the decisions, participants, and outcomes are fictional and created for learning.

## 1. Business context

AegisShield is a fictional provider of a cloud security monitoring service. Its customer BookEasy runs a scheduling application for businesses. BookEasy sends security events to AegisShield, and AegisShield's security analysts investigate the alerts.

Following a leadership change, the CTO commissioned an assessment. The findings and a phased modernization direction are handed to the project team as inputs. The assessment happened before this implementation project and is not part of the delivery work described here.

## 2. Assessment handoff

| Area | Finding supplied to the project |
|---|---|
| Runtime and dependencies | Node.js 14 and PostgreSQL 12 are out of community support. Express, Passport, and Axios need compatibility and security review. |
| BookEasy connector | Retry behavior needs stronger duplicate protection, and delivery failures are not sufficiently visible. |
| Operations | Release, restore, and monitoring procedures are incomplete. Existing detections and dashboard behavior must continue to work. |

## 3. Sponsor request

The CTO asks the Technical Project Manager to deliver a controlled first modernization increment for BookEasy. The increment should move selected runtime and database components toward supported versions, improve retry and duplicate handling, make delivery failures visible, and preserve existing login, event ingestion, alerts, and dashboard behavior.

The service must remain available during the work, customer data must be protected, and production requires evidence and sponsor approval. The initial planning assumption is 12 weeks. The delivery team, sponsor, and BookEasy will confirm capacity and acceptance criteria during planning.

## 4. What the Project Manager must validate

The handoff is intentionally incomplete. The Project Manager must validate:

- Target runtime and database versions.
- Current owners and available team capacity.
- BookEasy pilot scenarios and acceptance criteria.
- Test coverage for login, ingestion, alerts, and dashboard behavior.
- Backup, restore, rollback, and monitoring readiness.
- Approval path and production change window.

## 5. Initial boundaries

### In scope

- Supported Node.js runtime and compatible application dependencies.
- PostgreSQL migration rehearsal and restore validation.
- BookEasy connector retries, duplicate protection, and delivery-failure visibility.
- Existing login, event ingestion, detections, alerts, and dashboard checks.
- Monitoring, backups, rollback readiness, testing, and release communication.

### Out of scope

- Rebuilding the entire platform.
- Modernizing every customer connector.
- Creating a new cybersecurity product.
- Redesigning the dashboard or detection rules.
- Claiming production success before validation evidence exists.

## 6. Initial timeline

- Initiation, design, and baseline: weeks 1-2.
- Environment, backups, and runtime work: weeks 3-4.
- Connector, database rehearsal, and monitoring: weeks 5-7.
- Integration, security, and recovery tests: weeks 8-9.
- BookEasy pilot: week 10.
- Controlled release and handover: weeks 11-12.

The 12 weeks are a planning assumption, not a promise. The schedule must be validated against capacity, dependencies, and agreed acceptance criteria.

## 7. Stakeholders

The CTO sponsors the work. The Project Manager coordinates Engineering, Database, Security, DevOps/SRE, QA, Product, Support, Customer Success, and BookEasy. Technical owners remain accountable for their designs and validation. The sponsor approves major scope changes and the production go/no-go decision.

## 8. First responsibility

The first responsibility is to turn an incomplete request into a shared understanding of the problem. The next steps are to confirm the mandate, identify decision-makers, document facts and assumptions, map the current state, prioritize risks, and create the charter and delivery plan.
