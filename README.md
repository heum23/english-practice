# 🇺🇸 English Practice Mode — Claude Code Plugin

코딩하면서 자연스럽게 영어 연습하는 Claude Code 플러그인입니다.

## 설치

```bash
# 1. 마켓플레이스 등록
/plugin marketplace add heum23/english-practice

# 2. 플러그인 설치
/plugin install english-practice@english-practice

# 3. 플러그인 적용
/reload-plugins
```

## 사용법

### `/english-mode` — 레벨 선택

레벨을 선택하면 영어 모드가 자동으로 켜집니다.

| 레벨 | 설명 | 교정 범위 |
|------|------|----------|
| **casual** | 원어민처럼 자연스러운 톤 | 의미 전달에 문제 있는 것만 |
| **formal** | 프로페셔널한 톤 | 문법, 어휘, 어색한 표현 |
| **strict** | 빡세게 | 모든 에러 + 더 나은 표현 제안 |

### `/english-switch` — ON/OFF 토글

영어 모드를 켜거나 끕니다. 이전에 설정한 레벨이 유지됩니다.

## 레벨별 예시

### casual
```
You:    "I want fix this bug"
Claude: (**btw:** "want fix" → "wanna fix" or "want to fix")
        Yeah sure, lemme check that out.
```

### formal
```
You:    "I want fix this bug"
Claude: **영어 교정:** "I want fix" → "I want to fix" ("want" 뒤에 "to"가 필요합니다.)
        Sure, let me look at the bug now.
```

### strict
```
You:    "I want fix this bug in login page"
Claude: **영어 교정:**
        ❌ "I want fix this bug in login page"
        ✅ "I want to fix this bug on the login page"
        📝 (1) want to fix — to 부정사 필요
           (2) the login page — 정관사 the 필요
           (3) on the page — 웹페이지는 on 사용
        💡 더 자연스럽게: "I'd like to fix this bug on the login page."
        Sure, let me take a look right away.
```

### 한국어로 입력하면?

| 레벨 | 반응 |
|------|------|
| casual | 그냥 영어로 답변 |
| formal | "Try in English! Hint: ..." 힌트 제공 |
| strict | 번역 + 영어 표현 제시 |

## 삭제

```bash
/plugin uninstall english-practice@english-practice
```

## License

MIT
