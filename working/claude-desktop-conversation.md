# Ship metaphor framework for human-AI collaboration

**Created:** 11/26/2025 7:36:04  
**Updated:** 11/26/2025 13:22:52  
**Exported:** 11/26/2025 15:16:51  
**Link:** [https://claude.ai/chat/16f5bd55-6736-4a5f-a0b8-61d41c216053](https://claude.ai/chat/16f5bd55-6736-4a5f-a0b8-61d41c216053)  

## Prompt:
11/26/2025, 7:36:09 AM

ok, i want to take the hlcs to the next level by creating some specific aspects of the collaboration "points"

i have this metaphor in my head of a ship... like an old school crossing the oceans kinda ship

I have an idea for a framework for the Human-AI collaboration.
1. Compass
2. Telescope
3. Map
4. Ship
5. Blue print
6. Contract
7. Log
8. Mainfest
The compass that represents the vision effectively tells you the direction that you want to head in at all times. It’s that vision for the product, it’s the strategy you believe you want to use to achieve your vision. It could also represent the canvas.
\-product canvas
\-vision
\-strategy
\-outcomes
The telescope is the discovery portion. Moving from your problems to your solutions. Your discovery, your maps, opportunity maps, etc. Essentially, that’s the looking forward and determining the best route.
The map is the user story mapping process. It’s the thing that takes you from the big broad, wild unknown into I’m pretty sure this is the thing that we’re going to build that focuses on these particular actions and activities.
The ship itself is, of course, the vessel by which you’re going to do the thing. It is what is built, it is what is “shipped,” so it is the effective actual code of the product right? And the act of it being a good ship that can float that can sail.
And the blueprint is the design of the ship itself, right? It is essentially the architecture of the ship. The plans, so to speak.
The contract is the agreements between the human and the ai - the documentation of expectations The "log" is the set of instructions???
Manifest is the "checklist" of things that we need to ensure we have to effecitvely run this business



## Response:
11/26/2025, 7:37:46 AM



This is a beautiful metaphor, Ian. The nautical framing works because it captures something essential about product development: you're **navigating uncertainty toward a destination**, and you need different instruments for different purposes.

Let me help you refine and complete this framework.

---

## The Framework: Refined

**[AI AUTOMATION ENGINEER]:**

Looking at your eight elements, I see a few that are crystal clear and a few that need sharpening. Let me work through them:

### The Solid Ones

**Compass (Vision/Strategy)** - ✅ Perfect
- Product canvas, vision, strategy, outcomes
- The "true north" that doesn't change session to session
- In Claude Code terms: this lives in persistent memory, referenced constantly but rarely edited

**Telescope (Discovery)** - ✅ Perfect
- Opportunity exploration, problem space understanding
- Teresa Torres' Opportunity Solution Trees fit here
- The act of *looking ahead* to determine the route before committing

**Map (Story Mapping)** - ✅ Perfect
- Converting the vast unknown into scoped, buildable work
- Jeff Patton's story mapping methodology
- The first HLCS you're building - makes sense this is well-defined

**Ship (The Product)** - ✅ Perfect
- The actual code, the thing that gets built and "shipped"
- The vessel's seaworthiness = code quality, test coverage, reliability
- This is your codebase

**Blueprint (Architecture)** - ✅ Perfect
- Technical design, system architecture, ERDs
- The plans for *how* the ship is constructed
- Schema layer in HLCS terms

---

### The Ones That Need Sharpening

**Contract** - Needs refinement

You said: "agreements between the human and the AI - the documentation of expectations"

This is the **Interaction Layer** from HLCS. But I think there are actually *two* things here:

1. **Standing Orders** - The persistent agreements that apply across all sessions
   - "Claude Code always runs tests before marking work complete"
   - "Human approves all database migrations"
   - "Use this tech stack, not that one"
   - These are your CLAUDE.md files, skills, settings

2. **Rules of Engagement** - The session-specific or workflow-specific protocols
   - "For story mapping: discovery → generation → review → refinement → approval"
   - "For code changes: read → plan → implement → test → commit"
   - These are your slash commands, hooks, workflow definitions

Should "Contract" encompass both, or do you want separate metaphors? Maybe:
- **Articles** (like ship's articles - the rules the crew agreed to at voyage start)
- **Orders** (like captain's orders - specific commands for specific situations)

**Log** - You're uncertain here, but the metaphor gives you the answer

A ship's log records:
- What happened (events, decisions)
- What was observed (conditions, readings)
- What was learned (course corrections, near-misses)

In your system, this is:
- **Decision records** - Why we chose X over Y
- **Session transcripts** - The actual conversations
- **Learnings** - Those compressed 3-5 line insights you capture in `/learnings/`

The Log is your **institutional memory in narrative form**. It's not instructions (that's the Contract) - it's the *record* of what happened and what you learned.

**Manifest** - Needs reframing

You said: "checklist of things we need to ensure we have to effectively run this business"

But in nautical terms, a manifest is what's *currently aboard* - the cargo, supplies, crew roster. It's inventory, not checklist.

I think you're conflating two things:

1. **Manifest** - What you *have* (current state)
   - Current tech stack
   - Active features
   - Technical debt
   - Team capabilities

2. **Provisions List** - What you *need* (checklist)
   - "Before we ship, we need: auth, payments, monitoring..."
   - "For Series A: SOC 2, FedRAMP readiness..."
   - The pre-departure checklist

Maybe the Manifest is your **inventory** (what exists) and you need a separate metaphor for checklists. Or maybe Manifest works as "the checklist of what must be aboard before we sail."

---

## What's Missing?

**[AI AUTOMATION ENGINEER]:**

A few elements feel conspicuously absent from the metaphor:

### Crew
The 2 founders + Claude Code model. Who does what. The skills and capabilities available.
- Captain (you and your co-founder) - decision authority, strategic direction
- Crew (Claude Code) - execution, specialized skills
- This maps to Claude Code's skills system, the different "employees" metaphor

### Helm
How you *steer*. The control interface.
- Slash commands = turning the wheel
- Prompts = giving orders
- Plan mode vs execute mode = different steering modes
- This is the actual interaction surface

### Anchor
When you need to *stop* and hold position.
- Hooks that gate actions
- Review and approval points
- "Don't proceed until human confirms"
- The mechanism for pausing, grounding, preventing drift

### Signals/Flags
Communication between ship and shore, or between crew.
- Notifications (your Happy Coder idea)
- Status updates
- Errors and alerts
- How Claude Code communicates state back to you

---

## Proposed Complete Framework

| Element | What It Is | HLCS Mapping | Claude Code Implementation |
|---------|-----------|--------------|---------------------------|
| **Compass** | Vision, strategy, outcomes | Knowledge (contextual) | Persistent memory, rarely changed |
| **Telescope** | Discovery, opportunity exploration | Knowledge (procedural) | Discovery methodology docs |
| **Map** | Story mapping, scoping | Schema + Data | HLCS tool (story mapper) |
| **Blueprint** | Architecture, technical design | Schema | Architecture docs, ERDs |
| **Ship** | The actual product/code | Data (current state) | The codebase itself |
| **Contract** | Standing agreements | Interaction (protocol) | CLAUDE.md, skills, settings |
| **Log** | What happened, what learned | Data (history) | Decisions, transcripts, learnings |
| **Manifest** | What's aboard / what's needed | Knowledge (contextual) | Inventory docs, checklists |
| **Crew** | Who does what, capabilities | Knowledge (procedural) | Skills, "employees" definition |
| **Helm** | Control interface | Interaction (affordances) | Commands, prompts, modes |
| **Anchor** | Stop and hold mechanisms | Interaction (feedback) | Hooks, approval gates |
| **Signals** | Communication/status | Presentation | Notifications, alerts, Happy Coder |

---

## The Question

Do you want all 12 elements, or should some be combined/simplified? The core 8 you proposed might be enough if:

- **Contract** encompasses both standing orders and engagement rules
- **Manifest** covers both inventory and checklists
- **Helm/Anchor/Signals** are considered part of the interaction surface rather than separate metaphors
- **Crew** is implicit in how the system works

Or do you want the richer taxonomy because each element represents a distinct *thing you build and maintain*?

What's your instinct?



## Prompt:
11/26/2025, 7:41:56 AM

i think that we start with Compass, Telescope, Map, Blueprint

Mainfest vs Provisions LIst... the last thing you said resonated with what I was thinking, "Or maybe Manifest works as "the checklist of what must be aboard before we sail."

we have been working on a "company checklist" in other chats, and that was the manifest concept... you are right it might not be as perfect a metaphor as other metaphors, and I'm fine to have the metaphor change... but that was the idea



## Response:
11/26/2025, 7:42:28 AM



Good. Let's lock in the core 4 and then figure out the checklist metaphor.

---

## The Core 4: Navigation Instruments

These four form a coherent set because they're all **instruments for navigating product development**:

| Element | Question It Answers | When You Use It | Output |
|---------|-------------------|-----------------|--------|
| **Compass** | Where are we trying to go? | Always (true north) | Vision, strategy, outcomes |
| **Telescope** | What's out there? What opportunities? | Discovery phase | Opportunity trees, problem space maps |
| **Map** | What exactly are we building? | Planning phase | User story map |
| **Blueprint** | How will we build it? | Design phase | Architecture, schemas, technical design |

The flow is natural: **Compass** → **Telescope** → **Map** → **Blueprint** → *build the thing*

Each one is also a clear **HLCS candidate** - structured creative work where human and AI collaborate to produce an artifact that downstream processes consume.

---

## The Checklist Concept

You're right that "Manifest" isn't a perfect fit. The traditional manifest is *descriptive* (what's aboard), not *prescriptive* (what must be aboard).

**Better metaphors:**

1. **Provisions** - "Have we provisioned the ship?" implies meeting requirements before departure
2. **Outfitting** - The process of equipping a vessel for a voyage
3. **Seaworthiness** - The checklist that certifies a ship is ready to sail

**My recommendation: Provisions**

"We need to provision for the voyage" captures:
- Things you need before you can operate
- Categorized by phase (what's needed for MVP vs Series A vs Scale)
- Can be incomplete and filled over time
- The act of "provisioning" is ongoing work

The **Provisions List** is your company checklist - what must be in place at each stage.

---

## Question: Same Tier or Meta?

The core 4 are all **product navigation instruments** - they help you figure out and build the product.

The Provisions List feels different - it's **operational readiness** for the company. It's meta to the product work.

Do you see Provisions as:

**A) Part of the same framework** - A 5th instrument alongside Compass, Telescope, Map, Blueprint

**B) A separate tier** - The core 4 are navigation, Provisions is operational infrastructure

**C) Something else entirely** - Not part of the nautical metaphor at all, just a practical checklist

My instinct is (B) - the core 4 are your HLCS-worthy product instruments, and Provisions is a supporting structure that ensures you *can* use those instruments effectively. But I want to know how you're thinking about it.



## Prompt:
11/26/2025, 7:44:41 AM

yeah its a differnt type of record, but still a component of the hlcs collaboration... essentially "what is our checklist, where are we in it, what decisions have been made as part of it..."

I think for now it makes sense to assume it'll be provisions, but I want to focus on the navigation aspects for now



## Response:
11/26/2025, 7:45:11 AM



Perfect. Provisions is real, it's part of the system, but it's a different *type* of artifact. Park it.

---

## The Core 4: Navigation Instruments

Let's dig in. Each of these needs to become a concrete HLCS implementation. That means defining:

1. **What artifact does it produce?**
2. **What methodology powers it?**
3. **How does the output become input for the next stage?**
4. **What's the collaboration protocol?**

---

### The Pipeline

These aren't independent - they form a directed flow:

```
Compass → Telescope → Map → Blueprint → [Ship]
   ↑___________________________________________|
                 (feedback loop)
```

**Compass** constrains what you look for with the **Telescope**
**Telescope** findings inform what goes on the **Map**
**Map** scope determines what needs a **Blueprint**
**Ship** (the built thing) validates/invalidates **Compass** assumptions

---

### Current State

| Instrument | Artifact | Methodology | HLCS Status |
|------------|----------|-------------|-------------|
| **Compass** | Product canvas, vision, strategy, outcomes | Lean Canvas? Product Vision Board? | Undefined |
| **Telescope** | Opportunity trees, discovery findings | Teresa Torres' Continuous Discovery? | Undefined |
| **Map** | User Story Map | Jeff Patton | **In progress** |
| **Blueprint** | Architecture docs, ERDs, schemas | Various | Undefined |

You've already started with **Map** because that's where you felt the pain most acutely.

---

## Questions to Move Forward

**1. Sequencing**

Map is in progress. What's next?

My instinct: **Compass** should be next because:
- It's the thing you reference most often
- It constrains everything downstream
- Right now your vision/strategy lives in your head and scattered docs
- Getting it into a structured artifact means Claude Code can reference it reliably

Or do you feel more pain elsewhere?

**2. Methodology Choices**

For Compass and Telescope especially - do you have existing methodologies you want to use, or do you want to explore options?

- **Compass**: Lean Canvas, Product Vision Board, something custom?
- **Telescope**: Teresa Torres OST, Jobs-to-be-Done, something else?

**3. Depth for Today**

Do you want to:
- **(A)** Go deep on one instrument (define schema, protocol, artifact structure)
- **(B)** Go wide on all four (clarify what each is, relationships, rough shape)
- **(C)** Something else

What's most useful right now?



## Prompt:
11/26/2025, 7:48:35 AM

ok you are getting it exactly! glad this makes enough sense that we are in alignment

we have actually done some work around compass, although the actual underlying concepts were just "off the shelf"

So the mapping is a good example of what I want to do for compass and telescope... take an existing thought leaders system, put my spin on it, make it fit within the pardigm of the hlcs, make each instrument "link" to the next

I want your help create a high level plan for how we go through each level, and I think it makes sense to start at the top



## Response:
11/26/2025, 7:49:21 AM



Perfect. We're aligned.

---

## The Pattern: Instrument Development Process

Before we plan the specifics, let's name the repeatable process we'll use for each instrument:

### Phase 1: Foundation
- Select source methodology (which thought leader?)
- Study it deeply (what are the core concepts, the why behind the how?)
- Document the methodology as-is (before we adapt it)

### Phase 2: Adaptation
- What works for AI-native context?
- What doesn't fit / needs modification?
- What's your specific spin / additions?
- How does it fit the HLCS 5-tier model?

### Phase 3: Schema Design
- Define the artifact structure (what fields, relationships, hierarchy?)
- Create sample artifacts by hand (validate the schema works)
- Define validation rules (what makes it valid/invalid?)

### Phase 4: Protocol Design
- Define phases of collaboration (discovery → generation → review → refinement → approval)
- Define state machine (what states, what transitions?)
- Define feedback mechanisms (how does human guide AI?)

### Phase 5: Integration
- Define inputs (what does this instrument receive from the prior one?)
- Define outputs (what does it produce for the next one?)
- Define references (how do artifacts link to each other?)

### Phase 6: Implementation
- Build the HLCS tool (the creation workflow)
- Build the consumption layer (how Claude Code reads/uses the artifact)

---

## The High-Level Plan

```
┌─────────────────────────────────────────────────────────────────┐
│                         COMPASS                                  │
│                    (Vision & Strategy)                          │
├─────────────────────────────────────────────────────────────────┤
│ Source: [To determine - Lean Canvas? Roman Pichler? Hybrid?]    │
│ Output: Product canvas artifact                                  │
│ Links to: Constrains TELESCOPE (what problems to explore)       │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                        TELESCOPE                                 │
│                       (Discovery)                                │
├─────────────────────────────────────────────────────────────────┤
│ Source: [To determine - Teresa Torres? JTBD? Hybrid?]           │
│ Output: Opportunity tree / discovery findings artifact          │
│ Links to: Feeds MAP (which opportunities become features)       │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                           MAP                                    │
│                     (Story Mapping)                              │
├─────────────────────────────────────────────────────────────────┤
│ Source: Jeff Patton                                              │
│ Output: User story map artifact                                  │
│ Status: IN PROGRESS                                              │
│ Links to: Scopes BLUEPRINT (what needs technical design)        │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                        BLUEPRINT                                 │
│                      (Architecture)                              │
├─────────────────────────────────────────────────────────────────┤
│ Source: [To determine - C4? ADRs? Custom?]                      │
│ Output: Architecture docs, ERDs, technical design               │
│ Links to: Guides SHIP (how code gets built)                     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Sequencing Considerations

**Dependencies:**

1. **Compass doesn't depend on anything** - it's the root. Can start immediately.

2. **Telescope depends on Compass** - you need to know your vision to know what opportunities to explore. But you can design Telescope's *structure* before Compass is complete.

3. **Map depends on Telescope** - discoveries feed the map. But Map is already in progress, so we're working backward a bit.

4. **Blueprint depends on Map** - you need to know what you're building before you architect it.

**Practical reality:**

Map is in progress. That's fine. We can:
- Complete Map as a standalone HLCS
- Build Compass and Telescope, then retroactively connect them to Map
- The integration points can be added after each instrument exists

---

## Proposed Work Plan

### Sprint 1: Compass Foundation & Adaptation

**Goal:** Get clarity on what Compass is, select methodology, define your spin

**Work:**
1. Review what you've already done on Compass
2. Survey source methodologies (Lean Canvas, Product Vision Board, etc.)
3. Select primary source or decide on hybrid
4. Document core concepts
5. Define adaptations for AI-native / HLCS context
6. Define how Compass outputs constrain Telescope inputs

**Deliverable:** Compass methodology document (Knowledge Layer foundation)

---

### Sprint 2: Compass Schema & Protocol

**Goal:** Define what the Compass artifact looks like and how human-AI collaborate to create it

**Work:**
1. Define artifact schema (fields, structure, relationships)
2. Create sample Compass artifact by hand
3. Define validation rules
4. Design collaboration protocol (phases, state machine, feedback)
5. Define how Claude Code consumes Compass during other work

**Deliverable:** Compass schema + protocol specification

---

### Sprint 3: Telescope Foundation & Adaptation

**Goal:** Same as Sprint 1, but for Telescope

**Work:**
1. Survey discovery methodologies (Teresa Torres, JTBD, etc.)
2. Select primary source or hybrid
3. Document core concepts
4. Define adaptations
5. Define how Telescope receives from Compass, feeds to Map

**Deliverable:** Telescope methodology document

---

### Sprint 4: Telescope Schema & Protocol

**Goal:** Same as Sprint 2, but for Telescope

**Deliverable:** Telescope schema + protocol specification

---

### Sprint 5: Integration Pass

**Goal:** Connect all four instruments

**Work:**
1. Define explicit links between artifacts (how Map references Telescope, etc.)
2. Define shared vocabulary / ontology across instruments
3. Review Map (in progress) for integration points
4. Stub out Blueprint requirements (enough to know what Map needs to provide)

**Deliverable:** Integration specification + updated Map schema

---

### Sprint 6+: Implementation

Build the actual HLCS tools, starting with whichever is most urgent.

---

## Question: Starting Compass

You said you've done some work on Compass already. Before we dive into Sprint 1:

1. **What source methodology did you use?** (or what were you leaning toward?)
2. **What artifacts exist?** (even rough notes or partial docs)
3. **What felt incomplete or unsatisfying about what you have?**

This will let us pick up where you left off rather than starting from scratch.



## Prompt:
11/26/2025, 7:51:50 AM

i would just make two tweaks... in phase 1 I often will have more than one thought leader contributing to the baseline and for phase 2 i think we should split that and have the "ian's spin" as the next phase and then "ai-native/hlcs" phase



## Response:
11/26/2025, 7:52:05 AM



Good refinements. Both make the process more honest about what's actually happening.

---

## Revised: Instrument Development Process

### Phase 1: Foundation
- Identify source methodologies (which thought leaders? often multiple)
- Study each deeply (core concepts, the why behind the how)
- Document the methodologies as-is (before any adaptation)
- Synthesize the baseline (what you're drawing from each source)

### Phase 2: Ian's Spin
- What's your unique perspective on this?
- Where do you disagree with the sources?
- What's missing that your experience tells you matters?
- What's overcomplicating things?
- This is your intellectual contribution, independent of AI considerations

### Phase 3: AI-Native / HLCS Adaptation
- What works for human-AI collaboration?
- What doesn't fit / needs modification for Claude Code?
- How does it fit the HLCS 5-tier model?
- What's different when "outputs become inputs"?

### Phase 4: Schema Design
- Define the artifact structure
- Create sample artifacts by hand
- Define validation rules

### Phase 5: Protocol Design
- Define phases of collaboration
- Define state machine
- Define feedback mechanisms

### Phase 6: Integration
- Define inputs from prior instrument
- Define outputs to next instrument
- Define cross-references between artifacts

### Phase 7: Implementation
- Build the HLCS tool
- Build the consumption layer

---

This separation is important because Phase 2 (your spin) produces something valuable even outside an AI context. It's your methodology. Phase 3 then adapts *that* for the specific context of working with Claude Code.

Ready to start Compass?



## Prompt:
11/26/2025, 7:54:06 AM

this all looks great, I feel like we should document this officially so we can do multiple sessions... should we make this an artifact?



## Response:
11/26/2025, 7:55:10 AM



Yes. Let me create a comprehensive document capturing everything we've established.

````plaintext
Create File: Creating the Navigation Instruments Framework document - the HLCS methodology for Compass, Telescope, Map, and Blueprint
````



Done. Here's the document:

[View Navigation Instruments Framework](computer:///home/claude/navigation-instruments-framework.md)

---

## What's Captured

1. **The Core 4 Instruments** - Compass, Telescope, Map, Blueprint with their relationships
2. **7-Phase Development Process** - Foundation → Ian's Spin → AI-Native → Schema → Protocol → Integration → Implementation
3. **Sprint-Based Work Plan** - 8 sprints taking us through Compass and Telescope, with integration pass
4. **Current State Tracking** - Table showing status of each instrument
5. **HLCS Mapping** - How each instrument maps to the 5-tier model
6. **Provisions** - Parked but documented for later

---

## Suggested Location

This should live in your Claudian docs, probably:
```
/ai-dev/claudian/docs/navigation-instruments-framework.md
```

Or if you want it closer to the HLCS doc:
```
/ai-dev/claudian/docs/human-llm-collaborative-system-pattern.md  (existing)
/ai-dev/claudian/docs/navigation-instruments-framework.md       (new)
```

---

## Ready for Sprint 1?

When you want to start on Compass, we can pick up with:

1. What existing Compass work do you have?
2. Which source methodologies are you drawing from?

The framework doc will guide us through the phases.



## Prompt:
11/26/2025, 8:02:24 AM

ok, so i have had EXTENSIVE conversations within claude with my Jackson project that covers huge amounts of product theory... are you able to review any of that? do I need to go find it myself?



## Response:
11/26/2025, 8:03:10 AM

### Mapping Jackson → Navigation Instruments

| Jackson Concept | Navigation Instrument | Status |
|-----------------|----------------------|--------|
| Vision/Strategy + Goals | **Compass** | ✅ Fully developed |
| Ideas + Initiatives | **Telescope** | ✅ Fully developed |
| Solutions + User Stories | **Map** | ⚠️ Different framing than Jeff Patton |
| (Not explicit) | **Blueprint** | ❌ Not covered |

### Key Insight: Jackson Already Has Your Telescope

The **Ideas → Initiatives** flow in Jackson IS the Telescope. It answers "What's out there? What opportunities?":

- **Ideas**: Continuous capture from all sources (stakeholders, users, team)
- **Quarterly Mining**: Pattern analysis to identify themes
- **Strategic Filtering**: Evaluate alignment with Goals
- **Initiative Development**: Frame as testable problem space hypothesis

This is exactly what Teresa Torres' Opportunity Solution Trees do, just with different vocabulary.

### The Gap: Story Mapping vs. Solutions

Jackson defines **Solutions** and **User Stories** differently than Jeff Patton's story mapping:

**Jackson's Approach:**
- Solutions = validated approaches to user problems (post-discovery)
- User Stories = vertical slices of user value for sprint delivery

**Patton's Story Mapping:**
- Story Map = the entire user workflow as Activities → Steps → Stories
- It's a planning/visualization tool, not a delivery structure

**These are complementary, not conflicting.** A Story Map helps you SEE the whole user journey; Solutions/User Stories are how you DELIVER against it.

---

## What This Means for Navigation Instruments

### Revised Assessment

| Instrument | Jackson Coverage | Gap Analysis |
|------------|-----------------|--------------|
| **Compass** | ✅ Complete | Vision/Strategy/Goals fully specified |
| **Telescope** | ✅ Complete | Ideas/Initiatives/Discovery Bridge fully specified |
| **Map** | ⚠️ Partial | Jackson has delivery structure but not Patton-style visualization |
| **Blueprint** | ❌ Missing | Technical architecture not covered |

### The Real Question

Before we continue building, I need to understand:

1. **Is Jackson the foundation?** Should Navigation Instruments be an AI-native adaptation OF Jackson, or a separate parallel framework?

2. **What's the relationship between BRIEF.yaml and Jackson?** BRIEF.yaml seems to BE the Compass artifact. But Jackson also has Vision/Strategy/Goals documentation. How do these relate?

3. **What was "incomplete" about BRIEF.yaml?** You mentioned it felt incomplete. Was that because:
   - Missing Protocol (Phase 5)?
   - Missing Telescope integration (Phase 6)?
   - Something else entirely?

4. **What's the intended scope?** Jackson was designed for a government team with 80+ staff. Claudian is 2 founders + Claude Code. How much of Jackson transfers vs. needs complete reimagining?

---

What's your thinking here? Is Jackson the source methodology for the Navigation Instruments, or is it parallel prior art that informs but doesn't define them?



## Response:
11/26/2025, 8:44:31 AM

here are some more files /Users/ianswanson/ai-dev/jackson-temp/Training



## Prompt:
11/26/2025, 8:45:54 AM


## Complete Synthesis: Jackson → Navigation Instruments → Claudian

Now I have the full picture. This is **foundational work** - you weren't starting from scratch, you had already synthesized the thought leaders into a comprehensive framework. Let me map what you have.

---

### Jackson Framework Overview

Jackson is a **complete government digital services transformation framework** that already synthesizes:

| Thought Leader | What They Contribute |
|----------------|---------------------|
| **Jeff Patton** | Story Mapping, User Story format, vertical slices |
| **Teresa Torres** | Opportunity Solution Trees, Continuous Discovery, Product Trios |
| **Melissa Perri** | Escaping the Build Trap, outcome vs output focus, Product Kata |
| **Christina Wodtke** | OKRs, outcome-focused goal setting |
| **Tim Herbig** | Product Strategy-Metrics Sandwich |
| **Jeff Gothelf** | Lean UX, hypothesis-driven development |
| **18F** | Government context (Discovery, Define, Deliver, Enable), stakeholder management |

**You already did Phase 1 (Foundation) and Phase 2 (Ian's Spin) for most of the Navigation Instruments.**

---

### Jackson Information Architecture → Navigation Instruments Mapping

```
Jackson Information Architecture          Navigation Instrument
═══════════════════════════════════════════════════════════════

STRATEGIC LAYER (Annual/Stable)
├── Vision/Strategy                   →   COMPASS
└── Goals                             →   COMPASS

IDEAS LAYER (Continuous Capture)
├── Ideas capture                     →   TELESCOPE (input)
└── Ideas mining/filtering            →   TELESCOPE (process)

TACTICAL LAYER (Flowing/Dynamic)
├── Initiatives                       →   TELESCOPE (output)
├── Solutions                         →   MAP + BLUEPRINT
└── User Stories                      →   MAP
```

---

### What Jackson Already Covers

| Navigation Instrument | Jackson Coverage | What's There |
|----------------------|------------------|--------------|
| **Compass** | ✅ **95% Complete** | Vision/Strategy/Goals fully specified. 4-phase process (Define, Discover, Design & Develop, Deliver). Dual user group management. |
| **Telescope** | ✅ **90% Complete** | Ideas capture + quarterly mining + Initiative development. Two-track routing (strategic vs operational). Discovery Bridge concept. |
| **Map** | ⚠️ **60% Complete** | Solutions + User Stories defined. BUT missing Jeff Patton's story mapping VISUALIZATION - Jackson has delivery structure, not the planning/visualization tool. |
| **Blueprint** | ⚠️ **40% Complete** | Technical landscape discovery mentioned. Architecture not deeply covered. |

---

### The Gap: Jackson → BRIEF.yaml → Claudian

Jackson was designed for:
- 80+ person government team
- Multiple PMs, UX researchers, engineers, content strategists
- Human-to-human collaboration
- Tool agnostic (Aha, Jira, etc.)

Claudian needs:
- 2 founders + Claude Code
- AI as primary "employee"
- Machine-readable artifacts
- Claude Code as the tool

**BRIEF.yaml is the HLCS adaptation layer.** It takes Jackson's Vision/Strategy/Goals (the Compass) and makes it:
1. Machine-readable (YAML)
2. Fractal (works at product → feature → epic → task)
3. Claude Code consumable

---

### Revised Status Assessment

| Phase | Compass | Telescope | Map | Blueprint |
|-------|---------|-----------|-----|-----------|
| **1. Foundation** | ✅ Jackson | ✅ Jackson | ✅ Jackson + Patton | ❓ Needs source |
| **2. Ian's Spin** | ✅ BRIEF.yaml | ⚠️ Partial | ⚠️ Partial | ❌ Not started |
| **3. AI-Native** | ✅ BRIEF.yaml | ❌ Not started | ❌ Not started | ❌ Not started |
| **4. Schema** | ✅ BRIEF.yaml | ❌ Not started | ⚠️ Started | ❌ Not started |
| **5. Protocol** | ❓ Unclear | ❌ Not started | ❌ Not started | ❌ Not started |
| **6. Integration** | ⚠️ BRIEF→Map | ❌ Not started | ❌ Not started | ❌ Not started |
| **7. Implementation** | ❓ Unclear | ❌ Not started | ❌ Not started | ❌ Not started |

---

### Key Questions for You

1. **Is Jackson the canonical source?** Should Navigation Instruments be framed as "Jackson adapted for Claudian's AI-native model"?

2. **What was incomplete about BRIEF.yaml?** You mentioned it felt incomplete. Looking at the phases:
   - Phase 5 (Protocol): How do you + Claude Code collaborate to CREATE a BRIEF? This seems undefined.
   - Phase 7 (Implementation): Is there a workflow/tool, or just the schema?

3. **Telescope already exists in Jackson.** The Ideas → Mining → Initiatives flow is Teresa Torres' Opportunity Solution Trees with different vocabulary. Do you need to build a separate "Telescope" or just AI-adapt Jackson's existing flow?

4. **Map needs Patton's visualization.** Jackson has Solutions/User Stories for delivery. But Jeff Patton's contribution is the **visual story map** that shows the whole user journey. Is that what's missing?

5. **Blueprint sources?** Jackson mentions "technical landscape discovery" but doesn't have a full architecture methodology. What thought leaders inform your architecture thinking?

---

### Proposed Path Forward

**Option A: Jackson-First**
- Treat Jackson as Phase 1-2 complete for all instruments
- Focus on Phase 3-7 (AI adaptation → Implementation) for each
- Faster, leverages existing work

**Option B: Fresh Synthesis**
- Use Jackson as reference but build Navigation Instruments from first principles
- More work, but cleaner "Claudian-native" design

**My recommendation: Option A** - You've already done tremendous synthesis work. The gap is AI-native adaptation, not methodology.

---

What's your read? Is Jackson the foundation we build on, or reference material we learn from?



## Response:
11/26/2025, 10:55:11 AM

ok, so I will say this - my thinking is constantly evolving as I build new systems at new places. As I have to articulate and create records, etc... so you know have access to a couple of years worth of thought evolution.

I want everything I've given to you up until now to form background context.

Lets proceed to discuss the compass

Lets create a compass that is not for government but rather a private for profit company

I think that a canvas is a very useful tool as part 1 of compass

I like defining the problem/opportunity *crucially this problem has to big enough to be worth paying for. Then I like to have a well structured Vision statement that kinda wraps up the details of the canvas it the "pitch" I like having the financials (the costs and the pricing model), the market aka "where are we playing" I think having the unique element aka "hard to copy". I like having a list of important things

lets start there and see what your thoughts are



## Prompt:
11/26/2025, 11:06:41 AM

**[CPO PERSPECTIVE]**

Your initial sketch hits the essential elements. Let me react to each and then surface what I think is missing:

---

### What You Have (My Read)

| Element | What I Hear | Source Framework |
|---------|-------------|------------------|
| Canvas | Structured capture of the business model | Lean Canvas, BMC |
| Problem/Opportunity | The "why" - and critically, WTP validation | JTBD, Lean Canvas |
| Vision Statement | The pitch - compressed, communicable | Moore, Pichler |
| Financials | Costs + pricing model | Unit economics, BMC |
| Market | "Where to play" | Playing to Win (Lafley) |
| Unique Element | "Hard to copy" / moat | Unfair Advantage, defensibility |
| List of Important Things | ? | Unclear - let's define |

---

### What I'd Push On

**1. Customer before Problem**

You have "market" (where to play) and "problem" (what hurts), but I don't see explicit **customer definition**. In B2B especially, the buyer ≠ user ≠ champion. Who exactly are we serving?

From your Jackson work, you had "dual user groups" (end user vs internal user). For B2B SaaS, there's often a trio:
- **Buyer** (controls budget)
- **User** (uses daily)
- **Champion** (advocates internally)

Does "market" cover this, or is customer segment separate?

**2. "Big enough to be worth paying for" - this is the money question**

I love that you're foregrounding willingness-to-pay. But I'd push further: **what's the evidence?**

A problem can be:
- Real (people have it)
- Painful (they complain about it)
- Urgent (they're actively trying to solve it)
- Valuable (they'll pay money to solve it)

Most products fail at the last two. How does the Compass force articulation of evidence that this clears the "worth paying for" bar?

**3. Why Now?**

From Sequoia's pitch deck framework - **timing is often the difference between success and failure**. The same idea in 2015 vs 2025 can have radically different outcomes. What changed that makes this possible/necessary now?

This feels missing from your list.

**4. Alternatives / Competitive Landscape**

Related to "hard to copy" but distinct: what do people do TODAY to solve this problem? The answer is never "nothing." Even if there's no direct competitor, there's:
- Manual workarounds
- Spreadsheets
- Ignoring the problem
- Hiring people

Understanding current alternatives informs positioning and WTP.

**5. "List of Important Things" - What is this?**

A few interpretations:
- **Key Assumptions** - What must be true for this to work?
- **Critical Success Factors** - What few things must go right?
- **Non-Negotiables** - What are we unwilling to compromise on?
- **Strategic Bets** - What are we betting will be true?

I suspect you mean something specific. What's the intent?

---

### What I'd Propose Adding

| Element | Purpose | Why It Matters |
|---------|---------|----------------|
| **Customer Segments** | WHO specifically | B2B requires precision - buyer vs user vs champion |
| **Why Now** | Timing thesis | What changed that creates the window |
| **Alternatives** | Current state / competition | What they do today, why it's insufficient |
| **Key Assumptions** | What must be true | Forces honesty about what we're betting on |
| **Success Metrics** | How we'll know | Goals/OKRs that connect to the vision |
| **Constraints** | Boundaries we're operating in | Budget, timeline, technical, regulatory |

---

### A Possible Structure

Based on your sketch + my additions, here's a straw-man Compass structure:

```
COMPASS
├── 1. CANVAS (the structured model)
│   ├── Customer Segments (who)
│   ├── Problem (what hurts + WTP evidence)
│   ├── Alternatives (current solutions)
│   ├── Solution (our approach)
│   ├── Unique Value Prop (why us)
│   ├── Unfair Advantage (hard to copy)
│   └── Why Now (timing thesis)
│
├── 2. VISION (the pitch)
│   └── Compressed narrative that synthesizes canvas
│
├── 3. MARKET (where to play)
│   ├── Segment definition
│   ├── TAM/SAM/SOM (if relevant)
│   └── Beachhead strategy
│
├── 4. ECONOMICS (the math)
│   ├── Pricing model
│   ├── Unit economics (CAC, LTV, margins)
│   └── Cost structure
│
├── 5. ASSUMPTIONS & RISKS (the bets)
│   ├── Key assumptions (what must be true)
│   ├── Critical risks
│   └── Validation approach
│
└── 6. SUCCESS (how we'll know)
    ├── Primary metric
    ├── Leading indicators
    └── Validation milestones
```

---

**[AI AUTOMATION ENGINEER]**

Before I go too deep on structure, I want to flag something from the HLCS pattern work:

**The Compass artifact will be consumed by downstream AI processes.** 

When Claude Code runs `/new-feature` or starts discovery work, it needs to reference the Compass to understand:
- Who are we building for?
- What problem are we solving?
- What's our moat?
- What are the constraints?

This means the structure needs to support **machine-readable queries** like:
- "What's the primary customer segment?"
- "What assumptions haven't been validated yet?"
- "What's our pricing model?"

Your BRIEF.yaml work already solved this with the fractal YAML structure. The Compass likely needs similar treatment - structured enough for AI consumption, narrative enough for human communication.

---

### Questions Back to You

1. **"List of Important Things"** - what were you envisioning?

2. **Customer vs Market** - are these the same or distinct in your thinking?

3. **Why Now** - does this belong in the canvas or is it implicit?

4. **Success Metrics / Goals** - are these part of Compass, or does that live elsewhere (OKRs at a different layer)?

5. **Validation / Evidence** - how prominently should "what we know vs what we assume" feature in the Compass?

Where do you want to dig in first?



## Response:
11/26/2025, 11:01:43 AM

1. great, yes we need customer
1. love that idea of "big enough?" and then we would have "how you making money?"
2. I like it
3. I think that market could encapsulate this, but I agree that alternatives and landscape need to be factored in
4. I think that the "list" was meant to be a place of "these are facts that are just true and matter" and maybe "here are things that we are assuming that we ultimately have to be right about"... a place where we can stay honest with ourselves and not ignore important things



## Prompt:
11/26/2025, 11:02:23 AM


**[CPO PERSPECTIVE]**

Good. This is clarifying. Let me synthesize what I'm hearing:

---

### The Emerging Compass Structure

| Section | Core Question | What It Contains |
|---------|---------------|------------------|
| **Customer** | Who exactly? | Segments, buyer/user/champion, characteristics |
| **Problem** | What hurts? Is it big enough? | Pain, urgency, evidence of WTP |
| **Solution** | How do we solve it? | Our approach, what we're building |
| **Unique Value** | Why us? Hard to copy? | Differentiation, moat, unfair advantage |
| **Market** | Where are we playing? | Landscape, alternatives, competition, why now |
| **Revenue** | How do we make money? | Pricing model, unit economics, costs |
| **Vision** | What's the pitch? | Compressed narrative, the "so what" |
| **Truths & Bets** | What's real vs what we're betting on? | Facts we can't ignore + assumptions we must be right about |

---

### On "Truths & Bets" - This Is Key

You're describing something I don't see in most frameworks but is **essential for intellectual honesty**:

**Truths** (Facts that are just true and matter):
- "Government procurement cycles are 6-18 months"
- "Oregon legislative session runs Jan-June in odd years"
- "Our target buyer has a $50K discretionary budget"
- "We have 4 months of runway"

These are constraints, context, non-negotiables. You can't wish them away.

**Bets** (Assumptions we must be right about):
- "Legislative affairs professionals will pay for AI-powered testimony analysis"
- "Our cost per analysis will be under $0.50"
- "Word-of-mouth will be our primary acquisition channel"
- "The market is big enough to support a venture-scale business"

These are hypotheses. If they're wrong, the whole thing falls apart.

---

### Why This Matters for AI-Native

**[AI AUTOMATION ENGINEER]**

This "Truths & Bets" section is gold for Claude Code consumption. When starting any feature or initiative, Claude Code can:

1. **Check constraints**: "Does this violate any Truths?"
2. **Track validation**: "Which Bets have we validated? Which are still assumptions?"
3. **Flag drift**: "This feature seems to contradict our bet that X..."

It's the intellectual honesty layer that prevents the product from slowly drifting away from reality.

---

### Proposed Compass v1 Structure

```yaml
compass:
  # WHO are we serving?
  customer:
    primary_segment: ""           # The beachhead
    buyer: ""                     # Who writes the check
    user: ""                      # Who uses it daily
    champion: ""                  # Who advocates internally
    characteristics: []           # Defining traits

  # WHAT problem are we solving?
  problem:
    description: ""               # The pain in plain language
    current_alternatives: []      # How they solve it today
    why_alternatives_fail: ""     # Why current state is insufficient
    evidence_of_wtp: ""           # Why we believe they'll pay
    
  # HOW do we solve it?
  solution:
    approach: ""                  # Our method/insight
    what_we_build: ""             # The product/service
    key_capabilities: []          # Core features/functions

  # WHY us?
  unique_value:
    differentiation: ""           # What makes us different
    hard_to_copy: ""              # The moat / unfair advantage
    why_now: ""                   # Timing thesis

  # WHERE are we playing?
  market:
    segment_definition: ""        # The space we're in
    landscape: []                 # Key players, alternatives
    size: ""                      # TAM/SAM/SOM if relevant
    beachhead: ""                 # Where we start

  # HOW do we make money?
  revenue:
    pricing_model: ""             # How we charge
    unit_economics:               
      price_point: ""
      cac: ""
      ltv: ""
      margins: ""
    cost_structure: []            # Major cost drivers

  # WHAT's the pitch?
  vision:
    statement: ""                 # The compressed narrative
    tagline: ""                   # The one-liner

  # WHAT do we know vs believe?
  truths:                         # Facts that are just true and matter
    - ""
  
  bets:                           # Assumptions we must be right about
    - assumption: ""
      validation_approach: ""
      validated: false
```

---

### Questions

1. **Vision placement** - I have it late (after all the analysis). But you mentioned "wraps up the canvas" - should Vision come earlier as the framing device, or later as the synthesis?

2. **Why Now** - I put it under "Unique Value" since it's part of "why us, why this approach." Does it deserve its own section?

3. **Beachhead** - I mention it in both Customer (primary segment) and Market. Is this duplication or are they different lenses on the same thing?

4. **Bets validation tracking** - I added `validated: false` and `validation_approach`. Is this the right level of detail for Compass, or does validation tracking belong in Telescope?

5. **What's missing?** Looking at this structure, what feels absent?



## Response:
11/26/2025, 11:04:47 AM

1. i think that the vision is what is created last as essentially an encapsulation of the canvas elements, but also becomes really the first thing you see/show to others... and I historically have liked this version: https://www.prodpad.com/blog/product-vision-template/ but can be persuaded to update it if you have better ideas
2. Seems fine
3. what do you mean by it?
4. I think we should not include tracking at this level



## Prompt:
11/26/2025, 11:04:57 AM


## Response:
11/26/2025, 11:07:19 AM

**[CPO PERSPECTIVE]**

Got it. The ProdPad template is actually Geoffrey Moore's elevator pitch structure from *Crossing the Chasm*. It's a classic:

```
FOR [target customer]
WHO [statement of need or opportunity]
THE [product name] IS A [product category]
THAT [key benefit, compelling reason to buy]
UNLIKE [primary competitive alternative]
OUR PRODUCT [statement of primary differentiation]
```

This is battle-tested. I don't have a better alternative—Moore's template has endured because it forces you to articulate the essential elements in a specific, non-weaselly way. Each blank has to be filled with something concrete.

**On your creation-order vs display-order point**: Yes, exactly. You work through all the canvas elements first, then compress them into the Moore structure. But when presenting to others, you lead with the vision statement because it's the hook. The canvas is the supporting evidence.

---

### On "Beachhead"

I was being sloppy. **Beachhead** is Moore's term for the initial market segment you focus on dominating before expanding outward. It's the "land and expand" starting point.

I mentioned it twice:
- Under Customer as "primary segment" 
- Under Market as "where we start"

That's redundant. It should live in one place. **Market** makes more sense since beachhead is fundamentally about "where we're playing first"—a market decision that then implies customer focus.

Customer section should describe WHO they are (characteristics, buyer/user/champion). Market section should describe WHERE we're playing (including beachhead as the initial focus).

---

### Revised Compass Structure (v2)

```yaml
compass:
  # THE PITCH (created last, shown first)
  vision:
    # Moore's template
    for: ""                       # Target customer
    who: ""                       # Statement of need/opportunity  
    product_name: ""              
    is_a: ""                      # Product category
    that: ""                      # Key benefit, reason to buy
    unlike: ""                    # Primary competitive alternative
    our_product: ""               # Primary differentiation

  # WHO are we serving?
  customer:
    buyer: ""                     # Who writes the check
    user: ""                      # Who uses it daily
    champion: ""                  # Who advocates internally
    characteristics: []           # Defining traits

  # WHAT problem are we solving?
  problem:
    description: ""               # The pain in plain language
    current_alternatives: []      # How they solve it today
    why_alternatives_fail: ""     # Why current state is insufficient
    big_enough: ""                # Evidence this is worth paying for
    
  # HOW do we solve it?
  solution:
    approach: ""                  # Our method/insight
    what_we_build: ""             # The product/service
    key_capabilities: []          # Core features/functions

  # WHY us?
  unique_value:
    differentiation: ""           # What makes us different
    hard_to_copy: ""              # The moat / unfair advantage
    why_now: ""                   # Timing thesis

  # WHERE are we playing?
  market:
    landscape: []                 # Key players, alternatives, context
    beachhead: ""                 # Initial segment we dominate first
    expansion_path: ""            # Where we go after beachhead (optional)

  # HOW do we make money?
  revenue:
    pricing_model: ""             # How we charge
    price_point: ""               
    cost_drivers: []              # Major costs
    unit_economics: ""            # CAC, LTV, margins (when known)

  # WHAT do we know vs believe?
  truths: []                      # Facts that are just true and matter
  
  bets: []                        # Assumptions we must be right about
```

---

### Changes from v1:

1. **Vision restructured** to Moore's template with explicit fields
2. **Removed validation tracking** from bets (per your guidance)
3. **Consolidated beachhead** into Market only
4. **Simplified customer** - removed "primary_segment" (now in Market as beachhead)
5. **Renamed "evidence_of_wtp"** to **"big_enough"** - clearer intent
6. **Simplified market** - removed TAM/SAM/SOM (can go in expansion_path if needed)
7. **Simplified revenue** - flattened structure

---

### Questions:

1. **Moore template completeness** - His structure doesn't explicitly include "why now" or financials. Those live elsewhere in our Compass. Does that feel right, or should the vision statement somehow incorporate timing/economics?

2. **Truths and Bets as lists vs structured** - I simplified to just arrays of strings. Should each bet have any structure (like a category: market bet, technical bet, customer bet)?

3. **Anything feel over-structured or under-structured?**



## Prompt:
11/26/2025, 11:10:00 AM

yeah i think the customer section is about understanding the human "who" and the market section is more the mechanics of size of group/$$$ to narrow down for finance/marketing/sales/etc
1. maybe talk to me more about the "why now" and where that theory comes from... perhaps it needs its own section?
2. i think it doesn't need specific structure
3. feels good enough to test out to me



## Response:
11/26/2025, 11:10:41 AM

**[CPO PERSPECTIVE]**

### The "Why Now" Theory

This comes from venture capital, particularly Sequoia Capital's pitch deck framework. But the underlying insight is broader than fundraising.

**The core theory**: Timing is arguably the most important factor in whether a product succeeds. Bill Gross (Idealab founder) did a famous analysis of 200+ startups and found timing was the #1 predictor of success—more than team, idea, business model, or funding.

**"Why Now" forces you to answer**: What has changed in the world that makes this opportunity possible or necessary *at this moment* rather than 5 years ago or 5 years from now?

---

### Common "Why Now" Categories

| Category | Example |
|----------|---------|
| **Technology shift** | "LLMs can now analyze testimony at $0.10/document vs $50/hour for a human" |
| **Regulatory change** | "New transparency law requires agencies to respond to all public testimony" |
| **Behavioral shift** | "COVID normalized remote public comment, increasing testimony volume 10x" |
| **Cost curve** | "Cloud + AI costs dropped enough to make per-document pricing viable" |
| **Market maturity** | "GovTech is now a recognized category with proven procurement paths" |
| **Competitive gap** | "Incumbents are 15-year-old on-prem systems that can't adapt" |
| **Convergence** | "Multiple factors aligning simultaneously" (often the strongest) |

---

### For Claudian/LobbySherpa, "Why Now" Might Be:

- LLM capabilities crossed the threshold for reliable testimony analysis (2023-2024)
- AI costs dropped to enable per-analysis pricing model
- Government agencies are under modernization pressure post-COVID
- Existing legislative tracking tools haven't incorporated AI meaningfully
- Oregon's session timing creates a natural pilot window (Jan 2026)

**This is your timing thesis.** If any of these factors weren't true, the opportunity either wouldn't exist or would be much harder.

---

### Does It Deserve Its Own Section?

**Arguments for standalone section:**
- Important enough that every serious investor/buyer asks about it
- Conceptually distinct from "why us" (differentiation) and "where" (market)
- Forces explicit articulation rather than hoping it's implied
- When timing thesis is wrong, entire business fails—deserves prominence

**Arguments against:**
- Could nest under Market (market conditions that enable this)
- Could nest under Unique Value (timing as part of our advantage)
- Some products don't have dramatic "why now"—stable markets, evergreen problems
- More sections = more complexity

---

### My Take

**Give it its own section.** Here's why:

"Why Now" is existential in a way that other elements aren't. You can have the right customer, problem, solution, differentiation, and market—and still fail because timing is wrong. It's not a sub-element of something else; it's a peer-level consideration.

Also, for AI-native development, having an explicit timing thesis helps Claude Code understand context. "Why are we building this NOW and not waiting?" is a question that informs urgency, prioritization, and scope decisions.

---

### Revised Structure (v3)

```yaml
compass:
  # THE PITCH (created last, shown first)
  vision:
    for: ""                       # Target customer
    who: ""                       # Statement of need/opportunity  
    product_name: ""              
    is_a: ""                      # Product category
    that: ""                      # Key benefit, reason to buy
    unlike: ""                    # Primary competitive alternative
    our_product: ""               # Primary differentiation

  # WHO are we serving?
  customer:
    buyer: ""                     # Who writes the check
    user: ""                      # Who uses it daily
    champion: ""                  # Who advocates internally
    characteristics: []           # Defining traits

  # WHAT problem are we solving?
  problem:
    description: ""               # The pain in plain language
    current_alternatives: []      # How they solve it today
    why_alternatives_fail: ""     # Why current state is insufficient
    big_enough: ""                # Evidence this is worth paying for
    
  # HOW do we solve it?
  solution:
    approach: ""                  # Our method/insight
    what_we_build: ""             # The product/service
    key_capabilities: []          # Core features/functions

  # WHY us?
  unique_value:
    differentiation: ""           # What makes us different
    hard_to_copy: ""              # The moat / unfair advantage

  # WHY now?
  timing:
    thesis: ""                    # What changed that enables/demands this
    factors: []                   # Technology, regulatory, behavioral, cost, market shifts
    window: ""                    # How long is this window open? (optional)

  # WHERE are we playing?
  market:
    landscape: []                 # Key players, alternatives, context
    beachhead: ""                 # Initial segment we dominate first
    size: ""                      # TAM/SAM/SOM or qualitative sizing

  # HOW do we make money?
  revenue:
    pricing_model: ""             # How we charge
    price_point: ""               
    cost_drivers: []              # Major costs
    unit_economics: ""            # CAC, LTV, margins (when known)

  # WHAT do we know vs believe?
  truths: []                      # Facts that are just true and matter
  bets: []                        # Assumptions we must be right about
```

---

### Changes from v2:

1. **Added standalone `timing` section** with thesis, factors, and optional window
2. **Removed "why_now" from unique_value** - now has its own home
3. **Added `size` back to market** - you mentioned "mechanics of size/$$" belongs there

---

Ready to test this out? Want to fill one out for LobbySherpa as the proof case?



## Prompt:
11/26/2025, 11:12:07 AM

before testing, I don't want to burn through all our limits of conversations... where are we in our process of building out this hlcs?



## Response:
11/26/2025, 11:12:37 AM

**[AI AUTOMATION ENGINEER]**

Good check. Let me map where we are against the 7-phase process from your Navigation Instruments Framework:

---

### Compass Development Status

| Phase | Status | What We've Done | What Remains |
|-------|--------|-----------------|--------------|
| **1. Foundation** | ✅ Complete | Jackson synthesis, Moore's template, Sequoia "Why Now", Lean Canvas concepts | — |
| **2. Ian's Spin** | ✅ Complete | Truths & Bets, "big enough" framing, structure refinements | — |
| **3. AI-Native Adaptation** | ⚠️ Implicit | Discussed Claude Code consumption, YAML structure | Explicit HLCS 5-tier mapping |
| **4. Schema Design** | ⚠️ Draft | v3 YAML structure defined | Sample artifact, validation rules |
| **5. Protocol Design** | ❌ Not started | — | Phases, state machine, feedback mechanisms |
| **6. Integration** | ❌ Not started | — | Compass → Telescope handoff, cross-references |
| **7. Implementation** | ❌ Not started | — | Tool, consumption documentation |

---

### Where We Are

We're at the **end of Phase 2, partway through Phases 3-4**.

We have a schema draft but haven't:
1. Validated it with a real artifact (filling one out for LobbySherpa)
2. Defined validation rules (what makes a Compass valid/invalid)
3. Designed the collaboration protocol (how human + AI create/refine this together)
4. Defined integration points (what Telescope expects from Compass)

---

### Suggested Next Steps (When Ready)

**Cheapest validation**: Fill out LobbySherpa Compass by hand (you, not AI). This tests whether the schema actually works before we invest in protocol/tooling.

**Then**: Decide if protocol design is worth it now or if Compass is "simple enough" to skip formal HLCS tooling and just use the schema as a template.

Want me to save the current v3 schema somewhere so we can pick this up later?



## Prompt:
11/26/2025, 11:25:34 AM

so it strikes me that the knowledge layer is essentially also what we were just going through, determing the underlying concepts... how do we factor that in to our phases?



## Response:
11/26/2025, 11:26:03 AM

**[AI AUTOMATION ENGINEER]**

You're right. The 7 phases are a *development process*, but they don't cleanly map to the HLCS 5-tier *architecture*. Let me reconcile these:

---

### The Relationship

| Development Phase | Primary HLCS Tier Being Built |
|-------------------|-------------------------------|
| 1. Foundation | Knowledge Layer (ontological - what IS this thing) |
| 2. Ian's Spin | Knowledge Layer (evaluative - what makes it GOOD) |
| 3. AI-Native Adaptation | Knowledge Layer (procedural - how to CREATE it with AI) |
| 4. Schema Design | Schema Layer |
| 5. Protocol Design | Interaction Layer |
| 6. Integration | Cross-HLCS relationships (not a tier, a system concern) |
| 7. Implementation | Data Layer + Presentation Layer |

---

### What This Reveals

**Phases 1-3 are all Knowledge Layer work.** We've been building:

- **Ontological**: What is a Compass? (Moore's vision template, canvas elements, timing thesis)
- **Evaluative**: What makes a good one? (Must be specific, non-weaselly, "big enough" evidence)
- **Procedural**: How do you create one? (Work through canvas, compress to Moore format, vision created last/shown first)

We just didn't label it as Knowledge Layer work—but that's what it was.

---

### Revised Phase Model

Maybe the phases should make the tier-mapping explicit:

---

### Updated Compass Status

| HLCS Tier | Status | Evidence |
|-----------|--------|----------|
| **Knowledge Layer** | ⚠️ ~80% | We have ontological + evaluative. Procedural is implicit but not documented. |
| **Schema Layer** | ⚠️ ~60% | v3 structure exists. No validation rules, no tested sample. |
| **Interaction Layer** | ❌ 0% | No protocol defined |
| **Data Layer** | ❌ 0% | No storage/persistence |
| **Presentation Layer** | ❌ 0% | No visualization |

---

### The Question This Raises

**Do we need to capture the Knowledge Layer work we just did?**

Right now it exists in this conversation. If you start a new Claude Code session to build a Compass, that session won't know:
- Why Moore's template
- Why "Truths & Bets" matters
- Why timing deserves its own section
- What "big enough" means

Should we document this as a Knowledge Layer artifact before moving to schema validation?



## Prompt:
11/26/2025, 11:29:33 AM

i think integration can go after implementation

and I think we do want to capture the knowledge layer now since we have a v1 of the schema, in order to work on the interaction layer we need to have the knowledge that informs that conversation *i think



## Response:
11/26/2025, 11:30:10 AM

**[AI AUTOMATION ENGINEER]**

Agreed on both counts. Updated phase model:

```
KNOWLEDGE LAYER
├── Phase 1: Foundation (source methodologies)
├── Phase 2: Ian's Spin (unique contributions)  
└── Phase 3: AI-Native Adaptation (HLCS fit)

SCHEMA LAYER
└── Phase 4: Schema Design

INTERACTION LAYER
└── Phase 5: Protocol Design

IMPLEMENTATION
└── Phase 6: Data + Presentation Layers

INTEGRATION
└── Phase 7: Cross-Instrument Connections
```

---

### Knowledge Layer Documentation

Let me propose what we'd capture:

**Compass Knowledge Layer v1**

```markdown
# Compass - Knowledge Layer

## Ontological (What IS a Compass?)

### Definition
The Compass is the strategic foundation artifact that answers: "Where are 
we going and why?" It establishes true north for all downstream product 
decisions.

### Core Concepts

**Vision Statement (Moore's Template)**
Geoffrey Moore's elevator pitch structure from Crossing the Chasm:
- FOR [target customer]
- WHO [statement of need/opportunity]
- THE [product] IS A [category]
- THAT [key benefit]
- UNLIKE [competitive alternative]
- OUR PRODUCT [primary differentiation]

Created last (after working through all elements), shown first (the hook).

**Customer (The Human "Who")**
Three distinct roles in B2B:
- Buyer: writes the check
- User: uses it daily
- Champion: advocates internally

Understanding characteristics of each informs messaging, UX, and sales.

**Problem**
Must clear the "big enough" bar:
- Real (they feel it)
- Painful (it hurts)
- Urgent (needs solving now)
- Valuable (worth paying to fix)

Most products fail at urgent and/or valuable.

**Current Alternatives**
Never "nothing." People solve problems today via:
- Manual workarounds
- Spreadsheets
- Ignoring the problem
- Hiring people
- Competitor products

Understanding alternatives informs positioning and WTP.

**Timing Thesis (Why Now)**
From Sequoia's pitch framework. Bill Gross research: timing is #1 
predictor of startup success.

Categories of timing shifts:
- Technology shift
- Regulatory change
- Behavioral shift
- Cost curve crossing
- Market maturity
- Competitive gap
- Convergence (multiple factors)

If timing thesis is wrong, business fails regardless of other factors.

**Market (Mechanics)**
Where we're playing:
- Landscape (players, alternatives)
- Beachhead (initial segment to dominate)
- Size (TAM/SAM/SOM or qualitative)

Distinct from Customer (human who) - Market is the mechanics of 
segmentation, sizing, competitive positioning.

**Revenue (How We Make Money)**
- Pricing model
- Price point
- Cost drivers
- Unit economics (when known)

**Truths & Bets (Intellectual Honesty Layer)**
Two categories:

Truths: Facts that are just true and matter. Constraints, context, 
non-negotiables. Can't be wished away.

Bets: Assumptions we must be right about. Hypotheses that, if wrong, 
collapse the entire thesis.

This section prevents drift from reality.

---

## Evaluative (What Makes a Good Compass?)

### Quality Criteria
- **Specific, not vague**: Each field filled with concrete content
- **Non-weaselly**: Moore's template forces commitment
- **Evidence-backed**: "Big enough" has supporting evidence
- **Intellectually honest**: Truths & Bets don't hide uncomfortable realities
- **Compressible**: Vision statement works as 30-second pitch

### Anti-Patterns
- Lofty vision with no specifics
- Problem statement without WTP evidence
- Missing timing thesis (assuming "now" without articulating why)
- Buyer/user/champion collapsed into generic "customer"
- Empty Truths & Bets (everything looks rosy)
- Alternatives listed as "nothing" or only direct competitors

---

## Procedural (How Do You Create a Compass?)

### Creation Order
1. Work through canvas elements (Customer, Problem, Solution, etc.)
2. Each element informs the others (iterate as understanding deepens)
3. Truths & Bets crystallize through the process
4. Vision statement created LAST as compression of everything above

### Display Order
1. Vision statement FIRST (the hook)
2. Supporting elements provide evidence and depth
3. Truths & Bets as grounding/honesty check

### Iteration Expectation
Compass is not static. Returns to update when:
- Major bet validated or invalidated
- Market conditions shift
- Pivot or significant scope change
- New truth emerges

---

## AI-Native Considerations

### Claude Code Consumption
Compass artifact feeds downstream processes:
- `/new-feature` references customer, problem, unique value
- Discovery work checks against timing thesis
- Scope decisions reference beachhead
- Trade-offs weigh against truths/constraints

### Machine Readability
YAML structure enables queries:
- "What's our primary customer segment?"
- "What bets haven't been validated?"
- "What's our pricing model?"

### Stateless Session Support
Each Claude Code session starts fresh. Compass provides:
- Context without re-explanation
- Constraints without re-discovery
- Strategic grounding for tactical decisions
```

---

### Questions

1. **Does this capture what we discussed?** What's missing or mischaracterized?

2. **Where should this live?** Options:
   - `/docs/compass-knowledge-layer.md`
   - `/hlcs/compass/knowledge.md`
   - Inside a broader Compass HLCS directory structure

3. **Should the schema be in the same doc or separate?** I lean separate (Knowledge Layer doc + Schema doc), but could combine.



## Prompt:
11/26/2025, 11:33:15 AM

it feels like a good v1

just fyi we have been iterative on the hlcs now for a bit, you can see it here: /Users/ianswanson/ai-dev/claudian/products/story-mapper that was the first one and thne the 2nd one : /Users/ianswanson/ai-dev/claudian/products/compass



## Response:
11/26/2025, 11:45:15 AM


**[AI AUTOMATION ENGINEER]**

This is illuminating. Let me surface what I found:

---

### What Already Exists in `/products/compass/`

| Component | Status | Content |
|-----------|--------|---------|
| **Implementation** | Advanced | Next.js + Electron app, tests, CI/CD |
| **Knowledge Layer** | Exists | Roman Pichler's Product Canvas methodology |
| **Schema** | Implied | `/data/types.ts` (didn't read yet) |
| **Interaction Protocol** | Sketched | Discovery → Generation → Review → Refinement → Approval |
| **Data Layer** | In-memory | `/data/canvases.ts` |
| **Presentation** | Built | React components for canvas display |

---

### The Methodology Mismatch

The existing Compass uses **Roman Pichler's Product Canvas**:
- Name & Goal
- Personas (3-7 with pain points)
- Big Picture (User Journeys, Epics, Design Elements, Constraint Stories)
- Product Details (Sprint-level user stories)

What we've been designing today is **different**:
- Vision (Moore's template)
- Customer (buyer/user/champion)
- Problem (with "big enough" evidence)
- Solution
- Unique Value (differentiation + moat)
- Timing (why now)
- Market (landscape, beachhead, size)
- Revenue (pricing, economics)
- Truths & Bets

---

### The Relationship Question

These feel like **different levels of abstraction**:

| Our Compass (Strategic) | Pichler Canvas (Tactical) |
|------------------------|---------------------------|
| Why build this? | What to build? |
| Is this worth doing? | How do we do it? |
| Vision, market, revenue | Personas, journeys, epics |
| Pre-commit | Post-commit |
| "Should we?" | "How should we?" |

**Possible interpretations:**

1. **They're the same thing** - and we need to reconcile methodologies
2. **They're different things** - and both are needed (our Compass → Pichler Canvas → Story Map)
3. **The existing work should be renamed** - it's not really a "Compass" in the Navigation Instruments sense

---

### My Question

What's the relationship between:
- What we designed today (strategic Compass with Moore, Timing, Truths & Bets)
- What exists in `/products/compass/` (Pichler's Product Canvas implementation)

Are these:
- **The same artifact** needing methodology reconciliation?
- **Different artifacts** where our Compass feeds into Pichler's Canvas?
- **Something else**?

This affects whether we update the existing Knowledge Layer or create something new.



## Prompt:
11/26/2025, 11:36:01 AM

i went with roman's because I was trying to test out the whole process and the interaction and visualization... I was never attached to the theory and schema... what we created today is way way better



## Response:
11/26/2025, 11:36:26 AM


**[AI AUTOMATION ENGINEER]**

Got it. That clarifies everything.

**The situation:**
- Implementation infrastructure is solid (Next.js, Electron, tests, CI/CD)
- Methodology/schema was placeholder (Pichler was a test vehicle)
- What we built today is the real thing

---

### Revised Status

| Layer | Existing State | New State (Today's Work) |
|-------|----------------|--------------------------|
| **Knowledge Layer** | Pichler methodology (placeholder) | Moore + Timing + Truths & Bets (real) |
| **Schema Layer** | `/data/types.ts` (Pichler structure) | v3 YAML structure (needs replacement) |
| **Interaction Layer** | Sketched protocol | Same (not developed yet) |
| **Data Layer** | In-memory canvases | Same infrastructure, new schema |
| **Presentation Layer** | React components | Needs UI updates for new schema |
| **Implementation** | Next.js + Electron ✅ | Keep as-is |

---

### What Needs to Happen

1. **Document Knowledge Layer** → Replace `product-canvas-methodology.md` with what we developed today
2. **Update Schema** → Replace `/data/types.ts` with our v3 structure
3. **Design Protocol** → The interaction layer (Phase 5)
4. **Update UI** → Adapt presentation to new schema

The infrastructure investment is preserved. We're just swapping out the content/methodology.

---

### Proposed Next Step

**Write the Knowledge Layer document** based on our conversation today. This would replace the existing Pichler methodology file with:

- Ontological (Moore's template, Customer, Problem, Timing thesis, etc.)
- Evaluative (quality criteria, anti-patterns)
- Procedural (creation order vs display order, iteration expectations)
- AI-Native considerations (Claude Code consumption, machine readability)

This captures what we discussed before we lose it, and becomes the foundation for schema and protocol work.

Want me to draft that document now?



## Prompt:
11/26/2025, 11:37:28 AM

yes create the doc as an artifact so i don't hit a limit, then I want to ask some more questions



## Response:
11/26/2025, 11:39:43 AM



## Prompt:
11/26/2025, 11:41:16 AM

are you done?



## Response:
11/26/2025, 11:41:23 AM

Yes, the document is created. 

[View the Compass Knowledge Layer v1](computer:///home/claude/compass-knowledge-layer-v1.md)

What are your questions?



## Prompt:
11/26/2025, 11:43:53 AM

ok, it is the story mapper that had a much more thought out and rigorous knowledge layer... I had a lot of very specific things to say about that, so I think its worth you taking a peak at that and for us to consider how we should be structuring the knowledge layer

I'm fine just testing it and figuring it out as we go, just wanted to mention it now



## Response:
11/26/2025, 11:46:19 AM

Now I see what you mean. The story mapper has **extremely rigorous procedural documentation** with:

1. **Explicit abstraction level guidance** - Tables showing "Too Abstract" vs "Just Right" vs "Too Specific"
2. **Anti-pattern examples** - Good vs Bad explicitly contrasted
3. **Validation checklists** - Concrete "before returning, verify" lists
4. **The "So That" test** - A heuristic for checking correct level
5. **Confidence checks** - "If less than 90% confident..."
6. **Verb prohibition lists** - "DO NOT use these verbs"

Let me see if there's more in the reference and docs folders:

This is really valuable. The story mapper's knowledge layer is **dramatically more rigorous**. Here's what I'm seeing:

---

### Story Mapper Knowledge Layer Patterns

**1. Abstraction Level Tables** - Explicit comparisons:
```
| Activities (Too Abstract) | Tasks (Just Right) | Details (Too Specific) |
|---------------------------|-------------------|----------------------|
| Get Transportation        | Request Ride       | Enter destination address |
```

**2. Verb Prohibition Lists** - "DO NOT use these verbs":
- Click, Tap, Press, Swipe
- See, View, Display, Show
- Drag, Drop, Scroll

**3. The "So That" Test** - Reusable heuristic:
> "A detail is appropriately sized if you cannot decompose it further without losing the verb FROM THE USER'S PERSPECTIVE"

**4. 90% Confidence Threshold**:
> "If you are less than 90% confident about what level something belongs at, ask for clarification rather than guessing."

**5. Validation Checklists** - Checkbox format before output

**6. Good vs Bad Example Pairs** - Every concept has both

**7. Transformation Patterns**:
- ❌ "Click save button" → ✅ "Preserve work without losing changes"
- ❌ "See error message" → ✅ "Understand what went wrong and how to fix it"

---

### The Compass Knowledge Layer Gap

What I drafted has:
- ✅ Ontological content (what the sections ARE)
- ✅ Basic quality criteria per section
- ⚠️ Weak procedural guidance (no validation checklists, no transformation patterns)
- ❌ No abstraction level tables
- ❌ No 90% confidence rules
- ❌ No explicit "DO NOT" patterns
- ❌ Sparse examples (one per section vs multiple good/bad pairs)

---

### Your Call

We can either:

**A) Test it as-is** - See where it breaks in practice, iterate based on actual failure modes

**B) Strengthen now** - Apply story mapper rigor patterns before testing

Given your "fine just testing it" comment, I'd lean toward **A** - the failure modes will teach us exactly where to add rigor, rather than guessing what needs it.

What are your other questions?



## Prompt:
11/26/2025, 11:48:53 AM

ok cool... now next question

The Compass, aka "where are we going" is more than just a canvas

It also includes the "roadmap" which i have a lot of ideas about

what do we do with that fact? make the compass broader? make sub-sections of the compass?



## Response:
11/26/2025, 11:49:29 AM

**[STRATEGIC ADVISOR]**

This is a great architectural question. Let me think through it...

---

### The Compass Metaphor

"Where are we going?" naturally includes TWO things:

| Component | Question | Nature |
|-----------|----------|--------|
| **Destination** | What's true north? | Relatively static (changes with pivots) |
| **Course** | How do we get there over time? | More dynamic (changes with learning) |

The canvas we designed today is the **Destination**. The roadmap is the **Course**.

---

### Options

**Option A: Compound Compass**
```
Compass/
├── Canvas (what we built today)
└── Roadmap (Ian's ideas)
```
- Pro: Metaphor holds - compass helps you know both destination AND plot course
- Pro: Single "instrument" with two views
- Con: More complex artifact

**Option B: Separate Instruments**
```
Compass → Roadmap → Telescope → Map → Blueprint
```
- Pro: Clean separation
- Con: Now 5 instruments, breaks the pattern
- Con: Roadmap doesn't fit nautical instrument metaphor well

**Option C: Roadmap is part of Story Map**
- The Map already has "Releases" (delivery sequence)
- Maybe roadmap is just a higher-level release plan?
- Con: Conflates strategic planning with tactical planning

---

### My Intuition

**Option A (Compound Compass)** feels right because:

1. **Nautical coherence**: A real compass helps you both find north AND plot a course
2. **Abstraction match**: Both canvas and roadmap are strategic (vs tactical Map/Blueprint)
3. **Consumption pattern**: Claude Code would reference both when making strategic decisions

Structure might be:
```
Compass/
├── Canvas/        # "What's true north?" (static-ish)
│   └── compass-canvas.yaml
├── Roadmap/       # "What's our course?" (more dynamic)
│   └── roadmap.yaml
└── CLAUDE.md      # Knowledge layer covering both
```

---

### Before We Decide

What are your roadmap ideas? Understanding what you're envisioning will help determine if compound Compass makes sense or if it needs its own instrument.

Specifically:
- What does a "roadmap" contain in your mind?
- How does it relate to the Story Map releases?
- What makes it distinct from tactical planning?



## Prompt:
11/26/2025, 11:52:52 AM





## Response:
11/26/2025, 11:53:31 AM

This is excellent. Now I see the full picture.

---

### What the Roadmap Adds

| Canvas (What we built today) | Roadmap (Your template) |
|------------------------------|-------------------------|
| Vision (Moore pitch) | Vision (5+ year sci-fi) |
| Customer, Problem, Solution | Strategy + Approach |
| Unique Value, Timing, Market | Goals (1-2 year measurable outcomes) |
| Revenue | Goal Progress Tracking |
| Truths & Bets | Time Horizons (Now/Next/Later) |
| | Capacity Allocation (60/20/20) |
| | Work Type Categories |

---

### Key Insights from Your Template

1. **Language Progression** - Now (concrete delivery) → Next (solutioning) → Later (problems to explore)
   - This is brilliant. Specificity decreases as time horizon increases.

2. **Goals are behavior changes** - Not features, not outputs. User behavior changes with measurable baselines/targets.

3. **Capacity as explicit constraint** - 60% strategic, 20% small requests, 20% operational
   - Forces honesty about what you can actually do

4. **Work organized by Goal** - Each row shows all work advancing a specific outcome
   - Everything connects back to measurable progress

5. **Mandated work acknowledged** - "Required: work not tied to goals"
   - Intellectual honesty about constraints

---

### How They Relate

```
COMPASS CANVAS                    COMPASS ROADMAP
(The Thesis)                      (The Course)
─────────────────────────────────────────────────────
Vision (30-sec pitch)        →    Vision (5+ year sci-fi)
                                  Strategy + Approach
Problem + Solution           →    Goals (measurable outcomes)
                                  Progress Tracking
Truths & Bets               →    Capacity Constraints
                                  Time Horizons
                                  Work Categories
```

The **Canvas** is the positioning statement - relatively stable.
The **Roadmap** is the execution plan - reviewed quarterly.

---

### Compound Compass Structure

```
Compass/
├── Canvas/                    # "What's our position?"
│   └── compass-canvas.yaml    #  Moore pitch, Customer, Problem, etc.
│
├── Roadmap/                   # "What's our course?"
│   └── roadmap.yaml           #  Vision, Strategy, Goals, Now/Next/Later
│
└── Knowledge Layer/           # Covers both
    └── compass-methodology.md
```

---

### The Abstraction Relationship

| Level | Canvas | Roadmap |
|-------|--------|---------|
| **Why** | Vision (pitch) | Vision (sci-fi) |
| **What** | Problem/Solution | Goals (behavior changes) |
| **How** | Approach | Strategy + Approach |
| **When** | Timing (why now) | Now/Next/Later |
| **Constraints** | Truths & Bets | Capacity allocation |

They're **complementary views of the same strategic layer** - different enough to be separate artifacts, related enough to be one instrument.

---

### Question

Does this framing feel right? Compound Compass with Canvas (position) + Roadmap (course)?

Or do you see them differently?



## Prompt:
11/26/2025, 11:58:46 AM

so what we are calling vision in the canvas I would probably rename it Pitch and then the vision can be a prose statement that is inspriational... it what makes you come into the office and dedicate yourself to the pursuit. the problem/solution on the canvas is the highest level problem/solution that is the sum of all the things the product is going to do in exchange for the users money... the goals in the roadmap are timeboxed behavioral goals that are the current focus. I'm not positive what the how approach is on the canvas, but I would say that the canvas in general is a business document that C-suite use to make the company be profitable, that investors would use... granted a company can sell more than one product, but we would think of this as a product=company... i can't find the exact words, but one is written as a business document with a somewhat clinical look at operations... the roadmap is meant to tie more to the product process. it is something updated quarterly. its a coordination document for lack of a better term.



## Response:
11/26/2025, 11:59:26 AM

This is a really important clarification. Let me reflect back what I'm hearing:

---

### The Two Documents

| Canvas | Roadmap |
|--------|---------|
| **Business document** | **Coordination document** |
| C-suite, investors | Team, stakeholders |
| Clinical, operational | Product process |
| "Is this business viable?" | "What are we doing now?" |
| Changes with pivots | Updated quarterly |
| Product = Company level | Product development level |

---

### Terminology Fix

What we called **Vision** (Moore template) → **Pitch**

**Vision** should be:
- Inspirational prose
- "Why you come into the office"
- The thing that makes you dedicate yourself to the pursuit
- Not a template - a statement

---

### Where Does Vision Live?

Looking at your roadmap template, you have "VISION (5+ years)" at the top as the inspirational sci-fi future.

Options:

**A) Vision on Canvas, referenced by Roadmap**
- Canvas has the inspirational Vision (stable, foundational)
- Roadmap references it but doesn't duplicate it
- Makes sense: Vision is "why we exist" - that's a business question

**B) Vision on Roadmap, Canvas has Pitch only**
- Canvas is purely operational/clinical
- Roadmap carries the inspirational element
- Makes sense: Roadmap is where team looks, they need the inspiration

**C) Vision shared/duplicated**
- Both have it
- Redundancy but ensures it's always visible

My instinct: **Option A** - Vision lives on Canvas (it's foundational "why"), Roadmap starts with Goals that ladder up to that Vision.

---

### Revised Canvas Structure

```yaml
compass_canvas:
  # THE INSPIRATION
  vision: ""                      # Prose statement - why you come to work
  
  # THE PITCH (Moore template)
  pitch:
    for: ""                       # Target customer
    who: ""                       # Statement of need/opportunity  
    product_name: ""              
    is_a: ""                      # Product category
    that: ""                      # Key benefit
    unlike: ""                    # Primary alternative
    our_product: ""               # Primary differentiation

  # THE BUSINESS CASE
  customer:
    buyer: ""
    user: ""
    champion: ""
    characteristics: []

  problem:                        # Highest level - sum of all product value
    description: ""
    current_alternatives: []
    why_alternatives_fail: ""
    big_enough: ""
    
  solution:
    approach: ""                  # (you're not sure about this one)
    what_we_build: ""
    key_capabilities: []

  unique_value:
    differentiation: ""
    hard_to_copy: ""

  timing:
    thesis: ""
    factors: []

  market:
    landscape: []
    beachhead: ""
    size: ""

  revenue:
    pricing_model: ""
    price_point: ""
    cost_drivers: []
    unit_economics: ""

  truths: []
  bets: []
```

---

### Question on "Approach"

You mentioned you're not sure what "Approach" is on the Canvas. 

In my head it was: "Our method/insight for solving the problem" - the *how* at a strategic level (e.g., "AI-powered document analysis" vs "human reviewers").

But if Canvas is purely business/clinical, maybe Approach belongs on Roadmap under Strategy instead?

What's your instinct on where "how we're going to do this" lives?



## Prompt:
11/26/2025, 12:00:45 PM

i don't mean to make one sound sterile and one to sound like poetry... they just are looking at things from a different angle. Attempting to communicate to different audiences different elements. they are complimentary 100% and ultimately we want to avoid overlap/duplication. and if we are finding any, we should figure out how to reconcile



## Response:
11/26/2025, 12:01:19 PM

Got it. Complementary angles, different audiences, zero duplication. Let me try to draw a clean line.

---

### The Reconciliation Exercise

| Element | Canvas (Business Case) | Roadmap (Coordination) | Overlap? |
|---------|------------------------|------------------------|----------|
| Vision (inspirational) | Lives here | References Canvas | ✓ Reconcile |
| Pitch (Moore) | ✓ | - | Clean |
| Customer | ✓ | - | Clean |
| Problem (aggregate) | ✓ | - | Clean |
| Solution (aggregate) | ✓ | - | Clean |
| Strategy | ? | Lives in template | ? |
| Approach | ? | Lives in template | ? |
| Goals (timeboxed) | - | ✓ | Clean |
| Now/Next/Later | - | ✓ | Clean |
| Capacity | - | ✓ | Clean |
| Unique Value | ✓ | - | Clean |
| Timing (Why Now) | ✓ | - | Clean |
| Market | ✓ | - | Clean |
| Revenue | ✓ | - | Clean |
| Truths & Bets | ✓ | - | Clean |

---

### The Overlaps to Reconcile

**1. Vision**
- Your roadmap template has "VISION (5+ years)" at top
- We put Vision on Canvas
- **Proposal:** Vision is foundational, lives on Canvas. Roadmap *displays* it for context but doesn't own it. Single source of truth = Canvas.

**2. Strategy + Approach**
- Your roadmap template has both
- Canvas has... unclear
- **Question for you:** Is Strategy ("how we win in the market") a business-case thing (Canvas) or a coordination thing (Roadmap)? 

My instinct: Strategy feels like it bridges. It's strategic enough for investors but operational enough for team coordination.

---

### Two Ways to Cut It

**Option A: Strategy on Canvas**
```
Canvas owns: Vision, Pitch, Customer, Problem, Solution, Strategy, Unique Value, Timing, Market, Revenue, Truths & Bets

Roadmap owns: Goals, Progress Tracking, Now/Next/Later, Capacity
Roadmap references: Vision, Strategy (from Canvas)
```

**Option B: Strategy on Roadmap**
```
Canvas owns: Vision, Pitch, Customer, Problem, Solution, Unique Value, Timing, Market, Revenue, Truths & Bets

Roadmap owns: Strategy, Approach, Goals, Progress Tracking, Now/Next/Later, Capacity
Roadmap references: Vision (from Canvas)
```

---

Which feels right to you? Or is there a third cut I'm not seeing?



## Prompt:
11/26/2025, 12:03:51 PM

ok, this is great, we can sort this out as we go

which brings me to my next point

our core example that we should use for everything is using Trello, circa when it was first launched into the market as our way of testing this all out and use it as examples throughout the artifacts and docs we create



## Response:
11/26/2025, 12:04:10 PM

This is a great call. One canonical example that flows through everything:

- Compass Canvas (Trello's business case)
- Compass Roadmap (Trello's coordination plan)
- Story Map (Trello's user journey)
- Schema examples
- Knowledge layer anti-patterns

---

### Why Trello Works

- **Simple enough** to understand in 30 seconds
- **Complex enough** to be interesting (boards, lists, cards, collaboration)
- **Well-documented history** - lots written about early Fog Creek/Trello strategy
- **B2B SaaS** - relevant to your domain
- **Everyone knows it** - no explanation needed
- **Story mapper already uses it** - Kanban board examples in the prompts

---

### "Circa Launch" - What We're Modeling

Trello launched **September 2011** out of Fog Creek Software. At that point:

- Free product, no revenue model yet
- Targeting small teams, individuals
- Competing against: spreadsheets, whiteboards, Basecamp, sticky notes
- Core value prop: visual, simple, flexible
- Joel Spolsky / Michael Pryor backing

Do you want to model **actual historical Trello** (research what they really did) or **fictional early Trello** (what a reasonable founding team might have done)?

The former requires some research. The latter gives us more flexibility to demonstrate the methodology cleanly.



## Prompt:
11/26/2025, 12:06:14 PM

the latter



## Response:
11/26/2025, 12:06:27 PM

Perfect. **Fictional Early Trello** - what a reasonable founding team *might* have done, optimized to demonstrate the methodology.

---

### What This Gives Us

We can craft the example to:
- Hit every section of the Canvas cleanly
- Have clear Truths & Bets (some we "know" were validated)
- Show interesting Timing thesis (why 2011?)
- Demonstrate Now/Next/Later progression on Roadmap
- Flow naturally into Story Map (Activities → Tasks → Details)
- Show good/bad examples at each abstraction level

---

### Fictional Trello "Facts" We Can Establish

| Element | We Decide |
|---------|-----------|
| Vision | What inspired them |
| Problem | What pain they saw |
| Customer | Who they targeted first (beachhead) |
| Bets | What they were uncertain about |
| Timing | Why 2011 was the moment |
| Goals | What behavior changes they targeted |
| Now/Next/Later | What they prioritized when |

We're writing the founding story we wish existed for teaching purposes.

---

### Next Steps

When we're ready to build out examples, we'll need to establish "Fictional Trello Canon" - the agreed facts about our example company that all artifacts reference.

Should I draft that canon document now, or park it for later when we're actively building examples?



## Prompt:
11/26/2025, 12:09:08 PM

what do you think



## Response:
11/26/2025, 12:09:24 PM

**Do it now, lightweight.**

Reasoning:

1. **Stress-tests the Canvas** - Filling out fictional Trello will immediately reveal if our schema has gaps or awkward sections

2. **Story mapper already has Kanban examples** - Those prompts reference Trello-like boards. Having canon means we can align them rather than having inconsistent fictional "facts"

3. **Fresh context** - We just designed the Canvas structure. Best time to test it is while it's all in working memory

4. **Doesn't need to be complete** - Just enough to be a seed. We fill in Roadmap canon when we design that schema.

---

### Proposed Scope

Draft **Fictional Trello Canon - Canvas elements only**:
- Vision
- Pitch (Moore template)
- Customer
- Problem
- Solution
- Unique Value
- Timing
- Market
- Revenue
- Truths & Bets

Skip Roadmap canon (Strategy, Goals, Now/Next/Later) until we've designed that schema.

Want me to draft it?



## Prompt:
11/26/2025, 12:09:52 PM

go for it



## Response:
11/26/2025, 12:11:27 PM

[View Fictional Trello Canon](computer:///home/claude/fictional-trello-canon.yaml)

---

### What I Learned Filling It Out

**Schema validated well.** Every section had something natural to say. No section felt forced or redundant.

**A few observations:**

1. **Vision vs Pitch distinction works** - Vision is the poetry ("work should be visible, collaboration should feel like flow"), Pitch is the clinical Moore template. Different audiences, different purposes.

2. **"Big Enough" is doing important work** - Forces articulation of why this isn't a vitamin. "Basecamp has customers proving WTP; we're expanding the market to everyone who gave up on PM software."

3. **Truths & Bets separation is powerful** - Truths feel like solid ground (Fog Creek has resources, Joel has audience). Bets feel appropriately risky (simplicity beats features, word of mouth will work).

4. **Timing section earns its keep** - "The browser just became powerful enough" is a real insight. Without this section, it's just "we had an idea."

5. **Solution.approach might need refinement** - It's doing okay here, but feels slightly redundant with the Pitch. Worth watching as we test.

---

What do you think? Does this feel like the right fictional Trello to build all our examples from?



## Prompt:
11/26/2025, 12:12:28 PM

what is WTP?



## Response:
11/26/2025, 12:12:35 PM

**Willingness to Pay**

Jargon from customer development / pricing strategy. The question of whether customers will actually pay money to solve this problem (vs. just saying they want it solved).

I should have written it out. Good catch - the canon document should be readable without assumed jargon.



## Prompt:
11/26/2025, 12:16:41 PM

yeah this looks really great



## Response:
11/26/2025, 12:16:57 PM

Great. We've got:

- ✅ Compass Canvas schema (v3)
- ✅ Knowledge Layer draft (needs story-mapper-level rigor later)
- ✅ Fictional Trello Canon (Canvas elements)

Still open:
- Compass Roadmap schema (your template, needs to be formalized)
- Canvas ↔ Roadmap overlap reconciliation (Vision, Strategy - sort as we go)
- Swap into existing `/products/compass/` implementation

What's next?



## Prompt:
11/26/2025, 12:20:36 PM

lets work on the roadmap portion of the compass... which I am kinda coming around to the wording of destination (canvas) and course (roadmap)

I'd like to develop the course out more and then try the trello example



## Response:
11/26/2025, 12:20:58 PM

Love the terminology shift. **Destination** and **Course**. Clean.

---

### Starting Point: Your Template Elements

From the HTML template, the Course contains:

| Section | Purpose |
|---------|---------|
| Vision (5+ years) | → Lives on Destination, Course references |
| Strategy | Focus + Approach |
| Goals (1-2 years) | Timeboxed behavior changes, measurable |
| Goal Progress Tracking | Started → Last → Current → Target → Status |
| Now / Next / Later | Time horizons with language progression |
| Capacity Allocation | 60% strategic / 20% small / 20% operational |
| Work by Goal | Each row = all work advancing one outcome |
| Mandated Work | Required things not tied to goals |

---

### Questions to Develop the Schema

**1. Strategy + Approach**

Your template has:
- **Focus**: "How will you provide better end-to-end service?"
- **Approach**: "3-5 specific actions that support your strategy"

Is Strategy a single statement? A paragraph? Does it have sub-structure?

**2. Goals**

Template says "focus on specific user behavior changes." 

What's the anatomy of a Goal?
- Name/label
- Behavior change description
- Metric
- Baseline → Target
- Timeline?

How many goals? Your template shows 3.

**3. Now / Next / Later**

The language progression is brilliant:
- **Now**: Concrete deliverables (planned for release)
- **Next**: Solutions being designed (solutioning)
- **Later**: Problems to explore

What lives in each cell? Are these just text items, or structured (linked to goals, tagged, etc.)?

**4. Capacity**

60/20/20 in your template. Is this fixed doctrine or configurable per product/team?

---

Where do you want to start? Strategy? Goals? The time horizon structure?



## Prompt:
11/26/2025, 12:26:41 PM

ok let me give you some background

the vision was inspired by how jeff patton talks about vision

the strategy is inspired by good strategy/bad strategy and playing to win... I worked with claude 5 months ago to distill the concepts from those books into this strategy section

the lanugage in that roadmap html i shared is the theory behind how you are supposed to fill the roadmap out

The outcomes are influenced by Escaping the build trap and OKRs moreso jeff gothelf

Now/next later is influenced by jenna bastow but I applied more rigor to it

the capacity element I don't think that matters as much in a 2 person 1 ai company so i wouldn't worry about that



## Response:
11/26/2025, 12:26:59 PM

This is exactly what we need. Source methodology mapping:

| Element | Source(s) |
|---------|-----------|
| Vision | Jeff Patton |
| Strategy | Good Strategy/Bad Strategy (Rumelt) + Playing to Win (Lafley/Martin) |
| Goals/Outcomes | Escaping the Build Trap (Perri) + OKRs + Jeff Gothelf |
| Now/Next/Later | Jenna Bastow + Ian's rigor |
| Capacity | Skip for now |

---

### Two Things I Want to Pull

**1. The Strategy distillation from 5 months ago**

You said you worked with Claude to distill Rumelt + Lafley/Martin. Do you still have that? Would save us from re-deriving and would capture your thinking from that session.

**2. Your added rigor on Now/Next/Later**

Jenna Bastow's version is fairly loose ("don't put dates on things, use horizons"). You said you applied more rigor. What did you add?

---

These two are where "Ian's spin" lives. The other sources I can work from general knowledge, but your adaptations are the unique bits.



## Prompt:
11/26/2025, 12:34:24 PM

it was in one of these conversations /Users/ianswanson/ai-prompts/jackson/10-past-chats


