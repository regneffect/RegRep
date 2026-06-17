# File Routing Rules

Claude should use these rules when processing `00_Capture/Capture.md`.

## Route to `01_Active/`

Use for:
- live CMU projects
- grants in progress
- current partner conversations
- current program tasks
- active dissertation sections
- current article drafts
- current funding opportunities
- urgent operational needs
- current housing/hotel project work
- Smart Choices current implementation
- Passport or Quest current planning

## Route to `02_Resources/`

Use for:
- reference material
- quotes
- research
- policy notes
- legal/regulatory information
- book notes
- articles
- background knowledge
- models/frameworks
- reusable program ideas
- examples from other organizations

## Route to `03_Systems/`

Use for:
- Claude instructions
- prompts
- workflows
- SOPs
- templates
- AI agent rules
- automation logic
- Obsidian system changes

## Route to `04_Generated/`

Use for:
- Claude-generated outputs
- drafts
- summaries
- reports
- memos
- grant language
- article drafts
- meeting summaries
- project briefs

## Route to `05_Queue/`

Use for:
- tasks for Claude
- "write this"
- "summarize this"
- "turn this into"
- "research this"
- "draft email"
- "make a plan"
- "analyze this"
- anything requiring Claude action

## Route to `06_Calendar/`

Use for:
- dates
- deadlines
- meetings
- weekly planning
- daily logs
- reminders
- time-bound commitments

## Route to `07_Archive/`

Use for:
- completed items
- dead projects
- outdated drafts
- old notes
- superseded versions
- material no longer active

## Route to Notion (canonical operational record)

Notion owns operational data. When a capture item is operational, do NOT file a competing record in Obsidian — stage it in `05_Queue/To Notion.md` and route to the owning CMU skill. See [[Notion Bridge]] for the full database map.

Route to Notion for:
- new youth referral / intake → Youth (cmu-case-tracker)
- session log / case note → Sessions (cmu-case-tracker)
- outcome check-in (30/60/90/180/365) → Outcomes (cmu-case-tracker)
- site / mentor record → Sites / Mentors (cmu-case-tracker)
- project / lane status update → Lanes (cmu-executive-dashboard)
- load-bearing decision → Decisions (cmu-executive-dashboard)
- partner outreach / interaction / MOU → Touchpoints / Partners (cmu-partner-relations)
- anything compound or unclear → cmu-orchestrator

PII firewall: never put youth-level PII in Notion or Obsidian. Route PII to the local intake vault and de-identify before anything reaches Notion.

## Capture Processing Rules

When processing Capture:

1. Read all new raw capture items.
2. Break mixed notes into separate items.
3. Identify each item type.
4. Route each item to the correct folder.
5. Create or append to the correct note.
6. Extract tasks.
7. Add tasks to `05_Queue/Claude Queue.md` if Claude needs to act.
8. Add active projects to `01_Active/Active Projects.md`.
9. Add dated items to `06_Calendar/Weekly Plan.md` or `06_Calendar/Daily Log.md`.
10. Move processed capture text into `07_Archive/Processed Capture Log.md`.
11. Clear the processed section from `00_Capture/Capture.md`.
12. Leave a short processing summary at the top of Capture.
