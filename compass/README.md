# Compass - Strategic Direction Instrument

**Status:** Compound instrument with two components
**Components:** Destination (Canvas) + Course (Roadmap)

---

## What is Compass?

The **Compass** establishes strategic direction for all product decisions. It's a **compound instrument** with two parts:

```
COMPASS
  ├── DESTINATION (Canvas)  - Business case/thesis
  └── COURSE (Roadmap)      - Execution plan
```

**DESTINATION** answers: "Where are we positioned in the market? What's our business thesis?"

**COURSE** answers: "How do we get there? What's our strategic execution plan?"

Together, they provide complete strategic direction before committing to tactical work.

---

## Folder Structure

```
compass/
├── README.md                    (this file - Compass overview)
├── destination/
│   ├── knowledge-layer.md      (Canvas methodology)
│   ├── schema.json             (Canvas structure)
│   └── examples/               (Canvas examples)
└── course/
    ├── knowledge-layer.md      (Roadmap methodology)
    ├── schema.json             (Roadmap structure)
    ├── README.md               (Course overview)
    └── examples/               (Roadmap examples)
```

---

## DESTINATION (Canvas)

**Business case and market positioning**

### Core Questions
- Who exactly are we serving?
- Is the problem big enough to build a business around?
- Why would they choose us over alternatives?
- Why is NOW the right time?
- How do we make money?
- What must be true for this to work?

### Structure
| Section | Question |
|---------|----------|
| **Vision** | What's the pitch? |
| **Customer** | Who exactly? |
| **Problem** | What hurts? Is it big enough? |
| **Solution** | How do we solve it? |
| **Unique Value** | Why us? Hard to copy? |
| **Timing** | Why now? |
| **Market** | Where are we playing? |
| **Revenue** | How do we make money? |
| **Truths & Bets** | What's real vs assumed? |

### Source Methodologies
- Geoffrey Moore (Crossing the Chasm) - Vision template, beachhead
- Sequoia Capital - Pitch deck framework, "Why Now"
- Bill Gross - Timing as #1 success factor
- Lean Canvas / BMC - Problem/Solution/Revenue structure
- B2B Sales Theory - Buyer/User/Champion distinction
- Moat Theory - Hard-to-copy framework

**See:** `destination/knowledge-layer.md`

**Example:** `destination/examples/trello-destination.json` - Canonical example used across all HLCS methodology artifacts

---

## COURSE (Roadmap)

**Strategic execution plan with time-horizoned tactics**

### Core Questions
- What's our strategic vision? (5+ years)
- How will we compete and win? (2-5 years)
- What user behavior changes prove we're on track? (1-2 years)
- What are we doing now, next, later? (quarterly)

### Structure
| Section | Timeframe |
|---------|-----------|
| **Vision** | 5+ years (referenced from Destination) |
| **Strategy** | 2-5 years (diagnosis, principles, focus, tradeoffs) |
| **Goals** | 1-2 years (user behavior change evidence) |
| **Now/Next/Later** | Quarterly (deliverables/solutions/investigations) |

### Source Methodologies
- Jeff Patton - Vision as human transformation
- Rumelt (Good Strategy/Bad Strategy) - Diagnosis/guiding policy/coherent action
- Lafley/Martin (Playing to Win) - Strategy as compass
- Melissa Perri (Escaping the Build Trap) - Outcomes over outputs
- Jeff Gothelf - User behavior metrics
- OKRs - Measurable goals framework
- Jenna Bastok - Now/Next/Later time horizons
- 18F Product Guide - Roadmap theory

**See:** `course/knowledge-layer.md`

---

## Relationship Between Components

**DESTINATION** (Canvas) is the business thesis:
- Defines market position and competitive strategy
- Establishes foundational Vision
- Determines business model and revenue approach
- Stable - changes only with pivots

**COURSE** (Roadmap) is the execution plan:
- References Vision from Destination
- Translates thesis into strategy and goals
- Defines time-horizoned tactical work
- Dynamic - updated quarterly

**Flow:** Destination provides strategic constraints → Course plans execution within those constraints

---

## Relationship to Other Instruments

```
COMPASS (Destination + Course)  → "Where and how?"
    ↓
TELESCOPE (Discovery)           → "What opportunities exist?"
    ↓
MAP (Story Map)                 → "What exactly are we building?"
    ↓
BLUEPRINT (Architecture)        → "How do we build it?"
    ↓
SHIP (Product)                  → "What we're shipping"
```

The Compass provides strategic direction that constrains and informs all downstream work.

---

## Development Status

### DESTINATION (Canvas)

| Phase | Status |
|-------|--------|
| 1. Foundation | ✅ Complete |
| 2. Ian's Spin | ✅ Complete |
| 3. AI-Native Adaptation | ✅ Complete |
| 4. Schema Design | 🔄 In Progress |
| 5. Protocol Design | ⏳ Not Started |
| 6. Integration | ⏳ Not Started |
| 7. Implementation | ⏳ Not Started |

### COURSE (Roadmap)

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
