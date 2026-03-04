Generate a draft curriculum module for the SCBF 2.0 program.

## Parameters
- **Edition**: $ARGUMENTS (provide: community, school, or after-school)
- If no edition is specified, default to community-based.

## Instructions

1. Read CLAUDE.md for all standing rules before generating content.
2. Determine the edition type and apply the correct adaptations:
   - **community**: 90-minute session, community partner integration points
   - **school**: 45-50 minute session, TEKS alignment required, map to grade-level standards
   - **after-school**: 60-minute session, Jacob's Law compliance, enrichment framing
3. Use the STAR prompt structure (Situation, Task, Action, Result) for all reflection/discussion prompts.
4. **Never** include framework names (SCBF 2.0, etc.) in participant-facing content.
5. Place Harrington/NAPS citations only in facilitator-facing sections and reference appendices.
6. Output the module as a structured draft with these sections:
   - Module Title and Number
   - Learning Objectives
   - Materials Needed
   - Facilitator Preparation Notes (internal - may reference frameworks)
   - Session Outline with timing
   - Activities and participant handout content (no framework names)
   - STAR Reflection Prompts
   - Assessment / Check for Understanding
   - Citations and References (facilitator appendix)
7. Save the generated file to the correct edition subfolder under `modules/`.
