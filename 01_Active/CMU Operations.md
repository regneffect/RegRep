# CMU Operations — Control Panel

> **Notion is canonical.** This note is a *launchpad and working view*, not a data store. Lanes, youth, sessions, outcomes, partners, and decisions live in Notion and are written only by the owning CMU skills under their governance pre-check. Nothing operational is duplicated here. See [[Notion Bridge]].

Priority 1 in [[Claude]]. This is the daily cockpit for running CMU — it tells you *what to run* and *who owns it*, then the skill does the work in Notion.

---

## What lives where

| Operational data | Canonical home (Notion) | Owning skill |
|---|---|---|
| Lanes / project status / decisions | Lanes, Decisions | `cmu-executive-dashboard` |
| Youth, sessions, outcomes, sites, mentors | Youth / Sessions / Outcomes / Sites / Mentors | `cmu-case-tracker` |
| Partners, touchpoints, MOUs | Partners, Touchpoints | `cmu-partner-relations` |
| Funding pipeline | (tracked in [[Grants Tracker]] + skill) | `grant-master` |

This vault holds only: capture, knowledge, drafts, grants pipeline, and these launch commands.

---

## Operational cadences

### Daily
- Dump into [[Capture]]; process it (ops items auto-stage to Notion via [[To Notion]]).
- Optional: Morning Briefing.

### Weekly (Monday)
- Update **Current Weekly Priorities** in [[Claude]].
- Run the board/status pull.

### Weekly (Fri/Sun)
- Capture Processor → Queue Processor → Project Health Monitor → Weekly Review.

### Monthly / as triggered
- HCJPD compliance report; outcome check-ins (30/60/90/180/365); PO #1 billing; funder reports.

---

## Command launchpad

Paste a line to Claude. Each routes to the owning skill, which writes to Notion (side-effectful steps pause for your go).

**Executive / lanes** → `cmu-executive-dashboard`
```text
Weekly status — what's on fire, what's overdue, Monday agenda.
```
```text
Update the [lane name] lane in Notion / log this decision.
```

**Case & outcomes** → `cmu-case-tracker`  (de-identified; PII never in Notion)
```text
Log a Quest session / new intake / outcome check-in.
```
```text
Generate the HCJPD compliance report / caseload snapshot.
```

**Partners** → `cmu-partner-relations`
```text
Log a touchpoint with [partner] / draft follow-up / update the partner record.
```

**Funding** → `grant-master` (+ [[Grants Tracker]])
```text
Run the funding scan — what's open or reopening for CMU.
```

**Billing** → `hcjpd-po1-audit`
```text
Finalize Derek Reed's PO #1 timesheet into the billable hours report.
```

**Funding fit** → `rss-scorer` (CMU mode)
```text
Score this RFA against the RSS rubric — where will we lose points.
```

> Not sure who owns it, or it spans skills? Say **"route this through the CMU kernel"** → `cmu-orchestrator`.

---

## CMU Operations sub-areas (pointers, status lives in Notion lanes)

- **Quest mentoring** — HCJPD / Leadership Academy youth
- **Smart Choices, Bright Futures** — 8-module SUD education across CUP sites
- **Neighborhood expansion** — detention-connected → youth near Cottage 6
- **School-based prevention / violence interruption**
- **Passport program** — early development
- **Partnerships** — Harris County, juvenile probation, schools, CPS/foster care

For current status on any of these, pull the lane: *"What's the status of the [sub-area] lane?"* → `cmu-executive-dashboard`.

---

## Governance reminders (always on)

- **No person-level judgment.** Risk, eligibility, discharge, violation response = human staff decisions, never a skill or this panel.
- **PII firewall.** No youth names/DOB/addresses in Notion or Obsidian. PII stays in the local intake vault, de-identified before export.
- **Side-effectful = explicit go.** Sending, filing, submitting, or changing standing config pauses for your OK. Drafting/organizing doesn't.
- **Federation wall.** This is the CMU operational domain only — not the Power by Design or Mercer publishing stacks.
