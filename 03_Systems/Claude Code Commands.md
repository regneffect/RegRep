# Claude Code Commands

Use these commands with Claude Code. Copy a block, paste it into Claude, and let it run.

---

## Morning Briefing

```text
Read Claude.md and run the Morning Briefing Workflow from 03_Systems. Create today's morning briefing and save it in 04_Generated/Morning Briefings.
```

## Process Capture

```text
Read Claude.md, read File Routing Rules, then process everything in 00_Capture/Capture.md. Route notes to the correct folders, extract tasks to 05_Queue/Claude Queue.md, update Active Projects, archive processed capture, and leave a processing summary.
```

## Weekly Review

```text
Read Claude.md and run the Weekly Review Workflow. Review active projects, queue tasks, calendar notes, generated outputs, and recent notes. Create a weekly review and recommend next week's top 3 priorities.
```

## Queue Processor

```text
Read Claude.md and process all pending tasks in 05_Queue/Claude Queue.md. Create outputs in 04_Generated/Queue Outputs and move completed tasks into the Completed Tasks section with links.
```

## Project Health Monitor

```text
Read Claude.md and run the Project Health Monitor Workflow. Check all active projects. Flag anything stalled more than 7 days. Update the stalled project dashboard and create a project health report.
```

## Full Weekly Maintenance

```text
Run the full weekly maintenance sequence: process Capture, process Queue, run Project Health Monitor, then generate Weekly Review. Update dashboards and tell me the top 3 priorities for next week.
```

## Full Daily Maintenance

```text
Run daily maintenance: process Capture, check Queue, update Active Projects if needed, then create today's Morning Briefing.
```
