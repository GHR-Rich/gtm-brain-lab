# gtm-brain-lab

A lab for experimenting with go-to-market (GTM) workflows, data and AI tooling.

This repository holds a small "GTM brain" built from **fictional training data**
about one account (AlderWorks), one discovery call and one product (SignalNest).
It is plain files: no database, no scripts, no connectors.
Lab owner and reviewer: Rich Nigro.

## How it fits together

```
original sources  →  reviewed knowledge  →  decision and rationale  →  task context  →  checked answer
sources/             knowledge/              decisions/                 context/          tests/
```

| Layer | Folder | Why it exists |
|---|---|---|
| Original sources | `sources/` | The evidence, kept word for word with ID, owner, date and version. Nothing here is edited or interpreted. |
| Reviewed knowledge | `knowledge/` | People, accounts, needs and capabilities pulled out of the sources, each linked to its source and an exact quote. AI drafts start as *candidate* until a person reviews them. |
| Decision and rationale | `decisions/` | What we plan to do and why, with alternatives, unknowns and a revisit trigger. A proposal is not an approval. |
| Task context | `context/` | Only what is needed for the task at hand, assembled from reviewed knowledge and the decision. |
| Checked answer | `tests/` | Questions with expected answers, so we can tell whether an assistant using this context got it right. |

`views/connections.md` is a derived table linking customer need, capability and
decision. It is rebuilt from the files above and is never the source of truth.
`governance/rules.md` holds the rules everything else follows.

## Who owns which claims

| Source | Owner | Authoritative for | Not authoritative for |
|---|---|---|---|
| CRM-001 (`sources/account.md`) | Revenue Operations | Account and contact identity, CRM fields | What the customer said; product facts |
| CALL-001 (`sources/call.md`) | Account Executive | What the customer said and asked | Whether a product capability exists |
| PROD-001 v1 (`sources/product.md`) | Product Marketing | Approved capabilities and claims | Customer needs |

A customer asking for something (for example, a direct Salesforce connection)
does not make it available. Only PROD-001 says what SignalNest can do.

## Files

| Path | Status |
|---|---|
| `README.md` | This guide |
| `sources/account.md`, `sources/call.md`, `sources/product.md` | Original sources, unchanged |
| `governance/rules.md` | Sample rules; only the reviewer name filled in |
| `knowledge/entities.csv`, `knowledge/relationships.csv` | Candidate records |
| `decisions/DEC-001.md` | Proposed decision |
| `context/current-task.md` | Created after review |
| `tests/checks.md` | Created after review; checks start as Not run |
| `views/connections.md` | Derived view |

## Status words
- **candidate**: AI-generated, not yet checked by a person.
- **reviewed**: a person checked it against the quoted evidence.
- **proposed / approved**: decisions only; approval is recorded explicitly by the reviewer.
- **Not run / Pass / Fail**: checks only; set from observed answers and the reviewer's judgment.

Saving or pushing a file does not approve it.
