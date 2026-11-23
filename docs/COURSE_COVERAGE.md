# GoShop — Go Course Coverage Matrix

**Goal:** Preserve coverage of the **16 supplied Go course reports** (Lessons 1–9 and 11–17) while developing a small single-store e-commerce app **in product workflow order**.

> Every mapping below is **planned**, not proof of implementation or mastery. Mark an item complete only after the linked feature, test, lab or explanation is actually reviewed. The user did not provide Lesson 10, so it is intentionally **not mapped**.

## Evidence types

- **Core:** implemented in the GoShop app.
- **Lab:** small runnable exercise, ideally under `labs/`, not a core dependency.
- **Note:** short explanation/comparison; appropriate for topics only briefly mentioned in a lesson.

## Lesson-by-lesson coverage

| Lesson | Topics in supplied report | Planned evidence and Issues | Type | Verified complete? |
| --- | --- | --- | --- | --- |
| **1** | Go motivation/ecosystem, standard formatting, `go run`/`go build`, main package, concurrency overview, backend use cases | Initialize module, run/build app and explain choice of Go: [#1](https://github.com/emrelab/goshop/issues/1), [#3](https://github.com/emrelab/goshop/issues/3); concurrency later [#43](https://github.com/emrelab/goshop/issues/43) | Core + Note | ☐ |
| **2** | Editor/debug tooling, packages/imports, variable declarations/types/scope, functions, custom types, testing intro | Organize minimal packages [#1](https://github.com/emrelab/goshop/issues/1), product types [#4](https://github.com/emrelab/goshop/issues/4), first tests [#5](https://github.com/emrelab/goshop/issues/5); Delve/debugger exercise to confirm separately | Core + Lab | ☐ |
| **3** | `if`, `switch`, `for`, `range`, array, slice, map, `make`, flow control | Sample catalog [#5](https://github.com/emrelab/goshop/issues/5), search/filter/pagination [#7](https://github.com/emrelab/goshop/issues/7), cart operations [#23](https://github.com/emrelab/goshop/issues/23); explicitly demonstrate arrays vs slices and `make` | Core + Lab | ☐ |
| **4** | Parameters/returns, anonymous functions, closures, `defer`, pointers, HTTP `Handler`/`HandlerFunc` | Product HTTP handlers [#6](https://github.com/emrelab/goshop/issues/6), database resource cleanup [#10](https://github.com/emrelab/goshop/issues/10), closure/callback lab [#43](https://github.com/emrelab/goshop/issues/43) | Core + Lab | ☐ |
| **5** | Structs, methods/receivers, constructors, modules/packages, embedding/composition, interfaces/polymorphism | Product/category model [#4](https://github.com/emrelab/goshop/issues/4), in-memory catalog interface [#5](https://github.com/emrelab/goshop/issues/5), factory example [#43](https://github.com/emrelab/goshop/issues/43) | Core + Lab | ☐ |
| **6** | Interface/composition revision, JSON marshal/bytes, Fiber/framework tradeoffs, ORM/GORM concepts | Repository interface [#5](https://github.com/emrelab/goshop/issues/5), JSON API [#6](https://github.com/emrelab/goshop/issues/6), framework comparison [#9](https://github.com/emrelab/goshop/issues/9), GORM comparison [#13](https://github.com/emrelab/goshop/issues/13) | Core + Note | ☐ |
| **7** | XML/HTML/JSON, YAML/Dockerfile and data exchange formats | HTML product list [#8](https://github.com/emrelab/goshop/issues/8), JSON/XML serialization and YAML note [#9](https://github.com/emrelab/goshop/issues/9), Docker Compose [#42](https://github.com/emrelab/goshop/issues/42) | Core + Lab + Note | ☐ |
| **8** | SQL, DB drivers, connections, configuration, queries, transactions and injection safety | PostgreSQL connection [#10](https://github.com/emrelab/goshop/issues/10), migrations [#11](https://github.com/emrelab/goshop/issues/11), `database/sql` CRUD [#12](https://github.com/emrelab/goshop/issues/12), transaction tests [#15](https://github.com/emrelab/goshop/issues/15) | Core | ☐ |
| **9** | GORM/ORM model mapping, CRUD, SQL vs ORM, transaction | Product CRUD [#12](https://github.com/emrelab/goshop/issues/12), comparison [#13](https://github.com/emrelab/goshop/issues/13), validation/inventory [#14](https://github.com/emrelab/goshop/issues/14), checkout transaction [#29](https://github.com/emrelab/goshop/issues/29) | Core + Lab | ☐ |
| **11** | `html/template` vs `text/template`, handlers, view models, file/template loading | Product listing [#8](https://github.com/emrelab/goshop/issues/8), auth pages [#20](https://github.com/emrelab/goshop/issues/20), common layout [#34](https://github.com/emrelab/goshop/issues/34) | Core + Note | ☐ |
| **12** | Client/server architecture, TCP/UDP, `net/http`, headers/status, CORS/HSTS/CSRF, HTTP/3/QUIC | HTTP server [#6](https://github.com/emrelab/goshop/issues/6), session/security tests [#21](https://github.com/emrelab/goshop/issues/21), security review [#41](https://github.com/emrelab/goshop/issues/41), TCP/UDP and protocol note [#44](https://github.com/emrelab/goshop/issues/44) | Core + Lab + Note | ☐ |
| **13** | Register GET/POST, connection/request handling, Book API as example, JSON success/error body, status codes, ID parsing | Product API and error responses [#6](https://github.com/emrelab/goshop/issues/6), registration [#17](https://github.com/emrelab/goshop/issues/17), orders API [#30](https://github.com/emrelab/goshop/issues/30) | Core | ☐ |
| **14** | Repository pattern, JSON decode, validation, CRUD, transaction, uniform error body | SQL repository [#12](https://github.com/emrelab/goshop/issues/12), admin validation [#14](https://github.com/emrelab/goshop/issues/14), transactional checkout [#29](https://github.com/emrelab/goshop/issues/29), order API [#30](https://github.com/emrelab/goshop/issues/30) | Core | ☐ |
| **15** | Stateless HTTP, cookies, sessions, login/password forms, `SetCookie`, server-side session store | Login/logout [#18](https://github.com/emrelab/goshop/issues/18), middleware [#19](https://github.com/emrelab/goshop/issues/19), HTML forms [#20](https://github.com/emrelab/goshop/issues/20), session testing [#21](https://github.com/emrelab/goshop/issues/21) | Core | ☐ |
| **16** | NoSQL types, MongoDB collections/documents, Redis caching, Cassandra comparison, drivers, scaling | Independent Redis/MongoDB experiments, driver/SQL vs NoSQL comparison and scaling note [#44](https://github.com/emrelab/goshop/issues/44) | Lab + Note | ☐ |
| **17** | Builder/factory patterns, goroutine, channel, `select`, callback, context, `testing`, Testify, Ginkgo/Gomega, BDD, security | Notification worker/pattern lab [#43](https://github.com/emrelab/goshop/issues/43), automated tests [#40](https://github.com/emrelab/goshop/issues/40), security [#41](https://github.com/emrelab/goshop/issues/41), library/BDD comparison [#45](https://github.com/emrelab/goshop/issues/45) | Core + Lab + Note | ☐ |

**Lesson 10:** No report supplied. Do not infer course contents.

## Explicit topic checks before declaring course coverage complete

Some specific class concepts could be easy to overlook even if the feature works. Confirm them during the linked Issues or in a small lab:

- [ ] `go run`, `go build`, `gofmt`, modules/packages, scope, named/custom types and basic Delve debugging.
- [ ] Array vs slice; `map`, `make`, `for`/`range`, `if`/`switch`.
- [ ] Function vs method, pointer receiver, constructor-style function, interface, embedding/composition.
- [ ] Anonymous functions, closures, callbacks and `defer` for cleanup.
- [ ] JSON marshal/unmarshal and byte slices; compare HTML vs JSON vs XML vs YAML.
- [ ] HTTP request/response, method/status code/header, `Handler`/`HandlerFunc`, and safe error bodies.
- [ ] Raw SQL vs ORM/GORM, driver, connection pooling, `context`, transaction/rollback, SQL injection prevention.
- [ ] HTML templates, view models, cookie/session, role authorization, CSRF/CORS/HSTS basics.
- [ ] Goroutines, channels, `select`, context cancellation, factory/builder, Go `testing` and BDD tool comparison.
- [ ] Redis vs MongoDB vs relational storage; TCP vs UDP; HTTP versions/QUIC, gRPC, Kafka and Kubernetes as short **concept notes only** where appropriate.

## How to keep this accurate

1. For each lesson, link to a working implementation, test, runnable lab or reviewed note.
2. Check an item only when demonstrated. A planned Issue is **not** learning evidence.
3. Prefer a small illustrative lab rather than adding an unrelated service to the main app.
4. Update mappings if Issues change, and record any topic that could not be verified from the original report.
5. The underlying course reports were provided in chat and may not exist in this GitHub repository; this file is a traceability map, not a replacement for those sources.

**Final coverage review:** [#45 — Finalize documentation, learning coverage and release checklist](https://github.com/emrelab/goshop/issues/45).
