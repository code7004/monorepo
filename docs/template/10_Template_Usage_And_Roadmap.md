# Template Usage And Roadmap

> Template Usage & Long-Term Roadmap Specification

---

# 1. Overview

이 문서는 템플릿을 새 프로젝트에 재사용하는 방법과 장기 발전 방향을 정의한다.

목표:

* 새 프로젝트 초기 구조 고민 제거
* project docs 작성 기준 제공
* template의 장기 확장 방향 관리
* AI-Native Development Framework로 발전

---

# 2. New Project Flow

권장 흐름:

```text
1. Template 복사
2. Project name 변경
3. Package manager install
4. Environment file 구성
5. Optional package 선택
6. Project docs 작성
7. Domain 설계
8. Initial verification
```

---

# 3. Project Docs Setup

새 프로젝트에서 우선 작성할 문서:

```text
docs/project/01_Project_Overview.md
docs/project/02_Requirements.md
docs/project/03_Domain_Model.md
docs/project/10_Roadmap.md
```

구현이 시작되면 다음 문서를 함께 채운다.

```text
docs/project/04_Database_Schema.md
docs/project/05_API_Design.md
docs/project/06_Frontend_IA.md
docs/project/07_Backend_Architecture.md
docs/project/08_Security_Policy.md
docs/project/09_Operation_Policy.md
```

---

# 4. Package Selection

기본 유지 권장:

```text
packages/types
packages/utils
packages/config
```

Frontend가 있으면:

```text
packages/ui
```

Database가 있으면:

```text
packages/prisma
```

---

# 5. Initial Verification

새 프로젝트 생성 후 최소 검증:

```bash
pnpm install
pnpm lint
pnpm typecheck
pnpm build
```

---

# 6. Roadmap

장기 방향:

```text
Template Stabilization
→ Shared Foundation
→ UI System
→ API & Type Automation
→ Auth Foundation
→ Verification System
→ Deployment Foundation
→ AI Tooling
→ CLI Generator
```

---

# 7. Roadmap Rules

새 항목 추가 기준:

* 반복 작업을 줄이는가
* 재사용성을 높이는가
* 문서화 가능한가
* AI가 이해하고 실행할 수 있는가
* 기존 구조와 충돌하지 않는가

---

# 8. One-Line Summary

```text
Template은 구조를 복사하고,
project docs는 목적을 채우며,
roadmap은 framework의 성장 방향을 관리한다.
```
