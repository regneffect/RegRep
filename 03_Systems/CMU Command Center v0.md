---
type: system
system: CMU Command Center
version: v0 (structure-first, manual)
created: 2026-06-19
canonical-store: Notion 🛤️ Lanes DB
related: "[[Notion Bridge]]"
source: "Agent Engineering Manual (prompt caching / context engineering / advisor strategy talk)"
---

# CMU Command Center — v0

**What v0 is:** the *structure*, locked. Seven program-level objective cards, one Lane Brief per objective, reconciled against the Notion Lanes already in place. No automation yet (manual evidence packets). This is the Obsidian thinking layer — promotion to Notion happens under governance via `cmu-executive-dashboard`.

**Design sentence (the target architecture, not v0):**
> Stable cached context + tool router + programmatic extraction + living lane briefs + advisor review + Reggie approval.

v0 builds the **living lane briefs** rung only. The rest is v1+.

---

## 1. Altitude reconciliation (the one decision that gates Notion)

The live 🛤️ Lanes DB holds **initiatives**, not program objectives:

| Live Lane | Status (per memory) | Rolls up to objective |
|---|---|---|
| HCJPD PO #1 Billing | Active | Quest + Operations |
| Recovery Housing / Hotel Project | — | **#3 Hotel / Recovery Housing** (is itself an objective) |
| TCMI (Texas Credible Messenger Institute) | — | Partnerships / Quest |
| OJJDP SCA Youth Reentry (ReDirect) | Active (partner-led) | #4 Funding & Grants |
| OJJDP FY25 Expanding Youth Access | Closed | #4 Funding & Grants |
| Safe Schools · INF-2026-0147 | Closed (rule 5) | #4 Funding & Grants |

**The 7 objectives sit one altitude above these.** Two ways to wire it in Notion (Reggie picks — see §6):
- **Option A (recommended):** the 7 objectives become 7 program-level rows in the same Lanes DB; add a self-relation `Parent Objective` so existing initiative-lanes roll up. One DB, one source of truth.
- **Option B:** keep Lanes as-is; express the 7 objectives only as a grouped/saved view. Lighter, but objectives have no Money/Risk/Next-Move of their own.

Either way: **no new parallel operational table** (Notion Bridge rule).

---

## 2. The 7 objectives

1. **Smart Choices Delivery** — SCBF curriculum across CUP sites. Aggregate already wired (`📊 Smart Choices (SCBF) Aggregate`).
2. **Quest Youth Engagement** — HCJPD PO #1 case-management lane. Aggregate wired (`📊 Quest (PO #1 Case-Mgmt) Aggregate`).
3. **Hotel / Recovery Housing Project** — capital + operations.
4. **Funding & Grants** — pipeline (OJJDP SCA active/partner-led; OJJDP FY25 + Safe Schools closed).
5. **Partnerships & Contracts** — owned by `cmu-partner-relations` (Partners + Touchpoints).
6. **Public Voice / Journalism** — op-eds, media, Red Sea voice. (Drafting lives in Obsidian, not Notion.)
7. **Staff & Operations** — staffing, invoicing/billing throughput, internal capacity.

---

## 3. Lane Brief schema → Notion Lanes field map

| Lane Brief field | Notion Lanes field | Status |
|---|---|---|
| Current Objective | (page body / `Notes`) | exists |
| Money Impact | `Money Attached` | exists |
| Next Actions | `Next Move` + `Deadline` + `Owner` | exists |
| Risks | `Risk Level` + `Risk Notes` | exists |
| Decisions Made | `Related Decisions` (relation) | exists |
| Last Updated | `Last Reviewed` | exists |
| Lifecycle | `Status` (Active/Dev/Concept/Exploration/Paused/Closed) | exists |
| Staff burden | `Staff Burden` | exists |
| **Health** (🟢🟡🔴⚪🔵) | — | **GAP** — add `Health` select |
| **Advisor Review** | — | **GAP** — add `Advisor Review` select |
| Source Trail | (page body) | convention only |
| Open Questions / Blockers | (page body) | convention only |

Two small schema adds (`Health`, `Advisor Review`) close the gap. Both are additive/non-destructive — but still a schema change, so gated in §6.

---

## 4. The seven lane briefs (best current state)

> Honesty rule (from the manual): *fail closed, not fake confident.* Program aggregates currently read **zero** (Sessions/Referrals/IIPs are pre-population), so most Key Numbers are marked Gray. Do not invent figures.

### 4.1 Smart Choices Delivery
- **Health:** ⚪ Gray — aggregate wired, data pre-population
- **Objective:** Deliver SCBF curriculum across CUP sites; track completions.
- **Key Numbers:** served / sessions / completions = 0 (infra pre-population)
- **Source Trail:** `📊 Smart Choices (SCBF) Aggregate`, attendance tracker
- **Advisor Review:** Not needed
- **Next Action:** Reggie/Mentors — begin live session logging via cmu-case-tracker — TBD

### 4.2 Quest Youth Engagement
- **Health:** ⚪ Gray
- **Objective:** PO #1 case-management contacts (1:1, peer support, court support).
- **Open Question:** Quest aggregate `by_site` is meaningless (case-mgmt sessions aren't site-bound) — re-group view by Session Type or Mentor.
- **Source Trail:** `📊 Quest (PO #1 Case-Mgmt) Aggregate`
- **Advisor Review:** Not needed
- **Next Action:** fix Quest view grouping — TBD

### 4.3 Hotel / Recovery Housing Project
- **Health:** ⚪ Gray — populate from lane page
- **Objective:** Stand up recovery housing / hotel operation.
- **Advisor trigger:** money + contracts + capital stack → **Advisor required** before any go/no-go.
- **Source Trail:** Lane `Recovery Housing / Hotel Project`
- **Next Action:** pull current state into brief — TBD

### 4.4 Funding & Grants
- **Health:** 🟡 Yellow — one active partner-led grant; two lanes closed
- **Key Numbers:** OJJDP SCA Youth Reentry = Active (Penitents Grace applicant, CMU operating); OJJDP FY25 = Closed (deadline lapsed); Safe Schools = Closed (rule 5)
- **Compliance flag:** OJJDP permitted only partner-led, not CMU-as-direct-applicant (orchestrator rule 4, amended).
- **Advisor Review:** required on any new grant fit decision
- **Next Action:** run pipeline scan for next eligible opportunity — TBD

### 4.5 Partnerships & Contracts
- **Health:** ⚪ Gray
- **Objective:** Keep partner relationships warm; log touchpoints.
- **Owner skill:** `cmu-partner-relations` (Partners + Touchpoints DBs)
- **Source Trail:** Touchpoint round-trip proven (HCJPD partner)
- **Next Action:** populate active partner list + last-contact dates — TBD

### 4.6 Public Voice / Journalism
- **Health:** ⚪ Gray
- **Objective:** Op-eds / media in Red Sea voice.
- **Compliance flag:** public statements → **Advisor required** + Reggie approval before any external publish.
- **Note:** drafting lives in Obsidian (not an operational Notion lane unless tracking a specific placement).

### 4.7 Staff & Operations
- **Health:** 🟢 Green (billing process proven)
- **Key Numbers:** HCJPD PO #1 April 2026 = 163.5h billable (SCBF split out, Quest kept in PO #1)
- **Source Trail:** Lane `HCJPD PO #1 Billing`, hcjpd-po1-audit skill
- **Advisor Review:** Confirmed (Angela Audit pattern)
- **Next Action:** next monthly PO #1 audit when raw timesheet lands — recurring

---

## 5. Conventions

**Health vs Status:** Health is the at-a-glance signal (🟢🟡🔴⚪🔵). Status is lifecycle. They are different axes — a lane can be `Active` + 🔴 Red.

**Advisor trigger rules** — call the advisor before any objective touching: money, contracts, grants, legal/compliance, youth/client-sensitive data, funder-facing language, public statements, partner commitments, or conflicting evidence.

**Human approval:** the agent may summarize / draft / extract / flag / recommend / update internal status. It may **not** send external email, make commitments, change official records, approve spending, submit grants, or publish — without Reggie. *AI prepares the decision; Reggie makes it.*

**PII firewall:** no youth PII in Notion or Obsidian — it stays in the local encrypted intake vault and is de-identified first.

---

## 6. Promotion-to-Notion checklist (GOVERNANCE-GATED — needs Reggie)

Nothing below is done yet. Each is a side-effectful Notion write requiring the cmu-orchestrator pre-check + confirmation pause:

- [ ] **Decide altitude:** Option A (objectives as parent lanes + self-relation) vs Option B (grouped view only)
- [ ] **Schema add:** `Health` select + `Advisor Review` select on Lanes DB
- [ ] **Create 7 objective lane rows** (if Option A); relate existing initiatives as children
- [ ] **Backfill** each objective page body with its Lane Brief (§4)
- [ ] **Fix** Quest aggregate view grouping (Session Type / Mentor, not Site)

---

## 7. Out of scope for v0 (→ v1+)

Tool router, programmatic extraction (code-filtering Gmail/Sheets/transcripts), compaction automation, operator console (cache hit rate / cost / context telemetry), advisor automation, scheduled briefs. v0 is structure only — these bolt on once the lane briefs are live in Notion.
