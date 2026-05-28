# Code And Git Conventions

> Workspace Code & Git Convention Specification

---

# 1. Overview

이 문서는 workspace 전체의 코드 규칙과 Git 운영 기준을 정의한다.

목표:

* 코드 일관성 유지
* 명확한 변경 이력 유지
* AI/Codex 친화적 구조 유지
* 검증 가능한 협업 흐름 확보

---

# 2. Code Principles

```text
Readability First
Predictable Structure
Explicit Over Magic
Reusable First
```

---

# 3. Naming Rules

| Target              | Rule             |
| ------------------- | ---------------- |
| folder              | kebab-case       |
| file                | kebab-case       |
| React component     | PascalCase       |
| variable / function | camelCase        |
| constant            | UPPER_SNAKE_CASE |

---

# 4. TypeScript Rules

원칙:

* strict mode 유지
* `any` 최소화
* 공용 함수는 명시적 타입 우선
* shared types 우선 사용
* DTO와 domain type 분리

---

# 5. Import Rules

순서:

```text
1. external libraries
2. shared packages
3. internal modules
4. relative imports
```

상대 경로가 깊어지면 alias 사용을 고려한다.

---

# 6. Frontend Rules

원칙:

* domain-oriented structure
* pages는 composition 중심
* business logic은 domains에 위치
* server state는 React Query 우선
* global state 최소화

---

# 7. Backend Rules

원칙:

* controller는 얇게 유지
* business logic은 service에 위치
* database access는 repository 우선
* DTO validation 유지
* Prisma type 직접 노출 금지

---

# 8. Git Branch Strategy

기본 브랜치:

```text
main
develop
feature/*
fix/*
```

---

# 9. Commit Convention

기본:

```text
type: message
```

예:

```text
feat: add auth api client
fix: resolve login redirect issue
docs: update project requirements
refactor: split dashboard domain
```

권장 type:

```text
feat
fix
refactor
docs
style
test
chore
```

---

# 10. Merge Verification

Merge 전 최소 검증:

```bash
pnpm lint
pnpm typecheck
pnpm build
```

---

# 11. One-Line Summary

```text
명확하게 나누고,
예측 가능하게 유지하며,
작게 기록하고 검증한다.
```
