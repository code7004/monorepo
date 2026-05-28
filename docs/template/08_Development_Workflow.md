# Development Workflow

> Document-Driven & AI-Augmented Workflow Specification

---

# 1. Overview

이 문서는 workspace의 표준 개발 workflow를 정의한다.

목표:

* 예측 가능한 개발 흐름 유지
* 문서 기반 개발 체계 유지
* AI/Codex와 반복 가능한 협업 구조 확보
* 구현 후 검증과 문서 동기화 유지

---

# 2. Core Workflow

기본 흐름:

```text
Requirement
→ Architecture
→ Prompt
→ Implementation
→ Verification
→ Documentation
```

---

# 3. Requirement

구현 전에 요구사항을 정의한다.

포함:

* 목적
* 사용자 흐름
* API 필요 여부
* 상태 변화
* 예외 상황
* 검증 기준

---

# 4. Architecture

구현 전에 구조를 결정한다.

검토 대상:

* frontend domain
* backend domain
* shared types
* shared ui
* database schema
* env keys
* package extraction 필요 여부

---

# 5. Prompt

AI/Codex에게 작업을 요청할 때는 다음 정보를 포함한다.

```text
목표:
관련 문서:
수정 대상:
구조 원칙:
검증:
주의사항:
```

---

# 6. Implementation

원칙:

* 작은 단위로 변경
* 기존 구조 우선
* package 재사용 우선
* 명시적 naming 사용
* 불필요한 abstraction 지양

---

# 7. Verification

기본 검증:

```bash
pnpm lint
pnpm typecheck
pnpm build
```

기능별 검증:

* frontend rendering
* backend API response
* env validation
* database migration
* package build

---

# 8. Documentation Update

다음 변경은 문서 업데이트가 필요하다.

* folder structure 변경
* package 추가
* env 추가
* API response shape 변경
* database schema 변경
* workflow 변경
* convention 변경

---

# 9. One-Line Summary

```text
요구사항을 구조로 바꾸고,
구조를 구현으로 옮기며,
검증과 문서로 반복 가능하게 만든다.
```
