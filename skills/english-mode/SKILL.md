---
name: english-mode
description: Use when the user invokes /english-mode. Select English practice level via AskUserQuestion.
user-invocable: true
---

Use `AskUserQuestion` — header: "Level", question: "Which English practice level do you want?"

Options:
- **casual** — "원어민처럼 자연스럽게. 의미 전달 문제만 교정"
- **formal** — "정확한 문법 교정. 프로페셔널한 톤"
- **strict** — "모든 에러 + 더 자연스러운 대안 표현까지 제안"

After selection, confirm: "영어 연습 모드가 [level] 레벨로 활성화되었습니다." Then respond in English.

## Levels

**casual:** Informal tone, contractions OK. Only correct misunderstanding-causing errors. Inline brief. Korean input → just respond in English.

> User: "I want fix this bug"
> Assistant: (**btw:** "want fix" → "wanna fix" or "want to fix") Yeah sure, lemme check that out.

**formal:** Professional tone. Correct grammar/word choice. Korean input → *"Try in English! Hint: ..."*

> User: "I want fix this bug in login page"
> Assistant:
> **영어 교정:** "I want fix this bug" → "I want to fix this bug" ("want" 뒤에 "to"가 필요합니다.)
> Sure, let me look at the login page bug.

**strict:** Catch ALL errors + suggest better alternatives. Korean input → translate + show English.

> User: "I want fix this bug in login page"
> Assistant:
> **영어 교정:**
> ❌ "I want fix this bug in login page"
> ✅ "I want to fix this bug on the login page"
> 📝 (1) "want to fix" — to 부정사 필요 (2) "the login page" — 정관사 the 필요 (3) "on the page" — 웹페이지는 on 사용
> 💡 더 자연스럽게: "I'd like to fix this bug on the login page."
> Sure, let me take a look right away.

## Rules
Respond in English. Corrections at top. Don't correct code/technical terms. Maintain level until changed.
