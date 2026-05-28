# Security Policy

> Project Security Policy Specification

---

# 1. Overview

이 문서는 프로젝트의 보안 정책을 정의한다.

포함:

* authentication
* authorization
* secret handling
* data protection
* frontend exposure rule
* logging restriction

관련 template 문서:

* `docs/template/04_Backend_Architecture.md`
* `docs/template/07_Environment_Strategy.md`
* `docs/template/09_Code_And_Git_Conventions.md`

---

# 2. Authentication

인증 방식:

```text
TBD
```

예:

* JWT
* session
* OAuth
* API key

---

# 3. Authorization

권한 모델:

```text
TBD
```

예:

* role-based access
* resource-based access
* admin-only access

---

# 4. Secret Policy

Secret 관리 원칙:

* frontend env에 secret 금지
* repository에 production secret commit 금지
* backend env는 fail-fast validation 적용

---

# 5. Sensitive Data

민감 정보:

* TBD

처리 기준:

* TBD

---

# 6. Logging Policy

로그 금지 대상:

```text
password
token
secret
private key
api key
```

---

# 7. One-Line Summary

```text
Security Policy는 인증, 권한, secret, 민감 정보 처리 기준을 정의한다.
```
