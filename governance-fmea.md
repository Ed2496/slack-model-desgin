# AI System Governance & FMEA

## Failure Mode 1: Style Drift
Cause:
- Prompt 被改
- 多個 Agent 混用風格

Impact:
- 輸出不一致
- 報告失去信任

Mitigation:
- slack-style-design.md 為唯一來源
- style_locked = true

---

## Failure Mode 2: Over-Creativity
Cause:
- AI 自由發揮
- 未鎖定圖表規則

Impact:
- 花俏但沒結論

Mitigation:
- Blueprint chart selection logic
- Insight sentence mandatory

---

## Failure Mode 3: Human Overload
Cause:
- AI 一次給太多選項

Impact:
- 使用者疲勞
- 決策停滯

Mitigation:
- design-collaboration-agent-skill.md
- Max 3 options rule

---

## Versioning Rule
- All rule changes must:
  - Update md
  - Update agent json
  - Update README