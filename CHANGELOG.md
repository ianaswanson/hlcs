# HLCS Development Changelog

This log tracks the evolution of the HLCS sailing framework through conversation-driven development.

---

## 2025-11-26

### Infrastructure Setup

**Created utilities/hlcs/ structure for reliable multi-session work:**
- Added `.claude/CLAUDE.md` with working instructions
- Added `SESSION.md` for current session context
- Added `CHANGELOG.md` (this file) for historical tracking
- Added `README.md` for public orientation
- Created folder structure:
  - `reference/` for shared source materials (future RAG knowledge base)
  - `{instrument}/` folders for specifications
  - `working/` for active drafts and Claude Desktop imports
- Use `/transcribe` for structured session transcripts (saves to company-level `/transcripts/`)

**Key decisions:**
- Reference materials shared across all instruments (not per-instrument)
- Clear separation: README (what), CLAUDE.md (how), SESSION (now), CHANGELOG (history)
- No duplication between docs - each has one clear purpose

### Course (Roadmap) - Phase 1 Complete (Foundation)

**Completed foundational research and methodology synthesis:**

**Source Methodology Extraction:**
- Located Jackson-60 conversation (~June 2025) containing 5-month-old strategy distillation
- Extracted Strategy as Compass framework (Rumelt + Lafley/Martin synthesis)
- Extracted Ian's rigor additions to Now/Next/Later (Jenna Bastok base)
- Retrieved actual roadmap template HTML for schema extraction

**Reference Documents Created:**
- `reference/methodologies/strategy-as-compass-rumelt-lafley-martin.md`
  - Diagnosis, Guiding Principles, Focus Areas, Trade-offs structure
  - Compass Test for validating strategic content
  - Language guidelines (compass-level vs. initiative-level)
  - Common failure modes and fixes
- `reference/methodologies/now-next-later-jenna-bastok-ian-rigor.md`
  - Language progression (concrete → value → exploratory)
  - Artifact type differentiation (Deliverables/Solutions/Investigations)
  - Force specificity principle
  - Integration with strategy framework

**Course Knowledge Layer v0.1:**
- Created comprehensive `course/knowledge-layer.md` synthesizing all sources
- Ontological layer (what Course is, how it relates to other instruments)
- Evaluative layer (quality criteria for Vision, Strategy, Goals, Now/Next/Later)
- Procedural layer (how to create each component)
- Identified open questions (Course positioning, Vision home, capacity allocation)

**Schema Design:**
- Created `course/schema.json` - formal structure for roadmap artifacts
- Strategic layer: Vision, Strategy (diagnosis/principles/focus/tradeoffs), Goals
- Execution layer: Now/Next/Later horizons, capacity allocation, mandated work
- Definitions for Deliverable, Solution, Investigation artifact types
- Validation-ready JSON Schema (draft-07)

**Example Artifact:**
- Created `course/examples/multnomah-county-example.json`
- Validates schema structure
- Demonstrates all components with realistic content
- Shows goal-to-execution connection

**Key Insights Documented:**
- Strategy is compass (decision framework), not destination list (initiatives)
- Language progression critical to maintaining scale discipline
- Vision = "what SHOULD be" vs. "what CAN be" (audacious human transformation)
- Goals = user behavior change evidence, not output metrics
- Now/Next/Later requires artifact type clarity to avoid confusion

**Open Questions Identified:**
1. Where does Course fit in navigation sequence? (3 models under consideration)
2. Does Vision belong in Course or Compass/Destination?
3. Is capacity allocation (60/20/20) doctrine or example?

**Resolved During Session:**
1. ✅ Course is part of Compass (not separate instrument)
2. ✅ Vision lives on Destination, Course references it
3. ✅ 60/20/20 is example only (not doctrine)

**Folder Reorganization:**
- Moved Course into Compass as subfolder structure:
  - `compass/destination/` (Canvas)
  - `compass/course/` (Roadmap)
- Updated `compass/README.md` to reflect compound structure
- Removed top-level `course/` folder

**Schema Consistency:**
- Converted Destination schema from YAML to JSON for consistency
- Both components now use JSON Schema (draft-07)

**Canonical Example Completion:**
- Created Trello Course (roadmap) example to complement Destination
- Established naming convention: `{product}-{component}.json`
- Renamed files:
  - `fictional-trello-canon.json` → `trello-destination.json`
  - `fictional-trello-canon.json` → `trello-course.json`
- Trello now spans both Compass components with consistent vision, strategy, and goals

**Final Deliverables:**
- Complete Compass documentation (both components)
- JSON schemas for Destination and Course
- Knowledge layers with methodology synthesis
- Canonical Trello example across both components
- Reference materials for source methodologies

---

## 2025-11-27

### Session 1: Improved Session Startup Protocol

**Problem Identified:**
- Memory files (HLCS pattern, Navigation framework) are automatically loaded in `.claude/memory/`
- But CLAUDE.md guidance wasn't strong enough to ensure Claude verified these frameworks first
- Led to sessions starting without proper context loading

**Solution Implemented:**
- Updated `.claude/CLAUDE.md` "Core Framework Reference" section:
  - Changed from "Read these" to "CHECK MEMORY FIRST" with stronger emphasis
  - Clarified that files are automatically loaded (not manual Read required)
  - Listed explicit filenames and brief descriptions
  - Added reference to company-core.md availability
- Updated Session Protocol to make "Verify memory loaded" the first step
- This ensures future sessions will check framework understanding before starting work

**Impact:**
- Better session startup reliability
- Clearer checklist for Claude to follow
- Reduces risk of working without foundational context

### Session 2: Verified Migration from Claude Desktop

**Reviewed Claude Desktop conversation transfer:**
- Confirmed Navigation Instruments Framework successfully migrated to `.claude/memory/`
- Confirmed HLCS pattern migrated to `.claude/memory/`
- Verified Compass Destination knowledge layer migrated to `compass/destination/knowledge-layer.md`
- Verified Fictional Trello canon examples in place

**Cleanup:**
- Removed redundant files from `working/` folder:
  - `compass-knowledge-layer-v1.md` (duplicate - canonical version in compass/destination/)
  - `claude-desktop-conversation.md` (reviewed, content preserved)

**Status:**
- No information lost in Claude Desktop → Claude Code migration
- All artifacts in canonical locations
- Working folder clean and ready for new drafts

---

## 2025-11-28

### Session 3: Compass Visualization Wireframes

**Created HTML wireframe visualizations for both Compass components:**

**Destination Canvas Wireframe:**
- Created `compass/destination/visualization.html` - simple black/white wireframe
- Layout design with visual hierarchy:
  - Vision (full width, thick border) at top
  - Problem (2fr) | Solution+Customer stacked (1fr) | Unique Value (2fr) in main row
  - Timing | Market | Revenue (equal thirds) in context row
  - Truths | Bets (equal halves, dashed border for Bets) at bottom
- Minimal CSS, no colors, maximum clarity
- Final design emphasizes Problem and Unique Value as primary elements

**Course Roadmap Wireframe:**
- Created `compass/course/visualization.html` - simple black/white wireframe
- Layout design:
  - Vision reference (from Destination)
  - Strategy section (diagnosis, guiding principles, focus areas, tradeoffs)
  - Goals grid (Goal | Current | Target | Status)
  - Execution grid (Goal | NOW | NEXT | LATER)
- Removed capacity allocation, small requests, operational work (not in core schema)
- Clean grid structure with time-horizoned work organized by goal

**Schema Simplification:**
- Removed from `course/schema.json`:
  - `capacityAllocation` (and removed from required fields)
  - `smallRequests`
  - `operationalWork`
  - `mandatedWork`
- Updated `course/examples/trello-course.json` to match simplified schema
- Schema now matches visualization exactly - no unused fields

**Example Visualizations with Real Data:**
- Created `compass/destination/examples/trello-destination-visualization.html`
  - Filled wireframe with complete Trello Destination data
  - Shows Vision, Problem/Solution/Customer, Unique Value, Market context, Truths/Bets
  - Much easier to read than JSON
- Created `compass/course/examples/trello-course-visualization.html`
  - Filled wireframe with complete Trello Course data
  - Shows Strategy, 3 Goals with metrics, NOW/NEXT/LATER work by goal
  - Demonstrates how goals connect to execution

**Design Process:**
- Iterated on visual hierarchy and spacing
- Simplified from initial colorful design to minimal wireframe
- Adjusted column widths for optimal readability
- Removed unnecessary sections to focus on core content
- Result: Clean, scannable layouts that match schema structure

**Impact:**
- JSON schemas now validated against working visualizations
- Example data much more accessible and understandable
- Clear templates for future tool development
- Trello canonical example complete across both components with visualizations

---

## 2025-11-25 (approximate)

### Compass Knowledge Layer v1

**Published complete Compass specification:**
- Created knowledge-layer-v1.md with full methodology synthesis
- Defined schema v3 (Vision, Customer, Problem, Solution, Unique Value, Timing, Market, Revenue, Truths & Bets)
- Synthesized from multiple sources:
  - Geoffrey Moore (Crossing the Chasm) - Vision template, beachhead
  - Sequoia Capital - Pitch deck framework, "Why Now"
  - Bill Gross - Timing as #1 success factor
  - Lean Canvas / BMC - Problem/Solution/Revenue structure
  - B2B sales theory - Buyer/User/Champion distinction
  - Moat theory - Hard-to-copy framework

**Structure includes:**
- Ontological layer (what it is)
- Evaluative layer (what makes it good)
- Procedural layer (how to create it)
- AI-native considerations
- YAML schema specification

---

## 2025-11-25 (approximate)

### Navigation Instruments Framework

**Created foundational framework document:**
- Defined 4 core navigation instruments (Compass, Telescope, Map, Blueprint)
- Established 7-phase instrument development process:
  1. Foundation (source methodologies)
  2. Ian's Spin (unique adaptations)
  3. AI-Native Adaptation (HLCS considerations)
  4. Schema Design (artifact structure)
  5. Protocol Design (collaboration workflow)
  6. Integration (instrument connections)
  7. Implementation (build the tool)
- Documented in: `docs/patterns/navigation-instruments-framework.md`

**Key insights:**
- Each instrument is an HLCS implementation (human-AI collaboration producing artifacts)
- Outputs become inputs (Compass → Telescope → Map → Blueprint → Ship)
- Ian's spin is distinct from AI-native adaptation
- Methodology before schema (understand domain before structuring)

---

## Earlier Work

### Compass Product Prototype

**Built working Next.js app (`products/compass/`):**
- Generic canvas interaction/visualization
- Tested HLCS collaboration patterns
- File-based JSON storage
- Chat integration with Claude Code
- Successfully validated interaction concepts

**Key learning:** Canvas approach works well for this type of structured collaboration

### Story Mapper Development

**Prior iteration in `products/story-mapper/`:**
- Rigorous Jeff Patton story mapping methodology
- v5 schema (Activities → Tasks → Details with tags)
- HTML visualizer prototype
- Pre-dates HLCS 5-tier system integration
- Demonstrates vertical slice + discovery phase patterns

**Status:** In discovery phase, successful visualization + generation capability

---

## Original HLCS Ship Metaphor

**Developed nautical metaphor for human-AI collaboration:**
- Large conversation export (884KB) exploring the sailing framework
- Mapped product development to ship navigation concepts
- Identified collaboration "points" and artifacts
- Foundation for current instrument development

**Location:** Currently at `utilities/hlcs/Claude-Ship metaphor framework for human-AI collaboration.md` (needs migration to conversations/)

---

**Note:** This changelog started 2025-11-26. Earlier entries reconstructed from existing artifacts and context.
