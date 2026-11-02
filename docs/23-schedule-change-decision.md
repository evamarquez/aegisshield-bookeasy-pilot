# Schedule Change Request and Decision

## Change request

**Requested by:** Project Manager  
**Date requested:** February 27, 2026 (simulated)  
**Related issue:** ISS-01  
**Proposed change:** Move the plan from 12 to 13 calendar weeks while keeping scope and acceptance criteria unchanged.

ISS-01 blocks the BookEasy pilot because a timeout retry can create duplicate events. The PM recommends delaying the pilot rather than reducing testing. The request uses targeted part-time effort from Engineering, QA, PM, and Customer Success. No additional budget is requested at this point. BookEasy and the delivery team confirm availability for the revised dates.

## Pre-decision analysis

| Area | Impact |
|---|---|
| Dates | Pilot moves from week 10 to week 11; production from week 11 to week 12; stabilization, handover, and closure move to week 13. |
| Resources | Targeted recovery work is added; a full extra week is not assumed for every role. |
| Costs | No additional budget is approved; any material impact is escalated. |
| Risks | Keeping the original date risks duplicate events and weak acceptance evidence; reducing tests increases release risk. |

## Decision record

| Field | Record |
|---|---|
| Reference | DEC-01; related to ISS-01 and R03 |
| Requested by | Project Manager, based on Engineering and QA recovery estimate |
| Date requested | February 27, 2026 (simulated) |
| Decision maker | CTO / sponsor |
| Date approved | March 2, 2026 (simulated) |
| Decision | Approve a one-week schedule extension; keep scope and release criteria unchanged. |
| PM recommendation | Delay the pilot rather than reduce testing because the defect affects event integrity and customer acceptance. |
| Alternatives considered | Reduce test scope (rejected); keep week 10 without a fix (rejected); add capacity (reviewed but not required). |
| Decision limit | This decision does not authorize production; a separate go/no-go is required. |

## Revised baseline

| Milestone | Original baseline | Revised baseline |
|---|---|---|
| BookEasy pilot | Week 10 | Week 11, subject to passing retest |
| Controlled production release | Week 11 | Week 12, subject to pilot acceptance and go/no-go |
| Handover and project closure | Week 12 | Week 13 after stabilization |

The approved schedule becomes Revised Baseline v1.1.

## Resource and cost impact

The extra calendar week uses targeted part-time Engineering, QA, PM, and Customer Success effort. It does not mean a full extra week for every role. No additional budget is approved in this decision. Engineering, QA, and BookEasy confirmed availability for the revised dates; material capacity or cost changes require escalation.

## Key terms

**Schedule extension:** Adding time to the project plan.  
**Forecast:** The date the team expects to finish.  
**Revised baseline:** Sponsor-approved dates used to measure progress after a change.  
**Go/no-go:** The separate decision to proceed with or postpone production.
