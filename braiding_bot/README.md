# Braiding Bot: Grant Management & Operational Audit Engine

> **Three grants. Three organizations. One integrated system.**

The Braiding Bot is the operational infrastructure documentation for a three-organization consortium (GSI, CMU, SRS) applying for and managing three grants simultaneously. It ensures the consortium can manage, report on, and audit the braided grant system without double-billing, compliance gaps, or invisible labor.

---

## The Consortium

| Entity | Role |
|---|---|
| **Grace Solutions International (GSI)** | Lead applicant, fiscal agent, grant administration (all three grants) |
| **Credible Messengers United (CMU)** | Sub-grantee: peer recovery delivery, SCBF 2.0, CM mentoring, data collection |
| **Strategic Recovery Solutions (SRS)** | Sub-grantee: MOUD/MAT, telehealth, behavioral health, CFP services |
| **UTHealth Houston** | Evaluation partner (OJJDP) |
| **HCJPD** | System partner: referrals, facility access, probation supervision |

## The Three Grants

| Grant | Funder | Amount | Period | Status |
|---|---|---|---|---|
| OJJDP FY25 SCA Youth Reentry (Cat 2) | DOJ/OJJDP | $750,000 | 36 months | SF-424 due Mar 30; JustGrants due Apr 6 |
| OAFC Long-term CORE | TX Comptroller/OAFC | $749,565 | 3 years | Deadline passed Feb 10 — confirm status |
| Hogg TCBRI | Hogg Foundation | $15K-$75K/yr | 2 years | **Due March 13** |

---

## File Architecture

### Tier 1: Strategy and Planning
| File | Description |
|---|---|
| [`README.md`](README.md) | This file — overview, architecture, deadline dashboard |
| [`grant_skins.md`](grant_skins.md) | Grant specs, scoring criteria, skin paragraphs in each funder's language |
| [`funding_map.md`](funding_map.md) | Master cost allocation matrix — every dollar has one home |
| [`ccrb_spine.md`](ccrb_spine.md) | Service delivery model spine all three narratives draw from |
| [`braiding_crowdsourcing_architecture.md`](braiding_crowdsourcing_architecture.md) | BUIDM/ICDA framework: 5 braiding dimensions x 6 crowdsourcing channels |

### Tier 2: Audit Engine
| File | Description |
|---|---|
| [`braid_integrity_checklist.md`](braid_integrity_checklist.md) | Monthly checklist across five braiding dimensions |
| [`crowdsource_channel_tracker.md`](crowdsource_channel_tracker.md) | Quarterly tracker for six participatory design channels |
| [`convergence_audit_matrix.md`](convergence_audit_matrix.md) | 6x5 matrix: channels x dimensions, FIRING/DORMANT/BROKEN status |
| [`credential_stack_roster.md`](credential_stack_roster.md) | Living roster of staff credentials, layers, deployment sites |
| [`billing_capture_audit.md`](billing_capture_audit.md) | Monthly tracker: documented interactions vs. billed — gap = invisible labor |

### Tier 3: Data Architecture
| File | Description |
|---|---|
| [`data_dictionary.md`](data_dictionary.md) | Every field in the unified participant record |
| [`reporting_crosswalk.md`](reporting_crosswalk.md) | Funder reporting requirements mapped to data dictionary fields |
| [`instrument_registry.md`](instrument_registry.md) | Every screening tool, assessment, and survey with administration protocols |

### Tier 4: Compliance and Risk
| File | Description |
|---|---|
| [`language_audit.md`](language_audit.md) | Flagged terms and approved replacements for federal language environment |
| [`funder_firewall.md`](funder_firewall.md) | Cost allocation rules, shared cost percentages, documentation requirements |
| [`moa_mou_tracker.md`](moa_mou_tracker.md) | Status of every required partnership document |

### Tier 5: IP and Publication
| File | Description |
|---|---|
| [`ip_registry.md`](ip_registry.md) | CMU intellectual property inventory with attribution requirements |
| [`publication_pipeline.md`](publication_pipeline.md) | Academic articles, columns, conferences, data sharing protocols |
| [`open_questions.md`](open_questions.md) | All unresolved items requiring human decision — 16 items, 3 critical |

---

## Deadline Dashboard

| Grant | Action | Deadline | Status |
|---|---|---|---|
| Hogg TCBRI | Fluxx registration | March 6, 2026 | PASSED — confirm completed |
| **Hogg TCBRI** | **Proposal submission** | **March 13, 2026** | **6 DAYS** |
| OAFC CORE | Application | February 10, 2026 | PASSED — confirm status |
| OJJDP SCA | SAM.gov registration | March 16, 2026 | 9 days |
| OJJDP SCA | SF-424 in Grants.gov | March 30, 2026 | 23 days |
| OJJDP SCA | Full app in JustGrants | April 6, 2026 | 30 days |

---

## Conventions

- `[DECISION NEEDED]` — requires human judgment from Reggie
- `[DATA NEEDED]` — requires specific information (dollar amounts, staff names, confirmation)
- All unresolved items are tracked in [`open_questions.md`](open_questions.md)
- Monthly audits use [`braid_integrity_checklist.md`](braid_integrity_checklist.md)
- Quarterly audits use [`convergence_audit_matrix.md`](convergence_audit_matrix.md)
