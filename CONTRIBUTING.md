# Contributing to Cerid AI

Thank you for your interest in contributing. This document covers the process for all repositories under the Cerid AI organization.

---

## Before You Start

- Check the existing issues and pull requests to avoid duplicate work.
- For significant changes, open an issue first to discuss the approach.
- Review the `CLAUDE.md` in each repo for AI-assisted development conventions.

---

## Development Setup

Each repository has its own setup instructions in its `README.md`. General requirements:

- **Python repos:** Python 3.11+, Docker & Docker Compose v2+
- **Frontend:** Node 22+, see `.nvmrc` in each package
- **Secrets:** Use the repo's `.env.example` as a template; never commit `.env` files

---

## Pull Request Process

1. Fork the repo and create a branch from `main`.
2. Follow the existing code style — each repo uses `ruff` for Python, `eslint`/`prettier` for TypeScript.
3. Add or update tests to cover your changes.
4. Ensure all CI checks pass before requesting review.
5. Fill out the pull request template completely.
6. PRs that break tests or skip the template will not be merged.

---

## Code Standards

### Python
```bash
make lint       # ruff check
make typecheck  # mypy strict
make test       # pytest
```

### TypeScript / React
```bash
npm run lint
npm run typecheck
npm run test
```

---

## Commit Messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add new MCP tool for knowledge graph traversal
fix: correct VPIN calculation on empty orderbook
docs: update quick start instructions
refactor: split ingestion router into service layer
test: add hallucination agent edge case coverage
```

---

## Security

Do not open public issues for security vulnerabilities. See [SECURITY.md](SECURITY.md) for the responsible disclosure process.

---

## License

By contributing, you agree that your contributions will be licensed under the same license as the repository you are contributing to (Apache 2.0 for open repos; proprietary terms apply to closed repos).
