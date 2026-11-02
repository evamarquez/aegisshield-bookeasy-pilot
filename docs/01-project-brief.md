# Project Brief — Aegis Security Cloud Modernization

## 1. Case framing

This case explores how a Technical Project Manager could lead the modernization of a cybersecurity SaaS platform whose core components and integrations have not received a coordinated major update in approximately five years.

The project is fictional. The goal is to demonstrate the thinking, documentation, and coordination practices used in a real technical project—not to claim that the work was performed for a real company.

## 2. Fictional company context

**AegisShield** sells cybersecurity software to mid-sized companies that need a central view of their security posture without operating a large security team.

Its fictional platform, **Aegis Security Cloud**, currently includes:

- Endpoint and workload monitoring.
- Vulnerability and asset discovery.
- Network and cloud security integrations.
- Centralized security event collection.
- Executive and compliance reporting.

The product has paying customers and cannot simply be taken offline for a rebuild.

## 3. The problem

The platform has accumulated five years of uncoordinated technical change. Leadership does not yet have a reliable view of:

- Which application components are outdated or out of support.
- Which dependencies create security, reliability, or compliance risk.
- Which integrations may break during an upgrade.
- Which modules should be upgraded, replaced, retired, or left unchanged.
- How to sequence the work while protecting customer operations.

The immediate problem is not “upgrade everything.” The immediate problem is the absence of a trusted baseline and an agreed modernization sequence.

## 4. Project objective

Create and approve a risk-based modernization roadmap for Aegis Security Cloud, then coordinate a controlled BookEasy pilot. The first increment should move selected runtime and database components toward supported versions, improve connector reliability, make delivery failures visible, and preserve existing login, event ingestion, alerts, and dashboard behavior. Production release requires test evidence and sponsor approval.

## 5. Proposed outcomes

By the end of the case, the team should have:

1. A current-state inventory of major services, dependencies, integrations, and ownership.
2. A classification of components as upgrade, replace, retire, monitor, or investigate.
3. A prioritized risk register covering security, reliability, delivery, and customer impact.
4. A phased modernization roadmap with sequencing and dependencies.
5. A release and validation approach for the BookEasy pilot.
6. A stakeholder communication plan for internal teams and BookEasy.
7. A handover and rollback approach for the first increment.

These are planned deliverables, not claimed completed results.

## 6. In scope

- The selected application runtime and third-party dependencies.
- PostgreSQL migration rehearsal and restore validation.
- BookEasy connector retries, duplicate protection, and delivery-failure visibility.
- Existing login, event ingestion, detections, alerts, and dashboard checks.
- Monitoring, backups, rollback, testing, and release communication.

## 7. Out of scope for the first increment

- Rebuilding the entire platform from scratch.
- Replacing every vendor or cloud provider.
- Modernizing every customer connector.
- Redesigning the dashboard or detection rules.
- Claiming production migration success without evidence.

## 8. Roles in this case

### Business Analyst perspective

- Clarify the business problem and consequences of inaction.
- Gather stakeholder needs and constraints.
- Compare options and document assumptions.
- Help define decision criteria.

### Technical Project Manager perspective

- Establish scope, milestones, dependencies, and governance.
- Coordinate technical and non-technical stakeholders.
- Maintain the RAID log and decision log.
- Prepare delivery, testing, release, and communication plans.
- Escalate blockers and make progress visible.

### Product Manager perspective

- Protect customer and product priorities.
- Decide which modernization work is essential for the product roadmap.
- Balance platform health, customer value, and commercial commitments.
- Align the modernization roadmap with future product direction.

In the portfolio simulation, one person performs all three perspectives. Each artifact will label which perspective is being used.

## 9. Initial success measures

The project will be considered well-framed when:

- At least 95% of critical platform components have an identified owner and lifecycle status.
- Critical dependencies and customer-impact risks have documented mitigations.
- The BookEasy pilot has agreed acceptance criteria covering retry behavior, duplicate protection, event visibility, and existing core functions.
- Engineering, Security, QA, Product, and Customer Success approve the proposed sequence.
- The release plan includes validation, monitoring, rollback, customer communication, and sponsor go/no-go approval.

These are fictional target measures for the case and will be refined after the inventory is created.

## 10. Key assumptions to validate

- AegisShield has access to a staging environment representative of production.
- The platform supports multiple customer tenants.
- Some customers depend on legacy APIs or integrations.
- The engineering team has incomplete documentation.
- Security and customer support must approve high-impact changes.

## 11. Open questions

- What technology stack does the platform use?
- Which components are already out of vendor support?
- Which integrations are business-critical?
- What service-level commitments exist for customers?
- What maintenance windows are available?
- Which compliance frameworks influence the roadmap?
- What is the current incident and vulnerability baseline?

These questions will be answered gradually rather than assumed away.
