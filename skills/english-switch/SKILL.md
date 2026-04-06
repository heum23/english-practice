---
name: english-switch
description: Use when the user invokes /english-switch. Toggle English practice mode on/off via AskUserQuestion.
user-invocable: true
---

Use `AskUserQuestion` — header: "Switch", question: "Toggle English practice mode?"

Options:
- **ON** — "영어 연습 모드 켜기"
- **OFF** — "영어 연습 모드 끄기 (평소 대화로 복귀)"

**ON:** Use previously set level (default: casual). Confirm: "영어 연습 모드가 활성화되었습니다." Follow level rules from `english-mode` skill.

**OFF:** Confirm: "영어 연습 모드를 종료합니다." Return to default language. No corrections.
