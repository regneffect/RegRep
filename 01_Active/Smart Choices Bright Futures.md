# Smart Choices, Bright Futures — Control Panel

> **Notion is canonical** for operational data (program sessions, outcomes, youth, lane status). This note is a *launchpad and knowledge home*, not a data store. See [[Notion Bridge]].

Priority 3 in [[Claude]]. An 8-module substance-use education program taught across Harris County juvenile Community Unit Probation (CUP) sites. This panel is where you run the program and where its curriculum/evaluation work lives.

---

## What lives where

| Item | Home | Owner |
|---|---|---|
| Program sessions, outcomes, enrolled youth | **Notion** (Sessions / Outcomes / Youth) | `cmu-case-tracker` |
| Program lane status / decisions | **Notion** (Lanes / Decisions) | `cmu-executive-dashboard` |
| Curriculum, lesson plans, facilitator guides, evaluation design | **Obsidian** (`02_Resources` = canonical curriculum; `04_Generated` = drafts) | knowledge work |
| Funder/compliance reports | **Notion** data → report drafted in `04_Generated` | `cmu-case-tracker` |
| Funding fit & language | [[Grants Tracker]] | `grant-master` / `rss-scorer` |

Operational records never get duplicated here. Curriculum and drafts *do* live in Obsidian — that's knowledge, not operational data.

---

## The 8 Modules

Fill in the real module titles (left as slots so nothing is invented):

1. Module 1 — `[title]`
2. Module 2 — `[title]`
3. Module 3 — `[title]`
4. Module 4 — `[title]`
5. Module 5 — `[title]`
6. Module 6 — `[title]`
7. Module 7 — `[title]`
8. Module 8 — `[title]`

> Want me to draft a module map / lesson outlines? Use the launchpad below — drafts save to `04_Generated/`.

## Program components

- Screening · Assessment · Treatment planning
- Licensed counseling **when indicated**
- Group and one-on-one support
- Youth-centered education

⚠️ **Screening, assessment, treatment planning, and clinical decisions are made by licensed staff — never by Claude or this panel.** This panel organizes the work around them.

---

## Command launchpad

Paste a line to Claude. Routes to the owning skill; side-effectful steps pause for your go.

**Sessions & outcomes** → `cmu-case-tracker` (de-identified; PII never in Notion)
```text
Log a Smart Choices session / outcome check-in for a CUP site.
```
```text
Generate the Smart Choices funder/compliance report from the outcomes data.
```

**Program lane** → `cmu-executive-dashboard`
```text
Update the Smart Choices lane / log a program decision.
```

**Curriculum & evaluation** (Obsidian knowledge work → `04_Generated/`)
```text
Draft a facilitator guide / lesson plan / evaluation design for Module [n].
```

**Funding** → `grant-master` + `rss-scorer`
```text
What funding fits Smart Choices? Score this RFA for SUD-prevention fit.
```

> Spans skills or unsure? Say **"route this through the CMU kernel"** → `cmu-orchestrator`.

---

## Funding posture (governance)

- **CMU is not the clinical-SUD applicant.** Until the HHSC outpatient CDTF license (26 TAC Ch. 564) is secured, any clinical-SUD-service application routes as **GSI-lead / SRS-clinical / CMU-mentoring** — never CMU as the clinical applicant.
- **OJJDP must be partner-led.** If Smart Choices rides on an OJJDP proposal, a separate 501(c)(3) is the applicant and CMU is the operating/mentoring program (see [[Grant Calendar]]). Open queue item: confirm Smart Choices allowability as an OJJDP budget line.

---

## Work areas Claude can help with

Curriculum refinement · lesson plans · evaluation design · facilitator guides · reports · referral automation · outcome dashboards · grant/funder language · replication/licensing strategy. Outputs save to `04_Generated/`; finished curriculum graduates to `02_Resources/`.

## Governance reminders (always on)

- **No person-level judgment.** Clinical/screening decisions = licensed staff.
- **PII firewall.** No youth names/DOB in Notion or Obsidian; de-identify via the local intake vault.
- **Side-effectful = explicit go.**
- **Federation wall** — CMU operational domain only.
