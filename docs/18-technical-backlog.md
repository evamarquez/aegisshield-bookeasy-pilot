# Technical Backlog

## Prioritized work

| ID / WBS | Task / owner | Priority | Status | Effort | Dependency | Acceptance evidence |
|---|---|---|---|---|---|---|
| B01 / 2.1 | Update runtime and review dependencies / Engineering | High | Done | 4 days | Approved technical approach | Login, API, and regression tests pass |
| B02 / 2.2 | Implement stable IDs, retries, and deduplication / Backend | High | In progress | 5 days | BookEasy scenarios | Same event is processed once after timeout and retry |
| B03 / 3.1 | Rehearse migration and restore / Database | High | Done | 4 days | Test environment and representative data | Records reconcile and restore succeeds |
| B04 / 2.3 | Configure ingestion monitoring / DevOps | High | In progress | 3 days | Connector test environment | Simulated failure generates an actionable alert |
| B05 / 4.1 | Run integration and functional tests / QA | High | Pending | 4 days | B01-B04 ready | Agreed tests pass with no critical defects |
| B06 / 4.1 | Run security and data protection validation / Security | High | Pending | 2 days | Test build and data plan | Access, encryption, approved test data, and clean logs verified |
| B07 / 4.2 | Coordinate BookEasy pilot / Customer Success | High | Pending | 3 days | B05-B06 and scenarios | BookEasy accepts documented results |
| B08 / 4.3 | Execute application and connector release / DevOps | High | Pending | 2 days | Pilot acceptance and go/no-go | Deployment and production checks recorded |
| B09 / 4.4 | Transfer support procedures / DevOps and Support | Medium | Pending | 2 days | Release stabilization | Support accepts runbook and ownership |
| B10 / 1.3 | Close project and capture lessons learned / PM | Medium | Pending | 1 day | Handover accepted | Closure record completed |

## Key terms

**Backlog:** The ordered list of work planned for the project.  
**Dependency:** Work that must happen before another task can start or finish.  
**Acceptance evidence:** Proof that a requirement or task is complete.  
**Retry:** Trying delivery again after a temporary failure.  
**Deduplication:** Preventing the same event from being processed more than once.  
**Regression testing:** Checking that existing behavior still works after a change.  
**Runbook:** Step-by-step instructions for operating, supporting, or recovering a service.
