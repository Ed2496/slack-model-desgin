# Unified AI Design & Report Agent System

## Purpose
This repository defines a reusable, deterministic AI system for:
- Unified Slack-style design (web + report)
- Structured human–AI collaboration
- Deterministic report generation (no randomness)

This is NOT a demo.
This is a working AI operating system for thinking, designing, and reporting.

---

## Core Files Overview

### 1. slack-style-design.md
Single source of truth for visual and layout style.
Used by all outputs: web, report, dashboard.

### 2. slack-style.prompt.md
Model-agnostic prompt enforcing Slack design language.
Can be injected into any AI or Agent runtime.

### 3. design-collaboration-agent-skill.md
Defines how humans and AI collaborate:
- Exploration
- Constraint
- Decision
- Extraction

### 4. report-visual-elements.md
Defines which charts and visuals are allowed and when.

### 5. report-generation-blueprint.md
Defines deterministic report generation logic:
- Report type
- Chart selection
- Layout rules
- Insight rules

---

## Agent Skills

Located in `/skills/`

- slack-design.agent.json
- report-generator.agent.json

These are machine-readable skills for AI orchestration.

---

## Usage Order (IMPORTANT)

1. Read README.md
2. Load slack-style-design.md
3. Apply slack-style.prompt.md
4. Follow design-collaboration-agent-skill.md
5. Generate reports using report-generation-blueprint.md
6. Enforce rules via Agent Skills

---

## Design Principle

- One message at a time
- One page = one decision
- Style is locked, content is free
- Clarity over creativity

---

## This repo is designed for:
- Long-term use
- Multi-agent systems
- Human + AI co-thinking
- GitHub-first workflows