# Shared Packages

> Shared Package & UI System Specification

---

# 1. Overview

이 문서는 workspace 내 shared package와 UI system의 역할을 정의한다.

목표:

* 공통 코드 재사용
* app 간 중복 제거
* UI 일관성 유지
* package-oriented development 정착

---

# 2. Package Principles

Shared package는 다음 원칙을 따른다.

```text
Reusable
Independent
Predictable
Composable
```

---

# 3. Recommended Packages

```text
packages/
  ui/
  types/
  utils/
  config/
  prisma/
```

---

# 4. packages/ui

공통 UI component package.

포함 가능:

* Button
* Input
* Modal
* Dropdown
* Tabs
* Table
* Toast
* Form Field

원칙:

* composable
* reusable
* predictable props
* domain independent

---

# 5. packages/types

공통 타입 package.

예:

```ts
ApiResponse<T>
PaginationResponse<T>
Nullable<T>
```

원칙:

* frontend/backend 공유 가능
* business independent 유지
* runtime dependency 최소화

---

# 6. packages/utils

공통 utility package.

예:

```ts
formatDate()
sleep()
generateId()
debounce()
```

원칙:

* pure function 우선
* dependency 최소화
* side-effect 최소화

---

# 7. packages/config

공통 설정 package.

포함 가능:

* eslint
* prettier
* tsconfig
* commitlint

---

# 8. UI System Direction

UI system은 다음 원칙을 따른다.

* composition over inheritance
* controlled components first
* variant based API
* accessibility 고려
* Storybook 확장 가능

예:

```tsx
<Button variant="primary" size="md" />
```

---

# 9. One-Line Summary

```text
공통 기능은 package로 분리하고,
UI는 조합 가능하게 유지하며,
workspace 전체에서 재사용한다.
```
