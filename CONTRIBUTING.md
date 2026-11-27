# Contributing to GoShop

GoShop is a learning-oriented project that prioritizes simplicity, maintainability, and incremental development.

## 1. Development Principles

- Work on one GitHub issue at a time.
- Keep changes small and focused.
- Prefer simple and readable Go code.
- Avoid unnecessary dependencies and abstractions.
- Follow the project roadmap and MVP scope.
- Verify changes before committing.

## 2. Branch Naming

Use descriptive branch names with the following prefixes:

| Prefix | Purpose |
| --- | --- |
| `feat/` | New features |
| `fix/` | Bug fixes |
| `docs/` | Documentation |
| `test/` | Tests |
| `refactor/` | Code improvements |
| `ci/` | CI and automation |
| `chore/` | Maintenance |

Example: `feat/product-catalog`

## 3. Commit Messages

Follow the Conventional Commits approach.

Format: `type: short description`

Examples:

- `feat: add product model`
- `fix: prevent negative stock`
- `docs: update README`
- `test: add catalog tests`
- `ci: configure GitHub Actions`

Write commit messages in English. Reference the related GitHub issue when appropriate.

## 4. Development Workflow

1. Select a GitHub issue.
2. Move the issue to In Progress.
3. Create a branch from the latest main branch.
4. Implement the required changes.
5. Review the changes locally.
6. Run local validation checks.
7. Commit and push the changes.
8. Open a pull request.
9. Verify CI results and review the changes.
10. Merge the pull request.
11. Close the related issue and move it to Done.

## 5. Local Validation

Run the following commands before committing code:

- `go fmt ./...`
- `go build ./...`
- `go test ./...`
- `go vet ./...`
- `git diff --cached --check` after staging changes.

Use the Go version specified in `go.mod`.

## 6. Pull Requests

Every pull request should:

- Reference the related issue.
- Describe the purpose of the changes.
- Explain how the changes were verified.
- Include focused and relevant changes.
- Pass all required CI checks.

Do not merge pull requests with failing CI checks.

## 7. Security

- Never commit passwords, API keys, or access tokens.
- Never commit real `.env` files.
- Use `.env.example` for example configuration.
- Do not commit compiled binaries or unnecessary generated files.
- Review staged changes before committing.

## 8. Project Documentation

Keep the project documentation consistent with the implementation.

- [Project README](README.md)
- [Project Context](docs/PROJECT_CONTEXT.md)
- [MVP Scope](docs/MVP_SCOPE.md)
- [Course Coverage](docs/COURSE_COVERAGE.md)