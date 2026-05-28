# Database Strategy

> Database & Prisma Strategy Specification

---

# 1. Overview

이 문서는 workspace의 database와 Prisma 사용 전략을 정의한다.

Database는 optional layer로 유지한다.

목표:

* 명시적인 schema 관리
* migration 기반 변경 이력 유지
* backend와 database layer 분리
* repository abstraction 유지

---

# 2. Recommended Structure

```text
packages/prisma/
  prisma/
    schema.prisma
    migrations/
  src/
```

---

# 3. Schema Principles

원칙:

* explicit schema first
* UUID 기반 ID
* `createdAt`, `updatedAt` 기본 포함
* 관계 이름 명확화
* 상태값은 enum 우선
* 금액/정밀 수치는 Decimal 사용

---

# 4. Migration Rules

기본 흐름:

```text
schema change
→ migration generate
→ sql review
→ apply
```

Production direct push는 금지한다.

---

# 5. Repository Strategy

Backend에서는 Prisma 직접 호출보다 repository 계층을 우선한다.

목표:

* query centralization
* testability
* business logic isolation

---

# 6. DTO & Prisma Separation

Prisma model을 API response에 직접 노출하지 않는다.

기본 흐름:

```text
Prisma Model
→ Domain Type
→ DTO Response
```

---

# 7. One-Line Summary

```text
Database는 명시적으로 설계하고,
migration 기준으로 관리하며,
repository 계층으로 분리한다.
```
