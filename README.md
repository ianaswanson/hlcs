# HLCS Sailing Framework

The R&D workshop for developing **HLCS (Human-LLM Collaborative Systems)** using a sailing/navigation metaphor for product development.

## What This Is

This is **knowledge work in progress** - conversations and methodology synthesis that will eventually feed the build of interactive HLCS tools. We're developing the framework through conversation-driven research, synthesis, and specification.

**Current phase:** Specification (methodology → schemas → protocols)
**Future phase:** Product build (visualization + interaction layer)

## What Lives Here

- **Instrument specifications** - Navigation instruments (Compass, Telescope, Map, Blueprint, Course)
- **Reference materials** - Source methodologies, frameworks, theory (shared RAG knowledge base)
- **Conversation logs** - Exported discussions that built this framework
- **Working documents** - Active synthesis and exploration

## Quick Start

1. **See what's happening now:** Read `SESSION.md`
2. **Understand the framework:** Read `navigation-instruments-framework.md`
3. **Explore an instrument:** Browse `compass/`, `telescope/`, `map/`, etc.
4. **Check history:** Read `CHANGELOG.md`

## The Sailing Metaphor

Product development is like sailing - you need different instruments for different purposes:

- **Compass** - Vision, strategy, direction (where are we going?)
- **Telescope** - Discovery, opportunity exploration (what's out there?)
- **Map** - User story mapping, scoped work (what exactly are we building?)
- **Blueprint** - Architecture, technical design (how do we build it?)
- **Course** - Roadmap, strategic execution (how do we get there?)
- **Ship** - The product itself (what we build and "ship")

Each instrument is an **HLCS implementation** - a structured human-AI collaboration that produces artifacts downstream processes can consume.

## Structure

```
utilities/hlcs/
├── .claude/              # Claude Code working instructions
├── reference/            # Shared source materials (RAG knowledge base)
│   ├── methodologies/    # Jeff Patton, Rumelt, Moore, etc.
│   ├── frameworks/       # 18F guide, OKRs, Lean Canvas, etc.
│   └── hlcs-theory/      # 5-tier model, outputs-as-inputs, etc.
├── compass/              # Vision & strategy instrument
├── telescope/            # Discovery instrument
├── map/                  # Story mapping instrument
├── blueprint/            # Architecture instrument
├── course/               # Roadmap instrument
└── working/              # Active drafts, Claude Desktop imports

/transcripts/             # Structured session transcripts (company-level)
```

## For Claude Code

When working in this directory, read `.claude/CLAUDE.md` for working instructions and session protocols.

## Status

**Current state:** See `SESSION.md`
**History:** See `CHANGELOG.md`

---

**Last Updated:** November 26, 2025
