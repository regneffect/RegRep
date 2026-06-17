# Capture Processor Workflow

## Purpose

Process everything dumped into `00_Capture/Capture.md`.

## Claude Instructions

1. Read `Claude.md`.
2. Read `03_Systems/File Routing Rules.md`.
3. Read `00_Capture/Capture.md`.
4. Identify unprocessed items under `Raw Capture`.
5. Split mixed capture into separate notes/tasks.
6. Route each item to the right folder.
7. Create new notes when needed.
8. Append to existing notes when appropriate.
9. Extract tasks into `05_Queue/Claude Queue.md`.
10. Route operational items to Notion: stage them in `05_Queue/To Notion.md` for the owning CMU skill (see [[Notion Bridge]]). Check for PII first — PII goes to the local intake vault and is de-identified before Notion. Do not write a competing record in Obsidian.
11. Update the `01_Active/Active Projects.md` working mirror only as a pointer (Notion Lanes is canonical).
12. Move processed raw text into `07_Archive/Processed Capture Log.md`.
13. Clear the processed section from `00_Capture/Capture.md`.
14. Leave a short summary in Capture.

## Output Summary Format

At the top of `00_Capture/Capture.md`, write:

```markdown
## Last Processed

Date:
Items processed:
Moved to Active:
Moved to Resources:
Moved to Queue:
Moved to Calendar:
Archived:
Notes:
```
