# Getting Started

Set up a development environment for llmoxie-analysis and run the project's
checks.

## Prerequisites

This project uses [Pixi](https://pixi.sh) for dependency management and task
execution. It is the only package manager used here. Install it by following the
[installation instructions](https://pixi.sh/latest/#installation).

Supported platforms are `osx-arm64`, `linux-64`, and `linux-aarch64`.

## Install

Clone the repository, then create the environment:

```bash
git clone https://github.com/uw-ssec/llmoxie-analysis.git
cd llmoxie-analysis
pixi install
```

`pixi install` creates the `default` environment, which includes Python, the
development tools (pytest, ruff, pre-commit, build, hatchling), the
documentation tooling (MkDocs with Material), and `llmoxie-analysis` itself as
an editable install.

Confirm the package imports:

```bash
pixi run python -c "import llmoxie_analysis; print(llmoxie_analysis.__version__)"
```

## Common tasks

| Task                  | Command                   |
| --------------------- | ------------------------- |
| Run the test suite    | `pixi run test`           |
| Lint and check format | `pixi run lint`           |
| Build wheel and sdist | `pixi run build`          |
| Run pre-commit hooks  | `pixi run pre-commit-all` |
| Run the quality gate  | `pixi run verify`         |
| Preview these docs    | `pixi run docs-serve`     |
| Build these docs      | `pixi run docs-build`     |

Run `pixi task list` to see every available task with its description.

Run `pixi run verify` before committing or opening a pull request. It runs every
pre-commit hook on all files, then the test suite, and must exit with status 0.

## Preview the docs

```bash
pixi run docs-serve    # live reload at http://127.0.0.1:8000
pixi run docs-build    # build into site/, failing on any warning
```
