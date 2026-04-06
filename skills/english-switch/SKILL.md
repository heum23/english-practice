---
name: english-switch
description: Use when the user invokes /english-switch. Presents on/off toggle for English practice mode via AskUserQuestion selection UI.
user-invocable: true
---

# English Switch

When invoked, use the `AskUserQuestion` tool to toggle English mode:

## Ask On/Off

Use AskUserQuestion with these options:

- **ON** — "영어 연습 모드 켜기 (현재 설정된 레벨로 활성화)"
- **OFF** — "영어 연습 모드 끄기 (평소 대화로 복귀)"

Header: "Switch"
Question: "Toggle English practice mode?"

## Behavior

### If ON selected:
- If a level was previously set via `/english-mode`, use that level
- If no level was set, default to **casual**
- Confirm: "영어 연습 모드가 활성화되었습니다. (레벨: [level])"
- Then follow the level rules from the `english-mode` skill

### If OFF selected:
- Confirm: "영어 연습 모드를 종료합니다. 이제부터 평소처럼 진행하겠습니다."
- Return to user's default language
- No more English corrections
