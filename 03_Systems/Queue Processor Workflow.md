# Queue Processor Workflow

## Purpose

Process tasks dropped into `05_Queue/Claude Queue.md`.

## Claude Instructions

1. Read `Claude.md`.
2. Read `05_Queue/Claude Queue.md`.
3. Identify pending tasks.
4. Process each task one at a time.
5. Create the requested output.
6. Save each output in `04_Generated/Queue Outputs/`.
7. Move completed task to the Completed Tasks section.
8. Link the generated output under the completed task.
9. If a task is unclear, create a clarification note instead of guessing wildly.
10. If a task is high-value and incomplete, create a next-action recommendation.

## Output Location

Save each completed output as:

`04_Generated/Queue Outputs/YYYY-MM-DD - Task Title.md`

## Completion Format

In `Claude Queue.md`, move task to Completed Tasks and add:

```markdown
Completed:
Output:
Next action:
```
