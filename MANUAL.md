# 📖 The Manual — How to Use Your System

Everything we built, and exactly how to run it day to day. Written to be followed step by step.

---

## 0. The 30-second version

1. Dump everything into **Capture** — don't sort.
2. Tell Claude **"Process Capture."**
3. Approve anything it stages for **Notion**.
4. Backup happens by itself every 10 minutes.

That's the whole system. Everything below is detail.

---

## 1. What you have (the map)

**Three separate vaults**, each backed up to its own private GitHub repo:

| Vault | Folder | For |
|---|---|---|
| **Main** | `~/Obsidian` | CMU + personal: capture, projects, grants, dissertation, journalism |
| **Power by Design** | `~/Power-by-Design` | Your own-name publishing |
| **Mercer** | `~/Mercer` | Marco Lewis fiction (pen-name — work in its own window) |

**Three layers** that make it "smart":
- **State (what's true):** Notion (operations) + Obsidian (knowledge).
- **Memory (what Claude recalls):** `Claude.md` + Claude's memory files + Git history.
- **Agents (who does the work):** Claude Code skills.

---

## 2. How you actually talk to it

You drive the system through **Claude Code** (this chat), pointed at a vault folder.

- For CMU/personal work → open Claude Code in **`~/Obsidian`**.
- For publishing → open it in **`~/Power-by-Design`**.
- For fiction → open it in **`~/Mercer`** (its own session — keeps the wall).

Obsidian (the app) is where you *read, write, and click around*. Claude Code is where you *give commands*. They share the same files.

---

## 3. The daily habit (5–10 min)

**Step 1 — Capture.**
Open `00_Capture/Capture.md`. Type everything on your mind below the `Raw Capture` line — tasks, ideas, notes from a meeting, a funding lead, a session to log. Messy is fine. **Do not sort.**

**Step 2 — Process.**
In Claude Code, say:
> *"Process Capture."*
Claude reads it and routes each item: knowledge → filed in Obsidian, operational items → staged for Notion, tasks → the Queue, dated items → the Calendar, and anything with youth PII → blocked (routed to your local intake vault instead).

**Step 3 — Approve Notion writes.**
Open `05_Queue/To Notion.md`. You'll see operational items staged for Notion (a partner touchpoint, a lane update, etc.). When they look right, say:
> *"Write the approved items in To Notion."*
The owning CMU skill writes them to Notion. Nothing goes to Notion without your OK.

**Step 4 (optional) — Morning Briefing.**
> *"Run the Morning Briefing."*
You get today's top priorities in `04_Generated/Morning Briefings/`.

**Step 5 — Backup.**
Nothing to do. The Git plugin auto-commits and pushes every 10 minutes.

---

## 4. Working a specific area (the control panels)

Each big area has a **control panel** in `01_Active/` — a launchpad, not a data store. Open it, copy a command, paste it to Claude.

| Area | Panel | Example command |
|---|---|---|
| CMU operations | [[CMU Operations]] | *"Weekly status — what's on fire."* |
| Smart Choices | [[Smart Choices Bright Futures]] | *"Draft a facilitator guide for Module 3."* |
| Grants | [[Grants Tracker]] + [[Grant Calendar]] | *"What grants are open for CMU right now?"* |
| Journalism | [[Connect the Dots]] | *"Outline this piece — hook, dots to connect, claims."* |

Each panel lists its own commands and routes them to the right skill.

---

## 5. The weekly routine

**Monday (10 min)**
**Step 1.** Open `Claude.md`, scroll to **Current Weekly Priorities**, fill it in (this refreshes Claude's active memory for the week).
**Step 2.** Say *"Run the Morning Briefing"* or *"Give me this week's status."*

**Friday or Sunday (20–30 min)**
**Step 1.** Say:
> *"Run full weekly maintenance."*
This runs Capture Processor → Queue Processor → Project Health Monitor → Weekly Review, and updates the dashboards.
**Step 2.** Review the Weekly Review in `04_Generated/Weekly Reviews/`. Log any big decisions to Notion.

See [[Operating Routine]] for the short version.

---

## 6. The Notion rule (important)

**Notion is the single source of truth for operations** — youth, sessions, outcomes, lanes, partners, decisions. Obsidian never keeps a second copy; it only points to Notion.

- Operational items you capture get **staged** in `05_Queue/To Notion.md`, then written by the owning skill **after you approve**.
- **PII firewall:** youth names, DOB, addresses never go into Notion *or* Obsidian. They stay in your local intake vault and are de-identified first.

Full detail: [[Notion Bridge]].

---

## 7. The three vaults & the wall

- **Main** and **Power by Design** are both your real name — fine to use in normal sessions.
- **Mercer is your pen name.** Always open it in **its own Claude Code session / Obsidian window** — never side by side with the others. The vaults, the GitHub repos, and even the commit author ("Marco Lewis") are kept separate on purpose.

To switch vaults in Obsidian: click the **vault name (bottom-left) → Open another vault → Open folder as vault**, then pick the folder.

---

## 8. Backup & restore

**It's automatic** — every vault commits + pushes to GitHub every 10 minutes.

**To check it's working:** open your GitHub repos (`RegRep`, `power-by-design-`, `Mercer-Marco-Lewis-`) — you'll see recent commits.

**To recover an old version of a note:** in Obsidian, open the **Git** plugin's *"View file history"* (or *"Open history for current file"*), pick the version, restore. Or ask Claude: *"Show me what [note] looked like yesterday."*

**Manual backup anytime:** Git plugin command **"Commit-and-sync"**, or tell Claude *"commit and push the vault."*

---

## 9. Teaching the system (so it improves)

- **Correct me once** → say *"Remember that…"* → it's saved to memory and applied in every future session.
- **A rule that keeps coming up** → put it in `Claude.md` (for the whole vault) or in the owning skill.
- **A workflow you repeat** → say *"Make a skill for this."*

This is what makes the agents "teachable" — corrections stick instead of evaporating.

---

## 10. Quick reference card

| I want to… | Do this |
|---|---|
| Get something out of my head | Type it in `00_Capture/Capture.md` |
| Sort/organize my capture | *"Process Capture."* |
| Send operational items to Notion | Approve them in `To Notion`, then *"write the approved items."* |
| Know today's priorities | *"Run the Morning Briefing."* |
| Run a CMU task | Open [[CMU Operations]], copy a command |
| Find/track grants | [[Grants Tracker]] · [[Grant Calendar]] |
| Write an article | Open [[Connect the Dots]] |
| Do the weekly cleanup | *"Run full weekly maintenance."* |
| Teach me something permanent | *"Remember that…"* |
| Back up | Automatic (every 10 min) |
| Start here each day | [[Home]] |

---

*Built 2026-06-17. If anything here drifts from how the system actually behaves, tell Claude and it'll fix the manual.*
