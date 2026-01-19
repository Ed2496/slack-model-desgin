# Report Generation Blueprint
# Purpose: Deterministic, reusable, AI-safe report creation

---

## 1. Report Types Definition

### Executive Report
Audience: Executives / Decision Makers  
Goal: Fast understanding, clear signal

Use:
- Bar chart (comparison)
- Callout numbers (key metrics)

Avoid:
- Network graphs
- Dense tables

---

### Strategy Report
Audience: Planning / Architecture / PM  
Goal: Relationship, balance, direction

Use:
- Radar chart (capability balance)
- Network graph (dependency / influence)

Avoid:
- Too many time-series
- Operational details

---

### Operations Report
Audience: Ops / QA / Monitoring  
Goal: Trend, anomaly, stability

Use:
- Line chart (trend)
- Heatmap (risk / intensity)

Avoid:
- Conceptual diagrams
- Abstract language

---

## 2. Chart Selection Logic (AI Decision Rule)

IF goal == comparison
→ use bar chart

IF goal == balance OR capability
→ use radar chart

IF goal == relationship OR influence
→ use network graph

IF goal == trend over time
→ use line chart

IF goal == risk density OR anomaly
→ use heatmap

---

## 3. Page Layout Pattern (Strict)

Each page MUST contain:
1. Page title (what question is answered)
2. One main visual
3. One-sentence insight (mandatory)

Layout:
- Visual: left or top
- Insight text: right or below
- No more than ONE core message per page

---

## 4. Insight Sentence Rules

- Maximum 25 words
- Must answer: "So what?"
- No adjectives without evidence
- No future promise language

Bad:
"This shows strong improvement and great potential"

Good:
"Metric A increased 18% QoQ, driven mainly by Segment B"

---

## 5. Visual Hygiene Rules

- One primary color per chart
- Background always white or light gray
- Grid lines minimal or removed
- Labels preferred over legends
- No decorative icons in charts

---

## 6. AI Generation Sequence (Must Follow)

Step 1: Identify report type  
Step 2: Determine report goal  
Step 3: Select chart type (Section 2)  
Step 4: Generate visual structure  
Step 5: Generate insight sentence  
Step 6: Validate against rules  

IF any rule fails → regenerate Step 4–5

---

## 7. Failure Modes (AI Must Detect)

- Multiple messages on one page
- Visual without insight
- Insight without evidence
- Style inconsistent with Slack design system

If detected → STOP and correct

---

## End of Blueprint