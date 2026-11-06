# Setup Guide — Recreate CLOZR in SWITCH

This is a manual recreation guide, not a one-click importer. SWITCH UI labels/integrations may vary.

## Prerequisites
SWITCH workspace with agent/room permissions; supported model provider; Slack permissions; optional Google Workspace connection; Git.

## 1. Clone
```bash
git clone <repository-url>
cd clozr-switch-workflow
```

## 2. Create rooms
Create `#clozr-sales`, `#clozr-ba`, `#clozr-development`. Use `rooms/*.yaml` for membership. Invite human operator and only listed agents.

Recorded recommended settings: Auto mode ON; Bypass permissions OFF; Who can talk: human and invited agents; Can manage agents OFF. Use closest available controls and keep permissions conservative.

## 3. Create agents
For every `agents/*.md`: create agent; set Agent ID/name; copy description; copy full Instructions section into instruction/system prompt; select provider available to you; grant minimum tools; save; test harmlessly; invite to room.

Order: Sales Coordinator then Sales specialists; BA Manager then BA specialists; Development Manager. Six engineering specialists listed as future roles are not part of current build.

## 4. Integrations
Original workspace connected Google Workspace OAuth at SWITCH level and assigned it to Coordinator, Follow-up Manager, Meeting Coordinator. Calendar lookup was tested; Gmail draft creation was not verified. In your workspace, test each permission/action independently. Do not grant send permissions by default.

Original agents used Claude Code provider on the user's computer; choose a provider supported by your workspace.

## 5. Test Sales
Use `examples/sample-lead.md`. Verify source evidence, scoring rationale, independent challenge, draft-only outreach, availability-vs-booking distinction, and no invented commercial terms.

## 6. Test BA
Use fictional Nova Retail project. Require unique requirement IDs, scope labels, version history, estimate reconciliation, independent QA verdict.

## 7. Test cross-room handoff
Have BA Manager create actual Markdown/PDF file or verified link. Open it as a human. Share actual artifact in `#clozr-development`. Ask Development Manager to verify access/version/approval. If inaccessible, it must report BLOCKED. No implementation before explicit approval.

## Troubleshooting
- Document inaccessible: attach actual file or provide accessible link; a Slack message is not enough.
- Agent missing: verify it exists and is invited.
- Claimed action: request actual tool evidence.
- Google integration unavailable: demonstrate draft workflow and label integration unconfigured.
- YAML import fails: use files as manual setup references.
