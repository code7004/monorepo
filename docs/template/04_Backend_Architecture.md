# Backend Architecture

> NestJS Backend Architecture Specification

---

# 1. Overview

Backend는 domain 기반 구조와 명확한 책임 분리를 기준으로 설계한다.

목표:

* business logic 분리
* 확장 가능한 API architecture 유지
* 외부 의존성 격리
* AI/Codex 친화적 구조 유지

---

# 2. Core Stack

기본 기술:

* NestJS
* TypeScript
* Swagger
* class-validator
* class-transformer
* JWT Authentication

선택 가능:

* Prisma
* Redis
* BullMQ
* WebSocket

---

# 3. Directory Structure

기본 구조:

```text
src/
  core/
  domains/
  infra/
  common/
```

---

# 4. core/

Framework level 공통 시스템.

예:

```text
env/
logger/
errors/
guards/
interceptors/
decorators/
```

---

# 5. domains/

Business domain 영역.

기본 구조:

```text
domains/{domain}/
  dto/
  controller/
  service/
  repository/
  entity/
  types/
```

---

# 6. Layer Rules

| Layer      | Purpose                         |
| ---------- | ------------------------------- |
| controller | request handling / response map |
| service    | business logic / orchestration  |
| repository | database access                 |
| dto        | request/response validation     |
| infra      | external integration            |

Controller는 얇게 유지하고, business rule은 service에 둔다.

---

# 7. API Rules

기본은 REST API 기준이다.

Response shape:

```ts
{
  data,
  meta,
}
```

Error shape:

```ts
{
  statusCode,
  code,
  message,
  timestamp,
}
```

---

# 8. Security & Logging

기본 원칙:

* JWT 기반 인증 가능
* role/permission guard 확장 고려
* request id / execution time 로깅
* password/token/secret 로그 금지

---

# 9. One-Line Summary

```text
Backend는 domain 중심으로 구성하고,
business logic은 service에 두며,
외부 의존성은 infra로 격리한다.
```
