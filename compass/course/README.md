# Course - Roadmap (Part of Compass)

**Status:** Phase 1-2 Complete (Foundation + Ian's Spin)
**Schema:** v0.1 - See schema.json

---

## What is Course?

**Course** is the roadmap component of the **Compass** instrument. The Compass itself is compound:

**COMPASS = DESTINATION + COURSE**

- **DESTINATION** (Canvas) = Business case/thesis - where you're positioned
- **COURSE** (Roadmap) = Execution plan - how you'll get there

Course answers "How do we get there?" by defining the strategic execution path from vision to delivered value through time-horizoned planning.

---

## Core Questions

- What is our strategic roadmap?
- How do vision and strategy translate to execution?
- What are our measurable outcomes/goals?
- What do we do now, next, later?
- How do we track progress toward vision?

---

## Artifacts in This Folder

- **knowledge-layer.md** - Complete methodology synthesis (ontology, evaluation, procedures)
- **schema.json** - Roadmap structure definition (JSON Schema)
- **examples/** - Sample roadmap artifacts
  - **trello-course.json** - Canonical example (complements Destination)

---

## Source Methodologies

| Element | Source(s) |
|---------|-----------|
| Vision | Jeff Patton - "What SHOULD be" vs "what CAN be" |
| Strategy | Good Strategy/Bad Strategy (Rumelt) + Playing to Win (Lafley/Martin) - Strategy as compass |
| Goals/Outcomes | Escaping the Build Trap (Perri) + OKRs + Jeff Gothelf - User behavior change evidence |
| Now/Next/Later | Jenna Bastok + Ian's rigor (language progression + artifact types) |
| Roadmap Theory | 18F Product Guide |

See `../../reference/methodologies/` for detailed source materials:
- `strategy-as-compass-rumelt-lafley-martin.md`
- `now-next-later-jenna-bastok-ian-rigor.md`

---

## Course Structure

| Section | Timeframe | Purpose |
|---------|-----------|---------|
| **Vision** | 5+ years | Referenced from Destination - inspirational "why" |
| **Strategy** | 2-5 years | Diagnosis, guiding principles, focus areas, trade-offs |
| **Goals** | 1-2 years | User behavior change evidence (not outputs) |
| **Now/Next/Later** | Quarterly | Time-horizoned execution (deliverables/solutions/investigations) |

**Key insight:** Strategy is compass (decision framework), not destination list (initiatives)

---

## Relationship to Destination

**Vision** lives on Destination (Canvas) as foundational element. Course references it for context but doesn't own it. This avoids duplication while keeping the roadmap connected to core purpose.

**Strategy** lives on Course because it's about execution planning, not business thesis.

**Flow:** Destination defines where you're positioned → Course plans how to get there

---

## Relationship to Other Instruments

**Resolved:** Course is part of Compass, not separate.

```
COMPASS (Destination + Course) → TELESCOPE → MAP → BLUEPRINT → SHIP
```

**Course outputs feed downstream:**
- **To Telescope:** LATER column defines problem spaces to investigate
- **To Map:** NEXT→NOW transition identifies solutions ready for story mapping
- **To Blueprint:** Goals define outcomes to architect for
- **To Ship:** NOW column defines what's being built this quarter

---

## Development Status

| Phase | Status |
|-------|--------|
| 1. Foundation | ✅ Complete |
| 2. Ian's Spin | ✅ Complete |
| 3. AI-Native Adaptation | ⏳ Not Started |
| 4. Schema Design | ✅ Complete |
| 5. Protocol Design | ⏳ Not Started |
| 6. Integration | ⏳ Not Started |
| 7. Implementation | ⏳ Not Started |

---

**Last Updated:** November 27, 2025
