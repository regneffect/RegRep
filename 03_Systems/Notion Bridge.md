# Notion Bridge

**Notion is the canonical system of record for all CMU operational data.** Obsidian is the capture, thinking, writing, and knowledge workbench. This file defines the seam between them.

## The Rule

- **Operational data lives in Notion.** Youth, sessions, outcomes, sites, mentors, lanes/projects, decisions, partners, touchpoints — the authoritative record is Notion, never a parallel table in Obsidian.
- **Knowledge and drafts live in Obsidian.** Capture, grants, dissertation, journalism, SOPs, research, and Claude outputs.
- Obsidian never becomes a second source of truth for anything Notion owns. Where Obsidian shows operational info, it is a **read-only mirror or a pointer**, not the master copy.

## How Writes Happen (governance)

Claude does **not** write to Notion ad hoc from capture. Operational items are routed to the **owning CMU skill**, which performs the write under its existing governance pre-check:

| Item type | Notion database | Owning skill |
|---|---|---|
| New youth referral / intake | Youth | `cmu-case-tracker` |
| Session log / case note | Sessions | `cmu-case-tracker` |
| Outcome check-in (30/60/90/180/365) | Outcomes | `cmu-case-tracker` |
| Site / mentor record | Sites / Mentors | `cmu-case-tracker` |
| Project / lane status update | Lanes | `cmu-executive-dashboard` |
| Load-bearing decision | Decisions | `cmu-executive-dashboard` |
| Partner outreach / interaction / MOU | Touchpoints / Partners | `cmu-partner-relations` |
| Compound or unclear (spans skills) | — | `cmu-orchestrator` (routes + governance) |

For anything ambiguous or multi-skill, start with `cmu-orchestrator`.

## PII Firewall (hard rule)

- **No youth-level PII in Notion. No youth-level PII in Obsidian either.**
- PII stays in the local intake vault (`~/CMU-Bots/cmu-intake-tracker/`); only **de-identified** data is exported to Notion.
- If a capture item contains PII (names, DOB, addresses, case numbers), Claude **flags it and routes it to the local intake tracker**, de-identifying before anything reaches Notion. It does not paste PII into either tool.

## Capture → Notion Flow

When the Capture Processor finds an operational item:

1. Identify the item type and its Notion database + owning skill (table above).
2. Check for PII → if present, route to the local intake vault, de-identify first.
3. **Stage** the proposed Notion write in `05_Queue/To Notion.md` (what, which DB, which skill).
4. On Reggie's go-ahead, the owning skill performs the write under its governance pre-check.
5. Leave a pointer in Obsidian (e.g., in `Active Projects` working view) — never a duplicate record.

## What Stays Purely in Obsidian

- Raw capture, grants pipeline, dissertation, journalism, research, SOPs, templates, and all Claude drafts/outputs.
- These never need to round-trip to Notion unless they graduate into an operational commitment (then a pointer/lane update goes to Notion).
