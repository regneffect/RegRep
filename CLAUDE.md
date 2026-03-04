# RegRep - Project Memory

## Project Overview

RegRep is a curriculum development and intellectual property management system for the **SCBF 2.0** (Strengthening Communities and Building Futures) program. This repository tracks all curriculum modules, facilitator materials, and edition variants under version control.

---

## Curriculum Builder Mode Parameters

When generating or editing curriculum content, always apply these defaults unless overridden:

| Parameter | Default Value |
|-----------|--------------|
| **Setting** | Community-Based |
| **Session Duration** | 90 minutes |
| **Frameworks** | SCBF 2.0 framework (see standing rules on naming) |
| **Color Scheme** | Brand-consistent (defer to style guide when available) |

---

## Standing Rules

### 1. Framework Name Visibility
**CRITICAL:** Hide framework names from all participant-facing content. Frameworks (e.g., SCBF 2.0, underlying pedagogical models) may appear in facilitator guides and internal documentation only. Participant handouts, slides, and activity sheets must reference concepts without naming the framework.

### 2. Citation Placement - Harrington / NAPS
- **Harrington citations** and **NAPS (National AfterSchool Partnership Standards)** references must be placed according to the established citation format.
- Place citations in facilitator-facing materials, module footers, and reference appendices.
- Do not surface academic citations in participant-facing content.

### 3. STAR Prompt Structure
All reflection and discussion prompts follow the **STAR** format:
- **S**ituation - Set the context
- **T**ask - Define what was required
- **A**ction - Describe what was done
- **R**esult - Reflect on the outcome

Use STAR consistently across all editions and modules.

### 4. Edition Types and Adaptations

| Edition | Key Adaptations |
|---------|----------------|
| **Community-Based** | Default setting; flexible scheduling; community partner integration points |
| **School-Based** | TEKS (Texas Essential Knowledge and Skills) alignment required; maps activities to grade-level standards; follows school bell schedule constraints |
| **After-School** | Jacob's Law compliance required; compressed session formats; enrichment framing rather than instructional |

### 5. Session Duration by Edition

| Edition | Typical Duration |
|---------|-----------------|
| Community-Based | 90 minutes |
| School-Based | 45-50 minutes (class period) |
| After-School | 60 minutes |

---

## Repository Structure (Target)

```
RegRep/
  CLAUDE.md                    # This file - project memory
  .claude/
    commands/
      gen-module.md            # Custom command: generate a module draft
  modules/
    community-based/           # Community-Based edition modules
    school-based/              # School-Based edition modules
    after-school/              # After-School edition modules
  facilitator-guide/           # Facilitator Manual and supplements
  templates/                   # Shared content templates and source material
  style-guide/                 # Brand, formatting, and tone references
  references/                  # Harrington, NAPS, TEKS alignment maps
```

---

## Custom Commands

### `/gen-module` (planned)
Generate a draft curriculum module with parameters:
- `edition` - community | school | after-school
- `module_number` - integer
- `session_duration` - minutes (defaults per edition)
- `topic` - module topic/title

---

## Parallel Edition Generation

When generating multiple editions from a shared content source, use subagents in parallel:
1. Each agent receives the shared source content
2. Each applies edition-specific adaptations (TEKS for school, Jacob's Law for after-school)
3. Each respects the correct session duration constraints
4. All follow the standing rules above (framework name hiding, STAR prompts, citation placement)

---

## IP and Version Control Practices

- Every revision to SCBF 2.0 content, the Facilitator Manual, or any module is tracked via git.
- Use clear commit messages that reference the module/edition being changed.
- Maintain a clean audit trail for IP protection and funder reporting.
- Tag releases when editions are finalized (e.g., `v2.0-community-final`).
- Never commit participant PII or sensitive program data.

---

## Source Materials

### Youth and Young Adult Peer Support (YAYAPS) Facilitator Manual
- **Authors**: Jessi Davis & Darcy Kues
- **Publisher**: South Southwest MHTTC / UT Austin Steve Hicks School of Social Work
- **Funding**: SAMHSA Grant #6H79SM081778
- **Date**: May 2024
- **Structure**: 3-day intensive, 13 modules (~24 hours total)
- **Full Index**: `references/yayaps-facilitator-manual-index.md`
- **Adaptation Status**: Mapped for SCBF 2.0 edition generation
- **Citation Modules**: Harrington refs in Modules 3, 4, 5, 11; NAPS refs in Modules 3, 6, 9, 12

---

## Development Workflow

1. All work happens on feature branches.
2. Review diffs before merging to main.
3. Use `git diff` to compare revisions when auditing curriculum changes.
4. Roll back with confidence when revisions need to be undone.
