# Braiding Bot for CCRB (OAFC / Hogg / OJJDP)

Production-ready grant-extraction and braided-funding architecture for the **Court-Connected Recovery Bridge (CCRB)** program.

## Overview

The Braiding Bot operates as two coupled engines:

1. **Extraction Engine** — Builds one consistent CCRB "spine" from OAFC application and partner documents
2. **Controls Engine** — Forces non-duplication through cost objectives, explicit funder exclusions, and auditable timekeeping/reimbursement artifacts

## Deliverables

| File | Description |
|---|---|
| [`system_prompt.txt`](system_prompt.txt) | Production-ready Braiding Bot system prompt (no-hallucination rules, evidence discipline, required output sections) |
| [`ccrb_spine.md`](ccrb_spine.md) | One-page extracted OAFC program spine (identity, workflow, staffing, KPIs) |
| [`funding_map.md`](funding_map.md) | Braided funding map table (OAFC vs Hogg vs OJJDP) with explicit exclusions and non-duplication guardrails |
| [`interchangeability_matrix.md`](interchangeability_matrix.md) | Audit-shaped matrix: component, staff role, cost type, primary payer, split method, proof artifact, KPI |
| [`cost_allocation.md`](cost_allocation.md) | Chart-of-accounts labels, timesheet/LOE rules, documentation checklist |
| [`grant_skins.md`](grant_skins.md) | Universal spine paragraph (8-12 sentences) + 3 funder-specific skin paragraphs (OAFC, Hogg, OJJDP) |
| [`input_template.txt`](input_template.txt) | Filled input template example using OAFC details (Hogg/OJJDP as [NEEDED] placeholders) |
| [`open_questions.md`](open_questions.md) | 12 open questions / [NEEDED] items that must be resolved before full production use |
| [`diagrams/ccrb_workflow.mmd`](diagrams/ccrb_workflow.mmd) | Mermaid flowchart: CCRB workflow from court referral through YRC and workforce pathway |
| [`diagrams/timeline_year1.mmd`](diagrams/timeline_year1.mmd) | Mermaid Gantt chart: 12-month phased Year 1 timeline |

## Consortium

| Entity | Role |
|---|---|
| Grace Solutions International (GSI) | Prime / Fiscal Backbone |
| Credible Messengers United (CMU) | Subrecipient: Program Operations & Peer Recovery Delivery |
| Strategic Recovery Solutions (SRS) | Subrecipient: MOUD Navigation & Certified Family Partner Services |
| UTHealth Houston | Evaluation Partner |

## Compliance Anchors

- **OAFC**: Non-duplication (NOFA Para 140); reimbursement documentation (NOFA Para 531-537)
- **Federal (OJJDP)**: 2 CFR 200.403 (allowability), 200.405 (allocability), 200.303 (internal controls), 200.430 (salary documentation)
- **Hogg**: [NEEDED: exact initiative/RFP]

## Information Needed to Complete the Build

See [`open_questions.md`](open_questions.md) for the full list. Key items:
- Hogg Foundation opportunity name and restrictions
- OJJDP solicitation (program title/FY)
- MHPS and Peer Supervisor budget confirmation
- Staff split-funding decisions and allocation basis
