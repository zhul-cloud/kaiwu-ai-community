# Repository Guidelines

## Project Structure & Module Organization

This repository is currently an empty project scaffold: no source, test, or build directories exist yet. As the project grows, keep the layout predictable:

- `src/` — production code, organized by feature or domain.
- `tests/` — automated tests mirroring the `src/` structure.
- `assets/` — static images, fixtures, and other non-code resources.
- `docs/` — design notes and user or contributor documentation.

Keep reusable modules focused and avoid placing application logic in test or asset directories.

## Build, Test, and Development Commands

No build tool or package manager is configured yet. When one is introduced, document the canonical commands here and keep them runnable from the repository root. A typical command set is:

```sh
<package-manager> install   # install dependencies
<package-manager> run dev   # start local development
<package-manager> test      # run the full test suite
<package-manager> run build # create a production build
```

Prefer repository scripts over ad-hoc command sequences so local and CI workflows stay consistent.

## Coding Style & Naming Conventions

Use the formatter and linter selected by the project; commit their configuration with the code. Use two-space indentation unless the language ecosystem requires another standard. Name directories and files with lowercase `kebab-case`, types and classes with `PascalCase`, and functions, variables, and test cases with `camelCase`. Keep public APIs documented and avoid unrelated formatting changes.

## Testing Guidelines

Add tests under `tests/` with paths that mirror the code under test. Use descriptive names such as `tests/auth/login.test.*`, and cover normal, error, and boundary behavior. Run the complete suite before opening a pull request; add coverage checks once a test framework and CI pipeline are established.

## Commit & Pull Request Guidelines

There is no Git history yet, so no existing commit convention can be inferred. Use short, imperative commit subjects (for example, `Add project scaffold` or `Fix login validation`) and keep each commit focused. Pull requests should explain the change, include verification steps and relevant issue links, and attach screenshots or sample output for user-facing changes. Keep generated files and secrets out of commits.

## Security & Configuration

Never commit credentials, tokens, private keys, or local environment files. Provide a sanitized `.env.example` when configuration is needed, and document required variables and safe local setup in `docs/`.
