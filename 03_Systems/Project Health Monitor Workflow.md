# Project Health Monitor Workflow

## Purpose

Find projects that have stalled for more than 7 days and flag them.

## Claude Instructions

1. Read `Claude.md`.
2. Read `01_Active/Active Projects.md`.
3. Check every active project.
4. Look for the `Last Updated` field.
5. If a project has not been updated in more than 7 days, mark it as stalled.
6. Identify the likely reason it stalled.
7. Recommend the smallest next action.
8. Update the project risk field.
9. Generate a stalled project report.

## Output Location

Save report to:

`04_Generated/Project Health/YYYY-MM-DD Project Health Report.md`

Also update:

`09_Dashboards/Stalled Project Dashboard.md`

## Output Format

```markdown
# Project Health Report — YYYY-MM-DD

## Stalled Projects

| Project | Days Since Update | Likely Issue | Smallest Next Action | Risk |
|---|---:|---|---|---|

## Projects Moving Well

## Projects at Risk

## Recommended Intervention

## One Thing to Kill, Pause, or Archive
```
