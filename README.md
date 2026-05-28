# Monorepo Starter Framework

> Reusable Fullstack Development Framework  
> Vite + React + Tailwind + Sass + NestJS + Prisma

---

# Overview

이 프로젝트는 AI와 함께 빠르고 반복 가능하게 장기 유지보수 가능한 서비스를 구축하기 위한 재사용 가능한 Fullstack Development Framework이다.

반복되는 초기 개발 작업을 줄이고, 새 프로젝트에서도 그대로 복사해서 사용할 수 있는 표준 workspace 구조를 제공하는 것을 목표로 한다.

핵심 목표:

* 반복되는 초기 개발 제거
* Package-Oriented Development 기반 workspace 구축
* 장기 유지보수 가능한 구조 확보
* 문서 기반 개발 체계 구축
* AI/Codex 친화적 개발 환경 구축
* 사람 + AI 협업 workflow 표준화

---

# Philosophy

## Package-Oriented Development

```text
apps
= 실행 단위

packages
= 재사용 단위
```

반복되는 기능은 app 내부에 복사하지 않고 package로 분리한다.

---

## Document-Driven Development

문서는 단순 설명이 아니라 구조의 기준점이다.

```text
README
= onboarding

docs/template
= framework specification

docs/project
= project specification
```

---

## AI-Native Direction

AI/Codex가 구조를 쉽게 이해하고 반복 가능한 방식으로 작업할 수 있도록 다음 원칙을 유지한다.

* predictable structure
* explicit naming
* minimal ambiguity
* reusable patterns
* composable modules
* document-first workflow

---

# Tech Stack

## Frontend

* React
* Vite
* TypeScript
* TailwindCSS
* Sass
* React Router
* React Query

## Backend

* NestJS
* TypeScript
* Swagger
* class-validator
* JWT Authentication

## Database

* Prisma ORM
* PostgreSQL

Database layer는 optional package로 유지한다.

## Tooling

* pnpm workspace
* ESLint
* Prettier
* Husky
* lint-staged
* Commitlint

---

# Workspace Structure

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

# Quick Start

## Install

```bash
pnpm install
```

## Run Frontend

```bash
pnpm dev:frontend
```

## Run Backend

```bash
pnpm dev:backend
```

## Run All Apps

```bash
pnpm dev
```

---

# Development Workflow

기본 workflow:

```text
Requirement
→ Architecture
→ Prompt
→ Implementation
→ Verification
→ Documentation
```

---

# Root Scripts

```bash
pnpm dev
pnpm build
pnpm lint
pnpm typecheck
pnpm clean
pnpm reinstall
```

Database 사용 시:

```bash
pnpm db:generate
pnpm db:migrate
pnpm db:deploy
```

---

# Documentation

## Template Specification

이 모노레포 프레임워크 자체의 기준 문서이다.

* [01_Framework_Overview](docs/template/01_Framework_Overview.md)
* [02_Workspace_Architecture](docs/template/02_Workspace_Architecture.md)
* [03_Frontend_Architecture](docs/template/03_Frontend_Architecture.md)
* [04_Backend_Architecture](docs/template/04_Backend_Architecture.md)
* [05_Shared_Packages](docs/template/05_Shared_Packages.md)
* [06_Database_Strategy](docs/template/06_Database_Strategy.md)
* [07_Environment_Strategy](docs/template/07_Environment_Strategy.md)
* [08_Development_Workflow](docs/template/08_Development_Workflow.md)
* [09_Code_And_Git_Conventions](docs/template/09_Code_And_Git_Conventions.md)
* [10_Template_Usage_And_Roadmap](docs/template/10_Template_Usage_And_Roadmap.md)

## Project Specification

이 템플릿으로 실제 서비스를 만들 때 채우는 프로젝트별 문서이다.

* [Project Docs Index](docs/project/README.md)
* [01_Project_Overview](docs/project/01_Project_Overview.md)
* [02_Requirements](docs/project/02_Requirements.md)
* [03_Domain_Model](docs/project/03_Domain_Model.md)
* [04_Database_Schema](docs/project/04_Database_Schema.md)
* [05_API_Design](docs/project/05_API_Design.md)
* [06_Frontend_IA](docs/project/06_Frontend_IA.md)
* [07_Backend_Architecture](docs/project/07_Backend_Architecture.md)
* [08_Security_Policy](docs/project/08_Security_Policy.md)
* [09_Operation_Policy](docs/project/09_Operation_Policy.md)
* [10_Roadmap](docs/project/10_Roadmap.md)

---

# One-Line Summary

```text
AI와 함께 빠르고 반복 가능하게
장기 유지보수 가능한 서비스를 구축하기 위한
재사용 가능한 Fullstack Development Framework.
```
