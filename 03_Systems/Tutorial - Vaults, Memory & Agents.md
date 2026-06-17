# Tutorial — Leveraging Your Vaults: Active Memory & Teachable Agents

How Notion, your three Obsidian vaults, Claude Code, and a few GitHub plugins combine into a system with **active memory** (it stays current and remembers across sessions) and **teachable agents** (they get better as you correct them).

---

## 1. The mental model — three layers

Don't think "Notion vs Obsidian." Think three layers, each with a job:

| Layer | Job | Where it lives |
|---|---|---|
| **State** — what's true right now | Canonical record | **Notion** (operational); **Obsidian** (knowledge/drafts); local intake vault (PII) |
| **Memory** — what the agent remembers | Carry context across sessions | **CLAUDE.md** (per vault) + **Claude memory files** + Git history |
| **Agents** — who does the work | Run the workflows | **Claude Code skills** + subagents |

Active memory = current **State** + agent **Memory** + **history**. Teachable agents = the **Agents** layer plus the instructions you give them.

---

## 2. Active memory — the four parts

### a) CLAUDE.md (per vault) — the always-on context
When you open a vault as your Claude Code folder, its `CLAUDE.md` is **auto-loaded** every session. That's your standing context: identity, voice, priorities, rules. You have one in each vault (main, Power-by-Design, Mercer).
- **Keep it current:** update "Current Weekly Priorities" in the main `Claude.md` every Monday. Old priorities = stale memory.

### b) Claude memory files — durable facts across conversations
Separate from the vaults, Claude keeps memory at `~/.claude/projects/.../memory/` with a `MEMORY.md` index loaded each session. These are one-fact-per-file notes (who you are, decisions, project state).
- **How facts get there:** say *"remember that…"* or I save them proactively when something is non-obvious and durable (e.g., the "Notion is canonical" decision is already saved).
- **This is what survives a brand-new chat.**

### c) Notion — canonical live state
Notion holds the authoritative operational record (lanes, youth, outcomes, partners). Your **Capture → process** loop keeps it current: dump in Obsidian, Claude routes operational items to Notion via the owning skill. That's "active" memory — the state updates as you work.

### d) Git history — time travel + backup
Version every vault with Git (see §4). This gives you: backup, sync across machines, and the ability to recall *what a note said last week*. Memory you can rewind.

---

## 3. Teachable agents — how to actually teach them

Your "agents" are **Claude Code skills** (in `~/.claude/skills/`) and the instructions around them. Four ways to teach:

1. **Edit the skill.** A skill is a folder with a `SKILL.md` of rules, examples, and routing. Your `cmu-orchestrator` is a taught agent — its governance pre-check (no PII, no person-level judgment, OJJDP partner-led) *is* the teaching. Add a rule → it's learned for every future run.
2. **CLAUDE.md standing rules.** Teach voice and policy per vault (e.g., "RIS internal-only," "Notion is canonical").
3. **Memory feedback.** When you correct me, say so — it's saved as a `feedback` memory and applied going forward. Corrections compound instead of evaporating.
4. **Make new agents.** The `skill-creator` skill scaffolds a new skill from a description. Build one when a workflow repeats.

> Rule of thumb: if you find yourself re-explaining the same thing, that's a teaching moment — it belongs in a skill, a CLAUDE.md rule, or a memory, not in a one-off chat.

---

## 4. The GitHub plugins to install (in Obsidian)

Open Obsidian → **Settings → Community plugins → Browse**. All are open-source (GitHub) and optional — the system works without them, but these add real leverage.

| Plugin | Why | Priority |
|---|---|---|
| **Obsidian Git** | Auto-commits each vault to a private GitHub repo: backup + history + cross-device sync. This is your "active memory" backbone. | ⭐ Essential |
| **Dataview** | Query notes like a database — live dashboards (e.g., all Active projects by risk) that update themselves. | High |
| **Templater** | Dynamic templates — auto-date notes, scaffold captures/articles. | Medium |
| **Zotero Integration** (or **Citations**) | Pull your Zotero library into notes for the dissertation. | High (dissertation) |
| **Smart Connections** | Local semantic "related notes" recall inside Obsidian. | Optional |

### Critical wall rule for Git
Use **a separate PRIVATE repo per vault** — never one shared repo:
- `obsidian-main` (private), `power-by-design` (private), `mercer` (private).
- The **Mercer repo must be private and not tied to your name** — co-mingling it with the others in one repo breaks the pen-name wall.

### Git setup (once per vault)
1. Install **Obsidian Git**.
2. Create a **private** GitHub repo for that vault.
3. In the vault folder: `git init`, add the remote, first commit/push (Claude can do this for you).
4. In the plugin settings: enable **auto-commit** (e.g., every 10 min) and **auto-push**.

---

## 5. The loop that ties it together

**Daily**
1. Dump into `00_Capture/`.
2. Run the Capture Processor → knowledge stays in Obsidian, operational items stage for Notion, PII gets blocked.
3. Git auto-commits (history).

**Weekly**
1. Update weekly priorities in `Claude.md` (refresh active memory).
2. Run Weekly Review + Project Health.
3. Log decisions to Notion; save durable facts to memory.

**Teaching moments (ongoing)**
- Correct me → it becomes a memory.
- A rule repeats → it goes into a skill or CLAUDE.md.
- A workflow repeats → `skill-creator` makes it an agent.

That's the whole machine: **Notion = live state, Obsidian = knowledge + capture, Git = history, Claude memory + skills = an agent that remembers you and gets better.**
