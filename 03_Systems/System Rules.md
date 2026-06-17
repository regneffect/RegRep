# System Rules

These are the operating rules for the whole vault. Claude reads this together with `Claude.md` before acting.

## The Core Rule

Reggie only dumps raw notes into `00_Capture/Capture.md`. The system does the sorting, summarizing, task extraction, project tracking, and review. Never push the sorting burden back onto Reggie.

## Notion Is Canonical

Notion is the system of record for all CMU operational data. Obsidian is the capture/thinking/writing workbench. Operational items captured here are routed to Notion via the owning CMU skill (never duplicated as a competing table in Obsidian). Full seam, database map, and PII firewall: [[Notion Bridge]].

## Before Doing Any Work

1. Read `Claude.md`.
2. Read the Current Weekly Priorities in `Claude.md`.
3. Read `01_Active/Active Projects.md`.
4. Read `05_Queue/Claude Queue.md`.
5. Read recent notes in `00_Capture/`.

## Folder Purposes

- `00_Capture/` — inbox. Everything lands here first. No sorting.
- `01_Active/` — current live projects and urgent work.
- `02_Resources/` — reference and reusable knowledge.
- `03_Systems/` — instructions, workflows, SOPs, governance.
- `04_Generated/` — Claude outputs.
- `05_Queue/` — tasks for Claude to handle.
- `06_Calendar/` — daily/weekly/monthly and dated notes.
- `07_Archive/` — old, completed, or deprecated material.
- `08_Templates/` — reusable note templates.
- `09_Dashboards/` — home and review dashboards.

## Standing Conventions

- Plain Markdown only. No plugins required.
- Use Obsidian wiki links: `[[Note Name]]` or `[[Folder/Note Name]]`.
- Use `YYYY-MM-DD` for all dates.
- Never delete capture content — archive it to `07_Archive/Processed Capture Log.md`.
- When a task is unclear, write a clarification note instead of guessing wildly.
- Keep outputs clear, direct, usable, and honest about risk.

## Governance / Safety

- Claude drafts and organizes; it does not send messages, publish, or take outside-facing actions without Reggie's explicit go-ahead.
- Keep any sensitive personal information out of generated public-facing material.
- Stress-test weak ideas. Tell the truth.

## The Workflows

- [[Morning Briefing Workflow]]
- [[Capture Processor Workflow]]
- [[Weekly Review Workflow]]
- [[Queue Processor Workflow]]
- [[Project Health Monitor Workflow]]
