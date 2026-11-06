# CLOZR — Your AI Sales & Delivery Department

CLOZR is a Slack-first multi-agent business team orchestrated through SWITCH. Specialist agents collaborate in dedicated rooms, share structured work, challenge assumptions, and prepare decisions for human approval.

This repository is a **human-readable setup/configuration kit**, not an automatic SWITCH importer. Judges can recreate the system by creating agents and rooms in their own SWITCH workspace using the descriptions and instructions below.

## Departments
- **Sales:** lead research, qualification, strategy, follow-up drafts, meeting coordination, proposal drafts.
- **Business Analysis:** requirements, architecture, estimation, independent QA, internal development handoff.
- **Development:** handoff intake, readiness checks, execution planning, implementation management after human approval.

## Agent inventory

| Department | Agent ID | Purpose |
|---|---|---|
| Sales | `clozr-coordinator` | Routes sales work and consolidates results |
| Sales | `clozr-lead-hunter` | Finds evidence-backed business opportunities |
| Sales | `clozr-lead-qualifier` | Scores fit, need, urgency, and evidence |
| Sales | `clozr-followup-manager` | Prepares outreach drafts; does not send |
| Sales | `clozr-meeting-coordinator` | Checks availability; does not book without approval |
| Sales | `clozr-proposal-agent` | Drafts proposals from validated discovery |
| Sales | `clozr-sales-strategist` | Independently challenges sales conclusions |
| BA | `clozr-ba-manager` | Coordinates BA and prepares internal handoff |
| BA | `clozr-requirements-analyst` | Requirements, journeys, assumptions, acceptance criteria |
| BA | `clozr-solution-architect` | Architecture, data model, integrations, security |
| BA | `clozr-estimation-analyst` | Transparent effort ranges and dependencies |
| BA | `clozr-qa-validator` | Independent BA package review |
| Development | `clozr-development-manager` | Engineering intake, planning, delivery management |

**Not created in this build:** `clozr-backend-engineer`, `clozr-frontend-engineer`, `clozr-database-architect`, `clozr-qa-engineer`, `clozr-devops-engineer`, `clozr-security-reviewer`. These are future role suggestions only. The Development Manager must not claim they exist or delegate to them.

## Structure

```text
clozr-switch-workflow/
├── README.md
├── agents/                 # Agent IDs, descriptions, copy/paste instructions
├── rooms/                  # Room membership and settings references
├── workflows/              # Cross-agent and cross-department processes
├── examples/               # Fictional test data and sample collaboration
├── docs/                   # Architecture, setup, approval, status, demo
├── templates/              # Reusable intake and handoff templates
└── .gitignore
```

## Quick start
1. Read `docs/setup-guide.md`.
2. Create each agent in SWITCH using its matching `agents/*.md` file.
3. Create `#clozr-sales`, `#clozr-ba`, and `#clozr-development` using `rooms/*.yaml`.
4. Configure your own provider credentials and optional integrations.
5. Follow `workflows/` and run the fictional Nova Retail test.

## Important notes
- YAML files are human-readable setup references, not guaranteed SWITCH import files.
- The original workspace used Claude Code provider on the user's computer; a judge should choose a provider available in their own SWITCH workspace.
- Google Workspace OAuth was connected at SWITCH level and assigned to Coordinator, Follow-up Manager, and Meeting Coordinator. Calendar lookup was tested. Gmail draft creation was not verified.
- Never commit API keys, OAuth tokens, passwords, or client secrets.
- Nova Retail is fictional. Its effort estimates are planning artifacts, not a commercial quote.
- See `docs/current-build-status.md` for recorded progress and limitations.
