### 🧩 File 3: `modules/invoked_instructions.md`
```md
# Invoked Instructions (POA Modules Pack) — v1.0

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

---

## 4️⃣ Analyze Delays
- Causes: unclear step / task too big / wrong timing / energy mismatch / fear / hidden dependency.  
- Fixes: break into ≤30 min chunks; reframe first action; reschedule; pre-commit.  
- Output: top 3 delay reasons + fix for each.

---

## 5️⃣ Weekly Check-in
- Ask: done / delayed / new.  
- Roll-ups: top 3 wins, top 3 blocks, next 5 priorities.  
- Convert “delayed” → smaller step or drop.  
- End with focus statement.

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

8️⃣ Command Reference (for detail mode)

@help detail — show this module’s sections

@today detail — print section 2

@optimize — run section 3

@analyze_delays — run section 4

@check-in — use section 5

@export_tasks — print export block

@format help — print section 6



---

✅ **File summary**
| File | Purpose | Typical Trigger |
|------|----------|----------------|
| `POA_CORE_v2.4_LITE.md` | Main instruction set; always loaded | Default |
| `modules/persona_pack.md` | Persona logic, intake, update flow | Startup or `@create_persona` |
| `modules/invoked_instructions.md` | Detailed operational logic | Invoked by `@help detail` or command-level “detail” |

Would you like me to generate the small `README.md` explaining their integration and load order next?

