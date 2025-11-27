# Course - Knowledge Layer

**Navigation Instrument:** Course (Roadmap)
**Question:** How do we get there?
**Output:** Strategic roadmap connecting vision to execution

**Status:** Draft v0.1
**Last Updated:** November 26, 2025

---

## I. ONTOLOGICAL LAYER (What It Is)

### Core Definition

**Course** is the roadmap instrument that translates strategic direction into executable plans. It bridges the gap between **where you're going** (Compass/Destination) and **what you're building** (Map/Blueprint/Ship) by defining the time-horizoned execution path.

### Conceptual Model

Course operates at **two distinct scales** that must remain separate:

**Strategic Layer (Stable, 1-5 years):**
- Vision (5+ years)
- Strategy (2-5 years)
- Goals (1-2 years)

**Execution Layer (Dynamic, Quarterly):**
- Now (This quarter)
- Next (Next quarter)
- Later (Future quarters)

The **critical insight**: Strategy is the compass that guides decisions, not a list of big initiatives. The execution layer adapts based on learning while the strategic layer remains stable.

### Source Methodologies

| Element | Source(s) | Ian's Adaptation |
|---------|-----------|------------------|
| Vision | Jeff Patton | "What SHOULD be" vs. "what CAN be" - audacious human transformation |
| Strategy | Rumelt (Good Strategy/Bad Strategy) + Lafley/Martin (Playing to Win) | "Strategy as compass" - decision framework, not destination list |
| Goals | Melissa Perri (Escaping the Build Trap) + OKRs + Jeff Gothelf | User behavior change evidence, not output metrics |
| Now/Next/Later | Jenna Bastok (ProdPad) | Language progression + artifact type differentiation (Deliverables/Solutions/Investigations) |
| Roadmap Theory | 18F Product Guide | Integration of strategic and tactical layers |

### Relationship to Other Instruments

**Compass is compound:**

```
COMPASS
  ├── DESTINATION (Canvas) - Business case/thesis
  └── COURSE (Roadmap) - Execution plan
```

**Navigation flow:**

```
COMPASS (Destination + Course) → TELESCOPE → MAP → BLUEPRINT → SHIP
```

**Course relationship to Destination:**
- **Destination** (Canvas) defines: Market position, customer, problem/solution, unique value, business model, truths & bets
- **Course** (Roadmap) defines: Vision, strategy, goals, time-horizoned execution (Now/Next/Later)
- **Shared element:** Vision lives on Destination (foundational), Course references it for context
- **Boundary:** Destination = "where we're positioned", Course = "how we get there"

**Course relationship to downstream instruments:**
- **To Telescope:** Course's LATER column defines problem spaces to investigate
- **To Map:** Course's NEXT→NOW transition identifies solutions ready for story mapping
- **To Blueprint:** Goals define outcomes to architect for
- **To Ship:** NOW column defines what's being built this quarter

---

## II. EVALUATIVE LAYER (What Makes It Good)

### Quality Criteria

#### Vision Quality

**Audacious enough** to focus on what should be possible, not what current constraints allow

**Inspirational enough** to energize people beyond current frustrations

**Human enough** to connect with real community impact and lived experience

**Valuable enough** to maintain focus through changing priorities and leadership

**Specific enough** to guide strategic decisions without prescribing solutions

**Test:** Does it describe human transformation, not technological capability?

#### Strategy Quality

**Passes the Compass Test:**
- Will this guide decisions even when technology changes? ✓
- Will this help us choose between competing initiatives? ✓
- Does this explain WHY we're heading this direction, not WHAT we'll build? ✓
- Could this framework still apply in 3 years with different initiatives? ✓

**Contains all four components:**
1. Problem Diagnosis (patterns and root causes, not symptoms)
2. Guiding Principles (decision criteria that hold for 2-5 years)
3. Focus Areas (where to look, not what to build)
4. Trade-offs (explicit choices about what NOT to do)

**Avoids failure modes:**
- Strategy becomes initiative list
- Too concrete for strategic level
- Missing trade-offs (tries to do everything)
- Internal process focus vs. user value focus

#### Goals Quality

**User behavior change focus** - not outputs or internal metrics

**Measurable** with baseline → target tracking (OKR-style)

**Time-bound** (1-2 year horizon allows for real behavior change)

**Connected to strategy** - provides evidence the strategic compass is working

**Specific enough** to be measurable, but focused on outcomes not outputs

**Test:** Can you measure this user behavior change? Does achieving it prove your strategy is working?

#### Now/Next/Later Quality

**Language progression maintained:**
- NOW: Concrete delivery language (ready to ship)
- NEXT: User value language (solutions being designed)
- LATER: Problem space language (investigations)

**Artifact type clarity:**
- NOW contains Deliverables only
- NEXT contains Solutions only
- LATER contains Investigations only

**Goal connection explicit** - each row ties to a specific goal

**Force specificity** - if you can't name it specifically, you don't understand it well enough to roadmap it

**Capacity allocation realistic** - acknowledges strategic work, small requests, operational work

---

## III. PROCEDURAL LAYER (How to Create It)

### The Scale Problem

The biggest challenge in roadmapping is **scale confusion**. The same work can be a user story, epic, or initiative depending on vantage point.

**Solution:** Maintain clear scale separation through distinct sections and language.

### Creating the Strategic Layer

#### 1. Vision (5+ years)

**Process:**
1. Focus on human transformation, not technology
2. Describe what SHOULD be possible (ignore current constraints)
3. Paint specific user scenarios, not abstract concepts
4. Keep it pure and aspirational

**Language to use:**
- How people's lives will be different
- What becomes possible that isn't now
- Specific human scenarios (not "residents" but "Spanish-speaking immigrants", "seniors with disabilities")

**Language to avoid:**
- Technology features
- System capabilities
- Process improvements
- Abstract jargon ("Digital is a Public Service")

**Example (good):**
> Multnomah County residents seamlessly access any government service they need through intuitive digital experiences that work for everyone - from Spanish-speaking immigrants applying for benefits on their phones to seniors with disabilities navigating health services - with in-person visits only when they truly add value to the human experience.

**Example (bad):**
> Multnomah County envisions a future where Digital is a Public Service and it provides equitable access and opportunity.

#### 2. Strategy (2-5 years)

**Process:**
1. Start with diagnosis (what's systematically broken?)
2. Define guiding principles (how will we make decisions?)
3. Identify focus areas (where will we look for opportunities?)
4. State trade-offs explicitly (what won't we do?)

**The three questions (Rumelt):**
1. What's wrong with how we currently serve people? (diagnosis)
2. What approach will create better outcomes? (guiding policy)
3. How will these specific actions work together? (coherent action)

**Problem Diagnosis:**
- Focus on patterns and root causes, not specific pain points
- Identify assumptions that don't match reality
- Distinguish artificial constraints (process) from real constraints (legal/resource)
- Surface the fundamental gap between expectations and reality

**Guiding Principles:**
- Decision-making criteria that hold for 2-5 years
- "When choosing between X and Y, we'll prioritize..."
- "We'll know we're heading in the right direction when..."
- Stay at compass level, not initiative level

**Focus Areas:**
- Broad domains for investigation, not specific solutions
- Which user journeys or service areas get attention
- What types of problems to investigate
- Where to concentrate discovery efforts

**Trade-offs:**
- Which problems won't be solved in this period
- What user groups or use cases to defer
- Which internal improvements to postpone for user value focus

**Compass-level language (use this):**
- "Eliminate steps that exist for government convenience rather than user needs"
- "Treat user identity as a service asset, not a barrier"
- "Design for how people actually access services (mobile, stressed, multitasking)"

**Initiative-level language (avoid in strategy):**
- "Redesign the permit application process"
- "Implement single sign-on across all services"
- "Create a mobile-first website"

#### 3. Goals (1-2 years)

**Process:**
1. Identify what user behavior changes would prove strategy is working
2. Define 2-4 goals (more dilutes focus)
3. For each goal, specify: behavior change, metric, baseline, target
4. Connect each goal explicitly to strategic focus areas

**Formula:**
[Measurable change] in [user behavior] indicating [strategic success]

**Examples (good):**
- "Increase in non-English language page usage on Multco.us, indicating residents can successfully access services in their preferred language"
- "Decrease in WCAG compliance violations across county web content, indicating improved accessibility for residents with disabilities"

**Examples (bad):**
- "Launch new website" (output, not outcome)
- "Reduce call center volume by 20%" (internal metric, not user behavior)
- "Process 500 more applications per month" (efficiency, not user experience)

**Early stage consideration:**
If you don't have baselines yet, state directional changes (increase/decrease) rather than specific numbers.

**Accountability:**
Goals are leadership-owned targets that product manager figures out how to achieve.

### Creating the Execution Layer

#### 4. Now/Next/Later Grid

**Structure:**
- One row per goal
- Three time horizon columns
- Capacity allocation rows (Strategic/Small Requests/Operational)

**Process for each goal:**

**NOW Column (Deliverables):**
1. List concrete outputs being released this quarter
2. Use concrete delivery language
3. Be specific about what ships to users
4. Only include items with shipping criteria defined

**NEXT Column (Solutions):**
1. List user value being created through design work
2. Use solution language (problems being solved)
3. Focus on clear approaches to validated problems
4. Include items in active solutioning phase

**LATER Column (Investigations):**
1. List problem spaces to explore
2. Use exploratory language
3. Focus on research questions, not solutions
4. Include areas needing more discovery before commitment

**Capacity Allocation:**

Typical breakdown (adjustable per context):
- 60% Strategic Initiatives (tied to goals)
- 20% Small Requests (quick fixes, tactical work)
- 20% Operational Work (maintenance, security, routine)

**Mandated Work:**
Include required/compliance work explicitly, typically in LATER column for visibility even if not tied to goals.

**Language Progression Discipline:**

| Horizon | Language Type | Example |
|---------|--------------|---------|
| NOW | Concrete delivery | "Launch permit renewal self-service portal" |
| NEXT | User value | "Enable small business owners to renew licenses without office visits" |
| LATER | Problem exploration | "Investigate why 40% of permit applicants call for help instead of completing online" |

### Integration Workflow

**Quarterly rhythm:**
1. Review strategic layer (stable, minor adjustments only)
2. Update goal progress tracking (baseline/current/target)
3. Move items across Now/Next/Later as they mature
4. Mine "Later" column for next quarter's "Next" work
5. Update capacity allocation based on actual team reality

**Annual rhythm:**
1. Refresh goals (are they still the right behavior changes?)
2. Review strategy (is the compass still pointing true?)
3. Potentially update vision (rarely - only if fundamental shift)

---

## IV. AI-NATIVE ADAPTATION

**Status:** Not yet defined - requires HLCS framework application

**Questions to explore:**
- How does LLM collaboration enhance strategic thinking?
- What parts benefit from AI pattern recognition vs. human judgment?
- How to structure artifacts for both human and AI consumption?
- What validation loops ensure AI doesn't reinforce existing biases?

**Deferred to Phase 3** of Course instrument development.

---

## V. SCHEMA CONSIDERATIONS

**See:** `course/schema.json` (to be created)

**Key structures to define:**

1. **Vision artifact** (narrative + metadata)
2. **Strategy artifact** (diagnosis + principles + focus + tradeoffs)
3. **Goals artifact** (array of goal objects with metrics)
4. **Roadmap grid** (goals × horizons matrix)
5. **Roadmap items** (deliverables/solutions/investigations with goal linkage)

**Schema design deferred to Phase 4** after knowledge layer validation.

---

## VI. PROTOCOL CONSIDERATIONS

**See:** Course protocol (to be created in Phase 5)

**Key collaboration patterns to define:**

1. **Vision workshops** (leadership + team co-creation)
2. **Strategy diagnosis** (pattern identification from research)
3. **Goal definition** (metric selection and baseline establishment)
4. **Quarterly planning** (Now/Next/Later updates)
5. **Progress review** (goal tracking and course correction)

**Protocol design deferred to Phase 5** after schema validation.

---

## VII. INTEGRATION WITH OTHER INSTRUMENTS

**Inputs (from Compass/Destination):**
- Mission statement
- Market positioning
- Core values/principles
- Strategic bets

**Outputs (to Telescope):**
- Problem spaces to investigate (from LATER column)
- User behavior changes to validate (from Goals)
- Focus areas for opportunity discovery

**Outputs (to Map):**
- Solutions ready for story mapping (from NEXT → NOW transition)
- User outcomes to design for (from Goals)

**Continuous feedback:**
- Discovery learnings (Telescope) inform strategy adjustments
- Story mapping (Map) clarifies solution scope for roadmap
- Shipping outcomes (Ship) validate/invalidate goal progress

---

## VIII. OPEN QUESTIONS

### ✅ RESOLVED: Course Positioning

**Answer:** Course is **part of Compass**, not a separate instrument.

```
COMPASS
  ├── DESTINATION (Canvas) - Business case/thesis
  └── COURSE (Roadmap) - Execution plan
```

The Compass instrument is compound - it has two components that work together to provide strategic direction.

### ✅ RESOLVED: Vision Home

**Answer:** Vision lives on **Destination** (Canvas) as the foundational "why we exist."

Course **references** Vision for context (displays it at top of roadmap) but doesn't own it. Single source of truth = Destination.

**Rationale:** Vision is part of the business thesis (what position we'll hold), not the execution plan.

### Capacity Allocation

Current template uses 60/20/20 split. Is this:
- Doctrine (recommended default)?
- Example (teams should determine their own)?
- Context-dependent (varies by org size, maturity, constraints)?

**Current stance:** Example only, not prescriptive. 2-person + AI company has different needs than 50-person government team.

---

## IX. REFERENCES

**Methodology sources:**
- `reference/methodologies/strategy-as-compass-rumelt-lafley-martin.md`
- `reference/methodologies/now-next-later-jenna-bastok-ian-rigor.md`

**Source conversations:**
- Jackson-60 - Strategic Product Roadmap Framework (~June 2025)

**Reference artifacts:**
- `working/roadmap_template.html` - Implementation example

**Framework context:**
- `.claude/memory/navigation-instruments-framework.md` - 7-phase development process
- `.claude/memory/human-llm-collaborative-system-pattern.md` - HLCS 5-tier model

---

## X. NEXT STEPS

**Immediate (Phase 1 - Foundation):**
- [x] Document source methodologies
- [x] Create initial knowledge layer
- [ ] Validate knowledge layer with Ian

**Phase 2 - Ian's Spin:**
- [ ] Document unique adaptations vs. source methodologies
- [ ] Clarify vision vs. strategy boundary
- [ ] Resolve Course positioning question

**Phase 3 - AI-Native Adaptation:**
- [ ] Apply HLCS framework to Course
- [ ] Define human-AI collaboration patterns
- [ ] Identify AI augmentation opportunities

**Phase 4 - Schema Design:**
- [ ] Extract schema from roadmap template
- [ ] Define artifact structures (JSON/YAML)
- [ ] Create validation criteria

**Phase 5 - Protocol Design:**
- [ ] Define collaboration workflows
- [ ] Create facilitation guides
- [ ] Design review/update cadences

**Phase 6 - Integration:**
- [ ] Map connections to other instruments
- [ ] Define handoff protocols
- [ ] Create integration examples

**Phase 7 - Implementation:**
- [ ] (Future) Build Course product visualization
- [ ] (Future) Implement collaboration features
- [ ] (Future) Create AI assistance layer

---

**End of Knowledge Layer v0.1**
