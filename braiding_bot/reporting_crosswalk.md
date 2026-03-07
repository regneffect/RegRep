# Reporting Crosswalk

> **Last Updated**: March 7, 2026
> **Purpose**: Maps each funder's reporting requirements to specific fields in the data_dictionary.md. When a funder asks a question, this crosswalk tells you exactly which data fields answer it.

---

## OJJDP Semi-Annual Performance Reports

**Schedule**: Jan-Jun due July 30; Jul-Dec due Jan 30 (via JustGrants)

| OJJDP Reporting Requirement | Data Dictionary Field(s) | Source System | Notes |
|---|---|---|---|
| Number of youth served | ENR_enrollment_date, ENR_status | CMU Tracker | Count of unique participants with ENR_status ≠ Discharged during period |
| Youth demographics (age, race, gender) | DEM_age_at_enrollment, DEM_race_ethnicity, DEM_gender | CMU Tracker | Federal reporting categories required |
| Risk level at intake | SCR_risk_level, SCR_risk_needs_tool | CMU Tracker | Must specify validated tool used |
| Prerelease case planning (90+ days) | ENR_enrollment_date, SVC_date (first service), SVC_site = HCJPD | CMU Tracker, JIMS2 | Calculate days between first service at HCJPD and release date |
| Evidence-based programming delivered | SVC_type, SVC_scbf_edition, SVC_scbf_session_number | CMU Tracker | Document which EBPs delivered and dosage |
| Case management services | SVC_type, SVC_duration_minutes, SVC_provider_name | CMU Tracker | All service contacts during period |
| Family engagement | RCA_family_engagement, SVC_type = Family Conference | CMU Tracker | Count of family contacts and engagement level |
| Recidivism (24-month) | OUT_recidivism_24mo, OUT_new_adjudication, OUT_new_conviction, OUT_supervision_violation, OUT_residential_placement | JIMS2, UTHealth | OJJDP definition: return to residential placement/jail/prison with new adjudication/conviction OR supervision violation within 24 months |
| School enrollment/attendance | OUT_school_enrollment, OUT_school_attendance_rate | CMU Tracker | Pre/post comparison |
| Employment (18+) | RCA_employment_status | CMU Tracker | Pre/post comparison for age-eligible |
| Substance use outcomes | OUT_substance_use_status, OUT_moud_adherence | CMU Tracker | Pre/post comparison |
| Program completion rate | OUT_stabilization_completed, ENR_status | CMU Tracker | 90-day completion percentage |
| Evaluation progress | UTHealth deliverables | UTHealth Database | Status of quasi-experimental study |
| MOA/MOU status | See moa_mou_tracker.md | N/A | Must remain in effect; report any changes |
| Financial report (SF-425) | Fiscal records | GSI accounting | Separate from performance report |

---

## OAFC Quarterly Reports

**Schedule**: Quarterly via TxGMS [DATA NEEDED: specific submission dates]

| OAFC Reporting Requirement | Data Dictionary Field(s) | Source System | Notes |
|---|---|---|---|
| Youth enrolled this quarter | ENR_enrollment_date | CMU Tracker | New enrollments during quarter |
| Clinical assessment within 14 days | SCR_moud_linkage_days | CMU Tracker | Target: 85% within 14 days |
| Evidence-based treatment initiation | SVC_type, SVC_date (first EBP session) | CMU Tracker | Target: 75% |
| 90-day stabilization completion | OUT_stabilization_completed | CMU Tracker | Target: 70% |
| 12-month YRC engagement | OUT_yrc_engaged, OUT_yrc_months | CMU Tracker | Target: 50% |
| Naloxone kits distributed | SVC_naloxone_kits_count | CMU Tracker | Target: 150+ annually |
| Family engagement rate | RCA_family_engagement | CMU Tracker | Target: 80% |
| MOUD referrals and linkage | SCR_moud_referral_date, SCR_moud_assessment_date | CMU Tracker | For ages 16+ with suspected OUD |
| Service contacts by type | SVC_type (aggregated) | CMU Tracker | Breakdown by category |
| Workforce pipeline outputs | OUT_workforce_pathway | CMU Tracker | RSPS apprenticeships at 18+ |
| Budget expenditures | Fiscal records | GSI accounting | Must demonstrate no duplicate reimbursement |
| Strategy alignment evidence | Program documentation | Program Director | Alignment with A02/I04 strategy |

---

## Hogg Foundation Annual Narrative

**Schedule**: Annual narrative report [DATA NEEDED: specific due dates after August 2026 award]

| Hogg Reporting Requirement | Data Dictionary Field(s) | Source System | Notes |
|---|---|---|---|
| Community engagement evidence | Crowdsource channel tracker data | crowdsource_channel_tracker.md | Youth Design Labs, FRAC, CREM sessions held + outputs |
| Capacity building activities completed | SVC_type = Training, SVC_cost_objective = CO08 | CMU Tracker | Training sessions, SOPs developed, manuals produced |
| Staff trained / credentials earned | credential_stack_roster.md updates | credential_stack_roster.md | New credentials, training completions |
| Partnership development | moa_mou_tracker.md, SPFL data | moa_mou_tracker.md | New/renewed partnerships, partner feedback |
| Mental health/well-being impact | RCA_total_score (aggregate trends), qualitative narratives | CMU Tracker, qualitative data | Non-clinical impact on community mental health |
| Budget expenditure report | Fiscal records | GSI accounting | Must stay within 30% of operating budget cap |
| Strategic focus area progress | Program documentation | Program Director | Community, Partnerships, RIE, Policy |
| Challenges and adaptations | Program Director narrative | N/A | Candid assessment of obstacles and responses |

---

## UTHealth IRB / Evaluation Data

**Schedule**: Per IRB protocol and evaluation timeline

| UTHealth Data Requirement | Data Dictionary Field(s) | Source System | Notes |
|---|---|---|---|
| De-identified participant records | All DEM_, SCR_, SVC_, RCA_, OUT_ fields (de-identified) | CMU Tracker → UTHealth Database | Must follow IRB data sharing protocol |
| Baseline assessments | SCR_crafft_total, RCA_total_score, SCR_risk_needs_score | CMU Tracker | Collected at enrollment |
| Follow-up assessments | RCA_ fields at 30/60/90/YRC intervals | CMU Tracker | Longitudinal tracking |
| Treatment group assignment | ENR_grant_cohort + random assignment protocol | UTHealth Database | For quasi-experimental design |
| Comparison group data | [DATA NEEDED: source for comparison group] | JIMS2 / HCJPD | Matched comparison from non-participating youth |
| Recidivism outcomes (24-month) | OUT_recidivism_24mo and component fields | JIMS2 | Primary outcome measure |
| SCBF 2.0 pre/post survey data | Instrument-specific fields (see instrument_registry.md) | CMU Tracker | For SCBF effectiveness evaluation |
| Satisfaction/process data | RST_satisfaction_score, participant surveys | CMU Tracker | Process evaluation data |

---

## Cross-Funder Field Usage Map

Shows which fields serve multiple funders (fields that appear in more than one funder's reporting requirements):

| Field | OJJDP | OAFC | Hogg | UTHealth | Count |
|---|---|---|---|---|---|
| ENR_enrollment_date | X | X | | X | 3 |
| ENR_status | X | X | | X | 3 |
| SCR_crafft_total | X | X | | X | 3 |
| SCR_risk_level | X | | | X | 2 |
| SVC_type | X | X | X | X | 4 |
| RCA_family_engagement | X | X | X | X | 4 |
| OUT_stabilization_completed | X | X | | X | 3 |
| OUT_recidivism_24mo | X | | | X | 2 |
| OUT_substance_use_status | X | X | | X | 3 |

**Note**: These high-usage fields must be entered accurately ONCE — errors propagate across all funder reports.
