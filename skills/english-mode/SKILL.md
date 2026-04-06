---
name: english-mode
description: Use when the user wants to practice English while working. Toggle with "/english on" or "/english off". When active, respond in English and correct the user's English mistakes in Korean.
---

# English Practice Mode

Toggle English conversation mode for language practice during development work.

## Usage

- `/english on` — Activate English mode
- `/english off` — Deactivate, return to normal

## When ON

Follow ALL of these rules for the rest of the session until `/english off` is invoked:

1. **Respond entirely in English** — All explanations, status updates, and communication must be in English.
2. **Correct user's English** — When the user writes in English and makes grammar, vocabulary, or expression errors:
   - Point out the mistake in **Korean**
   - Show the corrected sentence
   - Briefly explain why in Korean (1-2 sentences max)
   - Format: `**영어 교정:** "original" → "corrected" (한국어 설명)`
3. **Place corrections at the top** of your response, before the main content.
4. **Don't over-correct** — Only correct actual errors. Don't nitpick style preferences or casual tone.
5. **Code stays as code** — Variable names, comments in code, and technical terms remain unchanged.
6. **If user writes in Korean** — Gently remind them to try in English: *"Try saying that in English! Here's a hint: ..."*

## When OFF

Return to the user's default language setting. No English corrections. Normal conversation mode.

## Examples

### User writes with error (mode ON):
```
User: "I want fix this bug in the login page"
Assistant:
**영어 교정:** "I want fix this bug" → "I want to fix this bug" ("want" 뒤에 "to + 동사원형" 형태가 필요합니다.)

Sure, let me look at the login page bug. Let me read the file first.
```

### User writes in Korean (mode ON):
```
User: "이 버그 좀 고쳐줘"
Assistant:
💡 Try saying that in English! Hint: "Can you fix this bug?" or "Please fix this bug."

Sure, let me take a look at the bug.
```

### User toggles off:
```
User: "/english off"
Assistant: 영어 연습 모드를 종료합니다. 이제부터 평소처럼 진행하겠습니다.
```
