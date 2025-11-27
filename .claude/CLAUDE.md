# HLCS Framework Development - Claude Code Context

## What This Is

R&D workshop for developing HLCS (Human-LLM Collaborative Systems) navigation instruments. This is **knowledge work** (conversations → specifications), not product development.

**Output:** Knowledge layers, schemas, protocols that will feed future product build.

## Core Framework Reference

**CRITICAL - CHECK MEMORY FIRST:**

These files are **automatically loaded** in `.claude/memory/` and contain the foundational frameworks:

- **human-llm-collaborative-system-pattern.md** - The 5-tier HLCS model (Schema, Knowledge, Data, Interaction, Presentation)
- **navigation-instruments-framework.md** - The sailing metaphor and 7-phase instrument development process

**Before starting any work:** Verify you have loaded and understood these frameworks. They define the foundation for all HLCS instrument development.

**Also available at company level:**
- `claudian/.claude/memory/company-core.md` - Claudian operating principles and standards

**Source of truth:** `/docs/patterns/` at company level (memory files are copies for convenient context loading)

---

## Session Protocol

### Start of Session
1. **Verify memory loaded** - Confirm you have the HLCS and Navigation frameworks from `.claude/memory/`
2. **Read** `SESSION.md` - current focus and context
3. **Check** `CHANGELOG.md` - recent progress
4. **Review** relevant instrument folder for context

### During Session
- Synthesize methodology into knowledge layers
- Update working/ docs as you explore
- Create/update specifications in instrument folders
- Use `/transcribe` to save session to `/transcripts/` (company-level)

### End of Session
- **Update** `@../SESSION.md` with progress and next steps
- **Log** in `@../CHANGELOG.md` what was accomplished
- **Note** any open questions or blockers

---

## Working Here

### This is NOT a Product Build

- No code to write yet
- Focus: markdown docs, JSON schemas, examples
- Output becomes input for future product

### Instrument Development Process

Each instrument follows 7 phases:

1. **Foundation** - Identify source methodologies, study deeply
2. **Ian's Spin** - Document unique adaptations/perspective
3. **AI-Native Adaptation** - HLCS considerations
4. **Schema Design** - Define artifact structure
5. **Protocol Design** - Collaboration workflow
6. **Integration** - Connections between instruments
7. **Implementation** - (Future) Build the actual tool

See `@../navigation-instruments-framework.md` for details.

---

## File Organization

### Where Things Go

```
reference/
  methodologies/     → Source material (Patton, Rumelt, Moore, etc.)
  frameworks/        → 18F guide, OKRs, Lean Canvas
  hlcs-theory/       → 5-tier model, core concepts

{instrument}/        → compass/, telescope/, map/, blueprint/, course/
  knowledge-layer.md → Methodology synthesis (ontology, evaluation, procedures)
  schema.json        → Artifact structure
  examples/          → Sample artifacts
  README.md          → Instrument overview

working/             → Active drafts, scratchpad, Claude Desktop imports

/transcripts/        → Structured session transcripts (company-level, use /transcribe)
```

### Naming Conventions

- **Transcripts:** Use `/transcribe` command (auto-formats to `YYYY-MM-DD-topic-description.md`)
- **Reference docs:** `author-name-topic.md` (e.g., `jeff-patton-story-mapping.md`)
- **Working docs:** Descriptive names, anything goes
- **Desktop imports:** Save to `working/` with clear naming

---

## Methodology Synthesis Pattern

When working on an instrument:

1. **Study sources** - Read reference materials deeply
2. **Identify Ian's spin** - What's unique about his adaptation?
3. **Synthesize** - Create knowledge layer document:
   - **Ontological** (what it is)
   - **Evaluative** (what makes it good)
   - **Procedural** (how to create it)
4. **Define schema** - JSON/YAML artifact structure
5. **Create examples** - Validate schema works
6. **Document integration** - How it connects to other instruments

---

## Key Principles

### Outputs Become Inputs

Everything here feeds the future product build. Specifications must be:
- Clear enough to implement
- Structured for machine consumption
- Human-readable for collaboration

### Ian's Spin is Distinct

Keep layers explicit:
1. Source methodology (as-is)
2. Ian's adaptation (unique perspective)
3. AI-native considerations (HLCS implementation)

### Phase-Appropriate Rigor

We're in discovery for the framework itself. Don't over-engineer. But DO maintain clear documentation.

### Reference Folder as RAG

The reference/ folder is building a curated knowledge base. Eventually becomes:
- Training material for embeddings
- Source citations
- Provenance documentation

---

## The Instruments

**Flow:** Compass → Telescope → Map → Blueprint → Ship

| Instrument | Question | Output |
|------------|----------|--------|
| **Compass** | Where are we going? | Vision, strategy, direction |
| **Telescope** | What's out there? | Opportunity trees, problem space |
| **Map** | What are we building? | User story map |
| **Blueprint** | How do we build it? | Architecture, schemas |
| **Course** | How do we get there? | Roadmap, strategic execution |

**Ship** is the actual product/codebase.

**Course** may integrate across instruments rather than being strictly sequential.

---

## Current Focus

See `@../SESSION.md` for current instrument and phase.

---

## References

- **Navigation framework:** `@../navigation-instruments-framework.md`
- **Company context:** `@../../../CLAUDE.md`
- **Current session:** `@../SESSION.md`
- **History:** `@../CHANGELOG.md`
