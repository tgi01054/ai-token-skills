# Repository Guidelines

## Project Structure

This repository collects token and context management tools under `vendor/` as Git submodules. Keep repository-level documentation at the root. Do not modify files inside a vendor submodule unless the task explicitly targets that upstream project.

The expected layout is:

```text
vendor/
  ponytail/
  caveman/
  rtk/
  headroom/
  context-mode/
  serena/
  token-optimizer/
```

## Build, Test, and Development Commands

There is no root build system or test runner. Run checks from the relevant submodule directory and follow that project’s own documentation. To initialize the configured submodules, run:

```sh
git submodule update --init --recursive
```

Do not claim that a command works until its configuration exists.

## Coding Style and Naming

Use the language’s standard formatter and keep formatting changes separate from behavior changes. Use two spaces for JSON, YAML, and JavaScript unless the project adds a formatter with a different rule. Name directories and non-class files with lowercase kebab-case, such as `token-parser/`. Use `PascalCase` for classes and `camelCase` for functions, variables, and JavaScript modules.

## Testing Guidelines

Add tests for new behavior and regressions under `tests/`, mirroring the relevant `src/` path. Use descriptive names that state the behavior under test, such as `parses_expired_token`. Keep tests deterministic and independent. Add coverage requirements when the project adopts a test framework.

## Commits and Pull Requests

No Git history is available yet, so no repository-specific commit convention can be inferred. Use short imperative commit subjects, such as `Add token parser`, and keep each commit focused. Pull requests should explain the user-visible change, list validation commands and results, link the related issue when one exists, and include screenshots for visual changes.

## Security and Configuration

Never commit tokens, credentials, private keys, or machine-specific configuration. Provide safe example configuration with placeholder values, and document required environment variables without recording their secrets.
