# RegRep - CCRB Braided Funding Documentation

Production-ready documentation for the **Braiding Bot** that supports the Court-Connected Recovery Bridge (CCRB) program's braided funding architecture across three payers: OAFC (state), Hogg Foundation (philanthropy), and OJJDP (federal).

## Overview

The CCRB is a court-to-community recovery continuum serving transitional age youth (ages 12-24) with opioid/substance use involvement, identified through Harris County juvenile and young adult courts. The program operates a 90-day stabilization model followed by 12 months of continuing care through a Youth Recovery Community (YRC).

The braided funding model follows the principle of **one spine, three lanes**:
- **OAFC**: Direct opioid-abatement service delivery
- **Hogg Foundation**: Non-clinical organizational capacity building
- **OJJDP**: Juvenile justice expansion + federal reporting/evaluation

## Repository Structure

```
docs/
  01-ccrb-program-spine.md        # Extracted CCRB program spine, workflow, and outcome targets
  02-braided-funding-map.md       # Three-lane funding map, interchangeability matrix, and grant skins
  03-cost-allocation-timekeeping.md  # Chart of accounts, timesheet rules, and documentation checklist
  04-open-questions.md            # Unresolved [NEEDED] items that block complete outputs
bot/
  system-prompt.md                # Ready-to-paste system prompt for the Braiding Bot
  input-template.md               # Input template with doc-tag structure and filled example
```

## Key Compliance Constraints

- All costs must be allowable, allocable, and documented per 2 CFR 200 (Uniform Guidance) once federal dollars enter
- Salary charges require records reflecting actual work performed (2 CFR 200.430); estimates alone are not sufficient
- DOJ Grants Financial Guide governs OJP recipients/subrecipients
- Subrecipient monitoring required per 2 CFR 200.332
- Hogg does not accept unsolicited proposals; funds only through posted opportunities
- No cost may be charged to more than one funder without a documented allocation method

## Consortium Partners

| Organization | Role |
|---|---|
| Grace Solutions International (GSI) | Prime applicant / fiscal agent |
| Credible Messengers United (CMU) | Program operations / peer services |
| Strategic Recovery Solutions (SRS) | MOUD linkage / Family Partner services |
| UTHealth Houston | Evaluation partner |

## Open Items

See [docs/04-open-questions.md](docs/04-open-questions.md) for the 8 unresolved items that must be provided before the Braiding Bot can produce complete outputs (notably: Hogg RFP identity, OJJDP solicitation, and staff role confirmations).
