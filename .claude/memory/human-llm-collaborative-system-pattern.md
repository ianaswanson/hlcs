# HLCS: Human-LLM Collaborative Systems
## The 5-Tier Architecture Pattern for Structured Creative Work

**HLCS (Human-LLM Collaborative System)** - A software pattern for situations where humans and LLMs must work together to produce structured artifacts through iterative refinement. Unlike traditional software (where code executes logic deterministically) or simple AI assistants (single-shot query-response), HLCS requires explicit architecture across 5 layers to coordinate creative collaboration.

### Key Characteristics:
- Multi-turn collaboration with state
- Structured output conforming to schema
- **Outputs become inputs** - Artifacts feed downstream AI/human processes
- Iterative refinement cycles
- Human review and approval gates
- Shared knowledge base between human and AI

## Core Principle

Unlike traditional software where logic is EXECUTED by code, human-AI collaborative systems require logic to be INTERPRETED by the AI and results to be REVIEWED by humans. This creates fundamentally different architectural requirements.

---

## Is This an HLCS Problem?

### The Pattern Recognition

**HLCS is appropriate when:**

1. **Output becomes input** - The artifact feeds downstream AI/human work
2. **Structure enables automation** - Machine-readable format lets AI consume it reliably
3. **Quality bar is high** - Wrong output has real consequences
4. **Iteration expected** - First draft is rarely final
5. **Collaboration is essential** - Neither human nor AI can do this well alone

### Why "Outputs Become Inputs" Matters

In AI-native workflows, artifacts aren't just documentation - they're executable knowledge:

- **Story map** → AI reads during `/new-feature` to understand scope
- **API contract** → AI generates client/server code from schema
- **Architecture diagram** → AI checks code against design decisions
- **Test plan** → AI generates tests following strategy

**The structure isn't for humans** - it's so AI can reliably consume and act on the artifact.

### Quick Validation

When you recognize an HLCS need, I'll ask 1-2 quick questions to confirm:
- What downstream process consumes this?
- Is iteration expected or one-shot sufficient?

Then we build it.

---

## The 5 Tiers

### 1. Schema Layer (The Contract)

**Purpose:** Defines what can exist in the system - the contract both human and AI must agree on.

**Sub-Layers:**
- **Type Definitions:** Structure and data types of all entities
- **Validation Rules:** Constraints and business rules for valid data
- **Relationships:** How entities connect (hierarchies, references, ordering)
- **Versioning Strategy:** How the schema evolves over time

**Example:** For story maps - Activities contain Steps, Steps contain Stories, each with specific fields and constraints.

---

### 2. Knowledge Layer (What the AI Needs to Know)

**Purpose:** Provides the AI with everything needed to understand and work with the domain.

**Key Distinction:** This is DOCUMENTATION the AI reads, not CODE that executes.

**Sub-Layers:**

**2.1 Ontological Layer (WHAT things are)**
- Definitions of domain terms
- Conceptual models
- Taxonomies and categorizations
- Fundamental principles

**2.2 Procedural Layer (HOW to do things)**
- Methods, processes, step-by-step instructions
- Decision trees and workflows
- When to use which approach

**2.3 Evaluative Layer (WHAT makes things good/bad)**
- Quality criteria and heuristics
- Good vs bad examples
- Anti-patterns to avoid
- Best practices

**2.4 Contextual Layer (WHAT's true about THIS situation)**
- Project-specific information
- Domain-specific facts
- Business constraints
- Decisions made in this session
- Accumulated conversation context

**Example:** Story mapping methodology (ontological), step-by-step generation process (procedural), anti-patterns to avoid (evaluative), specific product context (contextual).

---

### 3. Data Layer (The Shared State)

**Purpose:** Holds the actual instances of data being collaboratively created/modified.

**Sub-Layers:**
- **Current State:** The actual data right now, conforming to schema
- **History:** Past versions and evolution of changes
- **Metadata:** Information about the data (created, modified, status, etc.)
- **Derived State:** Information computed from base data

**Example:** The actual story map JSON file with all activities, steps, and stories.

---

### 4. Interaction Layer (How Human and AI Coordinate)

**Purpose:** Defines how human and AI coordinate their work on the shared data.

**Key Characteristic:** This is the NOVEL layer that doesn't exist in traditional software. It's essential and cannot be simplified.

**Sub-Layers:**

**4.1 Protocol**
- Phases of collaboration (discovery, generation, review, refinement, approval)
- Who does what in each phase
- What questions the AI asks
- What information the human provides
- How iterations work
- Exit criteria for each phase

**4.2 State Machine**
- Discrete states the collaboration can be in
- Valid transitions between states
- Entry/exit conditions
- Valid actions in each state

**4.3 Feedback Mechanisms**
- Types of feedback (approve, reject, modify, clarify)
- How feedback is expressed
- Required specificity
- Acknowledgment patterns

**4.4 Conflict Resolution**
- How to detect conflicts
- Types of conflicts
- Resolution strategies
- Who has authority
- Escalation paths

**4.5 Synchronization**
- What is authoritative source
- How changes propagate
- Timing (immediate, batched, manual)
- Preventing divergence

**Example:** Multi-step story map generation with discovery → generation → review → refinement → approval phases, explicit state transitions, structured feedback.

---

### 5. Presentation Layer (How Humans See and Interact)

**Purpose:** Make the data visible and manipulable for the human.

**Sub-Layers:**
- **Rendering:** Converting structured data to visual representation
- **Layout & Styling:** Visual design and aesthetic presentation
- **Interaction Affordances:** What actions human can take through interface
- **UI State Management:** Ephemeral state for interaction (not part of data model)

**Example:** Story map displayed as visual board with cards, drag-drop editing, filtering, etc.

---

## Why Traditional 3-Tier Architecture Fails

**Traditional 3-Tier:** Presentation ↔ Business Logic ↔ Data

**Problems for AI collaboration:**
1. No Knowledge Layer - Where does AI get domain expertise?
2. No Interaction Layer - How do human and AI coordinate?
3. Business Logic assumes determinism - AIs are probabilistic
4. No review loop - Traditional systems don't expect human approval of every output
5. No protocol - APIs are one-shot, not conversational

**The 5-Tier architecture addresses these gaps.**

---

## Critical Learning: The Interaction Layer Cannot Be Simplified

**What we learned:** Attempting to compress creative collaboration into a single command or simplified workflow fails.

**Example:** Our Claudian-level story map generator (agent + command) was overly reductive and simplistic. It tried to collapse discovery, generation, review, refinement, validation, and finalization into one interaction. **This doesn't work.**

**Why:** Layer 4 (Interaction) needs proper implementation with:
- Explicit phases and transitions
- State management
- Feedback loops
- Validation at each stage
- Ability to review and revise

**You cannot shortcut this layer.** It requires proper tooling, not just configuration or documentation.

---

## Where Each Layer Lives in Claudian Architecture

### Claude Code Configuration (Claudian Company Level)

**Can effectively implement:**
- ✅ **Knowledge Layer** - Memory files with methodology, anti-patterns, domain knowledge
- ✅ **Schema Layer (documentation)** - Reference documentation about schema structure

**Cannot effectively implement:**
- ❌ **Data Layer** - No persistence, history, metadata management
- ❌ **Interaction Layer** - Can document protocol but cannot enforce state machines, synchronization
- ❌ **Presentation Layer** - Terminal output only, no rich UI
- ❌ **Schema Layer (validation)** - Can check but cannot programmatically enforce

### Tools/Products (Proper Implementation)

**Must implement:**
- ✅ **Data Layer** - Persistence, history, metadata, derived state
- ✅ **Interaction Layer** - Protocol runner, state machine, feedback parsing, synchronization
- ✅ **Presentation Layer** - Rendering, layout, interaction affordances, UI state
- ✅ **Schema Layer (validation)** - Programmatic enforcement of rules

**Can import:**
- ✅ **Knowledge Layer** - Reference Claudian memory for domain expertise
- ✅ **Schema Layer (documentation)** - Use company schema definitions

---

## The Pattern: Create vs Consume

**For any collaborative artifact (story maps, architecture diagrams, API contracts, etc.):**

### Tool/Product Creates (Complex)
- Implements all 5 tiers properly
- Multi-step process with protocol
- State management and validation
- Feedback loops and refinement
- Exports standard format artifact

### Claudian Company Memory Teaches Consumption (Simple)
- What the artifact is (ontology)
- Where artifacts live (file locations)
- How to read them (schema reference)
- When to reference them (during what activities)
- How they integrate with workflows
- What they're NOT (misconceptions)

**This separation is clean and scalable.**

---

## Starting an HLCS Project

### Phase 1: Recognition & Scoping

**You'll say:** "We need to create a new HLCS for X"

**I'll validate:**
- What artifact are we creating?
- What downstream process consumes it?
- What's the quality bar?

**We agree and proceed.**

### Phase 2: Domain Understanding First

**Before schema, understand the domain:**

1. **What is this thing?** (Ontological)
   - Core concepts and definitions
   - How practitioners think about it
   - Fundamental principles

2. **What makes a good one?** (Evaluative)
   - Quality criteria
   - Common anti-patterns
   - Best practices from the field

3. **How do you create it?** (Procedural)
   - Rough process flow
   - Key decision points
   - Expert techniques

**Why this order:** You can't structure what you don't understand.

**Deliverable:** Domain knowledge documentation (rough notes are fine)

### Phase 3: Schema Design

**Now that we understand the domain:**

1. **Define entities and relationships**
   - What are the main objects?
   - How do they connect?
   - What's the hierarchy?

2. **Create sample artifact by hand**
   - Build a realistic example manually
   - This validates the schema works
   - Reveals missing fields/relationships

3. **Write validation rules**
   - Required fields
   - Valid values
   - Referential integrity
   - Business rules

4. **Define downstream consumption**
   - How will Claude Code read this?
   - What queries/operations are needed?
   - What derived data is useful?

**Deliverable:** `schema-v1.json` + sample artifact + validation spec

### Phase 4: Interaction Protocol Design

**Layer 4 (Interaction) - The critical layer:**

**The collaborators:** You (Ian) + Claude Code

1. **Map the phases**
   - Discovery: What must Claude ask you?
   - Generation: What does Claude create?
   - Review: How do you evaluate?
   - Refinement: How does Claude incorporate your feedback?
   - Approval: What's the exit criteria?

2. **Design state machine**
   - What states can the system be in?
   - Valid transitions?
   - Entry/exit conditions?

3. **Define feedback mechanisms**
   - How do you give feedback? (approve, reject, modify, clarify)
   - How does Claude interpret it?
   - Required specificity?

4. **Synchronization strategy**
   - What's source of truth?
   - When do changes propagate?
   - Conflict resolution rules

**Deliverable:** Protocol specification + state machine diagram

### Phase 5: Minimal Implementation

**Build in order:**

1. **Data Layer (Layer 3) - Basic**
   - File storage for artifacts
   - Current state only (no history yet)
   - Schema validation

2. **Presentation Layer (Layer 5) - Terminal**
   - Text rendering of artifact
   - Basic display
   - (Rich UI comes later)

3. **Interaction Layer (Layer 4) - Protocol Runner**
   - Implement phase transitions
   - State management
   - Feedback parsing
   - This is the hardest part

4. **Integration**
   - Connect all layers
   - End-to-end test
   - Validate with real use case

**Deliverable:** Working prototype HLCS

### Phase 6: Iteration & Refinement

**After first real use:**

1. **Refine knowledge** - What did Claude misunderstand?
2. **Improve protocol** - Where did collaboration break down?
3. **Enhance validation** - What corrupt data got through?
4. **Better presentation** - What was hard to review?

**Key metric:** Can you and Claude Code reliably produce valid, high-quality artifacts together?

---

## Design Principles

1. **Domain Understanding Before Schema** - Understand what you're structuring before structuring it
2. **Knowledge Is Explicit** - Don't assume AI knows your domain
3. **Interaction Is Protocol** - Define collaboration pattern as precisely as data structure
4. **Human Has Authority** - In conflicts, human judgment wins
5. **Transparency Over Magic** - Make AI reasoning visible
6. **Iterative Refinement** - Expect multiple rounds, support iteration
7. **Validation Is Mandatory** - Schema validation prevents corrupt data
8. **Context Accumulates** - System maintains and leverages conversation context

---

## Application to Claudian Products

### Story Mapper (First HLCS Implementation)

**HLCS Tool** (`utilities/story-mapper/`):
- Full 5-tier HLCS implementation
- Multi-step workflow with phases
- State management and validation
- Exports story-map-v5.json

**Claudian Memory** (`.claude/memory/`):
- Story mapping methodology (Knowledge Layer)
- How to read story map artifacts (consumption)
- When to reference story maps during development
- Integration with `/new-feature` workflow

**NOT an HLCS:**
- `/generate-story-map` command (too reductive, lacks protocol)
- Single-shot story map generation (no iteration)

### Planned HLCS Systems

**High Priority:**
- API Contract Designer (creates OpenAPI specs)
- Schema Designer (creates ERDs, migration plans)

**Medium Priority:**
- Architecture Mapper (creates architecture diagrams)
- Test Plan Generator (creates test strategies)

**Each follows the pattern:**
- HLCS tool implements 5 tiers and creates artifact
- Claudian memory teaches consumption of artifact
- Clear separation of create (complex) vs consume (simple)

---

## HLCS Anti-Patterns

### Anti-Pattern 1: The Oversimplified Command

**Symptom:** Trying to collapse HLCS into a single slash command
**Example:** `/generate-story-map "build a todo app"`
**Why it fails:** No protocol, no iteration, no review loop
**Fix:** Build proper HLCS tool with phases

### Anti-Pattern 2: The Mega-Prompt

**Symptom:** Trying to achieve HLCS through one giant prompt
**Example:** 5000-word prompt with all knowledge, examples, and instructions
**Why it fails:** Overwhelming context, no state management, no iteration
**Fix:** Structure knowledge properly, implement protocol

### Anti-Pattern 3: The Missing Schema

**Symptom:** Starting with interaction protocol before defining schema
**Example:** "Let's build a workflow to create X" without defining what X is
**Why it fails:** Can't validate what you can't define
**Fix:** Domain understanding first, then schema

### Anti-Pattern 4: The Assumed Knowledge

**Symptom:** Expecting AI to know domain without explicit knowledge layer
**Example:** "Claude should know how to do story mapping"
**Why it fails:** AI doesn't reliably learn from conversation history
**Fix:** Explicit knowledge documentation

### Anti-Pattern 5: The No-Review Creation

**Symptom:** Generating complete artifact without intermediate review
**Example:** AI generates entire story map, human approves or rejects whole thing
**Why it fails:** Too much to review at once, no way to course-correct
**Fix:** Phase-based protocol with incremental review

### Anti-Pattern 6: The Stateless Collaboration

**Symptom:** No persistence between sessions
**Example:** Every time you run the tool, start from scratch
**Why it fails:** Can't iterate, can't refine, can't build on previous work
**Fix:** Implement data layer with persistence

---

## Key Insight

**Complex creative collaboration cannot be simplified into configuration or single commands.**

The Interaction Layer requires proper implementation with:
- Multi-step protocols
- State machines
- Validation at each stage
- Feedback loops
- Review and revision capability

**Build proper tools for creation. Use Claudian memory for consumption.**

---

## References

- **Framework source:** Consultant theory on human-AI collaborative systems
- **Validation:** Story mapper experience (failed simple approach, need proper implementation)
- **Discussion:** See `/transcripts/2025-11-13-five-tier-framework-collaborative-systems.md`

---

**Status:** Active framework for designing collaborative tools
**Last Updated:** November 22, 2025
