# CLOZR Architecture

## Product shape
Slack-first multi-agent workflow. SWITCH provides orchestration/tool access; Slack is the human-facing collaboration surface.

## Departments
- Sales Coordinator routes research, qualification, strategy, follow-up, meetings, proposals.
- BA Manager coordinates requirements, architecture, estimation, QA, and versioned internal handoff.
- Development Manager verifies handoff, plans, and manages implementation after human approval.

## Collaboration
Dedicated Slack room per department; shared project IDs and document versions; actual accessible files for cross-room handoff; human approval for consequential actions.

## Companion application stack recorded
- Frontend: React, TypeScript, Vite, Tailwind CSS, shadcn/ui, React Router, TanStack Query, Axios, React Hook Form, Zod, Lucide.
- Backend: NestJS, TypeScript, TypeORM, PostgreSQL.
- Architecture: single modular monolith.
- SWITCH: agent orchestration.
- Slack: collaboration workspace.

Backend foundation and Leads CRUD were recorded complete; frontend shell and Leads UI integrated and CRUD verified. This repo documents agent workflow, not full application source.

## Security boundaries
Least privilege; no secrets in prompts/Slack/Git; approval before external communication, bookings, proposals, commitments, scope changes, production actions; report actual tool results; do not claim inaccessible documents were reviewed; protect client data and avoid cross-project leakage.
