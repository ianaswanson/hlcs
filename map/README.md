# Map - Story Mapping Instrument

**Status:** Active Development in Story Mapper Product
**Schema:** v5 (Activities → Tasks → Details)

---

## What is Map?

The **Map** is the story mapping instrument. It answers "What exactly are we building?" by converting the broad unknown into scoped, buildable work organized by user journey.

---

## Core Questions

- What is the complete user journey?
- What are the key activities users perform?
- What tasks support each activity?
- What details must we build for each task?
- How do we slice this into releases?

---

## Source Methodologies

- **Jeff Patton** - User Story Mapping methodology
- **Vertical slicing** - Complete value in small increments
- **Release planning** - Progressive enhancement approach

See `reference/methodologies/jeff-patton-story-mapping.md` for details.

---

## Current Implementation

The Map instrument is actively being developed in:
- **Location:** `products/story-mapper/`
- **Status:** Discovery phase
- **Schema:** v5 (Activities → Tasks → Details with tags)
- **Capabilities:** Visualization, AI generation, structured storage

See Story Mapper product for current implementation details.

---

## Relationship to Other Instruments

```
COMPASS → TELESCOPE → MAP → BLUEPRINT
```

The Map:
- **Receives from Telescope:** Validated opportunities, user insights, prioritized problems
- **Feeds to Blueprint:** Scoped features, technical requirements, release plan

---

## Development Status

| Phase | Status |
|-------|--------|
| 1. Foundation | ✅ Complete |
| 2. Ian's Spin | ✅ Complete (v5 schema rigor) |
| 3. AI-Native Adaptation | 🔄 In Progress (Story Mapper) |
| 4. Schema Design | ✅ Complete (v5) |
| 5. Protocol Design | 🔄 In Progress |
| 6. Integration | ⏳ Not Started |
| 7. Implementation | 🔄 In Progress (Story Mapper) |

---

**Last Updated:** November 26, 2025
