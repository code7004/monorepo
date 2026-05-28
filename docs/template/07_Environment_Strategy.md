# Environment Strategy

> Environment & Configuration Strategy Specification

---

# 1. Overview

이 문서는 workspace 전체의 환경 변수 및 실행 환경 전략을 정의한다.

목표:

* frontend/backend env 역할 분리
* secret 관리 일관성 유지
* fail-fast configuration 유지
* AI/Codex가 예측 가능한 env 구조 확보

---

# 2. Environment Principles

```text
Explicit
Separated
Centralized
Predictable
```

---

# 3. Frontend Env

Frontend는 public configuration만 허용한다.

Vite 기준:

```text
VITE_*
```

예:

```text
VITE_API_URL
VITE_APP_ENV
```

Forbidden:

```text
secret
private key
database url
jwt secret
api secret
```

---

# 4. Backend Env

Backend는 secret 관리 영역이다.

예:

```text
DATABASE_URL
JWT_SECRET
REDIS_URL
APP_ENV
LOG_LEVEL
```

원칙:

* `process.env` 직접 사용 최소화
* EnvService 우선 사용
* 필수 env 누락 시 즉시 종료

---

# 5. Environment Files

권장:

```text
.env
.env.local
.env.development
.env.production
.env.example
```

`.env.example`에는 required key와 sample value를 기록한다.

---

# 6. Environment Names

기본 환경:

```text
local
development
staging
production
```

---

# 7. One-Line Summary

```text
환경 변수는 명시적으로 관리하고,
secret은 backend에 격리하며,
환경은 명확하게 분리한다.
```
