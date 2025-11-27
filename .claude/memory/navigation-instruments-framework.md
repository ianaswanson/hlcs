# Navigation Instruments Framework
## HLCS Architecture for Product Development

**Status:** Active framework
**Last Updated:** November 26, 2025

---

## Overview

The Navigation Instruments Framework extends HLCS (Human-LLM Collaborative Systems) with a nautical metaphor for product development. These four instruments form a directed pipeline from vision to implementation, each producing structured artifacts that feed downstream processes.

### The Core Principle

Just as a ship's captain uses different instruments for different purposes—compass for direction, telescope for sighting, map for route planning, blueprint for vessel design—product development requires distinct instruments for distinct phases.

Each instrument is an **HLCS implementation**: a structured collaboration between human and AI to produce an artifact that downstream AI/human processes can reliably consume.

---

## The Four Navigation Instruments

```
Compass → Telescope → Map → Blueprint → [Ship]
   ↑___________________________________________|
                 (feedback loop)
```

| Instrument | Question It Answers | When You Use It | Output |
|------------|---------------------|-----------------|--------|
| **Compass** | Where are we trying to go? | Always (true north) | Vision, strategy, outcomes |
| **Telescope** | What's out there? What opportunities? | Discovery phase | Opportunity trees, problem space maps |
| **Map** | What exactly are we building? | Planning phase | User story map |
| **Blueprint** | How will we build it? | Design phase | Architecture, schemas, technical design |

### Flow Relationships

- **Compass** constrains what you look for with the **Telescope**
- **Telescope** findings inform what goes on the **Map**
- **Map** scope determines what needs a **Blueprint**
- **Ship** (the built thing) validates/invalidates **Compass** assumptions

---

## Instrument Development Process

Each instrument follows this 7-phase development process:

### Phase 1: Foundation
- Identify source methodologies (which thought leaders? often multiple)
- Study each deeply (core concepts, the why behind the how)
- Document the methodologies as-is (before any adaptation)
- Synthesize the baseline (what you're drawing from each source)

**Deliverable:** Methodology source document with synthesized baseline

### Phase 2: Ian's Spin
- What's your unique perspective on this?
- Where do you disagree with the sources?
- What's missing that your experience tells you matters?
- What's overcomplicating things?

*This is intellectual contribution independent of AI considerations.*

**Deliverable:** Adapted methodology with original contributions

### Phase 3: AI-Native / HLCS Adaptation
- What works for human-AI collaboration?
- What doesn't fit / needs modification for Claude Code?
- How does it fit the HLCS 5-tier model?
- What's different when "outputs become inputs"?

**Deliverable:** HLCS-adapted methodology

### Phase 4: Schema Design
- Define the artifact structure (fields, relationships, hierarchy)
- Create sample artifacts by hand (validate the schema works)
- Define validation rules (what makes it valid/invalid)

**Deliverable:** Schema specification + sample artifact

### Phase 5: Protocol Design
- Define phases of collaboration (discovery → generation → review → refinement → approval)
- Define state machine (what states, what transitions)
- Define feedback mechanisms (how does human guide AI)

**Deliverable:** Protocol specification

### Phase 6: Integration
- Define inputs from prior instrument
- Define outputs to next instrument
- Define cross-references between artifacts

**Deliverable:** Integration specification

### Phase 7: Implementation
- Build the HLCS tool (the creation workflow)
- Build the consumption layer (how Claude Code reads/uses the artifact)

**Deliverable:** Working HLCS tool + consumption documentation

---

## Current State

| Instrument | Status | Source Methodology | Schema | Protocol | Integration |
|------------|--------|-------------------|--------|----------|-------------|
| **Compass** | Not started | TBD | — | — | — |
| **Telescope** | Not started | TBD | — | — | — |
| **Map** | In progress | Jeff Patton | In progress | In progress | — |
| **Blueprint** | Not started | TBD | — | — | — |

---

## Work Plan

### Sprint 1: Compass Foundation & Ian's Spin

**Goal:** Establish methodology baseline and unique perspective

**Work:**
1. Review existing Compass work (if any)
2. Survey source methodologies (Lean Canvas, Product Vision Board, Roman Pichler, etc.)
3. Document each source methodology
4. Synthesize baseline
5. Define Ian's spin (unique contributions, disagreements, additions)

**Deliverable:** Compass methodology document (Phases 1-2)

---

### Sprint 2: Compass AI-Native Adaptation & Schema

**Goal:** Adapt for HLCS and define artifact structure

**Work:**
1. HLCS adaptation (Phase 3)
2. Define artifact schema
3. Create sample Compass artifact by hand
4. Define validation rules

**Deliverable:** Compass HLCS methodology + schema specification (Phases 3-4)

---

### Sprint 3: Compass Protocol & Integration

**Goal:** Define collaboration protocol and connections to Telescope

**Work:**
1. Design collaboration protocol (phases, state machine, feedback)
2. Define how Compass outputs constrain Telescope inputs
3. Define how Claude Code consumes Compass during other work

**Deliverable:** Compass protocol + integration specification (Phases 5-6)

---

### Sprint 4: Telescope Foundation & Ian's Spin

**Goal:** Establish discovery methodology baseline and unique perspective

**Work:**
1. Survey discovery methodologies (Teresa Torres, JTBD, etc.)
2. Document each source methodology
3. Synthesize baseline
4. Define Ian's spin

**Deliverable:** Telescope methodology document (Phases 1-2)

---

### Sprint 5: Telescope AI-Native Adaptation & Schema

**Goal:** Adapt for HLCS and define artifact structure

**Work:**
1. HLCS adaptation
2. Define artifact schema
3. Create sample Telescope artifact by hand
4. Define validation rules

**Deliverable:** Telescope HLCS methodology + schema specification (Phases 3-4)

---

### Sprint 6: Telescope Protocol & Integration

**Goal:** Define collaboration protocol and connections to Map

**Work:**
1. Design collaboration protocol
2. Define how Telescope receives from Compass
3. Define how Telescope feeds Map

**Deliverable:** Telescope protocol + integration specification (Phases 5-6)

---

### Sprint 7: Integration Pass

**Goal:** Connect all four instruments end-to-end

**Work:**
1. Define explicit links between artifacts
2. Define shared vocabulary / ontology across instruments
3. Review Map (in progress) for integration points
4. Stub out Blueprint requirements

**Deliverable:** Integration specification + updated Map schema

---

### Sprint 8+: Implementation

Build the actual HLCS tools, prioritized by need.

---

## Other Framework Components (Parked)

These are part of the broader system but not navigation instruments:

### Provisions
- **What it is:** The checklist of what must be in place at each company stage
- **Purpose:** Operational readiness (meta to product work)
- **Status:** Concept defined, implementation deferred

### Ship
- **What it is:** The actual product/codebase
- **Purpose:** The vessel being built and "shipped"
- **Status:** This is the codebase itself, not an HLCS artifact

---

## Relationship to HLCS 5-Tier Model

Each Navigation Instrument maps to the HLCS architecture:

| HLCS Tier | Compass | Telescope | Map | Blueprint |
|-----------|---------|-----------|-----|-----------|
| **Schema Layer** | Vision/strategy schema | Opportunity schema | Story map schema | Architecture schema |
| **Knowledge Layer** | Product strategy methodology | Discovery methodology | Story mapping methodology | Architecture methodology |
| **Data Layer** | Product canvas artifact | Opportunity tree artifact | Story map artifact | Architecture docs artifact |
| **Interaction Layer** | Vision collaboration protocol | Discovery collaboration protocol | Mapping collaboration protocol | Design collaboration protocol |
| **Presentation Layer** | Canvas visualization | Tree visualization | Map visualization | Diagram visualization |

---

## Key Principles

1. **Outputs become inputs** - Each instrument's artifact feeds the next stage
2. **Methodology before schema** - Understand the domain before structuring it
3. **Ian's spin is distinct** - Original contributions exist independent of AI adaptation
4. **AI-native is an adaptation layer** - Built on top of sound methodology, not instead of it
5. **Integration is explicit** - Links between instruments are designed, not assumed

---

## References

- **HLCS Framework:** `/docs/human-llm-collaborative-system-pattern.md`
- **Claude Code Capabilities:** `/docs/claude-code-capabilities-order-of-operations.md`
- **Story Mapper (Map instrument):** `/utilities/story-mapper/` (in progress)

---

## Changelog

**2025-11-26:**
- Initial framework document created
- Defined 4 navigation instruments (Compass, Telescope, Map, Blueprint)
- Defined 7-phase instrument development process
- Created sprint-based work plan
- Parked Provisions concept for later development
