# Backend Architecture

> Project Backend Architecture Specification

---

# 1. Overview

이 문서는 프로젝트별 backend architecture를 정의한다.

Template의 backend 구조를 따르되, 실제 서비스의 domain, module, external integration 기준을 이 문서에 기록한다.

관련 template 문서:

* `docs/template/04_Backend_Architecture.md`
* `docs/template/06_Database_Strategy.md`
* `docs/template/07_Environment_Strategy.md`

---

# 2. Backend Modules

| Module | Purpose | Domain |
| ------ | ------- | ------ |
| TBD    | TBD     | TBD    |

---

# 3. Domain Structure

예상 구조:

```text
src/domains/{domain}/
  dto/
  controller/
  service/
  repository/
  types/
```

---

# 4. External Integrations

| Integration | Purpose | Notes |
| ----------- | ------- | ----- |
| TBD         | TBD     | TBD   |

---

# 5. Background Jobs

필요한 job:

* TBD

---

# 6. Event / Queue Usage

Event 또는 queue 사용 여부:

```text
TBD
```

---

# 7. Backend Rules

프로젝트별 backend rule:

* TBD

---

# 8. One-Line Summary

```text
Backend Architecture는 프로젝트 backend의 module, domain, integration 기준을 정의한다.
```
