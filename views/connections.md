# Connections view (derived, not a source of truth)

This is a readable view built from `knowledge/entities.csv`,
`knowledge/relationships.csv` and `decisions/DEC-001.md`.
It is our knowledge/context graph written as a table: not a graph database
and not an automatic connector. Rebuild it whenever a source, record or
decision changes. Built: 2026-10-22. All rows inherit candidate / proposed status.

| Customer need (CALL-001) | Capability (PROD-001 v1) | Fit | Decision |
|---|---|---|---|
| NEED-003: See supplied call notes become a useful preparation brief (REL-007) | CAP-001: Preparation drafts from supplied notes and approved reference documents (REL-009) | Direct match to the request | DEC-001 (proposed): this is the demo |
| NEED-001: Reps prepare from scattered notes and sometimes outdated product information (REL-005) | CAP-001: drafts use *approved* reference documents (REL-009) | Interpretation: plausible fit, not proven | DEC-001 (proposed): talking point; no time-saving claim |
| NEED-002: Does SignalNest connect directly to Salesforce? (REL-006); AlderWorks uses Salesforce (REL-002) | CAP-002: native integration not generally available; manual export can be used (REL-010, REL-011) | Gap: request does not equal availability | DEC-001 (proposed): answer as written in PROD-001 v1 |

Tentative timing: MEET-001, October 27 suggested, not confirmed (REL-008).
Unknown: budget, purchase timing, contact title.
