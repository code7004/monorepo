# Documentation

> Workspace Documentation Map

---

# 1. Overview

이 workspace의 문서는 두 축으로 분리한다.

```text
docs/template
= 이 모노레포 프레임워크 자체 설명

docs/project
= 이 템플릿으로 만든 실제 서비스 설명
```

목표:

* template specification과 project specification 분리
* 새 프로젝트 생성 시 project docs만 교체 가능
* AI/Codex가 문서의 역할을 명확히 구분
* framework 규칙과 service 요구사항의 충돌 방지

---

# 2. docs/template

`docs/template/`은 이 모노레포 템플릿 자체의 기준 문서이다.

역할:

* workspace architecture
* frontend/backend architecture
* package strategy
* environment strategy
* development workflow
* code/git conventions
* template usage and roadmap

이 문서는 여러 프로젝트에서 재사용되는 framework specification이다.

문서 목록:

* `01_Framework_Overview.md`
* `02_Workspace_Architecture.md`
* `03_Frontend_Architecture.md`
* `04_Backend_Architecture.md`
* `05_Shared_Packages.md`
* `06_Database_Strategy.md`
* `07_Environment_Strategy.md`
* `08_Development_Workflow.md`
* `09_Code_And_Git_Conventions.md`
* `10_Template_Usage_And_Roadmap.md`

---

# 3. docs/project

`docs/project/`는 이 템플릿으로 만든 실제 서비스의 기준 문서이다.

역할:

* service purpose
* product requirements
* domain specification
* database schema
* API design
* frontend information architecture
* backend architecture
* security policy
* operation/deployment notes
* project roadmap

새 서비스를 만들 때 이 영역을 프로젝트 목적에 맞게 작성한다.

문서 목록:

* `01_Project_Overview.md`
* `02_Requirements.md`
* `03_Domain_Model.md`
* `04_Database_Schema.md`
* `05_API_Design.md`
* `06_Frontend_IA.md`
* `07_Backend_Architecture.md`
* `08_Security_Policy.md`
* `09_Operation_Policy.md`
* `10_Roadmap.md`

---

# 4. Documentation Rule

기본 원칙:

```text
template docs
= 바꾸기 어려운 framework 기준

project docs
= 서비스마다 달라지는 product 기준
```

Framework 구조를 바꾸면 `docs/template/`을 수정한다.

서비스 요구사항을 바꾸면 `docs/project/`를 수정한다.

---

# 5. One-Line Summary

```text
template은 만드는 방법을 설명하고,
project는 무엇을 만들지 설명한다.
```
