# Frontend Architecture

> React + Vite Frontend Architecture Specification

---

# 1. Overview

Frontend는 domain 기반 구조와 재사용 가능한 UI 시스템을 기준으로 설계한다.

목표:

* 빠른 UI 개발
* domain 기반 구조 유지
* 재사용 가능한 UI 시스템 구축
* AI/Codex 친화적 구조 유지

---

# 2. Core Stack

기본 기술:

* React
* Vite
* TypeScript
* TailwindCSS
* Sass
* React Router
* React Query

선택 가능:

* Zustand
* Redux Toolkit
* Framer Motion

---

# 3. Directory Structure

기본 구조:

```text
src/
  app/
  pages/
  domains/
  components/
  layouts/
  hooks/
  routes/
  services/
  store/
  styles/
  utils/
```

---

# 4. Layer Rules

| Layer      | Purpose                  |
| ---------- | ------------------------ |
| app        | app bootstrap/providers  |
| pages      | route/page composition   |
| domains    | business feature logic   |
| components | app-level reusable UI    |
| layouts    | layout composition       |
| services   | external API access      |
| store      | minimal global state     |

---

# 5. State Strategy

우선순위:

```text
1. local state
2. React Query
3. global state
```

Server state는 React Query를 우선 사용하고, global state는 auth/theme/app config처럼 제한된 범위에만 사용한다.

---

# 6. API Strategy

공통 API client를 사용한다.

예:

```text
services/api-client.ts
domains/{domain}/api
```

원칙:

* token handling 중앙화
* domain별 API grouping
* shared type 우선 사용

---

# 7. UI Strategy

공통 UI는 `packages/ui` 우선 사용한다.

반복 UI 예:

* Button
* Input
* Modal
* Dropdown
* Table
* Toast

Domain specific component는 app 내부 domain에 둔다.

---

# 8. Styling Strategy

기본 조합:

```text
TailwindCSS + Sass
```

원칙:

* utility first
* global style 최소화
* component-scoped styling 우선
* design token 확장 고려

---

# 9. One-Line Summary

```text
Frontend는 domain 중심으로 구성하고,
UI는 재사용 가능하게 유지하며,
상태는 단순하게 관리한다.
```
