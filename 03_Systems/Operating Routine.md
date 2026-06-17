# Operating Routine — Daily & Weekly

The habit that keeps the whole system alive. Capture → process → Notion → auto-backup. Don't sort by hand; let the system do it.

---

## Daily (5–10 min)

1. **Capture** — dump everything into [[Capture]]. Messy is fine. No sorting.
2. **Process** — tell Claude: *"Process Capture."* Knowledge files into Obsidian, operational items stage to Notion in [[To Notion]], PII gets blocked.
3. **Approve** — glance at [[To Notion]]; give the go on staged Notion writes (the owning skill does the write).
4. *(Optional)* **Morning Briefing** — *"Run the Morning Briefing."*
5. **Backup** — automatic. The Git plugin commits + pushes every 10 min. Nothing to do.

## Weekly — Monday (10 min)

1. Update **Current Weekly Priorities** in [[Claude]] (this refreshes active memory).
2. Run weekly status / Morning Briefing.

## Weekly — Friday or Sunday (20–30 min)

1. *"Run full weekly maintenance"* → Capture Processor → Queue Processor → Project Health Monitor → Weekly Review.
2. Log decisions to Notion; save durable facts to memory.

---

## Teaching moments (ongoing)

- Correct me once → say *"remember that…"* → it's saved to memory and applied going forward.
- A rule keeps coming up → put it in `CLAUDE.md` or the owning skill.
- A workflow repeats → make it a skill (`skill-creator`).

## The three layers (reminder)

- **State:** Notion (canonical operations) + Obsidian (knowledge/drafts).
- **Memory:** `CLAUDE.md` + Claude memory files + Git history.
- **Agents:** skills + workflows.

## Vault discipline

- Work each vault in **its own session** — especially **Mercer** (pen-name wall).
- Auto-backup (Git plugin "Git" by Vinzent03) runs in all three vaults.
- Backups: `~/Obsidian`→RegRep · `~/Power-by-Design`→power-by-design- · `~/Mercer`→Mercer-Marco-Lewis-.
