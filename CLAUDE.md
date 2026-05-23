# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working in this repository.

---

## Project Overview

<!-- TODO: Describe what this project does, its purpose, and target users. -->
<!-- Example: "wbtc_iri is a ..." -->

**Repository:** `roemu90/wbtc_iri`
**Primary language:** <!-- e.g. Python / TypeScript / Rust / Go -->
**Framework / runtime:** <!-- e.g. FastAPI, Next.js, Axum, gin -->

---

## Repository Structure

```
wbtc_iri/
├── CLAUDE.md          # This file
├── README.md          # (to be added)
├── src/               # Main source code
├── tests/             # Test suite
├── docs/              # Documentation
└── ...
```

<!-- TODO: Update the tree above once directories are created. Briefly describe each key directory's role. -->

---

## Development Setup

### Prerequisites

<!-- List required tools, versions, and how to install them. -->
<!-- Example:
- Python >= 3.11
- Node.js >= 20
- Docker (optional, for containerised dev)
-->

### First-time setup

```bash
# Clone and enter the repo
git clone https://github.com/roemu90/wbtc_iri.git
cd wbtc_iri

# TODO: add install / bootstrap steps
# e.g. pip install -e ".[dev]"  or  npm install
```

### Environment variables

<!-- List required and optional env vars with descriptions. -->
<!-- Example:
| Variable      | Required | Description                        |
|---------------|----------|------------------------------------|
| DATABASE_URL  | yes      | Postgres connection string         |
| API_KEY       | yes      | External service API key           |
| LOG_LEVEL     | no       | Logging verbosity (default: INFO)  |
-->

Copy `.env.example` to `.env` and fill in values before running the project.

---

## Running the Project

```bash
# TODO: replace with actual run command(s)
# e.g.  python -m wbtc_iri
#       npm run dev
#       cargo run
```

---

## Testing

```bash
# Run the full test suite
# TODO: e.g.  pytest  /  npm test  /  cargo test

# Run a single test file / module
# TODO: e.g.  pytest tests/test_foo.py

# Run with coverage
# TODO: e.g.  pytest --cov=src
```

### Test conventions

- Test files live in `tests/` and mirror the `src/` structure.
- <!-- TODO: add any naming conventions (e.g. `test_*.py`, `*.spec.ts`) -->
- Tests must pass before merging to `main`.

---

## Code Style & Conventions

### Formatting / linting

```bash
# TODO: add lint and format commands
# e.g.  ruff check . && ruff format .
#       npm run lint
#       cargo fmt && cargo clippy
```

- <!-- TODO: note formatter, line-length, tab/space preference -->
- Auto-formatting should be run before every commit (consider a pre-commit hook).

### Naming conventions

<!-- Document key naming patterns used in this codebase. Examples: -->
- Files: `snake_case.py` / `kebab-case.ts`
- Classes: `PascalCase`
- Functions / variables: `snake_case` / `camelCase`
- Constants: `UPPER_SNAKE_CASE`

### Comments

- Write comments only when the **why** is non-obvious.
- Do not explain what the code does — well-named identifiers do that.

---

## Git Workflow

### Branches

| Branch pattern       | Purpose                             |
|----------------------|-------------------------------------|
| `main`               | Stable, production-ready code       |
| `feature/<name>`     | New features                        |
| `fix/<name>`         | Bug fixes                           |
| `claude/<task-slug>` | AI-assisted tasks (auto-created)    |

### Commit messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short summary>

[optional body]
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `ci`

### Pull requests

- Keep PRs focused — one concern per PR.
- Ensure all tests pass and linting is clean before requesting review.
- PRs to `main` require at least one approval.

---

## Architecture & Key Concepts

<!-- TODO: Describe the high-level architecture, major components, and how they interact.
     Include diagrams (Mermaid) if helpful. -->

---

## External Services & Dependencies

<!-- TODO: List external APIs, databases, message queues, or cloud services used.
     Include links to docs where relevant.
     Example:
     - PostgreSQL — primary datastore
     - Redis — caching and job queue
     - CoinGecko API — price feed for WBTC
-->

---

## CI / CD

<!-- TODO: Describe the CI pipeline (GitHub Actions, etc.) and deployment process.
     Example:
     - `.github/workflows/ci.yml` — runs tests and linting on every PR
     - Merges to `main` trigger automatic deployment to staging
-->

---

## AI Assistant Guidelines

When working in this repository, follow these rules:

1. **Read before editing** — always read a file before modifying it.
2. **Minimal changes** — fix only what the task requires; avoid scope creep.
3. **No speculative code** — don't add error handling, abstractions, or features beyond the stated task.
4. **No unnecessary comments** — only comment when the *why* is non-obvious.
5. **Run tests** — after any code change, run the test suite and confirm it passes before reporting done.
6. **Lint clean** — ensure linting passes before committing.
7. **Commit to feature branch** — never push directly to `main`.
8. **Confirm before destructive actions** — ask before deleting files, dropping data, or force-pushing.
