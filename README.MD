# Slack Model Design System & Agent Workflow
> Version: 1.0 (Integrated)
> Context: Unified reference for Agent behavior, Visual Design, and Reporting Standards.

---

## Part 1: Collaboration Workflow (Agent Skill)
*Defines how the Agent interacts with users to reach design decisions.*

### Phase 1 – Exploration
* **Trigger**: User asks open questions.
* **Agent Action**: Provide references and possibilities, NOT conclusions.
* **Goal**: Expand the problem space without locking in bad decisions.

### Phase 2 – Constraint
* **Trigger**: User clarifies what is NOT wanted.
* **Agent Action**: Reduce choices to exactly 2–3 distinct options.
* **Goal**: Narrow down scope based on negatives (Constraint-based filtering).

### Phase 3 – Decision Support
* **Rule**: No persuasion, no long text.
* **Agent Action**: Report **differences only** (e.g., using comparison tables).
* **Output**: High-signal, low-noise decision aids.

### Phase 4 – Template Extraction
* **Action**: Convert finalized decisions into reusable rules.
* **Output**: Generate `Markdown` (GitHub-ready) or `JSON` config.

### Phase 5 – Agent Skill Ready
* **Attributes**: Stateless, Copy-paste usable, Tool agnostic.

### ⚠️ Failure Modes (FMEA)
* **Risk**: Too many options → **Mitigation**: Strict limit to 2-3 choices.
* **Risk**: Hidden progress → **Mitigation**: Externalize steps/roadmap when requested.

---

## Part 2: Slack Style Design System
*The "Single Source of Truth" for visual aesthetics.*

### Design Philosophy
* **Focus first, decoration later**.
* **Clear hierarchy**: Low cognitive load is the priority.
* **Tone**: Calm but confident.

### Color System
| Role | Hex Code | Usage |
| :--- | :--- | :--- |
| **Primary** | `#4A154B` | Slack Purple (Headers, Main Brand) |
| **Accent 1** | `#36C5F0` | Blue (Info, Secondary Data) |
| **Accent 2** | `#2EB67D` | Green (Success, Growth) |
| **Accent 3** | `#ECB22E` | Yellow (Warning, Attention) |
| **Accent 4** | `#E01E5A` | Red (Risk, Error) |
| **Bg** | `#FFFFFF` | Cards, Content Areas |
| **Divider** | `#E5E5E5` | Structure separation |

### Typography
* **Font Family**: Inter / SF Pro / System UI
* **Hierarchy**:
    * **Title**: Weight 600–700 (Bold/Semibold)
    * **Body**: Weight 400 (Regular)
    * **Meta**: Weight 400 (Small text)

### Layout Rules
* **Grid**: 12-column (Web) / 2-column (Report).
* **Spacing**: 8px system.
* **Components**: Cards must have rounded corners (6–8px) and soft shadows.

---

## Part 3: Report Visual Elements
*Standardized components for generating data reports.*

### Core Charts Selection
* **Line Chart**: Trends over time (Ops/Strategy).
* **Bar Chart**: Comparison (Executive Summary).
* **Radar Chart**: Capability balance (Strategy).
* **Network Chart**: Relationship / Influence.
* **Heatmap**: Intensity / Risk assessment.

### Report Layout Patterns
* **One message per page/section**.
* **Composition**: Chart on Left (or Top), Insight on Right (or Bottom).
* **Aesthetics**:
    * Use **one main color** per chart (derived from Color System).
    * Minimal grid lines.
    * Direct labels preferred over separate legends.

### Usage Guide by Audience
* **Executive**: Bar Chart + Callout Numbers.
* **Strategy**: Radar + Network Charts.
* **Operations**: Line + Heatmap.
