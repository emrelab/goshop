# GoShop

A beginner-friendly, single-store e-commerce learning project built with **Go**.

> **Project stage:** Roadmap and GitHub issues are prepared. This repository is being developed incrementally; features described below are **planned**, not automatically implemented.

## Purpose

Learn backend engineering by building a small, tangible online shop for tech accessories (keyboards, mice, headphones, cables, and similar products). Work through real product flows rather than following lesson numbers in order. The accompanying [course coverage matrix](docs/COURSE_COVERAGE.md) tracks all 16 supplied Go lesson reports.

**The priority is understanding each step, not shipping a complex production system quickly.**

## Planned MVP

| Customer | Administrator |
| --- | --- |
| Browse/search products and view details | Create and edit products |
| Register, sign in and sign out | Update prices and inventory |
| Add/update/remove cart items | View and update order status |
| Place a **simulated** order | See a simple admin dashboard |
| View own order history | |

**Not in scope:** real payments, courier/shipping integrations, multi-vendor marketplace, microservices, or a mobile app.

## Development principles

- **Small steps:** work on one GitHub Issue at a time; keep the app working after each milestone.
- **Learn first:** use plain Go and its standard library where possible; add a library only when its role is understood.
- **Simple before advanced:** begin with in-memory data; introduce PostgreSQL later; keep Redis/MongoDB and advanced network topics in optional learning labs.
- **Test while building:** add focused tests and handle errors as features are implemented.
- **No fake progress:** mark an Issue complete only when the required code, tests and/or documentation exist and can be verified.

## Roadmap

| Milestone | Deliverable | Issues |
| --- | --- | --- |
| M0 – Project Foundation | Go module, scope, repository conventions and CI foundation | [#1–#3](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M0-) |
| M1 – Product Catalog | Models, sample data, product API, search and simple listing page | [#4–#9](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M1-) |
| M2 – Inventory Management | PostgreSQL, SQL migrations, CRUD, stock and ORM comparison | [#10–#15](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M2-) |
| M3 – User Authentication | Registration, login, sessions and role authorization | [#16–#21](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M3-) |
| M4 – Shopping Cart | Cart services, totals, persistence and UI/API | [#22–#27](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M4-) |
| M5 – Checkout & Orders | Transactional checkout, stock integrity and order history | [#28–#33](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M5-) |
| M6 – Storefront & Administration | Connected customer and admin web pages | [#34–#39](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M6-) |
| M7 – Testing & Release | Security review, CI, Docker, advanced labs and documentation | [#40–#45](https://github.com/emrelab/goshop/issues?q=is%3Aissue+M7-) |

Milestones organize the **product-building workflow**, not the chronological order of the course lessons. The 45 Issues are a roadmap, not a claim of completed functionality.

## Technical approach (planned)

- **Language:** Go
- **HTTP:** `net/http`, JSON handlers, `httptest`
- **UI:** Go `html/template` with minimal CSS
- **Database:** PostgreSQL and `database/sql`; GORM explored for comparison
- **Authentication:** server-side sessions with secure cookies
- **Testing:** Go `testing` and integration tests
- **Optional labs:** Redis, MongoDB, channels/goroutines, TCP/UDP, patterns
- **Packaging:** Docker Compose in a later milestone

The final directory structure and commands will evolve during M0–M7. **Do not assume the above technologies are already installed or working.**

## Getting started (current stage)

1. Clone this repository or open your existing local clone.
2. Read [Project Context](docs/PROJECT_CONTEXT.md) to understand current status, project decisions and how to resume.
3. Pick the next unfinished Issue (start with [#1](https://github.com/emrelab/goshop/issues/1) if no progress is verified).
4. Follow that Issue's checklist and acceptance criteria. Verify locally, commit, push and update the Issue once complete.

A reliable `go run`/Docker startup guide will be added once a runnable entry point has been committed; **there is no claim of an already deployed shop**.

## Project tracking and handoff

- [Issues](https://github.com/emrelab/goshop/issues)
- [Milestones](https://github.com/emrelab/goshop/milestones)
- [GitHub Projects](https://github.com/users/emrelab/projects) — board name: **GoShop Development**
- [Project Context / AI handoff](docs/PROJECT_CONTEXT.md)
- [Lesson Coverage Matrix](docs/COURSE_COVERAGE.md)

If you are an AI coding agent or a new contributor, read **Project Context first**, then inspect the **actual Git state and open Issues** before proposing changes.
