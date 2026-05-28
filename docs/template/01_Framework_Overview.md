# Framework Overview

> Reusable Fullstack Development Framework Specification

---

# 1. Overview

이 템플릿은 AI와 함께 빠르고 반복 가능하게 장기 유지보수 가능한 서비스를 구축하기 위한 Fullstack Development Framework이다.

목표:

* 반복되는 초기 개발 제거
* 재사용 가능한 workspace 구축
* 장기 유지보수 가능한 구조 확보
* 문서 기반 개발 체계 유지
* AI/Codex 친화적 개발 환경 구축

---

# 2. Framework Identity

이 템플릿의 방향:

```text
개인용 모노레포 템플릿
→ 재사용 가능한 Fullstack Framework
→ AI-Native Development Framework
```

핵심 정체성:

```text
Reusable Fullstack Development Framework
```

---

# 3. Core Principles

Framework는 다음 원칙을 따른다.

```text
Predictable
Explicit
Reusable
Composable
Document-Driven
AI-Friendly
```

---

# 4. Package-Oriented Development

Workspace는 다음 기준으로 나눈다.

```text
apps
= 실행 단위

packages
= 재사용 단위
```

반복되는 기능은 app 내부에 계속 복사하지 않고 package로 분리한다.

---

# 5. Documentation Model

문서는 두 축으로 분리한다.

```text
docs/template
= framework specification

docs/project
= project specification
```

Template 문서는 만드는 방법을 설명하고, project 문서는 무엇을 만들지 설명한다.

---

# 6. One-Line Summary

```text
Framework는 반복을 줄이고,
구조를 명시하며,
사람과 AI가 같은 기준으로 개발하게 만든다.
```
