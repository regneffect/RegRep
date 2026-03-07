# Data Dictionary: Unified Participant Record

> **Last Updated**: March 7, 2026
> **Purpose**: Every field in the unified participant record. Staff enter data once; it serves every reporting obligation across all funders and evaluation.

---

## Field Naming Convention

- Fields prefixed with `SCR_` = Screening data
- Fields prefixed with `SVC_` = Service interaction data
- Fields prefixed with `RCA_` = Recovery Capital Assessment data
- Fields prefixed with `RST_` = Restorative process data
- Fields prefixed with `OUT_` = System outcome data
- Fields prefixed with `DEM_` = Demographics
- Fields prefixed with `ENR_` = Enrollment and program status

---

## Demographics and Enrollment

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| DEM_participant_id | String (unique) | System-generated unique identifier | CMU Tracker, UTHealth | Auto-generated |
| DEM_first_name | String | Participant first name | CMU Tracker | RSPS at intake |
| DEM_last_name | String | Participant last name | CMU Tracker | RSPS at intake |
| DEM_dob | Date | Date of birth | CMU Tracker | RSPS at intake |
| DEM_age_at_enrollment | Integer | Age calculated at enrollment | CMU Tracker | Auto-calculated |
| DEM_gender | Categorical | Gender identity | CMU Tracker | RSPS at intake |
| DEM_race_ethnicity | Categorical (multi-select) | Race/ethnicity per federal reporting categories | CMU Tracker, OJJDP reporting | RSPS at intake |
| DEM_zip_code | String (5-digit) | Residential zip code | CMU Tracker | RSPS at intake |
| DEM_county | Categorical | Harris / Austin / Other | CMU Tracker | RSPS at intake |
| DEM_school_status | Categorical | Enrolled / Dropped out / GED / Graduated / Other | CMU Tracker | RSPS at intake |
| DEM_guardian_contact | String | Primary guardian name and phone | CMU Tracker | RSPS at intake |
| ENR_enrollment_date | Date | Date of CCRB enrollment | CMU Tracker | RSPS |
| ENR_referral_source | Categorical | HCJPD / Austin County JP / Court / School / Self / Other | CMU Tracker, JIMS2 | RSPS at intake |
| ENR_grant_cohort | Categorical | OAFC / OJJDP / Dual | CMU Tracker | Program Director |
| ENR_status | Categorical | Active-Stabilization / Active-YRC / Completed / Discharged / Lost to Follow-Up | CMU Tracker | RSPS |
| ENR_discharge_date | Date | Date of discharge or completion | CMU Tracker | RSPS |
| ENR_discharge_reason | Categorical | Completed / Moved / Incarcerated / Disengaged / Aged out / Other | CMU Tracker | RSPS |

---

## Screening Data

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| SCR_crafft_date | Date | Date CRAFFT 2.1+N administered | CMU Tracker | RSPS at intake |
| SCR_crafft_total | Integer (0-9) | CRAFFT 2.1+N total score | CMU Tracker, UTHealth | RSPS |
| SCR_crafft_car | Boolean | CRAFFT Car question response | CMU Tracker | RSPS |
| SCR_crafft_nicotine | Integer | Nicotine module score | CMU Tracker | RSPS |
| SCR_crafft_risk_level | Categorical | Low / Moderate / High (based on cutoff scores) | CMU Tracker | Auto-calculated |
| SCR_oud_suspected | Boolean | OUD suspected based on screening | CMU Tracker | RSPS |
| SCR_moud_eligible | Boolean | Age 16+ AND OUD suspected | CMU Tracker | Auto-calculated |
| SCR_moud_referral_date | Date | Date referred for MOUD assessment | CMU Tracker | RSPS (SRS) |
| SCR_moud_assessment_date | Date | Date MOUD clinical assessment completed | CMU Tracker | RSPS (SRS) |
| SCR_moud_linkage_days | Integer | Days from referral to assessment (target: ≤14) | CMU Tracker | Auto-calculated |
| SCR_literacy_tool | Categorical | WRAT-5 / TABE / Other | CMU Tracker | RSPS |
| SCR_literacy_score | Numeric | Literacy screening score | CMU Tracker | RSPS |
| SCR_literacy_grade_equiv | String | Grade-level equivalent | CMU Tracker | RSPS |
| SCR_risk_needs_tool | String | Name of validated risk/needs assessment used | CMU Tracker, OJJDP reporting | RSPS |
| SCR_risk_needs_score | Numeric | Risk/needs assessment score | CMU Tracker, OJJDP reporting | RSPS |
| SCR_risk_level | Categorical | Low / Moderate / High | CMU Tracker, OJJDP reporting | RSPS |

---

## Service Interaction Data

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| SVC_interaction_id | String (unique) | Unique ID per interaction | CMU Tracker | Auto-generated |
| SVC_date | Date | Date of service | CMU Tracker | Provider |
| SVC_type | Categorical | Recovery Coaching / MOUD Navigation / Family Conference / Restorative Circle / Mentoring / Crisis Response / Systems Advocacy / SCBF Session / Training | CMU Tracker | Provider |
| SVC_duration_minutes | Integer | Duration in minutes | CMU Tracker | Provider |
| SVC_provider_name | String | Staff member who delivered service | CMU Tracker | Provider |
| SVC_provider_org | Categorical | CMU / SRS / GSI | CMU Tracker | Provider |
| SVC_provider_credential | Categorical | RSPS / CFP / LCDC / Training Coordinator | CMU Tracker | Provider |
| SVC_modality | Categorical | In-person / Telehealth / Phone / Virtual / Home Visit | CMU Tracker | Provider |
| SVC_site | Categorical | CUP 1-4,8 / HCJPD / CASE / Cottage 6 / Home / School / Telehealth / Community / Other | CMU Tracker | Provider |
| SVC_cost_objective | Categorical | CO01-CO09 | CMU Tracker | Provider (per credential_stack_roster.md) |
| SVC_grant_charged | Categorical | OAFC / OJJDP / Hogg / None | CMU Tracker | Fiscal staff |
| SVC_narrative | Text | Brief service note | CMU Tracker | Provider |
| SVC_scbf_edition | Categorical | Community-Based / School-Based / After-School / N/A | CMU Tracker | Provider |
| SVC_scbf_session_number | Integer | Session number within SCBF curriculum | CMU Tracker | Provider |
| SVC_naloxone_distributed | Boolean | Was naloxone distributed during this interaction? | CMU Tracker | Provider |
| SVC_naloxone_kits_count | Integer | Number of kits distributed | CMU Tracker | Provider |
| SVC_milestone | Categorical | 7-day / 30-day / 60-day / 90-day / YRC monthly / None | CMU Tracker | Provider |

---

## Recovery Capital Assessment Data

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| RCA_assessment_date | Date | Date RCAM administered | CMU Tracker, UTHealth | RSPS |
| RCA_assessment_type | Categorical | Baseline / 30-day / 60-day / 90-day / YRC Follow-up | CMU Tracker | RSPS |
| RCA_personal_score | Numeric | Personal recovery capital subscale | CMU Tracker, UTHealth | RSPS |
| RCA_social_score | Numeric | Social recovery capital subscale | CMU Tracker, UTHealth | RSPS |
| RCA_community_score | Numeric | Community recovery capital subscale | CMU Tracker, UTHealth | RSPS |
| RCA_total_score | Numeric | Total RCAM score | CMU Tracker, UTHealth | Auto-calculated |
| RCA_housing_status | Categorical | Stable / Unstable / Homeless / Transitional | CMU Tracker | RSPS |
| RCA_education_status | Categorical | Enrolled / Re-enrolled / GED / Dropped / Graduated | CMU Tracker | RSPS |
| RCA_employment_status | Categorical | Employed / Seeking / Not seeking / In training / N/A (under 16) | CMU Tracker | RSPS |
| RCA_family_engagement | Categorical | High / Moderate / Low / None | CMU Tracker | CFP |

---

## Restorative Process Data

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| RST_process_id | String (unique) | Unique ID per restorative process | CMU Tracker | Facilitator |
| RST_date | Date | Date of restorative process | CMU Tracker | Facilitator |
| RST_type | Categorical | Circle / Conference / Mediation / Community Accountability | CMU Tracker | Facilitator |
| RST_harm_type | Categorical | Interpersonal / Family / Community / School / Justice-Related | CMU Tracker | Facilitator |
| RST_response_type | Categorical | Repair / Accountability / Reintegration / Prevention | CMU Tracker | Facilitator |
| RST_participants_count | Integer | Number of participants | CMU Tracker | Facilitator |
| RST_agreement_reached | Boolean | Was a restorative agreement reached? | CMU Tracker | Facilitator |
| RST_agreement_status | Categorical | In Progress / Completed / Breached / N/A | CMU Tracker | Facilitator |
| RST_facilitator_name | String | Facilitator (must have Layer 3 credential) | CMU Tracker | Facilitator |
| RST_satisfaction_score | Numeric (1-5) | Participant satisfaction rating | CMU Tracker, UTHealth | Post-process survey |

---

## System Outcome Data

| Field Name | Data Type | Description | Data Layer | Entered By |
|---|---|---|---|---|
| OUT_probation_status | Categorical | Active / Completed / Revoked / Transferred | JIMS2, CMU Tracker | HCJPD / Program Director |
| OUT_school_enrollment | Boolean | Currently enrolled in school/GED? | CMU Tracker | RSPS |
| OUT_school_attendance_rate | Numeric (%) | Monthly attendance rate (if enrolled) | CMU Tracker | RSPS / School liaison |
| OUT_new_charges | Boolean | Any new charges during program? | JIMS2, CMU Tracker | HCJPD / Program Director |
| OUT_new_adjudication | Boolean | New juvenile adjudication? | JIMS2, OJJDP reporting | HCJPD |
| OUT_new_conviction | Boolean | New criminal conviction? | JIMS2, OJJDP reporting | HCJPD |
| OUT_supervision_violation | Boolean | Violation of supervision terms? | JIMS2, OJJDP reporting | HCJPD |
| OUT_residential_placement | Boolean | Returned to residential placement/jail/prison? | JIMS2, OJJDP reporting | HCJPD |
| OUT_recidivism_24mo | Boolean | Meets OJJDP recidivism definition within 24 months of release? | JIMS2, UTHealth, OJJDP reporting | Program Director (calculated) |
| OUT_substance_use_status | Categorical | Abstinent / Reduced / Stable / Increased / Unknown | CMU Tracker, UTHealth | RSPS |
| OUT_moud_adherence | Categorical | Adherent / Partially Adherent / Non-Adherent / N/A | CMU Tracker | RSPS (SRS) |
| OUT_stabilization_completed | Boolean | Completed 90-day stabilization? | CMU Tracker | RSPS |
| OUT_yrc_engaged | Boolean | Engaged in YRC continuing care? | CMU Tracker | RSPS |
| OUT_yrc_months | Integer | Months of YRC engagement | CMU Tracker | Auto-calculated |
| OUT_workforce_pathway | Boolean | Entered RSPS apprenticeship pathway (18+)? | CMU Tracker | Program Director |
| OUT_naloxone_used | Boolean | Was distributed naloxone used to reverse an overdose? | CMU Tracker | RSPS / family report |

---

## Data Layer Reference

| Layer | System | Primary Users | Feeds |
|---|---|---|---|
| Layer 1: Justice System | JIMS2 | HCJPD, court officers | Court reporting, OJJDP justice outcomes |
| Layer 2: Program Operations | CMU Recovery Tracker | RSPS, CFP, Program Director | OAFC quarterly reports, internal QA |
| Layer 3: Evaluation | UTHealth Database | UTHealth team | Publications, OJJDP performance measures |
| Layer 4: Reporting Crosswalk | reporting_crosswalk.md | Program Director, fiscal staff | All funder reports |
