# Instrument Registry

> **Last Updated**: March 7, 2026
> **Purpose**: Every screening tool, assessment, and survey used in CCRB. For each: what it measures, when administered, which data layer it feeds, and current version status.

---

## Screening and Assessment Instruments

### 1. CRAFFT 2.1+N (Substance Use Screening)

| Field | Detail |
|---|---|
| **Full Name** | Car, Relax, Alone, Forget, Friends, Trouble — Version 2.1 with Nicotine module |
| **What It Measures** | Substance use risk among adolescents; screens for problematic use patterns including nicotine |
| **Population** | Ages 12-21 (extended to 24 for CCRB TAY population) |
| **Administration Point** | Intake (Day 1-7); re-screening at 90-day completion if clinically indicated |
| **Administered By** | RSPS at intake |
| **Scoring** | Total score 0-9; ≥2 = positive screen warranting further assessment |
| **Data Layer** | CMU Tracker → UTHealth → OJJDP reporting → OAFC reporting |
| **Data Dictionary Fields** | SCR_crafft_date, SCR_crafft_total, SCR_crafft_car, SCR_crafft_nicotine, SCR_crafft_risk_level |
| **Current Version** | 2.1+N |
| **Source/License** | Boston Children's Hospital; free for clinical use |
| **Funder Alignment** | OJJDP (validated screening); OAFC (SUD identification); UTHealth (baseline data) |

### 2. RCAM — Recovery Capital Assessment Measure (Youth-Adapted)

| Field | Detail |
|---|---|
| **Full Name** | Recovery Capital Assessment Measure — Youth Adaptation |
| **What It Measures** | Personal, social, and community recovery capital; holistic assessment of recovery-supporting resources |
| **Population** | Youth and young adults in recovery |
| **Administration Point** | Baseline (Day 1-7); 30-day; 60-day; 90-day; YRC follow-ups (quarterly) |
| **Administered By** | RSPS |
| **Scoring** | Subscale scores (personal, social, community) + total score |
| **Data Layer** | CMU Tracker → UTHealth |
| **Data Dictionary Fields** | RCA_assessment_date, RCA_assessment_type, RCA_personal_score, RCA_social_score, RCA_community_score, RCA_total_score |
| **Current Version** | [DATA NEEDED: confirm version of youth adaptation] |
| **Source/License** | [DATA NEEDED: licensing/attribution for youth adaptation] |
| **Funder Alignment** | OJJDP (outcome measurement); OAFC (recovery tracking); UTHealth (longitudinal analysis) |

### 3. Validated Risk/Needs Assessment Tool

| Field | Detail |
|---|---|
| **Full Name** | [DATA NEEDED: specific tool — e.g., YLS/CMI, SAVRY, or other validated tool] |
| **What It Measures** | Risk of reoffending and criminogenic needs |
| **Population** | Justice-involved youth |
| **Administration Point** | Intake; OJJDP requires validated risk/needs assessment for all Category 2 participants |
| **Administered By** | [DATA NEEDED: RSPS or HCJPD probation officer?] |
| **Scoring** | [DATA NEEDED] |
| **Data Layer** | JIMS2 → CMU Tracker → OJJDP reporting |
| **Data Dictionary Fields** | SCR_risk_needs_tool, SCR_risk_needs_score, SCR_risk_level |
| **Current Version** | [DATA NEEDED] |
| **Funder Alignment** | OJJDP (mandatory for Category 2 — must use validated tool to identify moderate-to-high-risk youth) |

### 4. Literacy Screening (WRAT-5 / TABE)

| Field | Detail |
|---|---|
| **Full Name** | Wide Range Achievement Test — 5th Edition / Test of Adult Basic Education |
| **What It Measures** | Reading level, literacy, grade-level equivalency |
| **Population** | All CCRB enrollees |
| **Administration Point** | Intake (Day 1-7) |
| **Administered By** | RSPS |
| **Scoring** | Standard scores; grade-level equivalents |
| **Data Layer** | CMU Tracker |
| **Data Dictionary Fields** | SCR_literacy_tool, SCR_literacy_score, SCR_literacy_grade_equiv |
| **Current Version** | WRAT-5 or TABE [DATA NEEDED: confirm which is primary] |
| **Funder Alignment** | OAFC (education-linked recovery narrative); OJJDP (educational reentry planning) |

---

## Program Surveys and Feedback Instruments

### 5. SCBF 2.0 Pre/Post Surveys

| Field | Detail |
|---|---|
| **Full Name** | Smart Choices Bright Futures 2.0 — Pre/Post Knowledge and Attitude Survey |
| **What It Measures** | Psychometric change in substance use knowledge, decision-making attitudes, and behavioral intentions before and after SCBF curriculum delivery |
| **Editions** | Community-Based, School-Based, After-School (separate survey versions per edition) |
| **Administration Point** | Pre: first SCBF session; Post: final SCBF session |
| **Administered By** | SCBF facilitator (CMU) |
| **Scoring** | [DATA NEEDED: scoring rubric] |
| **Data Layer** | CMU Tracker → UTHealth |
| **Current Version** | 2.0 |
| **IP Owner** | CMU (see ip_registry.md) |
| **Funder Alignment** | OJJDP (evidence-based programming evidence); OAFC (treatment quality); UTHealth (effectiveness evaluation) |

### 6. Restorative Process Participant Satisfaction Survey

| Field | Detail |
|---|---|
| **Full Name** | Restorative Process Participant Satisfaction Survey |
| **What It Measures** | Participant experience of fairness, voice, respect, and satisfaction with restorative process outcomes |
| **Administration Point** | Immediately following each restorative circle/conference |
| **Administered By** | Facilitator (distributed; self-completed by participant) |
| **Scoring** | 5-point Likert scale; aggregate satisfaction score |
| **Data Layer** | CMU Tracker → UTHealth |
| **Data Dictionary Fields** | RST_satisfaction_score |
| **Current Version** | [DATA NEEDED: version number] |
| **Funder Alignment** | OJJDP (program quality); Hogg (community engagement evidence) |

### 7. Facilitator Debrief Form (OSCR Channel)

| Field | Detail |
|---|---|
| **Full Name** | Post-Session Facilitator Debrief Form |
| **What It Measures** | Facilitator observations: what worked, what was adapted, why, outcome |
| **Administration Point** | After each SCBF, MET/CBT, A-CRA, or restorative session |
| **Administered By** | Facilitator (self-completed, 10 minutes) |
| **Scoring** | Qualitative + structured categories |
| **Data Layer** | POGA Library → curriculum version control |
| **Current Version** | [DATA NEEDED] |
| **Funder Alignment** | Hogg (CQI/capacity building); OAFC (fidelity monitoring); OJJDP (evidence-based methodology) |

### 8. Partner Survey (SPFL Channel)

| Field | Detail |
|---|---|
| **Full Name** | Systems Partner Feedback Survey |
| **What It Measures** | Partner satisfaction, coordination quality, referral pathway efficiency, system-level barriers |
| **Administration Point** | Quarterly (15-minute digital instrument) |
| **Administered By** | Program Director (distributed to HCJPD, courts, schools, SRS, community providers) |
| **Scoring** | Likert scales + open-ended responses |
| **Data Layer** | crowdsource_channel_tracker.md |
| **Current Version** | [DATA NEEDED] |
| **Funder Alignment** | OJJDP (agency collaboration evidence); Hogg (partnership infrastructure); OAFC (court coordination) |

### 9. Youth Design Lab Output Template

| Field | Detail |
|---|---|
| **Full Name** | Youth Design Lab Session Documentation Template |
| **What It Measures** | Youth co-design inputs, journey maps, prototypes, recommendations |
| **Administration Point** | Each Youth Design Lab session (quarterly) |
| **Administered By** | Youth Design Lab facilitator |
| **Scoring** | Qualitative — structured template for design artifacts |
| **Data Layer** | crowdsource_channel_tracker.md → curriculum version control |
| **Current Version** | [DATA NEEDED] |
| **Funder Alignment** | Hogg (community voice); OJJDP (participatory action research); OAFC (program quality) |
| **IRB Note** | [DECISION NEEDED: if outputs feed UTHealth evaluation, IRB review may be required] |

### 10. Family Advisory Feedback Form

| Field | Detail |
|---|---|
| **Full Name** | Family Recovery Advisory Circle Feedback Form |
| **What It Measures** | Family member input on repair conferencing, caregiver support needs, service accessibility |
| **Administration Point** | Each FRAC session (bi-monthly) |
| **Administered By** | Certified Family Partner (distributed; self-completed) |
| **Scoring** | Mixed methods: Likert scales + open-ended |
| **Data Layer** | crowdsource_channel_tracker.md |
| **Current Version** | [DATA NEEDED] |
| **Funder Alignment** | Hogg (community engagement — 15 points); OAFC (family engagement KPI); OJJDP (reentry best practice) |

---

## Instrument Administration Schedule Summary

| Instrument | Intake | Day 30 | Day 60 | Day 90 | YRC Quarterly | Post-Session |
|---|---|---|---|---|---|---|
| CRAFFT 2.1+N | X | | | As needed | | |
| RCAM (youth-adapted) | X | X | X | X | X | |
| Risk/Needs Assessment | X | | | | | |
| Literacy Screening | X | | | | | |
| SCBF 2.0 Pre/Post | Pre at start | | | | | Post at end |
| RJ Satisfaction Survey | | | | | | X |
| Facilitator Debrief | | | | | | X |
| Partner Survey | | | | Quarterly | Quarterly | |
| Youth Design Lab Template | | | | Quarterly | Quarterly | |
| Family Advisory Feedback | | | | Bi-monthly | Bi-monthly | |
