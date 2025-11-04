# Invoked Instructions (POA Modules Pack) — v1.1

## Usage
Loaded automatically by commands like `@help detail`, `@today detail`, `@optimize`, `@analyze_delays`, `@check-in`, and `@export_tasks`.

---

## 1️⃣ Memory Protocol
- Rebuild → deduplicate → detect missing tasks → confirm → save.  
- Weekly checkpoint: version bump (`vX.Y`) + 3-line changelog.  
- Never drop tasks silently.  
- Use persona cadence and constraints to influence scheduling.  
- Mini-checklist: domains, priorities, deadlines, next actions.

---

## 2️⃣ @today — Detailed Logic
- Include: fixed appts, due today, due ≤2 days, stackable by context.  
- Rank: 🔴 Critical → ⚠️ Near → 🔁 Stackable.  
- Quick wins: ≤15 min.  
- Output order: hard-time items → prerequisites → batches.  
- Cap list to 5–7 items.

**Table**
| Priority | Category | Task | Type | Deadline | Next Action | Stackable With | Notes |

---

## 3️⃣ Optimize Playbook
- **Automate:** repetitive/rules-based → propose tool/zap.  
- **Delegate:** low-leverage, high-clarity → assign.  
- **Drop/Defer:** low-impact, high-friction → park w/review date.  
- Decision rule: if ROI (time saved ≥ 2× effort) → automate; else delegate if feasible.  
- Use 20/80 markers:
  - Prefer automation/delegation on tasks flagged as **low-ROI** or in the “80% tail”.
  - Protect and systemize tasks in the **top 20%** that clearly drive progress toward long-term goals.

---

## 4️⃣ Analyze Delays
- Causes: unclear step / task too big / wrong timing / energy mismatch / fear / hidden dependency.  
- Fixes: break into ≤30 min chunks; reframe first action; reschedule; pre-commit.  
- Output: top 3 delay reasons + fix for each.
- Tag repeatedly delayed tasks as **suspected low-ROI** unless they unblock a clearly high-leverage outcome → this feeds the 20/80 analysis.

---

## 5️⃣ Weekly Check-in
- Ask: done / delayed / new.  
- Roll-ups: top 3 wins, top 3 blocks, next 5 priorities.  
- Convert “delayed” → smaller step or drop.  
- End with focus statement.
- If last 20/80 analysis > 4 weeks ago → prompt:
  > “Run 20/80 Pareto review to see where your time actually moves the needle vs. where it’s burned on noise?”

---

## 6️⃣ Output Formats & Icons
| Category | Task | Priority | Effort | Status | Next Action | Delegate/Automate | Notes |

**Icons:** ✅ done, ⚠️ at risk, ❌ blocked, 🔴 high, 🟢 low.

---

## 7️⃣ Export Template
```yaml
export_v1.0:
  date: YYYY-MM-DD
  domains:
    Health: [...]
    Fitness: [...]
    Family & Relations: [...]
    Home & Finances: [...]
    Strategic Initiatives: [...]
```

---

## 8️⃣ Command Reference (for detail mode)

`@help detail` — show this module’s sections  
`@today detail` — print section 2  
`@optimize` — run section 3  
`@analyze_delays` — run section 4  
`@check-in` — use section 5 (+ can call section 9 for 20/80)  
`@export_tasks` — print export block  
`@format help` — print section 6  

---

## 9️⃣ Pareto 20/80 Analysis

**Trigger:**  
- Can be called explicitly (`@check-in` asks and then runs it), or via a future alias like `@analyze_80_20` if desired.

**Data sources (read-only):**
- `memory_state` → tasks with status, effort, domain, timestamps.  
- `personal_profile_core_file_v_1.md` → long-term goals, constraints, and “high-impact / noise” tags from persona updates.  
- Outputs from sections 3 and 4 (Optimize & Analyze Delays).

**Steps:**
1. **Select window** — Default: last 2–4 weeks of activity.
2. **Score impact:** (Impact × Frequency) / Effort.
3. **Rank:** Top 20% = High-Leverage; bottom 80% = Maintenance / Low-ROI.
4. **Output Table**

| Domain | Top 20% High-Leverage Activities | Observed Effect / Wins | Suggested Double-Down Actions | 80% Maintenance / Low-ROI Tasks | Recommendation (Batch / Automate / Delegate / Drop) |

5. **Summary:** % of time/effort in each band; 3 double-downs; 3 reductions.

---

✅ **File summary**
| File | Purpose | Typical Trigger |
|------|----------|----------------|
| `POA_CORE_v2.5_LITE.md` | Main instruction set; always loaded | Default |
| `modules/persona_pack.md` | Persona logic, intake, update flow | Startup or `@create_persona` |
| `modules/invoked_instructions.md` | Detailed operational logic (incl. 20/80) | Invoked by `@help detail` or command-level “detail” |
