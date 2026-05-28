# API Design

> Project API Design Specification

---

# 1. Overview

이 문서는 프로젝트 API 설계 기준과 endpoint contract를 정의한다.

API는 frontend와 backend가 공유하는 계약이다.

관련 template 문서:

* `docs/template/04_Backend_Architecture.md`
* `docs/template/05_Shared_Packages.md`
* `docs/template/09_Code_And_Git_Conventions.md`

---

# 2. API Principles

원칙:

* REST first
* DTO 기반 validation
* 명확한 response shape
* 명확한 error code
* shared type 우선
* backend domain 기준 endpoint 구성

---

# 3. Response Shape

기본 response:

```ts
{
  data,
  meta,
}
```

Error response:

```ts
{
  statusCode,
  code,
  message,
  timestamp,
}
```

---

# 4. Endpoint List

| Method | Path | Purpose | Auth | Domain |
| ------ | ---- | ------- | ---- | ------ |
| TBD    | TBD  | TBD     | TBD  | TBD    |

---

# 5. Request / Response DTO

DTO 초안:

```ts
// TBD
```

---

# 6. Error Codes

| Code | Meaning | HTTP Status |
| ---- | ------- | ----------- |
| TBD  | TBD     | TBD         |

---

# 7. One-Line Summary

```text
API Design은 frontend와 backend가 함께 따르는 통신 계약이다.
```
