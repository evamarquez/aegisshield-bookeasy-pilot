# Issue Log

## Issue ISS-01

| Field | Record |
|---|---|
| Detected | Week 8 during staging integration tests |
| Current status | Closed |
| Closure date | March 13, 2026 (simulated) |
| Priority | High |
| Target resolution | March 13, 2026 |
| Related risk and requirement | R03 - missing or duplicate events; REQ-03 |
| GitHub reference | github-board-during.md, ISS-01 card |
| Impact | Duplicate test events could produce repeated alerts and blocked pilot approval. No production impact is claimed. |
| Owner | Engineering lead; backend engineer implements the correction and QA verifies it |

## Cause and correction

**Root cause:** When the response timed out, the retry created a new event identifier.  
**Correction:** Preserve the original event ID and check processed-event records before writing so the same event is processed once.

## History

| When | Action / outcome | Owner |
|---|---|---|
| Week 8 | Reproduced timeout scenario and traced the identifier change. Status was Open. | Engineering / QA |
| Weeks 9-10 | Preserved the original ID, reviewed monitoring, and added timeout and duplicate tests. | Backend / DevOps / QA |
| Week 10 | QA reran normal delivery, timeout, retry, and duplicate scenarios. | QA / Engineering lead |
| Week 10 | Engineering lead verified the correction; QA recorded passing evidence; PM accepted closure against REQ-03. | Engineering / QA / PM |

## Closure evidence

The issue closed after the agreed acceptance scenarios passed. Evidence includes processing logs, retry test results, duplicate checks, and the QA test record. The result applies to the agreed pilot scenarios and does not claim that every possible failure condition has been eliminated.

## Key terms

**Issue:** A current problem that needs action. *Example: ISS-01 blocked the BookEasy pilot.*  
**Defect:** Behavior that fails an expected result. *Example: a retry processed one event twice.*  
**Root cause:** The underlying reason the defect happened. *Example: the retry created a new event ID.*  
**Retest:** Running the failed scenario again after a correction. *Example: QA repeated the timeout and retry test in week 10.*  
**Closure evidence:** Documented proof that the issue is resolved and verified. *Example: passing logs, duplicate checks, and QA results linked to REQ-03.*
