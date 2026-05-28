# Workspace Architecture

> Monorepo Workspace Architecture Specification

---

# 1. Overview

이 문서는 monorepo workspace 구조와 dependency boundary를 정의한다.

목표:

* app/package 역할 분리
* 재사용 가능한 package 구조 확보
* 신규 프로젝트 생성 단순화
* AI/Codex가 예측 가능한 구조 유지

---

# 2. Root Structure

기본 구조:

```text
monorepo-starter/

  apps/
    frontend/
    backend/

  packages/
    ui/
    types/
    utils/
    config/
    prisma/

  docs/
    template/
    project/

  scripts/
```

---

# 3. apps/

`apps/`는 실제 실행 가능한 application 영역이다.

원칙:

* 독립 실행 가능
* 독립 build 가능
* shared package 사용 가능
* app 간 직접 참조 금지

예:

```text
apps/frontend
apps/backend
```

---

# 4. packages/

`packages/`는 재사용 가능한 shared package 영역이다.

원칙:

* app independent
* reusable
* isolated
* independently buildable

예:

```text
packages/ui
packages/types
packages/utils
packages/config
packages/prisma
```

---

# 5. Dependency Rules

## Allowed

```text
apps/* → packages/*
packages/* → packages/*
```

---

## Forbidden

```text
frontend → backend
backend → frontend
```

공유가 필요한 코드는 app 간 직접 참조하지 않고 package로 분리한다.

---

# 6. Configuration Strategy

공통 설정은 `packages/config`에서 관리한다.

포함 가능:

* eslint
* prettier
* tsconfig
* commitlint

목표:

```text
workspace 전체 규칙 통일
```

---

# 7. scripts/

자동화 스크립트 영역이다.

예:

```text
create-app
create-package
generate-domain
```

목표:

* 반복 작업 제거
* workspace consistency 유지
* 향후 CLI generator 기반 마련

---

# 8. One-Line Summary

```text
App은 실행 단위,
Package는 재사용 단위,
Workspace는 구조의 기준점이다.
```
