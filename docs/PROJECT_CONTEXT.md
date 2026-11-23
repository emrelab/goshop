# GoShop — Project Context and AI Handoff

> **Last context review:** 2026-11-23. This file is an orientation snapshot, **not** a live dashboard. Recheck GitHub and the local checkout before taking action.

## 1. What GoShop is

GoShop is a **small, single-store e-commerce educational project in Go**. The example shop sells ordinary tech accessories such as keyboards, mice, headphones and USB cables.

The user's purpose is to learn the language and backend engineering through incremental, tangible features. The development sequence follows the **natural product workflow**, not the order of 16 course recordings. The project should stay approachable for a learner; avoid overengineering.

### Planned product flows

- **Customer:** browse/search product → view detail → register/login → cart → simulated checkout → own order history.
- **Admin:** manage products and stock → review orders → update order status.
- **Exclusions:** actual payment processing, shipping integrations, delivery tracking, multi-vendor marketplace, mobile apps, microservices.

**The plans do not mean the implementation exists yet.**

## 2. Source of truth and verified status

**Repository:** https://github.com/emrelab/goshop  
**Owner:** `emrelab`  
**Default branch:** `main`  
**GitHub Projects board:** `GoShop Development` (created/linked by user; exact item membership needs direct board verification).

As of **2026-11-23**, the GitHub connector verified:
- A public repository exists with `main` as default branch.
- The existing `README.md` had only `# goshop` **before** the documentation update that introduced this file.
- **45 planning Issues** exist with IDs `#1` through `#45`, organized under **8 milestones M0–M7**. Example milestone links were checked for every stage.
- User-provided screenshot showed the **Auto-add to project** workflow **On**, targeting `goshop` with filter `is:issue is:open`.
- The connector does **not** directly confirm that all 45 Issues are present as board cards, nor their `Todo / In Progress / Done` values.

**Local checkout (last user-provided path):**  
`/Users/emre/Development/Code/goshop`

Earlier, the user showed a local `main` branch with `README.md`, `docs/`, `go.mod` and `main.go` as untracked files, no commits, and no remote. The user subsequently said they configured the `origin` remote; the **current local branch history, commits, file contents, sync status and build are not re-verified**. These local files are **not assumed to be pushed to GitHub**.

### How to establish current progress

In the local repository, read-only first:

```bash
pwd
git status -sb
git remote -v
git log --oneline -5
git fetch origin
git status -sb
```

Then inspect files and run `go test ./...` **only if** a valid Go module and testable code are present. Compare actual work against the open Issues. Do not infer completion from a checkbox in a planning document.

**IMPORTANT:** Since this documentation is committed directly to `main`, an existing local checkout might now be behind `origin/main`. Do not blindly overwrite local files or force-push. Inspect differences and reconcile safely before merging or pushing.

## 3. Full roadmap and Issue ranges

| Milestone | Focus | Issue range |
| --- | --- | --- |
| M0 — Project Foundation | Project structure, MVP scope, workflow/CI | [#1–#3](https://github.com/emrelab/goshop/issues?q=M0-) |
| M1 — Product Catalog | Product/category, in-memory catalog, API, filters, templates | [#4–#9](https://github.com/emrelab/goshop/issues?q=M1-) |
| M2 — Inventory Management | PostgreSQL, migrations, `database/sql`, GORM comparison, stock | [#10–#15](https://github.com/emrelab/goshop/issues?q=M2-) |
| M3 — User Authentication | User accounts, password hashes, sessions, role checks | [#16–#21](https://github.com/emrelab/goshop/issues?q=M3-) |
| M4 — Shopping Cart | Cart rules, persistence, totals, endpoint/UI | [#22–#27](https://github.com/emrelab/goshop/issues?q=M4-) |
| M5 — Checkout & Orders | Orders, transactions, stock integrity, idempotent checkout | [#28–#33](https://github.com/emrelab/goshop/issues?q=M5-) |
| M6 — Storefront & Administration | Connected customer/admin pages | [#34–#39](https://github.com/emrelab/goshop/issues?q=M6-) |
| M7 — Testing & Release | Tests, security, Docker, optional labs, documentation | [#40–#45](https://github.com/emrelab/goshop/issues?q=M7-) |

**Next suggested task if there is no newer verified progress:** [#1 — Initialize GoShop project structure](https://github.com/emrelab/goshop/issues/1). Review local files first to avoid duplicating work.

## 4. Technical decisions and guardrails

1. **Optimize for learning.** Use small, understandable functions and packages. Explain the Go concept used in each task.
2. **One Issue at a time.** Select a small, relevant Issue; do not jump ahead into future milestone implementations.
3. **Use simple tools first.** Start with Go standard library and in-memory data; introduce database, GORM and external services only in their respective milestones.
4. **Keep business logic separate from transport and storage** only where it clarifies code; do not invent a complex layered architecture prematurely.
5. **Server is authoritative** for prices, totals, users and stock. Use integer minor units for money, transactional checkout, and enforce ownership.
6. **No real payment or delivery provider.** Checkout is a simulation for learning.
7. **Test incrementally.** Choose small unit tests and targeted integration tests as functionality arrives; M7 is a final audit, not the first time tests are written.
8. **Advanced topics** (goroutines/channels, Redis, MongoDB, TCP/UDP, design patterns, security/protocol comparisons) can be implemented as **small optional labs or notes**, not required services in the core runtime.
9. **No broad unilateral changes.** If acting as an AI agent, first analyze and explain proposed edits, and seek user's approval for repository mutations. Never silently alter/close Issues or rewrite branch history.

## 5. Recommended lightweight workflow

1. Inspect the repository, local checkout, [Issues](https://github.com/emrelab/goshop/issues) and [Milestones](https://github.com/emrelab/goshop/milestones).
2. Identify a single uncompleted Issue and any unmet prerequisite.
3. Set its board status to **In Progress** when work actually begins (if board access exists).
4. Make the smallest implementation; explain decisions and run relevant tests.
5. Commit/push changes using an appropriate branch/PR workflow once agreed with the user.
6. Link commit/PR/test evidence in the Issue; mark **Done** and close the Issue only after acceptance criteria are satisfied.

Use `Todo → In Progress → Done` as the board convention. GitHub Projects board cards and workflow statuses are separate from repository Issue metadata.

## 6. Documentation and course source notes

- [README](../README.md): purpose and roadmap.
- [Course Coverage](COURSE_COVERAGE.md): map of **16 available lessons** to application features, labs and discussion topics.
- The lesson reports are user-provided summaries of 2021 Go course recordings; the full original reports are **not guaranteed to be stored in this repository**.
- There is **no Lesson 10 report** among the provided material; do not invent its contents.
- The course coverage matrix tracks **planned learning evidence**, not automatically completed lessons.

## 7. Questions to resolve only when relevant

- Which current local files are implemented and already tracked?
- Are all 45 Issues present in **GoShop Development** and do status/priority fields reflect real progress?
- Should optional labs be separate runnable examples or concise research notes?
- Which database access approach is preferred after comparing raw SQL and GORM?

If unsure, report uncertainty rather than guessing. Preserve the beginner-friendly scope.
