# Persona Pack — v1.1 (Integration + Create/Update)

## Purpose
Provide consistent personal context for planning — goals, routines, constraints.  
File used: **`personal_profile_core_file_v_1.md`**

This file also acts as the reference frame for 20/80 (Pareto) analysis:
- Long-term goals define what “high-leverage” means.
- Constraints and routines define what is realistically sustainable.

---

## Auto / Manual Logic
- If file exists → load automatically as context.  
- If missing/stale (>7 days) → prompt user:  
  “Use existing / Create now / Skip.”  
- Never invent persona facts.  
- If answers are vague → ask one clarifier and offer:  
  “Go deeper now or keep high-level and refine later?”

---

## Quick Inline Stub (if user skips full intake)
- **Role & context** — 1 line summary  
- **Top goals (3 bullets)** — short, measurable  
- **Constraints (3 bullets)** — time, energy, or resources  
- **Cadence** — weekly/biweekly patterns  

Save as minimal version of `personal_profile_core_file_v_1.md`.

---

## Commands
| Command | Description |
|----------|-------------|
| **@create_persona** | Run conversational intake (`personal_profile_collector.md`) or quick stub |
| **@update_persona** | Patch or re-run intake; overwrite existing file |
| **@use_persona {file}** | Load alternate persona file |
| **@persona_status** | Show presence + last updated info |
| **@weekly_sync** | Run weekly micro-update (delta prompts + save) |

---

## Maintenance Cadence
- Recheck persona every 7 days or after major change.  
- At weekly check-in, ask:  
  “Update Persona? Any new constraints, routines, or goals?”  
- Append small changelog at bottom of file (date + 1–3 bullets).
- During updates, explicitly note:
  - Which activities felt **high-impact** toward long-term goals.
  - Which felt like **noise / obligation** with low visible return.
  These tags feed into the 20/80 analysis in `@check-in` and `@reflect`.

---

## File Skeleton (summary)
```md
# Personal Profile — Core File (v1.x)
**Owner:** <name>  
**Preferred name:** <alias>  
**Last updated:** <YYYY-MM-DD>

## Key Areas
- Family
- Hobbies & Interests
- Long-Term Goals
- Military / Service
- Financials
- Sports & Health

### Notes & Assumptions
- Keep items short, factual, and actionable.
- Explicitly mark high-leverage activities vs. maintenance vs. noise when obvious.
```
