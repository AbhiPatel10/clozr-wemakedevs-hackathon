# Human Approval and Safety Model

CLOZR prepares and coordinates work; humans retain control of consequential decisions.

| Action | Agent may prepare | Human approval to execute |
|---|---:|---:|
| Public lead research | Yes | Follow workspace policy |
| Lead score/strategy | Yes | No |
| Outreach draft | Yes | Yes, before sending |
| Email/prospect contact | No by default | Yes |
| Calendar availability lookup | Yes, if connected | No |
| Create/move/cancel meeting | No by default | Yes |
| Proposal draft | Yes | Yes, before sending |
| Pricing/commercial terms | Human inputs only | Yes |
| Requirements/architecture recommendations | Yes | Human sign-off |
| Internal handoff draft | Yes | BA Head approval |
| Development plan | Yes | Engineering Lead approval |
| Code implementation | Only after approval | Yes |
| Scope/architecture change | Recommend only | Yes |
| Production deployment/data changes | No by default | Yes |
| Final acceptance | Prepare evidence | Yes |

## Status vocabulary
- DRAFT — prepared, not approved.
- PENDING APPROVAL — waiting for named human.
- APPROVED FOR PLANNING — planning only.
- APPROVED FOR IMPLEMENTATION — implementation allowed within explicit scope.
- BLOCKED — missing access, decision, dependency, or permission.

## Non-negotiable
Sharing ≠ approval. Internal handoff ≠ client SOW. Slack summary ≠ source artifact. Never claim sent/booked/attached/tested/deployed without tool evidence. Stop affected work when blocked. Do not expose secrets.
